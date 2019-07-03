---
title: 將 Azure PowerShell 解除安裝
description: 如何執行 Azure PowerShell 完全解除安裝
ms.date: 05/10/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: b32547e9c3df0df7495d1631a43be6934e1f62dc
ms.sourcegitcommit: febbbd3f75c8dd1a296281d265289f015b6cb537
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/12/2019
ms.locfileid: "67037760"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="a5248-103">將 Azure PowerShell 模組解除安裝</span><span class="sxs-lookup"><span data-stu-id="a5248-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="a5248-104">本文說明如何將較舊版的 Azure PowerShell 解除安裝，或從您的系統將它完全移除。</span><span class="sxs-lookup"><span data-stu-id="a5248-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="a5248-105">如果您已決定要將 Azure PowerShell 完全解除安裝，請透過 [Send-Feedback](/powershell/module/az.accounts/send-feedback) Cmdlet 提供意見反應給我們。</span><span class="sxs-lookup"><span data-stu-id="a5248-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>
<span data-ttu-id="a5248-106">如果發生錯誤 (bug)，希望您[提出 GitHub 問題](https://github.com/azure/azure-powershell/issues)加以解決，非常感謝您。</span><span class="sxs-lookup"><span data-stu-id="a5248-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-the-az-module"></a><span data-ttu-id="a5248-107">將 Az 模組解除安裝</span><span class="sxs-lookup"><span data-stu-id="a5248-107">Uninstall the Az module</span></span>

<span data-ttu-id="a5248-108">若要將 Az 模組解除安裝，請使用 [Uninstall-module](/powershell/module/powershellget/uninstall-module) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a5248-108">To uninstall the Az modules, use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="a5248-109">不過，`Uninstall-Module` 只會解除安裝一個模組。</span><span class="sxs-lookup"><span data-stu-id="a5248-109">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="a5248-110">若要完全移除 Azure PowerShell，您必須個別將每個模組解除安裝。</span><span class="sxs-lookup"><span data-stu-id="a5248-110">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="a5248-111">如果您安裝了多個版本的 Azure PowerShell，則解除安裝可能會很複雜。</span><span class="sxs-lookup"><span data-stu-id="a5248-111">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="a5248-112">若要檢查您目前安裝的 Azure PowerShell 版本，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="a5248-112">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
0.7.0               Az                             PSGallery            Azure Resource Manager Module
1.0.0               Az                             PSGallery            Azure Resource Manager Module
```

<a name="uninstall-script"/>

<span data-ttu-id="a5248-113">下列指令碼會查詢 PowerShell 資源庫來取得相依子模組的清單。</span><span class="sxs-lookup"><span data-stu-id="a5248-113">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="a5248-114">然後，指令碼會將每個子模組的正確版本解除安裝。</span><span class="sxs-lookup"><span data-stu-id="a5248-114">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="a5248-115">您需要擁有系統管理員權限，才能在 `Process` 或 `CurrentUser`以外的範圍執行此指令碼。</span><span class="sxs-lookup"><span data-stu-id="a5248-115">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

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

<span data-ttu-id="a5248-116">若要使用此函式，請複製程式碼，然後貼到您的 PowerShell 工作階段。</span><span class="sxs-lookup"><span data-stu-id="a5248-116">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="a5248-117">下列範例示範如何執行函式，以將舊版的 Azure PowerShell 移除。</span><span class="sxs-lookup"><span data-stu-id="a5248-117">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

<span data-ttu-id="a5248-118">指令碼在執行時，會顯示要解除安裝的每個子模組名稱及版本。</span><span class="sxs-lookup"><span data-stu-id="a5248-118">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="a5248-119">若只想執行指令碼以查看會刪除的項目，而不要真正移除項目，請使用 `-WhatIf` 選項。</span><span class="sxs-lookup"><span data-stu-id="a5248-119">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

> [!NOTE]
> <span data-ttu-id="a5248-120">若此指令碼與要解除安裝的相依模組版本不完全相符，系統不會解除安裝該模組的_任何_版本。</span><span class="sxs-lookup"><span data-stu-id="a5248-120">If this script can't match an exact dependent module version to uninstall, it won't uninstall _any_ version of that module.</span></span> <span data-ttu-id="a5248-121">這是因為您的系統上可能有其他版本的 `Az` 需要使用這些相依性。</span><span class="sxs-lookup"><span data-stu-id="a5248-121">This is because there may be other versions of `Az` on your system which rely on these modules.</span></span> <span data-ttu-id="a5248-122">在此情況下，若有任何已安裝的模組，系統會列出這些找不到的模組版本。</span><span class="sxs-lookup"><span data-stu-id="a5248-122">In this case, the versions of the module that couldn't be found will be listed, if any were installed.</span></span> <span data-ttu-id="a5248-123">然後您就可以使用 `Uninstall-Module` 手動移除任何舊版本。</span><span class="sxs-lookup"><span data-stu-id="a5248-123">You can then remove any old versions manually with `Uninstall-Module`.</span></span>

<span data-ttu-id="a5248-124">請針對您要解除安裝的 Azure PowerShell 每個版本執行此命令。</span><span class="sxs-lookup"><span data-stu-id="a5248-124">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="a5248-125">為了方便起見，下列指令碼會將所有版本的 Az 解除安裝，__只留下__最新版本。</span><span class="sxs-lookup"><span data-stu-id="a5248-125">For convenience, the following script will uninstall all versions of Az __except__ for the latest.</span></span>

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="a5248-126">將 AzureRM 模組解除安裝</span><span class="sxs-lookup"><span data-stu-id="a5248-126">Uninstall the AzureRM module</span></span>

<span data-ttu-id="a5248-127">如果您的系統上安裝了 Az 模組，並想要將 AzureRM 解除安裝，有兩個選項可讓您不必執行上述的 `Uninstall-AllModules` 指令碼。</span><span class="sxs-lookup"><span data-stu-id="a5248-127">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options that don't require running the `Uninstall-AllModules` script above.</span></span> <span data-ttu-id="a5248-128">您要遵循哪個方法取決於您安裝 AzureRM 模組的方式。</span><span class="sxs-lookup"><span data-stu-id="a5248-128">Which method you follow depends on how you installed the AzureRM module.</span></span>
<span data-ttu-id="a5248-129">如果您不確定原始安裝方法，請先依照將 MSI 解除安裝的步驟操作。</span><span class="sxs-lookup"><span data-stu-id="a5248-129">If you're not sure of your original install method, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="a5248-130">解除安裝 Azure PowerShell MSI</span><span class="sxs-lookup"><span data-stu-id="a5248-130">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="a5248-131">如果您使用 MSI 套件安裝 Azure PowerShell AzureRM 模組，則必須透過 Windows 系統而非 PowerShell 來解除安裝。</span><span class="sxs-lookup"><span data-stu-id="a5248-131">If you installed the Azure PowerShell AzureRM modules using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="a5248-132">平台</span><span class="sxs-lookup"><span data-stu-id="a5248-132">Platform</span></span> | <span data-ttu-id="a5248-133">範例的指示</span><span class="sxs-lookup"><span data-stu-id="a5248-133">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="a5248-134">Windows 10</span><span class="sxs-lookup"><span data-stu-id="a5248-134">Windows 10</span></span> | <span data-ttu-id="a5248-135">[開始] > [設定] > [應用程式]</span><span class="sxs-lookup"><span data-stu-id="a5248-135">Start > Settings > Apps</span></span> |
| <span data-ttu-id="a5248-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a5248-136">Windows 7</span></span> </br><span data-ttu-id="a5248-137">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a5248-137">Windows 8</span></span> | <span data-ttu-id="a5248-138">[開啟] > [控制台] > [程式] > [解除安裝程式]</span><span class="sxs-lookup"><span data-stu-id="a5248-138">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="a5248-139">您在此畫面上應該會看到程式清單中的 __Azure PowerShell__。</span><span class="sxs-lookup"><span data-stu-id="a5248-139">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="a5248-140">這是要解除安裝的應用程式。</span><span class="sxs-lookup"><span data-stu-id="a5248-140">This is the app to uninstall.</span></span> <span data-ttu-id="a5248-141">如果並未列出此程式，而您是透過 PowerShellGet 安裝，則應遵循下一組指示。</span><span class="sxs-lookup"><span data-stu-id="a5248-141">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-from-powershell"></a><span data-ttu-id="a5248-142">從 PowerShell 解除安裝</span><span class="sxs-lookup"><span data-stu-id="a5248-142">Uninstall from PowerShell</span></span>

<span data-ttu-id="a5248-143">如果透過 PowerShellGet 安裝了 AzureRM，您可以使用 [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) 命令移除模組，您可以在 `Az.Accounts` 模模組中找到這個命令。</span><span class="sxs-lookup"><span data-stu-id="a5248-143">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) command, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="a5248-144">這會從機器中移除「所有」  AzureRM 模組，但需要系統管理員權限。</span><span class="sxs-lookup"><span data-stu-id="a5248-144">This removes _all_ AzureRM modules from your machine, but requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```

<span data-ttu-id="a5248-145">如果您無法順利執行 `Uninstall-AzureRM` 命令，請使用本文所提供的 [`Uninstall-AllModules` 指令碼](#uninstall-script)進行叫用：</span><span class="sxs-lookup"><span data-stu-id="a5248-145">If you can't successfully run the `Uninstall-AzureRM` command, use the [`Uninstall-AllModules` script](#uninstall-script) provided in this article with the following invocation:</span></span>

```powershell-interactive
$versions = (Get-InstalledModule AzureRM -AllVersions | Select-Object Version)
$versions | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```