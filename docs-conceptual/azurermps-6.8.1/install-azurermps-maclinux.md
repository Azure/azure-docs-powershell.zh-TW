---
title: 在 macOS 或 Linux 上安裝 Azure PowerShell
description: 如何在 macOS 或 Linux 上安裝 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 6e7d447ea9672c174e3f1d103bc56c11a7f37192
ms.sourcegitcommit: dca906e73e943aac207cee23b79915773419c673
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/30/2018
ms.locfileid: "43250479"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="19dc0-103">在 macOS 或 Linux 上安裝 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="19dc0-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="19dc0-104">針對非 Windows 平台，可以在 PowerShell Core v6 中執行 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="19dc0-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="19dc0-105">這版的 PowerShell 是針對支援 .NET Core 的任何平台使用所建置。</span><span class="sxs-lookup"><span data-stu-id="19dc0-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="19dc0-106">若要使用這些平台，可以使用 .NET Core 特別版本的 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="19dc0-106">To work with these platforms, there's a special .NET Core version of Azure PowerShell available.</span></span>

> [!NOTE]
> <span data-ttu-id="19dc0-107">PowerShell Core v6 與 Azure PowerShell for .NET Core 目前仍處於 Beta 階段。</span><span class="sxs-lookup"><span data-stu-id="19dc0-107">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="19dc0-108">這些產品只提供有限支援。</span><span class="sxs-lookup"><span data-stu-id="19dc0-108">Support for these products is limited.</span></span> <span data-ttu-id="19dc0-109">若有問題或發現錯誤，請在 GitHub 中提出。</span><span class="sxs-lookup"><span data-stu-id="19dc0-109">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="19dc0-110">關於 PowerShell Core v6 的問題</span><span class="sxs-lookup"><span data-stu-id="19dc0-110">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="19dc0-111">關於Azure PowerShell 的問題</span><span class="sxs-lookup"><span data-stu-id="19dc0-111">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a><span data-ttu-id="19dc0-112">安裝 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="19dc0-112">Install PowerShell Core</span></span>

<span data-ttu-id="19dc0-113">macOS 和大部分 Linux 發佈的 PowerShell Core 安裝指示皆不同。</span><span class="sxs-lookup"><span data-stu-id="19dc0-113">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="19dc0-114">您可以在下列文章中找到詳細的指示：</span><span class="sxs-lookup"><span data-stu-id="19dc0-114">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="19dc0-115">Install PowerShell Core on macOS</span><span class="sxs-lookup"><span data-stu-id="19dc0-115">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="19dc0-116">Install PowerShell Core on Linux</span><span class="sxs-lookup"><span data-stu-id="19dc0-116">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a><span data-ttu-id="19dc0-117">安裝 Azure PowerShell for .NET Core</span><span class="sxs-lookup"><span data-stu-id="19dc0-117">Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="19dc0-118">PowerShell Core 隨附於已安裝的 PowerShellGet 模組。</span><span class="sxs-lookup"><span data-stu-id="19dc0-118">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="19dc0-119">安裝 PowerShell 中的模組需要較高的權限，因此必須以超級使用者身分來啟動您的工作階段：</span><span class="sxs-lookup"><span data-stu-id="19dc0-119">Installation of modules in PowerShell requires elevated privileges, so you'll need to start your session as superuser:</span></span>

```bash
sudo pwsh
```

<span data-ttu-id="19dc0-120">若要安裝 Azure PowerShell，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="19dc0-120">To install Azure PowerShell, run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

> [!IMPORTANT]
> <span data-ttu-id="19dc0-121">其他文章中詳述的 `AzureRM` 模組並非針對 .NET Core 所建置，且無法搭配 PowerShell Core 使用。</span><span class="sxs-lookup"><span data-stu-id="19dc0-121">The `AzureRM` module detailed in other articles is not built for .NET Core and will not work with PowerShell Core.</span></span> <span data-ttu-id="19dc0-122">`AzureRM` 和 `AzureRM.NetCore` 都是使用相同的 Cmdlet 名稱，因此唯一的差異在於彙總套件模組的名稱，以及它們是針對哪個版本的 .NET 所建置。</span><span class="sxs-lookup"><span data-stu-id="19dc0-122">Both `AzureRM` and `AzureRM.NetCore` use the same cmdlet names, so the only difference is the name of the rollup module and which .NET version they are built against.</span></span>

<span data-ttu-id="19dc0-123">根據預設，PowerShell 資源庫未設為 PowerShellGet 的信任存放庫。</span><span class="sxs-lookup"><span data-stu-id="19dc0-123">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="19dc0-124">第一次使用 PSGallery 時，您會看到下列提示：</span><span class="sxs-lookup"><span data-stu-id="19dc0-124">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="19dc0-125">請回答 `Yes` 或 `Yes to All` 以繼續安裝。</span><span class="sxs-lookup"><span data-stu-id="19dc0-125">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="sign-in"></a><span data-ttu-id="19dc0-126">登入</span><span class="sxs-lookup"><span data-stu-id="19dc0-126">Sign in</span></span>

