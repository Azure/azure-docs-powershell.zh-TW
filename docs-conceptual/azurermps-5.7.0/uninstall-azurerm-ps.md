---
title: 將 Azure PowerShell 解除安裝
description: 如何執行 Azure PowerShell 完全解除安裝
ms.date: 06/20/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 3828a6f9d60a68c2837cc201a50d8707324f4f0a
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/05/2018
ms.locfileid: "52828564"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="2e3eb-103">將 Azure PowerShell 模組解除安裝</span><span class="sxs-lookup"><span data-stu-id="2e3eb-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="2e3eb-104">本文說明如何將較舊版的 Azure PowerShell 解除安裝，或從您的系統將它完全移除。</span><span class="sxs-lookup"><span data-stu-id="2e3eb-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="2e3eb-105">如果您已決定要將 Azure PowerShell 完全解除安裝，請透過 [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) Cmdlet 提供一些意見反應給我們。</span><span class="sxs-lookup"><span data-stu-id="2e3eb-105">If you've decided to completely uninstall the Azure PowerShell, please give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="2e3eb-106">如果發生錯誤 (bug)，希望您[提出 GitHub 問題](https://github.com/azure/azure-powershell/issues)，非常感謝您。</span><span class="sxs-lookup"><span data-stu-id="2e3eb-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-msi-or-web-platform-installer"></a><span data-ttu-id="2e3eb-107">將 MSI 或 Web Platform Installer 解除安裝</span><span class="sxs-lookup"><span data-stu-id="2e3eb-107">Uninstall MSI or Web Platform Installer</span></span>

<span data-ttu-id="2e3eb-108">如果您使用 MSI 套件或 Web Platform Installer 來安裝 Azure PowerShell，則必須透過 Windows 系統而非 PowerShell 來解除安裝。</span><span class="sxs-lookup"><span data-stu-id="2e3eb-108">If you installed Azure PowerShell using the MSI package or the Web Platform Installer, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="2e3eb-109">平台</span><span class="sxs-lookup"><span data-stu-id="2e3eb-109">Platform</span></span> | <span data-ttu-id="2e3eb-110">範例的指示</span><span class="sxs-lookup"><span data-stu-id="2e3eb-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="2e3eb-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="2e3eb-111">Windows 10</span></span> | <span data-ttu-id="2e3eb-112">[開始] > [設定] > [應用程式]</span><span class="sxs-lookup"><span data-stu-id="2e3eb-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="2e3eb-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2e3eb-113">Windows 7</span></span> </br><span data-ttu-id="2e3eb-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2e3eb-114">Windows 8</span></span> | <span data-ttu-id="2e3eb-115">[開啟] > [控制台] > [程式] > [解除安裝程式]</span><span class="sxs-lookup"><span data-stu-id="2e3eb-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="2e3eb-116">您在此畫面上應該會看到程式清單中的 "Azure PowerShell"，並可從該處解除安裝。</span><span class="sxs-lookup"><span data-stu-id="2e3eb-116">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="2e3eb-117">從 PowerShell 解除安裝</span><span class="sxs-lookup"><span data-stu-id="2e3eb-117">Uninstall from PowerShell</span></span>

<span data-ttu-id="2e3eb-118">如果您使用 PowerShellGet 安裝 Azure PowerShell，則可以使用 [Uninstall-Module](/powershell/module/powershellget/uninstall-module) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2e3eb-118">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="2e3eb-119">不過，`Uninstall-Module` 只會解除安裝一個模組。</span><span class="sxs-lookup"><span data-stu-id="2e3eb-119">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="2e3eb-120">若要完全移除 Azure PowerShell，您必須個別將每個模組解除安裝。</span><span class="sxs-lookup"><span data-stu-id="2e3eb-120">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="2e3eb-121">如果您安裝了多個版本的 Azure PowerShell，則解除安裝可能會很複雜。</span><span class="sxs-lookup"><span data-stu-id="2e3eb-121">Uninstallation can be complicated if you have multiple versions of Azure PowerShell installed.</span></span>

<span data-ttu-id="2e3eb-122">請使用下列指令碼，可用來將單一版本的 Azure PowerShell 完全移除。</span><span class="sxs-lookup"><span data-stu-id="2e3eb-122">You use the following script can be used to completely remove a single version of Azure PowerShell.</span></span> <span data-ttu-id="2e3eb-123">指令碼會查詢 PowerShell 資源庫來取得相依子模組的清單。</span><span class="sxs-lookup"><span data-stu-id="2e3eb-123">The script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="2e3eb-124">然後，指令碼會將每個子模組的正確版本解除安裝。</span><span class="sxs-lookup"><span data-stu-id="2e3eb-124">Then, the script uninstalls the correct version of each submodule.</span></span>

```powershell-interactive
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

<span data-ttu-id="2e3eb-125">若要使用此函式，請複製程式碼，然後貼到您的 PowerShell 工作階段。</span><span class="sxs-lookup"><span data-stu-id="2e3eb-125">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="2e3eb-126">下列範例示範如何執行函式，以將舊版的 Azure PowerShell 移除。</span><span class="sxs-lookup"><span data-stu-id="2e3eb-126">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="2e3eb-127">指令碼在執行時，會顯示要解除安裝的每個子模組名稱及版本。</span><span class="sxs-lookup"><span data-stu-id="2e3eb-127">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

<span data-ttu-id="2e3eb-128">請針對您要解除安裝的 Azure PowerShell 每個版本執行此命令。</span><span class="sxs-lookup"><span data-stu-id="2e3eb-128">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span>