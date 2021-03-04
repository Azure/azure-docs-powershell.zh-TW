---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: https://docs.microsoft.com/powershell/module/az.datafactory/suspend-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
ms.openlocfilehash: 7b909669ecec054ac4cbef13c5babf7e5cdcdb08
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914037"
---
# <span data-ttu-id="fbe74-101">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="fbe74-101">Suspend-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="fbe74-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fbe74-102">SYNOPSIS</span></span>
<span data-ttu-id="fbe74-103">在 Azure Data Factory 中暫停管線。</span><span class="sxs-lookup"><span data-stu-id="fbe74-103">Suspends a pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="fbe74-104">語法</span><span class="sxs-lookup"><span data-stu-id="fbe74-104">SYNTAX</span></span>

### <span data-ttu-id="fbe74-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="fbe74-105">ByFactoryName (Default)</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbe74-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fbe74-106">ByFactoryObject</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbe74-107">描述</span><span class="sxs-lookup"><span data-stu-id="fbe74-107">DESCRIPTION</span></span>
<span data-ttu-id="fbe74-108">**Suspend-AzDataFactoryPipeline** Cmdlet 會暫停 Azure Data Factory 中的管線。</span><span class="sxs-lookup"><span data-stu-id="fbe74-108">The **Suspend-AzDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="fbe74-109">您可以使用 Cmdlet 繼續Resume-AzDataFactoryPipeline管道。</span><span class="sxs-lookup"><span data-stu-id="fbe74-109">You can resume the pipeline by using the Resume-AzDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="fbe74-110">例子</span><span class="sxs-lookup"><span data-stu-id="fbe74-110">EXAMPLES</span></span>

### <span data-ttu-id="fbe74-111">範例 1：暫停管線</span><span class="sxs-lookup"><span data-stu-id="fbe74-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="fbe74-112">此命令會暫停名為 WIKIADF 的資料工廠中名為DPWikiSample 的管線。</span><span class="sxs-lookup"><span data-stu-id="fbe74-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="fbe74-113">命令會返回 $True。</span><span class="sxs-lookup"><span data-stu-id="fbe74-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="fbe74-114">參數</span><span class="sxs-lookup"><span data-stu-id="fbe74-114">PARAMETERS</span></span>

### <span data-ttu-id="fbe74-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="fbe74-115">-DataFactory</span></span>
<span data-ttu-id="fbe74-116">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="fbe74-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="fbe74-117">此 Cmdlet 會暫停屬於此參數指定之資料工廠的管線。</span><span class="sxs-lookup"><span data-stu-id="fbe74-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fbe74-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fbe74-118">-DataFactoryName</span></span>
<span data-ttu-id="fbe74-119">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="fbe74-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="fbe74-120">此 Cmdlet 會暫停屬於此參數指定之資料工廠的管線。</span><span class="sxs-lookup"><span data-stu-id="fbe74-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fbe74-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbe74-121">-DefaultProfile</span></span>
<span data-ttu-id="fbe74-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="fbe74-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbe74-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="fbe74-123">-Name</span></span>
<span data-ttu-id="fbe74-124">指定要暫停的管線名稱。</span><span class="sxs-lookup"><span data-stu-id="fbe74-124">Specifies the name of the pipeline to suspend.</span></span>

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

### <span data-ttu-id="fbe74-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbe74-125">-ResourceGroupName</span></span>
<span data-ttu-id="fbe74-126">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fbe74-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="fbe74-127">此 Cmdlet 會暫停屬於此參數指定之群組的管線。</span><span class="sxs-lookup"><span data-stu-id="fbe74-127">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fbe74-128">-確認</span><span class="sxs-lookup"><span data-stu-id="fbe74-128">-Confirm</span></span>
<span data-ttu-id="fbe74-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fbe74-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbe74-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbe74-130">-WhatIf</span></span>
<span data-ttu-id="fbe74-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fbe74-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbe74-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fbe74-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbe74-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbe74-133">CommonParameters</span></span>
<span data-ttu-id="fbe74-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fbe74-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbe74-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="fbe74-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbe74-136">輸入</span><span class="sxs-lookup"><span data-stu-id="fbe74-136">INPUTS</span></span>

### <span data-ttu-id="fbe74-137">System.String</span><span class="sxs-lookup"><span data-stu-id="fbe74-137">System.String</span></span>

### <span data-ttu-id="fbe74-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="fbe74-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="fbe74-139">輸出</span><span class="sxs-lookup"><span data-stu-id="fbe74-139">OUTPUTS</span></span>

### <span data-ttu-id="fbe74-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fbe74-140">System.Boolean</span></span>

## <span data-ttu-id="fbe74-141">筆記</span><span class="sxs-lookup"><span data-stu-id="fbe74-141">NOTES</span></span>
* <span data-ttu-id="fbe74-142">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="fbe74-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fbe74-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="fbe74-143">RELATED LINKS</span></span>

[<span data-ttu-id="fbe74-144">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="fbe74-144">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="fbe74-145">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="fbe74-145">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="fbe74-146">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="fbe74-146">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="fbe74-147">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="fbe74-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="fbe74-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="fbe74-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


