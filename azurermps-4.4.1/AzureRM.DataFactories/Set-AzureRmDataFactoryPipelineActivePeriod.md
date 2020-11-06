---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: D853A91F-95E7-4C36-AC0F-2C10DFCF68F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryPipelineActivePeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryPipelineActivePeriod.md
ms.openlocfilehash: 033b787d444d8a4f97650b93f7621399648b1343
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444952"
---
# <span data-ttu-id="9ba25-101">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="9ba25-101">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>

## <span data-ttu-id="9ba25-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9ba25-102">SYNOPSIS</span></span>
<span data-ttu-id="9ba25-103">針對資料切片設定有效期間。</span><span class="sxs-lookup"><span data-stu-id="9ba25-103">Configures the active period for data slices.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ba25-104">句法</span><span class="sxs-lookup"><span data-stu-id="9ba25-104">SYNTAX</span></span>

### <span data-ttu-id="9ba25-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="9ba25-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactoryName] <String>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ba25-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9ba25-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactory] <PSDataFactory>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ba25-107">說明</span><span class="sxs-lookup"><span data-stu-id="9ba25-107">DESCRIPTION</span></span>
<span data-ttu-id="9ba25-108">AzureRmDataFactoryPipelineActivePeriod Cmdlet 會針對 Azure 資料工廠中的管道所處理的資料切片 **設定** 作用期間。</span><span class="sxs-lookup"><span data-stu-id="9ba25-108">The **Set-AzureRmDataFactoryPipelineActivePeriod** cmdlet configures the active period for the data slices that are processed by a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="9ba25-109">如果您使用 Set-AzureRmDataFactorySliceStatus Cmdlet 來修改資料集的扇面狀態，請確認該扇面的 [開始時間] 和 [結束時間] 是在管線的作用期間內。</span><span class="sxs-lookup"><span data-stu-id="9ba25-109">If you use the Set-AzureRmDataFactorySliceStatus cmdlet to modify the status of slices for a dataset, make sure that the start time and end time for a slice are in the active period of the pipeline.</span></span>

<span data-ttu-id="9ba25-110">建立管線之後，您可以指定進行資料處理的期間。</span><span class="sxs-lookup"><span data-stu-id="9ba25-110">After you create a pipeline, you can specify the period in which data processing occurs.</span></span>
<span data-ttu-id="9ba25-111">指定管線的作用期間：根據針對每個資料工廠資料集定義的 **可用性** 屬性，來定義處理資料切片的時間長度。</span><span class="sxs-lookup"><span data-stu-id="9ba25-111">Specifying the active period for a pipeline defines the time duration in which the data slices are processed based on the **Availability** properties that were defined for each Data Factory dataset.</span></span>

## <span data-ttu-id="9ba25-112">示例</span><span class="sxs-lookup"><span data-stu-id="9ba25-112">EXAMPLES</span></span>

