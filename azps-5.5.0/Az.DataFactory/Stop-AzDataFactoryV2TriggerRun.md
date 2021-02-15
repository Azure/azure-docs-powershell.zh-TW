---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: e2800614e414a041073ae5396fb4b0e1e5833b59
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136423"
---
# <span data-ttu-id="e8548-101">Stop-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="e8548-101">Stop-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="e8548-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8548-102">SYNOPSIS</span></span>
<span data-ttu-id="e8548-103">停止在資料工廠中執行的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="e8548-103">Stops a trigger run in a data factory.</span></span>

## <span data-ttu-id="e8548-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8548-104">SYNTAX</span></span>

### <span data-ttu-id="e8548-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="e8548-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8548-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e8548-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8548-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e8548-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8548-108">說明</span><span class="sxs-lookup"><span data-stu-id="e8548-108">DESCRIPTION</span></span>
<span data-ttu-id="e8548-109">**AzDataFactoryV2TriggerRun** Cmdlet 會在使用觸發程式名稱和觸發程式 ID 指定的資料工廠中停止觸發觸發程式。</span><span class="sxs-lookup"><span data-stu-id="e8548-109">The **Stop-AzDataFactoryV2TriggerRun** cmdlet stops a trigger run in a data factory specified with the trigger name and trigger run ID.</span></span>
<span data-ttu-id="e8548-110">目前僅支援在 WaitingOnDependency 狀態中 TumblingWindowTriggers。</span><span class="sxs-lookup"><span data-stu-id="e8548-110">Currently only supported for TumblingWindowTriggers in WaitingOnDependency State.</span></span>

## <span data-ttu-id="e8548-111">示例</span><span class="sxs-lookup"><span data-stu-id="e8548-111">EXAMPLES</span></span>

### <span data-ttu-id="e8548-112">範例1</span><span class="sxs-lookup"><span data-stu-id="e8548-112">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```

<span data-ttu-id="e8548-113">這個命令會在工廠 WikiADF 中停止 id 為「08586002468005888497807248799CU16」的觸發程式執行。</span><span class="sxs-lookup"><span data-stu-id="e8548-113">This command stops the trigger run with id '08586002468005888497807248799CU16' in the factory WikiADF.</span></span>

## <span data-ttu-id="e8548-114">參數</span><span class="sxs-lookup"><span data-stu-id="e8548-114">PARAMETERS</span></span>

### <span data-ttu-id="e8548-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e8548-115">-DataFactory</span></span>
<span data-ttu-id="e8548-116">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="e8548-116">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8548-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e8548-117">-DataFactoryName</span></span>
<span data-ttu-id="e8548-118">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="e8548-118">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8548-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8548-119">-DefaultProfile</span></span>
<span data-ttu-id="e8548-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8548-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8548-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8548-121">-InputObject</span></span>
<span data-ttu-id="e8548-122">觸發程式執行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e8548-122">The information about the trigger run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8548-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8548-123">-PassThru</span></span>
<span data-ttu-id="e8548-124">如果已指定，則在 case 操作成功時，此 Cmdlet 會寫入 true。</span><span class="sxs-lookup"><span data-stu-id="e8548-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="e8548-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8548-125">-ResourceGroupName</span></span>
<span data-ttu-id="e8548-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8548-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8548-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="e8548-127">-TriggerName</span></span>
<span data-ttu-id="e8548-128">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="e8548-128">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8548-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="e8548-129">-TriggerRunId</span></span>
<span data-ttu-id="e8548-130">觸發程式的 [執行識別碼]。</span><span class="sxs-lookup"><span data-stu-id="e8548-130">The Run ID of the trigger.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8548-131">-確認</span><span class="sxs-lookup"><span data-stu-id="e8548-131">-Confirm</span></span>
<span data-ttu-id="e8548-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e8548-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8548-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8548-133">-WhatIf</span></span>
<span data-ttu-id="e8548-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e8548-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8548-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8548-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8548-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8548-136">CommonParameters</span></span>
<span data-ttu-id="e8548-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8548-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8548-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e8548-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8548-139">輸入</span><span class="sxs-lookup"><span data-stu-id="e8548-139">INPUTS</span></span>

### <span data-ttu-id="e8548-140">PSTriggerRun 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="e8548-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="e8548-141">System.object</span><span class="sxs-lookup"><span data-stu-id="e8548-141">System.String</span></span>

### <span data-ttu-id="e8548-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e8548-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="e8548-143">輸出</span><span class="sxs-lookup"><span data-stu-id="e8548-143">OUTPUTS</span></span>

### <span data-ttu-id="e8548-144">System.object</span><span class="sxs-lookup"><span data-stu-id="e8548-144">System.Boolean</span></span>

## <span data-ttu-id="e8548-145">筆記</span><span class="sxs-lookup"><span data-stu-id="e8548-145">NOTES</span></span>

## <span data-ttu-id="e8548-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8548-146">RELATED LINKS</span></span>
