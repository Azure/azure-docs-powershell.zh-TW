---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D853A91F-95E7-4C36-AC0F-2C10DFCF68F8
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactorypipelineactiveperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
ms.openlocfilehash: 5cbb353a0a6349842878ef787b75c1ce34b1cfd3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905154"
---
# <span data-ttu-id="2c198-101">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="2c198-101">Set-AzDataFactoryPipelineActivePeriod</span></span>

## <span data-ttu-id="2c198-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2c198-102">SYNOPSIS</span></span>
<span data-ttu-id="2c198-103">設定資料區段的活動期間。</span><span class="sxs-lookup"><span data-stu-id="2c198-103">Configures the active period for data slices.</span></span>

## <span data-ttu-id="2c198-104">語法</span><span class="sxs-lookup"><span data-stu-id="2c198-104">SYNTAX</span></span>

### <span data-ttu-id="2c198-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="2c198-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactoryName] <String>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c198-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="2c198-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactory] <PSDataFactory>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c198-107">描述</span><span class="sxs-lookup"><span data-stu-id="2c198-107">DESCRIPTION</span></span>
<span data-ttu-id="2c198-108">**Set-AzDataFactoryPipelineActivePeriod** Cmdlet 會設定 Azure Data Factory 中管線處理之資料區的活動期間。</span><span class="sxs-lookup"><span data-stu-id="2c198-108">The **Set-AzDataFactoryPipelineActivePeriod** cmdlet configures the active period for the data slices that are processed by a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="2c198-109">如果您使用 Set-AzDataFactorySliceStatus Cmdlet 來修改資料集的區段狀態，請確定該區段的開始時間和結束時間均在管線的使用期間。</span><span class="sxs-lookup"><span data-stu-id="2c198-109">If you use the Set-AzDataFactorySliceStatus cmdlet to modify the status of slices for a dataset, make sure that the start time and end time for a slice are in the active period of the pipeline.</span></span>
<span data-ttu-id="2c198-110">建立管線之後，您可以指定進行資料處理的期間。</span><span class="sxs-lookup"><span data-stu-id="2c198-110">After you create a pipeline, you can specify the period in which data processing occurs.</span></span>
<span data-ttu-id="2c198-111">指定管線的活動期間會定義根據每個 Data Factory 資料集所定義的可用性屬性處理資料區的時間長度。 </span><span class="sxs-lookup"><span data-stu-id="2c198-111">Specifying the active period for a pipeline defines the time duration in which the data slices are processed based on the **Availability** properties that were defined for each Data Factory dataset.</span></span>

## <span data-ttu-id="2c198-112">例子</span><span class="sxs-lookup"><span data-stu-id="2c198-112">EXAMPLES</span></span>

