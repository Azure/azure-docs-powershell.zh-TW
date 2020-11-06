---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Get-AzureRmDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
ms.openlocfilehash: caab43824c63e73e7011c0377d0bd7665befe5dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451199"
---
# <span data-ttu-id="9e3b3-101">Get-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="9e3b3-101">Get-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="9e3b3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9e3b3-102">SYNOPSIS</span></span>
<span data-ttu-id="9e3b3-103">檢索與 Azure Database 遷移服務遷移任務相關聯的 PSProjectTask 物件。</span><span class="sxs-lookup"><span data-stu-id="9e3b3-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e3b3-104">句法</span><span class="sxs-lookup"><span data-stu-id="9e3b3-104">SYNTAX</span></span>

### <span data-ttu-id="9e3b3-105">ListByComponent (預設) </span><span class="sxs-lookup"><span data-stu-id="9e3b3-105">ListByComponent (Default)</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e3b3-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="9e3b3-106">ListByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e3b3-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="9e3b3-107">GetByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e3b3-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="9e3b3-108">GetByInputObjectResultType</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e3b3-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="9e3b3-109">ListByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e3b3-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9e3b3-110">GetByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e3b3-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="9e3b3-111">GetByResourceIdResultType</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e3b3-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="9e3b3-112">GetByComponent</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e3b3-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="9e3b3-113">GetByComponentResultType</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e3b3-114">說明</span><span class="sxs-lookup"><span data-stu-id="9e3b3-114">DESCRIPTION</span></span>
<span data-ttu-id="9e3b3-115">Get-AzureRmDataMigrationTask Cmdlet 會檢索與 Azure Database 遷移服務遷移工作相關聯的屬性。</span><span class="sxs-lookup"><span data-stu-id="9e3b3-115">The Get-AzureRmDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="9e3b3-116">示例</span><span class="sxs-lookup"><span data-stu-id="9e3b3-116">EXAMPLES</span></span>

### <span data-ttu-id="9e3b3-117">範例1</span><span class="sxs-lookup"><span data-stu-id="9e3b3-117">Example 1</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="9e3b3-118">上述範例示範如何使用 Get-AzureRmDataMigrationTask Cmdlet，以根據以輸入參數傳入的任務名稱來檢索與 Azure Database 遷移服務遷移工作相關聯的屬性</span><span class="sxs-lookup"><span data-stu-id="9e3b3-118">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="9e3b3-119">範例2</span><span class="sxs-lookup"><span data-stu-id="9e3b3-119">Example 2</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -Project $myProject
```

<span data-ttu-id="9e3b3-120">上述範例示範如何使用 Get-AzureRmDataMigrationTask Cmdlet 來檢索與以輸入參數傳遞的 PSProject 物件相關的所有遷移工作</span><span class="sxs-lookup"><span data-stu-id="9e3b3-120">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="9e3b3-121">參數</span><span class="sxs-lookup"><span data-stu-id="9e3b3-121">PARAMETERS</span></span>

### <span data-ttu-id="9e3b3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e3b3-122">-DefaultProfile</span></span>
<span data-ttu-id="9e3b3-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9e3b3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e3b3-124">-展開</span><span class="sxs-lookup"><span data-stu-id="9e3b3-124">-Expand</span></span>
<span data-ttu-id="9e3b3-125">展開輸出</span><span class="sxs-lookup"><span data-stu-id="9e3b3-125">Expand output</span></span>

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

### <span data-ttu-id="9e3b3-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e3b3-126">-InputObject</span></span>
<span data-ttu-id="9e3b3-127">PSProject 物件。</span><span class="sxs-lookup"><span data-stu-id="9e3b3-127">PSProject Object.</span></span>

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

### <span data-ttu-id="9e3b3-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="9e3b3-128">-Name</span></span>
<span data-ttu-id="9e3b3-129">任務的名稱。</span><span class="sxs-lookup"><span data-stu-id="9e3b3-129">The name of the task.</span></span>

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

### <span data-ttu-id="9e3b3-130">-專案名稱</span><span class="sxs-lookup"><span data-stu-id="9e3b3-130">-ProjectName</span></span>
<span data-ttu-id="9e3b3-131">專案名稱。</span><span class="sxs-lookup"><span data-stu-id="9e3b3-131">The name of the project.</span></span>

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

### <span data-ttu-id="9e3b3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e3b3-132">-ResourceGroupName</span></span>
<span data-ttu-id="9e3b3-133">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9e3b3-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="9e3b3-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e3b3-134">-ResourceId</span></span>
<span data-ttu-id="9e3b3-135">[專案資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="9e3b3-135">Project Resource Id.</span></span>

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

### <span data-ttu-id="9e3b3-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="9e3b3-136">-ResultType</span></span>
<span data-ttu-id="9e3b3-137">展開指定結果類型的輸出。</span><span class="sxs-lookup"><span data-stu-id="9e3b3-137">Expand output of given result type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ResultTypeEnum
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:
Accepted values: MigrationLevelOutput, DatabaseLevelOutput, TableLevelOutput, MigrationValidationOutput, MigrationValidationDatabaseLevelOutput, LoginLevelOutput, AgentJobLevelOutput

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e3b3-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9e3b3-138">-ServiceName</span></span>
<span data-ttu-id="9e3b3-139">資料庫移轉服務名稱。</span><span class="sxs-lookup"><span data-stu-id="9e3b3-139">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="9e3b3-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="9e3b3-140">-TaskType</span></span>
<span data-ttu-id="9e3b3-141">依 TaskType 篩選。</span><span class="sxs-lookup"><span data-stu-id="9e3b3-141">Filter by TaskType.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum]
Parameter Sets: ListByComponent, ListByInputObject, ListByResourceId
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e3b3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e3b3-142">CommonParameters</span></span>
<span data-ttu-id="9e3b3-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9e3b3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e3b3-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9e3b3-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e3b3-145">輸入</span><span class="sxs-lookup"><span data-stu-id="9e3b3-145">INPUTS</span></span>

### <span data-ttu-id="9e3b3-146">PSProject 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="9e3b3-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="9e3b3-147">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="9e3b3-147">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="9e3b3-148">System.object</span><span class="sxs-lookup"><span data-stu-id="9e3b3-148">System.String</span></span>

## <span data-ttu-id="9e3b3-149">輸出</span><span class="sxs-lookup"><span data-stu-id="9e3b3-149">OUTPUTS</span></span>

### <span data-ttu-id="9e3b3-150">PSProjectTask 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="9e3b3-150">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="9e3b3-151">筆記</span><span class="sxs-lookup"><span data-stu-id="9e3b3-151">NOTES</span></span>

## <span data-ttu-id="9e3b3-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e3b3-152">RELATED LINKS</span></span>
