---
title: 將 Azure PowerShell 解除安裝
description: 如何執行 Azure PowerShell 完全解除安裝
ms.date: 06/10/2019
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 58d861f09eef04638cfa7e784ef0e28e9f4751d4
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "89244257"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="d4266-103">將 Azure PowerShell 模組解除安裝</span><span class="sxs-lookup"><span data-stu-id="d4266-103">Uninstall the Azure PowerShell module</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="d4266-104">本文說明如何將較舊版的 Azure PowerShell 解除安裝，或從您的系統將它完全移除。</span><span class="sxs-lookup"><span data-stu-id="d4266-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="d4266-105">如果您已決定要將 Azure PowerShell 完全解除安裝，請透過 [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) Cmdlet 提供意見反應給我們。</span><span class="sxs-lookup"><span data-stu-id="d4266-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="d4266-106">如果發生錯誤 (bug)，希望您[提出 GitHub 問題](https://github.com/azure/azure-powershell/issues)，非常感謝您。</span><span class="sxs-lookup"><span data-stu-id="d4266-106">If you encounter a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>


## <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="d4266-107">解除安裝 Azure PowerShell MSI</span><span class="sxs-lookup"><span data-stu-id="d4266-107">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="d4266-108">如果您使用 MSI 套件安裝 Azure PowerShell，則必須透過 Windows 系統而非 PowerShell 來解除安裝。</span><span class="sxs-lookup"><span data-stu-id="d4266-108">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="d4266-109">平台</span><span class="sxs-lookup"><span data-stu-id="d4266-109">Platform</span></span> | <span data-ttu-id="d4266-110">Instructions</span><span class="sxs-lookup"><span data-stu-id="d4266-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="d4266-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="d4266-111">Windows 10</span></span> | <span data-ttu-id="d4266-112">[開始] > [設定] > [應用程式]</span><span class="sxs-lookup"><span data-stu-id="d4266-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="d4266-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d4266-113">Windows 7</span></span> </br><span data-ttu-id="d4266-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d4266-114">Windows 8</span></span> | <span data-ttu-id="d4266-115">[啟動] > [控制台] -> [程式集] -> [解除安裝程式]</span><span class="sxs-lookup"><span data-stu-id="d4266-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="d4266-116">您在此畫面上應該會看到程式清單中的 __Azure PowerShell__。</span><span class="sxs-lookup"><span data-stu-id="d4266-116">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="d4266-117">這是要解除安裝的應用程式。</span><span class="sxs-lookup"><span data-stu-id="d4266-117">This is the app to uninstall.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="d4266-118">從 PowerShell 解除安裝</span><span class="sxs-lookup"><span data-stu-id="d4266-118">Uninstall from PowerShell</span></span>

<span data-ttu-id="d4266-119">如果您使用 PowerShellGet 安裝 Azure PowerShell，則可以使用 [Uninstall-Module](/powershell/module/powershellget/uninstall-module) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d4266-119">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="d4266-120">不過，`Uninstall-Module` 只會解除安裝一個模組。</span><span class="sxs-lookup"><span data-stu-id="d4266-120">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="d4266-121">若要完全移除 Azure PowerShell，您必須個別將每個模組解除安裝。</span><span class="sxs-lookup"><span data-stu-id="d4266-121">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="d4266-122">如果您安裝了多個版本的 Azure PowerShell，則解除安裝可能會很複雜。</span><span class="sxs-lookup"><span data-stu-id="d4266-122">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="d4266-123">若要檢查您目前安裝的 Azure PowerShell 版本，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="d4266-123">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

```output
Version              Name                                Repository           Description
-------              ----                                ----------           -----------
6.11.0               AzureRM                             PSGallery            Azure Resource Manager Module
6.13.1               AzureRM                             PSGallery            Azure Resource Manager Module
```

<span data-ttu-id="d4266-124">下列指令碼會查詢 PowerShell 資源庫來取得相依子模組的清單。</span><span class="sxs-lookup"><span data-stu-id="d4266-124">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="d4266-125">然後，指令碼會將每個子模組的正確版本解除安裝。</span><span class="sxs-lookup"><span data-stu-id="d4266-125">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="d4266-126">您需要擁有系統管理員權限，才能在 `Process` 或 `CurrentUser`以外的範圍執行此指令碼。</span><span class="sxs-lookup"><span data-stu-id="d4266-126">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

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

<span data-ttu-id="d4266-127">若要使用此函式，請複製程式碼，然後貼到您的 PowerShell 工作階段。</span><span class="sxs-lookup"><span data-stu-id="d4266-127">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="d4266-128">下列範例示範如何執行函式，以將舊版的 Azure PowerShell 移除。</span><span class="sxs-lookup"><span data-stu-id="d4266-128">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="d4266-129">指令碼在執行時，會顯示要解除安裝的每個子模組名稱及版本。</span><span class="sxs-lookup"><span data-stu-id="d4266-129">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="d4266-130">若只想執行指令碼以查看會刪除的項目，而不要真正移除項目，請使用 `-WhatIf` 選項。</span><span class="sxs-lookup"><span data-stu-id="d4266-130">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

> [!NOTE]
> <span data-ttu-id="d4266-131">若此指令碼與要解除安裝之相同版本的相依性不完全相符，系統不會解除安裝該相依性的_任何_版本。</span><span class="sxs-lookup"><span data-stu-id="d4266-131">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependecy.</span></span> <span data-ttu-id="d4266-132">這是因為您的系統上可能有其他版本的目標模組需要使用這些相依性。</span><span class="sxs-lookup"><span data-stu-id="d4266-132">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span> <span data-ttu-id="d4266-133">在此情況下，會列出可用的相依性版本。</span><span class="sxs-lookup"><span data-stu-id="d4266-133">In this case, the available versions of the dependency are listed.</span></span>
> <span data-ttu-id="d4266-134">然後您就可以使用 `Uninstall-Module` 手動移除任何舊版本。</span><span class="sxs-lookup"><span data-stu-id="d4266-134">You can then remove any old versions manually with `Uninstall-Module`.</span></span>


<span data-ttu-id="d4266-135">請針對您要解除安裝的 Azure PowerShell 每個版本執行此命令。</span><span class="sxs-lookup"><span data-stu-id="d4266-135">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="d4266-136">為了方便起見，下列指令碼會將所有版本的 AzureRM 解除安裝，__只留下__最新版本。</span><span class="sxs-lookup"><span data-stu-id="d4266-136">For convenience, the following script will uninstall all versions of AzureRM __except__ for the latest.</span></span>

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
