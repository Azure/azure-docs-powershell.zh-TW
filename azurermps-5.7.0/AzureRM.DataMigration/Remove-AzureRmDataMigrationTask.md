---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
ms.openlocfilehash: d192b7f422557b4d4373f794e98cdb2556db3c63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450619"
---
# <span data-ttu-id="90aa6-101">Remove-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="90aa6-101">Remove-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="90aa6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="90aa6-102">SYNOPSIS</span></span>
<span data-ttu-id="90aa6-103">從 Azure 移除 Azure 資料庫移轉服務任務。</span><span class="sxs-lookup"><span data-stu-id="90aa6-103">Removes an Azure Database Migration Service task from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90aa6-104">句法</span><span class="sxs-lookup"><span data-stu-id="90aa6-104">SYNTAX</span></span>

### <span data-ttu-id="90aa6-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="90aa6-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="90aa6-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="90aa6-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="90aa6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="90aa6-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="90aa6-108">說明</span><span class="sxs-lookup"><span data-stu-id="90aa6-108">DESCRIPTION</span></span>
<span data-ttu-id="90aa6-109">Remove-AzureRmDataMigrationTask Cmdlet 會從 Azure 中移除 Azure 資料庫移轉服務任務。</span><span class="sxs-lookup"><span data-stu-id="90aa6-109">The Remove-AzureRmDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="90aa6-110">示例</span><span class="sxs-lookup"><span data-stu-id="90aa6-110">EXAMPLES</span></span>

### <span data-ttu-id="90aa6-111">範例1</span><span class="sxs-lookup"><span data-stu-id="90aa6-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask –TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup

```

<span data-ttu-id="90aa6-112">上述範例會從 Azure 根據 [任務名稱] 參數移除名為 TestTask 的 Azure 資料庫移轉服務任務。</span><span class="sxs-lookup"><span data-stu-id="90aa6-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="90aa6-113">範例2</span><span class="sxs-lookup"><span data-stu-id="90aa6-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask –InputObject $TestTask

```

<span data-ttu-id="90aa6-114">前面的範例會根據傳入的 PSProjectTask 物件，移除 Azure 資料庫移轉服務任務。</span><span class="sxs-lookup"><span data-stu-id="90aa6-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="90aa6-115">參數</span><span class="sxs-lookup"><span data-stu-id="90aa6-115">PARAMETERS</span></span>

### <span data-ttu-id="90aa6-116">-確認</span><span class="sxs-lookup"><span data-stu-id="90aa6-116">-Confirm</span></span>
<span data-ttu-id="90aa6-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="90aa6-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90aa6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90aa6-118">-DefaultProfile</span></span>
<span data-ttu-id="90aa6-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="90aa6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90aa6-120">-Force</span><span class="sxs-lookup"><span data-stu-id="90aa6-120">-Force</span></span>
<span data-ttu-id="90aa6-121">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="90aa6-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="90aa6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90aa6-122">-InputObject</span></span>
<span data-ttu-id="90aa6-123">PSProjectTask 物件。</span><span class="sxs-lookup"><span data-stu-id="90aa6-123">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="90aa6-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="90aa6-124">-Name</span></span>
<span data-ttu-id="90aa6-125">任務的名稱。</span><span class="sxs-lookup"><span data-stu-id="90aa6-125">The name of the task.</span></span>

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

### <span data-ttu-id="90aa6-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90aa6-126">-PassThru</span></span>
<span data-ttu-id="90aa6-127">會傳回 true/false。</span><span class="sxs-lookup"><span data-stu-id="90aa6-127">Returns an true/false.</span></span>
<span data-ttu-id="90aa6-128">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="90aa6-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="90aa6-129">-專案名稱</span><span class="sxs-lookup"><span data-stu-id="90aa6-129">-ProjectName</span></span>
<span data-ttu-id="90aa6-130">專案名稱。</span><span class="sxs-lookup"><span data-stu-id="90aa6-130">The name of the project.</span></span>

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

### <span data-ttu-id="90aa6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90aa6-131">-ResourceGroupName</span></span>
<span data-ttu-id="90aa6-132">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="90aa6-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="90aa6-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90aa6-133">-ResourceId</span></span>
<span data-ttu-id="90aa6-134">[專案資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="90aa6-134">Project Resource Id.</span></span>

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

### <span data-ttu-id="90aa6-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="90aa6-135">-ServiceName</span></span>
<span data-ttu-id="90aa6-136">資料移轉服務名稱。</span><span class="sxs-lookup"><span data-stu-id="90aa6-136">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="90aa6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90aa6-137">-WhatIf</span></span>
<span data-ttu-id="90aa6-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="90aa6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90aa6-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90aa6-139">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="90aa6-140">輸入</span><span class="sxs-lookup"><span data-stu-id="90aa6-140">INPUTS</span></span>

### <span data-ttu-id="90aa6-141">PSProjectTask 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="90aa6-141">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>
<span data-ttu-id="90aa6-142">System.object</span><span class="sxs-lookup"><span data-stu-id="90aa6-142">System.String</span></span>


## <span data-ttu-id="90aa6-143">輸出</span><span class="sxs-lookup"><span data-stu-id="90aa6-143">OUTPUTS</span></span>

### <span data-ttu-id="90aa6-144">System.object</span><span class="sxs-lookup"><span data-stu-id="90aa6-144">System.Boolean</span></span>


## <span data-ttu-id="90aa6-145">筆記</span><span class="sxs-lookup"><span data-stu-id="90aa6-145">NOTES</span></span>

## <span data-ttu-id="90aa6-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="90aa6-146">RELATED LINKS</span></span>


