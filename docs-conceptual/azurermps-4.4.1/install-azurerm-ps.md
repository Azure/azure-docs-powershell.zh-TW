---
title: 安裝並設定 Azure PowerShell | Microsoft Docs
description: 如何安裝並設定 Azure PowerShell 以供第一次使用。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 3f4b05352ef5e5c7f32495d002a78aadd3e056e1
ms.sourcegitcommit: 038cb42a3bd8c009bc57c8c1c252e66fa170c84b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/24/2020
ms.locfileid: "92523286"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="fa073-103">使用 PowerShellGet 在 Windows 上安裝 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="fa073-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="fa073-104">本文說明使用 PowerShellGet 為 Windows PowerShell 5.x 安裝 Azure PowerShell 模組的步驟。</span><span class="sxs-lookup"><span data-stu-id="fa073-104">This article explains the steps to install the Azure PowerShell modules for PowerShell 5.x for Windows using PowerShellGet.</span></span> <span data-ttu-id="fa073-105">PowerShellGet 和模組管理是安裝 Azure PowerShell 的偏好方式，但是如果您想要使用 Web Platform Installer 或 MSI 套件來安裝，請參閱[其他安裝方法](other-install.md)。</span><span class="sxs-lookup"><span data-stu-id="fa073-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="fa073-106">這個版本的 Azure PowerShell 不支援 Azure 傳統部署模型。</span><span class="sxs-lookup"><span data-stu-id="fa073-106">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="fa073-107">如需傳統部署的支援，請遵循[安裝 Azure PowerShell 服務管理模組](/powershell/azure/servicemanagement/install-azure-ps)中的指示。</span><span class="sxs-lookup"><span data-stu-id="fa073-107">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fa073-108">AzureRM 模組不支援 macOS 或 Linux。</span><span class="sxs-lookup"><span data-stu-id="fa073-108">The AzureRM module is not supported for macOS or Linux.</span></span> <span data-ttu-id="fa073-109">若要在這些平台上使用 Azure PowerShell Cmdlet，請[安裝 Az 模組](/powershell/azure/install-az-ps)。</span><span class="sxs-lookup"><span data-stu-id="fa073-109">To use Azure PowerShell cmdlets on these platforms, [Install the Az module](/powershell/azure/install-az-ps).</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="fa073-110">步驟 1:安裝 PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="fa073-110">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="fa073-111">從 PowerShell 資源庫安裝項目需要有 PowerShellGet 模組。</span><span class="sxs-lookup"><span data-stu-id="fa073-111">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="fa073-112">確定您有適當版本的 PowerShellGet 及其他系統需求。</span><span class="sxs-lookup"><span data-stu-id="fa073-112">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="fa073-113">執行下列命令，以查看您的系統上是否已安裝 PowerShellGet。</span><span class="sxs-lookup"><span data-stu-id="fa073-113">Run the following command to see if you have PowerShellGet installed on your system.</span></span>


