---
title: 將 Azure PowerShell 解除安裝
description: 如何執行 Azure PowerShell 完全解除安裝
ms.date: 06/20/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 92af0fdd8db451e2f0f092d66a3e296ad8d6a09e
ms.sourcegitcommit: f648ac92fafb16cc0e9ca6bc85d00fa327baf396
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/28/2018
ms.locfileid: "43018615"
---
# <a name="uninstall-the-azure-powershell-module"></a>將 Azure PowerShell 模組解除安裝

本文說明如何將較舊版的 Azure PowerShell 解除安裝，或從您的系統將它完全移除。 如果您已決定要將 Azure PowerShell 完全解除安裝，請透過 [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) Cmdlet 提供一些意見反應給我們。
如果發生錯誤 (bug)，希望您[提出 GitHub 問題](https://github.com/azure/azure-powershell/issues)，非常感謝您。

## <a name="uninstall-msi"></a>解除安裝 MSI

如果您使用 MSI 套件安裝 Azure PowerShell，則必須透過 Windows 系統而非 PowerShell 來解除安裝。

| 平台 | 範例的指示 |
|----------|--------------|
| Windows 10 | [開始] > [設定] > [應用程式] |
| Windows 7 </br>Windows 8 | [開啟] > [控制台] > [程式] > [解除安裝程式] |

您在此畫面上應該會看到程式清單中的 "Azure PowerShell"，並可從該處解除安裝。

## <a name="uninstall-from-powershell"></a>從 PowerShell 解除安裝

如果您使用 PowerShellGet 安裝 Azure PowerShell，則可以使用 [Uninstall-Module](/powershell/module/powershellget/uninstall-module) Cmdlet。 不過，`Uninstall-Module` 只會解除安裝一個模組。 若要完全移除 Azure PowerShell，您必須個別將每個模組解除安裝。 如果您安裝了多個版本的 Azure PowerShell，則解除安裝可能會很複雜。

下列指令碼可用來將單一版本的 Azure PowerShell 完全移除。 指令碼會查詢 PowerShell 資源庫來取得相依子模組的清單。 然後，指令碼會將每個子模組的正確版本解除安裝。

```powershell
function Uninstall-AllModules {
  param(
    [Parameter(Mandatory=$true)]
    [string]$TargetModule,

    [Parameter(Mandatory=$true)]
    [string]$Version,

    [switch]$Force
  )

  $AllModules = @()

  'Creating list of dependencies...'
  $target = Find-Module $TargetModule -RequiredVersion $version
  $target.Dependencies | ForEach-Object {
    $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredversion}
  }
  $AllModules += New-Object -TypeName psobject -Property @{name=$TargetModule; version=$Version}

  foreach ($module in $AllModules) {
    Write-Host ('Uninstalling {0} version {1}' -f $module.name,$module.version)
    try {
      Uninstall-Module -Name $module.name -RequiredVersion $module.version -Force:$Force -ErrorAction Stop
    } catch {
      Write-Host ("`t" + $_.Exception.Message)
    }
  }
}
```

若要使用此函式，請複製程式碼，然後貼到您的 PowerShell 工作階段。 下列範例示範如何執行函式，以將舊版的 Azure PowerShell 移除。

```powershell
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

指令碼在執行時，會顯示要解除安裝的每個子模組名稱及版本。

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

請針對您要解除安裝的 Azure PowerShell 每個版本執行此命令。
