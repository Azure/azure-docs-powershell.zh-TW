---
title: 將 Azure PowerShell 解除安裝
description: 如何執行 Azure PowerShell 完全解除安裝
ms.date: 06/10/2019
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 6fc8ff8af0355ab705007f5df81d2aba8444c266
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/14/2020
ms.locfileid: "83388001"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="e76fd-103">將 Azure PowerShell 模組解除安裝</span><span class="sxs-lookup"><span data-stu-id="e76fd-103">Uninstall the Azure PowerShell module</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="e76fd-104">本文說明如何將較舊版的 Azure PowerShell 解除安裝，或從您的系統將它完全移除。</span><span class="sxs-lookup"><span data-stu-id="e76fd-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="e76fd-105">如果您已決定要將 Azure PowerShell 完全解除安裝，請透過 [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) Cmdlet 提供一些意見反應給我們。</span><span class="sxs-lookup"><span data-stu-id="e76fd-105">If you've decided to completely uninstall the Azure PowerShell, please give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="e76fd-106">如果發生錯誤 (bug)，希望您[提出 GitHub 問題](https://github.com/azure/azure-powershell/issues)，非常感謝您。</span><span class="sxs-lookup"><span data-stu-id="e76fd-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-msi-or-web-platform-installer"></a><span data-ttu-id="e76fd-107">將 MSI 或 Web Platform Installer 解除安裝</span><span class="sxs-lookup"><span data-stu-id="e76fd-107">Uninstall MSI or Web Platform Installer</span></span>

<span data-ttu-id="e76fd-108">如果您使用 MSI 套件或 Web Platform Installer 來安裝 Azure PowerShell，則必須透過 Windows 系統而非 PowerShell 來解除安裝。</span><span class="sxs-lookup"><span data-stu-id="e76fd-108">If you installed Azure PowerShell using the MSI package or the Web Platform Installer, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="e76fd-109">平台</span><span class="sxs-lookup"><span data-stu-id="e76fd-109">Platform</span></span> | <span data-ttu-id="e76fd-110">Instructions</span><span class="sxs-lookup"><span data-stu-id="e76fd-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="e76fd-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="e76fd-111">Windows 10</span></span> | <span data-ttu-id="e76fd-112">[開始] > [設定] > [應用程式]</span><span class="sxs-lookup"><span data-stu-id="e76fd-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="e76fd-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e76fd-113">Windows 7</span></span> </br><span data-ttu-id="e76fd-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e76fd-114">Windows 8</span></span> | <span data-ttu-id="e76fd-115">[啟動] > [控制台] -> [程式集] -> [解除安裝程式]</span><span class="sxs-lookup"><span data-stu-id="e76fd-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="e76fd-116">您在此畫面上應該會看到程式清單中的 "Azure PowerShell"，並可從該處解除安裝。</span><span class="sxs-lookup"><span data-stu-id="e76fd-116">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="e76fd-117">從 PowerShell 解除安裝</span><span class="sxs-lookup"><span data-stu-id="e76fd-117">Uninstall from PowerShell</span></span>

<span data-ttu-id="e76fd-118">如果您使用 PowerShellGet 安裝 Azure PowerShell，則可以使用 [Uninstall-Module](/powershell/module/powershellget/uninstall-module) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e76fd-118">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="e76fd-119">不過，`Uninstall-Module` 只會解除安裝一個模組。</span><span class="sxs-lookup"><span data-stu-id="e76fd-119">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="e76fd-120">若要完全移除 Azure PowerShell，您必須個別將每個模組解除安裝。</span><span class="sxs-lookup"><span data-stu-id="e76fd-120">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="e76fd-121">如果您安裝了多個版本的 Azure PowerShell，則解除安裝可能會很複雜。</span><span class="sxs-lookup"><span data-stu-id="e76fd-121">Uninstallation can be complicated if you have multiple versions of Azure PowerShell installed.</span></span>

<span data-ttu-id="e76fd-122">請使用下列指令碼，可用來將單一版本的 Azure PowerShell 完全移除。</span><span class="sxs-lookup"><span data-stu-id="e76fd-122">You use the following script can be used to completely remove a single version of Azure PowerShell.</span></span> <span data-ttu-id="e76fd-123">指令碼會查詢 PowerShell 資源庫來取得相依子模組的清單。</span><span class="sxs-lookup"><span data-stu-id="e76fd-123">The script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="e76fd-124">然後，指令碼會將每個子模組的正確版本解除安裝。</span><span class="sxs-lookup"><span data-stu-id="e76fd-124">Then, the script uninstalls the correct version of each submodule.</span></span>

