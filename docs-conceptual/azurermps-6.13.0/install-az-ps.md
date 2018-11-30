---
title: 使用 PowerShellGet 安裝 Azure PowerShell 'Az'
description: 如何使用 PowerShellGet 在 Windows、macOS 和 Linux 上安裝 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/26/2018
ms.openlocfilehash: 3d52b18750341f220dc8e10d6bf89796457c5a10
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/29/2018
ms.locfileid: "52588174"
---
# <a name="install-the-azure-powershell-az-module"></a><span data-ttu-id="dd939-103">安裝 Azure PowerShell 'Az' 模組</span><span class="sxs-lookup"><span data-stu-id="dd939-103">Install the Azure PowerShell 'Az' module</span></span>

<span data-ttu-id="dd939-104">本文說明如何使用 PowerShellGet 安裝 Azure PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="dd939-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="dd939-105">這些指示適用於 Windows、macOS 和 Linux 平台。</span><span class="sxs-lookup"><span data-stu-id="dd939-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="dd939-106">在 Az 預覽版本中，不支援任何其他安裝方法。</span><span class="sxs-lookup"><span data-stu-id="dd939-106">For the preview release of Az, no other install methods are supported.</span></span> 

## <a name="requirements"></a><span data-ttu-id="dd939-107">需求</span><span class="sxs-lookup"><span data-stu-id="dd939-107">Requirements</span></span>

<span data-ttu-id="dd939-108">Azure PowerShell 可搭配 Windows 上的 PowerShell 5.x 或任何平台上的 PowerShell 6.x 運作。</span><span class="sxs-lookup"><span data-stu-id="dd939-108">Azure PowerShell works with either PowerShell 5.x on Windows, or PowerShell 6.x on any platform.</span></span> <span data-ttu-id="dd939-109">若要檢查您電腦上執行的 PowerShell 版本，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="dd939-109">To check the version of PowerShell running on your machine, run the following command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="dd939-110">如果您有過時的版本或需要安裝 PowerShell，請參閱[安裝各種版本的 PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6)。</span><span class="sxs-lookup"><span data-stu-id="dd939-110">If you have an outdated version or need to install PowerShell, see [Installing various versions of PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6).</span></span> <span data-ttu-id="dd939-111">適用於您平台的安裝資訊是連結自該頁面。</span><span class="sxs-lookup"><span data-stu-id="dd939-111">Install information for your platform is linked from that page.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="dd939-112">安裝 Azure PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="dd939-112">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="dd939-113">您可以同時安裝 `AzureRM` 和 `Az` 模組。</span><span class="sxs-lookup"><span data-stu-id="dd939-113">You can have both the `AzureRM` and `Az` modules installed at the same time.</span></span> <span data-ttu-id="dd939-114">若您已安裝了兩個模組，__請勿啟用別名__。</span><span class="sxs-lookup"><span data-stu-id="dd939-114">If you have both modules installed, __don't enable aliases__.</span></span>
> <span data-ttu-id="dd939-115">啟用別名會讓 `AzureRM` Cmdlet 和 `Az` 命令別名產生衝突，且可能導致未預期的行為。</span><span class="sxs-lookup"><span data-stu-id="dd939-115">Enabling aliases will cause conflicts between `AzureRM` cmdlets and `Az` command aliases, and could cause unexpected behavior.</span></span>
> <span data-ttu-id="dd939-116">建議您在安裝 `Az` 模組之前，先將 `AzureRM` 解除安裝。</span><span class="sxs-lookup"><span data-stu-id="dd939-116">It's recommended that before installing the `Az` module, you uninstall `AzureRM`.</span></span> <span data-ttu-id="dd939-117">您可以隨時將 `AzureRM` 解除安裝，或啟用別名。</span><span class="sxs-lookup"><span data-stu-id="dd939-117">You can always uninstall `AzureRM` or enable aliases at any time.</span></span> <span data-ttu-id="dd939-118">如需解除安裝作的指示，請參閱[將 Azure PowerShell 模組 (AzureRM) 解除安裝](uninstall-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="dd939-118">For uninstall instructions, see [Uninstall the Azure PowerShell module (AzureRM)](uninstall-azurerm-ps.md).</span></span> 

