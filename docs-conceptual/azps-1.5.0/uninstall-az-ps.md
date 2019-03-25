---
title: 將 Azure PowerShell 解除安裝
description: 如何執行 Azure PowerShell 完全解除安裝
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 6a34ac1821c3cec359d0d64664d3f1689621b304
ms.sourcegitcommit: e736293cbc7b813b6b133781c88c7978fb22122a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/20/2019
ms.locfileid: "58215265"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="4482c-103">將 Azure PowerShell 模組解除安裝</span><span class="sxs-lookup"><span data-stu-id="4482c-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="4482c-104">本文說明如何將較舊版的 Azure PowerShell 解除安裝，或從您的系統將它完全移除。</span><span class="sxs-lookup"><span data-stu-id="4482c-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="4482c-105">如果您已決定要將 Azure PowerShell 完全解除安裝，請透過 [Send-Feedback](/powershell/module/az.accounts/send-feedback) Cmdlet 提供意見反應給我們。</span><span class="sxs-lookup"><span data-stu-id="4482c-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>
<span data-ttu-id="4482c-106">如果發生錯誤 (bug)，希望您[提出 GitHub 問題](https://github.com/azure/azure-powershell/issues)，非常感謝您。</span><span class="sxs-lookup"><span data-stu-id="4482c-106">If you encounter a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-the-az-module"></a><span data-ttu-id="4482c-107">將 Az 模組解除安裝</span><span class="sxs-lookup"><span data-stu-id="4482c-107">Uninstall the Az module</span></span>

<span data-ttu-id="4482c-108">若要將 Az 模組解除安裝，請使用 [Uninstall-module](/powershell/module/powershellget/uninstall-module) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4482c-108">To uninstall the Az modules, use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="4482c-109">不過，`Uninstall-Module` 只會解除安裝一個模組。</span><span class="sxs-lookup"><span data-stu-id="4482c-109">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="4482c-110">若要完全移除 Azure PowerShell，您必須個別將每個模組解除安裝。</span><span class="sxs-lookup"><span data-stu-id="4482c-110">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="4482c-111">如果您安裝了多個版本的 Azure PowerShell，則解除安裝可能會很複雜。</span><span class="sxs-lookup"><span data-stu-id="4482c-111">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="4482c-112">若要檢查您目前安裝的 Azure PowerShell 版本，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="4482c-112">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
0.7.0               Az                             PSGallery            Azure Resource Manager Module
1.0.0               Az                             PSGallery            Azure Resource Manager Module
```

<span data-ttu-id="4482c-113">下列指令碼會查詢 PowerShell 資源庫來取得相依子模組的清單。</span><span class="sxs-lookup"><span data-stu-id="4482c-113">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="4482c-114">然後，指令碼會將每個子模組的正確版本解除安裝。</span><span class="sxs-lookup"><span data-stu-id="4482c-114">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="4482c-115">您需要擁有系統管理員權限，才能在 `Process` 或 `CurrentUser`以外的範圍執行此指令碼。</span><span class="sxs-lookup"><span data-stu-id="4482c-115">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

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
    if ($_.requiredVersion) {
      $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredVersion}
    }
    else { # Assume minimum version
      # Minimum version actually reports the installed dependency
      # which is used, not the actual "minimum dependency." Check to
      # see if the requested version was installed as a dependency earlier.
      $candidate = Get-InstalledModule $_.name -RequiredVersion $version
      if ($candidate) {
        $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$version}
      }
      else {
        Write-Warning ("Could not find uninstall candidate for {0}:{1} - module may require manual uninstall" -f $_.name,$version)
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

<span data-ttu-id="4482c-116">若要使用此函式，請複製程式碼，然後貼到您的 PowerShell 工作階段。</span><span class="sxs-lookup"><span data-stu-id="4482c-116">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="4482c-117">下列範例示範如何執行函式，以將舊版的 Azure PowerShell 移除。</span><span class="sxs-lookup"><span data-stu-id="4482c-117">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

<span data-ttu-id="4482c-118">指令碼在執行時，會顯示要解除安裝的每個子模組名稱及版本。</span><span class="sxs-lookup"><span data-stu-id="4482c-118">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="4482c-119">若只想執行指令碼以查看會刪除的項目，而不要真正移除項目，請使用 `-WhatIf` 選項。</span><span class="sxs-lookup"><span data-stu-id="4482c-119">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

<span data-ttu-id="4482c-120">請針對您要解除安裝的 Azure PowerShell 每個版本執行此命令。</span><span class="sxs-lookup"><span data-stu-id="4482c-120">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="4482c-121">為了方便起見，下列指令碼會將所有版本的 Az 解除安裝，__只留下__最新版本。</span><span class="sxs-lookup"><span data-stu-id="4482c-121">For convenience, the following script will uninstall all versions of Az __except__ for the latest.</span></span>

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="4482c-122">將 AzureRM 模組解除安裝</span><span class="sxs-lookup"><span data-stu-id="4482c-122">Uninstall the AzureRM module</span></span>

<span data-ttu-id="4482c-123">如果您的系統上安裝了 Az 模組，並想要將 AzureRM 解除安裝，有兩個選項可讓您不必執行上述的 `Uninstall-AllModules` 指令碼。</span><span class="sxs-lookup"><span data-stu-id="4482c-123">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options that don't require running the `Uninstall-AllModules` script above.</span></span> <span data-ttu-id="4482c-124">您要遵循哪個方法取決於您安裝 AzureRM 模組的方式。</span><span class="sxs-lookup"><span data-stu-id="4482c-124">Which method you follow depends on how you installed the AzureRM module.</span></span>
<span data-ttu-id="4482c-125">如果您不確定，請先遵循如何將 MSI 解除安裝的步驟。</span><span class="sxs-lookup"><span data-stu-id="4482c-125">If you're not sure, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="4482c-126">解除安裝 Azure PowerShell MSI</span><span class="sxs-lookup"><span data-stu-id="4482c-126">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="4482c-127">如果您使用 MSI 套件安裝 Azure PowerShell AzureRM 模組，則必須透過 Windows 系統而非 PowerShell 來解除安裝。</span><span class="sxs-lookup"><span data-stu-id="4482c-127">If you installed the Azure PowerShell AzureRM modules using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="4482c-128">平台</span><span class="sxs-lookup"><span data-stu-id="4482c-128">Platform</span></span> | <span data-ttu-id="4482c-129">範例的指示</span><span class="sxs-lookup"><span data-stu-id="4482c-129">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="4482c-130">Windows 10</span><span class="sxs-lookup"><span data-stu-id="4482c-130">Windows 10</span></span> | <span data-ttu-id="4482c-131">[開始] > [設定] > [應用程式]</span><span class="sxs-lookup"><span data-stu-id="4482c-131">Start > Settings > Apps</span></span> |
| <span data-ttu-id="4482c-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4482c-132">Windows 7</span></span> </br><span data-ttu-id="4482c-133">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4482c-133">Windows 8</span></span> | <span data-ttu-id="4482c-134">[開啟] > [控制台] > [程式] > [解除安裝程式]</span><span class="sxs-lookup"><span data-stu-id="4482c-134">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="4482c-135">您在此畫面上應該會看到程式清單中的 __Azure PowerShell__。</span><span class="sxs-lookup"><span data-stu-id="4482c-135">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="4482c-136">這是要解除安裝的應用程式。</span><span class="sxs-lookup"><span data-stu-id="4482c-136">This is the app to uninstall.</span></span> <span data-ttu-id="4482c-137">如果並未列出此程式，而您是透過 PowerShellGet 安裝，則應遵循下一組指示。</span><span class="sxs-lookup"><span data-stu-id="4482c-137">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-from-powershell"></a><span data-ttu-id="4482c-138">從 PowerShell 解除安裝</span><span class="sxs-lookup"><span data-stu-id="4482c-138">Uninstall from PowerShell</span></span>

<span data-ttu-id="4482c-139">如果透過 PowerShellGet 安裝了 AzureRM，您可以使用 [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) 命令移除模組，您可以在 `Az.Accounts` 模模組中找到這個命令。</span><span class="sxs-lookup"><span data-stu-id="4482c-139">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) command, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="4482c-140">這會從機器中移除「所有」AzureRM 模組，但需要系統管理員權限。</span><span class="sxs-lookup"><span data-stu-id="4482c-140">This removes _all_ AzureRM modules from your machine, but requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```

<span data-ttu-id="4482c-141">如果您無法順利執行 `Uninstall-AzureRM` 命令，請改用本文所提供的 `Uninstall-AllModules` 指令碼。</span><span class="sxs-lookup"><span data-stu-id="4482c-141">If you can't successfully run the `Uninstall-AzureRM` command, use the `Uninstall-AllModules` script provided in this article instead.</span></span>