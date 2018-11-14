---
title: 使用 PowerShellGet 安裝 Azure PowerShell
description: 如何使用 PowerShellGet 安裝 Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: c4af07816aaa6713d67e3349a45880f8cc22c80a
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/08/2018
ms.locfileid: "51276029"
---
# <a name="install-azure-powershell-with-powershellget"></a><span data-ttu-id="ecaab-103">使用 PowerShellGet 安裝 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ecaab-103">Install Azure PowerShell with PowerShellGet</span></span>

<span data-ttu-id="ecaab-104">本文說明如何使用 PowerShellGet 安裝 Azure PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="ecaab-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="ecaab-105">在 Az 預覽版本中，不支援任何其他安裝方法。</span><span class="sxs-lookup"><span data-stu-id="ecaab-105">For the preview release of Az, no other install methods are supported.</span></span> 

## <a name="requirements"></a><span data-ttu-id="ecaab-106">需求</span><span class="sxs-lookup"><span data-stu-id="ecaab-106">Requirements</span></span>

<span data-ttu-id="ecaab-107">Azure PowerShell 可搭配 Windows 上的 PowerShell 5.x 或任何平台上的 PowerShell 6.x 運作。</span><span class="sxs-lookup"><span data-stu-id="ecaab-107">Azure PowerShell works with either PowerShell 5.x on Windows, or PowerShell 6.x on any platform.</span></span> <span data-ttu-id="ecaab-108">若要檢查您電腦上執行的 PowerShell 版本，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="ecaab-108">To check the version of PowerShell running on your machine, run the following command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="ecaab-109">如果您有過時的版本或需要安裝 PowerShell，請參閱[安裝各種版本的 PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6)。</span><span class="sxs-lookup"><span data-stu-id="ecaab-109">If you have an outdated version or need to install PowerShell, see [Installing various versions of PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6).</span></span> <span data-ttu-id="ecaab-110">適用於您平台的安裝資訊是連結自該頁面。</span><span class="sxs-lookup"><span data-stu-id="ecaab-110">Install information for your platform is linked from that page.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="ecaab-111">安裝 Azure PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="ecaab-111">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="ecaab-112">您不得同時在一個系統上安裝 `AzureRM` 和 `Az` 模組。</span><span class="sxs-lookup"><span data-stu-id="ecaab-112">You shouldn't have both the `AzureRM` and `Az` modules installed on a system at the same time.</span></span> <span data-ttu-id="ecaab-113">若要安裝 `Az` 模組，必須先將 `AzureRM` 解除安裝。</span><span class="sxs-lookup"><span data-stu-id="ecaab-113">In order to install the `Az` module, `AzureRM` must be uninstalled.</span></span> <span data-ttu-id="ecaab-114">如需執行該動作的指示，請參閱[將 Azure PowerShell 模組 (AzureRM) 解除安裝](uninstall-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="ecaab-114">For instructions on how to do that, see [Uninstall the Azure PowerShell module (AzureRM)](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="ecaab-115">若要在全域範圍安裝模組，您需要較高的權限，以從 PowerShell 資源庫安裝模組。</span><span class="sxs-lookup"><span data-stu-id="ecaab-115">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="ecaab-116">若要安裝 Azure PowerShell，請在提升權限的工作階段中執行下列命令 (在 Windows 上「以系統管理員身分執行」，或在 macOS 或 Linux 上使用超級使用者權限執行)：</span><span class="sxs-lookup"><span data-stu-id="ecaab-116">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="ecaab-117">如果您沒有系統管理員權限，藉由新增 `-Scope` 引數，即可為目前使用者進行安裝。</span><span class="sxs-lookup"><span data-stu-id="ecaab-117">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="ecaab-118">根據預設，PowerShell 資源庫未設為 PowerShellGet 的信任存放庫。</span><span class="sxs-lookup"><span data-stu-id="ecaab-118">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="ecaab-119">第一次使用 PSGallery 時，您會看到下列提示：</span><span class="sxs-lookup"><span data-stu-id="ecaab-119">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="ecaab-120">請回答 `Yes` 或 `Yes to All` 以繼續安裝。</span><span class="sxs-lookup"><span data-stu-id="ecaab-120">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="ecaab-121">`Az` 模組是 Azure PowerShell Cmdlet 的彙總套件模組。</span><span class="sxs-lookup"><span data-stu-id="ecaab-121">The `Az` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="ecaab-122">安裝此項目會下載所有可用的 Azure Resource Manager 模組，並使這些模組的 Cmdlet 可供使用。</span><span class="sxs-lookup"><span data-stu-id="ecaab-122">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="ecaab-123">登入</span><span class="sxs-lookup"><span data-stu-id="ecaab-123">Sign in</span></span>

