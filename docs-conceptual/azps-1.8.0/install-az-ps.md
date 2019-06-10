---
title: 使用 PowerShellGet 安裝 Azure PowerShell
description: 如何使用 PowerShellGet 安裝 Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: d99265c7f156622d876d700106e2b06dd729e8b8
ms.sourcegitcommit: 020c69430358b13cbd99fedd5d56607c9b10047b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/29/2019
ms.locfileid: "66365727"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="22a39-103">安裝 Azure PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="22a39-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="22a39-104">本文說明如何使用 PowerShellGet 安裝 Azure PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="22a39-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="22a39-105">這些指示適用於 Windows、macOS 和 Linux 平台。</span><span class="sxs-lookup"><span data-stu-id="22a39-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="22a39-106">至於 Az 模組，目前不支援其他安裝方法。</span><span class="sxs-lookup"><span data-stu-id="22a39-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="22a39-107">需求</span><span class="sxs-lookup"><span data-stu-id="22a39-107">Requirements</span></span>

<span data-ttu-id="22a39-108">Azure PowerShell 可在 Windows 上與 PowerShell 5.1 或更新版本搭配運作，或在所有平台上與 PowerShell Core 6.x 和更新版本搭配運作。</span><span class="sxs-lookup"><span data-stu-id="22a39-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="22a39-109">如果您不確定是否有 PowerShell，或不確定是在 macOS 還是 Linux 上，請[安裝最新版的 PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core)。</span><span class="sxs-lookup"><span data-stu-id="22a39-109">If you aren't sure if you have PowerShell, or are on macOS or Linux, [install the latest version of PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span></span>

<span data-ttu-id="22a39-110">若要檢查 PowerShell 版本，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="22a39-110">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="22a39-111">若要在 Windows 上的 PowerShell 5.1 中執行 Azure PowerShell：</span><span class="sxs-lookup"><span data-stu-id="22a39-111">To run Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="22a39-112">視需要更新至 [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell)。</span><span class="sxs-lookup"><span data-stu-id="22a39-112">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="22a39-113">如果您是在 Windows 10 上，則已安裝 PowerShell 5.1。</span><span class="sxs-lookup"><span data-stu-id="22a39-113">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="22a39-114">安裝 [.NET Framework 4.7.2 或更新版本](/dotnet/framework/install)。</span><span class="sxs-lookup"><span data-stu-id="22a39-114">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

