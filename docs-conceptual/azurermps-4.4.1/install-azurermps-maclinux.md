---
title: 在 macOS 與 Linux 上安裝和設定 Azure PowerShell | Microsoft Docs
description: 如何在 macOS 與 Linux 上安裝 Azure PowerShell，以及針對初次使用來進行設定。
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/12/2018
ms.openlocfilehash: 9e4c727c9adc378b9f1a65d3cb3dda7af05c33f5
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/23/2018
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a><span data-ttu-id="d8916-103">在 macOS 與 Linux 上安裝和設定 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d8916-103">Install and configure Azure PowerShell on macOS and Linux</span></span>

<span data-ttu-id="d8916-104">現在可以將 PowerShell Core v6 與 Azure PowerShell 安裝在非 Windows 平台上。</span><span class="sxs-lookup"><span data-stu-id="d8916-104">It is now possible to install PowerShell Core v6 and Azure PowerShell on non-Windows platforms.</span></span>
<span data-ttu-id="d8916-105">將 Azure PowerShell 安裝在 macOS 與 Linux 的程序與安裝在 Windows 上沒有不同，但您必須先安裝 PowerShell Core v6。</span><span class="sxs-lookup"><span data-stu-id="d8916-105">The process of installing Azure PowerShell on macOS and Linux is not that different from Windows, however, you must first install PowerShell Core v6.</span></span>

> [!NOTE]

