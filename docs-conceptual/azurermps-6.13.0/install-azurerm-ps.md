---
title: 使用 PowerShellGet 在 Windows 上安裝 Azure PowerShell
description: 如何使用 PowerShellGet 安裝 Azure PowerShell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: b04d4070e420f2d1e64f233eda6b3e250f8bb68c
ms.sourcegitcommit: 9f5c7d231b069ad501729bf015a829f3fe89bc6a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/28/2020
ms.locfileid: "84122041"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="c4aaa-103">使用 PowerShellGet 在 Windows 上安裝 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c4aaa-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="c4aaa-104">本文說明使用 PowerShellGet 為 Windows PowerShell 5.x 安裝 Azure PowerShell 模組的步驟。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-104">This article explains the steps to install the Azure PowerShell modules for PowerShell 5.x for Windows using PowerShellGet.</span></span> <span data-ttu-id="c4aaa-105">PowerShellGet 和模組管理是安裝 Azure PowerShell 的偏好方式，但是如果您想要使用 Web Platform Installer 或 MSI 套件來安裝，請參閱[其他安裝方法](other-install.md)。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="c4aaa-106">這個版本的 Azure PowerShell 不支援 Azure 傳統部署模型。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-106">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="c4aaa-107">如需傳統部署的支援，請遵循[安裝 Azure PowerShell 服務管理模組](/powershell/azure/servicemanagement/install-azure-ps)中的指示。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-107">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c4aaa-108">AzureRM 模組不支援 macOS 或 Linux。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-108">The AzureRM module is not supported for macOS or Linux.</span></span> <span data-ttu-id="c4aaa-109">若要在這些平台上使用 Azure PowerShell Cmdlet，請[安裝 Az 模組](/powershell/azure/install-az-ps)。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-109">To use Azure PowerShell cmdlets on these platforms, [Install the Az module](/powershell/azure/install-az-ps).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4aaa-110">需求</span><span class="sxs-lookup"><span data-stu-id="c4aaa-110">Requirements</span></span>

