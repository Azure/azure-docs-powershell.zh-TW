---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
ms.openlocfilehash: 8352f7a63e40986e27c4b521dca58aaf003679bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454600"
---
# <span data-ttu-id="e4389-101">New-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="e4389-101">New-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="e4389-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e4389-102">SYNOPSIS</span></span>
<span data-ttu-id="e4389-103">在 Azure 資料庫移轉服務中建立及啟動資料移轉工作。</span><span class="sxs-lookup"><span data-stu-id="e4389-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4389-104">句法</span><span class="sxs-lookup"><span data-stu-id="e4389-104">SYNTAX</span></span>

### <span data-ttu-id="e4389-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e4389-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e4389-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4389-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4389-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4389-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4389-108">說明</span><span class="sxs-lookup"><span data-stu-id="e4389-108">DESCRIPTION</span></span>
<span data-ttu-id="e4389-109">New-AzureRmDataMigrationTask Cmdlet 會建立資料移轉任務。</span><span class="sxs-lookup"><span data-stu-id="e4389-109">The New-AzureRmDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="e4389-110">這個 Cmdlet 採用任務類型枚舉器、Azure 資源群組、關聯 Azure 資料庫移轉服務的名稱和專案作為輸入的參數。</span><span class="sxs-lookup"><span data-stu-id="e4389-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Database Migration Service and Project as input.</span></span> 

## <span data-ttu-id="e4389-111">示例</span><span class="sxs-lookup"><span data-stu-id="e4389-111">EXAMPLES</span></span>

### <span data-ttu-id="e4389-112">範例1</span><span class="sxs-lookup"><span data-stu-id="e4389-112">Example 1</span></span>
```
PS C:\> New-AzureRmDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs
```

<span data-ttu-id="e4389-113">這個範例腳本示範如何在名為 [myDMSProject] 的專案或名為 [TestService] 的服務中，建立名為 MyMigrationTask 的新資料移轉任務。</span><span class="sxs-lookup"><span data-stu-id="e4389-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="e4389-114">參數</span><span class="sxs-lookup"><span data-stu-id="e4389-114">PARAMETERS</span></span>

### <span data-ttu-id="e4389-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4389-115">-DefaultProfile</span></span>
<span data-ttu-id="e4389-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e4389-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4389-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4389-117">-InputObject</span></span>
<span data-ttu-id="e4389-118">PSProject 物件。</span><span class="sxs-lookup"><span data-stu-id="e4389-118">PSProject Object.</span></span>

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

### <span data-ttu-id="e4389-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="e4389-119">-Name</span></span>
<span data-ttu-id="e4389-120">任務的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4389-120">The name of the task.</span></span>

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

### <span data-ttu-id="e4389-121">-專案名稱</span><span class="sxs-lookup"><span data-stu-id="e4389-121">-ProjectName</span></span>
<span data-ttu-id="e4389-122">專案名稱。</span><span class="sxs-lookup"><span data-stu-id="e4389-122">The name of the project.</span></span>

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

### <span data-ttu-id="e4389-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4389-123">-ResourceGroupName</span></span>
<span data-ttu-id="e4389-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4389-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="e4389-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4389-125">-ResourceId</span></span>
<span data-ttu-id="e4389-126">[專案資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="e4389-126">Project Resource Id.</span></span>

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

### <span data-ttu-id="e4389-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e4389-127">-ServiceName</span></span>
<span data-ttu-id="e4389-128">資料庫移轉服務名稱。</span><span class="sxs-lookup"><span data-stu-id="e4389-128">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="e4389-129">-TaskType</span><span class="sxs-lookup"><span data-stu-id="e4389-129">-TaskType</span></span>
<span data-ttu-id="e4389-130">任務類型。</span><span class="sxs-lookup"><span data-stu-id="e4389-130">Task Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4389-131">-確認</span><span class="sxs-lookup"><span data-stu-id="e4389-131">-Confirm</span></span>
<span data-ttu-id="e4389-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e4389-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4389-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4389-133">-WhatIf</span></span>
<span data-ttu-id="e4389-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e4389-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4389-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e4389-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4389-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4389-136">CommonParameters</span></span>
<span data-ttu-id="e4389-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e4389-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4389-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e4389-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4389-139">輸入</span><span class="sxs-lookup"><span data-stu-id="e4389-139">INPUTS</span></span>

### <span data-ttu-id="e4389-140">PSProject 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="e4389-140">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="e4389-141">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="e4389-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="e4389-142">System.object</span><span class="sxs-lookup"><span data-stu-id="e4389-142">System.String</span></span>

## <span data-ttu-id="e4389-143">輸出</span><span class="sxs-lookup"><span data-stu-id="e4389-143">OUTPUTS</span></span>

### <span data-ttu-id="e4389-144">PSProjectTask 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="e4389-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="e4389-145">筆記</span><span class="sxs-lookup"><span data-stu-id="e4389-145">NOTES</span></span>

## <span data-ttu-id="e4389-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="e4389-146">RELATED LINKS</span></span>
