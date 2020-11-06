---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D853A91F-95E7-4C36-AC0F-2C10DFCF68F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactorypipelineactiveperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
ms.openlocfilehash: edb2e94900d383675bd183c09df16e295828aae1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612922"
---
# <span data-ttu-id="8e538-101">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="8e538-101">Set-AzDataFactoryPipelineActivePeriod</span></span>

## <span data-ttu-id="8e538-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8e538-102">SYNOPSIS</span></span>
<span data-ttu-id="8e538-103">針對資料切片設定有效期間。</span><span class="sxs-lookup"><span data-stu-id="8e538-103">Configures the active period for data slices.</span></span>

## <span data-ttu-id="8e538-104">句法</span><span class="sxs-lookup"><span data-stu-id="8e538-104">SYNTAX</span></span>

### <span data-ttu-id="8e538-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="8e538-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactoryName] <String>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e538-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8e538-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactory] <PSDataFactory>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e538-107">說明</span><span class="sxs-lookup"><span data-stu-id="8e538-107">DESCRIPTION</span></span>
<span data-ttu-id="8e538-108">AzDataFactoryPipelineActivePeriod Cmdlet 會針對 Azure 資料工廠中的管道所處理的資料切片 **設定** 作用期間。</span><span class="sxs-lookup"><span data-stu-id="8e538-108">The **Set-AzDataFactoryPipelineActivePeriod** cmdlet configures the active period for the data slices that are processed by a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="8e538-109">如果您使用 Set-AzDataFactorySliceStatus Cmdlet 來修改資料集的扇面狀態，請確認該扇面的 [開始時間] 和 [結束時間] 是在管線的作用期間內。</span><span class="sxs-lookup"><span data-stu-id="8e538-109">If you use the Set-AzDataFactorySliceStatus cmdlet to modify the status of slices for a dataset, make sure that the start time and end time for a slice are in the active period of the pipeline.</span></span>
<span data-ttu-id="8e538-110">建立管線之後，您可以指定進行資料處理的期間。</span><span class="sxs-lookup"><span data-stu-id="8e538-110">After you create a pipeline, you can specify the period in which data processing occurs.</span></span>
<span data-ttu-id="8e538-111">指定管線的作用期間：根據針對每個資料工廠資料集定義的 **可用性** 屬性，來定義處理資料切片的時間長度。</span><span class="sxs-lookup"><span data-stu-id="8e538-111">Specifying the active period for a pipeline defines the time duration in which the data slices are processed based on the **Availability** properties that were defined for each Data Factory dataset.</span></span>

## <span data-ttu-id="8e538-112">示例</span><span class="sxs-lookup"><span data-stu-id="8e538-112">EXAMPLES</span></span>

