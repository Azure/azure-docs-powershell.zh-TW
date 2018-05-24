---
title: 安裝並設定 Azure PowerShell | Microsoft Docs
description: 如何安裝並設定 Azure PowerShell 以供第一次使用。
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.openlocfilehash: 0df1208db69fedcb61ca7e3e8fcf5d05dfef5379
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/23/2018
---
# <a name="install-and-configure-azure-powershell"></a><span data-ttu-id="d2041-103">安裝並設定 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d2041-103">Install and configure Azure PowerShell</span></span>

<span data-ttu-id="d2041-104">本文說明在 Windows 環境中安裝 Azure PowerShell 模組的步驟。</span><span class="sxs-lookup"><span data-stu-id="d2041-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment.</span></span>
<span data-ttu-id="d2041-105">如果您想要在 macOS 或 Linux 上使用 Azure PowerShell，請參閱下列文章：[在 macOS 與 Linux 上安裝和設定 Azure PowerShell](install-azurermps-maclinux.md)。</span><span class="sxs-lookup"><span data-stu-id="d2041-105">If you want to use Azure PowerShell on macOS or Linux, see the following article: [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="system-requirements"></a><span data-ttu-id="d2041-106">系統需求</span><span class="sxs-lookup"><span data-stu-id="d2041-106">System requirements</span></span>

<span data-ttu-id="d2041-107">Azure PowerShell 版本 6.0.0 需要 PowerShell 版本 5.0 (或更新版本)。</span><span class="sxs-lookup"><span data-stu-id="d2041-107">Azure PowerShell version 6.0.0 requires version 5.0 (or higher) of PowerShell.</span></span> <span data-ttu-id="d2041-108">Azure PowerShell 的舊版_至少需要_ PowerShell 版本 3.0，才能執行任何 Cmdlet。如需升級至 PowerShell 5.0 的詳細資訊，請參閱[此表格](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell)。</span><span class="sxs-lookup"><span data-stu-id="d2041-108">Previous versions of Azure PowerShell required _at least_ version 3.0 of PowerShell to run any cmdlet.For information on upgrading to PowerShell 5.0, please see [this table](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="d2041-109">步驟 1：安裝 PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="d2041-109">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="d2041-110">從 PowerShell 資源庫安裝 Azure PowerShell 是慣用的安裝方法。</span><span class="sxs-lookup"><span data-stu-id="d2041-110">Installing Azure PowerShell from the PowerShell Gallery is the preferred method of installation.</span></span>

<span data-ttu-id="d2041-111">從 PowerShell 資源庫安裝項目需要有 PowerShellGet 模組。</span><span class="sxs-lookup"><span data-stu-id="d2041-111">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="d2041-112">確定您有適當版本的 PowerShellGet 及其他系統需求。</span><span class="sxs-lookup"><span data-stu-id="d2041-112">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="d2041-113">執行下列命令，以查看您的系統上是否已安裝 PowerShellGet。</span><span class="sxs-lookup"><span data-stu-id="d2041-113">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="d2041-114">您應該會看到類似下面的輸出：</span><span class="sxs-lookup"><span data-stu-id="d2041-114">You should see something similar to the following output:</span></span>

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="d2041-115">您需要 PowerShellGet 1.1.2.0 版或更高版本。</span><span class="sxs-lookup"><span data-stu-id="d2041-115">You need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="d2041-116">若要更新 PowerShellGet，請使用下列命令：</span><span class="sxs-lookup"><span data-stu-id="d2041-116">To update PowerShellGet, use the following command:</span></span>

```powershell
Install-Module PowerShellGet -Force
```

<span data-ttu-id="d2041-117">如果您未安裝 PowerShellGet，請參閱本文的[如何取得 PowerShellGet](#how-to-get-powershellget)一節。</span><span class="sxs-lookup"><span data-stu-id="d2041-117">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget) section of this article.</span></span>

> [!NOTE]
> <span data-ttu-id="d2041-118">若要使用 PowerShellGet，需要有可讓您執行指令碼的執行原則。</span><span class="sxs-lookup"><span data-stu-id="d2041-118">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="d2041-119">如需 PowerShell 的執行原則詳細資訊，請參閱[關於執行原則](/powershell/module/microsoft.powershell.core/about/about_execution_policies)。</span><span class="sxs-lookup"><span data-stu-id="d2041-119">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="d2041-120">步驟 2：安裝 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d2041-120">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="d2041-121">從 PowerShell 資源庫安裝 Azure PowerShell 需要提高的權限。</span><span class="sxs-lookup"><span data-stu-id="d2041-121">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="d2041-122">從提高權限的 PowerShell 工作階段執行下列命令︰</span><span class="sxs-lookup"><span data-stu-id="d2041-122">Run the following command from an elevated PowerShell session:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="d2041-123">根據預設，PowerShell 資源庫未設為 PowerShellGet 的信任存放庫。</span><span class="sxs-lookup"><span data-stu-id="d2041-123">By default, the PowerShell gallery is not configured as a Trusted repository for PowerShellGet.</span></span> <span data-ttu-id="d2041-124">第一次使用 PSGallery 時，您會看到下列提示：</span><span class="sxs-lookup"><span data-stu-id="d2041-124">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

<span data-ttu-id="d2041-125">請回答「是」或「全部皆是」以繼續安裝。</span><span class="sxs-lookup"><span data-stu-id="d2041-125">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="d2041-126">如果您的 NuGet 版本比 2.8.5.201 舊，系統會提示您下載並安裝最新版的 NuGet。</span><span class="sxs-lookup"><span data-stu-id="d2041-126">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="d2041-127">AzureRM 模組是 Azure Resource Manager Cmdlet 的彙總套件模組。</span><span class="sxs-lookup"><span data-stu-id="d2041-127">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="d2041-128">當您安裝 AzureRM 模組時，系統會從 PowerShell 資源庫下載先前未安裝的任何 Azure PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="d2041-128">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded and from the PowerShell Gallery.</span></span>

<span data-ttu-id="d2041-129">若有安裝舊版的 Azure PowerShell，則可能會出現錯誤。</span><span class="sxs-lookup"><span data-stu-id="d2041-129">If you have a previous version of Azure PowerShell installed you may receive an error.</span></span> <span data-ttu-id="d2041-130">若要解決此問題，請參閱本文的[更新為新版的 Azure PowerShell](#update-azps) 小節。</span><span class="sxs-lookup"><span data-stu-id="d2041-130">To resolve this issue, see the [Updating to a new version of Azure PowerShell](#update-azps) section of this article.</span></span>

## <a name="step-3-load-the-azurerm-module"></a><span data-ttu-id="d2041-131">步驟 3︰載入 AzureRM 模組</span><span class="sxs-lookup"><span data-stu-id="d2041-131">Step 3: Load the AzureRM module</span></span>
<span data-ttu-id="d2041-132">安裝模組後，您需要將模組載入您的 PowerShell 工作階段。</span><span class="sxs-lookup"><span data-stu-id="d2041-132">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="d2041-133">您應該在一般 (未提高權限) PowerShell 工作階段中執行此動作。</span><span class="sxs-lookup"><span data-stu-id="d2041-133">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="d2041-134">使用 `Import-Module`Cmdlet 載入模組，如下所示︰</span><span class="sxs-lookup"><span data-stu-id="d2041-134">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module -Name AzureRM
```

## <a name="next-steps"></a><span data-ttu-id="d2041-135">後續步驟</span><span class="sxs-lookup"><span data-stu-id="d2041-135">Next Steps</span></span>

<span data-ttu-id="d2041-136">如需有關使用 Azure PowerShell 的詳細資訊，請參閱下列文章：</span><span class="sxs-lookup"><span data-stu-id="d2041-136">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="d2041-137">開始使用 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d2041-137">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="d2041-138">報告問題和意見反應</span><span class="sxs-lookup"><span data-stu-id="d2041-138">Reporting issues and feedback</span></span>

<span data-ttu-id="d2041-139">如果您遇到任何與工具有關的錯誤，請在 GitHub 存放庫的[問題](https://github.com/Azure/azure-powershell/issues)一節中提出問題。</span><span class="sxs-lookup"><span data-stu-id="d2041-139">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-powershell/issues) section of our GitHub repo.</span></span> <span data-ttu-id="d2041-140">若要從命令列提供意見反應，請使用 `Send-Feedback` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d2041-140">To provide feedback from the command line, use the `Send-Feedback` cmdlet.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="d2041-141">常見問題集</span><span class="sxs-lookup"><span data-stu-id="d2041-141">Frequently asked questions</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="d2041-142">如何取得 PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="d2041-142">How to get PowerShellGet</span></span>

|<span data-ttu-id="d2041-143">案例</span><span class="sxs-lookup"><span data-stu-id="d2041-143">Scenario</span></span>|<span data-ttu-id="d2041-144">安裝指示</span><span class="sxs-lookup"><span data-stu-id="d2041-144">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="d2041-145">Windows 10</span><span class="sxs-lookup"><span data-stu-id="d2041-145">Windows 10</span></span><br/><span data-ttu-id="d2041-146">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d2041-146">Windows Server 2016</span></span>|<span data-ttu-id="d2041-147">內建於 OS 包含的 Windows Management Framework (WMF) 5.0</span><span class="sxs-lookup"><span data-stu-id="d2041-147">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="d2041-148">我想要升級至 PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="d2041-148">I want to upgrade to PowerShell 5</span></span>|<ol><li>[<span data-ttu-id="d2041-149">安裝最新版的 WMF</span><span class="sxs-lookup"><span data-stu-id="d2041-149">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)</li><li><span data-ttu-id="d2041-150">執行以下命令：</span><span class="sxs-lookup"><span data-stu-id="d2041-150">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|
|<span data-ttu-id="d2041-151">我是在採用 PowerShell 3 或 PowerShell 4 的 Windows 版本上執行</span><span class="sxs-lookup"><span data-stu-id="d2041-151">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|<ol><span data-ttu-id="d2041-152"><il>[取得 PackageManagement 模組](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span><span class="sxs-lookup"><span data-stu-id="d2041-152"><il>[Get the PackageManagement modules](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span></span><li><span data-ttu-id="d2041-153">執行以下命令：</span><span class="sxs-lookup"><span data-stu-id="d2041-153">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a><span data-ttu-id="d2041-154">檢查 Azure PowerShell 的版本</span><span class="sxs-lookup"><span data-stu-id="d2041-154">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="d2041-155">雖然我們鼓勵您儘早升級至最新版本，但仍針對數個 Azure PowerShell 版本提供支援。</span><span class="sxs-lookup"><span data-stu-id="d2041-155">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="d2041-156">若要判斷已安裝的 Azure PowerShell 版本，請從命令列執行 `Get-Module AzureRM`。</span><span class="sxs-lookup"><span data-stu-id="d2041-156">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a><span data-ttu-id="d2041-157">對於傳統部署方法的支援</span><span class="sxs-lookup"><span data-stu-id="d2041-157">Support for classic deployment methods</span></span>

<span data-ttu-id="d2041-158">如果您有使用傳統部署模型的部署，則可以安裝 Azure PowerShell 的服務管理版本。</span><span class="sxs-lookup"><span data-stu-id="d2041-158">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="d2041-159">如需詳細資訊，請參閱[安裝 Azure PowerShell 服務管理模組](/powershell/azure/servicemanagement/install-azure-ps)。</span><span class="sxs-lookup"><span data-stu-id="d2041-159">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="d2041-160">Azure 和 AzureRM 模組會共用通用相依性。</span><span class="sxs-lookup"><span data-stu-id="d2041-160">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="d2041-161">若您同時使用 Azure 與 AzureRM 模組，則應該安裝每個套件的相同版本。</span><span class="sxs-lookup"><span data-stu-id="d2041-161">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a id="update-azps"></a><span data-ttu-id="d2041-162">更新為新版的 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d2041-162">Updating to a new version of Azure PowerShell</span></span>

<span data-ttu-id="d2041-163">若有安裝包括服務管理模組的舊版 Azure PowerShell，則可能會出現下列錯誤：</span><span class="sxs-lookup"><span data-stu-id="d2041-163">If you have a previous version of Azure PowerShell installed that includes the Service Management module, you may receive the following error:</span></span>

```Output
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

<span data-ttu-id="d2041-164">如錯誤訊息所述，您必須使用 -AllowClobber 參數來安裝模組。</span><span class="sxs-lookup"><span data-stu-id="d2041-164">As the error message states, you need to use the -AllowClobber parameter to install the module.</span></span> <span data-ttu-id="d2041-165">使用下列命令：</span><span class="sxs-lookup"><span data-stu-id="d2041-165">Use the following command:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="d2041-166">如需詳細資訊，請參閱 [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module) 的說明主題。</span><span class="sxs-lookup"><span data-stu-id="d2041-166">For more information, see the help topic for [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span></span>

### <a name="installing-module-versions-side-by-side"></a><span data-ttu-id="d2041-167">並存安裝模組版本</span><span class="sxs-lookup"><span data-stu-id="d2041-167">Installing module versions side by side</span></span>

<span data-ttu-id="d2041-168">PowerShellGet 安裝方法是唯一支援的多個版本安裝方法。</span><span class="sxs-lookup"><span data-stu-id="d2041-168">The PowerShellGet method of installation is the only method that supports the installation of multiple versions.</span></span> <span data-ttu-id="d2041-169">例如，您的指令碼可能是使用您沒有時間或資源更新的舊版 Azure PowerShell 所撰寫。</span><span class="sxs-lookup"><span data-stu-id="d2041-169">For example, you may have scripts written using a previous version of Azure PowerShell that you don't have the time or resources to updated.</span></span> <span data-ttu-id="d2041-170">下列命令說明如何安裝多個 Azure PowerShell 版本︰</span><span class="sxs-lookup"><span data-stu-id="d2041-170">The following commands illustrate how to install multiple versions of Azure PowerShell:</span></span>

```powershell
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="d2041-171">在一個 PowerShell 工作階段中只可以載入一個模組版本。</span><span class="sxs-lookup"><span data-stu-id="d2041-171">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="d2041-172">您必須開啟新的 PowerShell 視窗，並使用 `Import-Module` 來匯入特定版本的 AzureRM Cmdlet︰</span><span class="sxs-lookup"><span data-stu-id="d2041-172">You must open a new PowerShell window and use `Import-Module` to import a specific version of the AzureRM cmdlets:</span></span>

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> <span data-ttu-id="d2041-173">2.1.0 版和 1.2.6 版是第一批設計成可並存安裝及使用的模組版本。</span><span class="sxs-lookup"><span data-stu-id="d2041-173">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="d2041-174">載入舊版的 Azure PowerShell 時，會載入不相容的 **AzureRM.Profile** 模組版本。</span><span class="sxs-lookup"><span data-stu-id="d2041-174">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="d2041-175">這會導致每當您執行某個 Cmdlet 時，Cmdlet 都會提示您登入。</span><span class="sxs-lookup"><span data-stu-id="d2041-175">This results in the cmdlets prompting you to log in whenever you execute a cmdlet.</span></span>

### <a name="other-installation-methods"></a><span data-ttu-id="d2041-176">其他安裝方法</span><span class="sxs-lookup"><span data-stu-id="d2041-176">Other installation methods</span></span>

<span data-ttu-id="d2041-177">如需有關使用 Web Platform Installer 或 MSI 套件進行安裝的資訊，請參閱[其他安裝方法](other-install.md)</span><span class="sxs-lookup"><span data-stu-id="d2041-177">For information about installing using the Web Platform Installer or the MSI Package, see [Other installation methods](other-install.md)</span></span>
