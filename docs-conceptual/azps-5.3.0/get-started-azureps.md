---
title: 開始使用 Azure PowerShell
description: 開始使用 Azure PowerShell
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 04/24/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 68b2b50afdd2dc79bdbd8f8b203a7cd3664c4973
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "97893510"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="131a8-103">開始使用 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="131a8-103">Get started with Azure PowerShell</span></span>

<span data-ttu-id="131a8-104">Azure PowerShell 的設計訴求是從命令列管理 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="131a8-104">Azure PowerShell is designed for managing and administering Azure resources from the command line.</span></span>
<span data-ttu-id="131a8-105">當您想要建置使用 Azure Resource Manager 模型的自動化工具時，就可以使用 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="131a8-105">Use Azure PowerShell when you want to build automated tools that use the Azure Resource Manager model.</span></span> <span data-ttu-id="131a8-106">您可以在瀏覽器中嘗試將其與 [Azure Cloud Shell](/azure/cloud-shell/overview) 搭配使用，或是將其安裝在本機電腦上。</span><span class="sxs-lookup"><span data-stu-id="131a8-106">Try it out in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or install on your local machine.</span></span>

<span data-ttu-id="131a8-107">本文可協助您開始使用 Azure PowerShell，並讓您知道其背後的核心概念。</span><span class="sxs-lookup"><span data-stu-id="131a8-107">This article helps you get started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-or-run-in-azure-cloud-shell"></a><span data-ttu-id="131a8-108">在 Azure Cloud Shell 中安裝或執行</span><span class="sxs-lookup"><span data-stu-id="131a8-108">Install or run in Azure Cloud Shell</span></span>

<span data-ttu-id="131a8-109">開始使用 Azure PowerShell 最簡單的方式是在 Azure Cloud Shell 環境中試用。</span><span class="sxs-lookup"><span data-stu-id="131a8-109">The easiest way to get started with Azure PowerShell is by trying it out in an Azure Cloud Shell environment.</span></span> <span data-ttu-id="131a8-110">若要啟動並執行 Cloud Shell，請參閱 [Azure Cloud Shell 中的 PowerShell 快速入門](/azure/cloud-shell/quickstart-powershell)。</span><span class="sxs-lookup"><span data-stu-id="131a8-110">To get up and running with Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span> <span data-ttu-id="131a8-111">Cloud Shell 會在 Linux 容器上執行 PowerShell，因此無法使用 Windows 特有的功能。</span><span class="sxs-lookup"><span data-stu-id="131a8-111">Cloud Shell runs PowerShell on a Linux container, so Windows-specific functionality isn't available.</span></span>

<span data-ttu-id="131a8-112">當您準備好在本機電腦上安裝 Azure PowerShell 時，請遵循[安裝 Azure PowerShell 模組](install-az-ps.md)中的指示。</span><span class="sxs-lookup"><span data-stu-id="131a8-112">When you're ready to install Azure PowerShell on your local machine, follow the instructions in [Install the Azure PowerShell module](install-az-ps.md).</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="131a8-113">登入 Azure</span><span class="sxs-lookup"><span data-stu-id="131a8-113">Sign in to Azure</span></span>