<span data-ttu-id="22a39-115">使用 PowerShell Core 時，Azure PowerShell 沒有額外的需求。</span><span class="sxs-lookup"><span data-stu-id="22a39-115">There are no additional requirements for Azure PowerShell when using PowerShell Core.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="22a39-116">安裝 Azure PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="22a39-116">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="22a39-117">您可以同時安裝 AzureRM 和 Az 模組。</span><span class="sxs-lookup"><span data-stu-id="22a39-117">You can have both the AzureRM and Az modules installed at the same time.</span></span> <span data-ttu-id="22a39-118">若您已安裝了兩個模組，__請勿啟用別名__。</span><span class="sxs-lookup"><span data-stu-id="22a39-118">If you have both modules installed, __don't enable aliases__.</span></span>
> <span data-ttu-id="22a39-119">啟用別名會讓 AzureRM Cmdlet 和 Az 命令別名產生衝突，且可能導致未預期的行為。</span><span class="sxs-lookup"><span data-stu-id="22a39-119">Enabling aliases will cause conflicts between AzureRM cmdlets and Az command aliases, and could cause unexpected behavior.</span></span>
> <span data-ttu-id="22a39-120">建議您在安裝 Az 模組之前，先將 AzureRM 解除安裝。</span><span class="sxs-lookup"><span data-stu-id="22a39-120">It's recommended that before installing the Az module, you uninstall AzureRM.</span></span> <span data-ttu-id="22a39-121">您可以隨時將 AzureRM 解除安裝，或啟用別名。</span><span class="sxs-lookup"><span data-stu-id="22a39-121">You can always uninstall AzureRM or enable aliases at any time.</span></span> <span data-ttu-id="22a39-122">若要了解 AzureRM 命令別名，請參閱[從 AzureRM 遷移至 Az](migrate-from-azurerm-to-az.md)。</span><span class="sxs-lookup"><span data-stu-id="22a39-122">To learn about the AzureRM command aliases, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
> <span data-ttu-id="22a39-123">如需解除安裝作的指示，請參閱[將 AzureRM 模組解除安裝](uninstall-az-ps.md#uninstall-the-azurerm-module)。</span><span class="sxs-lookup"><span data-stu-id="22a39-123">For uninstall instructions, see [Uninstall the AzureRM module](uninstall-az-ps.md#uninstall-the-azurerm-module).</span></span> 

<span data-ttu-id="22a39-124">若要在全域範圍安裝模組，您需要較高的權限，以從 PowerShell 資源庫安裝模組。</span><span class="sxs-lookup"><span data-stu-id="22a39-124">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="22a39-125">若要安裝 Azure PowerShell，請在提升權限的工作階段中執行下列命令 (在 Windows 上「以系統管理員身分執行」，或在 macOS 或 Linux 上使用超級使用者權限執行)：</span><span class="sxs-lookup"><span data-stu-id="22a39-125">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="22a39-126">如果您沒有系統管理員權限，藉由新增 `-Scope` 引數，即可為目前使用者進行安裝。</span><span class="sxs-lookup"><span data-stu-id="22a39-126">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="22a39-127">根據預設，PowerShell 資源庫未設為 PowerShellGet 的信任存放庫。</span><span class="sxs-lookup"><span data-stu-id="22a39-127">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="22a39-128">第一次使用 PSGallery 時，您會看到下列提示：</span><span class="sxs-lookup"><span data-stu-id="22a39-128">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="22a39-129">請回答 `Yes` 或 `Yes to All` 以繼續安裝。</span><span class="sxs-lookup"><span data-stu-id="22a39-129">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="22a39-130">Az 模組是 Azure PowerShell Cmdlet 的彙總套件模組。</span><span class="sxs-lookup"><span data-stu-id="22a39-130">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="22a39-131">安裝此項目會下載所有可用的 Azure Resource Manager 模組，並使這些模組的 Cmdlet 可供使用。</span><span class="sxs-lookup"><span data-stu-id="22a39-131">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="22a39-132">登入</span><span class="sxs-lookup"><span data-stu-id="22a39-132">Sign in</span></span>

<span data-ttu-id="22a39-133">若要開始使用 Azure PowerShell，請使用您的 Azure 認證登入。</span><span class="sxs-lookup"><span data-stu-id="22a39-133">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="22a39-134">如果您已停用自動載入模組功能，則必須透過 `Import-Module Az` 來手動匯入模組。</span><span class="sxs-lookup"><span data-stu-id="22a39-134">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="22a39-135">因為模組的結構化方式，這可能需要幾秒鐘的時間。</span><span class="sxs-lookup"><span data-stu-id="22a39-135">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="22a39-136">您必須針對每個啟動的新 PowerShell 工作階段重複這些步驟。</span><span class="sxs-lookup"><span data-stu-id="22a39-136">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="22a39-137">若要了解如何在 PowerShell 工作階段之間保存您的 Azure 登入，請參閱[在 PowerShell 工作階段之間保存使用者認證](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="22a39-137">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="22a39-138">更新 Azure PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="22a39-138">Update the Azure PowerShell module</span></span>

<span data-ttu-id="22a39-139">由於 Az 模組的封裝方式，[Update-module](/powershell/module/powershellget/update-module) 命令將不會正確更新您的安裝。</span><span class="sxs-lookup"><span data-stu-id="22a39-139">Because of how the Az module is package, the [Update-Module](/powershell/module/powershellget/update-module) command won't update your installation correctly.</span></span> <span data-ttu-id="22a39-140">Az 在技術上是中繼模組，其中包含與 Azure 服務互動的 Cmdlet 所屬的所有子模組。</span><span class="sxs-lookup"><span data-stu-id="22a39-140">Az is technically a meta-module, encompassing all of the submodules that contain cmdlets to interact with Azure services.</span></span> <span data-ttu-id="22a39-141">這表示，若要更新 Azure PowerShell 模組，您必須__重新安裝__，而不只是__更新__。</span><span class="sxs-lookup"><span data-stu-id="22a39-141">That means that to update the Azure PowerShell module, you will need to __reinstall__, rather than just __update__.</span></span> <span data-ttu-id="22a39-142">其操作方式與安裝相同，但您可能需要新增 `-Force` 引數：</span><span class="sxs-lookup"><span data-stu-id="22a39-142">This is done in the same way as installing, but you may need to add the `-Force` argument:</span></span>

```powershell
Install-Module -Name Az -AllowClobber -Force
```

<span data-ttu-id="22a39-143">雖然這可以覆寫已安裝的模組，但您的系統上仍可能殘留較舊的版本。</span><span class="sxs-lookup"><span data-stu-id="22a39-143">Although this can overwrite installed modules, you may still have older versions left on your system.</span></span>
<span data-ttu-id="22a39-144">若要了解如何從系統中移除舊版 Azure PowerShell，請參閱[將 Azure PowerShell 模組解除安裝](uninstall-az-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="22a39-144">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="22a39-145">使用多個版本的 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="22a39-145">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="22a39-146">您可以安裝多個版本的 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="22a39-146">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="22a39-147">若要檢查是否安裝了多個 Azure PowerShell 版本，請使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="22a39-147">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="22a39-148">若想移除 Azure PowerShell 版本，請參閱[解除安裝 Azure PowerShell 模組](uninstall-az-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="22a39-148">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="22a39-149">您可使用 `-RequiredVersion` 引數來安裝或載入特定版本的 `Az` 模組：</span><span class="sxs-lookup"><span data-stu-id="22a39-149">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="22a39-150">如果您安裝了多個模組版本，模組會自動載入，`Import-Module` 則預設會載入最新的版本。</span><span class="sxs-lookup"><span data-stu-id="22a39-150">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="22a39-151">提供意見反應</span><span class="sxs-lookup"><span data-stu-id="22a39-151">Provide feedback</span></span>

<span data-ttu-id="22a39-152">如果您發現 Azure Powershell 有錯誤，請[在 GitHub 上提出問題](https://github.com/Azure/azure-powershell/issues)。</span><span class="sxs-lookup"><span data-stu-id="22a39-152">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="22a39-153">若要從命令列提供意見反應，請使用 [Send-Feedback](/powershell/module/az.accounts/send-feedback) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="22a39-153">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="22a39-154">後續步驟</span><span class="sxs-lookup"><span data-stu-id="22a39-154">Next Steps</span></span>

<span data-ttu-id="22a39-155">若要深入了解 Azure PowerShell 模組和其功能，請參閱[開始使用 Azure PowerShell](get-started-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="22a39-155">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="22a39-156">如果您熟悉 Azure PowerShell 且需要從 AzureRM 遷移，請參閱[從 AzureRM 遷移至 Az](migrate-from-azurerm-to-az.md)。</span><span class="sxs-lookup"><span data-stu-id="22a39-156">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
