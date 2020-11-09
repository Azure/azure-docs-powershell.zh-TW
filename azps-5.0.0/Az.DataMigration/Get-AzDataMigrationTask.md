---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
ms.openlocfilehash: bcc1c39af722d5f12c333152e8458228f583a842
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284966"
---
# <span data-ttu-id="2edea-101">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="2edea-101">Get-AzDataMigrationTask</span></span>

## <span data-ttu-id="2edea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2edea-102">SYNOPSIS</span></span>
<span data-ttu-id="2edea-103">檢索與 Azure Database 遷移服務遷移任務相關聯的 PSProjectTask 物件。</span><span class="sxs-lookup"><span data-stu-id="2edea-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="2edea-104">句法</span><span class="sxs-lookup"><span data-stu-id="2edea-104">SYNTAX</span></span>

### <span data-ttu-id="2edea-105">ListByComponent (預設) </span><span class="sxs-lookup"><span data-stu-id="2edea-105">ListByComponent (Default)</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2edea-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="2edea-106">ListByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2edea-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="2edea-107">GetByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2edea-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="2edea-108">GetByInputObjectResultType</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2edea-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="2edea-109">ListByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2edea-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2edea-110">GetByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2edea-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="2edea-111">GetByResourceIdResultType</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2edea-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="2edea-112">GetByComponent</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2edea-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="2edea-113">GetByComponentResultType</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2edea-114">說明</span><span class="sxs-lookup"><span data-stu-id="2edea-114">DESCRIPTION</span></span>
<span data-ttu-id="2edea-115">Get-AzDataMigrationTask Cmdlet 會檢索與 Azure Database 遷移服務遷移工作相關聯的屬性。</span><span class="sxs-lookup"><span data-stu-id="2edea-115">The Get-AzDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="2edea-116">示例</span><span class="sxs-lookup"><span data-stu-id="2edea-116">EXAMPLES</span></span>

### <span data-ttu-id="2edea-117">範例1</span><span class="sxs-lookup"><span data-stu-id="2edea-117">Example 1</span></span>
```
PS C:\> Get -AzDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="2edea-118">上述範例示範如何使用 Get-AzDataMigrationTask Cmdlet，以根據以輸入參數傳入的任務名稱來檢索與 Azure Database 遷移服務遷移工作相關聯的屬性</span><span class="sxs-lookup"><span data-stu-id="2edea-118">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="2edea-119">範例2</span><span class="sxs-lookup"><span data-stu-id="2edea-119">Example 2</span></span>
```
PS C:\> Get -AzDataMigrationTask -Project $myProject
```

<span data-ttu-id="2edea-120">上述範例示範如何使用 Get-AzDataMigrationTask Cmdlet 來檢索與以輸入參數傳遞的 PSProject 物件相關的所有遷移工作</span><span class="sxs-lookup"><span data-stu-id="2edea-120">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="2edea-121">參數</span><span class="sxs-lookup"><span data-stu-id="2edea-121">PARAMETERS</span></span>

### <span data-ttu-id="2edea-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2edea-122">-DefaultProfile</span></span>
<span data-ttu-id="2edea-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2edea-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2edea-124">-展開</span><span class="sxs-lookup"><span data-stu-id="2edea-124">-Expand</span></span>
<span data-ttu-id="2edea-125">展開輸出</span><span class="sxs-lookup"><span data-stu-id="2edea-125">Expand output</span></span>

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

### <span data-ttu-id="2edea-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2edea-126">-InputObject</span></span>
<span data-ttu-id="2edea-127">PSProject 物件。</span><span class="sxs-lookup"><span data-stu-id="2edea-127">PSProject Object.</span></span>

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

### <span data-ttu-id="2edea-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="2edea-128">-Name</span></span>
<span data-ttu-id="2edea-129">任務的名稱。</span><span class="sxs-lookup"><span data-stu-id="2edea-129">The name of the task.</span></span>

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

### <span data-ttu-id="2edea-130">-專案名稱</span><span class="sxs-lookup"><span data-stu-id="2edea-130">-ProjectName</span></span>
<span data-ttu-id="2edea-131">專案名稱。</span><span class="sxs-lookup"><span data-stu-id="2edea-131">The name of the project.</span></span>

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

### <span data-ttu-id="2edea-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2edea-132">-ResourceGroupName</span></span>
<span data-ttu-id="2edea-133">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2edea-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="2edea-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2edea-134">-ResourceId</span></span>
<span data-ttu-id="2edea-135">[專案資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="2edea-135">Project Resource Id.</span></span>

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

### <span data-ttu-id="2edea-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="2edea-136">-ResultType</span></span>
<span data-ttu-id="2edea-137">展開指定結果類型的輸出。</span><span class="sxs-lookup"><span data-stu-id="2edea-137">Expand output of given result type.</span></span>

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

### <span data-ttu-id="2edea-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2edea-138">-ServiceName</span></span>
<span data-ttu-id="2edea-139">資料庫移轉服務名稱。</span><span class="sxs-lookup"><span data-stu-id="2edea-139">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="2edea-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="2edea-140">-TaskType</span></span>
<span data-ttu-id="2edea-141">依 TaskType 篩選。</span><span class="sxs-lookup"><span data-stu-id="2edea-141">Filter by TaskType.</span></span>

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

### <span data-ttu-id="2edea-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2edea-142">CommonParameters</span></span>
<span data-ttu-id="2edea-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2edea-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2edea-144">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2edea-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2edea-145">輸入</span><span class="sxs-lookup"><span data-stu-id="2edea-145">INPUTS</span></span>

### <span data-ttu-id="2edea-146">PSProject 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="2edea-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="2edea-147">System.object</span><span class="sxs-lookup"><span data-stu-id="2edea-147">System.String</span></span>

## <span data-ttu-id="2edea-148">輸出</span><span class="sxs-lookup"><span data-stu-id="2edea-148">OUTPUTS</span></span>

### <span data-ttu-id="2edea-149">PSProjectTask 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="2edea-149">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="2edea-150">筆記</span><span class="sxs-lookup"><span data-stu-id="2edea-150">NOTES</span></span>

## <span data-ttu-id="2edea-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="2edea-151">RELATED LINKS</span></span>