### <span data-ttu-id="9ba25-113">範例1：設定使用期間</span><span class="sxs-lookup"><span data-stu-id="9ba25-113">Example 1: Configure the active period</span></span>
```
PS C:\>Set-AzureRmDataFactoryPipelineActivePeriod -ResourceGroupName "ADF" -PipelineName "DPWikisample" -DataFactoryName "WikiADF" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-22T16:00:00Z
Confirm
Are you sure you want to set pipeline 'DPWikisample' active period from '05/21/2014 16:00:00' to
'05/22/2014 16:00:00'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="9ba25-114">這個命令會針對名為 DPWikisample 處理的管線，為數據切片設定有效期間。</span><span class="sxs-lookup"><span data-stu-id="9ba25-114">This command configures the active period for the data slices that the pipeline named DPWikisample processes.</span></span>
<span data-ttu-id="9ba25-115">此命令提供資料切片的起點和終點作為值。</span><span class="sxs-lookup"><span data-stu-id="9ba25-115">The command provides beginning and end points for the data slices as values.</span></span>
<span data-ttu-id="9ba25-116">命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="9ba25-116">The command returns a value of $True.</span></span>

## <span data-ttu-id="9ba25-117">參數</span><span class="sxs-lookup"><span data-stu-id="9ba25-117">PARAMETERS</span></span>

### <span data-ttu-id="9ba25-118">-自動解析</span><span class="sxs-lookup"><span data-stu-id="9ba25-118">-AutoResolve</span></span>
<span data-ttu-id="9ba25-119">表示此 Cmdlet 使用自動解析。</span><span class="sxs-lookup"><span data-stu-id="9ba25-119">Indicates that this cmdlet uses auto resolve.</span></span>

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

### <span data-ttu-id="9ba25-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9ba25-120">-DataFactory</span></span>
<span data-ttu-id="9ba25-121">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="9ba25-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="9ba25-122">這個 Cmdlet 會修改屬於此參數指定之資料工廠之管線的活動期間。</span><span class="sxs-lookup"><span data-stu-id="9ba25-122">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9ba25-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9ba25-123">-DataFactoryName</span></span>
<span data-ttu-id="9ba25-124">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ba25-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9ba25-125">這個 Cmdlet 會修改屬於此參數指定之資料工廠之管線的活動期間。</span><span class="sxs-lookup"><span data-stu-id="9ba25-125">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9ba25-126">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="9ba25-126">-EndDateTime</span></span>
<span data-ttu-id="9ba25-127">將時段的結尾指定為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="9ba25-127">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="9ba25-128">進行資料處理，或在此期間處理資料切片。</span><span class="sxs-lookup"><span data-stu-id="9ba25-128">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="9ba25-129">如需 **DateTime** 物件的詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="9ba25-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="9ba25-130">*EndDateTime* 必須以 ISO8601 格式指定，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="9ba25-130">*EndDateTime* must be specified in the ISO8601 format as in the following examples:</span></span> 

<span data-ttu-id="9ba25-131">2015-01-01Z 2015-01-01T00：00： 00Z 2015-01-01T00：00： 00.000 Z (UTC) 2015-01-01T00：00： 00-08： 00 (太平洋標準時間) </span><span class="sxs-lookup"><span data-stu-id="9ba25-131">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time)</span></span>

<span data-ttu-id="9ba25-132">預設時區指示符為 UTC。</span><span class="sxs-lookup"><span data-stu-id="9ba25-132">The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="9ba25-133">-ForceRecalculate</span><span class="sxs-lookup"><span data-stu-id="9ba25-133">-ForceRecalculate</span></span>
<span data-ttu-id="9ba25-134">表示此 Cmdlet 使用強制重新計算。</span><span class="sxs-lookup"><span data-stu-id="9ba25-134">Indicates that this cmdlet uses force recalculate.</span></span>

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

### <span data-ttu-id="9ba25-135">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="9ba25-135">-PipelineName</span></span>
<span data-ttu-id="9ba25-136">指定管線的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ba25-136">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="9ba25-137">這個 Cmdlet 會設定此參數指定之管線的作用期間。</span><span class="sxs-lookup"><span data-stu-id="9ba25-137">This cmdlet sets the active period for the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="9ba25-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ba25-138">-ResourceGroupName</span></span>
<span data-ttu-id="9ba25-139">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ba25-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9ba25-140">這個 Cmdlet 會修改屬於此參數指定之群組之管線的活動期間。</span><span class="sxs-lookup"><span data-stu-id="9ba25-140">This cmdlet modifies the active period for a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9ba25-141">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="9ba25-141">-StartDateTime</span></span>
<span data-ttu-id="9ba25-142">指定時段的開頭作為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="9ba25-142">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="9ba25-143">進行資料處理，或在此期間處理資料切片。</span><span class="sxs-lookup"><span data-stu-id="9ba25-143">Data processing occurs or data slices are processed within this period.</span></span>

<span data-ttu-id="9ba25-144">*StartDateTime* 必須指定為 ISO8601 格式。</span><span class="sxs-lookup"><span data-stu-id="9ba25-144">*StartDateTime* must be specified in the ISO8601 format.</span></span>

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

### <span data-ttu-id="9ba25-145">-確認</span><span class="sxs-lookup"><span data-stu-id="9ba25-145">-Confirm</span></span>
<span data-ttu-id="9ba25-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9ba25-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ba25-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ba25-147">-WhatIf</span></span>
<span data-ttu-id="9ba25-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9ba25-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ba25-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9ba25-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ba25-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ba25-150">-DefaultProfile</span></span>
<span data-ttu-id="9ba25-151">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9ba25-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ba25-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ba25-152">CommonParameters</span></span>
<span data-ttu-id="9ba25-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9ba25-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ba25-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9ba25-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ba25-155">輸入</span><span class="sxs-lookup"><span data-stu-id="9ba25-155">INPUTS</span></span>

## <span data-ttu-id="9ba25-156">輸出</span><span class="sxs-lookup"><span data-stu-id="9ba25-156">OUTPUTS</span></span>

### <span data-ttu-id="9ba25-157">System.object</span><span class="sxs-lookup"><span data-stu-id="9ba25-157">System.Boolean</span></span>

## <span data-ttu-id="9ba25-158">筆記</span><span class="sxs-lookup"><span data-stu-id="9ba25-158">NOTES</span></span>
* <span data-ttu-id="9ba25-159">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="9ba25-159">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9ba25-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="9ba25-160">RELATED LINKS</span></span>

[<span data-ttu-id="9ba25-161">新-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="9ba25-161">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="9ba25-162">Set-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="9ba25-162">Set-AzureRmDataFactorySliceStatus</span></span>](./Set-AzureRmDataFactorySliceStatus.md)

