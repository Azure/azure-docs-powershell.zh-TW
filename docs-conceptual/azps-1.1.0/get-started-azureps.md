---
title: 開始使用 Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 01/14/2019
ms.openlocfilehash: 483e74d7d047562b1c170c3767495161b9c5eb2f
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/16/2019
ms.locfileid: "54341884"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="dcac1-102">開始使用 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="dcac1-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="dcac1-103">Azure PowerShell 的設計訴求是從命令列管理 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="dcac1-103">Azure PowerShell is designed for managing and administering Azure resources from the command line.</span></span> <span data-ttu-id="dcac1-104">當您想要建置使用 Azure Resource Manager 模型的自動化工具時，就可以使用 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="dcac1-104">Use Azure PowerShell when you want to build automated tools that use the Azure Resource Manager model.</span></span>
<span data-ttu-id="dcac1-105">您可以在瀏覽器中嘗試將其與 [Azure Cloud Shell](/azure/cloud-shell/overview) 搭配使用，或是將其安裝在本機電腦上。</span><span class="sxs-lookup"><span data-stu-id="dcac1-105">Try it out in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or install on your local machine.</span></span>

<span data-ttu-id="dcac1-106">本文可協助您開始使用 Azure PowerShell，並讓您知道其背後的核心概念。</span><span class="sxs-lookup"><span data-stu-id="dcac1-106">This article helps you get started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-or-run-in-azure-cloud-shell"></a><span data-ttu-id="dcac1-107">在 Azure Cloud Shell 中安裝或執行</span><span class="sxs-lookup"><span data-stu-id="dcac1-107">Install or run in Azure Cloud Shell</span></span>

<span data-ttu-id="dcac1-108">開始使用 Azure PowerShell 最簡單的方式是在 Azure Cloud Shell 環境中試用。</span><span class="sxs-lookup"><span data-stu-id="dcac1-108">The easiest way to get started with Azure PowerShell is by trying it out in an Azure Cloud Shell environment.</span></span>
<span data-ttu-id="dcac1-109">若要啟動並執行 Cloud Shell，請參閱 [Azure Cloud Shell 中的 PowerShell 快速入門](/azure/cloud-shell/quickstart-powershell)。</span><span class="sxs-lookup"><span data-stu-id="dcac1-109">To get up and running with Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
<span data-ttu-id="dcac1-110">Cloud Shell 會在 Linux 容器上執行 PowerShell 6，因此無法使用 Windows 特有的功能。</span><span class="sxs-lookup"><span data-stu-id="dcac1-110">Cloud Shell runs PowerShell 6 on a Linux container, so Windows-specific functionality isn't available.</span></span>

<span data-ttu-id="dcac1-111">當您準備好在本機電腦上安裝 Azure PowerShell 時，請遵循[安裝 Azure PowerShell 模組](install-az-ps.md)中的指示。</span><span class="sxs-lookup"><span data-stu-id="dcac1-111">When you're ready to install Azure PowerShell on your local machine, follow the instructions in [Install the Azure PowerShell module](install-az-ps.md).</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="dcac1-112">登入 Azure</span><span class="sxs-lookup"><span data-stu-id="dcac1-112">Sign in to Azure</span></span>

<span data-ttu-id="dcac1-113">使用 `Connect-AzAccount` Cmdlet 以互動方式登入。</span><span class="sxs-lookup"><span data-stu-id="dcac1-113">Sign in interactively with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="dcac1-114">如果您使用 Cloud Shell，請略過此步驟：您的 Azure Cloud Shell 工作階段已向啟動 Cloud Shell 工作階段的環境、訂用帳戶及租用戶完成驗證。</span><span class="sxs-lookup"><span data-stu-id="dcac1-114">Skip this step if you use Cloud Shell: Your Auzre Cloud Shell session is already authenticated for the environment, subscription, and tenant that launched the Cloud Shell session.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="dcac1-115">如果您不是位於美國區域，請使用 `-Environment` 參數來登入。</span><span class="sxs-lookup"><span data-stu-id="dcac1-115">If you're in a non-US region, use the `-Environment` parameter to sign in.</span></span> <span data-ttu-id="dcac1-116">請使用 [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) Cmdlet 取得您區域的環境名稱。</span><span class="sxs-lookup"><span data-stu-id="dcac1-116">Get the name of the environment for your region by using the [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet.</span></span> <span data-ttu-id="dcac1-117">例如，若要登入 Azure China 21Vianet：</span><span class="sxs-lookup"><span data-stu-id="dcac1-117">For example, to sign in to Azure China 21Vianet:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="dcac1-118">您會獲得在 https://microsoft.com/devicelogin 上使用的權杖。</span><span class="sxs-lookup"><span data-stu-id="dcac1-118">You'll get a token to use on https://microsoft.com/devicelogin.</span></span> <span data-ttu-id="dcac1-119">在瀏覽器中開啟此頁面並輸入權杖，使用 Azure 帳戶認證來登入，然後授權 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="dcac1-119">Open this page in your browser and enter the token, then sign in with your Azure account credentials and authorize Azure PowerShell.</span></span> 

