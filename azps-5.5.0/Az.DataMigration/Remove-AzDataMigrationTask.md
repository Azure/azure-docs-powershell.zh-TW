---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
ms.openlocfilehash: c5307aa4e7f78e8586ff28fd77bd125cdf736602
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129435"
---
# <span data-ttu-id="49391-101">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="49391-101">Remove-AzDataMigrationTask</span></span>

## <span data-ttu-id="49391-102">摘要</span><span class="sxs-lookup"><span data-stu-id="49391-102">SYNOPSIS</span></span>
<span data-ttu-id="49391-103">從 Azure 移除 Azure 資料庫移轉服務任務。</span><span class="sxs-lookup"><span data-stu-id="49391-103">Removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="49391-104">句法</span><span class="sxs-lookup"><span data-stu-id="49391-104">SYNTAX</span></span>

### <span data-ttu-id="49391-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="49391-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49391-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49391-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49391-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49391-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49391-108">說明</span><span class="sxs-lookup"><span data-stu-id="49391-108">DESCRIPTION</span></span>
<span data-ttu-id="49391-109">Remove-AzDataMigrationTask Cmdlet 會從 Azure 中移除 Azure 資料庫移轉服務任務。</span><span class="sxs-lookup"><span data-stu-id="49391-109">The Remove-AzDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="49391-110">示例</span><span class="sxs-lookup"><span data-stu-id="49391-110">EXAMPLES</span></span>

### <span data-ttu-id="49391-111">範例1</span><span class="sxs-lookup"><span data-stu-id="49391-111">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationTask -TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="49391-112">上述範例會從 Azure 根據 [任務名稱] 參數移除名為 TestTask 的 Azure 資料庫移轉服務任務。</span><span class="sxs-lookup"><span data-stu-id="49391-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="49391-113">範例2</span><span class="sxs-lookup"><span data-stu-id="49391-113">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationTask -InputObject $TestTask
```

<span data-ttu-id="49391-114">前面的範例會根據傳入的 PSProjectTask 物件，移除 Azure 資料庫移轉服務任務。</span><span class="sxs-lookup"><span data-stu-id="49391-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="49391-115">參數</span><span class="sxs-lookup"><span data-stu-id="49391-115">PARAMETERS</span></span>

### <span data-ttu-id="49391-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49391-116">-DefaultProfile</span></span>
<span data-ttu-id="49391-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="49391-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49391-118">-Force</span><span class="sxs-lookup"><span data-stu-id="49391-118">-Force</span></span>
<span data-ttu-id="49391-119">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="49391-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="49391-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49391-120">-InputObject</span></span>
<span data-ttu-id="49391-121">PSProjectTask 物件。</span><span class="sxs-lookup"><span data-stu-id="49391-121">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="49391-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="49391-122">-Name</span></span>
<span data-ttu-id="49391-123">任務的名稱。</span><span class="sxs-lookup"><span data-stu-id="49391-123">The name of the task.</span></span>

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

### <span data-ttu-id="49391-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49391-124">-PassThru</span></span>
<span data-ttu-id="49391-125">會傳回 true/false。</span><span class="sxs-lookup"><span data-stu-id="49391-125">Returns an true/false.</span></span>
<span data-ttu-id="49391-126">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="49391-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="49391-127">-專案名稱</span><span class="sxs-lookup"><span data-stu-id="49391-127">-ProjectName</span></span>
<span data-ttu-id="49391-128">專案名稱。</span><span class="sxs-lookup"><span data-stu-id="49391-128">The name of the project.</span></span>

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

### <span data-ttu-id="49391-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49391-129">-ResourceGroupName</span></span>
<span data-ttu-id="49391-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="49391-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="49391-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49391-131">-ResourceId</span></span>
<span data-ttu-id="49391-132">[專案資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="49391-132">Project Resource Id.</span></span>

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

### <span data-ttu-id="49391-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="49391-133">-ServiceName</span></span>
<span data-ttu-id="49391-134">資料庫移轉服務名稱。</span><span class="sxs-lookup"><span data-stu-id="49391-134">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="49391-135">-確認</span><span class="sxs-lookup"><span data-stu-id="49391-135">-Confirm</span></span>
<span data-ttu-id="49391-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="49391-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49391-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49391-137">-WhatIf</span></span>
<span data-ttu-id="49391-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="49391-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49391-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="49391-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49391-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49391-140">CommonParameters</span></span>
<span data-ttu-id="49391-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="49391-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49391-142">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="49391-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49391-143">輸入</span><span class="sxs-lookup"><span data-stu-id="49391-143">INPUTS</span></span>

### <span data-ttu-id="49391-144">PSProjectTask 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="49391-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="49391-145">System.object</span><span class="sxs-lookup"><span data-stu-id="49391-145">System.String</span></span>

## <span data-ttu-id="49391-146">輸出</span><span class="sxs-lookup"><span data-stu-id="49391-146">OUTPUTS</span></span>

### <span data-ttu-id="49391-147">System.object</span><span class="sxs-lookup"><span data-stu-id="49391-147">System.Boolean</span></span>

## <span data-ttu-id="49391-148">筆記</span><span class="sxs-lookup"><span data-stu-id="49391-148">NOTES</span></span>

## <span data-ttu-id="49391-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="49391-149">RELATED LINKS</span></span>