### <span data-ttu-id="8e538-113">範例1：設定使用期間</span><span class="sxs-lookup"><span data-stu-id="8e538-113">Example 1: Configure the active period</span></span>
```
PS C:\>Set-AzDataFactoryPipelineActivePeriod -ResourceGroupName "ADF" -PipelineName "DPWikisample" -DataFactoryName "WikiADF" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-22T16:00:00Z
Confirm
Are you sure you want to set pipeline 'DPWikisample' active period from '05/21/2014 16:00:00' to
'05/22/2014 16:00:00'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="8e538-114">這個命令會針對名為 DPWikisample 處理的管線，為數據切片設定有效期間。</span><span class="sxs-lookup"><span data-stu-id="8e538-114">This command configures the active period for the data slices that the pipeline named DPWikisample processes.</span></span>
<span data-ttu-id="8e538-115">此命令提供資料切片的起點和終點作為值。</span><span class="sxs-lookup"><span data-stu-id="8e538-115">The command provides beginning and end points for the data slices as values.</span></span>
<span data-ttu-id="8e538-116">命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="8e538-116">The command returns a value of $True.</span></span>

## <span data-ttu-id="8e538-117">參數</span><span class="sxs-lookup"><span data-stu-id="8e538-117">PARAMETERS</span></span>

### <span data-ttu-id="8e538-118">-自動解析</span><span class="sxs-lookup"><span data-stu-id="8e538-118">-AutoResolve</span></span>
<span data-ttu-id="8e538-119">表示此 Cmdlet 使用自動解析。</span><span class="sxs-lookup"><span data-stu-id="8e538-119">Indicates that this cmdlet uses auto resolve.</span></span>

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

### <span data-ttu-id="8e538-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8e538-120">-DataFactory</span></span>
<span data-ttu-id="8e538-121">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="8e538-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="8e538-122">這個 Cmdlet 會修改屬於此參數指定之資料工廠之管線的活動期間。</span><span class="sxs-lookup"><span data-stu-id="8e538-122">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8e538-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8e538-123">-DataFactoryName</span></span>
<span data-ttu-id="8e538-124">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e538-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="8e538-125">這個 Cmdlet 會修改屬於此參數指定之資料工廠之管線的活動期間。</span><span class="sxs-lookup"><span data-stu-id="8e538-125">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8e538-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e538-126">-DefaultProfile</span></span>
<span data-ttu-id="8e538-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8e538-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e538-128">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="8e538-128">-EndDateTime</span></span>
<span data-ttu-id="8e538-129">將時段的結尾指定為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="8e538-129">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="8e538-130">進行資料處理，或在此期間處理資料切片。</span><span class="sxs-lookup"><span data-stu-id="8e538-130">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="8e538-131">如需 **DateTime** 物件的詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="8e538-131">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="8e538-132">*EndDateTime* 必須在 ISO8601 格式中指定，如下列範例所示： 2015-01-01Z 2015-01-01T00 .. 00： 00Z 2015-01-01T00：00： 00.000 z (UTC) 2015-01-01T00：00：00： 00 (太平洋標準時間) 預設的時區指示符是 UTC。</span><span class="sxs-lookup"><span data-stu-id="8e538-132">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="8e538-133">-ForceRecalculate</span><span class="sxs-lookup"><span data-stu-id="8e538-133">-ForceRecalculate</span></span>
<span data-ttu-id="8e538-134">表示此 Cmdlet 使用強制重新計算。</span><span class="sxs-lookup"><span data-stu-id="8e538-134">Indicates that this cmdlet uses force recalculate.</span></span>

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

### <span data-ttu-id="8e538-135">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="8e538-135">-PipelineName</span></span>
<span data-ttu-id="8e538-136">指定管線的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e538-136">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="8e538-137">這個 Cmdlet 會設定此參數指定之管線的作用期間。</span><span class="sxs-lookup"><span data-stu-id="8e538-137">This cmdlet sets the active period for the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="8e538-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e538-138">-ResourceGroupName</span></span>
<span data-ttu-id="8e538-139">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e538-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8e538-140">這個 Cmdlet 會修改屬於此參數指定之群組之管線的活動期間。</span><span class="sxs-lookup"><span data-stu-id="8e538-140">This cmdlet modifies the active period for a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8e538-141">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="8e538-141">-StartDateTime</span></span>
<span data-ttu-id="8e538-142">指定時段的開頭作為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="8e538-142">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="8e538-143">進行資料處理，或在此期間處理資料切片。</span><span class="sxs-lookup"><span data-stu-id="8e538-143">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="8e538-144">*StartDateTime* 必須指定為 ISO8601 格式。</span><span class="sxs-lookup"><span data-stu-id="8e538-144">*StartDateTime* must be specified in the ISO8601 format.</span></span>

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

### <span data-ttu-id="8e538-145">-確認</span><span class="sxs-lookup"><span data-stu-id="8e538-145">-Confirm</span></span>
<span data-ttu-id="8e538-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8e538-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e538-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e538-147">-WhatIf</span></span>
<span data-ttu-id="8e538-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8e538-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e538-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e538-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e538-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e538-150">CommonParameters</span></span>
<span data-ttu-id="8e538-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8e538-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e538-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8e538-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e538-153">輸入</span><span class="sxs-lookup"><span data-stu-id="8e538-153">INPUTS</span></span>

### <span data-ttu-id="8e538-154">System.object</span><span class="sxs-lookup"><span data-stu-id="8e538-154">System.String</span></span>

### <span data-ttu-id="8e538-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8e538-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="8e538-156">輸出</span><span class="sxs-lookup"><span data-stu-id="8e538-156">OUTPUTS</span></span>

### <span data-ttu-id="8e538-157">System.object</span><span class="sxs-lookup"><span data-stu-id="8e538-157">System.Boolean</span></span>

## <span data-ttu-id="8e538-158">筆記</span><span class="sxs-lookup"><span data-stu-id="8e538-158">NOTES</span></span>
* <span data-ttu-id="8e538-159">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="8e538-159">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8e538-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e538-160">RELATED LINKS</span></span>

[<span data-ttu-id="8e538-161">新-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="8e538-161">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="8e538-162">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="8e538-162">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)

