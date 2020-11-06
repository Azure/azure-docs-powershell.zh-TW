---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 77cb56c08e29bd209ccf53fcdee42545b774c650
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454403"
---
# <span data-ttu-id="fcad4-101">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="fcad4-101">Remove-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="fcad4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fcad4-102">SYNOPSIS</span></span>
<span data-ttu-id="fcad4-103">從資料工廠移除資料集。</span><span class="sxs-lookup"><span data-stu-id="fcad4-103">Removes a dataset from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcad4-104">句法</span><span class="sxs-lookup"><span data-stu-id="fcad4-104">SYNTAX</span></span>

### <span data-ttu-id="fcad4-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="fcad4-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="fcad4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fcad4-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="fcad4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fcad4-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="fcad4-108">說明</span><span class="sxs-lookup"><span data-stu-id="fcad4-108">DESCRIPTION</span></span>
<span data-ttu-id="fcad4-109">Remove-AzureRmDataFactoryV2Dataset Cmdlet 會從 Azure 資料工廠中移除資料集。</span><span class="sxs-lookup"><span data-stu-id="fcad4-109">The Remove-AzureRmDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="fcad4-110">示例</span><span class="sxs-lookup"><span data-stu-id="fcad4-110">EXAMPLES</span></span>

### <span data-ttu-id="fcad4-111">範例1：移除資料集</span><span class="sxs-lookup"><span data-stu-id="fcad4-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="fcad4-112">這個命令會從名為 WikiADF 的資料工廠中移除名為 DAWikiAggregatedData 的資料集。</span><span class="sxs-lookup"><span data-stu-id="fcad4-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="fcad4-113">命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="fcad4-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="fcad4-114">參數</span><span class="sxs-lookup"><span data-stu-id="fcad4-114">PARAMETERS</span></span>

### <span data-ttu-id="fcad4-115">-確認</span><span class="sxs-lookup"><span data-stu-id="fcad4-115">-Confirm</span></span>
<span data-ttu-id="fcad4-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fcad4-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcad4-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fcad4-117">-DataFactoryName</span></span>
<span data-ttu-id="fcad4-118">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="fcad4-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="fcad4-119">這個 Cmdlet 會從資料工廠中移除此參數指定的資料集。</span><span class="sxs-lookup"><span data-stu-id="fcad4-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fcad4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcad4-120">-InputObject</span></span>
<span data-ttu-id="fcad4-121">指定要移除的資料集物件。</span><span class="sxs-lookup"><span data-stu-id="fcad4-121">Specifies a Dataset object to remove.</span></span>

```yaml
Type: PSDataset
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fcad4-122">-Force</span><span class="sxs-lookup"><span data-stu-id="fcad4-122">-Force</span></span>
<span data-ttu-id="fcad4-123">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fcad4-123">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="fcad4-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="fcad4-124">-Name</span></span>
<span data-ttu-id="fcad4-125">指定要移除的資料集名稱。</span><span class="sxs-lookup"><span data-stu-id="fcad4-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcad4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcad4-126">-ResourceGroupName</span></span>
<span data-ttu-id="fcad4-127">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fcad4-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="fcad4-128">這個 Cmdlet 會從這個參數指定的群組中移除資料集。</span><span class="sxs-lookup"><span data-stu-id="fcad4-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fcad4-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fcad4-129">-ResourceId</span></span>
<span data-ttu-id="fcad4-130">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="fcad4-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="fcad4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcad4-131">-WhatIf</span></span>
<span data-ttu-id="fcad4-132">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fcad4-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="fcad4-133">輸入</span><span class="sxs-lookup"><span data-stu-id="fcad4-133">INPUTS</span></span>

### <span data-ttu-id="fcad4-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="fcad4-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>
<span data-ttu-id="fcad4-135">System.object</span><span class="sxs-lookup"><span data-stu-id="fcad4-135">System.String</span></span>


## <span data-ttu-id="fcad4-136">輸出</span><span class="sxs-lookup"><span data-stu-id="fcad4-136">OUTPUTS</span></span>

### <span data-ttu-id="fcad4-137">System.object</span><span class="sxs-lookup"><span data-stu-id="fcad4-137">System.Object</span></span>

## <span data-ttu-id="fcad4-138">筆記</span><span class="sxs-lookup"><span data-stu-id="fcad4-138">NOTES</span></span>
<span data-ttu-id="fcad4-139">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="fcad4-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fcad4-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="fcad4-140">RELATED LINKS</span></span>
[<span data-ttu-id="fcad4-141">AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="fcad4-141">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="fcad4-142">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="fcad4-142">Set-AzureRmDataFactoryV2Dataset</span></span>]()
