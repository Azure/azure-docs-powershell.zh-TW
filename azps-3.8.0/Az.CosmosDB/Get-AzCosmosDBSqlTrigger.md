---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 6631cad83260a935f2849391941ec0cf6514b188
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956502"
---
# <span data-ttu-id="128ff-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="128ff-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="128ff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="128ff-102">SYNOPSIS</span></span>
<span data-ttu-id="128ff-103">取得 CosmosDB Sql 觸發程式。</span><span class="sxs-lookup"><span data-stu-id="128ff-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="128ff-104">句法</span><span class="sxs-lookup"><span data-stu-id="128ff-104">SYNTAX</span></span>

### <span data-ttu-id="128ff-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="128ff-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="128ff-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="128ff-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="128ff-107">說明</span><span class="sxs-lookup"><span data-stu-id="128ff-107">DESCRIPTION</span></span>
<span data-ttu-id="128ff-108">**AzCosmosDBSqlTrigger** Cmdlet 會取得特定 ResourceGroupName、Accountname、databasename 與的所有現有 CosmosDB sql 觸發器清單，並取得特定 ResourceGroupName、Accountname、databasename、和 TriggerName 的單一 CosmosDB sql 觸發程式。</span><span class="sxs-lookup"><span data-stu-id="128ff-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="128ff-109">示例</span><span class="sxs-lookup"><span data-stu-id="128ff-109">EXAMPLES</span></span>

### <span data-ttu-id="128ff-110">範例1</span><span class="sxs-lookup"><span data-stu-id="128ff-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="128ff-111">參數</span><span class="sxs-lookup"><span data-stu-id="128ff-111">PARAMETERS</span></span>

### <span data-ttu-id="128ff-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="128ff-112">-AccountName</span></span>
<span data-ttu-id="128ff-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="128ff-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="128ff-114">-容器</span><span class="sxs-lookup"><span data-stu-id="128ff-114">-ContainerName</span></span>
<span data-ttu-id="128ff-115">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="128ff-115">Container name.</span></span>

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

### <span data-ttu-id="128ff-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="128ff-116">-DatabaseName</span></span>
<span data-ttu-id="128ff-117">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="128ff-117">Database name.</span></span>

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

### <span data-ttu-id="128ff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="128ff-118">-DefaultProfile</span></span>
<span data-ttu-id="128ff-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="128ff-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="128ff-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="128ff-120">-InputObject</span></span>
<span data-ttu-id="128ff-121">Sql 容器物件。</span><span class="sxs-lookup"><span data-stu-id="128ff-121">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="128ff-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="128ff-122">-Name</span></span>
<span data-ttu-id="128ff-123">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="128ff-123">Trigger name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="128ff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="128ff-124">-ResourceGroupName</span></span>
<span data-ttu-id="128ff-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="128ff-125">Name of resource group.</span></span>

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

### <span data-ttu-id="128ff-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="128ff-126">CommonParameters</span></span>
<span data-ttu-id="128ff-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="128ff-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="128ff-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="128ff-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="128ff-129">輸入</span><span class="sxs-lookup"><span data-stu-id="128ff-129">INPUTS</span></span>

### <span data-ttu-id="128ff-130">所有</span><span class="sxs-lookup"><span data-stu-id="128ff-130">None</span></span>

## <span data-ttu-id="128ff-131">輸出</span><span class="sxs-lookup"><span data-stu-id="128ff-131">OUTPUTS</span></span>

### <span data-ttu-id="128ff-132">PSSqlTriggerGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="128ff-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="128ff-133">筆記</span><span class="sxs-lookup"><span data-stu-id="128ff-133">NOTES</span></span>

## <span data-ttu-id="128ff-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="128ff-134">RELATED LINKS</span></span>
