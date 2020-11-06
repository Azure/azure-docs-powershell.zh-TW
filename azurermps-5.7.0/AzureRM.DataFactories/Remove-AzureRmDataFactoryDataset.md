---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryDataset.md
ms.openlocfilehash: 35810cf1d190f9ee8ada758fbd2e52fe41ca2455
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444608"
---
# <span data-ttu-id="ff1fc-101">Remove-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="ff1fc-101">Remove-AzureRmDataFactoryDataset</span></span>

## <span data-ttu-id="ff1fc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ff1fc-102">SYNOPSIS</span></span>
<span data-ttu-id="ff1fc-103">從 Azure 資料工廠移除資料集。</span><span class="sxs-lookup"><span data-stu-id="ff1fc-103">Removes a dataset from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff1fc-104">句法</span><span class="sxs-lookup"><span data-stu-id="ff1fc-104">SYNTAX</span></span>

### <span data-ttu-id="ff1fc-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="ff1fc-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff1fc-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ff1fc-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff1fc-107">說明</span><span class="sxs-lookup"><span data-stu-id="ff1fc-107">DESCRIPTION</span></span>
<span data-ttu-id="ff1fc-108">**AzureRmDataFactoryDataset** Cmdlet 會從 Azure 資料工廠中移除資料集。</span><span class="sxs-lookup"><span data-stu-id="ff1fc-108">The **Remove-AzureRmDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="ff1fc-109">示例</span><span class="sxs-lookup"><span data-stu-id="ff1fc-109">EXAMPLES</span></span>

### <span data-ttu-id="ff1fc-110">範例1：移除資料集</span><span class="sxs-lookup"><span data-stu-id="ff1fc-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="ff1fc-111">這個命令會從名為 WikiADF 的資料工廠中移除名為 DAWikiAggregatedData 的資料集。</span><span class="sxs-lookup"><span data-stu-id="ff1fc-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="ff1fc-112">命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="ff1fc-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="ff1fc-113">參數</span><span class="sxs-lookup"><span data-stu-id="ff1fc-113">PARAMETERS</span></span>

### <span data-ttu-id="ff1fc-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ff1fc-114">-DataFactory</span></span>
<span data-ttu-id="ff1fc-115">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="ff1fc-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="ff1fc-116">這個 Cmdlet 會從資料工廠中移除此參數指定的資料集。</span><span class="sxs-lookup"><span data-stu-id="ff1fc-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff1fc-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ff1fc-117">-DataFactoryName</span></span>
<span data-ttu-id="ff1fc-118">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="ff1fc-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ff1fc-119">這個 Cmdlet 會從資料工廠中移除此參數指定的資料集。</span><span class="sxs-lookup"><span data-stu-id="ff1fc-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ff1fc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff1fc-120">-DefaultProfile</span></span>
<span data-ttu-id="ff1fc-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ff1fc-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff1fc-122">-Force</span><span class="sxs-lookup"><span data-stu-id="ff1fc-122">-Force</span></span>
<span data-ttu-id="ff1fc-123">指示此 Cmdlet 移除資料集，但不提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ff1fc-123">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="ff1fc-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="ff1fc-124">-Name</span></span>
<span data-ttu-id="ff1fc-125">指定要移除的資料集名稱。</span><span class="sxs-lookup"><span data-stu-id="ff1fc-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff1fc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff1fc-126">-ResourceGroupName</span></span>
<span data-ttu-id="ff1fc-127">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ff1fc-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ff1fc-128">這個 Cmdlet 會從這個參數指定的群組中移除資料集。</span><span class="sxs-lookup"><span data-stu-id="ff1fc-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ff1fc-129">-確認</span><span class="sxs-lookup"><span data-stu-id="ff1fc-129">-Confirm</span></span>
<span data-ttu-id="ff1fc-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ff1fc-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff1fc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff1fc-131">-WhatIf</span></span>
<span data-ttu-id="ff1fc-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ff1fc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff1fc-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ff1fc-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff1fc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff1fc-134">CommonParameters</span></span>
<span data-ttu-id="ff1fc-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ff1fc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff1fc-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ff1fc-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff1fc-137">輸入</span><span class="sxs-lookup"><span data-stu-id="ff1fc-137">INPUTS</span></span>

### <span data-ttu-id="ff1fc-138">所有</span><span class="sxs-lookup"><span data-stu-id="ff1fc-138">None</span></span>
<span data-ttu-id="ff1fc-139">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="ff1fc-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ff1fc-140">輸出</span><span class="sxs-lookup"><span data-stu-id="ff1fc-140">OUTPUTS</span></span>

### <span data-ttu-id="ff1fc-141">System.object</span><span class="sxs-lookup"><span data-stu-id="ff1fc-141">System.Boolean</span></span>

## <span data-ttu-id="ff1fc-142">筆記</span><span class="sxs-lookup"><span data-stu-id="ff1fc-142">NOTES</span></span>
* <span data-ttu-id="ff1fc-143">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="ff1fc-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ff1fc-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="ff1fc-144">RELATED LINKS</span></span>

[<span data-ttu-id="ff1fc-145">AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="ff1fc-145">Get-AzureRmDataFactoryDataset</span></span>](./Get-AzureRmDataFactoryDataset.md)

[<span data-ttu-id="ff1fc-146">新-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="ff1fc-146">New-AzureRmDataFactoryDataset</span></span>](./New-AzureRmDataFactoryDataset.md)


