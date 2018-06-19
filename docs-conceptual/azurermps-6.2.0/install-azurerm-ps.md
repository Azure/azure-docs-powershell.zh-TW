---
title: 使用 PowerShellGet 安裝 Azure PowerShell
description: 如何使用 PowerShellGet 安裝 Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/31/2018
ms.openlocfilehash: 9b7046157e32a5c8473210e9840f9ae1b2f45902
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323096"
---
# <a name="install-azure-powershell-with-powershellget"></a><span data-ttu-id="246b7-103">使用 PowerShellGet 安裝 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="246b7-103">Install Azure PowerShell with PowerShellGet</span></span>

<span data-ttu-id="246b7-104">本文說明在 Windows 環境中使用 PowerShellGet 安裝 Azure PowerShell 模組的步驟。</span><span class="sxs-lookup"><span data-stu-id="246b7-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment using PowerShellGet.</span></span>  <span data-ttu-id="246b7-105">這是安裝 Azure PowerShell 的偏好方式，但是如果您想要使用 Web Platform Installer 或 MSI 套件來安裝，請參閱[其他安裝方法](other-install.md)。</span><span class="sxs-lookup"><span data-stu-id="246b7-105">This is the preferred way to install Azure PowerShell, but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="246b7-106">如果您想要在 macOS 或 Linux 上使用 Azure PowerShell，請參閱下列文章：[在 macOS 與 Linux 上安裝和設定 Azure PowerShell](install-azurermps-maclinux.md)。</span><span class="sxs-lookup"><span data-stu-id="246b7-106">If you want to use Azure PowerShell on macOS or Linux, see the following article: [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="system-requirements"></a><span data-ttu-id="246b7-107">系統需求</span><span class="sxs-lookup"><span data-stu-id="246b7-107">System requirements</span></span>

