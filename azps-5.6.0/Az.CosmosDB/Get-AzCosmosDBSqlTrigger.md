---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 28b616315913ae70722b5a600d4b10879c7b8334
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910741"
---
# <span data-ttu-id="1b001-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="1b001-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="1b001-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1b001-102">SYNOPSIS</span></span>
<span data-ttu-id="1b001-103">獲得一個一次 。。</span><span class="sxs-lookup"><span data-stu-id="1b001-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="1b001-104">語法</span><span class="sxs-lookup"><span data-stu-id="1b001-104">SYNTAX</span></span>

### <span data-ttu-id="1b001-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b001-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b001-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b001-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b001-107">描述</span><span class="sxs-lookup"><span data-stu-id="1b001-107">DESCRIPTION</span></span>
<span data-ttu-id="1b001-108">**Get-AzCosmosDBSqlTrigger Cmdlet** 會取得一個給定 ResourceGroupName、AccountName、DatabaseName 和 ContainerName 的所有現有一切現有一切系統管理 Sql Trigger 清單，並取得單一的一個 ResourceGroupName、AccountName、DatabaseName、ContainerName 和 TriggerName。</span><span class="sxs-lookup"><span data-stu-id="1b001-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="1b001-109">例子</span><span class="sxs-lookup"><span data-stu-id="1b001-109">EXAMPLES</span></span>

### <span data-ttu-id="1b001-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="1b001-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="1b001-111">參數</span><span class="sxs-lookup"><span data-stu-id="1b001-111">PARAMETERS</span></span>

### <span data-ttu-id="1b001-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1b001-112">-AccountName</span></span>
<span data-ttu-id="1b001-113">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b001-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1b001-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="1b001-114">-ContainerName</span></span>
<span data-ttu-id="1b001-115">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="1b001-115">Container name.</span></span>

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

### <span data-ttu-id="1b001-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1b001-116">-DatabaseName</span></span>
<span data-ttu-id="1b001-117">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="1b001-117">Database name.</span></span>

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

### <span data-ttu-id="1b001-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b001-118">-DefaultProfile</span></span>
<span data-ttu-id="1b001-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b001-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b001-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="1b001-120">-Name</span></span>
<span data-ttu-id="1b001-121">觸發名稱。</span><span class="sxs-lookup"><span data-stu-id="1b001-121">Trigger name.</span></span>

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

### <span data-ttu-id="1b001-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1b001-122">-ParentObject</span></span>
<span data-ttu-id="1b001-123">Sql Container 物件。</span><span class="sxs-lookup"><span data-stu-id="1b001-123">Sql Container object.</span></span>

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

### <span data-ttu-id="1b001-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b001-124">-ResourceGroupName</span></span>
<span data-ttu-id="1b001-125">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b001-125">Name of resource group.</span></span>

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

### <span data-ttu-id="1b001-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b001-126">CommonParameters</span></span>
<span data-ttu-id="1b001-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1b001-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b001-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b001-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b001-129">輸入</span><span class="sxs-lookup"><span data-stu-id="1b001-129">INPUTS</span></span>

### <span data-ttu-id="1b001-130">沒有</span><span class="sxs-lookup"><span data-stu-id="1b001-130">None</span></span>

## <span data-ttu-id="1b001-131">輸出</span><span class="sxs-lookup"><span data-stu-id="1b001-131">OUTPUTS</span></span>

### <span data-ttu-id="1b001-132">Microsoft.Azure.Commands.AzsDB.Models.PSSqlTrigetResults</span><span class="sxs-lookup"><span data-stu-id="1b001-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="1b001-133">筆記</span><span class="sxs-lookup"><span data-stu-id="1b001-133">NOTES</span></span>

## <span data-ttu-id="1b001-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b001-134">RELATED LINKS</span></span>