<span data-ttu-id="c4aaa-111">自 Azure PowerShell 6.0 版開始，Azure PowerShell 需要 PowerShell 5.0 版。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-111">Starting with Azure PowerShell version 6.0, Azure PowerShell requires PowerShell version 5.0.</span></span> <span data-ttu-id="c4aaa-112">若要檢查您電腦上執行的 PowerShell 版本，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="c4aaa-112">To check the version of PowerShell running on your machine, run the following command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="c4aaa-113">如果您的版本過期，請參閱[升級現有的 Windows PowerShell](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell)。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-113">If you have an outdated version, see [Upgrading existing Windows PowerShell](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c4aaa-114">本文件中所述的模組 AzureRM 會使用 .NET Framework。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-114">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="c4aaa-115">這會造成與使用 .NET Core 的 PowerShell 6.0 不相容。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-115">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="c4aaa-116">如果您使用 PowerShell 6.0，請遵循[適用於 macOS 和 Linux 的安裝指示](install-azurermps-maclinux.md)。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-116">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="c4aaa-117">安裝 Azure PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="c4aaa-117">Install the Azure PowerShell module</span></span>

<span data-ttu-id="c4aaa-118">您需要較高的權限，以從 PowerShell 資源庫安裝模組。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-118">You need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="c4aaa-119">若要安裝 Azure PowerShell，請在已提升權限的工作階段中執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="c4aaa-119">To install Azure PowerShell, run the following command in an elevated session:</span></span>

```azurepowershell-interactive
Install-Module -Name AzureRM -AllowClobber
```

> [!NOTE]
> <span data-ttu-id="c4aaa-120">如果您的 NuGet 版本比 2.8.5.201 舊，系統會提示您下載並安裝最新版的 NuGet。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-120">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="c4aaa-121">根據預設，PowerShell 資源庫未設為 PowerShellGet 的信任存放庫。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-121">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="c4aaa-122">第一次使用 PSGallery 時，您會看到下列提示：</span><span class="sxs-lookup"><span data-stu-id="c4aaa-122">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="c4aaa-123">請回答 `Yes` 或 `Yes to All` 以繼續安裝。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-123">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="c4aaa-124">`AzureRM` 模組是 Azure PowerShell Cmdlet 的彙總套件模組。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-124">The `AzureRM` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="c4aaa-125">安裝此項目會下載所有可用的 Azure Resource Manager 模組，並使這些模組的 Cmdlet 可供使用。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-125">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="c4aaa-126">登入</span><span class="sxs-lookup"><span data-stu-id="c4aaa-126">Sign in</span></span>

<span data-ttu-id="c4aaa-127">若要開始使用 Azure PowerShell，請使用您的 Azure 認證登入。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-127">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```azurepowershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
> <span data-ttu-id="c4aaa-128">如果您已停用自動載入模組功能，則必須透過 `Import-Module AzureRM` 來手動匯入模組。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-128">If you've disabled module autoloading, you need to manually import the module with `Import-Module AzureRM`.</span></span> <span data-ttu-id="c4aaa-129">因為模組的結構化方式，這可能需要幾秒鐘的時間。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-129">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="c4aaa-130">您必須針對每個啟動的新 PowerShell 工作階段重複這些步驟。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-130">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="c4aaa-131">若要了解如何在 PowerShell 工作階段之間保存您的 Azure 登入，請參閱[在 PowerShell 工作階段之間保存使用者認證](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-131">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="c4aaa-132">更新 Azure PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="c4aaa-132">Update the Azure PowerShell module</span></span>

<span data-ttu-id="c4aaa-133">您可以執行 [Update-Module](/powershell/module/powershellget/update-module) 來更新您的 Azure PowerShell 安裝。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-133">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="c4aaa-134">這個命令「不會」將舊版解除安裝。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-134">This command does **not** uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name AzureRM
```

<span data-ttu-id="c4aaa-135">如果您想要從系統中移除較舊版本的 Azure PowerShell，請參閱[將 Azure PowerShell 模組解除安裝](uninstall-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-135">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="c4aaa-136">使用多個版本的 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c4aaa-136">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="c4aaa-137">您可以安裝多個版本的 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-137">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="c4aaa-138">若要檢查是否安裝了多個 Azure PowerShell 版本，請使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="c4aaa-138">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```azurepowershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions | select Name,Version
```

<span data-ttu-id="c4aaa-139">若想移除 Azure PowerShell 版本，請參閱[解除安裝 Azure PowerShell 模組](uninstall-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-139">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="c4aaa-140">如果您使用內部部署 Azure Stack 資源、執行較舊的 Windows 版本，或使用 Azure 傳統部署模型，則可能需要多個版本。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-140">You might need more than one version if you work with on-premises Azure Stack resources, run an older version of Windows, or use the Azure classic deployment model.</span></span> <span data-ttu-id="c4aaa-141">若要安裝較舊的版本，請在安裝時提供 `-RequiredVersion` 引數。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-141">To install an older version, provide the `-RequiredVersion` argument when installing.</span></span>

```azurepowershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

<span data-ttu-id="c4aaa-142">當您載入 Azure PowerShell 模組時，預設會載入最新版本。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-142">When loading the Azure PowerShell module the latest version is loaded by default.</span></span> <span data-ttu-id="c4aaa-143">若要載入不同的版本，請提供 `-RequiredVersion` 引數。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-143">To load a different version, provide the `-RequiredVersion` argument.</span></span>

```azurepowershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a><span data-ttu-id="c4aaa-144">提供意見反應</span><span class="sxs-lookup"><span data-stu-id="c4aaa-144">Provide feedback</span></span>

<span data-ttu-id="c4aaa-145">如果您在使用 Azure Powershell 時發現錯誤，請[在 GitHub 上提出問題](https://github.com/Azure/azure-powershell/issues)。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-145">If you find a bug when using Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="c4aaa-146">若要從命令列提供意見反應，請使用 [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-146">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c4aaa-147">後續步驟</span><span class="sxs-lookup"><span data-stu-id="c4aaa-147">Next Steps</span></span>

<span data-ttu-id="c4aaa-148">若要開始使用 Azure PowerShell，請參閱[開始使用 Azure PowerShell](get-started-azureps.md) 以深入了解模組及其功能。</span><span class="sxs-lookup"><span data-stu-id="c4aaa-148">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>