<span data-ttu-id="dcac1-120">登入後，您可以使用 Azure PowerShell Cmdlet 來存取和管理訂用帳戶中的資源。</span><span class="sxs-lookup"><span data-stu-id="dcac1-120">Once signed in, use the Azure PowerShell cmdlets to access and manage resources in your subscription.</span></span> <span data-ttu-id="dcac1-121">若要深入了解登入程序和驗證方法，請參閱[使用 Azure PowerShell 登入](authenticate-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="dcac1-121">To learn more about the sign-in process and authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="find-commands"></a><span data-ttu-id="dcac1-122">尋找命令</span><span class="sxs-lookup"><span data-stu-id="dcac1-122">Find commands</span></span>

<span data-ttu-id="dcac1-123">Azure PowerShell Cmdlet 會遵循 PowerShell 的標準命名慣例：`VERB-NOUN`。</span><span class="sxs-lookup"><span data-stu-id="dcac1-123">Azure PowerShell cmdlets follow a standard naming convention for PowerShell, `VERB-NOUN`.</span></span> <span data-ttu-id="dcac1-124">動詞描述動作 (例如 `Create`、`Get`、`Set`、`Delete`)，而名詞描述資源類型 (例如 `AzVM`、`AzKeyVaultCertificate`、`AzFirewall`、`AzVirtualNetworkGateway`)。</span><span class="sxs-lookup"><span data-stu-id="dcac1-124">The verb describes the action (examples include `Create`, `Get`, `Set`, `Delete`) and the noun describes the resource type (examples include `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span></span> <span data-ttu-id="dcac1-125">Azure PowerShell 中的名詞一律具有前置詞：`Az`。</span><span class="sxs-lookup"><span data-stu-id="dcac1-125">Nouns in Azure PowerShell always start with the prefix `Az`.</span></span> <span data-ttu-id="dcac1-126">如需標準動詞命令的完整清單，請參閱 [PowerShell 命令的已核准動詞](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands)。</span><span class="sxs-lookup"><span data-stu-id="dcac1-126">For the full list of standard verbs, see [Approved verbs for PowerShell Commands](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span></span>

<span data-ttu-id="dcac1-127">了解可用的名詞、動詞和 Azure PowerShell 模組可協助您透過 [Get-Command](/powershell/module/microsoft.powershell.core/get-command) Cmdlet 來尋找命令。</span><span class="sxs-lookup"><span data-stu-id="dcac1-127">Knowing the nouns, verbs, and the Azure PowerShell modules available help you find commands with the [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet.</span></span> <span data-ttu-id="dcac1-128">例如，若要尋找使用 `Get` 動詞的所有 VM 相關命令：</span><span class="sxs-lookup"><span data-stu-id="dcac1-128">For example, to find all VM-related commands that use the `Get` verb:</span></span>

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

<span data-ttu-id="dcac1-129">為協助您尋找常見的命令，此資料表列出可與 `Get-Command` 搭配的資源類型、對應 Azure PowerShell 模組和名詞前置詞：</span><span class="sxs-lookup"><span data-stu-id="dcac1-129">To help you find common commands, this table lists the resource type, corresponding Azure PowerShell module, and noun prefix to use with `Get-Command`:</span></span>

| <span data-ttu-id="dcac1-130">資源類型</span><span class="sxs-lookup"><span data-stu-id="dcac1-130">Resource type</span></span> | <span data-ttu-id="dcac1-131">Azure PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="dcac1-131">Azure PowerShell module</span></span> | <span data-ttu-id="dcac1-132">名詞前置詞</span><span class="sxs-lookup"><span data-stu-id="dcac1-132">Noun prefix</span></span> |
|---------------|-------------------------|----------------|
| [<span data-ttu-id="dcac1-133">資源群組</span><span class="sxs-lookup"><span data-stu-id="dcac1-133">Resource group</span></span>](/azure/azure-resource-manager/resource-group-overview) | [<span data-ttu-id="dcac1-134">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcac1-134">Az.Resources</span></span>](/powershell/module/az.resources#resources) | `AzResourceGroup` |
| [<span data-ttu-id="dcac1-135">虛擬機器</span><span class="sxs-lookup"><span data-stu-id="dcac1-135">Virtual machines</span></span>](/azure/virtual-machines) | [<span data-ttu-id="dcac1-136">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcac1-136">Az.Compute</span></span>](/powershell/module/az.compute#virtual_machines) | `AzVM` |
| [<span data-ttu-id="dcac1-137">儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="dcac1-137">Storage accounts</span></span>](/azure/storage/common/storage-introduction) | [<span data-ttu-id="dcac1-138">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcac1-138">Az.Storage</span></span>](/powershell/module/az.storage/) | `AzStorageAccount` |
| [<span data-ttu-id="dcac1-139">金鑰保存庫</span><span class="sxs-lookup"><span data-stu-id="dcac1-139">Key Vault</span></span>](/azure/key-vault/key-vault-whatis) | [<span data-ttu-id="dcac1-140">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dcac1-140">Az.KeyVault</span></span>](/powershell/module/az.keyvault) | `AzKeyVault` |
| [<span data-ttu-id="dcac1-141">Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="dcac1-141">Web applications</span></span>](/azure/app-service) | [<span data-ttu-id="dcac1-142">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dcac1-142">Az.Websites</span></span>](/powershell/module/az.websites) | `AzWebApp` |
| [<span data-ttu-id="dcac1-143">SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="dcac1-143">SQL databases</span></span>](/azure/sql-database) | [<span data-ttu-id="dcac1-144">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcac1-144">Az.Sql</span></span>](/powershell/module/az.sql) | `AzSqlDatabase` |

<span data-ttu-id="dcac1-145">如需 Azure PowerShell 中的完整模組清單，請參閱裝載於 GitHub 上的 [Azure PowerShell 模組清單](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md)。</span><span class="sxs-lookup"><span data-stu-id="dcac1-145">For a full list of the modules in Azure PowerShell, see the [Azure PowerShell modules list](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hosted on GitHub.</span></span>

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a><span data-ttu-id="dcac1-146">透過快速入門和教學課程了解 Azure PowerShell 基本概念</span><span class="sxs-lookup"><span data-stu-id="dcac1-146">Learn Azure PowerShell basics with quickstarts and tutorials</span></span>

<span data-ttu-id="dcac1-147">若要開始使用 Azure PowerShell，請從深入的教學課程嘗試設定虛擬機器，並學習如何查詢這些虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="dcac1-147">To get started with Azure PowerShell, try an in-depth tutorial for setting up virtual machines and learning how to query them.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="dcac1-148">使用 Azure PowerShell 建立虛擬機器</span><span class="sxs-lookup"><span data-stu-id="dcac1-148">Create virtual machines with Azure PowerShell</span></span>](azureps-vm-tutorial.yml)

<span data-ttu-id="dcac1-149">另外還有其他熱門 Azure 服務的 Azure PowerShell 快速入門：</span><span class="sxs-lookup"><span data-stu-id="dcac1-149">There are also Azure PowerShell quickstarts for other popular Azure services:</span></span>

* [<span data-ttu-id="dcac1-150">建立儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="dcac1-150">Create a storage account</span></span>](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [<span data-ttu-id="dcac1-151"> 在 Azure Blob 儲存體之間傳送物件</span><span class="sxs-lookup"><span data-stu-id="dcac1-151">Transfer objects to/from Azure Blob storage</span></span>](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [<span data-ttu-id="dcac1-152">從 Azure Key Vault 建立及擷取祕密</span><span class="sxs-lookup"><span data-stu-id="dcac1-152">Create and retrieve secrets from Azure Key Vault</span></span>](/azure/key-vault/quick-create-powershell)
* [<span data-ttu-id="dcac1-153">建立 Azure SQL 資料庫和防火牆</span><span class="sxs-lookup"><span data-stu-id="dcac1-153">Create an Azure SQL database and firewall</span></span>](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [<span data-ttu-id="dcac1-154">在 Azure 容器執行個體中執行容器</span><span class="sxs-lookup"><span data-stu-id="dcac1-154">Run a container in Azure Container Instances</span></span>](/azure/container-instances/container-instances-quickstart-powershell)
* [<span data-ttu-id="dcac1-155">建立虛擬機器擴展集 (VMSS)</span><span class="sxs-lookup"><span data-stu-id="dcac1-155">Create a Virtual Machine Scale Set (VMSS)</span></span>](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [<span data-ttu-id="dcac1-156">建立標準負載平衡器</span><span class="sxs-lookup"><span data-stu-id="dcac1-156">Create a standard load balancer</span></span>](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a><span data-ttu-id="dcac1-157">後續步驟</span><span class="sxs-lookup"><span data-stu-id="dcac1-157">Next steps</span></span>

* [<span data-ttu-id="dcac1-158">使用 Azure PowerShell 登入</span><span class="sxs-lookup"><span data-stu-id="dcac1-158">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="dcac1-159">使用 Azure PowerShell 來管理 Azure 訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="dcac1-159">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="dcac1-160">使用 Azure PowerShell 建立服務主體</span><span class="sxs-lookup"><span data-stu-id="dcac1-160">Create service principals with Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="dcac1-161">從社群獲得協助︰</span><span class="sxs-lookup"><span data-stu-id="dcac1-161">Get help from the community:</span></span>
  * [<span data-ttu-id="dcac1-162">MSDN 上的 Azure 論壇</span><span class="sxs-lookup"><span data-stu-id="dcac1-162">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="dcac1-163">Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="dcac1-163">Stacki Overflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
