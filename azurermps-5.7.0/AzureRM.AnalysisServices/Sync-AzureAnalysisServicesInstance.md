---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/sync-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: f3fb2377fd78db4b330afd39a8691f958597f07a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447101"
---
# <span data-ttu-id="11b4b-101">Sync-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="11b4b-101">Sync-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="11b4b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11b4b-102">SYNOPSIS</span></span>

<span data-ttu-id="11b4b-103">將指定的 Analysis Services 伺服器實例上的指定資料庫同步處理到目前登入的 scaleout 中的所有查詢實例，如 Add-AzureAnalysisServicesAccount 命令中所指定</span><span class="sxs-lookup"><span data-stu-id="11b4b-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11b4b-104">句法</span><span class="sxs-lookup"><span data-stu-id="11b4b-104">SYNTAX</span></span>

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-Passthru]
```

## <span data-ttu-id="11b4b-105">說明</span><span class="sxs-lookup"><span data-stu-id="11b4b-105">DESCRIPTION</span></span>

<span data-ttu-id="11b4b-106">Sync-AzureAnalysisServicesInstance Cmdlet 會將指定的 Analysis Services 伺服器實例上的指定資料庫同步處理到目前已登入的 [Add-AzureAnalysisServicesAccount] 命令中指定的所有查詢 scaleout 實例</span><span class="sxs-lookup"><span data-stu-id="11b4b-106">The Sync-AzureAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="11b4b-107">示例</span><span class="sxs-lookup"><span data-stu-id="11b4b-107">EXAMPLES</span></span>

### <span data-ttu-id="11b4b-108">範例1</span><span class="sxs-lookup"><span data-stu-id="11b4b-108">Example 1</span></span>

```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="11b4b-109">這個命令會在環境 westus.asazure.windows.net 中，同步處理名為「contoso」的伺服器中名為 SalesOrders 的資料庫，前提是使用者已使用 Add-AzureAnalysisServicesAccount 命令登入此環境。</span><span class="sxs-lookup"><span data-stu-id="11b4b-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this enviroment using Add-AzureAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="11b4b-110">參數</span><span class="sxs-lookup"><span data-stu-id="11b4b-110">PARAMETERS</span></span>

### <span data-ttu-id="11b4b-111">-實例</span><span class="sxs-lookup"><span data-stu-id="11b4b-111">-Instance</span></span>

<span data-ttu-id="11b4b-112">要重新開機之 Analysis Services 伺服器實例的名稱</span><span class="sxs-lookup"><span data-stu-id="11b4b-112">Name of the Analysis Services server instance to restart</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11b4b-113">-資料庫</span><span class="sxs-lookup"><span data-stu-id="11b4b-113">-Database</span></span>

<span data-ttu-id="11b4b-114">要同步處理的資料庫身分識別</span><span class="sxs-lookup"><span data-stu-id="11b4b-114">Identity of the database to be synchronized</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11b4b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11b4b-115">-PassThru</span></span>

<span data-ttu-id="11b4b-116">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="11b4b-116">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: Switch
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="11b4b-117">輸入</span><span class="sxs-lookup"><span data-stu-id="11b4b-117">INPUTS</span></span>

### <span data-ttu-id="11b4b-118">所有</span><span class="sxs-lookup"><span data-stu-id="11b4b-118">None</span></span>
<span data-ttu-id="11b4b-119">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="11b4b-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="11b4b-120">輸出</span><span class="sxs-lookup"><span data-stu-id="11b4b-120">OUTPUTS</span></span>

### <span data-ttu-id="11b4b-121">System.object</span><span class="sxs-lookup"><span data-stu-id="11b4b-121">System.Boolean</span></span>

## <span data-ttu-id="11b4b-122">筆記</span><span class="sxs-lookup"><span data-stu-id="11b4b-122">NOTES</span></span>

<span data-ttu-id="11b4b-123">別名： Sync-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="11b4b-123">Alias: Sync-AzureAsInstance</span></span>

## <span data-ttu-id="11b4b-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="11b4b-124">RELATED LINKS</span></span>
