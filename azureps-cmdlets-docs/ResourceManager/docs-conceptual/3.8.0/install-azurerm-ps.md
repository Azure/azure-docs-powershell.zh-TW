---
title: "<span data-ttu-id=\"323eb-101\">安裝並設定 Azure PowerShell | Microsoft Docs</span><span class=\"sxs-lookup\"><span data-stu-id=\"323eb-101\">Install and configure Azure PowerShell | Microsoft Docs</span></span>"
description: "<span data-ttu-id=\"323eb-102\">如何安裝並設定 Azure PowerShell 以供第一次使用。</span><span class=\"sxs-lookup\"><span data-stu-id=\"323eb-102\">How to install and configure Azure PowerShell for first time use.</span></span>"
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/17/2017
ms.openlocfilehash: 0c1500a8748a3aa4546c6ce1e8d16a635b056edb
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/29/2017
---
# <span data-ttu-id="323eb-103">安裝並設定 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="323eb-103">Install and configure Azure PowerShell</span></span>
<a id="install-and-configure-azure-powershell" class="xliff"></a>

<span data-ttu-id="323eb-104">從 PowerShell 資源庫安裝 Azure PowerShell 是慣用的安裝方法。</span><span class="sxs-lookup"><span data-stu-id="323eb-104">Installing Azure PowerShell from the PowerShell Gallery is the preferred method of installation.</span></span>

## <span data-ttu-id="323eb-105">步驟 1：安裝 PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="323eb-105">Step 1: Install PowerShellGet</span></span>
<a id="step-1-install-powershellget" class="xliff"></a>

