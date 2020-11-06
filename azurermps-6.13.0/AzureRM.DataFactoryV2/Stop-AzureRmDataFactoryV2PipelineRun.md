---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/stop-azurermdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2PipelineRun.md
ms.openlocfilehash: d93cd05122d0a2c321ef4ab6d858f975e84bc9a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449202"
---
# <span data-ttu-id="fe11f-101">Stop-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="fe11f-101">Stop-AzureRmDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="fe11f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe11f-102">SYNOPSIS</span></span>
<span data-ttu-id="fe11f-103">停止在資料工廠中執行 pieline。</span><span class="sxs-lookup"><span data-stu-id="fe11f-103">Stops a pieline run in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe11f-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe11f-104">SYNTAX</span></span>

### <span data-ttu-id="fe11f-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="fe11f-105">ByFactoryName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe11f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fe11f-106">ByInputObject</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe11f-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fe11f-107">ByFactoryObject</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe11f-108">說明</span><span class="sxs-lookup"><span data-stu-id="fe11f-108">DESCRIPTION</span></span>
<span data-ttu-id="fe11f-109">**AzureRmDataFactoryV2PipelineRun** Cmdlet 會停止在以 PIELINE 執行 ID 指定的資料工廠中執行管線。</span><span class="sxs-lookup"><span data-stu-id="fe11f-109">The **Stop-AzureRmDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pieline run ID.</span></span>

## <span data-ttu-id="fe11f-110">示例</span><span class="sxs-lookup"><span data-stu-id="fe11f-110">EXAMPLES</span></span>

### <span data-ttu-id="fe11f-111">範例1</span><span class="sxs-lookup"><span data-stu-id="fe11f-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="fe11f-112">這個命令會在工廠 WikiADF 中停止執行 id 為 b9730a13-aa12-4926-a8b3-8e3a974ab0bd 的管道。</span><span class="sxs-lookup"><span data-stu-id="fe11f-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="fe11f-113">參數</span><span class="sxs-lookup"><span data-stu-id="fe11f-113">PARAMETERS</span></span>

### <span data-ttu-id="fe11f-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="fe11f-114">-DataFactory</span></span>
<span data-ttu-id="fe11f-115">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="fe11f-115">The data factory object.</span></span>

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

### <span data-ttu-id="fe11f-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fe11f-116">-DataFactoryName</span></span>
<span data-ttu-id="fe11f-117">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="fe11f-117">The data factory name.</span></span>

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

### <span data-ttu-id="fe11f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe11f-118">-DefaultProfile</span></span>
<span data-ttu-id="fe11f-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe11f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe11f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe11f-120">-InputObject</span></span>
<span data-ttu-id="fe11f-121">管線的 [執行識別碼]。</span><span class="sxs-lookup"><span data-stu-id="fe11f-121">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="fe11f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe11f-122">-PassThru</span></span>
<span data-ttu-id="fe11f-123">如果已指定，則在 case 操作成功時，此 Cmdlet 會寫入 true。</span><span class="sxs-lookup"><span data-stu-id="fe11f-123">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="fe11f-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="fe11f-124">-PipelineRunId</span></span>
<span data-ttu-id="fe11f-125">管線的 [執行識別碼]。</span><span class="sxs-lookup"><span data-stu-id="fe11f-125">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="fe11f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe11f-126">-ResourceGroupName</span></span>
<span data-ttu-id="fe11f-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fe11f-127">The resource group name.</span></span>

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

### <span data-ttu-id="fe11f-128">-確認</span><span class="sxs-lookup"><span data-stu-id="fe11f-128">-Confirm</span></span>
<span data-ttu-id="fe11f-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fe11f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe11f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe11f-130">-WhatIf</span></span>
<span data-ttu-id="fe11f-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fe11f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe11f-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fe11f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe11f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe11f-133">CommonParameters</span></span>
<span data-ttu-id="fe11f-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe11f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe11f-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fe11f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe11f-136">輸入</span><span class="sxs-lookup"><span data-stu-id="fe11f-136">INPUTS</span></span>

### <span data-ttu-id="fe11f-137">PSPipelineRun 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="fe11f-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>
<span data-ttu-id="fe11f-138">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="fe11f-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="fe11f-139">System.object</span><span class="sxs-lookup"><span data-stu-id="fe11f-139">System.String</span></span>

### <span data-ttu-id="fe11f-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="fe11f-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="fe11f-141">參數： DataFactory (ByValue) </span><span class="sxs-lookup"><span data-stu-id="fe11f-141">Parameters: DataFactory (ByValue)</span></span>

## <span data-ttu-id="fe11f-142">輸出</span><span class="sxs-lookup"><span data-stu-id="fe11f-142">OUTPUTS</span></span>

### <span data-ttu-id="fe11f-143">System.object</span><span class="sxs-lookup"><span data-stu-id="fe11f-143">System.Boolean</span></span>

## <span data-ttu-id="fe11f-144">筆記</span><span class="sxs-lookup"><span data-stu-id="fe11f-144">NOTES</span></span>

## <span data-ttu-id="fe11f-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe11f-145">RELATED LINKS</span></span>
