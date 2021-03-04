---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/stop-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 096ee403a0ee12c80462a1fb87db4378e3d86f01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914042"
---
# <span data-ttu-id="a26c9-101">Stop-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="a26c9-101">Stop-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="a26c9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a26c9-102">SYNOPSIS</span></span>
<span data-ttu-id="a26c9-103">停止在資料工廠中執行管線。</span><span class="sxs-lookup"><span data-stu-id="a26c9-103">Stops a pipeline run in a data factory.</span></span>

## <span data-ttu-id="a26c9-104">語法</span><span class="sxs-lookup"><span data-stu-id="a26c9-104">SYNTAX</span></span>

### <span data-ttu-id="a26c9-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="a26c9-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a26c9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a26c9-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a26c9-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a26c9-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a26c9-108">描述</span><span class="sxs-lookup"><span data-stu-id="a26c9-108">DESCRIPTION</span></span>
<span data-ttu-id="a26c9-109">**Stop-AzDataFactoryV2PipelineRun** Cmdlet 會停止以管線執行識別碼指定之資料工廠中的管線執行。</span><span class="sxs-lookup"><span data-stu-id="a26c9-109">The **Stop-AzDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pipeline run ID.</span></span>

## <span data-ttu-id="a26c9-110">例子</span><span class="sxs-lookup"><span data-stu-id="a26c9-110">EXAMPLES</span></span>

### <span data-ttu-id="a26c9-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="a26c9-111">Example 1</span></span>
```
PS C:\> Stop-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="a26c9-112">此命令會停止使用 id b9730a13-aa12-4926-a8b3-8e3a974ab0bd 在工廠 WikiADF 中執行管線。</span><span class="sxs-lookup"><span data-stu-id="a26c9-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="a26c9-113">參數</span><span class="sxs-lookup"><span data-stu-id="a26c9-113">PARAMETERS</span></span>

### <span data-ttu-id="a26c9-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a26c9-114">-DataFactory</span></span>
<span data-ttu-id="a26c9-115">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="a26c9-115">The data factory object.</span></span>

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

### <span data-ttu-id="a26c9-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a26c9-116">-DataFactoryName</span></span>
<span data-ttu-id="a26c9-117">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="a26c9-117">The data factory name.</span></span>

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

### <span data-ttu-id="a26c9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a26c9-118">-DefaultProfile</span></span>
<span data-ttu-id="a26c9-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a26c9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a26c9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a26c9-120">-InputObject</span></span>
<span data-ttu-id="a26c9-121">管線的執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="a26c9-121">The Run ID of the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a26c9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a26c9-122">-PassThru</span></span>
<span data-ttu-id="a26c9-123">如果指定 Cmdlet 寫入 true，以防作業成功。</span><span class="sxs-lookup"><span data-stu-id="a26c9-123">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="a26c9-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="a26c9-124">-PipelineRunId</span></span>
<span data-ttu-id="a26c9-125">管線的執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="a26c9-125">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="a26c9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a26c9-126">-ResourceGroupName</span></span>
<span data-ttu-id="a26c9-127">資源組名。</span><span class="sxs-lookup"><span data-stu-id="a26c9-127">The resource group name.</span></span>

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

### <span data-ttu-id="a26c9-128">-確認</span><span class="sxs-lookup"><span data-stu-id="a26c9-128">-Confirm</span></span>
<span data-ttu-id="a26c9-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a26c9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a26c9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a26c9-130">-WhatIf</span></span>
<span data-ttu-id="a26c9-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a26c9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a26c9-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a26c9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a26c9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a26c9-133">CommonParameters</span></span>
<span data-ttu-id="a26c9-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a26c9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a26c9-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a26c9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a26c9-136">輸入</span><span class="sxs-lookup"><span data-stu-id="a26c9-136">INPUTS</span></span>

### <span data-ttu-id="a26c9-137">Microsoft.Azure.Commands.DataFactoryV2.models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="a26c9-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

### <span data-ttu-id="a26c9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a26c9-138">System.String</span></span>

### <span data-ttu-id="a26c9-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a26c9-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="a26c9-140">輸出</span><span class="sxs-lookup"><span data-stu-id="a26c9-140">OUTPUTS</span></span>

### <span data-ttu-id="a26c9-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a26c9-141">System.Boolean</span></span>

## <span data-ttu-id="a26c9-142">筆記</span><span class="sxs-lookup"><span data-stu-id="a26c9-142">NOTES</span></span>

## <span data-ttu-id="a26c9-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="a26c9-143">RELATED LINKS</span></span>
