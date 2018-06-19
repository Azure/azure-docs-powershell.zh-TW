---
title: 在 macOS 或 Linux 上安裝 Azure PowerShell
description: 如何在 macOS 或 Linux 上安裝 Azure PowerShell。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 17912c155255b6fdfd3cfb9242163b67d405dc03
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323249"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="2809a-103">在 macOS 或 Linux 上安裝 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="2809a-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="2809a-104">針對非 Windows 平台，可以在 PowerShell Core v6 的基礎上執行 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="2809a-104">For non-Windows platforms, it's possible to run Azure PowerShell on top of PowerShell Core v6.</span></span> <span data-ttu-id="2809a-105">這個產品並非是在 .NET Framework for Windows 上建置的標準 Azure PowerShell，而是針對 .NET Core 建置，可以在支援 .Net Core 執行階段的任何平台上執行。</span><span class="sxs-lookup"><span data-stu-id="2809a-105">Rather than the standard Azure PowerShell built on .NET Framework for Windows, this product is built for .NET Core and can run on any platform which supports the .Net Core runtime.</span></span>

> [!NOTE]
> <span data-ttu-id="2809a-106">PowerShell Core v6 與 Azure PowerShell for .NET Core 目前仍處於 Beta 階段。</span><span class="sxs-lookup"><span data-stu-id="2809a-106">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="2809a-107">這些產品只提供有限支援。</span><span class="sxs-lookup"><span data-stu-id="2809a-107">Support for these products is limited.</span></span> <span data-ttu-id="2809a-108">若有問題或發現錯誤，請在 GitHub 中提出。</span><span class="sxs-lookup"><span data-stu-id="2809a-108">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="2809a-109">關於 PowerShell Core v6 的問題</span><span class="sxs-lookup"><span data-stu-id="2809a-109">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="2809a-110">關於Azure PowerShell 的問題</span><span class="sxs-lookup"><span data-stu-id="2809a-110">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core-v6"></a><span data-ttu-id="2809a-111">安裝 PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="2809a-111">Install PowerShell Core v6</span></span>

<span data-ttu-id="2809a-112">Linux 或 macOS 上的 PowerShell Core v6 安裝作業會因為 Linux 發行版本和作業系統版本不同而有所差異。</span><span class="sxs-lookup"><span data-stu-id="2809a-112">Installing PowerShell Core v6 on Linux or macOS varies depending on the Linux distribution and OS version.</span></span>
<span data-ttu-id="2809a-113">您可以在下列文章中找到詳細的指示：</span><span class="sxs-lookup"><span data-stu-id="2809a-113">Detailed instructions can be found in the following articles:</span></span>