<span data-ttu-id="246b7-108">Azure PowerShell 版本 6.1.0 需要 PowerShell 版本 5.0 (或更新版本)。</span><span class="sxs-lookup"><span data-stu-id="246b7-108">Azure PowerShell version 6.1.0 requires version 5.0 (or higher) of PowerShell.</span></span> <span data-ttu-id="246b7-109">如需升級到 PowerShell 5.0 的詳細資訊，請參閱[升級現有的 Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell)。</span><span class="sxs-lookup"><span data-stu-id="246b7-109">For information on upgrading to PowerShell 5.0, see [Upgrading existing Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

<span data-ttu-id="246b7-110">PowerShellGet 會自動包含在 PowerShell 5.0 中。</span><span class="sxs-lookup"><span data-stu-id="246b7-110">PowerShellGet is automatically included as part of PowerShell 5.0.</span></span>

## <a name="install-or-update-the-azure-powershell-module"></a><span data-ttu-id="246b7-111">安裝或更新 Azure PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="246b7-111">Install or update the Azure PowerShell module</span></span>

<span data-ttu-id="246b7-112">從 PowerShell 資源庫安裝 Azure PowerShell 需要提高的權限。</span><span class="sxs-lookup"><span data-stu-id="246b7-112">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="246b7-113">從提高權限的 PowerShell 工作階段執行下列命令︰</span><span class="sxs-lookup"><span data-stu-id="246b7-113">Run the following command from an elevated PowerShell session:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

> [!IMPORTANT]
> <span data-ttu-id="246b7-114">這個命令會更新您系統上的任何現有 Azure PowerShell 安裝。</span><span class="sxs-lookup"><span data-stu-id="246b7-114">This command will update any existing installation of Azure PowerShell on your system.</span></span> <span data-ttu-id="246b7-115">如果您需要安裝一個以上的版本，請參閱[可以安裝多個版本的 Azure PowerShell 嗎？](#multiple-versions)的常見問題集答案</span><span class="sxs-lookup"><span data-stu-id="246b7-115">If you need to have more than one version installed, see the FAQ answer for [Can I install multiple versions of Azure PowerShell?](#multiple-versions)</span></span>

<span data-ttu-id="246b7-116">根據預設，PowerShell 資源庫未設為 PowerShellGet 的信任存放庫。</span><span class="sxs-lookup"><span data-stu-id="246b7-116">By default, the PowerShell gallery is not configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="246b7-117">第一次使用 PSGallery 時，您會看到下列提示：</span><span class="sxs-lookup"><span data-stu-id="246b7-117">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="246b7-118">請回答「是」或「全部皆是」以繼續安裝。</span><span class="sxs-lookup"><span data-stu-id="246b7-118">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="246b7-119">如果您的 NuGet 版本比 2.8.5.201 舊，系統會提示您下載並安裝最新版的 NuGet。</span><span class="sxs-lookup"><span data-stu-id="246b7-119">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="246b7-120">AzureRM 模組是 Azure Resource Manager Cmdlet 的彙總套件模組。</span><span class="sxs-lookup"><span data-stu-id="246b7-120">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="246b7-121">當您安裝 AzureRM 模組時，系統會從 PowerShell 資源庫下載先前未安裝的任何 Azure PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="246b7-121">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded from the PowerShell Gallery.</span></span>

## <a name="load-the-azure-powershell-module"></a><span data-ttu-id="246b7-122">載入 Azure PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="246b7-122">Load the Azure PowerShell module</span></span>

<span data-ttu-id="246b7-123">安裝模組後，您需要將模組載入您的 PowerShell 工作階段。</span><span class="sxs-lookup"><span data-stu-id="246b7-123">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="246b7-124">您應該在一般 (未提高權限) PowerShell 工作階段中執行此動作。</span><span class="sxs-lookup"><span data-stu-id="246b7-124">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="246b7-125">使用 `Import-Module`Cmdlet 載入模組，如下所示︰</span><span class="sxs-lookup"><span data-stu-id="246b7-125">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module -Name AzureRM
```

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="246b7-126">報告問題和意見反應</span><span class="sxs-lookup"><span data-stu-id="246b7-126">Reporting issues and feedback</span></span>

<span data-ttu-id="246b7-127">如果您遇到任何工具錯誤，請[在 GitHub 上提出問題](https://github.com/Azure/azure-powershell/issues)。</span><span class="sxs-lookup"><span data-stu-id="246b7-127">If you encounter any bugs with the tool, please [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="246b7-128">若要從命令列提供意見反應，請使用 `Send-Feedback` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="246b7-128">To provide feedback from the command line, use the `Send-Feedback` cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="246b7-129">後續步驟</span><span class="sxs-lookup"><span data-stu-id="246b7-129">Next Steps</span></span>

<span data-ttu-id="246b7-130">如需有關使用 Azure PowerShell 的詳細資訊，請參閱下列文章：</span><span class="sxs-lookup"><span data-stu-id="246b7-130">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="246b7-131">開始使用 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="246b7-131">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <a name="frequently-asked-questions"></a><span data-ttu-id="246b7-132">常見問題集</span><span class="sxs-lookup"><span data-stu-id="246b7-132">Frequently asked questions</span></span>

### <a id="helpmechoose"></a><span data-ttu-id="246b7-133">如何檢查 Azure PowerShell 版本？</span><span class="sxs-lookup"><span data-stu-id="246b7-133">How do I check the version of Azure PowerShell?</span></span>

<span data-ttu-id="246b7-134">雖然我們鼓勵您儘早升級至最新版本，但仍針對數個 Azure PowerShell 版本提供支援。</span><span class="sxs-lookup"><span data-stu-id="246b7-134">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="246b7-135">若要判斷已安裝的 Azure PowerShell 版本，請從命令列執行 `Get-Module AzureRM`。</span><span class="sxs-lookup"><span data-stu-id="246b7-135">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="can-i-use-azure-powershell-for-azure-classic-deployments"></a><span data-ttu-id="246b7-136">可以針對 Azure 傳統部署使用 Azure PowerShell 嗎？</span><span class="sxs-lookup"><span data-stu-id="246b7-136">Can I use Azure PowerShell for Azure Classic deployments?</span></span>

<span data-ttu-id="246b7-137">如果您有使用傳統部署模型的部署，則可以安裝 Azure PowerShell 的服務管理版本。</span><span class="sxs-lookup"><span data-stu-id="246b7-137">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="246b7-138">如需詳細資訊，請參閱[安裝 Azure PowerShell 服務管理模組](/powershell/azure/servicemanagement/install-azure-ps)。</span><span class="sxs-lookup"><span data-stu-id="246b7-138">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="246b7-139">Azure 和 AzureRM 模組會共用通用相依性。</span><span class="sxs-lookup"><span data-stu-id="246b7-139">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="246b7-140">若您同時使用 Azure 與 AzureRM 模組，則應該安裝每個套件的相同版本。</span><span class="sxs-lookup"><span data-stu-id="246b7-140">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a name="a-namemultiple-versionscan-i-install-multiple-versions-of-azure-powershell"></a><span data-ttu-id="246b7-141"><a name="multiple-versions"/>可以安裝多個版本的 Azure PowerShell 嗎？</span><span class="sxs-lookup"><span data-stu-id="246b7-141"><a name="multiple-versions"/>Can I install multiple versions of Azure PowerShell?</span></span>

<span data-ttu-id="246b7-142">PowerShellGet 是唯一支援安裝多個版本的方法。</span><span class="sxs-lookup"><span data-stu-id="246b7-142">PowerShellGet the only method of installation that supports multiple versions.</span></span> <span data-ttu-id="246b7-143">若要安裝多個版本，您可以將 `-RequiredVersion` 參數新增至 `Install-Module` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="246b7-143">To install multiple versions, you can add the `-RequiredVersion` parameter to the `Install-Module` cmdlet.</span></span> <span data-ttu-id="246b7-144">例如，若要同時安裝 6.1.0 版和 1.2.9 版：</span><span class="sxs-lookup"><span data-stu-id="246b7-144">For example, to install both versions 6.1.0 and 1.2.9:</span></span>

```powershell
Install-Module -Name AzureRM -RequiredVersion 6.1.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="246b7-145">在一個 PowerShell 工作階段中只可以載入一個模組版本。</span><span class="sxs-lookup"><span data-stu-id="246b7-145">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="246b7-146">您必須開啟新的 PowerShell 視窗，並使用 `Import-Module` 來匯入特定版本的 Azure PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="246b7-146">You must open a new PowerShell window and use `Import-Module` to import a specific version of the Azure PowerShell module.</span></span>

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> <span data-ttu-id="246b7-147">2.1.0 版和 1.2.6 版是第一批設計成可並存安裝及使用的模組版本。</span><span class="sxs-lookup"><span data-stu-id="246b7-147">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="246b7-148">載入舊版的 Azure PowerShell 時，會載入不相容的 **AzureRM.Profile** 模組版本。</span><span class="sxs-lookup"><span data-stu-id="246b7-148">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="246b7-149">這會導致每當您執行某個 Cmdlet 時，Cmdlet 都會提示您登入。</span><span class="sxs-lookup"><span data-stu-id="246b7-149">This results in the cmdlets prompting you to log in whenever you execute a cmdlet.</span></span>