<span data-ttu-id="131a8-114">請使用 [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) Cmdlet，以互動方式登入。</span><span class="sxs-lookup"><span data-stu-id="131a8-114">Sign in interactively with the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span> <span data-ttu-id="131a8-115">如果您使用 Cloud Shell，請略過此步驟。</span><span class="sxs-lookup"><span data-stu-id="131a8-115">Skip this step if you use Cloud Shell.</span></span> <span data-ttu-id="131a8-116">您的 Azure Cloud Shell 工作階段已向啟動 Cloud Shell 工作階段的環境、訂用帳戶及租用戶完成驗證。</span><span class="sxs-lookup"><span data-stu-id="131a8-116">Your Azure Cloud Shell session is already authenticated for the environment, subscription, and tenant that launched the Cloud Shell session.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="131a8-117">Azure 雲端服務提供符合區域資料處理法規的環境。</span><span class="sxs-lookup"><span data-stu-id="131a8-117">Azure cloud services offer environments compliant with regional data-handling laws.</span></span> <span data-ttu-id="131a8-118">針對區域雲端中的帳戶，請使用 **環境** 參數來登入。</span><span class="sxs-lookup"><span data-stu-id="131a8-118">For accounts in a regional cloud, use the **Environment** parameter to sign in.</span></span> <span data-ttu-id="131a8-119">請使用 [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) Cmdlet 取得您區域的環境名稱。</span><span class="sxs-lookup"><span data-stu-id="131a8-119">Get the name of the environment for your region using the [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet.</span></span>
<span data-ttu-id="131a8-120">例如，若要登入 Azure China 21Vianet：</span><span class="sxs-lookup"><span data-stu-id="131a8-120">For example, to sign in to Azure China 21Vianet:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="131a8-121">您會在 Windows PowerShell 5.1 環境中收到登入對話方塊，請提供您 Azure 帳戶的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="131a8-121">In Windows PowerShell 5.1 environments, you'll receive a sign-in dialog to provide a username and password for your Azure account.</span></span> <span data-ttu-id="131a8-122">若使用其他版本的 PowerShell，則您會在 [microsoft.com/devicelogin](https://microsoft.com/devicelogin) 中取得要使用的權杖。</span><span class="sxs-lookup"><span data-stu-id="131a8-122">On every other version of PowerShell, you'll get a token to use on [microsoft.com/devicelogin](https://microsoft.com/devicelogin).</span></span> <span data-ttu-id="131a8-123">在瀏覽器中開啟此頁面並輸入權杖，使用 Azure 帳戶認證來登入，然後授權 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="131a8-123">Open this page in your browser and enter the token, then sign in with your Azure account credentials and authorize Azure PowerShell.</span></span>

<span data-ttu-id="131a8-124">登入之後，您會看到指出哪一個 Azure 訂用帳戶為作用中的資訊。</span><span class="sxs-lookup"><span data-stu-id="131a8-124">After signing in, you'll see information indicating which of your Azure subscriptions is active.</span></span> <span data-ttu-id="131a8-125">如果您的帳戶中有多個 Azure 訂用帳戶，且想要選取不同訂用帳戶，請使用 [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) 取得可用的訂用帳戶，並透過訂用帳戶識別碼使用 [Set-AzContext](/powershell/module/az.accounts/set-azcontext) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="131a8-125">If you have multiple Azure subscriptions in your account and want to select a different one, get your available subscriptions with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet with your subscription ID.</span></span> <span data-ttu-id="131a8-126">如需管理 Azure PowerShell 中的 Azure 訂用帳戶詳細資訊，請參閱[使用多個 Azure 訂用帳戶](manage-subscriptions-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="131a8-126">For more information about managing your Azure subscriptions in Azure PowerShell, see [Use multiple Azure subscriptions](manage-subscriptions-azureps.md).</span></span>

<span data-ttu-id="131a8-127">登入後，您可以使用 Azure PowerShell Cmdlet 來存取和管理訂用帳戶中的資源。</span><span class="sxs-lookup"><span data-stu-id="131a8-127">Once signed in, use the Azure PowerShell cmdlets to access and manage resources in your subscription.</span></span> <span data-ttu-id="131a8-128">若要深入了解登入程序和驗證方法，請參閱[使用 Azure PowerShell 登入](authenticate-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="131a8-128">To learn more about the sign-in process and authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="find-commands"></a><span data-ttu-id="131a8-129">尋找命令</span><span class="sxs-lookup"><span data-stu-id="131a8-129">Find commands</span></span>

<span data-ttu-id="131a8-130">Azure PowerShell Cmdlet 會遵循 PowerShell 的標準命名慣例：`Verb-Noun`。</span><span class="sxs-lookup"><span data-stu-id="131a8-130">Azure PowerShell cmdlets follow a standard naming convention for PowerShell, `Verb-Noun`.</span></span> <span data-ttu-id="131a8-131">動詞描述動作 (例如 `New`、`Get`、`Set`、`Remove`)，而名詞描述資源類型 (例如 `AzVM`、`AzKeyVaultCertificate`、`AzFirewall`、`AzVirtualNetworkGateway`)。</span><span class="sxs-lookup"><span data-stu-id="131a8-131">The verb describes the action (examples include `New`, `Get`, `Set`, `Remove`) and the noun describes the resource type (examples include `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span></span> <span data-ttu-id="131a8-132">Azure PowerShell 中的名詞一律具有前置詞：`Az`。</span><span class="sxs-lookup"><span data-stu-id="131a8-132">Nouns in Azure PowerShell always start with the prefix `Az`.</span></span> <span data-ttu-id="131a8-133">如需標準動詞命令的完整清單，請參閱 [PowerShell 命令的已核准動詞](/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands)。</span><span class="sxs-lookup"><span data-stu-id="131a8-133">For the full list of standard verbs, see [Approved verbs for PowerShell Commands](/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span></span>

<span data-ttu-id="131a8-134">了解可用的名詞、動詞和 Azure PowerShell 模組可協助您透過 [Get-Command](/powershell/module/microsoft.powershell.core/get-command) Cmdlet 來尋找命令。</span><span class="sxs-lookup"><span data-stu-id="131a8-134">Knowing the nouns, verbs, and the Azure PowerShell modules available helps you find commands with the [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet.</span></span> <span data-ttu-id="131a8-135">例如，若要尋找使用 `Get` 動詞的所有 VM 相關命令：</span><span class="sxs-lookup"><span data-stu-id="131a8-135">For example, to find all VM-related commands that use the `Get` verb:</span></span>

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

<span data-ttu-id="131a8-136">為協助您尋找常見的命令，此資料表列出可與 `Get-Command` 搭配的資源類型、對應 Azure PowerShell 模組和名詞前置詞：</span><span class="sxs-lookup"><span data-stu-id="131a8-136">To help you find common commands, this table lists the resource type, corresponding Azure PowerShell module, and noun prefix to use with `Get-Command`:</span></span>

|                              <span data-ttu-id="131a8-137">資源類型</span><span class="sxs-lookup"><span data-stu-id="131a8-137">Resource type</span></span>                              |                   <span data-ttu-id="131a8-138">Azure PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="131a8-138">Azure PowerShell module</span></span>                    |    <span data-ttu-id="131a8-139">名詞前置詞</span><span class="sxs-lookup"><span data-stu-id="131a8-139">Noun prefix</span></span>     |
| ----------------------------------------------------------------------- | ------------------------------------------------------------ | ------------------ |
| [<span data-ttu-id="131a8-140">資源群組</span><span class="sxs-lookup"><span data-stu-id="131a8-140">Resource group</span></span>](/azure/azure-resource-manager/resource-group-overview) | [<span data-ttu-id="131a8-141">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="131a8-141">Az.Resources</span></span>](/powershell/module/az.resources#resources)    | `AzResourceGroup`  |
| [<span data-ttu-id="131a8-142">虛擬機器</span><span class="sxs-lookup"><span data-stu-id="131a8-142">Virtual machines</span></span>](/azure/virtual-machines)                             | [<span data-ttu-id="131a8-143">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="131a8-143">Az.Compute</span></span>](/powershell/module/az.compute#virtual_machines) | `AzVM`             |
| [<span data-ttu-id="131a8-144">儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="131a8-144">Storage accounts</span></span>](/azure/storage/common/storage-introduction)          | [<span data-ttu-id="131a8-145">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="131a8-145">Az.Storage</span></span>](/powershell/module/az.storage/)                 | `AzStorageAccount` |
| [<span data-ttu-id="131a8-146">金鑰保存庫</span><span class="sxs-lookup"><span data-stu-id="131a8-146">Key Vault</span></span>](/azure/key-vault/key-vault-whatis)                          | [<span data-ttu-id="131a8-147">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="131a8-147">Az.KeyVault</span></span>](/powershell/module/az.keyvault)                | `AzKeyVault`       |
| [<span data-ttu-id="131a8-148">Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="131a8-148">Web applications</span></span>](/azure/app-service)                                  | [<span data-ttu-id="131a8-149">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="131a8-149">Az.Websites</span></span>](/powershell/module/az.websites)                | `AzWebApp`         |
| [<span data-ttu-id="131a8-150">SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="131a8-150">SQL databases</span></span>](/azure/sql-database)                                    | [<span data-ttu-id="131a8-151">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="131a8-151">Az.Sql</span></span>](/powershell/module/az.sql)                          | `AzSqlDatabase`    |

<span data-ttu-id="131a8-152">如需 Azure PowerShell 中的完整模組清單，請參閱裝載於 GitHub 上的 [Azure PowerShell 模組清單](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md)。</span><span class="sxs-lookup"><span data-stu-id="131a8-152">For a full list of the modules in Azure PowerShell, see the [Azure PowerShell modules list](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hosted on GitHub.</span></span>

## <a name="telemetry"></a><span data-ttu-id="131a8-153">遙測</span><span class="sxs-lookup"><span data-stu-id="131a8-153">Telemetry</span></span>

<span data-ttu-id="131a8-154">Azure PowerShell 預設為自動收集遙測資料。</span><span class="sxs-lookup"><span data-stu-id="131a8-154">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="131a8-155">Microsoft 彙總收集的資料，以識別使用模式、識別常見的問題，以及改善 Azure PowerShell 的體驗。</span><span class="sxs-lookup"><span data-stu-id="131a8-155">Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span> <span data-ttu-id="131a8-156">Microsoft Azure PowerShell 不會收集任何私人或個人資料。</span><span class="sxs-lookup"><span data-stu-id="131a8-156">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="131a8-157">若要停用資料收集，您必須執行 [AzDataCollection](/powershell/module/az.accounts/disable-azdatacollection)，以明確退出。</span><span class="sxs-lookup"><span data-stu-id="131a8-157">To disable data collection, you must explicitly opt out by executing [Disable-AzDataCollection](/powershell/module/az.accounts/disable-azdatacollection).</span></span>

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a><span data-ttu-id="131a8-158">透過快速入門和教學課程了解 Azure PowerShell 基本概念</span><span class="sxs-lookup"><span data-stu-id="131a8-158">Learn Azure PowerShell basics with quickstarts and tutorials</span></span>

<span data-ttu-id="131a8-159">若要開始使用 Azure PowerShell，請從深入的教學課程嘗試設定虛擬機器，並學習如何查詢這些虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="131a8-159">To get started with Azure PowerShell, try an in-depth tutorial for setting up virtual machines and learning how to query them.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="131a8-160">使用 Azure PowerShell 建立虛擬機器</span><span class="sxs-lookup"><span data-stu-id="131a8-160">Create virtual machines with Azure PowerShell</span></span>](azureps-vm-tutorial.yml)

<span data-ttu-id="131a8-161">另外還有其他熱門 Azure 服務的 Azure PowerShell 快速入門：</span><span class="sxs-lookup"><span data-stu-id="131a8-161">There are also Azure PowerShell quickstarts for other popular Azure services:</span></span>

* [<span data-ttu-id="131a8-162">建立儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="131a8-162">Create a storage account</span></span>](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [<span data-ttu-id="131a8-163"> 在 Azure Blob 儲存體之間傳送物件</span><span class="sxs-lookup"><span data-stu-id="131a8-163">Transfer objects to/from Azure Blob storage</span></span>](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [<span data-ttu-id="131a8-164">從 Azure Key Vault 建立及擷取祕密</span><span class="sxs-lookup"><span data-stu-id="131a8-164">Create and retrieve secrets from Azure Key Vault</span></span>](/azure/key-vault/quick-create-powershell)
* [<span data-ttu-id="131a8-165">建立 Azure SQL 資料庫和防火牆</span><span class="sxs-lookup"><span data-stu-id="131a8-165">Create an Azure SQL database and firewall</span></span>](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [<span data-ttu-id="131a8-166">在 Azure 容器執行個體中執行容器</span><span class="sxs-lookup"><span data-stu-id="131a8-166">Run a container in Azure Container Instances</span></span>](/azure/container-instances/container-instances-quickstart-powershell)
* [<span data-ttu-id="131a8-167">建立虛擬機器擴展集</span><span class="sxs-lookup"><span data-stu-id="131a8-167">Create a Virtual Machine Scale Set</span></span>](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [<span data-ttu-id="131a8-168">建立標準負載平衡器</span><span class="sxs-lookup"><span data-stu-id="131a8-168">Create a standard load balancer</span></span>](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a><span data-ttu-id="131a8-169">後續步驟</span><span class="sxs-lookup"><span data-stu-id="131a8-169">Next steps</span></span>

* [<span data-ttu-id="131a8-170">使用 Azure PowerShell 登入</span><span class="sxs-lookup"><span data-stu-id="131a8-170">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="131a8-171">使用 Azure PowerShell 來管理 Azure 訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="131a8-171">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="131a8-172">使用 Azure PowerShell 建立服務主體</span><span class="sxs-lookup"><span data-stu-id="131a8-172">Create service principals with Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="131a8-173">從社群獲得協助︰</span><span class="sxs-lookup"><span data-stu-id="131a8-173">Get help from the community:</span></span>
  * [<span data-ttu-id="131a8-174">MSDN 上的 Azure 論壇</span><span class="sxs-lookup"><span data-stu-id="131a8-174">Azure forum on MSDN</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="131a8-175">Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="131a8-175">Stack Overflow</span></span>](https://go.microsoft.com/fwlink/?LinkId=320213)
