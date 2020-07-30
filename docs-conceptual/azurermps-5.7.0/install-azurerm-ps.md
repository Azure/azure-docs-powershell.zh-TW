---
title: 使用 PowerShellGet 在 Windows 上安裝 Azure PowerShell
description: 如何使用 PowerShellGet 安裝 Azure PowerShell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.openlocfilehash: bd9cbdd66c1a9a623461ca8b0291ac1cb61f1e54
ms.sourcegitcommit: c19bf5a96a82a56e2b1fa9ab5e106690f850cedf
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/27/2020
ms.locfileid: "87177470"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="92240-103">使用 PowerShellGet 在 Windows 上安裝 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="92240-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="92240-104">本文說明使用 PowerShellGet 為 Windows PowerShell 5.x 安裝 Azure PowerShell 模組的步驟。</span><span class="sxs-lookup"><span data-stu-id="92240-104">This article explains the steps to install the Azure PowerShell modules for PowerShell 5.x for Windows using PowerShellGet.</span></span> <span data-ttu-id="92240-105">PowerShellGet 和模組管理是安裝 Azure PowerShell 的偏好方式，但是如果您想要使用 Web Platform Installer 或 MSI 套件來安裝，請參閱[其他安裝方法](other-install.md)。</span><span class="sxs-lookup"><span data-stu-id="92240-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="92240-106">這個版本的 Azure PowerShell 不支援 Azure 傳統部署模型。</span><span class="sxs-lookup"><span data-stu-id="92240-106">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="92240-107">如需傳統部署的支援，請遵循[安裝 Azure PowerShell 服務管理模組](/powershell/azure/servicemanagement/install-azure-ps)中的指示。</span><span class="sxs-lookup"><span data-stu-id="92240-107">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="92240-108">AzureRM 模組不支援 macOS 或 Linux。</span><span class="sxs-lookup"><span data-stu-id="92240-108">The AzureRM module is not supported for macOS or Linux.</span></span> <span data-ttu-id="92240-109">若要在這些平台上使用 Azure PowerShell Cmdlet，請[安裝 Az 模組](/powershell/azure/install-az-ps)。</span><span class="sxs-lookup"><span data-stu-id="92240-109">To use Azure PowerShell cmdlets on these platforms, [Install the Az module](/powershell/azure/install-az-ps).</span></span>

## <a name="requirements"></a><span data-ttu-id="92240-110">需求</span><span class="sxs-lookup"><span data-stu-id="92240-110">Requirements</span></span>

<span data-ttu-id="92240-111">若要安裝 Azure PowerShell，您需要 PowerShellGet 1.1.2.0 版或更高版本。</span><span class="sxs-lookup"><span data-stu-id="92240-111">To install Azure PowerShell, you need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="92240-112">若要檢查您的系統上是否可使用，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="92240-112">To check if it is available on your system, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name PowerShellGet -AllVersions | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="92240-113">您應該會看到類似下面的輸出：</span><span class="sxs-lookup"><span data-stu-id="92240-113">You should see something similar to the following output:</span></span>

