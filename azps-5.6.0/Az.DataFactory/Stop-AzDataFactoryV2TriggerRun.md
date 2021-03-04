---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/stop-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: 1e3310b99173c0a7fa83dcada286833747457213
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905141"
---
# <span data-ttu-id="4960c-101">Stop-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="4960c-101">Stop-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="4960c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4960c-102">SYNOPSIS</span></span>
<span data-ttu-id="4960c-103">停止在資料工廠中執行觸發程式。</span><span class="sxs-lookup"><span data-stu-id="4960c-103">Stops a trigger run in a data factory.</span></span>

## <span data-ttu-id="4960c-104">語法</span><span class="sxs-lookup"><span data-stu-id="4960c-104">SYNTAX</span></span>

### <span data-ttu-id="4960c-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="4960c-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4960c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4960c-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4960c-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4960c-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4960c-108">描述</span><span class="sxs-lookup"><span data-stu-id="4960c-108">DESCRIPTION</span></span>
<span data-ttu-id="4960c-109">**Stop-AzDataFactoryV2TriggerRun** Cmdlet 會停止以觸發程式名稱指定的資料工廠中的觸發程式執行，並觸發執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="4960c-109">The **Stop-AzDataFactoryV2TriggerRun** cmdlet stops a trigger run in a data factory specified with the trigger name and trigger run ID.</span></span>
<span data-ttu-id="4960c-110">目前僅支援 WaitingOnDependency 狀態中的 WindowTriggers。</span><span class="sxs-lookup"><span data-stu-id="4960c-110">Currently only supported for TumblingWindowTriggers in WaitingOnDependency State.</span></span>

## <span data-ttu-id="4960c-111">例子</span><span class="sxs-lookup"><span data-stu-id="4960c-111">EXAMPLES</span></span>

### <span data-ttu-id="4960c-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="4960c-112">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```

<span data-ttu-id="4960c-113">此命令會停止觸發程式在工廠 WikiADF 中以 id 為 '0858600246800588497807248799CU16'執行。</span><span class="sxs-lookup"><span data-stu-id="4960c-113">This command stops the trigger run with id '08586002468005888497807248799CU16' in the factory WikiADF.</span></span>

## <span data-ttu-id="4960c-114">參數</span><span class="sxs-lookup"><span data-stu-id="4960c-114">PARAMETERS</span></span>

### <span data-ttu-id="4960c-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="4960c-115">-DataFactory</span></span>
<span data-ttu-id="4960c-116">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="4960c-116">The data factory object.</span></span>

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

### <span data-ttu-id="4960c-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4960c-117">-DataFactoryName</span></span>
<span data-ttu-id="4960c-118">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="4960c-118">The data factory name.</span></span>

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

### <span data-ttu-id="4960c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4960c-119">-DefaultProfile</span></span>
<span data-ttu-id="4960c-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4960c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4960c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4960c-121">-InputObject</span></span>
<span data-ttu-id="4960c-122">觸發程式執行的資訊。</span><span class="sxs-lookup"><span data-stu-id="4960c-122">The information about the trigger run.</span></span>

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

### <span data-ttu-id="4960c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4960c-123">-PassThru</span></span>
<span data-ttu-id="4960c-124">如果指定 Cmdlet 寫入 true，以防作業成功。</span><span class="sxs-lookup"><span data-stu-id="4960c-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="4960c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4960c-125">-ResourceGroupName</span></span>
<span data-ttu-id="4960c-126">資源組名。</span><span class="sxs-lookup"><span data-stu-id="4960c-126">The resource group name.</span></span>

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

### <span data-ttu-id="4960c-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="4960c-127">-TriggerName</span></span>
<span data-ttu-id="4960c-128">觸發者名稱。</span><span class="sxs-lookup"><span data-stu-id="4960c-128">The trigger name.</span></span>

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

### <span data-ttu-id="4960c-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="4960c-129">-TriggerRunId</span></span>
<span data-ttu-id="4960c-130">觸發程式執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="4960c-130">The Run ID of the trigger.</span></span>

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

### <span data-ttu-id="4960c-131">-確認</span><span class="sxs-lookup"><span data-stu-id="4960c-131">-Confirm</span></span>
<span data-ttu-id="4960c-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4960c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4960c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4960c-133">-WhatIf</span></span>
<span data-ttu-id="4960c-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4960c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4960c-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4960c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4960c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4960c-136">CommonParameters</span></span>
<span data-ttu-id="4960c-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4960c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4960c-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4960c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4960c-139">輸入</span><span class="sxs-lookup"><span data-stu-id="4960c-139">INPUTS</span></span>

### <span data-ttu-id="4960c-140">Microsoft.Azure.Commands.DataFactoryV2.models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="4960c-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="4960c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="4960c-141">System.String</span></span>

### <span data-ttu-id="4960c-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4960c-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="4960c-143">輸出</span><span class="sxs-lookup"><span data-stu-id="4960c-143">OUTPUTS</span></span>

### <span data-ttu-id="4960c-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4960c-144">System.Boolean</span></span>

## <span data-ttu-id="4960c-145">筆記</span><span class="sxs-lookup"><span data-stu-id="4960c-145">NOTES</span></span>

## <span data-ttu-id="4960c-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="4960c-146">RELATED LINKS</span></span>