> <span data-ttu-id="d8916-106">PowerShell Core v6 與 Azure PowerShell for .NET Core 目前仍處於 Beta 階段。</span><span class="sxs-lookup"><span data-stu-id="d8916-106">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="d8916-107">這些產品只提供有限支援。</span><span class="sxs-lookup"><span data-stu-id="d8916-107">Support for these products is limited.</span></span> <span data-ttu-id="d8916-108">若有問題或發現錯誤，請在 GitHub 中提出。</span><span class="sxs-lookup"><span data-stu-id="d8916-108">If you have problems or discover bugs, please file Issues in GitHub.</span></span>
>
> * [<span data-ttu-id="d8916-109">關於 PowerShell Core v6 的問題</span><span class="sxs-lookup"><span data-stu-id="d8916-109">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="d8916-110">關於Azure PowerShell 的問題</span><span class="sxs-lookup"><span data-stu-id="d8916-110">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-core-v6"></a><span data-ttu-id="d8916-111">步驟 1：安裝 PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="d8916-111">Step 1: Install PowerShell Core v6</span></span>

<span data-ttu-id="d8916-112">PowerShell Core v6 安裝程序因目標作業系統而異。</span><span class="sxs-lookup"><span data-stu-id="d8916-112">The process of installing PowerShell Core v6 on varies depending on the target operating system.</span></span>
<span data-ttu-id="d8916-113">雖然 PowerShell Core v6 可以安裝在 Windows 上，但本文只說明在 macOS 與 Linux 上安裝的步驟。</span><span class="sxs-lookup"><span data-stu-id="d8916-113">While it is possible to install PowerShell Core v6 on Windows, this article focuses on macOS and Linux.</span></span> <span data-ttu-id="d8916-114">如果您想要在 Windows 中使用 Azure PowerShell，請參閱 Windows 適用的[安裝](./install-azurerm-ps.md)文章。</span><span class="sxs-lookup"><span data-stu-id="d8916-114">If you want to use Azure PowerShell on Windows, see the [install](./install-azurerm-ps.md) article for Windows.</span></span>

<span data-ttu-id="d8916-115">Linux 或 macOS 上的 **PowerShell Core v6** 安裝作業會因為 Linux 發行版本和作業系統版本不同而有所差異。</span><span class="sxs-lookup"><span data-stu-id="d8916-115">Installing **PowerShell Core v6** on Linux or macOS varies depending on the Linux distribution and OS version.</span></span>
<span data-ttu-id="d8916-116">您可以在下列文章中找到詳細的指示：</span><span class="sxs-lookup"><span data-stu-id="d8916-116">Detailed instructions can be found in the following article:</span></span>

- [<span data-ttu-id="d8916-117">在 macOS 和 Linux 上安裝 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="d8916-117">Installing PowerShell Core on macOS and Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos-and-linux)

## <a name="step-2-install-azure-powershell-for-net-core"></a><span data-ttu-id="d8916-118">步驟 2：安裝 Azure PowerShell for .NET Core</span><span class="sxs-lookup"><span data-stu-id="d8916-118">Step 2: Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="d8916-119">PowerShell Core v6 隨附於已安裝的 PowerShellGet 模組。</span><span class="sxs-lookup"><span data-stu-id="d8916-119">PowerShell Core v6 comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="d8916-120">這可讓您輕鬆地安裝任何已發佈到 PowerShell 資源庫的模組。</span><span class="sxs-lookup"><span data-stu-id="d8916-120">This makes it easy to install any module that is published to the PowerShell Gallery.</span></span> <span data-ttu-id="d8916-121">若要安裝 Azure PowerShell，請開啟新的 PowerShell 工作階段，並執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="d8916-121">To install Azure PowerShell, open a new PowerShell session and run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a><span data-ttu-id="d8916-122">步驟 3：載入 AzureRM.Netcore 模組</span><span class="sxs-lookup"><span data-stu-id="d8916-122">Step 3: Load the AzureRM.Netcore module</span></span>

<span data-ttu-id="d8916-123">安裝模組後，您需要將模組載入您的 PowerShell 工作階段。</span><span class="sxs-lookup"><span data-stu-id="d8916-123">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="d8916-124">使用 `Import-Module`Cmdlet 載入模組，如下所示︰</span><span class="sxs-lookup"><span data-stu-id="d8916-124">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

<span data-ttu-id="d8916-125">匯入完成後，您可以嘗試使用下列命令登入 Azure，來測試新安裝的模組：</span><span class="sxs-lookup"><span data-stu-id="d8916-125">After the import completes, you can test your newly installed and module by attempting to sign into Azure using the following command:</span></span>

```powershell
Login-AzureRMAccount
```

<span data-ttu-id="d8916-126">上述命令應會提示您移至 `https://aka.ms/devicelogin`，並輸入您收到的驗證碼。</span><span class="sxs-lookup"><span data-stu-id="d8916-126">The above command should prompt you to go to `https://aka.ms/devicelogin` and enter the provided code.</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="d8916-127">可用的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d8916-127">Available cmdlets</span></span>

<span data-ttu-id="d8916-128">Azure PowerShell modules for .NET Standard 模組仍在開發中。</span><span class="sxs-lookup"><span data-stu-id="d8916-128">The Azure PowerShell modules for .NET Standard are still in development.</span></span> <span data-ttu-id="d8916-129">這些模組未提供適用於 Windows 版模組的所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d8916-129">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="d8916-130">AzureRM.Netcore 模組實作了下列功能：</span><span class="sxs-lookup"><span data-stu-id="d8916-130">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="d8916-131">帳戶管理</span><span class="sxs-lookup"><span data-stu-id="d8916-131">Account management</span></span>
  - <span data-ttu-id="d8916-132">透過 Microsoft Azure Active Directory，以 Microsoft 帳戶、組織帳戶或服務主體登入</span><span class="sxs-lookup"><span data-stu-id="d8916-132">Login with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  - <span data-ttu-id="d8916-133">透過 Save-AzureRmContext 將認證儲存到磁碟上，及使用 Import-AzureRmContext 載入儲存的認證</span><span class="sxs-lookup"><span data-stu-id="d8916-133">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="d8916-134">環境</span><span class="sxs-lookup"><span data-stu-id="d8916-134">Environment</span></span>
  - <span data-ttu-id="d8916-135">取得其他現成可用的 Microsoft Azure 環境</span><span class="sxs-lookup"><span data-stu-id="d8916-135">Get the different out-of-box Microsoft Azure environments</span></span>
  - <span data-ttu-id="d8916-136">新增/設定/移除自訂環境 (例如 Azure Stack 或 Windows Azure 套件環境)</span><span class="sxs-lookup"><span data-stu-id="d8916-136">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="d8916-137">使用資源管理員與服務管理介面之 Azure 服務適用的管理平面 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d8916-137">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  - <span data-ttu-id="d8916-138">虛擬機器</span><span class="sxs-lookup"><span data-stu-id="d8916-138">Virtual Machine</span></span>
  - <span data-ttu-id="d8916-139">App Service (網站)</span><span class="sxs-lookup"><span data-stu-id="d8916-139">App Service (Websites)</span></span>
  - <span data-ttu-id="d8916-140">SQL Database</span><span class="sxs-lookup"><span data-stu-id="d8916-140">SQL Database</span></span>
  - <span data-ttu-id="d8916-141">儲存體</span><span class="sxs-lookup"><span data-stu-id="d8916-141">Storage</span></span>
  - <span data-ttu-id="d8916-142">網路</span><span class="sxs-lookup"><span data-stu-id="d8916-142">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="d8916-143">後續步驟</span><span class="sxs-lookup"><span data-stu-id="d8916-143">Next Steps</span></span>

<span data-ttu-id="d8916-144">如需有關使用 Azure PowerShell 的詳細資訊，請參閱[開始使用 Azure PowerShell](get-started-azureps.md)文章。</span><span class="sxs-lookup"><span data-stu-id="d8916-144">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
