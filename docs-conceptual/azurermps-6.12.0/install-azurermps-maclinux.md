---
title: 在 macOS 或 Linux 上安裝 Azure PowerShell
description: 如何在 macOS 或 Linux 上安裝 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/05/2018
ms.openlocfilehash: f60ea1c608be4b1c8319d53303713ba039276abc
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/07/2018
ms.locfileid: "51212623"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="bfeda-103">在 macOS 或 Linux 上安裝 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="bfeda-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="bfeda-104">針對非 Windows 平台，可以在 PowerShell Core v6 中執行 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="bfeda-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="bfeda-105">這版的 PowerShell 是針對支援 .NET Core 的任何平台使用所建置。</span><span class="sxs-lookup"><span data-stu-id="bfeda-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="bfeda-106">若要使用這些平台，可以使用 .NET Standard 版本的 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="bfeda-106">To work with these platforms, there's a .NET Standard version of Azure PowerShell available.</span></span>

> [!NOTE]
> <span data-ttu-id="bfeda-107">目前，適用於 .NET Standard 的 Azure PowerShell 仍是搶鮮版 (Beta)。</span><span class="sxs-lookup"><span data-stu-id="bfeda-107">At this time, Azure PowerShell for .NET Standard is still in beta.</span></span>
> <span data-ttu-id="bfeda-108">若有問題或發現錯誤，請在 GitHub 中提出。</span><span class="sxs-lookup"><span data-stu-id="bfeda-108">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="bfeda-109">關於Azure PowerShell 的問題</span><span class="sxs-lookup"><span data-stu-id="bfeda-109">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a><span data-ttu-id="bfeda-110">安裝 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="bfeda-110">Install PowerShell Core</span></span>

<span data-ttu-id="bfeda-111">macOS 和大部分 Linux 發佈的 PowerShell Core 安裝指示皆不同。</span><span class="sxs-lookup"><span data-stu-id="bfeda-111">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="bfeda-112">您可以在下列文章中找到詳細的指示：</span><span class="sxs-lookup"><span data-stu-id="bfeda-112">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="bfeda-113">Install PowerShell Core on macOS</span><span class="sxs-lookup"><span data-stu-id="bfeda-113">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="bfeda-114">Install PowerShell Core on Linux</span><span class="sxs-lookup"><span data-stu-id="bfeda-114">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-standard"></a><span data-ttu-id="bfeda-115">安裝 Azure PowerShell for .NET Standard</span><span class="sxs-lookup"><span data-stu-id="bfeda-115">Install Azure PowerShell for .NET Standard</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bfeda-116">其他文章中詳述的 `AzureRM` 模組無法搭配 PowerShell Core 使用。</span><span class="sxs-lookup"><span data-stu-id="bfeda-116">The `AzureRM` module detailed in other articles does not work with PowerShell Core.</span></span>
> <span data-ttu-id="bfeda-117">您必須安裝 `Az` 模組，才能讓 Azure PowerShell 在 PowerShell Core 中發揮功能。</span><span class="sxs-lookup"><span data-stu-id="bfeda-117">You must install the `Az` module to get Azure PowerShell functionality in PowerShell Core.</span></span>

<span data-ttu-id="bfeda-118">PowerShell Core 隨附於已安裝的 PowerShellGet 模組。</span><span class="sxs-lookup"><span data-stu-id="bfeda-118">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="bfeda-119">以命令啟動 PowerShell：</span><span class="sxs-lookup"><span data-stu-id="bfeda-119">Start PowerShell with the command:</span></span>

```bash
pwsh
```

<span data-ttu-id="bfeda-120">若要安裝 Azure PowerShell，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="bfeda-120">To install Azure PowerShell, run the following command:</span></span>

```powershell-interactive
Install-Module Az
```

> [!NOTE]
> <span data-ttu-id="bfeda-121">如果您在嘗試安裝模組時遇到權限錯誤，可能需要以超級使用者模式執行 PowerShell，才能安裝模組。</span><span class="sxs-lookup"><span data-stu-id="bfeda-121">If you encounter a permissions error when attempting to install the module, you may need to run PowerShell in superuser mode to install modules.</span></span>
>
> ```bash
> sudo pwsh
> ```

