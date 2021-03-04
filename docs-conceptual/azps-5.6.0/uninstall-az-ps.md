---
title: 將 Azure PowerShell 解除安裝
description: 如何執行 Azure PowerShell 完全解除安裝
ms.date: 09/15/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: ec4ecc9902f700e12ce6b22c32b4e07b13b4d4dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101881800"
---
# <a name="how-to-uninstall-azure-powershell-modules"></a>如何解除安裝 Azure PowerShell 模組

本文說明如何將較舊版的 Azure PowerShell 解除安裝，或從您的系統將它完全移除。 如果您已決定要將 Azure PowerShell 完全解除安裝，請透過 [Send-Feedback](/powershell/module/az.accounts/send-feedback) Cmdlet 提供意見反應給我們。 如果發生錯誤 (bug)，希望您[提出 GitHub 問題](https://github.com/azure/azure-powershell/issues)加以解決，非常感謝您。

## <a name="uninstall-the-az-module"></a>將 Az 模組解除安裝

如果您的系統上安裝了 Az 模組，而想要將其解除安裝，有兩個選項。 您要遵循哪個方法取決於安裝 Az 模組的方式。 如果您不確定原始安裝方法，請先依照 MSI 的步驟解除安裝。

### <a name="option-1-uninstall-the-az-powershell-module-from-msi"></a>選項 1：透過 MSI 解除安裝 Az PowerShell 模組

如果您使用 MSI 套件安裝 Az PowerShell 模組，則必須透過 Windows 系統而非 PowerShell 來解除安裝。

|         平台         |                      Instructions                      |
| ------------------------ | ------------------------------------------------------ |
| Windows 10               | [開始] > [設定] > [應用程式]                                |
| Windows 7 </br>Windows 8 | [啟動] > [控制台] -> [程式集] -> [解除安裝程式] |

您在此畫面上應該會看到程式清單中的 **Azure PowerShell**。 這是要解除安裝的應用程式。 如果並未列出此程式，而您是透過 PowerShellGet 安裝，則應遵循下一組指示。

### <a name="option-2-uninstall-the-az-powershell-module-from-powershellget"></a>選項 2：透過 PowerShellGet 解除安裝 Az PowerShell 模組

若要將 Az 模組解除安裝，請使用 [Uninstall-Module](/powershell/module/powershellget/uninstall-module) Cmdlet。 不過，`Uninstall-Module` 只會解除安裝一個模組。 若要完全移除 Az PowerShell 模組，您必須個別將每個模組解除安裝。 如果您安裝了多個版本的 Azure PowerShell，則解除安裝可能會很複雜。

若要檢查您安裝的 Az PowerShell 模組版本，請執行下列命令：

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
3.8.0               Az                             PSGallery            Microsoft Azure PowerShell
4.1.0               Az                             PSGallery            Microsoft Azure PowerShell
```

下列指令碼會查詢 PowerShell 資源庫來取得相依子模組的清單。 然後，指令碼會將每個子模組的正確版本解除安裝。 您需要擁有系統管理員權限，才能在 **流程** 或 **目前使用者** 以外的範圍執行此指令碼。

```powershell-interactive
function Uninstall-AzModule {
  [CmdletBinding(SupportsShouldProcess)]
  param(
    [ValidateNotNullOrEmpty()]
    [ValidateSet('Az','AzureRM','Azure')]
    [string]$Name = 'Az',

    [Parameter(Mandatory)]
    [string]$Version,

    [switch]$AllowPrerelease
  )

  $Params = @{}

  if ($PSBoundParameters.AllowPrerelease) {
    $Params.AllowPrerelease = $true
  }

  $IsAdmin = ([Security.Principal.WindowsPrincipal] [Security.Principal.WindowsIdentity]::GetCurrent()).IsInRole([Security.Principal.WindowsBuiltInRole] 'Administrator')

  if (-not(Get-InstalledModule -Name $Name -RequiredVersion $Version -ErrorAction SilentlyContinue -OutVariable RootModule @Params)) {

    Write-Warning -Message "Uninstall aborted. $Name version $Version not found."

  } elseif (($RootModule.InstalledLocation -notlike "*$env:USERPROFILE*") -and ($IsAdmin -eq $false)) {

    Write-Warning -Message "Uninstall aborted. $Name version $Version exists in a system path. PowerShell must be run elevated as an admin to remove it."

  } elseif ((Get-Process -Name powershell, pwsh -OutVariable Sessions -ErrorAction SilentlyContinue).Count -gt 1) {

    Write-Warning -Message "Uninstall aborted. Please close all other PowerShell sessions before continuing. There are currently $($Sessions.Count) PowerShell sessions running."

  } else {
    Write-Verbose -Message 'Creating list of dependencies...'
    $target = Find-Module -Name $Name -RequiredVersion $Version @Params

    $AllModules = @([pscustomobject]@{
      Name = $Name
      Version = $Version
    })

    $AllModules += foreach ($dependency in $target.Dependencies) {
      switch ($dependency.keys) {
        {$_ -contains 'RequiredVersion'} {$UninstallVersion = $dependency.RequiredVersion; break}
        {$_ -contains 'MinimumVersion'} {$UninstallVersion = $dependency.MinimumVersion; break}
      }

      [pscustomobject]@{
        Name = $dependency.Name
        Version = $UninstallVersion
      }
    }

    [int]$i = 100 / $AllModules.Count

    foreach ($module in $AllModules) {
      Write-Progress -Activity 'Uninstallation in Progress' -Status "$i% Complete:" -PercentComplete $i
      $i++

      if (Get-InstalledModule -Name $module.Name -RequiredVersion $module.Version -ErrorAction SilentlyContinue @Params) {
        Write-Verbose -Message "Uninstalling $($module.Name) version $($module.Version)"

        Remove-Module -FullyQualifiedName @{ModuleName=$module.Name;ModuleVersion=$module.Version} -ErrorAction SilentlyContinue

        try {
          if ($PSCmdlet.ShouldProcess("$($module.Name) version $($module.Version)")) {
            Uninstall-Module -Name $module.Name -RequiredVersion $module.Version -Force -ErrorAction Stop @Params
          }
          $State = 'Uninstalled'
        } Catch {
          $State = 'Manual uninstall required'
          Write-Verbose -Message "$($module.Name) version: $($module.Version) may require manual uninstallation."
        }

      } else {
        $State = 'Not found'
        Write-Verbose -Message "$($module.Name) version: $($module.Version) not found."
      }

      if (-not $PSBoundParameters.WhatIf) {
        [pscustomobject]@{
          ModuleName = $module.Name
          Version = $module.Version
          State = $State
        }
      }

    }
  }
}
```

若要使用此函式，請複製程式碼，然後貼到您的 PowerShell 工作階段。 下列範例示範如何執行函式，以將舊版的 Az PowerShell 模組和其子模組移除。

```powershell-interactive
Uninstall-AzModule -Name Az -Version 1.8.0
```

指令碼在執行時，會顯示要解除安裝每個子模組的 **名稱**、**版本** 及 **狀態**。 若執行指令碼只是查看會刪除的項目，而不要真正移除項目，請指定 `-WhatIf` 參數。

```output
ModuleName              Version  State
----------              -------  -----
Az.Accounts             1.5.1    Not found
Az.Aks                  1.0.1    Uninstalled
Az.AnalysisServices     1.1.0    Uninstalled
Az.ApiManagement        1.0.0    Uninstalled
Az.ApplicationInsights  1.0.0    Uninstalled
...
```

> [!IMPORTANT]
> 若此指令碼與要解除安裝之相同版本的相依性不完全相符，系統不會解除安裝該相依性的 _任何_ 版本。 這是因為您的系統上可能有其他版本的目標模組需要使用這些相依性。

針對您要解除安裝的 Az PowerShell 模組每個版本執行下列範例。
為了方便起見，下列指令碼會將所有版本的 Az 解除安裝，**只留下** 最新版本。

```powershell-interactive
$Modules = Get-InstalledModule -Name Az -AllVersions |
    Sort-Object -Property Version -Descending |
        Select-Object -Skip 1
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```

## <a name="uninstall-the-azurerm-module"></a>將 AzureRM 模組解除安裝

如果您的系統上安裝了 Az 模組，並想要將 AzureRM 解除安裝，有兩個選項。 您要遵循哪個方法取決於您安裝 AzureRM 模組的方式。 如果您不確定原始安裝方法，請先依照 MSI 的步驟解除安裝。

### <a name="option-1-uninstall-the-azurerm-powershell-module-from-msi"></a>選項 1：透過 MSI 解除安裝 AzureRM PowerShell 模組

如果您使用 MSI 套件安裝 AzureRM PowerShell 模組，則必須透過 Windows 系統而非 PowerShell 來解除安裝。

|         平台         |                      Instructions                      |
| ------------------------ | ------------------------------------------------------ |
| Windows 10               | [開始] > [設定] > [應用程式]                                |
| Windows 7 </br>Windows 8 | [啟動] > [控制台] -> [程式集] -> [解除安裝程式] |

您在此畫面上應該會看到程式清單中的 **Azure PowerShell** 或 **Microsoft Azure PowerShell - 月份年份**。 這是要解除安裝的應用程式。 如果並未列出此程式，而您是透過 PowerShellGet 安裝，則應遵循下一組指示。

### <a name="option-2-uninstall-the-azurerm-powershell-module-from-powershellget"></a>選項 2：透過 PowerShellGet 解除安裝 AzureRM PowerShell 模組

如果透過 PowerShellGet 安裝了 AzureRM，您可以使用 [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) Cmdlet 移除模組，您可以在 `Az.Accounts` 模組中找到這個命令。

若要使用 `Az.Accounts` 模組，您必須安裝 Az 模組。  不支援同時安裝 AzureRM 和 Az 模組，但 Az 模組可以用來立即解除安裝 AzureRM 模組。  如果您尚未安裝 Az 模組，則可以使用下列命令來安裝 Az 模組並略過 AzureRM 模組警告訊息：

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

安裝 Az 模組之後，下列命令會從您的電腦移除 _所有_ AzureRM 模組。 此動作需要系統管理員權限。

```powershell-interactive
Uninstall-AzureRm
```
