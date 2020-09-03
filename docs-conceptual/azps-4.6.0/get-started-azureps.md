---
title: 開始使用 Azure PowerShell
description: ''
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 04/24/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 6281ac5f6ec8941e0d5c1755f90f99552db9aa92
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "89242251"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="1a83f-102">開始使用 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1a83f-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="1a83f-103">Azure PowerShell 的設計訴求是從命令列管理 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="1a83f-103">Azure PowerShell is designed for managing and administering Azure resources from the command line.</span></span>
<span data-ttu-id="1a83f-104">當您想要建置使用 Azure Resource Manager 模型的自動化工具時，就可以使用 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="1a83f-104">Use Azure PowerShell when you want to build automated tools that use the Azure Resource Manager model.</span></span> <span data-ttu-id="1a83f-105">您可以在瀏覽器中嘗試將其與 [Azure Cloud Shell](/azure/cloud-shell/overview) 搭配使用，或是將其安裝在本機電腦上。</span><span class="sxs-lookup"><span data-stu-id="1a83f-105">Try it out in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or install on your local machine.</span></span>

<span data-ttu-id="1a83f-106">本文可協助您開始使用 Azure PowerShell，並讓您知道其背後的核心概念。</span><span class="sxs-lookup"><span data-stu-id="1a83f-106">This article helps you get started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-or-run-in-azure-cloud-shell"></a><span data-ttu-id="1a83f-107">在 Azure Cloud Shell 中安裝或執行</span><span class="sxs-lookup"><span data-stu-id="1a83f-107">Install or run in Azure Cloud Shell</span></span>

<span data-ttu-id="1a83f-108">開始使用 Azure PowerShell 最簡單的方式是在 Azure Cloud Shell 環境中試用。</span><span class="sxs-lookup"><span data-stu-id="1a83f-108">The easiest way to get started with Azure PowerShell is by trying it out in an Azure Cloud Shell environment.</span></span> <span data-ttu-id="1a83f-109">若要啟動並執行 Cloud Shell，請參閱 [Azure Cloud Shell 中的 PowerShell 快速入門](/azure/cloud-shell/quickstart-powershell)。</span><span class="sxs-lookup"><span data-stu-id="1a83f-109">To get up and running with Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span> <span data-ttu-id="1a83f-110">Cloud Shell 會在 Linux 容器上執行 PowerShell，因此無法使用 Windows 特有的功能。</span><span class="sxs-lookup"><span data-stu-id="1a83f-110">Cloud Shell runs PowerShell on a Linux container, so Windows-specific functionality isn't available.</span></span>

<span data-ttu-id="1a83f-111">當您準備好在本機電腦上安裝 Azure PowerShell 時，請遵循[安裝 Azure PowerShell 模組](install-az-ps.md)中的指示。</span><span class="sxs-lookup"><span data-stu-id="1a83f-111">When you're ready to install Azure PowerShell on your local machine, follow the instructions in [Install the Azure PowerShell module](install-az-ps.md).</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="1a83f-112">登入 Azure</span><span class="sxs-lookup"><span data-stu-id="1a83f-112">Sign in to Azure</span></span>