### <span data-ttu-id="2c198-113">範例 1：設定使用期間</span><span class="sxs-lookup"><span data-stu-id="2c198-113">Example 1: Configure the active period</span></span>
```
PS C:\>Set-AzDataFactoryPipelineActivePeriod -ResourceGroupName "ADF" -PipelineName "DPWikisample" -DataFactoryName "WikiADF" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-22T16:00:00Z
Confirm
Are you sure you want to set pipeline 'DPWikisample' active period from '05/21/2014 16:00:00' to
'05/22/2014 16:00:00'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="2c198-114">此命令會設定管道名為DPWikisample 程式之資料區的活動期間。</span><span class="sxs-lookup"><span data-stu-id="2c198-114">This command configures the active period for the data slices that the pipeline named DPWikisample processes.</span></span>
<span data-ttu-id="2c198-115">該命令提供資料區值的開頭和終點。</span><span class="sxs-lookup"><span data-stu-id="2c198-115">The command provides beginning and end points for the data slices as values.</span></span>
<span data-ttu-id="2c198-116">命令會返回 $True。</span><span class="sxs-lookup"><span data-stu-id="2c198-116">The command returns a value of $True.</span></span>

## <span data-ttu-id="2c198-117">參數</span><span class="sxs-lookup"><span data-stu-id="2c198-117">PARAMETERS</span></span>

### <span data-ttu-id="2c198-118">-AutoResolve</span><span class="sxs-lookup"><span data-stu-id="2c198-118">-AutoResolve</span></span>
<span data-ttu-id="2c198-119">表示此 Cmdlet 使用自動解析。</span><span class="sxs-lookup"><span data-stu-id="2c198-119">Indicates that this cmdlet uses auto resolve.</span></span>

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

### <span data-ttu-id="2c198-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="2c198-120">-DataFactory</span></span>
<span data-ttu-id="2c198-121">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="2c198-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="2c198-122">此 Cmdlet 會修改屬於此參數指定之資料工廠之管線的活動期間。</span><span class="sxs-lookup"><span data-stu-id="2c198-122">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="2c198-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2c198-123">-DataFactoryName</span></span>
<span data-ttu-id="2c198-124">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c198-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="2c198-125">此 Cmdlet 會修改屬於此參數指定之資料工廠之管線的活動期間。</span><span class="sxs-lookup"><span data-stu-id="2c198-125">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="2c198-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c198-126">-DefaultProfile</span></span>
<span data-ttu-id="2c198-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="2c198-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c198-128">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="2c198-128">-EndDateTime</span></span>
<span data-ttu-id="2c198-129">將時間週期的結尾指定為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="2c198-129">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="2c198-130">會發生資料處理，或在這一期間處理資料區。</span><span class="sxs-lookup"><span data-stu-id="2c198-130">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="2c198-131">有關 **DateTime** 物件的資訊，請鍵入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="2c198-131">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="2c198-132">*EndDateTime* 必須以 ISO8601 格式指定，如下列範例所示：2015-01-01Z 2015-01T00：00：00Z 2015-01-01T00 ：00：00.000Z (UTC) 2015-01-01T00：00：00：00-08：00 (太平洋標準時間) 預設時區設計工具為 UTC。</span><span class="sxs-lookup"><span data-stu-id="2c198-132">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c198-133">-ForceRecalculate</span><span class="sxs-lookup"><span data-stu-id="2c198-133">-ForceRecalculate</span></span>
<span data-ttu-id="2c198-134">表示此 Cmdlet 使用強制重新計算。</span><span class="sxs-lookup"><span data-stu-id="2c198-134">Indicates that this cmdlet uses force recalculate.</span></span>

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

### <span data-ttu-id="2c198-135">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="2c198-135">-PipelineName</span></span>
<span data-ttu-id="2c198-136">指定管線的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c198-136">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="2c198-137">此 Cmdlet 會設定此參數指定的管線使用期間。</span><span class="sxs-lookup"><span data-stu-id="2c198-137">This cmdlet sets the active period for the pipeline that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c198-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c198-138">-ResourceGroupName</span></span>
<span data-ttu-id="2c198-139">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c198-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="2c198-140">此 Cmdlet 會修改屬於此參數指定群組之管線的活動期間。</span><span class="sxs-lookup"><span data-stu-id="2c198-140">This cmdlet modifies the active period for a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2c198-141">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="2c198-141">-StartDateTime</span></span>
<span data-ttu-id="2c198-142">將時間週期的開始指定為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="2c198-142">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="2c198-143">會發生資料處理，或在這一期間處理資料區。</span><span class="sxs-lookup"><span data-stu-id="2c198-143">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="2c198-144">*StartDateTime* 必須以 ISO8601 格式指定。</span><span class="sxs-lookup"><span data-stu-id="2c198-144">*StartDateTime* must be specified in the ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c198-145">-確認</span><span class="sxs-lookup"><span data-stu-id="2c198-145">-Confirm</span></span>
<span data-ttu-id="2c198-146">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2c198-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c198-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c198-147">-WhatIf</span></span>
<span data-ttu-id="2c198-148">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2c198-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c198-149">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2c198-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c198-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c198-150">CommonParameters</span></span>
<span data-ttu-id="2c198-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2c198-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c198-152">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2c198-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c198-153">輸入</span><span class="sxs-lookup"><span data-stu-id="2c198-153">INPUTS</span></span>

### <span data-ttu-id="2c198-154">System.String</span><span class="sxs-lookup"><span data-stu-id="2c198-154">System.String</span></span>

### <span data-ttu-id="2c198-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2c198-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="2c198-156">輸出</span><span class="sxs-lookup"><span data-stu-id="2c198-156">OUTPUTS</span></span>

### <span data-ttu-id="2c198-157">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2c198-157">System.Boolean</span></span>

## <span data-ttu-id="2c198-158">筆記</span><span class="sxs-lookup"><span data-stu-id="2c198-158">NOTES</span></span>
* <span data-ttu-id="2c198-159">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="2c198-159">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="2c198-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c198-160">RELATED LINKS</span></span>

[<span data-ttu-id="2c198-161">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="2c198-161">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="2c198-162">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="2c198-162">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)


