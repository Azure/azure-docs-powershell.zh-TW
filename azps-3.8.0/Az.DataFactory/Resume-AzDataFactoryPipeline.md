---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F522841A-4246-4028-A754-393D8DADD924
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/resume-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Resume-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Resume-AzDataFactoryPipeline.md
ms.openlocfilehash: 26b0073cafebbd3e24afae5e8265b4acc9f4b0a9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798801"
---
# <span data-ttu-id="1bb4d-101">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1bb4d-101">Resume-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="1bb4d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1bb4d-102">SYNOPSIS</span></span>
<span data-ttu-id="1bb4d-103">在資料工廠中繼續執行暫停的管線。</span><span class="sxs-lookup"><span data-stu-id="1bb4d-103">Resumes a suspended pipeline in Data Factory.</span></span>

## <span data-ttu-id="1bb4d-104">句法</span><span class="sxs-lookup"><span data-stu-id="1bb4d-104">SYNTAX</span></span>

### <span data-ttu-id="1bb4d-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="1bb4d-105">ByFactoryName (Default)</span></span>
```
Resume-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bb4d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1bb4d-106">ByFactoryObject</span></span>
```
Resume-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bb4d-107">說明</span><span class="sxs-lookup"><span data-stu-id="1bb4d-107">DESCRIPTION</span></span>
<span data-ttu-id="1bb4d-108">**Resume AzDataFactoryPipeline** Cmdlet 會在 Azure 資料工廠中繼續暫停的管線。</span><span class="sxs-lookup"><span data-stu-id="1bb4d-108">The **Resume-AzDataFactoryPipeline** cmdlet resumes a suspended pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="1bb4d-109">示例</span><span class="sxs-lookup"><span data-stu-id="1bb4d-109">EXAMPLES</span></span>

### <span data-ttu-id="1bb4d-110">範例1：繼續管線</span><span class="sxs-lookup"><span data-stu-id="1bb4d-110">Example 1: Resume a pipeline</span></span>
```
PS C:\>Resume-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to resume pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="1bb4d-111">這個命令會在名為 WikiADF 的資料工廠中，恢復名為 DPWikisample 的管道。</span><span class="sxs-lookup"><span data-stu-id="1bb4d-111">This command resumes the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="1bb4d-112">使用 **AzDataFactoryPipeline** Cmdlet 來暫停管線。</span><span class="sxs-lookup"><span data-stu-id="1bb4d-112">Use the **Suspend-AzDataFactoryPipeline** cmdlet to suspend a pipeline.</span></span>
<span data-ttu-id="1bb4d-113">命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="1bb4d-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="1bb4d-114">參數</span><span class="sxs-lookup"><span data-stu-id="1bb4d-114">PARAMETERS</span></span>

### <span data-ttu-id="1bb4d-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1bb4d-115">-DataFactory</span></span>
<span data-ttu-id="1bb4d-116">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="1bb4d-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="1bb4d-117">這個 Cmdlet 會繼續屬於此參數指定之資料工廠的管線。</span><span class="sxs-lookup"><span data-stu-id="1bb4d-117">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb4d-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1bb4d-118">-DataFactoryName</span></span>
<span data-ttu-id="1bb4d-119">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="1bb4d-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1bb4d-120">這個 Cmdlet 會繼續屬於此參數指定之資料工廠的管線。</span><span class="sxs-lookup"><span data-stu-id="1bb4d-120">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1bb4d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bb4d-121">-DefaultProfile</span></span>
<span data-ttu-id="1bb4d-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1bb4d-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1bb4d-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="1bb4d-123">-Name</span></span>
<span data-ttu-id="1bb4d-124">指定要繼續的管道名稱。</span><span class="sxs-lookup"><span data-stu-id="1bb4d-124">Specifies the name of the pipeline to resume.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb4d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bb4d-125">-ResourceGroupName</span></span>
<span data-ttu-id="1bb4d-126">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1bb4d-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1bb4d-127">這個 Cmdlet 會繼續屬於此參數指定之群組的管線。</span><span class="sxs-lookup"><span data-stu-id="1bb4d-127">This cmdlet resumes a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1bb4d-128">-確認</span><span class="sxs-lookup"><span data-stu-id="1bb4d-128">-Confirm</span></span>
<span data-ttu-id="1bb4d-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1bb4d-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb4d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bb4d-130">-WhatIf</span></span>
<span data-ttu-id="1bb4d-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1bb4d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bb4d-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1bb4d-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb4d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bb4d-133">CommonParameters</span></span>
<span data-ttu-id="1bb4d-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1bb4d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bb4d-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1bb4d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bb4d-136">輸入</span><span class="sxs-lookup"><span data-stu-id="1bb4d-136">INPUTS</span></span>

### <span data-ttu-id="1bb4d-137">System.object</span><span class="sxs-lookup"><span data-stu-id="1bb4d-137">System.String</span></span>

### <span data-ttu-id="1bb4d-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1bb4d-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="1bb4d-139">輸出</span><span class="sxs-lookup"><span data-stu-id="1bb4d-139">OUTPUTS</span></span>

### <span data-ttu-id="1bb4d-140">System.object</span><span class="sxs-lookup"><span data-stu-id="1bb4d-140">System.Boolean</span></span>

## <span data-ttu-id="1bb4d-141">筆記</span><span class="sxs-lookup"><span data-stu-id="1bb4d-141">NOTES</span></span>
* <span data-ttu-id="1bb4d-142">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="1bb4d-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1bb4d-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="1bb4d-143">RELATED LINKS</span></span>

[<span data-ttu-id="1bb4d-144">AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1bb4d-144">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="1bb4d-145">新-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1bb4d-145">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="1bb4d-146">移除-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1bb4d-146">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="1bb4d-147">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="1bb4d-147">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="1bb4d-148">暫停-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1bb4d-148">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)