```powershell-interactive
function Uninstall-AllModules {
  param(
    [Parameter(Mandatory=$true)]
    [string]$TargetModule,

    [Parameter(Mandatory=$true)]
    [string]$Version,

    [switch]$Force,

    [switch]$WhatIf
  )
  
  $AllModules = @()
  
  'Creating list of dependencies...'
  $target = Find-Module $TargetModule -RequiredVersion $version
  $target.Dependencies | ForEach-Object {
    if ($_.PSObject.Properties.Name -contains 'requiredVersion') {
      $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredVersion}
    }
    else { # Assume minimum version
      # Minimum version actually reports the installed dependency
      # which is used, not the actual "minimum dependency." Check to
      # see if the requested version was installed as a dependency earlier.
      $candidate = Get-InstalledModule $_.name -RequiredVersion $version -ErrorAction Ignore
      if ($candidate) {
        $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$version}
      }
      else {
        $availableModules = Get-InstalledModule $_.name -AllVersions
        Write-Warning ("Could not find uninstall candidate for {0}:{1} - module may require manual uninstall. Available versions are: {2}" -f $_.name,$version,($availableModules.Version -join ', '))
      }
    }
  }
  $AllModules += New-Object -TypeName psobject -Property @{name=$TargetModule; version=$Version}

  foreach ($module in $AllModules) {
    Write-Host ('Uninstalling {0} version {1}...' -f $module.name,$module.version)
    try {
      Uninstall-Module -Name $module.name -RequiredVersion $module.version -Force:$Force -ErrorAction Stop -WhatIf:$WhatIf
    } catch {
      Write-Host ("`t" + $_.Exception.Message)
    }
  }
}
```

<span data-ttu-id="e76fd-125">若要使用此函式，請複製程式碼，然後貼到您的 PowerShell 工作階段。</span><span class="sxs-lookup"><span data-stu-id="e76fd-125">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="e76fd-126">下列範例示範如何執行函式，以將舊版的 Azure PowerShell 移除。</span><span class="sxs-lookup"><span data-stu-id="e76fd-126">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="e76fd-127">指令碼在執行時，會顯示要解除安裝的每個子模組名稱及版本。</span><span class="sxs-lookup"><span data-stu-id="e76fd-127">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="e76fd-128">若只想執行指令碼以查看會刪除的項目，而不要真正移除項目，請使用 `-WhatIf` 選項。</span><span class="sxs-lookup"><span data-stu-id="e76fd-128">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

> [!NOTE]
> <span data-ttu-id="e76fd-129">若此指令碼與要解除安裝之相同版本的相依性不完全相符，系統不會解除安裝該相依性的_任何_版本。</span><span class="sxs-lookup"><span data-stu-id="e76fd-129">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependecy.</span></span> <span data-ttu-id="e76fd-130">這是因為您的系統上可能有其他版本的目標模組需要使用這些相依性。</span><span class="sxs-lookup"><span data-stu-id="e76fd-130">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span> <span data-ttu-id="e76fd-131">在此情況下，會列出可用的相依性版本。</span><span class="sxs-lookup"><span data-stu-id="e76fd-131">In this case, the available versions of the dependency are listed.</span></span>
> <span data-ttu-id="e76fd-132">然後您就可以使用 `Uninstall-Module` 手動移除任何舊版本。</span><span class="sxs-lookup"><span data-stu-id="e76fd-132">You can then remove any old versions manually with `Uninstall-Module`.</span></span>


<span data-ttu-id="e76fd-133">請針對您要解除安裝的 Azure PowerShell 每個版本執行此命令。</span><span class="sxs-lookup"><span data-stu-id="e76fd-133">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="e76fd-134">為了方便起見，下列指令碼會將所有版本的 AzureRM 解除安裝，__只留下__最新版本。</span><span class="sxs-lookup"><span data-stu-id="e76fd-134">For convenience, the following script will uninstall all versions of AzureRM __except__ for the latest.</span></span>

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