<span data-ttu-id="323eb-106">從 PowerShell 資源庫安裝項目需要有 PowerShellGet 模組。</span><span class="sxs-lookup"><span data-stu-id="323eb-106">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="323eb-107">確定您有適當版本的 PowerShellGet 及其他系統需求。</span><span class="sxs-lookup"><span data-stu-id="323eb-107">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="323eb-108">執行下列命令，以查看您的系統上是否已安裝 PowerShellGet。</span><span class="sxs-lookup"><span data-stu-id="323eb-108">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-Module PowerShellGet -list | Select-Object Name,Version,Path
```

<span data-ttu-id="323eb-109">您應該會看到類似下面的輸出：</span><span class="sxs-lookup"><span data-stu-id="323eb-109">You should see something similar to the following output:</span></span>

```
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="323eb-110">如果您未安裝 PowerShellGet，請參閱本文的[如何取得 PowerShellGet](#how-to-get-powershellget)一節。</span><span class="sxs-lookup"><span data-stu-id="323eb-110">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget) section of this article.</span></span>

> [!NOTE]
> <span data-ttu-id="323eb-111">若要使用 PowerShellGet，需要有可讓您執行指令碼的執行原則。</span><span class="sxs-lookup"><span data-stu-id="323eb-111">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="323eb-112">如需 PowerShell 的執行原則詳細資訊，請參閱[關於執行原則](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.core/about/about_execution_policies)。</span><span class="sxs-lookup"><span data-stu-id="323eb-112">For more information about PowerShell's Execution Policy, see [About Execution Policies](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.core/about/about_execution_policies).</span></span>

## <span data-ttu-id="323eb-113">步驟 2：安裝 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="323eb-113">Step 2: Install Azure PowerShell</span></span>
<a id="step-2-install-azure-powershell" class="xliff"></a>

<span data-ttu-id="323eb-114">從 PowerShell 資源庫安裝 Azure PowerShell 需要提高的權限。</span><span class="sxs-lookup"><span data-stu-id="323eb-114">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="323eb-115">從提高權限的 PowerShell 工作階段執行下列命令︰</span><span class="sxs-lookup"><span data-stu-id="323eb-115">Run the following command from an elevated PowerShell session:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module AzureRM
```

<span data-ttu-id="323eb-116">根據預設，PowerShell 資源庫未設為 PowerShellGet 的信任存放庫。</span><span class="sxs-lookup"><span data-stu-id="323eb-116">By default, the PowerShell gallery is not configured as a Trusted repository for PowerShellGet.</span></span> <span data-ttu-id="323eb-117">第一次使用 PSGallery 時，您會看到下列提示：</span><span class="sxs-lookup"><span data-stu-id="323eb-117">The first time you use the PSGallery you see the following prompt:</span></span>

```
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

<span data-ttu-id="323eb-118">請回答「是」或「全部皆是」以繼續安裝。</span><span class="sxs-lookup"><span data-stu-id="323eb-118">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="323eb-119">如果您的 NuGet 版本比 2.8.5.201 舊，系統會提示您下載並安裝最新版的 NuGet。</span><span class="sxs-lookup"><span data-stu-id="323eb-119">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="323eb-120">AzureRM 模組是 Azure Resource Manager Cmdlet 的彙總套件模組。</span><span class="sxs-lookup"><span data-stu-id="323eb-120">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="323eb-121">當您安裝 AzureRM 模組時，系統會從 PowerShell 資源庫下載先前未安裝的任何 Azure PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="323eb-121">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded and from the PowerShell Gallery.</span></span>

<span data-ttu-id="323eb-122">若有安裝舊版的 Azure PowerShell，則可能會出現錯誤。</span><span class="sxs-lookup"><span data-stu-id="323eb-122">If you have a previous version of Azure PowerShell installed you may receive an error.</span></span> <span data-ttu-id="323eb-123">若要解決此問題，請參閱本文的[更新為新版的 Azure PowerShell](#update-azps) 小節。</span><span class="sxs-lookup"><span data-stu-id="323eb-123">To resolve this issue, see the [Updating to a new version of Azure PowerShell](#update-azps) section of this article.</span></span>

## <span data-ttu-id="323eb-124">步驟 3︰載入 AzureRM 模組</span><span class="sxs-lookup"><span data-stu-id="323eb-124">Step 3: Load the AzureRM module</span></span>
<a id="step-3-load-the-azurerm-module" class="xliff"></a>
<span data-ttu-id="323eb-125">安裝模組後，您需要將模組載入您的 PowerShell 工作階段。</span><span class="sxs-lookup"><span data-stu-id="323eb-125">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="323eb-126">您應該在一般 (未提高權限) PowerShell 工作階段中執行此動作。</span><span class="sxs-lookup"><span data-stu-id="323eb-126">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="323eb-127">使用 `Import-Module`Cmdlet 載入模組，如下所示︰</span><span class="sxs-lookup"><span data-stu-id="323eb-127">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM
```

## <span data-ttu-id="323eb-128">後續步驟</span><span class="sxs-lookup"><span data-stu-id="323eb-128">Next Steps</span></span>
<a id="next-steps" class="xliff"></a>

<span data-ttu-id="323eb-129">如需有關使用 Azure PowerShell 的詳細資訊，請參閱下列文章：</span><span class="sxs-lookup"><span data-stu-id="323eb-129">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="323eb-130">開始使用 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="323eb-130">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <span data-ttu-id="323eb-131">常見問題集</span><span class="sxs-lookup"><span data-stu-id="323eb-131">Frequently asked questions</span></span>
<a id="frequently-asked-questions" class="xliff"></a>

### <span data-ttu-id="323eb-132">如何取得 PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="323eb-132">How to get PowerShellGet</span></span>
<a id="how-to-get-powershellget" class="xliff"></a>

|<span data-ttu-id="323eb-133">作業系統版本</span><span class="sxs-lookup"><span data-stu-id="323eb-133">OS Version</span></span>|<span data-ttu-id="323eb-134">安裝指示</span><span class="sxs-lookup"><span data-stu-id="323eb-134">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="323eb-135">我有 Windows 10 或 Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="323eb-135">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="323eb-136">內建於 OS 包含的 Windows Management Framework (WMF) 5.0</span><span class="sxs-lookup"><span data-stu-id="323eb-136">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="323eb-137">我想要升級至 PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="323eb-137">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="323eb-138">安裝最新版的 WMF</span><span class="sxs-lookup"><span data-stu-id="323eb-138">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|<span data-ttu-id="323eb-139">我是在採用 PowerShell 3 或 PowerShell 4 的 Windows 版本上執行</span><span class="sxs-lookup"><span data-stu-id="323eb-139">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|[<span data-ttu-id="323eb-140">取得 PackageManagement 模組</span><span class="sxs-lookup"><span data-stu-id="323eb-140">Get the PackageManagement modules</span></span>](http://go.microsoft.com/fwlink/?LinkID=746217)|

<a id="helpmechoose"></a>
### <span data-ttu-id="323eb-141">檢查 Azure PowerShell 的版本</span><span class="sxs-lookup"><span data-stu-id="323eb-141">Checking the version of Azure PowerShell</span></span>
<a id="checking-the-version-of-azure-powershell" class="xliff"></a>

<span data-ttu-id="323eb-142">雖然我們鼓勵您儘早升級至最新版本，但支援的 Azure PowerShell 版本有好幾個。</span><span class="sxs-lookup"><span data-stu-id="323eb-142">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are support.</span></span> <span data-ttu-id="323eb-143">若要判斷已安裝的 Azure PowerShell 版本，請從命令列執行 `Get-Module AzureRM`。</span><span class="sxs-lookup"><span data-stu-id="323eb-143">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -list | Select-Object Name,Version,Path
```

### <span data-ttu-id="323eb-144">對於傳統部署方法的支援</span><span class="sxs-lookup"><span data-stu-id="323eb-144">Support for classic deployment methods</span></span>
<a id="support-for-classic-deployment-methods" class="xliff"></a>

<span data-ttu-id="323eb-145">如果您有使用傳統部署模型的部署，則可以安裝 Azure PowerShell 的服務管理版本。</span><span class="sxs-lookup"><span data-stu-id="323eb-145">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="323eb-146">如需詳細資訊，請參閱[安裝 Azure PowerShell 服務管理模組](/powershell/azure/servicemanagement/install-azure-ps)。</span><span class="sxs-lookup"><span data-stu-id="323eb-146">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="323eb-147">Azure 和 AzureRM 模組會共用通用相依性。</span><span class="sxs-lookup"><span data-stu-id="323eb-147">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="323eb-148">若您同時使用 Azure 與 AzureRM 模組，則應該安裝每個套件的相同版本。</span><span class="sxs-lookup"><span data-stu-id="323eb-148">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <span data-ttu-id="323eb-149"><a id="update-azps"></a>更新為新版的 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="323eb-149"><a id="update-azps"></a>Updating to a new version of Azure PowerShell</span></span>

<span data-ttu-id="323eb-150">若有安裝包括服務管理模組的舊版 Azure PowerShell，則可能會出現下列錯誤：</span><span class="sxs-lookup"><span data-stu-id="323eb-150">If you have a previous version of Azure PowerShell installed that includes the Service Management module, you may receive the following error:</span></span>

```
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

<span data-ttu-id="323eb-151">如錯誤訊息所述，您必須使用 -AllowClobber 參數來安裝模組。</span><span class="sxs-lookup"><span data-stu-id="323eb-151">As the error message states, you need to use the -AllowClobber parameter to install the module.</span></span> <span data-ttu-id="323eb-152">使用下列命令：</span><span class="sxs-lookup"><span data-stu-id="323eb-152">Use the following command:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module AzureRM -AllowClobber
```

<span data-ttu-id="323eb-153">如需詳細資訊，請參閱 [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module) 的說明主題。</span><span class="sxs-lookup"><span data-stu-id="323eb-153">For more information, see the help topic for [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span></span>

### <span data-ttu-id="323eb-154">並存安裝模組版本</span><span class="sxs-lookup"><span data-stu-id="323eb-154">Installing module versions side by side</span></span>
<a id="installing-module-versions-side-by-side" class="xliff"></a>

<span data-ttu-id="323eb-155">PowerShellGet 安裝方法是唯一支援的多個版本安裝方法。</span><span class="sxs-lookup"><span data-stu-id="323eb-155">The PowerShellGet method of installation is the only method that supports the installation of multiple versions.</span></span> <span data-ttu-id="323eb-156">例如，您的指令碼可能是使用您沒有時間或資源更新的舊版 Azure PowerShell 所撰寫。</span><span class="sxs-lookup"><span data-stu-id="323eb-156">For example, you may have scripts written using a previous version of Azure PowerShell that you don't have the time or resources to updated.</span></span> <span data-ttu-id="323eb-157">下列命令說明如何安裝多個 Azure PowerShell 版本︰</span><span class="sxs-lookup"><span data-stu-id="323eb-157">The following commands illustrate how to install multiple versions of Azure PowerShell:</span></span>

```powershell
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="323eb-158">在一個 PowerShell 工作階段中只可以載入一個模組版本。</span><span class="sxs-lookup"><span data-stu-id="323eb-158">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="323eb-159">您必須開啟新的 PowerShell 視窗，並使用 `Import-Module` 來匯入特定版本的 AzureRM Cmdlet︰</span><span class="sxs-lookup"><span data-stu-id="323eb-159">You must open a new PowerShell window and use `Import-Module` to import a specific version of the AzureRM cmdlets:</span></span>

```powershell
Import-Module AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> <span data-ttu-id="323eb-160">2.1.0 版和 1.2.6 版是第一批設計成可並存安裝及使用的模組版本。</span><span class="sxs-lookup"><span data-stu-id="323eb-160">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="323eb-161">載入舊版的 Azure PowerShell 時，會載入不相容的 **AzureRM.Profile** 模組版本。</span><span class="sxs-lookup"><span data-stu-id="323eb-161">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="323eb-162">這會導致每當您執行某個 Cmdlet 時，Cmdlet 都會提示您登入。</span><span class="sxs-lookup"><span data-stu-id="323eb-162">This results in the cmdlets prompting you to log in whenever you execute a cmdlet.</span></span>

### <span data-ttu-id="323eb-163">其他安裝方法</span><span class="sxs-lookup"><span data-stu-id="323eb-163">Other installation methods</span></span>
<a id="other-installation-methods" class="xliff"></a>

<span data-ttu-id="323eb-164">如需有關使用 Web Platform Installer 或 MSI 套件進行安裝的資訊，請參閱[其他安裝方法](other-install.md)</span><span class="sxs-lookup"><span data-stu-id="323eb-164">For information about installing using the Web Platform Installer or the MSI Package, see [Other installation methods](other-install.md)</span></span>