```powershell-interactive
Get-InstalledModule -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="fa073-114">您應該會看到類似下面的輸出：</span><span class="sxs-lookup"><span data-stu-id="fa073-114">You should see something similar to the following output:</span></span>

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="fa073-115">您需要 PowerShellGet 1.1.2.0 版或更高版本。</span><span class="sxs-lookup"><span data-stu-id="fa073-115">You need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="fa073-116">若要更新 PowerShellGet，請使用下列命令：</span><span class="sxs-lookup"><span data-stu-id="fa073-116">To update PowerShellGet, use the following command:</span></span>

```powershell-interactive
Install-Module PowerShellGet -Force
```

<span data-ttu-id="fa073-117">如果您未安裝 PowerShellGet，請參閱本文的[如何取得 PowerShellGet](#how-to-get-powershellget)一節。</span><span class="sxs-lookup"><span data-stu-id="fa073-117">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget) section of this article.</span></span>

> [!NOTE]
> <span data-ttu-id="fa073-118">若要使用 PowerShellGet，需要有可讓您執行指令碼的執行原則。</span><span class="sxs-lookup"><span data-stu-id="fa073-118">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="fa073-119">如需 PowerShell 的執行原則詳細資訊，請參閱[關於執行原則](/powershell/module/microsoft.powershell.core/about/about_execution_policies)。</span><span class="sxs-lookup"><span data-stu-id="fa073-119">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>
>
> [!IMPORTANT]
> <span data-ttu-id="fa073-120">本文件中所述的模組 AzureRM 會使用 .NET Framework。</span><span class="sxs-lookup"><span data-stu-id="fa073-120">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="fa073-121">這會造成與使用 .NET Core 的 PowerShell 6.0 不相容。</span><span class="sxs-lookup"><span data-stu-id="fa073-121">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="fa073-122">如果您使用 PowerShell 6.0，請遵循[適用於 macOS 和 Linux 的安裝指示](/powershell/azure/install-az-ps)。</span><span class="sxs-lookup"><span data-stu-id="fa073-122">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](/powershell/azure/install-az-ps).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="fa073-123">步驟 2:安裝 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="fa073-123">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="fa073-124">從 PowerShell 資源庫安裝 Azure PowerShell 需要提高的權限。</span><span class="sxs-lookup"><span data-stu-id="fa073-124">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="fa073-125">從提高權限的 PowerShell 工作階段執行下列命令︰</span><span class="sxs-lookup"><span data-stu-id="fa073-125">Run the following command from an elevated PowerShell session:</span></span>

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="fa073-126">根據預設，PowerShell 資源庫未設為 PowerShellGet 的信任存放庫。</span><span class="sxs-lookup"><span data-stu-id="fa073-126">By default, the PowerShell gallery is not configured as a Trusted repository for PowerShellGet.</span></span> <span data-ttu-id="fa073-127">第一次使用 PSGallery 時，您會看到下列提示：</span><span class="sxs-lookup"><span data-stu-id="fa073-127">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

<span data-ttu-id="fa073-128">請回答「是」或「全部皆是」以繼續安裝。</span><span class="sxs-lookup"><span data-stu-id="fa073-128">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="fa073-129">如果您的 NuGet 版本比 2.8.5.201 舊，系統會提示您下載並安裝最新版的 NuGet。</span><span class="sxs-lookup"><span data-stu-id="fa073-129">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="fa073-130">AzureRM 模組是 Azure Resource Manager Cmdlet 的彙總套件模組。</span><span class="sxs-lookup"><span data-stu-id="fa073-130">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="fa073-131">當您安裝 AzureRM 模組時，系統會從 PowerShell 資源庫下載先前未安裝的任何 Azure PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="fa073-131">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded and from the PowerShell Gallery.</span></span>

<span data-ttu-id="fa073-132">若有安裝舊版的 Azure PowerShell，則可能會出現錯誤。</span><span class="sxs-lookup"><span data-stu-id="fa073-132">If you have a previous version of Azure PowerShell installed you may receive an error.</span></span> <span data-ttu-id="fa073-133">若要解決此問題，請參閱本文的[更新為新版的 Azure PowerShell](#update-azps) 小節。</span><span class="sxs-lookup"><span data-stu-id="fa073-133">To resolve this issue, see the [Updating to a new version of Azure PowerShell](#update-azps) section of this article.</span></span>

## <a name="step-3-load-the-azurerm-module"></a><span data-ttu-id="fa073-134">步驟 3：載入 AzureRM 模組</span><span class="sxs-lookup"><span data-stu-id="fa073-134">Step 3: Load the AzureRM module</span></span>

<span data-ttu-id="fa073-135">安裝模組後，您需要將模組載入您的 PowerShell 工作階段。</span><span class="sxs-lookup"><span data-stu-id="fa073-135">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="fa073-136">您應該在一般 (未提高權限) PowerShell 工作階段中執行此動作。</span><span class="sxs-lookup"><span data-stu-id="fa073-136">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="fa073-137">使用 `Import-Module`Cmdlet 載入模組，如下所示︰</span><span class="sxs-lookup"><span data-stu-id="fa073-137">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell-interactive
Import-Module -Name AzureRM
```

