---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Remove-AzureRmDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
ms.openlocfilehash: 295ac647bcbe04e26e761e4fdf8fe2bd30282218
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456088"
---
# <span data-ttu-id="c6674-101">Remove-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="c6674-101">Remove-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="c6674-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c6674-102">SYNOPSIS</span></span>
<span data-ttu-id="c6674-103">從 Azure 移除 Azure 資料庫移轉服務任務。</span><span class="sxs-lookup"><span data-stu-id="c6674-103">Removes an Azure Database Migration Service task from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6674-104">句法</span><span class="sxs-lookup"><span data-stu-id="c6674-104">SYNTAX</span></span>

### <span data-ttu-id="c6674-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c6674-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6674-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6674-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6674-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6674-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6674-108">說明</span><span class="sxs-lookup"><span data-stu-id="c6674-108">DESCRIPTION</span></span>
<span data-ttu-id="c6674-109">Remove-AzureRmDataMigrationTask Cmdlet 會從 Azure 中移除 Azure 資料庫移轉服務任務。</span><span class="sxs-lookup"><span data-stu-id="c6674-109">The Remove-AzureRmDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="c6674-110">示例</span><span class="sxs-lookup"><span data-stu-id="c6674-110">EXAMPLES</span></span>

### <span data-ttu-id="c6674-111">範例1</span><span class="sxs-lookup"><span data-stu-id="c6674-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask -TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="c6674-112">上述範例會從 Azure 根據 [任務名稱] 參數移除名為 TestTask 的 Azure 資料庫移轉服務任務。</span><span class="sxs-lookup"><span data-stu-id="c6674-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="c6674-113">範例2</span><span class="sxs-lookup"><span data-stu-id="c6674-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask -InputObject $TestTask
```

<span data-ttu-id="c6674-114">前面的範例會根據傳入的 PSProjectTask 物件，移除 Azure 資料庫移轉服務任務。</span><span class="sxs-lookup"><span data-stu-id="c6674-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="c6674-115">參數</span><span class="sxs-lookup"><span data-stu-id="c6674-115">PARAMETERS</span></span>

### <span data-ttu-id="c6674-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6674-116">-DefaultProfile</span></span>
<span data-ttu-id="c6674-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6674-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6674-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c6674-118">-Force</span></span>
<span data-ttu-id="c6674-119">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="c6674-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="c6674-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6674-120">-InputObject</span></span>
<span data-ttu-id="c6674-121">PSProjectTask 物件。</span><span class="sxs-lookup"><span data-stu-id="c6674-121">PSProjectTask Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6674-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="c6674-122">-Name</span></span>
<span data-ttu-id="c6674-123">任務的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6674-123">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6674-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6674-124">-PassThru</span></span>
<span data-ttu-id="c6674-125">會傳回 true/false。</span><span class="sxs-lookup"><span data-stu-id="c6674-125">Returns an true/false.</span></span>
<span data-ttu-id="c6674-126">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="c6674-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c6674-127">-專案名稱</span><span class="sxs-lookup"><span data-stu-id="c6674-127">-ProjectName</span></span>
<span data-ttu-id="c6674-128">專案名稱。</span><span class="sxs-lookup"><span data-stu-id="c6674-128">The name of the project.</span></span>

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

### <span data-ttu-id="c6674-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6674-129">-ResourceGroupName</span></span>
<span data-ttu-id="c6674-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6674-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="c6674-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6674-131">-ResourceId</span></span>
<span data-ttu-id="c6674-132">[專案資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="c6674-132">Project Resource Id.</span></span>

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

### <span data-ttu-id="c6674-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c6674-133">-ServiceName</span></span>
<span data-ttu-id="c6674-134">資料庫移轉服務名稱。</span><span class="sxs-lookup"><span data-stu-id="c6674-134">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="c6674-135">-確認</span><span class="sxs-lookup"><span data-stu-id="c6674-135">-Confirm</span></span>
<span data-ttu-id="c6674-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c6674-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6674-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6674-137">-WhatIf</span></span>
<span data-ttu-id="c6674-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c6674-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6674-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6674-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6674-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6674-140">CommonParameters</span></span>
<span data-ttu-id="c6674-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c6674-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6674-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c6674-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6674-143">輸入</span><span class="sxs-lookup"><span data-stu-id="c6674-143">INPUTS</span></span>

### <span data-ttu-id="c6674-144">PSProjectTask 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="c6674-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>
<span data-ttu-id="c6674-145">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="c6674-145">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="c6674-146">System.object</span><span class="sxs-lookup"><span data-stu-id="c6674-146">System.String</span></span>

## <span data-ttu-id="c6674-147">輸出</span><span class="sxs-lookup"><span data-stu-id="c6674-147">OUTPUTS</span></span>

### <span data-ttu-id="c6674-148">System.object</span><span class="sxs-lookup"><span data-stu-id="c6674-148">System.Boolean</span></span>

## <span data-ttu-id="c6674-149">筆記</span><span class="sxs-lookup"><span data-stu-id="c6674-149">NOTES</span></span>

## <span data-ttu-id="c6674-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6674-150">RELATED LINKS</span></span>