<span data-ttu-id="dd939-119">若要在全域範圍安裝模組，您需要較高的權限，以從 PowerShell 資源庫安裝模組。</span><span class="sxs-lookup"><span data-stu-id="dd939-119">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="dd939-120">若要安裝 Azure PowerShell，請在提升權限的工作階段中執行下列命令 (在 Windows 上「以系統管理員身分執行」，或在 macOS 或 Linux 上使用超級使用者權限執行)：</span><span class="sxs-lookup"><span data-stu-id="dd939-120">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="dd939-121">如果您沒有系統管理員權限，藉由新增 `-Scope` 引數，即可為目前使用者進行安裝。</span><span class="sxs-lookup"><span data-stu-id="dd939-121">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="dd939-122">根據預設，PowerShell 資源庫未設為 PowerShellGet 的信任存放庫。</span><span class="sxs-lookup"><span data-stu-id="dd939-122">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="dd939-123">第一次使用 PSGallery 時，您會看到下列提示：</span><span class="sxs-lookup"><span data-stu-id="dd939-123">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="dd939-124">請回答 `Yes` 或 `Yes to All` 以繼續安裝。</span><span class="sxs-lookup"><span data-stu-id="dd939-124">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="dd939-125">`Az` 模組是 Azure PowerShell Cmdlet 的彙總套件模組。</span><span class="sxs-lookup"><span data-stu-id="dd939-125">The `Az` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="dd939-126">安裝此項目會下載所有可用的 Azure Resource Manager 模組，並使這些模組的 Cmdlet 可供使用。</span><span class="sxs-lookup"><span data-stu-id="dd939-126">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="dd939-127">登入</span><span class="sxs-lookup"><span data-stu-id="dd939-127">Sign in</span></span>

<span data-ttu-id="dd939-128">若要開始使用 Azure PowerShell，請使用您的 Azure 認證登入。</span><span class="sxs-lookup"><span data-stu-id="dd939-128">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="dd939-129">如果您已停用自動載入模組功能，則必須透過 `Import-Module Az` 來手動匯入模組。</span><span class="sxs-lookup"><span data-stu-id="dd939-129">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="dd939-130">因為模組的結構化方式，這可能需要幾秒鐘的時間。</span><span class="sxs-lookup"><span data-stu-id="dd939-130">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="dd939-131">您必須針對每個啟動的新 PowerShell 工作階段重複這些步驟。</span><span class="sxs-lookup"><span data-stu-id="dd939-131">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="dd939-132">若要了解如何在 PowerShell 工作階段之間保存您的 Azure 登入，請參閱[在 PowerShell 工作階段之間保存使用者認證](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="dd939-132">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="dd939-133">更新 Azure PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="dd939-133">Update the Azure PowerShell module</span></span>

<span data-ttu-id="dd939-134">您可以執行 [Update-Module](/powershell/module/powershellget/update-module) 來更新您的 Azure PowerShell 安裝。</span><span class="sxs-lookup"><span data-stu-id="dd939-134">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="dd939-135">這個命令「不會」將舊版解除安裝。</span><span class="sxs-lookup"><span data-stu-id="dd939-135">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name Az
```

<span data-ttu-id="dd939-136">如果您想要從系統中移除較舊版本的 Azure PowerShell，請參閱[將 Azure PowerShell 模組解除安裝](uninstall-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="dd939-136">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="dd939-137">使用多個版本的 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="dd939-137">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="dd939-138">您可以安裝多個版本的 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="dd939-138">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="dd939-139">若要檢查是否安裝了多個 Azure PowerShell 版本，請使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="dd939-139">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-Module -Name Az -List | select Name,Version
```

<span data-ttu-id="dd939-140">若想移除 Azure PowerShell 版本，請參閱[解除安裝 Azure PowerShell 模組](uninstall-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="dd939-140">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="dd939-141">您可使用 `-RequiredVersion` 引數搭配 `Install-Module` 和 `Import-Module`，以載入特定版本的 `Az` 模組：</span><span class="sxs-lookup"><span data-stu-id="dd939-141">You can load a specific version of the `Az` module by using the `-RequiredVersion` argument with `Install-Module` and `Import-Module`:</span></span>

```powershell-interactive
Install-Module -Name Az -RequiredVersion 0.4.0
Import-Module -Name Az -RequiredVersion 0.4.0
```

<span data-ttu-id="dd939-142">如果您已安裝多個版本的模組，則預設會載入最新版本。</span><span class="sxs-lookup"><span data-stu-id="dd939-142">If you have more than one version of the module installed, the latest version is loaded by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="dd939-143">提供意見反應</span><span class="sxs-lookup"><span data-stu-id="dd939-143">Provide feedback</span></span>

<span data-ttu-id="dd939-144">如果您在使用 Azure Powershell 時發現錯誤，請[在 GitHub 上提出問題](https://github.com/Azure/azure-powershell/issues)。</span><span class="sxs-lookup"><span data-stu-id="dd939-144">If you find a bug when using Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="dd939-145">若要從命令列提供意見反應，請使用 [Send-Feedback](/powershell/module/az.profile/send-feedback) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dd939-145">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="dd939-146">後續步驟</span><span class="sxs-lookup"><span data-stu-id="dd939-146">Next Steps</span></span>

<span data-ttu-id="dd939-147">若要開始使用 Azure PowerShell，請參閱[開始使用 Azure PowerShell](get-started-azureps.md) 以深入了解模組及其功能。</span><span class="sxs-lookup"><span data-stu-id="dd939-147">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>
