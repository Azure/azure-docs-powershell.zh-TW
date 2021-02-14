---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 400862dbb27eb38d3189c08f741bb595a8e939b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141054"
---
# <span data-ttu-id="cc4e7-101">Stop-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="cc4e7-101">Stop-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="cc4e7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cc4e7-102">SYNOPSIS</span></span>
<span data-ttu-id="cc4e7-103">停止在資料工廠中執行管線。</span><span class="sxs-lookup"><span data-stu-id="cc4e7-103">Stops a pipeline run in a data factory.</span></span>

## <span data-ttu-id="cc4e7-104">句法</span><span class="sxs-lookup"><span data-stu-id="cc4e7-104">SYNTAX</span></span>

### <span data-ttu-id="cc4e7-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="cc4e7-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc4e7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cc4e7-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc4e7-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="cc4e7-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc4e7-108">說明</span><span class="sxs-lookup"><span data-stu-id="cc4e7-108">DESCRIPTION</span></span>
<span data-ttu-id="cc4e7-109">**AzDataFactoryV2PipelineRun** Cmdlet 會停止在使用管線執行 ID 指定的資料工廠中執行管線。</span><span class="sxs-lookup"><span data-stu-id="cc4e7-109">The **Stop-AzDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pipeline run ID.</span></span>

## <span data-ttu-id="cc4e7-110">示例</span><span class="sxs-lookup"><span data-stu-id="cc4e7-110">EXAMPLES</span></span>

### <span data-ttu-id="cc4e7-111">範例1</span><span class="sxs-lookup"><span data-stu-id="cc4e7-111">Example 1</span></span>
```
PS C:\> Stop-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="cc4e7-112">這個命令會在工廠 WikiADF 中停止執行 id 為 b9730a13-aa12-4926-a8b3-8e3a974ab0bd 的管道。</span><span class="sxs-lookup"><span data-stu-id="cc4e7-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="cc4e7-113">參數</span><span class="sxs-lookup"><span data-stu-id="cc4e7-113">PARAMETERS</span></span>

### <span data-ttu-id="cc4e7-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="cc4e7-114">-DataFactory</span></span>
<span data-ttu-id="cc4e7-115">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="cc4e7-115">The data factory object.</span></span>

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

### <span data-ttu-id="cc4e7-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cc4e7-116">-DataFactoryName</span></span>
<span data-ttu-id="cc4e7-117">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="cc4e7-117">The data factory name.</span></span>

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

### <span data-ttu-id="cc4e7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc4e7-118">-DefaultProfile</span></span>
<span data-ttu-id="cc4e7-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc4e7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc4e7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc4e7-120">-InputObject</span></span>
<span data-ttu-id="cc4e7-121">管線的 [執行識別碼]。</span><span class="sxs-lookup"><span data-stu-id="cc4e7-121">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="cc4e7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc4e7-122">-PassThru</span></span>
<span data-ttu-id="cc4e7-123">如果已指定，則在 case 操作成功時，此 Cmdlet 會寫入 true。</span><span class="sxs-lookup"><span data-stu-id="cc4e7-123">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="cc4e7-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="cc4e7-124">-PipelineRunId</span></span>
<span data-ttu-id="cc4e7-125">管線的 [執行識別碼]。</span><span class="sxs-lookup"><span data-stu-id="cc4e7-125">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="cc4e7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc4e7-126">-ResourceGroupName</span></span>
<span data-ttu-id="cc4e7-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc4e7-127">The resource group name.</span></span>

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

### <span data-ttu-id="cc4e7-128">-確認</span><span class="sxs-lookup"><span data-stu-id="cc4e7-128">-Confirm</span></span>
<span data-ttu-id="cc4e7-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cc4e7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc4e7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc4e7-130">-WhatIf</span></span>
<span data-ttu-id="cc4e7-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cc4e7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc4e7-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc4e7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc4e7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc4e7-133">CommonParameters</span></span>
<span data-ttu-id="cc4e7-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cc4e7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc4e7-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cc4e7-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc4e7-136">輸入</span><span class="sxs-lookup"><span data-stu-id="cc4e7-136">INPUTS</span></span>

### <span data-ttu-id="cc4e7-137">PSPipelineRun 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="cc4e7-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

### <span data-ttu-id="cc4e7-138">System.object</span><span class="sxs-lookup"><span data-stu-id="cc4e7-138">System.String</span></span>

### <span data-ttu-id="cc4e7-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="cc4e7-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="cc4e7-140">輸出</span><span class="sxs-lookup"><span data-stu-id="cc4e7-140">OUTPUTS</span></span>

### <span data-ttu-id="cc4e7-141">System.object</span><span class="sxs-lookup"><span data-stu-id="cc4e7-141">System.Boolean</span></span>

## <span data-ttu-id="cc4e7-142">筆記</span><span class="sxs-lookup"><span data-stu-id="cc4e7-142">NOTES</span></span>

## <span data-ttu-id="cc4e7-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc4e7-143">RELATED LINKS</span></span>