```output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="92240-114">若您需要更新 PowerShellGet 的安裝，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="92240-114">If you need to update your installation of PowerShellGet, run the following command:</span></span>

```powershell-interactive
Install-Module PowerShellGet -Force
```

<span data-ttu-id="92240-115">若您尚未安裝 PowerShellGet，請遵循下表中適用您系統的指示。</span><span class="sxs-lookup"><span data-stu-id="92240-115">If you don't have PowerShellGet installed, follow the instructions in the table below for your system.</span></span>

|<span data-ttu-id="92240-116">狀況</span><span class="sxs-lookup"><span data-stu-id="92240-116">Scenario</span></span>|<span data-ttu-id="92240-117">安裝指示</span><span class="sxs-lookup"><span data-stu-id="92240-117">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="92240-118">Windows 10</span><span class="sxs-lookup"><span data-stu-id="92240-118">Windows 10</span></span><br/><span data-ttu-id="92240-119">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="92240-119">Windows Server 2016</span></span>|<span data-ttu-id="92240-120">內建於 OS 包含的 Windows Management Framework (WMF) 5.0</span><span class="sxs-lookup"><span data-stu-id="92240-120">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="92240-121">升級至 PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="92240-121">Upgrade to PowerShell 5</span></span>| <ol><li>[<span data-ttu-id="92240-122">安裝最新版的 WMF</span><span class="sxs-lookup"><span data-stu-id="92240-122">Install the latest version of WMF</span></span>](https://www.microsoft.com/download/details.aspx?id=54616)</li><li><span data-ttu-id="92240-123">執行以下命令：</span><span class="sxs-lookup"><span data-stu-id="92240-123">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|
|<span data-ttu-id="92240-124">Windows 與 PowerShell 3 或 PowerShell 4</span><span class="sxs-lookup"><span data-stu-id="92240-124">Windows with PowerShell 3 or PowerShell 4</span></span>|<ol><span data-ttu-id="92240-125"><il>[取得 PackageManagement 模組](https://go.microsoft.com/fwlink/?LinkID=746217)</il></span><span class="sxs-lookup"><span data-stu-id="92240-125"><il>[Get the PackageManagement modules](https://go.microsoft.com/fwlink/?LinkID=746217)</il></span></span><li><span data-ttu-id="92240-126">執行以下命令：</span><span class="sxs-lookup"><span data-stu-id="92240-126">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|

> [!NOTE]
> <span data-ttu-id="92240-127">若要使用 PowerShellGet，需要有可讓您執行指令碼的執行原則。</span><span class="sxs-lookup"><span data-stu-id="92240-127">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="92240-128">如需 PowerShell 的執行原則詳細資訊，請參閱[關於執行原則](/powershell/module/microsoft.powershell.core/about/about_execution_policies)。</span><span class="sxs-lookup"><span data-stu-id="92240-128">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>
>
> [!IMPORTANT]
> <span data-ttu-id="92240-129">本文件中所述的模組 AzureRM 會使用 .NET Framework。</span><span class="sxs-lookup"><span data-stu-id="92240-129">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="92240-130">這會造成與使用 .NET Core 的 PowerShell 6.0 不相容。</span><span class="sxs-lookup"><span data-stu-id="92240-130">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="92240-131">如果您使用 PowerShell 6.0，請遵循[適用於 macOS 和 Linux 的安裝指示](/powershell/azure/install-az-ps)。</span><span class="sxs-lookup"><span data-stu-id="92240-131">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](/powershell/azure/install-az-ps).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="92240-132">安裝 Azure PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="92240-132">Install the Azure PowerShell module</span></span>

<span data-ttu-id="92240-133">您需要較高的權限，以從 PowerShell 資源庫安裝模組。</span><span class="sxs-lookup"><span data-stu-id="92240-133">You need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="92240-134">若要安裝 Azure PowerShell，請在已提升權限的工作階段中執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="92240-134">To install Azure PowerShell, run the following command in an elevated session:</span></span>

```powershell-interactive
Install-Module -Name AzureRM
```

> [!NOTE]
> <span data-ttu-id="92240-135">如果您的 NuGet 版本比 2.8.5.201 舊，系統會提示您下載並安裝最新版的 NuGet。</span><span class="sxs-lookup"><span data-stu-id="92240-135">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="92240-136">根據預設，PowerShell 資源庫未設為 PowerShellGet 的信任存放庫。</span><span class="sxs-lookup"><span data-stu-id="92240-136">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="92240-137">第一次使用 PSGallery 時，您會看到下列提示：</span><span class="sxs-lookup"><span data-stu-id="92240-137">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="92240-138">請回答 `Yes` 或 `Yes to All` 以繼續安裝。</span><span class="sxs-lookup"><span data-stu-id="92240-138">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="92240-139">`AzureRM` 模組是 Azure PowerShell Cmdlet 的彙總套件模組。</span><span class="sxs-lookup"><span data-stu-id="92240-139">The `AzureRM` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="92240-140">安裝此項目會下載所有可用的 Azure Resource Manager 模組，並使這些模組的 Cmdlet 可供使用。</span><span class="sxs-lookup"><span data-stu-id="92240-140">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="92240-141">登入</span><span class="sxs-lookup"><span data-stu-id="92240-141">Sign in</span></span>

<span data-ttu-id="92240-142">若要開始使用 Azure PowerShell，您必須使用 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) Cmdlet 將 `AzureRM` 載入您目前的 PowerShell 工作階段，然後使用您的 Azure 認證登入。</span><span class="sxs-lookup"><span data-stu-id="92240-142">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="92240-143">您必須針對每個啟動的新 PowerShell 工作階段重複這些步驟。</span><span class="sxs-lookup"><span data-stu-id="92240-143">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="92240-144">自動匯入 `AzureRM` 模組需要設定 PowerShell 設定檔，您可以在[關於設定檔](/powershell/module/microsoft.powershell.core/about/about_profiles)中加以了解。</span><span class="sxs-lookup"><span data-stu-id="92240-144">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="92240-145">若要了解如何在工作階段之間保存您的 Azure 登入，請參閱[在 PowerShell 工作階段之間保存使用者認證](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="92240-145">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="92240-146">更新 Azure PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="92240-146">Update the Azure PowerShell module</span></span>

<span data-ttu-id="92240-147">您可以執行 [Update-Module](/powershell/module/powershellget/update-module) 來更新您的 Azure PowerShell 安裝。</span><span class="sxs-lookup"><span data-stu-id="92240-147">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="92240-148">這個命令「不會」將舊版解除安裝。</span><span class="sxs-lookup"><span data-stu-id="92240-148">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name AzureRM
```