<span data-ttu-id="1a83f-113">請使用 [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) Cmdlet，以互動方式登入。</span><span class="sxs-lookup"><span data-stu-id="1a83f-113">Sign in interactively with the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span> <span data-ttu-id="1a83f-114">如果您使用 Cloud Shell，請略過此步驟。</span><span class="sxs-lookup"><span data-stu-id="1a83f-114">Skip this step if you use Cloud Shell.</span></span> <span data-ttu-id="1a83f-115">您的 Azure Cloud Shell 工作階段已向啟動 Cloud Shell 工作階段的環境、訂用帳戶及租用戶完成驗證。</span><span class="sxs-lookup"><span data-stu-id="1a83f-115">Your Azure Cloud Shell session is already authenticated for the environment, subscription, and tenant that launched the Cloud Shell session.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="1a83f-116">Azure 雲端服務提供符合區域資料處理法規的環境。</span><span class="sxs-lookup"><span data-stu-id="1a83f-116">Azure cloud services offer environments compliant with regional data-handling laws.</span></span> <span data-ttu-id="1a83f-117">針對區域雲端中的帳戶，請使用**環境**參數來登入。</span><span class="sxs-lookup"><span data-stu-id="1a83f-117">For accounts in a regional cloud, use the **Environment** parameter to sign in.</span></span> <span data-ttu-id="1a83f-118">請使用 [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) Cmdlet 取得您區域的環境名稱。</span><span class="sxs-lookup"><span data-stu-id="1a83f-118">Get the name of the environment for your region using the [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet.</span></span>
<span data-ttu-id="1a83f-119">例如，若要登入 Azure China 21Vianet：</span><span class="sxs-lookup"><span data-stu-id="1a83f-119">For example, to sign in to Azure China 21Vianet:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="1a83f-120">您會在 Windows PowerShell 5.1 環境中收到登入對話方塊，請提供您 Azure 帳戶的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="1a83f-120">In Windows PowerShell 5.1 environments, you'll receive a sign-in dialog to provide a username and password for your Azure account.</span></span> <span data-ttu-id="1a83f-121">若使用其他版本的 PowerShell，則您會在 [microsoft.com/devicelogin](https://microsoft.com/devicelogin) 中取得要使用的權杖。</span><span class="sxs-lookup"><span data-stu-id="1a83f-121">On every other version of PowerShell, you'll get a token to use on [microsoft.com/devicelogin](https://microsoft.com/devicelogin).</span></span> <span data-ttu-id="1a83f-122">在瀏覽器中開啟此頁面並輸入權杖，使用 Azure 帳戶認證來登入，然後授權 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="1a83f-122">Open this page in your browser and enter the token, then sign in with your Azure account credentials and authorize Azure PowerShell.</span></span>

<span data-ttu-id="1a83f-123">登入之後，您會看到指出哪一個 Azure 訂用帳戶為作用中的資訊。</span><span class="sxs-lookup"><span data-stu-id="1a83f-123">After signing in, you'll see information indicating which of your Azure subscriptions is active.</span></span> <span data-ttu-id="1a83f-124">如果您的帳戶中有多個 Azure 訂用帳戶，且想要選取不同訂用帳戶，請使用 [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) 取得可用的訂用帳戶，並透過訂用帳戶識別碼使用 [Set-AzContext](/powershell/module/az.accounts/set-azcontext) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1a83f-124">If you have multiple Azure subscriptions in your account and want to select a different one, get your available subscriptions with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet with your subscription ID.</span></span> <span data-ttu-id="1a83f-125">如需管理 Azure PowerShell 中的 Azure 訂用帳戶詳細資訊，請參閱[使用多個 Azure 訂用帳戶](manage-subscriptions-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="1a83f-125">For more information about managing your Azure subscriptions in Azure PowerShell, see [Use multiple Azure subscriptions](manage-subscriptions-azureps.md).</span></span>

<span data-ttu-id="1a83f-126">登入後，您可以使用 Azure PowerShell Cmdlet 來存取和管理訂用帳戶中的資源。</span><span class="sxs-lookup"><span data-stu-id="1a83f-126">Once signed in, use the Azure PowerShell cmdlets to access and manage resources in your subscription.</span></span> <span data-ttu-id="1a83f-127">若要深入了解登入程序和驗證方法，請參閱[使用 Azure PowerShell 登入](authenticate-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="1a83f-127">To learn more about the sign-in process and authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="find-commands"></a><span data-ttu-id="1a83f-128">尋找命令</span><span class="sxs-lookup"><span data-stu-id="1a83f-128">Find commands</span></span>

<span data-ttu-id="1a83f-129">Azure PowerShell Cmdlet 會遵循 PowerShell 的標準命名慣例：`Verb-Noun`。</span><span class="sxs-lookup"><span data-stu-id="1a83f-129">Azure PowerShell cmdlets follow a standard naming convention for PowerShell, `Verb-Noun`.</span></span> <span data-ttu-id="1a83f-130">動詞描述動作 (例如 `New`、`Get`、`Set`、`Remove`)，而名詞描述資源類型 (例如 `AzVM`、`AzKeyVaultCertificate`、`AzFirewall`、`AzVirtualNetworkGateway`)。</span><span class="sxs-lookup"><span data-stu-id="1a83f-130">The verb describes the action (examples include `New`, `Get`, `Set`, `Remove`) and the noun describes the resource type (examples include `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span></span> <span data-ttu-id="1a83f-131">Azure PowerShell 中的名詞一律具有前置詞：`Az`。</span><span class="sxs-lookup"><span data-stu-id="1a83f-131">Nouns in Azure PowerShell always start with the prefix `Az`.</span></span> <span data-ttu-id="1a83f-132">如需標準動詞命令的完整清單，請參閱 [PowerShell 命令的已核准動詞](/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands)。</span><span class="sxs-lookup"><span data-stu-id="1a83f-132">For the full list of standard verbs, see [Approved verbs for PowerShell Commands](/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span></span>

<span data-ttu-id="1a83f-133">了解可用的名詞、動詞和 Azure PowerShell 模組可協助您透過 [Get-Command](/powershell/module/microsoft.powershell.core/get-command) Cmdlet 來尋找命令。</span><span class="sxs-lookup"><span data-stu-id="1a83f-133">Knowing the nouns, verbs, and the Azure PowerShell modules available helps you find commands with the [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet.</span></span> <span data-ttu-id="1a83f-134">例如，若要尋找使用 `Get` 動詞的所有 VM 相關命令：</span><span class="sxs-lookup"><span data-stu-id="1a83f-134">For example, to find all VM-related commands that use the `Get` verb:</span></span>

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

<span data-ttu-id="1a83f-135">為協助您尋找常見的命令，此資料表列出可與 `Get-Command` 搭配的資源類型、對應 Azure PowerShell 模組和名詞前置詞：</span><span class="sxs-lookup"><span data-stu-id="1a83f-135">To help you find common commands, this table lists the resource type, corresponding Azure PowerShell module, and noun prefix to use with `Get-Command`:</span></span>

|                              <span data-ttu-id="1a83f-136">資源類型</span><span class="sxs-lookup"><span data-stu-id="1a83f-136">Resource type</span></span>                              |                   <span data-ttu-id="1a83f-137">Azure PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="1a83f-137">Azure PowerShell module</span></span>                    |    <span data-ttu-id="1a83f-138">名詞前置詞</span><span class="sxs-lookup"><span data-stu-id="1a83f-138">Noun prefix</span></span>     |
| ----------------------------------------------------------------------- | ------------------------------------------------------------ | ------------------ |
| [<span data-ttu-id="1a83f-139">資源群組</span><span class="sxs-lookup"><span data-stu-id="1a83f-139">Resource group</span></span>](/azure/azure-resource-manager/resource-group-overview) | [<span data-ttu-id="1a83f-140">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1a83f-140">Az.Resources</span></span>](/powershell/module/az.resources#resources)    | `AzResourceGroup`  |
| [<span data-ttu-id="1a83f-141">虛擬機器</span><span class="sxs-lookup"><span data-stu-id="1a83f-141">Virtual machines</span></span>](/azure/virtual-machines)                             | [<span data-ttu-id="1a83f-142">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1a83f-142">Az.Compute</span></span>](/powershell/module/az.compute#virtual_machines) | `AzVM`             |
| [<span data-ttu-id="1a83f-143">儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="1a83f-143">Storage accounts</span></span>](/azure/storage/common/storage-introduction)          | [<span data-ttu-id="1a83f-144">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1a83f-144">Az.Storage</span></span>](/powershell/module/az.storage/)                 | `AzStorageAccount` |
| [<span data-ttu-id="1a83f-145">金鑰保存庫</span><span class="sxs-lookup"><span data-stu-id="1a83f-145">Key Vault</span></span>](/azure/key-vault/key-vault-whatis)                          | [<span data-ttu-id="1a83f-146">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1a83f-146">Az.KeyVault</span></span>](/powershell/module/az.keyvault)                | `AzKeyVault`       |
| [<span data-ttu-id="1a83f-147">Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="1a83f-147">Web applications</span></span>](/azure/app-service)                                  | [<span data-ttu-id="1a83f-148">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1a83f-148">Az.Websites</span></span>](/powershell/module/az.websites)                | `AzWebApp`         |
| [<span data-ttu-id="1a83f-149">SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="1a83f-149">SQL databases</span></span>](/azure/sql-database)                                    | [<span data-ttu-id="1a83f-150">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1a83f-150">Az.Sql</span></span>](/powershell/module/az.sql)                          | `AzSqlDatabase`    |

<span data-ttu-id="1a83f-151">如需 Azure PowerShell 中的完整模組清單，請參閱裝載於 GitHub 上的 [Azure PowerShell 模組清單](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md)。</span><span class="sxs-lookup"><span data-stu-id="1a83f-151">For a full list of the modules in Azure PowerShell, see the [Azure PowerShell modules list](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hosted on GitHub.</span></span>

## <a name="telemetry"></a><span data-ttu-id="1a83f-152">遙測</span><span class="sxs-lookup"><span data-stu-id="1a83f-152">Telemetry</span></span>

<span data-ttu-id="1a83f-153">Azure PowerShell 預設為自動收集遙測資料。</span><span class="sxs-lookup"><span data-stu-id="1a83f-153">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="1a83f-154">Microsoft 彙總收集的資料，以識別使用模式、識別常見的問題，以及改善 Azure PowerShell 的體驗。</span><span class="sxs-lookup"><span data-stu-id="1a83f-154">Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span> <span data-ttu-id="1a83f-155">Microsoft Azure PowerShell 不會收集任何私人或個人資料。</span><span class="sxs-lookup"><span data-stu-id="1a83f-155">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="1a83f-156">若要停用資料收集，您必須執行 [AzDataCollection](/powershell/module/az.accounts/disable-azdatacollection)，以明確退出。</span><span class="sxs-lookup"><span data-stu-id="1a83f-156">To disable data collection, you must explicitly opt out by executing [Disable-AzDataCollection](/powershell/module/az.accounts/disable-azdatacollection).</span></span>

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a><span data-ttu-id="1a83f-157">透過快速入門和教學課程了解 Azure PowerShell 基本概念</span><span class="sxs-lookup"><span data-stu-id="1a83f-157">Learn Azure PowerShell basics with quickstarts and tutorials</span></span>

<span data-ttu-id="1a83f-158">若要開始使用 Azure PowerShell，請從深入的教學課程嘗試設定虛擬機器，並學習如何查詢這些虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="1a83f-158">To get started with Azure PowerShell, try an in-depth tutorial for setting up virtual machines and learning how to query them.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="1a83f-159">使用 Azure PowerShell 建立虛擬機器</span><span class="sxs-lookup"><span data-stu-id="1a83f-159">Create virtual machines with Azure PowerShell</span></span>](azureps-vm-tutorial.yml)

<span data-ttu-id="1a83f-160">另外還有其他熱門 Azure 服務的 Azure PowerShell 快速入門：</span><span class="sxs-lookup"><span data-stu-id="1a83f-160">There are also Azure PowerShell quickstarts for other popular Azure services:</span></span>

* [<span data-ttu-id="1a83f-161">建立儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="1a83f-161">Create a storage account</span></span>](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [<span data-ttu-id="1a83f-162"> 在 Azure Blob 儲存體之間傳送物件</span><span class="sxs-lookup"><span data-stu-id="1a83f-162">Transfer objects to/from Azure Blob storage</span></span>](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [<span data-ttu-id="1a83f-163">從 Azure Key Vault 建立及擷取祕密</span><span class="sxs-lookup"><span data-stu-id="1a83f-163">Create and retrieve secrets from Azure Key Vault</span></span>](/azure/key-vault/quick-create-powershell)
* [<span data-ttu-id="1a83f-164">建立 Azure SQL 資料庫和防火牆</span><span class="sxs-lookup"><span data-stu-id="1a83f-164">Create an Azure SQL database and firewall</span></span>](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [<span data-ttu-id="1a83f-165">在 Azure 容器執行個體中執行容器</span><span class="sxs-lookup"><span data-stu-id="1a83f-165">Run a container in Azure Container Instances</span></span>](/azure/container-instances/container-instances-quickstart-powershell)
* [<span data-ttu-id="1a83f-166">建立虛擬機器擴展集</span><span class="sxs-lookup"><span data-stu-id="1a83f-166">Create a Virtual Machine Scale Set</span></span>](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [<span data-ttu-id="1a83f-167">建立標準負載平衡器</span><span class="sxs-lookup"><span data-stu-id="1a83f-167">Create a standard load balancer</span></span>](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a><span data-ttu-id="1a83f-168">後續步驟</span><span class="sxs-lookup"><span data-stu-id="1a83f-168">Next steps</span></span>

* [<span data-ttu-id="1a83f-169">使用 Azure PowerShell 登入</span><span class="sxs-lookup"><span data-stu-id="1a83f-169">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="1a83f-170">使用 Azure PowerShell 來管理 Azure 訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="1a83f-170">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="1a83f-171">使用 Azure PowerShell 建立服務主體</span><span class="sxs-lookup"><span data-stu-id="1a83f-171">Create service principals with Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="1a83f-172">從社群獲得協助︰</span><span class="sxs-lookup"><span data-stu-id="1a83f-172">Get help from the community:</span></span>
  * [<span data-ttu-id="1a83f-173">MSDN 上的 Azure 論壇</span><span class="sxs-lookup"><span data-stu-id="1a83f-173">Azure forum on MSDN</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="1a83f-174">Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="1a83f-174">Stack Overflow</span></span>](https://go.microsoft.com/fwlink/?LinkId=320213)
