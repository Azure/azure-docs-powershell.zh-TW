---
title: 在 macOS 或 Linux 上安裝 Azure PowerShell
description: 如何在 macOS 或 Linux 上安裝 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: f014d62e898da195a38052db6b7e37a2cd96dfdd
ms.sourcegitcommit: 3a02e0c85c83de873981dd392500bc82c1cf9286
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/24/2018
ms.locfileid: "46560111"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="db085-103">在 macOS 或 Linux 上安裝 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="db085-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="db085-104">針對非 Windows 平台，可以在 PowerShell Core v6 中執行 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="db085-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="db085-105">這版的 PowerShell 是針對支援 .NET Core 的任何平台使用所建置。</span><span class="sxs-lookup"><span data-stu-id="db085-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="db085-106">若要使用這些平台，可以使用 .NET Standard 版本的 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="db085-106">To work with these platforms, there's a .NET Standard version of Azure PowerShell available.</span></span>

> [!NOTE]
> <span data-ttu-id="db085-107">PowerShell Core v6 與 Azure PowerShell for .NET Core 目前仍處於 Beta 階段。</span><span class="sxs-lookup"><span data-stu-id="db085-107">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="db085-108">這些產品只提供有限支援。</span><span class="sxs-lookup"><span data-stu-id="db085-108">Support for these products is limited.</span></span> <span data-ttu-id="db085-109">若有問題或發現錯誤，請在 GitHub 中提出。</span><span class="sxs-lookup"><span data-stu-id="db085-109">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="db085-110">關於 PowerShell Core v6 的問題</span><span class="sxs-lookup"><span data-stu-id="db085-110">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="db085-111">關於Azure PowerShell 的問題</span><span class="sxs-lookup"><span data-stu-id="db085-111">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a><span data-ttu-id="db085-112">安裝 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="db085-112">Install PowerShell Core</span></span>

<span data-ttu-id="db085-113">macOS 和大部分 Linux 發佈的 PowerShell Core 安裝指示皆不同。</span><span class="sxs-lookup"><span data-stu-id="db085-113">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="db085-114">您可以在下列文章中找到詳細的指示：</span><span class="sxs-lookup"><span data-stu-id="db085-114">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="db085-115">Install PowerShell Core on macOS</span><span class="sxs-lookup"><span data-stu-id="db085-115">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="db085-116">Install PowerShell Core on Linux</span><span class="sxs-lookup"><span data-stu-id="db085-116">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a><span data-ttu-id="db085-117">安裝 Azure PowerShell for .NET Core</span><span class="sxs-lookup"><span data-stu-id="db085-117">Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="db085-118">PowerShell Core 隨附於已安裝的 PowerShellGet 模組。</span><span class="sxs-lookup"><span data-stu-id="db085-118">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="db085-119">安裝 PowerShell 中的模組需要較高的權限，因此必須以超級使用者身分來啟動您的工作階段：</span><span class="sxs-lookup"><span data-stu-id="db085-119">Installation of modules in PowerShell requires elevated privileges, so you'll need to start your session as superuser:</span></span>

```bash
sudo pwsh
```

<span data-ttu-id="db085-120">若要安裝 Azure PowerShell，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="db085-120">To install Azure PowerShell, run the following command:</span></span>

```powershell
Install-Module Az
```

> [!IMPORTANT]
> <span data-ttu-id="db085-121">其他文章中詳述的 `AzureRM` 模組並非針對 .NET Core 所建置，且無法搭配 PowerShell Core 使用。</span><span class="sxs-lookup"><span data-stu-id="db085-121">The `AzureRM` module detailed in other articles is not built for .NET Core and will not work with PowerShell Core.</span></span> <span data-ttu-id="db085-122">`Az` 模組包含所有 `AzureRM` Cmdlet 的命令別名，因此適用於所有的 `AzureRM` 文件。</span><span class="sxs-lookup"><span data-stu-id="db085-122">The `Az` modules contain command aliases for all `AzureRM` cmdlets, so all of the documentation for `AzureRM` applies.</span></span>

<span data-ttu-id="db085-123">根據預設，PowerShell 資源庫未設為 PowerShellGet 的信任存放庫。</span><span class="sxs-lookup"><span data-stu-id="db085-123">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="db085-124">第一次使用 PSGallery 時，您會看到下列提示：</span><span class="sxs-lookup"><span data-stu-id="db085-124">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="db085-125">請回答 `Yes` 或 `Yes to All` 以繼續安裝。</span><span class="sxs-lookup"><span data-stu-id="db085-125">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="sign-in"></a><span data-ttu-id="db085-126">登入</span><span class="sxs-lookup"><span data-stu-id="db085-126">Sign in</span></span>

<span data-ttu-id="db085-127">若要開始使用 Azure PowerShell，您必須使用 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) Cmdlet 將 `Az` 載入您的 PowerShell 工作階段，然後使用您的 Azure 認證登入。</span><span class="sxs-lookup"><span data-stu-id="db085-127">To start working with Azure PowerShell, you need to load `Az` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="db085-128">匯入模組「不」需要較高的權限。</span><span class="sxs-lookup"><span data-stu-id="db085-128">Importing a module does __not__ require elevated privileges.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="db085-129">您必須針對每個啟動的新 PowerShell 工作階段重複這些步驟。</span><span class="sxs-lookup"><span data-stu-id="db085-129">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="db085-130">自動匯入 `Az` 模組需要設定 PowerShell 設定檔，您可以在[關於設定檔](/powershell/module/microsoft.powershell.core/about/about_profiles)中加以了解。</span><span class="sxs-lookup"><span data-stu-id="db085-130">Automatically importing the `Az` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="db085-131">在 macOS 和 Linux 上，您應該透過 `$Profile` 環境變數來使用設定檔。</span><span class="sxs-lookup"><span data-stu-id="db085-131">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="db085-132">若要了解如何在工作階段之間保存您的 Azure 登入，請參閱[在 PowerShell 工作階段之間保存使用者認證](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="db085-132">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="db085-133">後續步驟</span><span class="sxs-lookup"><span data-stu-id="db085-133">Next Steps</span></span>

<span data-ttu-id="db085-134">如需有關使用 Azure PowerShell 的詳細資訊，請參閱[開始使用 Azure PowerShell](get-started-azureps.md)文章。</span><span class="sxs-lookup"><span data-stu-id="db085-134">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