## <a name="next-steps"></a><span data-ttu-id="fa073-138">後續步驟</span><span class="sxs-lookup"><span data-stu-id="fa073-138">Next Steps</span></span>

<span data-ttu-id="fa073-139">如需有關使用 Azure PowerShell 的詳細資訊，請參閱下列文章：</span><span class="sxs-lookup"><span data-stu-id="fa073-139">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="fa073-140">開始使用 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="fa073-140">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="fa073-141">報告問題和意見反應</span><span class="sxs-lookup"><span data-stu-id="fa073-141">Reporting issues and feedback</span></span>

<span data-ttu-id="fa073-142">如果您遇到任何與工具有關的錯誤，請在 GitHub 存放庫的[問題](https://github.com/Azure/azure-powershell/issues)一節中提出問題。</span><span class="sxs-lookup"><span data-stu-id="fa073-142">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-powershell/issues) section of our GitHub repo.</span></span> <span data-ttu-id="fa073-143">若要從命令列提供意見反應，請使用 `Send-Feedback` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fa073-143">To provide feedback from the command line, use the `Send-Feedback` cmdlet.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="fa073-144">常見問題集</span><span class="sxs-lookup"><span data-stu-id="fa073-144">Frequently asked questions</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="fa073-145">如何取得 PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="fa073-145">How to get PowerShellGet</span></span>

|<span data-ttu-id="fa073-146">作業系統版本</span><span class="sxs-lookup"><span data-stu-id="fa073-146">OS Version</span></span>|<span data-ttu-id="fa073-147">安裝指示</span><span class="sxs-lookup"><span data-stu-id="fa073-147">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="fa073-148">我有 Windows 10 或 Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fa073-148">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="fa073-149">內建於 OS 包含的 Windows Management Framework (WMF) 5.0</span><span class="sxs-lookup"><span data-stu-id="fa073-149">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="fa073-150">我想要升級至 PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="fa073-150">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="fa073-151">安裝最新版的 WMF</span><span class="sxs-lookup"><span data-stu-id="fa073-151">Install the latest version of WMF</span></span>](https://www.microsoft.com/download/details.aspx?id=54616)|

### <a name="div-idhelpmechoosechecking-the-version-of-azure-powershell"></a><div id="helpmechoose"/><span data-ttu-id="fa073-152">檢查 Azure PowerShell 的版本</span><span class="sxs-lookup"><span data-stu-id="fa073-152">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="fa073-153">雖然我們鼓勵您儘早升級至最新版本，但仍針對數個 Azure PowerShell 版本提供支援。</span><span class="sxs-lookup"><span data-stu-id="fa073-153">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="fa073-154">若要判斷已安裝的 Azure PowerShell 版本，請從命令列執行 `Get-InstalledModule AzureRM`。</span><span class="sxs-lookup"><span data-stu-id="fa073-154">To determine the version of Azure PowerShell you have installed, run `Get-InstalledModule AzureRM` from your command line.</span></span>

```powershell-interactive
Get-InstalledModule AzureRM -AllVersions | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a><span data-ttu-id="fa073-155">對於傳統部署方法的支援</span><span class="sxs-lookup"><span data-stu-id="fa073-155">Support for classic deployment methods</span></span>

<span data-ttu-id="fa073-156">如果您有使用傳統部署模型的部署，則可以安裝 Azure PowerShell 的服務管理版本。</span><span class="sxs-lookup"><span data-stu-id="fa073-156">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="fa073-157">如需詳細資訊，請參閱[安裝 Azure PowerShell 服務管理模組](/powershell/azure/servicemanagement/install-azure-ps)。</span><span class="sxs-lookup"><span data-stu-id="fa073-157">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="fa073-158">Azure 和 AzureRM 模組會共用通用相依性。</span><span class="sxs-lookup"><span data-stu-id="fa073-158">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="fa073-159">若您同時使用 Azure 與 AzureRM 模組，則應該安裝每個套件的相同版本。</span><span class="sxs-lookup"><span data-stu-id="fa073-159">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a name="div-idupdate-azpsupdating-to-a-new-version-of-azure-powershell"></a><div id="update-azps"/><span data-ttu-id="fa073-160">更新為新版的 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="fa073-160">Updating to a new version of Azure PowerShell</span></span>

<span data-ttu-id="fa073-161">若有安裝包括服務管理模組的舊版 Azure PowerShell，則可能會出現下列錯誤：</span><span class="sxs-lookup"><span data-stu-id="fa073-161">If you have a previous version of Azure PowerShell installed that includes the Service Management module, you may receive the following error:</span></span>

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

<span data-ttu-id="fa073-162">如錯誤訊息所述，您必須使用 -AllowClobber 參數來安裝模組。</span><span class="sxs-lookup"><span data-stu-id="fa073-162">As the error message states, you need to use the -AllowClobber parameter to install the module.</span></span> <span data-ttu-id="fa073-163">使用下列命令：</span><span class="sxs-lookup"><span data-stu-id="fa073-163">Use the following command:</span></span>

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="fa073-164">如需詳細資訊，請參閱 [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module) 的說明主題。</span><span class="sxs-lookup"><span data-stu-id="fa073-164">For more information, see the help topic for [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span></span>

### <a name="installing-module-versions-side-by-side"></a><span data-ttu-id="fa073-165">並存安裝模組版本</span><span class="sxs-lookup"><span data-stu-id="fa073-165">Installing module versions side by side</span></span>

<span data-ttu-id="fa073-166">PowerShellGet 安裝方法是唯一支援的多個版本安裝方法。</span><span class="sxs-lookup"><span data-stu-id="fa073-166">The PowerShellGet method of installation is the only method that supports the installation of multiple versions.</span></span> <span data-ttu-id="fa073-167">例如，您的指令碼可能是使用您沒有時間或資源更新的舊版 Azure PowerShell 所撰寫。</span><span class="sxs-lookup"><span data-stu-id="fa073-167">For example, you may have scripts written using a previous version of Azure PowerShell that you don't have the time or resources to updated.</span></span> <span data-ttu-id="fa073-168">下列命令說明如何安裝多個 Azure PowerShell 版本︰</span><span class="sxs-lookup"><span data-stu-id="fa073-168">The following commands illustrate how to install multiple versions of Azure PowerShell:</span></span>

```powershell-interactive
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

<span data-ttu-id="fa073-169">在一個 PowerShell 工作階段中只可以載入一個模組版本。</span><span class="sxs-lookup"><span data-stu-id="fa073-169">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="fa073-170">您必須開啟新的 PowerShell 視窗，並使用 `Import-Module` 來匯入特定版本的 AzureRM Cmdlet︰</span><span class="sxs-lookup"><span data-stu-id="fa073-170">You must open a new PowerShell window and use `Import-Module` to import a specific version of the AzureRM cmdlets:</span></span>

```powershell-interactive
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

> [!NOTE]
> <span data-ttu-id="fa073-171">2\.1.0 版和 1.2.6 版是第一批設計成可並存安裝及使用的模組版本。</span><span class="sxs-lookup"><span data-stu-id="fa073-171">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="fa073-172">載入舊版的 Azure PowerShell 時，會載入不相容的 **AzureRM.Profile** 模組版本。</span><span class="sxs-lookup"><span data-stu-id="fa073-172">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="fa073-173">這會導致每當您執行某個 Cmdlet 時，Cmdlet 都會提示您登入。</span><span class="sxs-lookup"><span data-stu-id="fa073-173">This results in the cmdlets prompting you to sign in whenever you execute a cmdlet.</span></span>

### <a name="other-installation-methods"></a><span data-ttu-id="fa073-174">其他安裝方法</span><span class="sxs-lookup"><span data-stu-id="fa073-174">Other installation methods</span></span>

<span data-ttu-id="fa073-175">如需有關使用 Web Platform Installer 或 MSI 套件進行安裝的資訊，請參閱[其他安裝方法](other-install.md)</span><span class="sxs-lookup"><span data-stu-id="fa073-175">For information about installing using the Web Platform Installer or the MSI Package, see [Other installation methods](other-install.md)</span></span>
