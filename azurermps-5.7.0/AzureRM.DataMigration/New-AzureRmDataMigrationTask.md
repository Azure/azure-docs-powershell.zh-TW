---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
ms.openlocfilehash: 1bdf66311acd1b8ff1de43b5ea199d5d0a17c394
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624095"
---
# <span data-ttu-id="28ba2-101">New-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="28ba2-101">New-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="28ba2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="28ba2-102">SYNOPSIS</span></span>
<span data-ttu-id="28ba2-103">在 Azure 資料庫移轉服務中建立及啟動資料移轉工作。</span><span class="sxs-lookup"><span data-stu-id="28ba2-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28ba2-104">句法</span><span class="sxs-lookup"><span data-stu-id="28ba2-104">SYNTAX</span></span>

### <span data-ttu-id="28ba2-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="28ba2-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="28ba2-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28ba2-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="28ba2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28ba2-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="28ba2-108">說明</span><span class="sxs-lookup"><span data-stu-id="28ba2-108">DESCRIPTION</span></span>
<span data-ttu-id="28ba2-109">New-AzureRmDataMigrationTask Cmdlet 會建立資料移轉任務。</span><span class="sxs-lookup"><span data-stu-id="28ba2-109">The New-AzureRmDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="28ba2-110">這個 Cmdlet 採用任務類型枚舉器、Azure 資源群組、關聯 Azure 資料移轉服務的名稱和專案作為輸入的參數。</span><span class="sxs-lookup"><span data-stu-id="28ba2-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Data Migration Service and Project as input.</span></span> 

## <span data-ttu-id="28ba2-111">示例</span><span class="sxs-lookup"><span data-stu-id="28ba2-111">EXAMPLES</span></span>

### <span data-ttu-id="28ba2-112">範例1</span><span class="sxs-lookup"><span data-stu-id="28ba2-112">Example 1</span></span>
```
PS C:\> New-AzureRmDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs
```
<span data-ttu-id="28ba2-113">這個範例腳本示範如何在名為 [myDMSProject] 的專案或名為 [TestService] 的服務中，建立名為 MyMigrationTask 的新資料移轉任務。</span><span class="sxs-lookup"><span data-stu-id="28ba2-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="28ba2-114">參數</span><span class="sxs-lookup"><span data-stu-id="28ba2-114">PARAMETERS</span></span>

### <span data-ttu-id="28ba2-115">-確認</span><span class="sxs-lookup"><span data-stu-id="28ba2-115">-Confirm</span></span>
<span data-ttu-id="28ba2-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="28ba2-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ba2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28ba2-117">-DefaultProfile</span></span>
<span data-ttu-id="28ba2-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="28ba2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ba2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28ba2-119">-InputObject</span></span>
<span data-ttu-id="28ba2-120">PSProject 物件。</span><span class="sxs-lookup"><span data-stu-id="28ba2-120">PSProject Object.</span></span>

```yaml
Type: PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28ba2-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="28ba2-121">-Name</span></span>
<span data-ttu-id="28ba2-122">任務的名稱。</span><span class="sxs-lookup"><span data-stu-id="28ba2-122">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ba2-123">-專案名稱</span><span class="sxs-lookup"><span data-stu-id="28ba2-123">-ProjectName</span></span>
<span data-ttu-id="28ba2-124">專案名稱。</span><span class="sxs-lookup"><span data-stu-id="28ba2-124">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ba2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28ba2-125">-ResourceGroupName</span></span>
<span data-ttu-id="28ba2-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="28ba2-126">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ba2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28ba2-127">-ResourceId</span></span>
<span data-ttu-id="28ba2-128">[專案資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="28ba2-128">Project Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28ba2-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="28ba2-129">-ServiceName</span></span>
<span data-ttu-id="28ba2-130">資料移轉服務名稱。</span><span class="sxs-lookup"><span data-stu-id="28ba2-130">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ba2-131">-TaskType</span><span class="sxs-lookup"><span data-stu-id="28ba2-131">-TaskType</span></span>
<span data-ttu-id="28ba2-132">任務類型。</span><span class="sxs-lookup"><span data-stu-id="28ba2-132">Task Type.</span></span>

```yaml
Type: TaskTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ba2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28ba2-133">-WhatIf</span></span>
<span data-ttu-id="28ba2-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="28ba2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28ba2-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28ba2-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="28ba2-136">輸入</span><span class="sxs-lookup"><span data-stu-id="28ba2-136">INPUTS</span></span>

### <span data-ttu-id="28ba2-137">PSProject 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="28ba2-137">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="28ba2-138">System.object</span><span class="sxs-lookup"><span data-stu-id="28ba2-138">System.String</span></span>


## <span data-ttu-id="28ba2-139">輸出</span><span class="sxs-lookup"><span data-stu-id="28ba2-139">OUTPUTS</span></span>

### <span data-ttu-id="28ba2-140">PSProjectTask 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="28ba2-140">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>


## <span data-ttu-id="28ba2-141">筆記</span><span class="sxs-lookup"><span data-stu-id="28ba2-141">NOTES</span></span>

## <span data-ttu-id="28ba2-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="28ba2-142">RELATED LINKS</span></span>


