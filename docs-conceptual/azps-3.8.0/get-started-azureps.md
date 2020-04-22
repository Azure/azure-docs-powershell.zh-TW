---
title: 開始使用 Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 01/17/2020
ms.openlocfilehash: 718f0dc0f1ef9b0c2aa3d0630ca099fa5cec7ec0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "81740349"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="22554-102">開始使用 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="22554-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="22554-103">Azure PowerShell 的設計訴求是從命令列管理 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="22554-103">Azure PowerShell is designed for managing and administering Azure resources from the command line.</span></span> <span data-ttu-id="22554-104">當您想要建置使用 Azure Resource Manager 模型的自動化工具時，就可以使用 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="22554-104">Use Azure PowerShell when you want to build automated tools that use the Azure Resource Manager model.</span></span>
<span data-ttu-id="22554-105">您可以在瀏覽器中嘗試將其與 [Azure Cloud Shell](/azure/cloud-shell/overview) 搭配使用，或是將其安裝在本機電腦上。</span><span class="sxs-lookup"><span data-stu-id="22554-105">Try it out in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or install on your local machine.</span></span>

<span data-ttu-id="22554-106">本文可協助您開始使用 Azure PowerShell，並讓您知道其背後的核心概念。</span><span class="sxs-lookup"><span data-stu-id="22554-106">This article helps you get started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-or-run-in-azure-cloud-shell"></a><span data-ttu-id="22554-107">在 Azure Cloud Shell 中安裝或執行</span><span class="sxs-lookup"><span data-stu-id="22554-107">Install or run in Azure Cloud Shell</span></span>

<span data-ttu-id="22554-108">開始使用 Azure PowerShell 最簡單的方式是在 Azure Cloud Shell 環境中試用。</span><span class="sxs-lookup"><span data-stu-id="22554-108">The easiest way to get started with Azure PowerShell is by trying it out in an Azure Cloud Shell environment.</span></span>
<span data-ttu-id="22554-109">若要啟動並執行 Cloud Shell，請參閱 [Azure Cloud Shell 中的 PowerShell 快速入門](/azure/cloud-shell/quickstart-powershell)。</span><span class="sxs-lookup"><span data-stu-id="22554-109">To get up and running with Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
<span data-ttu-id="22554-110">Cloud Shell 會在 Linux 容器上執行 PowerShell 6，因此無法使用 Windows 特有的功能。</span><span class="sxs-lookup"><span data-stu-id="22554-110">Cloud Shell runs PowerShell 6 on a Linux container, so Windows-specific functionality isn't available.</span></span>

<span data-ttu-id="22554-111">當您準備好在本機電腦上安裝 Azure PowerShell 時，請遵循[安裝 Azure PowerShell 模組](install-az-ps.md)中的指示。</span><span class="sxs-lookup"><span data-stu-id="22554-111">When you're ready to install Azure PowerShell on your local machine, follow the instructions in [Install the Azure PowerShell module](install-az-ps.md).</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="22554-112">登入 Azure</span><span class="sxs-lookup"><span data-stu-id="22554-112">Sign in to Azure</span></span>

