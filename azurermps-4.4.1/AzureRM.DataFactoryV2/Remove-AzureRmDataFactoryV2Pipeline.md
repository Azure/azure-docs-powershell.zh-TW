---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: cc43b2982ff2269a1e0e72da065a806895cc798e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457639"
---
# <span data-ttu-id="88021-101">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="88021-101">Remove-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="88021-102">摘要</span><span class="sxs-lookup"><span data-stu-id="88021-102">SYNOPSIS</span></span>
<span data-ttu-id="88021-103">從資料工廠移除管線。</span><span class="sxs-lookup"><span data-stu-id="88021-103">Removes a pipeline from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88021-104">句法</span><span class="sxs-lookup"><span data-stu-id="88021-104">SYNTAX</span></span>

### <span data-ttu-id="88021-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="88021-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="88021-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="88021-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="88021-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="88021-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="88021-108">說明</span><span class="sxs-lookup"><span data-stu-id="88021-108">DESCRIPTION</span></span>
<span data-ttu-id="88021-109">Remove-AzureRmDataFactoryV2Pipeline Cmdlet 會從 Azure 資料工廠中移除管線。</span><span class="sxs-lookup"><span data-stu-id="88021-109">The Remove-AzureRmDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="88021-110">示例</span><span class="sxs-lookup"><span data-stu-id="88021-110">EXAMPLES</span></span>

### <span data-ttu-id="88021-111">範例1：移除管線</span><span class="sxs-lookup"><span data-stu-id="88021-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="88021-112">這個 Cmdlet 會從資料工廠（名為 WikiADF）移除名為 DPWikisample 的管線。</span><span class="sxs-lookup"><span data-stu-id="88021-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="88021-113">命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="88021-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="88021-114">參數</span><span class="sxs-lookup"><span data-stu-id="88021-114">PARAMETERS</span></span>

### <span data-ttu-id="88021-115">-確認</span><span class="sxs-lookup"><span data-stu-id="88021-115">-Confirm</span></span>
<span data-ttu-id="88021-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="88021-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88021-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="88021-117">-DataFactoryName</span></span>
<span data-ttu-id="88021-118">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="88021-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="88021-119">這個 Cmdlet 會從資料工廠中移除此參數指定的管線。</span><span class="sxs-lookup"><span data-stu-id="88021-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88021-120">-Force</span><span class="sxs-lookup"><span data-stu-id="88021-120">-Force</span></span>
<span data-ttu-id="88021-121">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="88021-121">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88021-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="88021-122">-Name</span></span>
<span data-ttu-id="88021-123">指定要移除的管線名稱。</span><span class="sxs-lookup"><span data-stu-id="88021-123">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88021-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88021-124">-InputObject</span></span>
<span data-ttu-id="88021-125">指定管線物件。</span><span class="sxs-lookup"><span data-stu-id="88021-125">Specifies a Pipeline object.</span></span>
<span data-ttu-id="88021-126">這個 Cmdlet 會移除此參數指定的管線。</span><span class="sxs-lookup"><span data-stu-id="88021-126">This cmdlet removes the pipeline that this parameter specifies.</span></span>

```yaml
Type: PSPipeline
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88021-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88021-127">-ResourceGroupName</span></span>
<span data-ttu-id="88021-128">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="88021-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="88021-129">這個 Cmdlet 會從群組中移除此參數指定的管線。</span><span class="sxs-lookup"><span data-stu-id="88021-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88021-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88021-130">-ResourceId</span></span>
<span data-ttu-id="88021-131">要移除之管線的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="88021-131">The Azure resource ID of the pipeline to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88021-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88021-132">-WhatIf</span></span>
<span data-ttu-id="88021-133">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="88021-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="88021-134">輸入</span><span class="sxs-lookup"><span data-stu-id="88021-134">INPUTS</span></span>

### <span data-ttu-id="88021-135">PSPipeline 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="88021-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="88021-136">System.object</span><span class="sxs-lookup"><span data-stu-id="88021-136">System.String</span></span>


## <span data-ttu-id="88021-137">輸出</span><span class="sxs-lookup"><span data-stu-id="88021-137">OUTPUTS</span></span>

### <span data-ttu-id="88021-138">System.object</span><span class="sxs-lookup"><span data-stu-id="88021-138">System.Object</span></span>

## <span data-ttu-id="88021-139">筆記</span><span class="sxs-lookup"><span data-stu-id="88021-139">NOTES</span></span>
<span data-ttu-id="88021-140">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="88021-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="88021-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="88021-141">RELATED LINKS</span></span>
[<span data-ttu-id="88021-142">AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="88021-142">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="88021-143">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="88021-143">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="88021-144">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="88021-144">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

