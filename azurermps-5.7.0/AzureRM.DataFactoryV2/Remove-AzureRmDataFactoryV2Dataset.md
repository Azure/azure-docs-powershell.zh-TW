---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: faf5d80b231b93124279f3c9bb6a347f89d988d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623467"
---
# <span data-ttu-id="8558a-101">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="8558a-101">Remove-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="8558a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8558a-102">SYNOPSIS</span></span>
<span data-ttu-id="8558a-103">從資料工廠移除資料集。</span><span class="sxs-lookup"><span data-stu-id="8558a-103">Removes a dataset from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8558a-104">句法</span><span class="sxs-lookup"><span data-stu-id="8558a-104">SYNTAX</span></span>

### <span data-ttu-id="8558a-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="8558a-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8558a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8558a-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8558a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8558a-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8558a-108">說明</span><span class="sxs-lookup"><span data-stu-id="8558a-108">DESCRIPTION</span></span>
<span data-ttu-id="8558a-109">Remove-AzureRmDataFactoryV2Dataset Cmdlet 會從 Azure 資料工廠中移除資料集。</span><span class="sxs-lookup"><span data-stu-id="8558a-109">The Remove-AzureRmDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="8558a-110">示例</span><span class="sxs-lookup"><span data-stu-id="8558a-110">EXAMPLES</span></span>

### <span data-ttu-id="8558a-111">範例1：移除資料集</span><span class="sxs-lookup"><span data-stu-id="8558a-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="8558a-112">這個命令會從名為 WikiADF 的資料工廠中移除名為 DAWikiAggregatedData 的資料集。</span><span class="sxs-lookup"><span data-stu-id="8558a-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="8558a-113">命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="8558a-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="8558a-114">參數</span><span class="sxs-lookup"><span data-stu-id="8558a-114">PARAMETERS</span></span>

### <span data-ttu-id="8558a-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8558a-115">-DataFactoryName</span></span>
<span data-ttu-id="8558a-116">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="8558a-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="8558a-117">這個 Cmdlet 會從資料工廠中移除此參數指定的資料集。</span><span class="sxs-lookup"><span data-stu-id="8558a-117">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8558a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8558a-118">-DefaultProfile</span></span>
<span data-ttu-id="8558a-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8558a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8558a-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8558a-120">-Force</span></span>
<span data-ttu-id="8558a-121">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8558a-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="8558a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8558a-122">-InputObject</span></span>
<span data-ttu-id="8558a-123">指定要移除的資料集物件。</span><span class="sxs-lookup"><span data-stu-id="8558a-123">Specifies a Dataset object to remove.</span></span>

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

### <span data-ttu-id="8558a-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="8558a-124">-Name</span></span>
<span data-ttu-id="8558a-125">指定要移除的資料集名稱。</span><span class="sxs-lookup"><span data-stu-id="8558a-125">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="8558a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8558a-126">-ResourceGroupName</span></span>
<span data-ttu-id="8558a-127">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8558a-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8558a-128">這個 Cmdlet 會從這個參數指定的群組中移除資料集。</span><span class="sxs-lookup"><span data-stu-id="8558a-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8558a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8558a-129">-ResourceId</span></span>
<span data-ttu-id="8558a-130">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8558a-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="8558a-131">-確認</span><span class="sxs-lookup"><span data-stu-id="8558a-131">-Confirm</span></span>
<span data-ttu-id="8558a-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8558a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8558a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8558a-133">-WhatIf</span></span>
<span data-ttu-id="8558a-134">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8558a-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="8558a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8558a-135">CommonParameters</span></span>
<span data-ttu-id="8558a-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8558a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8558a-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8558a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8558a-138">輸入</span><span class="sxs-lookup"><span data-stu-id="8558a-138">INPUTS</span></span>

### <span data-ttu-id="8558a-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="8558a-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>
<span data-ttu-id="8558a-140">System.object</span><span class="sxs-lookup"><span data-stu-id="8558a-140">System.String</span></span>

## <span data-ttu-id="8558a-141">輸出</span><span class="sxs-lookup"><span data-stu-id="8558a-141">OUTPUTS</span></span>

### <span data-ttu-id="8558a-142">System.object</span><span class="sxs-lookup"><span data-stu-id="8558a-142">System.Object</span></span>

## <span data-ttu-id="8558a-143">筆記</span><span class="sxs-lookup"><span data-stu-id="8558a-143">NOTES</span></span>
<span data-ttu-id="8558a-144">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="8558a-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8558a-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="8558a-145">RELATED LINKS</span></span>

[<span data-ttu-id="8558a-146">AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="8558a-146">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="8558a-147">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="8558a-147">Set-AzureRmDataFactoryV2Dataset</span></span>]()
