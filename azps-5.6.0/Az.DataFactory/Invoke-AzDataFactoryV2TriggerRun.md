---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/invoke-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: 91eb23f3af613cf349219f82d133d08dd6e65b5c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907677"
---
# <span data-ttu-id="c81b7-101">Invoke-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="c81b7-101">Invoke-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="c81b7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c81b7-102">SYNOPSIS</span></span>
 <span data-ttu-id="c81b7-103">會啟動觸發程式執行的另一個實例。</span><span class="sxs-lookup"><span data-stu-id="c81b7-103">Invokes another instance of a trigger run.</span></span>

## <span data-ttu-id="c81b7-104">語法</span><span class="sxs-lookup"><span data-stu-id="c81b7-104">SYNTAX</span></span>

### <span data-ttu-id="c81b7-105">ByFactoryNameByParameterFile (預設) </span><span class="sxs-lookup"><span data-stu-id="c81b7-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c81b7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c81b7-106">ByInputObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c81b7-107">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="c81b7-107">ByFactoryName</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c81b7-108">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c81b7-108">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c81b7-109">描述</span><span class="sxs-lookup"><span data-stu-id="c81b7-109">DESCRIPTION</span></span>
<span data-ttu-id="c81b7-110">**Invoke-AzDataFactoryV2TriggerRun** 命令會以新的觸發程式執行識別碼啟動另一個觸發程式執行實例。</span><span class="sxs-lookup"><span data-stu-id="c81b7-110">The **Invoke-AzDataFactoryV2TriggerRun** command starts another instance of a trigger run with a new trigger run id.</span></span>

## <span data-ttu-id="c81b7-111">例子</span><span class="sxs-lookup"><span data-stu-id="c81b7-111">EXAMPLES</span></span>

### <span data-ttu-id="c81b7-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="c81b7-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```
<span data-ttu-id="c81b7-113">以新的觸發程式執行識別碼啟動另一個觸發程式執行實例，並保留與原始觸發程式執行相同的視窗StartTime 和 windowEndTime。</span><span class="sxs-lookup"><span data-stu-id="c81b7-113">Starts another instance of a trigger run with a new trigger run id, keeping the same windowStartTime and windowEndTime as the original trigger run.</span></span>

## <span data-ttu-id="c81b7-114">參數</span><span class="sxs-lookup"><span data-stu-id="c81b7-114">PARAMETERS</span></span>

### <span data-ttu-id="c81b7-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="c81b7-115">-DataFactory</span></span>
<span data-ttu-id="c81b7-116">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="c81b7-116">The data factory object.</span></span>

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

### <span data-ttu-id="c81b7-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c81b7-117">-DataFactoryName</span></span>
<span data-ttu-id="c81b7-118">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="c81b7-118">The data factory name.</span></span>

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

### <span data-ttu-id="c81b7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c81b7-119">-DefaultProfile</span></span>
<span data-ttu-id="c81b7-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c81b7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c81b7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c81b7-121">-InputObject</span></span>
<span data-ttu-id="c81b7-122">觸發程式執行的資訊。</span><span class="sxs-lookup"><span data-stu-id="c81b7-122">The information about the trigger run.</span></span>

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

### <span data-ttu-id="c81b7-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c81b7-123">-PassThru</span></span>
<span data-ttu-id="c81b7-124">如果指定 Cmdlet 寫入 true，以防作業成功。</span><span class="sxs-lookup"><span data-stu-id="c81b7-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="c81b7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c81b7-125">-ResourceGroupName</span></span>
<span data-ttu-id="c81b7-126">資源組名。</span><span class="sxs-lookup"><span data-stu-id="c81b7-126">The resource group name.</span></span>

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

### <span data-ttu-id="c81b7-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="c81b7-127">-TriggerName</span></span>
<span data-ttu-id="c81b7-128">觸發者名稱。</span><span class="sxs-lookup"><span data-stu-id="c81b7-128">The trigger name.</span></span>

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

### <span data-ttu-id="c81b7-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="c81b7-129">-TriggerRunId</span></span>
<span data-ttu-id="c81b7-130">觸發程式執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="c81b7-130">The Run ID of the trigger.</span></span>

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

### <span data-ttu-id="c81b7-131">-確認</span><span class="sxs-lookup"><span data-stu-id="c81b7-131">-Confirm</span></span>
<span data-ttu-id="c81b7-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c81b7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c81b7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c81b7-133">-WhatIf</span></span>
<span data-ttu-id="c81b7-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c81b7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c81b7-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c81b7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c81b7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c81b7-136">CommonParameters</span></span>
<span data-ttu-id="c81b7-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c81b7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c81b7-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c81b7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c81b7-139">輸入</span><span class="sxs-lookup"><span data-stu-id="c81b7-139">INPUTS</span></span>

### <span data-ttu-id="c81b7-140">Microsoft.Azure.Commands.DataFactoryV2.models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="c81b7-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="c81b7-141">System.String</span><span class="sxs-lookup"><span data-stu-id="c81b7-141">System.String</span></span>

### <span data-ttu-id="c81b7-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c81b7-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="c81b7-143">輸出</span><span class="sxs-lookup"><span data-stu-id="c81b7-143">OUTPUTS</span></span>

### <span data-ttu-id="c81b7-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="c81b7-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="c81b7-145">筆記</span><span class="sxs-lookup"><span data-stu-id="c81b7-145">NOTES</span></span>

## <span data-ttu-id="c81b7-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="c81b7-146">RELATED LINKS</span></span>