<span data-ttu-id="19dc0-127">若要開始使用 Azure PowerShell，您必須使用 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) Cmdlet 將 `AzureRM.Netcore` 載入您的 PowerShell 工作階段，然後使用您的 Azure 認證登入。</span><span class="sxs-lookup"><span data-stu-id="19dc0-127">To start working with Azure PowerShell, you need to load `AzureRM.Netcore` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="19dc0-128">匯入模組「不」需要較高的權限。</span><span class="sxs-lookup"><span data-stu-id="19dc0-128">Importing a module does __not__ require elevated privileges.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM.Netcore
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="19dc0-129">您必須針對每個啟動的新 PowerShell 工作階段重複這些步驟。</span><span class="sxs-lookup"><span data-stu-id="19dc0-129">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="19dc0-130">自動匯入 `AzureRM` 模組需要設定 PowerShell 設定檔，您可以在[關於設定檔](/powershell/module/microsoft.powershell.core/about/about_profiles)中加以了解。</span><span class="sxs-lookup"><span data-stu-id="19dc0-130">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="19dc0-131">在 macOS 和 Linux 上，您應該透過 `$Profile` 環境變數來使用設定檔。</span><span class="sxs-lookup"><span data-stu-id="19dc0-131">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="19dc0-132">若要了解如何在工作階段之間保存您的 Azure 登入，請參閱[在 PowerShell 工作階段之間保存使用者認證](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="19dc0-132">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="19dc0-133">可用的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="19dc0-133">Available cmdlets</span></span>

<span data-ttu-id="19dc0-134">適用於 .NET Core 的 Azure PowerShell 模組仍在開發中。</span><span class="sxs-lookup"><span data-stu-id="19dc0-134">The Azure PowerShell modules for .NET Core are still in development.</span></span> <span data-ttu-id="19dc0-135">這些模組未提供適用於 Windows 版模組的所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="19dc0-135">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="19dc0-136">AzureRM.Netcore 模組實作了下列功能：</span><span class="sxs-lookup"><span data-stu-id="19dc0-136">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="19dc0-137">帳戶管理</span><span class="sxs-lookup"><span data-stu-id="19dc0-137">Account management</span></span>
  * <span data-ttu-id="19dc0-138">透過 Microsoft Azure Active Directory，使用 Microsoft 帳戶、組織帳戶或服務主體登入</span><span class="sxs-lookup"><span data-stu-id="19dc0-138">Sign in with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  * <span data-ttu-id="19dc0-139">透過 Save-AzureRmContext 將認證儲存到磁碟上，及使用 Import-AzureRmContext 載入儲存的認證</span><span class="sxs-lookup"><span data-stu-id="19dc0-139">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="19dc0-140">環境</span><span class="sxs-lookup"><span data-stu-id="19dc0-140">Environment</span></span>
  * <span data-ttu-id="19dc0-141">取得其他現成可用的 Microsoft Azure 環境</span><span class="sxs-lookup"><span data-stu-id="19dc0-141">Get the different out-of-box Microsoft Azure environments</span></span>
  * <span data-ttu-id="19dc0-142">新增/設定/移除自訂環境 (例如 Azure Stack 或 Windows Azure 套件環境)</span><span class="sxs-lookup"><span data-stu-id="19dc0-142">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="19dc0-143">使用資源管理員與服務管理介面之 Azure 服務適用的管理平面 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="19dc0-143">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  * <span data-ttu-id="19dc0-144">虛擬機器</span><span class="sxs-lookup"><span data-stu-id="19dc0-144">Virtual Machine</span></span>
  * <span data-ttu-id="19dc0-145">App Service (網站)</span><span class="sxs-lookup"><span data-stu-id="19dc0-145">App Service (Websites)</span></span>
  * <span data-ttu-id="19dc0-146">SQL Database</span><span class="sxs-lookup"><span data-stu-id="19dc0-146">SQL Database</span></span>
  * <span data-ttu-id="19dc0-147">儲存體</span><span class="sxs-lookup"><span data-stu-id="19dc0-147">Storage</span></span>
  * <span data-ttu-id="19dc0-148">網路</span><span class="sxs-lookup"><span data-stu-id="19dc0-148">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="19dc0-149">後續步驟</span><span class="sxs-lookup"><span data-stu-id="19dc0-149">Next Steps</span></span>

<span data-ttu-id="19dc0-150">如需有關使用 Azure PowerShell 的詳細資訊，請參閱[開始使用 Azure PowerShell](get-started-azureps.md)文章。</span><span class="sxs-lookup"><span data-stu-id="19dc0-150">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
