---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
ms.openlocfilehash: c40bd5761d7e0966e7d756a758f79bfb3592a2ad
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622473"
---
# <span data-ttu-id="c8029-101">New-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="c8029-101">New-AzDataMigrationTask</span></span>

## <span data-ttu-id="c8029-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c8029-102">SYNOPSIS</span></span>
<span data-ttu-id="c8029-103">在 Azure 資料庫移轉服務中建立及啟動資料移轉工作。</span><span class="sxs-lookup"><span data-stu-id="c8029-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

## <span data-ttu-id="c8029-104">句法</span><span class="sxs-lookup"><span data-stu-id="c8029-104">SYNTAX</span></span>

### <span data-ttu-id="c8029-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c8029-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8029-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8029-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8029-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8029-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8029-108">說明</span><span class="sxs-lookup"><span data-stu-id="c8029-108">DESCRIPTION</span></span>
<span data-ttu-id="c8029-109">New-AzDataMigrationTask Cmdlet 會建立資料移轉任務。</span><span class="sxs-lookup"><span data-stu-id="c8029-109">The New-AzDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="c8029-110">這個 Cmdlet 採用任務類型枚舉器、Azure 資源群組、關聯 Azure 資料庫移轉服務的名稱和專案作為輸入的參數。</span><span class="sxs-lookup"><span data-stu-id="c8029-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Database Migration Service and Project as input.</span></span> 

## <span data-ttu-id="c8029-111">示例</span><span class="sxs-lookup"><span data-stu-id="c8029-111">EXAMPLES</span></span>

### <span data-ttu-id="c8029-112">範例1</span><span class="sxs-lookup"><span data-stu-id="c8029-112">Example 1</span></span>
```
PS C:\> New-AzDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs -MigrationValidation $validationTask
```

<span data-ttu-id="c8029-113">這個範例腳本示範如何在名為 [myDMSProject] 的專案或名為 [TestService] 的服務中，建立名為 MyMigrationTask 的新資料移轉任務。</span><span class="sxs-lookup"><span data-stu-id="c8029-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="c8029-114">參數</span><span class="sxs-lookup"><span data-stu-id="c8029-114">PARAMETERS</span></span>

### <span data-ttu-id="c8029-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8029-115">-DefaultProfile</span></span>
<span data-ttu-id="c8029-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c8029-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8029-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8029-117">-InputObject</span></span>
<span data-ttu-id="c8029-118">PSProject 物件。</span><span class="sxs-lookup"><span data-stu-id="c8029-118">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8029-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="c8029-119">-Name</span></span>
<span data-ttu-id="c8029-120">任務的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8029-120">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8029-121">-專案名稱</span><span class="sxs-lookup"><span data-stu-id="c8029-121">-ProjectName</span></span>
<span data-ttu-id="c8029-122">專案名稱。</span><span class="sxs-lookup"><span data-stu-id="c8029-122">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8029-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8029-123">-ResourceGroupName</span></span>
<span data-ttu-id="c8029-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8029-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8029-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8029-125">-ResourceId</span></span>
<span data-ttu-id="c8029-126">[專案資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="c8029-126">Project Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8029-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c8029-127">-ServiceName</span></span>
<span data-ttu-id="c8029-128">資料庫移轉服務名稱。</span><span class="sxs-lookup"><span data-stu-id="c8029-128">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8029-129">-TaskType</span><span class="sxs-lookup"><span data-stu-id="c8029-129">-TaskType</span></span>
<span data-ttu-id="c8029-130">任務類型。</span><span class="sxs-lookup"><span data-stu-id="c8029-130">Task Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi, MigrateSqlServerSqlDbSync, ConnectToSourceSqlServerSync, ConnectToTargetSqlSync, GetUserTablesSqlSync, ValidateSqlServerSqlDbSync, ConnectToSourceMongoDb, ConnectToTargetMongoDb, MigrateMongoDb, ValidateMongoDbMigration, ConnectToTargetSqlDbMiSync, ValidateSqlServerSqlDbMiSync, MigrateSqlServerSqlDbMiSync

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8029-131">-MigrationValidation</span><span class="sxs-lookup"><span data-stu-id="c8029-131">-MigrationValidation</span></span> 
<span data-ttu-id="c8029-132">依驗證通話的任務回應物件，選用但建議使用。</span><span class="sxs-lookup"><span data-stu-id="c8029-132">Task response object by validation call, optional but recommended.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8029-133">-稍候</span><span class="sxs-lookup"><span data-stu-id="c8029-133">-Wait</span></span>
<span data-ttu-id="c8029-134">是否等待任務完成。</span><span class="sxs-lookup"><span data-stu-id="c8029-134">Whether to wait for task to finish.</span></span> <span data-ttu-id="c8029-135">如果已設定旗標，則會在工作完成後再檢查一秒，然後返回使用者可檢查輸出或錯誤的任務屬性。</span><span class="sxs-lookup"><span data-stu-id="c8029-135">If the flag is set, checks every one seconds till the task finishes and return to user the task properties where output or error can be inspected.</span></span> 
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8029-136">-確認</span><span class="sxs-lookup"><span data-stu-id="c8029-136">-Confirm</span></span>
<span data-ttu-id="c8029-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c8029-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8029-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8029-138">-WhatIf</span></span>
<span data-ttu-id="c8029-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c8029-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8029-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c8029-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8029-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8029-141">CommonParameters</span></span>
<span data-ttu-id="c8029-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c8029-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8029-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c8029-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8029-144">輸入</span><span class="sxs-lookup"><span data-stu-id="c8029-144">INPUTS</span></span>

### <span data-ttu-id="c8029-145">PSProject 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="c8029-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="c8029-146">System.object</span><span class="sxs-lookup"><span data-stu-id="c8029-146">System.String</span></span>

## <span data-ttu-id="c8029-147">輸出</span><span class="sxs-lookup"><span data-stu-id="c8029-147">OUTPUTS</span></span>

### <span data-ttu-id="c8029-148">PSProjectTask 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="c8029-148">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="c8029-149">筆記</span><span class="sxs-lookup"><span data-stu-id="c8029-149">NOTES</span></span>

## <span data-ttu-id="c8029-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8029-150">RELATED LINKS</span></span>
