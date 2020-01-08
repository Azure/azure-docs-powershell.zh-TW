---
title: 開始使用 Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 01/14/2019
ms.openlocfilehash: c515fcbbe4dcb0b6578a56da137a77e3f843a2e6
ms.sourcegitcommit: 2d0c3ffaa5246f680784fa7e15b0d2536c27ff80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2020
ms.locfileid: "75722035"
---
# <a name="get-started-with-azure-powershell"></a>開始使用 Azure PowerShell

Azure PowerShell 的設計訴求是從命令列管理 Azure 資源。 當您想要建置使用 Azure Resource Manager 模型的自動化工具時，就可以使用 Azure PowerShell。
您可以在瀏覽器中嘗試將其與 [Azure Cloud Shell](/azure/cloud-shell/overview) 搭配使用，或是將其安裝在本機電腦上。

本文可協助您開始使用 Azure PowerShell，並讓您知道其背後的核心概念。

## <a name="install-or-run-in-azure-cloud-shell"></a>在 Azure Cloud Shell 中安裝或執行

開始使用 Azure PowerShell 最簡單的方式是在 Azure Cloud Shell 環境中試用。
若要啟動並執行 Cloud Shell，請參閱 [Azure Cloud Shell 中的 PowerShell 快速入門](/azure/cloud-shell/quickstart-powershell)。
Cloud Shell 會在 Linux 容器上執行 PowerShell 6，因此無法使用 Windows 特有的功能。

當您準備好在本機電腦上安裝 Azure PowerShell 時，請遵循[安裝 Azure PowerShell 模組](install-az-ps.md)中的指示。

## <a name="sign-in-to-azure"></a>登入 Azure

使用 `Connect-AzAccount` Cmdlet 以互動方式登入。 如果您使用 Cloud Shell，請略過此步驟：您的 Azure Cloud Shell 工作階段已向啟動 Cloud Shell 工作階段的環境、訂用帳戶及租用戶完成驗證。

```azurepowershell-interactive
Connect-AzAccount
```

如果您不是位於美國區域，請使用 `-Environment` 參數來登入。 請使用 [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) Cmdlet 取得您區域的環境名稱。 例如，若要登入 Azure China 21Vianet：

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

您會在 PowerShell 5.1 環境中看到登入對話方塊，請提供您 Azure 帳戶的使用者名稱和密碼。 若使用其他版本的 PowerShell，則您會在 [https://microsoft.com/devicelogin ] 中取得要使用的權杖。
在瀏覽器中開啟此頁面並輸入權杖，使用 Azure 帳戶認證來登入，然後授權 Azure PowerShell。

登入之後，您會看到指出哪一個 Azure 訂用帳戶為作用中的資訊。 如果您的帳戶中有多個 Azure 訂用帳戶，且想要選取不同訂用帳戶，請使用 [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) 取得可用的訂用帳戶，並透過訂用帳戶識別碼使用 [Set-AzContext](/powershell/module/az.accounts/set-azcontext) Cmdlet。
如需管理 Azure PowerShell 中的 Azure 訂用帳戶詳細資訊，請參閱[使用多個 Azure 訂用帳戶](manage-subscriptions-azureps.md)。

登入後，您可以使用 Azure PowerShell Cmdlet 來存取和管理訂用帳戶中的資源。 若要深入了解登入程序和驗證方法，請參閱[使用 Azure PowerShell 登入](authenticate-azureps.md)。

## <a name="find-commands"></a>尋找命令

Azure PowerShell Cmdlet 會遵循 PowerShell 的標準命名慣例：`VERB-NOUN`。 動詞描述動作 (例如 `New`、`Get`、`Set`、`Remove`)，而名詞描述資源類型 (例如 `AzVM`、`AzKeyVaultCertificate`、`AzFirewall`、`AzVirtualNetworkGateway`)。 Azure PowerShell 中的名詞一律具有前置詞：`Az`。 如需標準動詞命令的完整清單，請參閱 [PowerShell 命令的已核准動詞](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands)。

了解可用的名詞、動詞和 Azure PowerShell 模組可協助您透過 [Get-Command](/powershell/module/microsoft.powershell.core/get-command) Cmdlet 來尋找命令。 例如，若要尋找使用 `Get` 動詞的所有 VM 相關命令：

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

為協助您尋找常見的命令，此資料表列出可與 `Get-Command` 搭配的資源類型、對應 Azure PowerShell 模組和名詞前置詞：

| 資源類型 | Azure PowerShell 模組 | 名詞前置詞 |
|---------------|-------------------------|----------------|
| [資源群組](/azure/azure-resource-manager/resource-group-overview) | [Az.Resources](/powershell/module/az.resources#resources) | `AzResourceGroup` |
| [虛擬機器](/azure/virtual-machines) | [Az.Compute](/powershell/module/az.compute#virtual_machines) | `AzVM` |
| [儲存體帳戶](/azure/storage/common/storage-introduction) | [Az.Storage](/powershell/module/az.storage/) | `AzStorageAccount` |
| [金鑰保存庫](/azure/key-vault/key-vault-whatis) | [Az.KeyVault](/powershell/module/az.keyvault) | `AzKeyVault` |
| [Web 應用程式](/azure/app-service) | [Az.Websites](/powershell/module/az.websites) | `AzWebApp` |
| [SQL 資料庫](/azure/sql-database) | [Az.Sql](/powershell/module/az.sql) | `AzSqlDatabase` |

如需 Azure PowerShell 中的完整模組清單，請參閱裝載於 GitHub 上的 [Azure PowerShell 模組清單](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md)。

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a>透過快速入門和教學課程了解 Azure PowerShell 基本概念

若要開始使用 Azure PowerShell，請從深入的教學課程嘗試設定虛擬機器，並學習如何查詢這些虛擬機器。

> [!div class="nextstepaction"]
> [使用 Azure PowerShell 建立虛擬機器](azureps-vm-tutorial.yml)

另外還有其他熱門 Azure 服務的 Azure PowerShell 快速入門：

* [建立儲存體帳戶](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [ 在 Azure Blob 儲存體之間傳送物件](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [從 Azure Key Vault 建立及擷取祕密](/azure/key-vault/quick-create-powershell)
* [建立 Azure SQL 資料庫和防火牆](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [在 Azure 容器執行個體中執行容器](/azure/container-instances/container-instances-quickstart-powershell)
* [建立虛擬機器擴展集 (VMSS)](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [建立標準負載平衡器](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a>後續步驟

* [使用 Azure PowerShell 登入](authenticate-azureps.md)
* [使用 Azure PowerShell 來管理 Azure 訂用帳戶](manage-subscriptions-azureps.md)
* [使用 Azure PowerShell 建立服務主體](create-azure-service-principal-azureps.md)
* 從社群獲得協助︰
  * [MSDN 上的 Azure 論壇](https://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [Stack Overflow](https://go.microsoft.com/fwlink/?LinkId=320213)
