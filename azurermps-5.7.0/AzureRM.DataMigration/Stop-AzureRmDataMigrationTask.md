---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/stop-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationTask.md
ms.openlocfilehash: 7cf68cd27125580c6f0e57a7849c1fadc8cb47fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624309"
---
# <span data-ttu-id="5b7a6-101">Stop-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="5b7a6-101">Stop-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="5b7a6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5b7a6-102">SYNOPSIS</span></span>
<span data-ttu-id="5b7a6-103">停止處於執行中狀態的 Azure 資料庫移轉服務任務。</span><span class="sxs-lookup"><span data-stu-id="5b7a6-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b7a6-104">句法</span><span class="sxs-lookup"><span data-stu-id="5b7a6-104">SYNTAX</span></span>

### <span data-ttu-id="5b7a6-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5b7a6-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="5b7a6-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b7a6-106">ComponentObjectParameterSet</span></span>
```
Stop-AzureRmDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="5b7a6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b7a6-107">ResourceIdParameterSet</span></span>
```
Stop-AzureRmDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="5b7a6-108">說明</span><span class="sxs-lookup"><span data-stu-id="5b7a6-108">DESCRIPTION</span></span>
<span data-ttu-id="5b7a6-109">Stop-AzureRmDataMigrationTask Cmdlet 會停止執行中狀態的資料庫移轉活動。</span><span class="sxs-lookup"><span data-stu-id="5b7a6-109">Stop-AzureRmDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="5b7a6-110">示例</span><span class="sxs-lookup"><span data-stu-id="5b7a6-110">EXAMPLES</span></span>

### <span data-ttu-id="5b7a6-111">範例1</span><span class="sxs-lookup"><span data-stu-id="5b7a6-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="5b7a6-112">上面的範例會停止名為 myDMSTask 的 Azure 資料庫移轉服務工作與名為 TestService 的 project myDMSProject 和 Azure Database 遷移服務實例</span><span class="sxs-lookup"><span data-stu-id="5b7a6-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="5b7a6-113">範例2</span><span class="sxs-lookup"><span data-stu-id="5b7a6-113">Example 2</span></span>
```
PS C:\> Stop-AzureRmDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="5b7a6-114">上述範例會停止以輸入參數 PSProjectTask 物件形式傳入的 Azure Database 遷移服務任務</span><span class="sxs-lookup"><span data-stu-id="5b7a6-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="5b7a6-115">參數</span><span class="sxs-lookup"><span data-stu-id="5b7a6-115">PARAMETERS</span></span>

### <span data-ttu-id="5b7a6-116">-確認</span><span class="sxs-lookup"><span data-stu-id="5b7a6-116">-Confirm</span></span>
<span data-ttu-id="5b7a6-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5b7a6-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b7a6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b7a6-118">-DefaultProfile</span></span>
<span data-ttu-id="5b7a6-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5b7a6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b7a6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b7a6-120">-InputObject</span></span>
<span data-ttu-id="5b7a6-121">PSProjectTask 物件。</span><span class="sxs-lookup"><span data-stu-id="5b7a6-121">PSProjectTask Object.</span></span>

```yaml
Type: PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b7a6-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="5b7a6-122">-Name</span></span>
<span data-ttu-id="5b7a6-123">任務的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b7a6-123">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b7a6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b7a6-124">-PassThru</span></span>
<span data-ttu-id="5b7a6-125">會傳回 true/false。</span><span class="sxs-lookup"><span data-stu-id="5b7a6-125">Returns an true/false.</span></span>
<span data-ttu-id="5b7a6-126">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="5b7a6-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b7a6-127">-專案名稱</span><span class="sxs-lookup"><span data-stu-id="5b7a6-127">-ProjectName</span></span>
<span data-ttu-id="5b7a6-128">專案名稱。</span><span class="sxs-lookup"><span data-stu-id="5b7a6-128">The name of the project.</span></span>

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

### <span data-ttu-id="5b7a6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b7a6-129">-ResourceGroupName</span></span>
<span data-ttu-id="5b7a6-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b7a6-130">The name of the resource group .</span></span>

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

### <span data-ttu-id="5b7a6-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b7a6-131">-ResourceId</span></span>
<span data-ttu-id="5b7a6-132">ProjectTask 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5b7a6-132">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="5b7a6-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5b7a6-133">-ServiceName</span></span>
<span data-ttu-id="5b7a6-134">資料移轉服務名稱。</span><span class="sxs-lookup"><span data-stu-id="5b7a6-134">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="5b7a6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b7a6-135">-WhatIf</span></span>
<span data-ttu-id="5b7a6-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5b7a6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b7a6-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5b7a6-137">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="5b7a6-138">輸入</span><span class="sxs-lookup"><span data-stu-id="5b7a6-138">INPUTS</span></span>

### <span data-ttu-id="5b7a6-139">PSProjectTask 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="5b7a6-139">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>
<span data-ttu-id="5b7a6-140">System.object</span><span class="sxs-lookup"><span data-stu-id="5b7a6-140">System.String</span></span>


## <span data-ttu-id="5b7a6-141">輸出</span><span class="sxs-lookup"><span data-stu-id="5b7a6-141">OUTPUTS</span></span>

### <span data-ttu-id="5b7a6-142">System.object</span><span class="sxs-lookup"><span data-stu-id="5b7a6-142">System.Boolean</span></span>


## <span data-ttu-id="5b7a6-143">筆記</span><span class="sxs-lookup"><span data-stu-id="5b7a6-143">NOTES</span></span>

## <span data-ttu-id="5b7a6-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b7a6-144">RELATED LINKS</span></span>