<span data-ttu-id="bfeda-122">根據預設，PowerShell 資源庫未設為 PowerShellGet 的信任存放庫。</span><span class="sxs-lookup"><span data-stu-id="bfeda-122">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="bfeda-123">第一次使用 PSGallery 時，您會看到下列提示：</span><span class="sxs-lookup"><span data-stu-id="bfeda-123">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="bfeda-124">請回答 `Yes` 或 `Yes to All` 以繼續安裝。</span><span class="sxs-lookup"><span data-stu-id="bfeda-124">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="enable-aliases"></a><span data-ttu-id="bfeda-125">啟用別名</span><span class="sxs-lookup"><span data-stu-id="bfeda-125">Enable aliases</span></span>

<span data-ttu-id="bfeda-126">為了與現有 `AzureRM` 模組相容，新的 `Az` 模組可建立具備回溯相容性的別名來使用 `AzureRM` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bfeda-126">For compatibility with the existing `AzureRM` module, the new `Az` module has the ability to create backwards compatible aliases for the `AzureRM` cmdlets.</span></span> <span data-ttu-id="bfeda-127">第一次使用模組之前，請使用下列命令設定這些別名：</span><span class="sxs-lookup"><span data-stu-id="bfeda-127">Before using the module for the first time, set up these aliases with the following command:</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Enable AzureRM aliases for the user
Enable-AzureRmAlias -Scope CurrentUser
```

<span data-ttu-id="bfeda-128">這只會設定為目前使用者的別名。</span><span class="sxs-lookup"><span data-stu-id="bfeda-128">This sets up aliases for the current user only.</span></span> <span data-ttu-id="bfeda-129">請針對其他可供 `-Scope` 使用以設定別名的值，查看 Cmdlet 的協助。</span><span class="sxs-lookup"><span data-stu-id="bfeda-129">Check the cmdlet help for other values that can be provided to `-Scope` to set up the aliases.</span></span>

> [!NOTE]
> <span data-ttu-id="bfeda-130">如果您遇到與路徑位置有關的錯誤，請確定該路徑位置存在於您的本機系統中。</span><span class="sxs-lookup"><span data-stu-id="bfeda-130">If you encounter an error about a path location, make sure that it exists on your local system.</span></span> <span data-ttu-id="bfeda-131">針對 `CurrentUser` 範圍，可以藉由在 `bash` 中執行下列命令來解決此錯誤：</span><span class="sxs-lookup"><span data-stu-id="bfeda-131">For the `CurrentUser` scope, this error can be resolved by running the following command in `bash`:</span></span>
>
> ```bash
> mkdir -p $HOME/.config/powershell
> ```

## <a name="sign-in"></a><span data-ttu-id="bfeda-132">登入</span><span class="sxs-lookup"><span data-stu-id="bfeda-132">Sign in</span></span>

<span data-ttu-id="bfeda-133">若要開始使用 Azure PowerShell，您必須使用 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) Cmdlet 將 `Az` 載入您的 PowerShell 工作階段，然後使用您的 Azure 認證登入。</span><span class="sxs-lookup"><span data-stu-id="bfeda-133">To start working with Azure PowerShell, you need to load `Az` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="bfeda-134">匯入模組「不」需要較高的權限。</span><span class="sxs-lookup"><span data-stu-id="bfeda-134">Importing a module does __not__ require elevated privileges.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="bfeda-135">您必須針對每個啟動的新 PowerShell 工作階段重複這些步驟。</span><span class="sxs-lookup"><span data-stu-id="bfeda-135">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="bfeda-136">自動匯入 `Az` 模組需要設定 PowerShell 設定檔，您可以在[關於設定檔](/powershell/module/microsoft.powershell.core/about/about_profiles)中加以了解。</span><span class="sxs-lookup"><span data-stu-id="bfeda-136">Automatically importing the `Az` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="bfeda-137">在 macOS 和 Linux 上，您應該透過 `$Profile` 環境變數來使用設定檔。</span><span class="sxs-lookup"><span data-stu-id="bfeda-137">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="bfeda-138">若要了解如何在工作階段之間保存您的 Azure 登入，請參閱[在 PowerShell 工作階段之間保存使用者認證](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="bfeda-138">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="bfeda-139">後續步驟</span><span class="sxs-lookup"><span data-stu-id="bfeda-139">Next Steps</span></span>

<span data-ttu-id="bfeda-140">如需有關使用 Azure PowerShell 的詳細資訊，請參閱[開始使用 Azure PowerShell](get-started-azureps.md)文章。</span><span class="sxs-lookup"><span data-stu-id="bfeda-140">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
