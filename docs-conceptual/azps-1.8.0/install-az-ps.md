---
title: 使用 PowerShellGet 安裝 Azure PowerShell
description: 如何使用 PowerShellGet 安裝 Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 269119333b2197a15ed7bb50e3e5d90588456174
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2019
ms.locfileid: "63068875"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="6fc03-103">安裝 Azure PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="6fc03-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="6fc03-104">本文說明如何使用 PowerShellGet 安裝 Azure PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="6fc03-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="6fc03-105">這些指示適用於 Windows、macOS 和 Linux 平台。</span><span class="sxs-lookup"><span data-stu-id="6fc03-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="6fc03-106">至於 Az 模組，目前不支援其他安裝方法。</span><span class="sxs-lookup"><span data-stu-id="6fc03-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fc03-107">需求</span><span class="sxs-lookup"><span data-stu-id="6fc03-107">Requirements</span></span>

<span data-ttu-id="6fc03-108">Azure PowerShell 可在 Windows 上搭配 PowerShell 5.1 或更新版本，或在任何平台上搭配 PowerShell 6 運作。</span><span class="sxs-lookup"><span data-stu-id="6fc03-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell 6 on any platform.</span></span>
<span data-ttu-id="6fc03-109">若要檢查 PowerShell 版本，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="6fc03-109">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="6fc03-110">如果您有過時的版本或需要安裝 PowerShell，請參閱[安裝各種版本的 PowerShell](/powershell/scripting/setup/installing-powershell)。</span><span class="sxs-lookup"><span data-stu-id="6fc03-110">If you have an outdated version or need to install PowerShell, see [Installing various versions of PowerShell](/powershell/scripting/setup/installing-powershell).</span></span> <span data-ttu-id="6fc03-111">適用於您平台的安裝資訊是連結自該頁面。</span><span class="sxs-lookup"><span data-stu-id="6fc03-111">Install information for your platform is linked from that page.</span></span>