<span data-ttu-id="92240-149">如果您想要從系統中移除較舊版本的 Azure PowerShell，請參閱[將 Azure PowerShell 模組解除安裝](uninstall-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="92240-149">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="92240-150">使用多個版本的 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="92240-150">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="92240-151">可以安裝多個版本的 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="92240-151">It's possible to install multiple versions of Azure PowerShell.</span></span> <span data-ttu-id="92240-152">如果您使用內部部署 Azure Stack 資源、執行較舊版本的 Windows 而無法更新至 PowerShell 5.0，或使用 Azure 傳統部署模型，可能需要一個以上的版本。</span><span class="sxs-lookup"><span data-stu-id="92240-152">You might need more than one version if you work with on-premises Azure Stack resources, run an older version of Windows that you can't update to PowerShell 5.0, or use the Azure classic deployment model.</span></span> <span data-ttu-id="92240-153">若要安裝較舊的版本，請在安裝時提供 `-RequiredVersion` 引數。</span><span class="sxs-lookup"><span data-stu-id="92240-153">To install an older version, provide the `-RequiredVersion` argument when installing.</span></span>

```powershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

<span data-ttu-id="92240-154">當您載入 Azure PowerShell 模組時，預設會載入最新版本。</span><span class="sxs-lookup"><span data-stu-id="92240-154">When loading the Azure PowerShell module the latest version is loaded by default.</span></span> <span data-ttu-id="92240-155">若要載入不同的版本，請提供 `-RequiredVersion` 引數。</span><span class="sxs-lookup"><span data-stu-id="92240-155">To load a different version, provide the `-RequiredVersion` argument.</span></span>

```powershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a><span data-ttu-id="92240-156">提供意見反應</span><span class="sxs-lookup"><span data-stu-id="92240-156">Provide feedback</span></span>

<span data-ttu-id="92240-157">如果您在使用 Azure Powershell 時發現錯誤，請[在 GitHub 上提出問題](https://github.com/Azure/azure-powershell/issues)。</span><span class="sxs-lookup"><span data-stu-id="92240-157">If you find a bug when using Azure Powershell, please [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="92240-158">若要從命令列提供意見反應，請使用 [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="92240-158">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="92240-159">後續步驟</span><span class="sxs-lookup"><span data-stu-id="92240-159">Next Steps</span></span>

<span data-ttu-id="92240-160">若要開始使用 Azure PowerShell，請參閱[開始使用 Azure PowerShell](get-started-azureps.md) 以深入了解模組及其功能。</span><span class="sxs-lookup"><span data-stu-id="92240-160">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>
