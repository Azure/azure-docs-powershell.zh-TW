---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
ms.openlocfilehash: 6df8d425967133e50dc45e44b6d567aca58465a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915550"
---
# <span data-ttu-id="1372a-101">Get-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="1372a-101">Get-AzCosmosDBAccount</span></span>

## <span data-ttu-id="1372a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1372a-102">SYNOPSIS</span></span>
<span data-ttu-id="1372a-103">取得部科斯DB 帳戶。</span><span class="sxs-lookup"><span data-stu-id="1372a-103">Get CosmosDB Account.</span></span>

## <span data-ttu-id="1372a-104">語法</span><span class="sxs-lookup"><span data-stu-id="1372a-104">SYNTAX</span></span>

### <span data-ttu-id="1372a-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1372a-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1372a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1372a-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1372a-107">描述</span><span class="sxs-lookup"><span data-stu-id="1372a-107">DESCRIPTION</span></span>
<span data-ttu-id="1372a-108">**Get-AzCosmosDBAccount** Cmdlet 會取得一個給定 ResourceGroupName 的所有現有一般管理帳戶清單，並取得一個針對給定 ResourceGroupName 和 AccountName 的單一一個一個管理中心帳戶。</span><span class="sxs-lookup"><span data-stu-id="1372a-108">The **Get-AzCosmosDBAccount** cmdlet gets the list of all existing CosmosDB accounts for a given ResourceGroupName and gets a single CosmosDB account for a given ResourceGroupName and AccountName.</span></span>

## <span data-ttu-id="1372a-109">例子</span><span class="sxs-lookup"><span data-stu-id="1372a-109">EXAMPLES</span></span>

### <span data-ttu-id="1372a-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="1372a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBAccount -ResourceGroupName {resourceGroupName} -Name {databaseAccountName}


Id                            : /subscriptions/{subscriptionid}/resourceGroups/{resourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{databaseAccountName}
Name                          : {databaseAccountName}
FailoverPolicies              : {databaseAccountName-region1}
ReadLocations                 : {databaseAccountName-region1}
WriteLocations                : {databaseAccountName-region1}
Capabilities                  : {}
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Models.ConsistencyPolicy
EnableAutomaticFailover       : False
IsVirtualNetworkFilterEnabled : False
IpRangeFilter                 :
DatabaseAccountOfferType      : Standard
DocumentEndpoint              : https://databaseAccountName.documents.azure.com:443/
ProvisioningState             : Succeeded
Kind                          : GlobalDocumentDB
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
NetworkAclBypass              : None
NetworkAclBypassResourceIds   : {}
```

<span data-ttu-id="1372a-111">取得在 ResourceGroup resourceGroupName 中名稱 databaseAccountName 的部下管理資料庫帳戶。</span><span class="sxs-lookup"><span data-stu-id="1372a-111">Get CosmosDB database account with name databaseAccountName in ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="1372a-112">參數</span><span class="sxs-lookup"><span data-stu-id="1372a-112">PARAMETERS</span></span>

### <span data-ttu-id="1372a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1372a-113">-DefaultProfile</span></span>
<span data-ttu-id="1372a-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1372a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1372a-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="1372a-115">-Name</span></span>
<span data-ttu-id="1372a-116">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="1372a-116">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1372a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1372a-117">-ResourceGroupName</span></span>
<span data-ttu-id="1372a-118">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1372a-118">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1372a-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1372a-119">-ResourceId</span></span>
<span data-ttu-id="1372a-120">資源的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="1372a-120">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1372a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1372a-121">CommonParameters</span></span>
<span data-ttu-id="1372a-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1372a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1372a-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1372a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1372a-124">輸入</span><span class="sxs-lookup"><span data-stu-id="1372a-124">INPUTS</span></span>

### <span data-ttu-id="1372a-125">沒有</span><span class="sxs-lookup"><span data-stu-id="1372a-125">None</span></span>

## <span data-ttu-id="1372a-126">輸出</span><span class="sxs-lookup"><span data-stu-id="1372a-126">OUTPUTS</span></span>

### <span data-ttu-id="1372a-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="1372a-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="1372a-128">筆記</span><span class="sxs-lookup"><span data-stu-id="1372a-128">NOTES</span></span>

## <span data-ttu-id="1372a-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="1372a-129">RELATED LINKS</span></span>