<span data-ttu-id="22554-113">使用 `Connect-AzAccount` Cmdlet 以互動方式登入。</span><span class="sxs-lookup"><span data-stu-id="22554-113">Sign in interactively with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="22554-114">如果您使用 Cloud Shell，請略過此步驟：您的 Azure Cloud Shell 工作階段已向啟動 Cloud Shell 工作階段的環境、訂用帳戶及租用戶完成驗證。</span><span class="sxs-lookup"><span data-stu-id="22554-114">Skip this step if you use Cloud Shell: Your Azure Cloud Shell session is already authenticated for the environment, subscription, and tenant that launched the Cloud Shell session.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="22554-115">如果您不是位於美國區域，請使用 `-Environment` 參數來登入。</span><span class="sxs-lookup"><span data-stu-id="22554-115">If you're in a non-US region, use the `-Environment` parameter to sign in.</span></span> <span data-ttu-id="22554-116">請使用 [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) Cmdlet 取得您區域的環境名稱。</span><span class="sxs-lookup"><span data-stu-id="22554-116">Get the name of the environment for your region by using the [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet.</span></span> <span data-ttu-id="22554-117">例如，若要登入 Azure China 21Vianet：</span><span class="sxs-lookup"><span data-stu-id="22554-117">For example, to sign in to Azure China 21Vianet:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="22554-118">您會在 PowerShell 5.1 環境中看到登入對話方塊，請提供您 Azure 帳戶的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="22554-118">In PowerShell 5.1 environments, you'll get a sign-in dialog to provide a username and password for your Azure account.</span></span> <span data-ttu-id="22554-119">若使用其他版本的 PowerShell，則您會在 [https://microsoft.com/devicelogin ] 中取得要使用的權杖。</span><span class="sxs-lookup"><span data-stu-id="22554-119">On every other version of PowerShell, you'll get a token to use on [https://microsoft.com/devicelogin].</span></span>
<span data-ttu-id="22554-120">在瀏覽器中開啟此頁面並輸入權杖，使用 Azure 帳戶認證來登入，然後授權 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="22554-120">Open this page in your browser and enter the token, then sign in with your Azure account credentials and authorize Azure PowerShell.</span></span>

<span data-ttu-id="22554-121">登入之後，您會看到指出哪一個 Azure 訂用帳戶為作用中的資訊。</span><span class="sxs-lookup"><span data-stu-id="22554-121">After signing in, you'll see information indicating which of your Azure subscriptions is active.</span></span> <span data-ttu-id="22554-122">如果您的帳戶中有多個 Azure 訂用帳戶，且想要選取不同訂用帳戶，請使用 [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) 取得可用的訂用帳戶，並透過訂用帳戶識別碼使用 [Set-AzContext](/powershell/module/az.accounts/set-azcontext) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="22554-122">If you have multiple Azure subscriptions in your account and want to select a different one, get your available subscriptions with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet with your subscription ID.</span></span>
<span data-ttu-id="22554-123">如需管理 Azure PowerShell 中的 Azure 訂用帳戶詳細資訊，請參閱[使用多個 Azure 訂用帳戶](manage-subscriptions-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="22554-123">For more information about managing your Azure subscriptions in Azure PowerShell, see [Use multiple Azure subscriptions](manage-subscriptions-azureps.md).</span></span>

<span data-ttu-id="22554-124">登入後，您可以使用 Azure PowerShell Cmdlet 來存取和管理訂用帳戶中的資源。</span><span class="sxs-lookup"><span data-stu-id="22554-124">Once signed in, use the Azure PowerShell cmdlets to access and manage resources in your subscription.</span></span> <span data-ttu-id="22554-125">若要深入了解登入程序和驗證方法，請參閱[使用 Azure PowerShell 登入](authenticate-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="22554-125">To learn more about the sign-in process and authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="find-commands"></a><span data-ttu-id="22554-126">尋找命令</span><span class="sxs-lookup"><span data-stu-id="22554-126">Find commands</span></span>

<span data-ttu-id="22554-127">Azure PowerShell Cmdlet 會遵循 PowerShell 的標準命名慣例：`VERB-NOUN`。</span><span class="sxs-lookup"><span data-stu-id="22554-127">Azure PowerShell cmdlets follow a standard naming convention for PowerShell, `VERB-NOUN`.</span></span> <span data-ttu-id="22554-128">動詞描述動作 (例如 `New`、`Get`、`Set`、`Remove`)，而名詞描述資源類型 (例如 `AzVM`、`AzKeyVaultCertificate`、`AzFirewall`、`AzVirtualNetworkGateway`)。</span><span class="sxs-lookup"><span data-stu-id="22554-128">The verb describes the action (examples include `New`, `Get`, `Set`, `Remove`) and the noun describes the resource type (examples include `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span></span> <span data-ttu-id="22554-129">Azure PowerShell 中的名詞一律具有前置詞：`Az`。</span><span class="sxs-lookup"><span data-stu-id="22554-129">Nouns in Azure PowerShell always start with the prefix `Az`.</span></span> <span data-ttu-id="22554-130">如需標準動詞命令的完整清單，請參閱 [PowerShell 命令的已核准動詞](/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands)。</span><span class="sxs-lookup"><span data-stu-id="22554-130">For the full list of standard verbs, see [Approved verbs for PowerShell Commands](/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span></span>

<span data-ttu-id="22554-131">了解可用的名詞、動詞和 Azure PowerShell 模組可協助您透過 [Get-Command](/powershell/module/microsoft.powershell.core/get-command) Cmdlet 來尋找命令。</span><span class="sxs-lookup"><span data-stu-id="22554-131">Knowing the nouns, verbs, and the Azure PowerShell modules available help you find commands with the [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet.</span></span> <span data-ttu-id="22554-132">例如，若要尋找使用 `Get` 動詞的所有 VM 相關命令：</span><span class="sxs-lookup"><span data-stu-id="22554-132">For example, to find all VM-related commands that use the `Get` verb:</span></span>

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

<span data-ttu-id="22554-133">為協助您尋找常見的命令，此資料表列出可與 `Get-Command` 搭配的資源類型、對應 Azure PowerShell 模組和名詞前置詞：</span><span class="sxs-lookup"><span data-stu-id="22554-133">To help you find common commands, this table lists the resource type, corresponding Azure PowerShell module, and noun prefix to use with `Get-Command`:</span></span>

| <span data-ttu-id="22554-134">資源類型</span><span class="sxs-lookup"><span data-stu-id="22554-134">Resource type</span></span> | <span data-ttu-id="22554-135">Azure PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="22554-135">Azure PowerShell module</span></span> | <span data-ttu-id="22554-136">名詞前置詞</span><span class="sxs-lookup"><span data-stu-id="22554-136">Noun prefix</span></span> |
|---------------|-------------------------|----------------|
| [<span data-ttu-id="22554-137">資源群組</span><span class="sxs-lookup"><span data-stu-id="22554-137">Resource group</span></span>](/azure/azure-resource-manager/resource-group-overview) | [<span data-ttu-id="22554-138">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="22554-138">Az.Resources</span></span>](/powershell/module/az.resources#resources) | `AzResourceGroup` |
| [<span data-ttu-id="22554-139">虛擬機器</span><span class="sxs-lookup"><span data-stu-id="22554-139">Virtual machines</span></span>](/azure/virtual-machines) | [<span data-ttu-id="22554-140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="22554-140">Az.Compute</span></span>](/powershell/module/az.compute#virtual_machines) | `AzVM` |
| [<span data-ttu-id="22554-141">儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="22554-141">Storage accounts</span></span>](/azure/storage/common/storage-introduction) | [<span data-ttu-id="22554-142">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="22554-142">Az.Storage</span></span>](/powershell/module/az.storage/) | `AzStorageAccount` |
| [<span data-ttu-id="22554-143">金鑰保存庫</span><span class="sxs-lookup"><span data-stu-id="22554-143">Key Vault</span></span>](/azure/key-vault/key-vault-whatis) | [<span data-ttu-id="22554-144">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="22554-144">Az.KeyVault</span></span>](/powershell/module/az.keyvault) | `AzKeyVault` |
| [<span data-ttu-id="22554-145">Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="22554-145">Web applications</span></span>](/azure/app-service) | [<span data-ttu-id="22554-146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="22554-146">Az.Websites</span></span>](/powershell/module/az.websites) | `AzWebApp` |
| [<span data-ttu-id="22554-147">SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="22554-147">SQL databases</span></span>](/azure/sql-database) | [<span data-ttu-id="22554-148">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="22554-148">Az.Sql</span></span>](/powershell/module/az.sql) | `AzSqlDatabase` |

<span data-ttu-id="22554-149">如需 Azure PowerShell 中的完整模組清單，請參閱裝載於 GitHub 上的 [Azure PowerShell 模組清單](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md)。</span><span class="sxs-lookup"><span data-stu-id="22554-149">For a full list of the modules in Azure PowerShell, see the [Azure PowerShell modules list](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hosted on GitHub.</span></span>

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a><span data-ttu-id="22554-150">透過快速入門和教學課程了解 Azure PowerShell 基本概念</span><span class="sxs-lookup"><span data-stu-id="22554-150">Learn Azure PowerShell basics with quickstarts and tutorials</span></span>

<span data-ttu-id="22554-151">若要開始使用 Azure PowerShell，請從深入的教學課程嘗試設定虛擬機器，並學習如何查詢這些虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="22554-151">To get started with Azure PowerShell, try an in-depth tutorial for setting up virtual machines and learning how to query them.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="22554-152">使用 Azure PowerShell 建立虛擬機器</span><span class="sxs-lookup"><span data-stu-id="22554-152">Create virtual machines with Azure PowerShell</span></span>](azureps-vm-tutorial.yml)

<span data-ttu-id="22554-153">另外還有其他熱門 Azure 服務的 Azure PowerShell 快速入門：</span><span class="sxs-lookup"><span data-stu-id="22554-153">There are also Azure PowerShell quickstarts for other popular Azure services:</span></span>

* [<span data-ttu-id="22554-154">建立儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="22554-154">Create a storage account</span></span>](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [<span data-ttu-id="22554-155"> 在 Azure Blob 儲存體之間傳送物件</span><span class="sxs-lookup"><span data-stu-id="22554-155">Transfer objects to/from Azure Blob storage</span></span>](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [<span data-ttu-id="22554-156">從 Azure Key Vault 建立及擷取祕密</span><span class="sxs-lookup"><span data-stu-id="22554-156">Create and retrieve secrets from Azure Key Vault</span></span>](/azure/key-vault/quick-create-powershell)
* [<span data-ttu-id="22554-157">建立 Azure SQL 資料庫和防火牆</span><span class="sxs-lookup"><span data-stu-id="22554-157">Create an Azure SQL database and firewall</span></span>](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [<span data-ttu-id="22554-158">在 Azure 容器執行個體中執行容器</span><span class="sxs-lookup"><span data-stu-id="22554-158">Run a container in Azure Container Instances</span></span>](/azure/container-instances/container-instances-quickstart-powershell)
* [<span data-ttu-id="22554-159">建立虛擬機器擴展集 (VMSS)</span><span class="sxs-lookup"><span data-stu-id="22554-159">Create a Virtual Machine Scale Set (VMSS)</span></span>](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [<span data-ttu-id="22554-160">建立標準負載平衡器</span><span class="sxs-lookup"><span data-stu-id="22554-160">Create a standard load balancer</span></span>](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a><span data-ttu-id="22554-161">後續步驟</span><span class="sxs-lookup"><span data-stu-id="22554-161">Next steps</span></span>

* [<span data-ttu-id="22554-162">使用 Azure PowerShell 登入</span><span class="sxs-lookup"><span data-stu-id="22554-162">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="22554-163">使用 Azure PowerShell 來管理 Azure 訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="22554-163">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="22554-164">使用 Azure PowerShell 建立服務主體</span><span class="sxs-lookup"><span data-stu-id="22554-164">Create service principals with Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="22554-165">從社群獲得協助︰</span><span class="sxs-lookup"><span data-stu-id="22554-165">Get help from the community:</span></span>
  * [<span data-ttu-id="22554-166">MSDN 上的 Azure 論壇</span><span class="sxs-lookup"><span data-stu-id="22554-166">Azure forum on MSDN</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="22554-167">Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="22554-167">Stack Overflow</span></span>](https://go.microsoft.com/fwlink/?LinkId=320213)