<span data-ttu-id="6fc03-112">如果您在 Windows 上使用 PowerShell 5，則還需要安裝 .NET Framework 4.7.2。</span><span class="sxs-lookup"><span data-stu-id="6fc03-112">If you are using PowerShell 5 on Windows, you also need .NET Framework 4.7.2 installed.</span></span> <span data-ttu-id="6fc03-113">如需更新或安裝新版 .NET Framework 的指示，請參閱 [.NET Framework 安裝指南](/dotnet/framework/install)。</span><span class="sxs-lookup"><span data-stu-id="6fc03-113">For instructions on updating or installing a new version of .NET Framework, see the [.NET Framework installation guide](/dotnet/framework/install).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="6fc03-114">安裝 Azure PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="6fc03-114">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="6fc03-115">您可以同時安裝 AzureRM 和 Az 模組。</span><span class="sxs-lookup"><span data-stu-id="6fc03-115">You can have both the AzureRM and Az modules installed at the same time.</span></span> <span data-ttu-id="6fc03-116">若您已安裝了兩個模組，__請勿啟用別名__。</span><span class="sxs-lookup"><span data-stu-id="6fc03-116">If you have both modules installed, __don't enable aliases__.</span></span>
> <span data-ttu-id="6fc03-117">啟用別名會讓 AzureRM Cmdlet 和 Az 命令別名產生衝突，且可能導致未預期的行為。</span><span class="sxs-lookup"><span data-stu-id="6fc03-117">Enabling aliases will cause conflicts between AzureRM cmdlets and Az command aliases, and could cause unexpected behavior.</span></span>
> <span data-ttu-id="6fc03-118">建議您在安裝 Az 模組之前，先將 AzureRM 解除安裝。</span><span class="sxs-lookup"><span data-stu-id="6fc03-118">It's recommended that before installing the Az module, you uninstall AzureRM.</span></span> <span data-ttu-id="6fc03-119">您可以隨時將 AzureRM 解除安裝，或啟用別名。</span><span class="sxs-lookup"><span data-stu-id="6fc03-119">You can always uninstall AzureRM or enable aliases at any time.</span></span> <span data-ttu-id="6fc03-120">若要了解 AzureRM 命令別名，請參閱[從 AzureRM 遷移至 Az](migrate-from-azurerm-to-az.md)。</span><span class="sxs-lookup"><span data-stu-id="6fc03-120">To learn about the AzureRM command aliases, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
> <span data-ttu-id="6fc03-121">如需解除安裝作的指示，請參閱[將 AzureRM 模組解除安裝](uninstall-az-ps.md#uninstall-the-azurerm-module)。</span><span class="sxs-lookup"><span data-stu-id="6fc03-121">For uninstall instructions, see [Uninstall the AzureRM module](uninstall-az-ps.md#uninstall-the-azurerm-module).</span></span> 

<span data-ttu-id="6fc03-122">若要在全域範圍安裝模組，您需要較高的權限，以從 PowerShell 資源庫安裝模組。</span><span class="sxs-lookup"><span data-stu-id="6fc03-122">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="6fc03-123">若要安裝 Azure PowerShell，請在提升權限的工作階段中執行下列命令 (在 Windows 上「以系統管理員身分執行」，或在 macOS 或 Linux 上使用超級使用者權限執行)：</span><span class="sxs-lookup"><span data-stu-id="6fc03-123">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="6fc03-124">如果您沒有系統管理員權限，藉由新增 `-Scope` 引數，即可為目前使用者進行安裝。</span><span class="sxs-lookup"><span data-stu-id="6fc03-124">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="6fc03-125">根據預設，PowerShell 資源庫未設為 PowerShellGet 的信任存放庫。</span><span class="sxs-lookup"><span data-stu-id="6fc03-125">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="6fc03-126">第一次使用 PSGallery 時，您會看到下列提示：</span><span class="sxs-lookup"><span data-stu-id="6fc03-126">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="6fc03-127">請回答 `Yes` 或 `Yes to All` 以繼續安裝。</span><span class="sxs-lookup"><span data-stu-id="6fc03-127">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="6fc03-128">Az 模組是 Azure PowerShell Cmdlet 的彙總套件模組。</span><span class="sxs-lookup"><span data-stu-id="6fc03-128">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="6fc03-129">安裝此項目會下載所有可用的 Azure Resource Manager 模組，並使這些模組的 Cmdlet 可供使用。</span><span class="sxs-lookup"><span data-stu-id="6fc03-129">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="6fc03-130">登入</span><span class="sxs-lookup"><span data-stu-id="6fc03-130">Sign in</span></span>

<span data-ttu-id="6fc03-131">若要開始使用 Azure PowerShell，請使用您的 Azure 認證登入。</span><span class="sxs-lookup"><span data-stu-id="6fc03-131">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="6fc03-132">如果您已停用自動載入模組功能，則必須透過 `Import-Module Az` 來手動匯入模組。</span><span class="sxs-lookup"><span data-stu-id="6fc03-132">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="6fc03-133">因為模組的結構化方式，這可能需要幾秒鐘的時間。</span><span class="sxs-lookup"><span data-stu-id="6fc03-133">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="6fc03-134">您必須針對每個啟動的新 PowerShell 工作階段重複這些步驟。</span><span class="sxs-lookup"><span data-stu-id="6fc03-134">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="6fc03-135">若要了解如何在 PowerShell 工作階段之間保存您的 Azure 登入，請參閱[在 PowerShell 工作階段之間保存使用者認證](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="6fc03-135">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="6fc03-136">更新 Azure PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="6fc03-136">Update the Azure PowerShell module</span></span>

<span data-ttu-id="6fc03-137">您可以執行 [Update-Module](/powershell/module/powershellget/update-module) 來更新您的 Azure PowerShell 安裝。</span><span class="sxs-lookup"><span data-stu-id="6fc03-137">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="6fc03-138">這個命令「不會」將舊版解除安裝。</span><span class="sxs-lookup"><span data-stu-id="6fc03-138">This command does __not__ uninstall older versions.</span></span>

```powershell-interactive
Update-Module -Name Az
```

<span data-ttu-id="6fc03-139">若要了解如何從系統中移除舊版 Azure PowerShell，請參閱[將 Azure PowerShell 模組解除安裝](uninstall-az-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="6fc03-139">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="6fc03-140">使用多個版本的 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6fc03-140">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="6fc03-141">您可以安裝多個版本的 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="6fc03-141">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="6fc03-142">若要檢查是否安裝了多個 Azure PowerShell 版本，請使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="6fc03-142">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="6fc03-143">若想移除 Azure PowerShell 版本，請參閱[解除安裝 Azure PowerShell 模組](uninstall-az-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="6fc03-143">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="6fc03-144">您可使用 `-RequiredVersion` 引數來安裝或載入特定版本的 `Az` 模組：</span><span class="sxs-lookup"><span data-stu-id="6fc03-144">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="6fc03-145">如果您安裝了多個模組版本，模組會自動載入，`Import-Module` 則預設會載入最新的版本。</span><span class="sxs-lookup"><span data-stu-id="6fc03-145">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="6fc03-146">提供意見反應</span><span class="sxs-lookup"><span data-stu-id="6fc03-146">Provide feedback</span></span>

<span data-ttu-id="6fc03-147">如果您發現 Azure Powershell 有錯誤，請[在 GitHub 上提出問題](https://github.com/Azure/azure-powershell/issues)。</span><span class="sxs-lookup"><span data-stu-id="6fc03-147">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="6fc03-148">若要從命令列提供意見反應，請使用 [Send-Feedback](/powershell/module/az.accounts/send-feedback) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6fc03-148">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="6fc03-149">後續步驟</span><span class="sxs-lookup"><span data-stu-id="6fc03-149">Next Steps</span></span>

<span data-ttu-id="6fc03-150">若要深入了解 Azure PowerShell 模組和其功能，請參閱[開始使用 Azure PowerShell](get-started-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="6fc03-150">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="6fc03-151">如果您熟悉 Azure PowerShell 且需要從 AzureRM 遷移，請參閱[從 AzureRM 遷移至 Az](migrate-from-azurerm-to-az.md)。</span><span class="sxs-lookup"><span data-stu-id="6fc03-151">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
