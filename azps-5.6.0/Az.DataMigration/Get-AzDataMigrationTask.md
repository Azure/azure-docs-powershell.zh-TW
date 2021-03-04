---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Get-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
ms.openlocfilehash: 08f87d40eec10f10b12f568cae8e899f5b7468d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905110"
---
# <span data-ttu-id="a5328-101">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="a5328-101">Get-AzDataMigrationTask</span></span>

## <span data-ttu-id="a5328-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a5328-102">SYNOPSIS</span></span>
<span data-ttu-id="a5328-103">會取回與 Azure 資料庫移移服務移移工作相關聯的 PSProjectTask 物件。</span><span class="sxs-lookup"><span data-stu-id="a5328-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="a5328-104">語法</span><span class="sxs-lookup"><span data-stu-id="a5328-104">SYNTAX</span></span>

### <span data-ttu-id="a5328-105">ListByComponent (預設) </span><span class="sxs-lookup"><span data-stu-id="a5328-105">ListByComponent (Default)</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5328-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="a5328-106">ListByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5328-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="a5328-107">GetByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5328-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="a5328-108">GetByInputObjectResultType</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5328-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="a5328-109">ListByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5328-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a5328-110">GetByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5328-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="a5328-111">GetByResourceIdResultType</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5328-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="a5328-112">GetByComponent</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5328-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="a5328-113">GetByComponentResultType</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5328-114">描述</span><span class="sxs-lookup"><span data-stu-id="a5328-114">DESCRIPTION</span></span>
<span data-ttu-id="a5328-115">此Get-AzDataMigrationTask Cmdlet 會取回與 Azure 資料庫移轉服務移轉工作關聯的屬性。</span><span class="sxs-lookup"><span data-stu-id="a5328-115">The Get-AzDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="a5328-116">例子</span><span class="sxs-lookup"><span data-stu-id="a5328-116">EXAMPLES</span></span>

### <span data-ttu-id="a5328-117">範例 1</span><span class="sxs-lookup"><span data-stu-id="a5328-117">Example 1</span></span>
```
PS C:\> Get -AzDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="a5328-118">上述範例說明使用 Get-AzDataMigrationTask Cmdlet 根據以輸入參數傳遞的工作名稱，來取回與 Azure 資料庫移轉服務移轉工作關聯的屬性</span><span class="sxs-lookup"><span data-stu-id="a5328-118">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="a5328-119">範例 2</span><span class="sxs-lookup"><span data-stu-id="a5328-119">Example 2</span></span>
```
PS C:\> Get -AzDataMigrationTask -Project $myProject
```

<span data-ttu-id="a5328-120">上述範例說明如何使用 Get-AzDataMigrationTask Cmdlet 來取回以輸入參數傳遞之 PSProject 物件相關的所有移轉工作</span><span class="sxs-lookup"><span data-stu-id="a5328-120">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="a5328-121">參數</span><span class="sxs-lookup"><span data-stu-id="a5328-121">PARAMETERS</span></span>

### <span data-ttu-id="a5328-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5328-122">-DefaultProfile</span></span>
<span data-ttu-id="a5328-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a5328-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5328-124">-展開</span><span class="sxs-lookup"><span data-stu-id="a5328-124">-Expand</span></span>
<span data-ttu-id="a5328-125">展開輸出</span><span class="sxs-lookup"><span data-stu-id="a5328-125">Expand output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByInputObject, GetByResourceId, GetByComponent
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5328-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5328-126">-InputObject</span></span>
<span data-ttu-id="a5328-127">PSProject 物件。</span><span class="sxs-lookup"><span data-stu-id="a5328-127">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ListByInputObject
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: GetByInputObject, GetByInputObjectResultType
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5328-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="a5328-128">-Name</span></span>
<span data-ttu-id="a5328-129">工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5328-129">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByInputObject, GetByInputObjectResultType, GetByResourceId, GetByResourceIdResultType, GetByComponentResultType
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByComponent
Aliases: TaskName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5328-130">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="a5328-130">-ProjectName</span></span>
<span data-ttu-id="a5328-131">專案名稱。</span><span class="sxs-lookup"><span data-stu-id="a5328-131">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5328-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5328-132">-ResourceGroupName</span></span>
<span data-ttu-id="a5328-133">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5328-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5328-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5328-134">-ResourceId</span></span>
<span data-ttu-id="a5328-135">專案資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a5328-135">Project Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceId, GetByResourceIdResultType
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5328-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="a5328-136">-ResultType</span></span>
<span data-ttu-id="a5328-137">展開給定結果類型的輸出。</span><span class="sxs-lookup"><span data-stu-id="a5328-137">Expand output of given result type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ResultTypeEnum
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:
Accepted values: MigrationLevelOutput, DatabaseLevelOutput, TableLevelOutput, MigrationValidationOutput, MigrationValidationDatabaseLevelOutput, LoginLevelOutput, AgentJobLevelOutput, Command

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5328-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a5328-138">-ServiceName</span></span>
<span data-ttu-id="a5328-139">資料庫移移服務名稱。</span><span class="sxs-lookup"><span data-stu-id="a5328-139">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5328-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="a5328-140">-TaskType</span></span>
<span data-ttu-id="a5328-141">根據 TaskType 篩選。</span><span class="sxs-lookup"><span data-stu-id="a5328-141">Filter by TaskType.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum]
Parameter Sets: ListByComponent, ListByInputObject, ListByResourceId
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi, MigrateSqlServerSqlDbSync, ConnectToSourceSqlServerSync, ConnectToTargetSqlSync, GetUserTablesSqlSync, ValidateSqlServerSqlDbSync

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5328-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5328-142">CommonParameters</span></span>
<span data-ttu-id="a5328-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a5328-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5328-144">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a5328-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5328-145">輸入</span><span class="sxs-lookup"><span data-stu-id="a5328-145">INPUTS</span></span>

### <span data-ttu-id="a5328-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="a5328-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="a5328-147">System.String</span><span class="sxs-lookup"><span data-stu-id="a5328-147">System.String</span></span>

## <span data-ttu-id="a5328-148">輸出</span><span class="sxs-lookup"><span data-stu-id="a5328-148">OUTPUTS</span></span>

### <span data-ttu-id="a5328-149">Microsoft.Azure.Commands.DataMigration.models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="a5328-149">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="a5328-150">筆記</span><span class="sxs-lookup"><span data-stu-id="a5328-150">NOTES</span></span>

## <span data-ttu-id="a5328-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5328-151">RELATED LINKS</span></span>
