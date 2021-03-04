---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
ms.openlocfilehash: 5e9e121e3210510ed073cacfe93d6ec196888db6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912022"
---
# <span data-ttu-id="af4fd-101">New-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="af4fd-101">New-AzDataMigrationTask</span></span>

## <span data-ttu-id="af4fd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="af4fd-102">SYNOPSIS</span></span>
<span data-ttu-id="af4fd-103">在 Azure 資料庫移移服務中建立及啟動資料移轉工作。</span><span class="sxs-lookup"><span data-stu-id="af4fd-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

## <span data-ttu-id="af4fd-104">語法</span><span class="sxs-lookup"><span data-stu-id="af4fd-104">SYNTAX</span></span>

### <span data-ttu-id="af4fd-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="af4fd-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af4fd-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af4fd-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af4fd-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="af4fd-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af4fd-108">描述</span><span class="sxs-lookup"><span data-stu-id="af4fd-108">DESCRIPTION</span></span>
<span data-ttu-id="af4fd-109">Cmdlet New-AzDataMigrationTask建立資料移轉工作。</span><span class="sxs-lookup"><span data-stu-id="af4fd-109">The New-AzDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="af4fd-110">此 Cmdlet 會採用任務類型列舉器、Azure 資源群組的參數、相關聯的 Azure 資料庫移轉服務名稱和 Project 做為輸入。</span><span class="sxs-lookup"><span data-stu-id="af4fd-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Database Migration Service and Project as input.</span></span> 

## <span data-ttu-id="af4fd-111">例子</span><span class="sxs-lookup"><span data-stu-id="af4fd-111">EXAMPLES</span></span>

### <span data-ttu-id="af4fd-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="af4fd-112">Example 1</span></span>
```
PS C:\> New-AzDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs -MigrationValidation $validationTask
```

<span data-ttu-id="af4fd-113">此範例腳本顯示如何在名為 MyDMSProject 和服務 TestService 的專案中，建立名為 MyMigrationTask 的新資料移轉工作。</span><span class="sxs-lookup"><span data-stu-id="af4fd-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="af4fd-114">參數</span><span class="sxs-lookup"><span data-stu-id="af4fd-114">PARAMETERS</span></span>

### <span data-ttu-id="af4fd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af4fd-115">-DefaultProfile</span></span>
<span data-ttu-id="af4fd-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="af4fd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af4fd-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af4fd-117">-InputObject</span></span>
<span data-ttu-id="af4fd-118">PSProject 物件。</span><span class="sxs-lookup"><span data-stu-id="af4fd-118">PSProject Object.</span></span>

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

### <span data-ttu-id="af4fd-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="af4fd-119">-Name</span></span>
<span data-ttu-id="af4fd-120">工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="af4fd-120">The name of the task.</span></span>

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

### <span data-ttu-id="af4fd-121">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="af4fd-121">-ProjectName</span></span>
<span data-ttu-id="af4fd-122">專案名稱。</span><span class="sxs-lookup"><span data-stu-id="af4fd-122">The name of the project.</span></span>

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

### <span data-ttu-id="af4fd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af4fd-123">-ResourceGroupName</span></span>
<span data-ttu-id="af4fd-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="af4fd-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="af4fd-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af4fd-125">-ResourceId</span></span>
<span data-ttu-id="af4fd-126">專案資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="af4fd-126">Project Resource Id.</span></span>

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

### <span data-ttu-id="af4fd-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="af4fd-127">-ServiceName</span></span>
<span data-ttu-id="af4fd-128">資料庫移移服務名稱。</span><span class="sxs-lookup"><span data-stu-id="af4fd-128">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="af4fd-129">-TaskType</span><span class="sxs-lookup"><span data-stu-id="af4fd-129">-TaskType</span></span>
<span data-ttu-id="af4fd-130">任務類型。</span><span class="sxs-lookup"><span data-stu-id="af4fd-130">Task Type.</span></span>

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

### <span data-ttu-id="af4fd-131">-MigrationValidation</span><span class="sxs-lookup"><span data-stu-id="af4fd-131">-MigrationValidation</span></span> 
<span data-ttu-id="af4fd-132">按驗證呼叫來回應工作物件，選擇性，但建議使用。</span><span class="sxs-lookup"><span data-stu-id="af4fd-132">Task response object by validation call, optional but recommended.</span></span>

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

### <span data-ttu-id="af4fd-133">-等待</span><span class="sxs-lookup"><span data-stu-id="af4fd-133">-Wait</span></span>
<span data-ttu-id="af4fd-134">是否要等待工作完成。</span><span class="sxs-lookup"><span data-stu-id="af4fd-134">Whether to wait for task to finish.</span></span> <span data-ttu-id="af4fd-135">如果已設定標號，請每隔一秒檢查一次，直到工作完成為止，並返回可檢查輸出或錯誤的工作屬性給使用者。</span><span class="sxs-lookup"><span data-stu-id="af4fd-135">If the flag is set, checks every one seconds till the task finishes and return to user the task properties where output or error can be inspected.</span></span> 
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

### <span data-ttu-id="af4fd-136">-確認</span><span class="sxs-lookup"><span data-stu-id="af4fd-136">-Confirm</span></span>
<span data-ttu-id="af4fd-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="af4fd-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af4fd-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af4fd-138">-WhatIf</span></span>
<span data-ttu-id="af4fd-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="af4fd-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af4fd-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="af4fd-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af4fd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af4fd-141">CommonParameters</span></span>
<span data-ttu-id="af4fd-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="af4fd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af4fd-143">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="af4fd-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af4fd-144">輸入</span><span class="sxs-lookup"><span data-stu-id="af4fd-144">INPUTS</span></span>

### <span data-ttu-id="af4fd-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="af4fd-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="af4fd-146">System.String</span><span class="sxs-lookup"><span data-stu-id="af4fd-146">System.String</span></span>

## <span data-ttu-id="af4fd-147">輸出</span><span class="sxs-lookup"><span data-stu-id="af4fd-147">OUTPUTS</span></span>

### <span data-ttu-id="af4fd-148">Microsoft.Azure.Commands.DataMigration.models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="af4fd-148">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="af4fd-149">筆記</span><span class="sxs-lookup"><span data-stu-id="af4fd-149">NOTES</span></span>

## <span data-ttu-id="af4fd-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="af4fd-150">RELATED LINKS</span></span>