<span data-ttu-id="ecaab-124">若要開始使用 Azure PowerShell，您必須使用 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) Cmdlet 將 `Az` 載入您目前的 PowerShell 工作階段，然後使用您的 Azure 認證登入。</span><span class="sxs-lookup"><span data-stu-id="ecaab-124">To start working with Azure PowerShell, you need to load `Az` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

<span data-ttu-id="ecaab-125">您必須針對每個啟動的新 PowerShell 工作階段重複這些步驟。</span><span class="sxs-lookup"><span data-stu-id="ecaab-125">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="ecaab-126">自動匯入 `Az` 模組需要設定 PowerShell 設定檔，您可以在[關於設定檔](/powershell/module/microsoft.powershell.core/about/about_profiles)中加以了解。</span><span class="sxs-lookup"><span data-stu-id="ecaab-126">Automatically importing the `Az` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="ecaab-127">若要了解如何在工作階段之間保存您的 Azure 登入，請參閱[在 PowerShell 工作階段之間保存使用者認證](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="ecaab-127">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="ecaab-128">更新 Azure PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="ecaab-128">Update the Azure PowerShell module</span></span>

<span data-ttu-id="ecaab-129">您可以執行 [Update-Module](/powershell/module/powershellget/update-module) 來更新您的 Azure PowerShell 安裝。</span><span class="sxs-lookup"><span data-stu-id="ecaab-129">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="ecaab-130">這個命令「不會」將舊版解除安裝。</span><span class="sxs-lookup"><span data-stu-id="ecaab-130">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name Az
```

<span data-ttu-id="ecaab-131">如果您想要從系統中移除較舊版本的 Azure PowerShell，請參閱[將 Azure PowerShell 模組解除安裝](uninstall-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="ecaab-131">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="ecaab-132">使用多個版本的 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ecaab-132">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="ecaab-133">您可以安裝多個版本的 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="ecaab-133">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="ecaab-134">若要檢查是否安裝了多個 Azure PowerShell 版本，請使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="ecaab-134">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-Module -Name Az -List | select Name,Version
```

<span data-ttu-id="ecaab-135">若想移除 Azure PowerShell 版本，請參閱[解除安裝 Azure PowerShell 模組](uninstall-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="ecaab-135">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="ecaab-136">您可使用 `-RequiredVersion` 引數搭配 `Install-Module` 或 `Import-Module`，以載入特定版本的 `Az` 模組：</span><span class="sxs-lookup"><span data-stu-id="ecaab-136">You can load a specific version of the `Az` module by using the `-RequiredVersion` argument with `Install-Module` or `Import-Module`:</span></span>

```powershell-interactive
Install-Module -Name Az -RequiredVersion 0.4.0
Import-Module -Name Az -RequiredVersion 0.4.0
```

<span data-ttu-id="ecaab-137">如果您已安裝多個版本的模組，則預設會在匯入時載入最新版本。</span><span class="sxs-lookup"><span data-stu-id="ecaab-137">If you have more than one version of the module installed, the latest version is loaded by default when importing.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="ecaab-138">提供意見反應</span><span class="sxs-lookup"><span data-stu-id="ecaab-138">Provide feedback</span></span>

<span data-ttu-id="ecaab-139">如果您在使用 Azure Powershell 時發現錯誤，請[在 GitHub 上提出問題](https://github.com/Azure/azure-powershell/issues)。</span><span class="sxs-lookup"><span data-stu-id="ecaab-139">If you find a bug when using Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="ecaab-140">若要從命令列提供意見反應，請使用 [Send-Feedback](/powershell/module/az.profile/send-feedback) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ecaab-140">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ecaab-141">後續步驟</span><span class="sxs-lookup"><span data-stu-id="ecaab-141">Next Steps</span></span>

<span data-ttu-id="ecaab-142">若要開始使用 Azure PowerShell，請參閱[開始使用 Azure PowerShell](get-started-azureps.md) 以深入了解模組及其功能。</span><span class="sxs-lookup"><span data-stu-id="ecaab-142">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>