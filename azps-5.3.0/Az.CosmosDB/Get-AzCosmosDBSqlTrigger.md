---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 10faa4b020633fdf46122c4864d50f00ef3ba54c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446128"
---
# <span data-ttu-id="75a86-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="75a86-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="75a86-102">摘要</span><span class="sxs-lookup"><span data-stu-id="75a86-102">SYNOPSIS</span></span>
<span data-ttu-id="75a86-103">取得 CosmosDB Sql 觸發程式。</span><span class="sxs-lookup"><span data-stu-id="75a86-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="75a86-104">句法</span><span class="sxs-lookup"><span data-stu-id="75a86-104">SYNTAX</span></span>

### <span data-ttu-id="75a86-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="75a86-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75a86-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75a86-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75a86-107">說明</span><span class="sxs-lookup"><span data-stu-id="75a86-107">DESCRIPTION</span></span>
<span data-ttu-id="75a86-108">**AzCosmosDBSqlTrigger** Cmdlet 會取得特定 ResourceGroupName、Accountname、databasename 與的所有現有 CosmosDB sql 觸發器清單，並取得特定 ResourceGroupName、Accountname、databasename、和 TriggerName 的單一 CosmosDB sql 觸發程式。</span><span class="sxs-lookup"><span data-stu-id="75a86-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="75a86-109">示例</span><span class="sxs-lookup"><span data-stu-id="75a86-109">EXAMPLES</span></span>

### <span data-ttu-id="75a86-110">範例1</span><span class="sxs-lookup"><span data-stu-id="75a86-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="75a86-111">參數</span><span class="sxs-lookup"><span data-stu-id="75a86-111">PARAMETERS</span></span>

### <span data-ttu-id="75a86-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="75a86-112">-AccountName</span></span>
<span data-ttu-id="75a86-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="75a86-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="75a86-114">-容器</span><span class="sxs-lookup"><span data-stu-id="75a86-114">-ContainerName</span></span>
<span data-ttu-id="75a86-115">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="75a86-115">Container name.</span></span>

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

### <span data-ttu-id="75a86-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="75a86-116">-DatabaseName</span></span>
<span data-ttu-id="75a86-117">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="75a86-117">Database name.</span></span>

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

### <span data-ttu-id="75a86-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75a86-118">-DefaultProfile</span></span>
<span data-ttu-id="75a86-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="75a86-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75a86-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="75a86-120">-Name</span></span>
<span data-ttu-id="75a86-121">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="75a86-121">Trigger name.</span></span>

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

### <span data-ttu-id="75a86-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="75a86-122">-ParentObject</span></span>
<span data-ttu-id="75a86-123">Sql 容器物件。</span><span class="sxs-lookup"><span data-stu-id="75a86-123">Sql Container object.</span></span>

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

### <span data-ttu-id="75a86-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75a86-124">-ResourceGroupName</span></span>
<span data-ttu-id="75a86-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="75a86-125">Name of resource group.</span></span>

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

### <span data-ttu-id="75a86-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75a86-126">CommonParameters</span></span>
<span data-ttu-id="75a86-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="75a86-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75a86-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="75a86-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75a86-129">輸入</span><span class="sxs-lookup"><span data-stu-id="75a86-129">INPUTS</span></span>

### <span data-ttu-id="75a86-130">所有</span><span class="sxs-lookup"><span data-stu-id="75a86-130">None</span></span>

## <span data-ttu-id="75a86-131">輸出</span><span class="sxs-lookup"><span data-stu-id="75a86-131">OUTPUTS</span></span>

### <span data-ttu-id="75a86-132">PSSqlTriggerGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="75a86-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="75a86-133">筆記</span><span class="sxs-lookup"><span data-stu-id="75a86-133">NOTES</span></span>

## <span data-ttu-id="75a86-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="75a86-134">RELATED LINKS</span></span>
