---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
ms.openlocfilehash: a5c7ca7a651510d8b417beedc28cbd5ba26e6fe1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902606"
---
# <span data-ttu-id="76ff9-101">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="76ff9-101">Remove-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="76ff9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="76ff9-102">SYNOPSIS</span></span>
<span data-ttu-id="76ff9-103">從 Data Factory 移除資料集。</span><span class="sxs-lookup"><span data-stu-id="76ff9-103">Removes a dataset from Data Factory.</span></span>

## <span data-ttu-id="76ff9-104">語法</span><span class="sxs-lookup"><span data-stu-id="76ff9-104">SYNTAX</span></span>

### <span data-ttu-id="76ff9-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="76ff9-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76ff9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="76ff9-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76ff9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="76ff9-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76ff9-108">描述</span><span class="sxs-lookup"><span data-stu-id="76ff9-108">DESCRIPTION</span></span>
<span data-ttu-id="76ff9-109">此Remove-AzDataFactoryV2Dataset Cmdlet 會從 Azure Data Factory 移除資料集。</span><span class="sxs-lookup"><span data-stu-id="76ff9-109">The Remove-AzDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="76ff9-110">例子</span><span class="sxs-lookup"><span data-stu-id="76ff9-110">EXAMPLES</span></span>

### <span data-ttu-id="76ff9-111">範例 1：移除資料集</span><span class="sxs-lookup"><span data-stu-id="76ff9-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="76ff9-112">此命令會從名為 WikiADF 的資料工廠移除名為 DAWikiAggregatedData 的資料集。</span><span class="sxs-lookup"><span data-stu-id="76ff9-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="76ff9-113">命令會返回 $True。</span><span class="sxs-lookup"><span data-stu-id="76ff9-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="76ff9-114">參數</span><span class="sxs-lookup"><span data-stu-id="76ff9-114">PARAMETERS</span></span>

### <span data-ttu-id="76ff9-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="76ff9-115">-DataFactoryName</span></span>
<span data-ttu-id="76ff9-116">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="76ff9-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="76ff9-117">此 Cmdlet 會從此參數指定的資料工廠移除資料集。</span><span class="sxs-lookup"><span data-stu-id="76ff9-117">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="76ff9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76ff9-118">-DefaultProfile</span></span>
<span data-ttu-id="76ff9-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="76ff9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76ff9-120">-強制</span><span class="sxs-lookup"><span data-stu-id="76ff9-120">-Force</span></span>
<span data-ttu-id="76ff9-121">執行 Cmdlet 而不提示確認。</span><span class="sxs-lookup"><span data-stu-id="76ff9-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="76ff9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76ff9-122">-InputObject</span></span>
<span data-ttu-id="76ff9-123">指定要移除的資料集物件。</span><span class="sxs-lookup"><span data-stu-id="76ff9-123">Specifies a Dataset object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76ff9-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="76ff9-124">-Name</span></span>
<span data-ttu-id="76ff9-125">指定要移除的資料集名稱。</span><span class="sxs-lookup"><span data-stu-id="76ff9-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76ff9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76ff9-126">-ResourceGroupName</span></span>
<span data-ttu-id="76ff9-127">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="76ff9-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="76ff9-128">此 Cmdlet 會從此參數指定的群組移除資料集。</span><span class="sxs-lookup"><span data-stu-id="76ff9-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="76ff9-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76ff9-129">-ResourceId</span></span>
<span data-ttu-id="76ff9-130">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="76ff9-130">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76ff9-131">-確認</span><span class="sxs-lookup"><span data-stu-id="76ff9-131">-Confirm</span></span>
<span data-ttu-id="76ff9-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="76ff9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76ff9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76ff9-133">-WhatIf</span></span>
<span data-ttu-id="76ff9-134">顯示如果 Cmdlet 執行，但不執行 Cmdlet 會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="76ff9-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="76ff9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76ff9-135">CommonParameters</span></span>
<span data-ttu-id="76ff9-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="76ff9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76ff9-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="76ff9-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76ff9-138">輸入</span><span class="sxs-lookup"><span data-stu-id="76ff9-138">INPUTS</span></span>

### <span data-ttu-id="76ff9-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="76ff9-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="76ff9-140">System.String</span><span class="sxs-lookup"><span data-stu-id="76ff9-140">System.String</span></span>

## <span data-ttu-id="76ff9-141">輸出</span><span class="sxs-lookup"><span data-stu-id="76ff9-141">OUTPUTS</span></span>

### <span data-ttu-id="76ff9-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="76ff9-142">System.Void</span></span>

## <span data-ttu-id="76ff9-143">筆記</span><span class="sxs-lookup"><span data-stu-id="76ff9-143">NOTES</span></span>
<span data-ttu-id="76ff9-144">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="76ff9-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="76ff9-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="76ff9-145">RELATED LINKS</span></span>

[<span data-ttu-id="76ff9-146">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="76ff9-146">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="76ff9-147">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="76ff9-147">Set-AzDataFactoryV2Dataset</span></span>]()
