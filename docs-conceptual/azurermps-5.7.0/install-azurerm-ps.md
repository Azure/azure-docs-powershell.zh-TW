---
title: 使用 PowerShellGet 在 Windows 上安裝 Azure PowerShell
description: 如何使用 PowerShellGet 安裝 Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.openlocfilehash: 5561fd7a1b2018c126da26eaad7d51049497ec8e
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2019
ms.locfileid: "56153022"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="f70e8-103">使用 PowerShellGet 在 Windows 上安裝 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f70e8-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

<span data-ttu-id="f70e8-104">本文說明在 Windows 環境中使用 PowerShellGet 安裝 Azure PowerShell 模組的步驟。</span><span class="sxs-lookup"><span data-stu-id="f70e8-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment using PowerShellGet.</span></span> <span data-ttu-id="f70e8-105">PowerShellGet 和模組管理是安裝 Azure PowerShell 的偏好方式，但是如果您想要使用 Web Platform Installer 或 MSI 套件來安裝，請參閱[其他安裝方法](other-install.md)。</span><span class="sxs-lookup"><span data-stu-id="f70e8-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="f70e8-106">如需在其他平台上安裝 Azure PowerShell 的指示，請參閱[在 macOS 與 Linux 上安裝和設定 Azure PowerShell](install-azurermps-maclinux.md)。</span><span class="sxs-lookup"><span data-stu-id="f70e8-106">For instructions to install Azure PowerShell on other platforms, see [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f70e8-107">需求</span><span class="sxs-lookup"><span data-stu-id="f70e8-107">Requirements</span></span>

<span data-ttu-id="f70e8-108">若要安裝 Azure PowerShell，您需要 PowerShellGet 1.1.2.0 版或更高版本。</span><span class="sxs-lookup"><span data-stu-id="f70e8-108">To install Azure PowerShell, you need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="f70e8-109">若要檢查您的系統上是否可使用，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="f70e8-109">To check if it is available on your system, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name PowerShellGet -AllVersions | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="f70e8-110">您應該會看到類似下面的輸出：</span><span class="sxs-lookup"><span data-stu-id="f70e8-110">You should see something similar to the following output:</span></span>

```output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="f70e8-111">若您需要更新 PowerShellGet 的安裝，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="f70e8-111">If you need to update your installation of PowerShellGet, run the following command:</span></span>

```powershell-interactive
Install-Module PowerShellGet -Force
```

<span data-ttu-id="f70e8-112">若您尚未安裝 PowerShellGet，請遵循下表中適用您系統的指示。</span><span class="sxs-lookup"><span data-stu-id="f70e8-112">If you don't have PowerShellGet installed, follow the instructions in the table below for your system.</span></span>

|<span data-ttu-id="f70e8-113">案例</span><span class="sxs-lookup"><span data-stu-id="f70e8-113">Scenario</span></span>|<span data-ttu-id="f70e8-114">安裝指示</span><span class="sxs-lookup"><span data-stu-id="f70e8-114">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="f70e8-115">Windows 10</span><span class="sxs-lookup"><span data-stu-id="f70e8-115">Windows 10</span></span><br/><span data-ttu-id="f70e8-116">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f70e8-116">Windows Server 2016</span></span>|<span data-ttu-id="f70e8-117">內建於 OS 包含的 Windows Management Framework (WMF) 5.0</span><span class="sxs-lookup"><span data-stu-id="f70e8-117">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="f70e8-118">升級至 PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="f70e8-118">Upgrade to PowerShell 5</span></span>| <ol><li>[<span data-ttu-id="f70e8-119">安裝最新版的 WMF</span><span class="sxs-lookup"><span data-stu-id="f70e8-119">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)</li><li><span data-ttu-id="f70e8-120">執行以下命令：</span><span class="sxs-lookup"><span data-stu-id="f70e8-120">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|
|<span data-ttu-id="f70e8-121">Windows 與 PowerShell 3 或 PowerShell 4</span><span class="sxs-lookup"><span data-stu-id="f70e8-121">Windows with PowerShell 3 or PowerShell 4</span></span>|<ol><span data-ttu-id="f70e8-122"><il>[取得 PackageManagement 模組](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span><span class="sxs-lookup"><span data-stu-id="f70e8-122"><il>[Get the PackageManagement modules](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span></span><li><span data-ttu-id="f70e8-123">執行以下命令：</span><span class="sxs-lookup"><span data-stu-id="f70e8-123">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|

> [!NOTE]
> <span data-ttu-id="f70e8-124">若要使用 PowerShellGet，需要有可讓您執行指令碼的執行原則。</span><span class="sxs-lookup"><span data-stu-id="f70e8-124">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="f70e8-125">如需 PowerShell 的執行原則詳細資訊，請參閱[關於執行原則](/powershell/module/microsoft.powershell.core/about/about_execution_policies)。</span><span class="sxs-lookup"><span data-stu-id="f70e8-125">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>
>
> [!IMPORTANT]
> <span data-ttu-id="f70e8-126">本文件中所述的模組 AzureRM 會使用 .NET Framework。</span><span class="sxs-lookup"><span data-stu-id="f70e8-126">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="f70e8-127">這會造成與使用 .NET Core 的 PowerShell 6.0 不相容。</span><span class="sxs-lookup"><span data-stu-id="f70e8-127">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="f70e8-128">如果您使用 PowerShell 6.0，請遵循[適用於 macOS 和 Linux 的安裝指示](install-azurermps-maclinux.md)。</span><span class="sxs-lookup"><span data-stu-id="f70e8-128">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="f70e8-129">安裝 Azure PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="f70e8-129">Install the Azure PowerShell module</span></span>

<span data-ttu-id="f70e8-130">您需要較高的權限，以從 PowerShell 資源庫安裝模組。</span><span class="sxs-lookup"><span data-stu-id="f70e8-130">You need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="f70e8-131">若要安裝 Azure PowerShell，請在已提升權限的工作階段中執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="f70e8-131">To install Azure PowerShell, run the following command in an elevated session:</span></span>

```powershell-interactive
Install-Module -Name AzureRM
```

> [!NOTE]
> <span data-ttu-id="f70e8-132">如果您的 NuGet 版本比 2.8.5.201 舊，系統會提示您下載並安裝最新版的 NuGet。</span><span class="sxs-lookup"><span data-stu-id="f70e8-132">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="f70e8-133">根據預設，PowerShell 資源庫未設為 PowerShellGet 的信任存放庫。</span><span class="sxs-lookup"><span data-stu-id="f70e8-133">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="f70e8-134">第一次使用 PSGallery 時，您會看到下列提示：</span><span class="sxs-lookup"><span data-stu-id="f70e8-134">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="f70e8-135">請回答 `Yes` 或 `Yes to All` 以繼續安裝。</span><span class="sxs-lookup"><span data-stu-id="f70e8-135">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="f70e8-136">`AzureRM` 模組是 Azure PowerShell Cmdlet 的彙總套件模組。</span><span class="sxs-lookup"><span data-stu-id="f70e8-136">The `AzureRM` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="f70e8-137">安裝此項目會下載所有可用的 Azure Resource Manager 模組，並使這些模組的 Cmdlet 可供使用。</span><span class="sxs-lookup"><span data-stu-id="f70e8-137">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="f70e8-138">登入</span><span class="sxs-lookup"><span data-stu-id="f70e8-138">Sign in</span></span>

<span data-ttu-id="f70e8-139">若要開始使用 Azure PowerShell，您必須使用 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) Cmdlet 將 `AzureRM` 載入您目前的 PowerShell 工作階段，然後使用您的 Azure 認證登入。</span><span class="sxs-lookup"><span data-stu-id="f70e8-139">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="f70e8-140">您必須針對每個啟動的新 PowerShell 工作階段重複這些步驟。</span><span class="sxs-lookup"><span data-stu-id="f70e8-140">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="f70e8-141">自動匯入 `AzureRM` 模組需要設定 PowerShell 設定檔，您可以在[關於設定檔](/powershell/module/microsoft.powershell.core/about/about_profiles)中加以了解。</span><span class="sxs-lookup"><span data-stu-id="f70e8-141">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="f70e8-142">若要了解如何在工作階段之間保存您的 Azure 登入，請參閱[在 PowerShell 工作階段之間保存使用者認證](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="f70e8-142">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="f70e8-143">更新 Azure PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="f70e8-143">Update the Azure PowerShell module</span></span>

<span data-ttu-id="f70e8-144">您可以執行 [Update-Module](/powershell/module/powershellget/update-module) 來更新您的 Azure PowerShell 安裝。</span><span class="sxs-lookup"><span data-stu-id="f70e8-144">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="f70e8-145">這個命令「不會」將舊版解除安裝。</span><span class="sxs-lookup"><span data-stu-id="f70e8-145">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name AzureRM
```

<span data-ttu-id="f70e8-146">如果您想要從系統中移除較舊版本的 Azure PowerShell，請參閱[將 Azure PowerShell 模組解除安裝](uninstall-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="f70e8-146">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="f70e8-147">使用多個版本的 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f70e8-147">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="f70e8-148">可以安裝多個版本的 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="f70e8-148">It's possible to install multiple versions of Azure PowerShell.</span></span> <span data-ttu-id="f70e8-149">如果您使用內部部署 Azure Stack 資源、執行較舊版本的 Windows 而無法更新至 PowerShell 5.0，或使用 Azure 傳統部署模型，可能需要一個以上的版本。</span><span class="sxs-lookup"><span data-stu-id="f70e8-149">You might need more than one version if you work with on-premises Azure Stack resources, run an older version of Windows that you can't update to PowerShell 5.0, or use the Azure classic deployment model.</span></span> <span data-ttu-id="f70e8-150">若要安裝較舊的版本，請在安裝時提供 `-RequiredVersion` 引數。</span><span class="sxs-lookup"><span data-stu-id="f70e8-150">To install an older version, provide the `-RequiredVersion` argument when installing.</span></span>

```powershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

<span data-ttu-id="f70e8-151">當您載入 Azure PowerShell 模組時，預設會載入最新版本。</span><span class="sxs-lookup"><span data-stu-id="f70e8-151">When loading the Azure PowerShell module the latest version is loaded by default.</span></span> <span data-ttu-id="f70e8-152">若要載入不同的版本，請提供 `-RequiredVersion` 引數。</span><span class="sxs-lookup"><span data-stu-id="f70e8-152">To load a different version, provide the `-RequiredVersion` argument.</span></span>

```powershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a><span data-ttu-id="f70e8-153">提供意見反應</span><span class="sxs-lookup"><span data-stu-id="f70e8-153">Provide feedback</span></span>

<span data-ttu-id="f70e8-154">如果您在使用 Azure Powershell 時發現錯誤，請[在 GitHub 上提出問題](https://github.com/Azure/azure-powershell/issues)。</span><span class="sxs-lookup"><span data-stu-id="f70e8-154">If you find a bug when using Azure Powershell, please [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="f70e8-155">若要從命令列提供意見反應，請使用 [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f70e8-155">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="f70e8-156">後續步驟</span><span class="sxs-lookup"><span data-stu-id="f70e8-156">Next Steps</span></span>

<span data-ttu-id="f70e8-157">若要開始使用 Azure PowerShell，請參閱[開始使用 Azure PowerShell](get-started-azureps.md) 以深入了解模組及其功能。</span><span class="sxs-lookup"><span data-stu-id="f70e8-157">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>