- [<span data-ttu-id="2809a-114">Install PowerShell Core on macOS</span><span class="sxs-lookup"><span data-stu-id="2809a-114">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
- [<span data-ttu-id="2809a-115">Install PowerShell Core on Linux</span><span class="sxs-lookup"><span data-stu-id="2809a-115">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a><span data-ttu-id="2809a-116">安裝 Azure PowerShell for .NET Core</span><span class="sxs-lookup"><span data-stu-id="2809a-116">Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="2809a-117">PowerShell Core v6 隨附於已安裝的 PowerShellGet 模組。</span><span class="sxs-lookup"><span data-stu-id="2809a-117">PowerShell Core v6 comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="2809a-118">這可讓您輕鬆地安裝任何已發佈到 PowerShell 資源庫的模組。</span><span class="sxs-lookup"><span data-stu-id="2809a-118">This makes it easy to install any module that is published to the PowerShell Gallery.</span></span> <span data-ttu-id="2809a-119">若要安裝 Azure PowerShell，請開啟新的 PowerShell 工作階段，並執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="2809a-119">To install Azure PowerShell, open a new PowerShell session and run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

## <a name="load-the-azurermnetcore-module"></a><span data-ttu-id="2809a-120">載入 AzureRM.Netcore 模組</span><span class="sxs-lookup"><span data-stu-id="2809a-120">Load the AzureRM.Netcore module</span></span>

<span data-ttu-id="2809a-121">安裝模組後，您需要將模組載入您的 PowerShell 工作階段。</span><span class="sxs-lookup"><span data-stu-id="2809a-121">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="2809a-122">使用 `Import-Module`Cmdlet 載入模組，如下所示︰</span><span class="sxs-lookup"><span data-stu-id="2809a-122">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

<span data-ttu-id="2809a-123">匯入完成後，您可以嘗試使用下列命令登入 Azure，來測試新安裝的模組：</span><span class="sxs-lookup"><span data-stu-id="2809a-123">After the import completes, you can test your newly installed and module by attempting to sign into Azure using the following command:</span></span>

```powershell
Connect-AzureRmAccount
```

<span data-ttu-id="2809a-124">上述命令應會提示您移至 `https://aka.ms/devicelogin`，並輸入您收到的驗證碼。</span><span class="sxs-lookup"><span data-stu-id="2809a-124">The above command should prompt you to go to `https://aka.ms/devicelogin` and enter the provided code.</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="2809a-125">可用的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2809a-125">Available cmdlets</span></span>

<span data-ttu-id="2809a-126">Azure PowerShell modules for .NET Standard 模組仍在開發中。</span><span class="sxs-lookup"><span data-stu-id="2809a-126">The Azure PowerShell modules for .NET Standard are still in development.</span></span> <span data-ttu-id="2809a-127">這些模組未提供適用於 Windows 版模組的所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2809a-127">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="2809a-128">AzureRM.Netcore 模組實作了下列功能：</span><span class="sxs-lookup"><span data-stu-id="2809a-128">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="2809a-129">帳戶管理</span><span class="sxs-lookup"><span data-stu-id="2809a-129">Account management</span></span>
  - <span data-ttu-id="2809a-130">透過 Microsoft Azure Active Directory，以 Microsoft 帳戶、組織帳戶或服務主體登入</span><span class="sxs-lookup"><span data-stu-id="2809a-130">Login with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  - <span data-ttu-id="2809a-131">透過 Save-AzureRmContext 將認證儲存到磁碟上，及使用 Import-AzureRmContext 載入儲存的認證</span><span class="sxs-lookup"><span data-stu-id="2809a-131">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="2809a-132">環境</span><span class="sxs-lookup"><span data-stu-id="2809a-132">Environment</span></span>
  - <span data-ttu-id="2809a-133">取得其他現成可用的 Microsoft Azure 環境</span><span class="sxs-lookup"><span data-stu-id="2809a-133">Get the different out-of-box Microsoft Azure environments</span></span>
  - <span data-ttu-id="2809a-134">新增/設定/移除自訂環境 (例如 Azure Stack 或 Microsoft Azure 套件環境)</span><span class="sxs-lookup"><span data-stu-id="2809a-134">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="2809a-135">使用資源管理員與服務管理介面之 Azure 服務適用的管理平面 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2809a-135">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  - <span data-ttu-id="2809a-136">虛擬機器</span><span class="sxs-lookup"><span data-stu-id="2809a-136">Virtual Machine</span></span>
  - <span data-ttu-id="2809a-137">App Service (網站)</span><span class="sxs-lookup"><span data-stu-id="2809a-137">App Service (Websites)</span></span>
  - <span data-ttu-id="2809a-138">SQL Database</span><span class="sxs-lookup"><span data-stu-id="2809a-138">SQL Database</span></span>
  - <span data-ttu-id="2809a-139">儲存體</span><span class="sxs-lookup"><span data-stu-id="2809a-139">Storage</span></span>
  - <span data-ttu-id="2809a-140">網路</span><span class="sxs-lookup"><span data-stu-id="2809a-140">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="2809a-141">後續步驟</span><span class="sxs-lookup"><span data-stu-id="2809a-141">Next Steps</span></span>

<span data-ttu-id="2809a-142">如需有關使用 Azure PowerShell 的詳細資訊，請參閱[開始使用 Azure PowerShell](get-started-azureps.md)文章。</span><span class="sxs-lookup"><span data-stu-id="2809a-142">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
