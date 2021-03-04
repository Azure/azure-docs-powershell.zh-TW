---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
ms.openlocfilehash: 70673fd001078fbeff620f3a6a5ed7dc534ebe2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903273"
---
# <span data-ttu-id="ee1fd-101">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="ee1fd-101">Remove-AzDataFactoryDataset</span></span>

## <span data-ttu-id="ee1fd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ee1fd-102">SYNOPSIS</span></span>
<span data-ttu-id="ee1fd-103">從 Azure Data Factory 移除資料集。</span><span class="sxs-lookup"><span data-stu-id="ee1fd-103">Removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="ee1fd-104">語法</span><span class="sxs-lookup"><span data-stu-id="ee1fd-104">SYNTAX</span></span>

### <span data-ttu-id="ee1fd-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="ee1fd-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee1fd-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ee1fd-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee1fd-107">描述</span><span class="sxs-lookup"><span data-stu-id="ee1fd-107">DESCRIPTION</span></span>
<span data-ttu-id="ee1fd-108">**Remove-AzDataFactoryDataset** Cmdlet 會從 Azure Data Factory 移除資料集。</span><span class="sxs-lookup"><span data-stu-id="ee1fd-108">The **Remove-AzDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="ee1fd-109">例子</span><span class="sxs-lookup"><span data-stu-id="ee1fd-109">EXAMPLES</span></span>

### <span data-ttu-id="ee1fd-110">範例 1：移除資料集</span><span class="sxs-lookup"><span data-stu-id="ee1fd-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="ee1fd-111">此命令會從名為 WikiADF 的資料工廠移除名為 DAWikiAggregatedData 的資料集。</span><span class="sxs-lookup"><span data-stu-id="ee1fd-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="ee1fd-112">命令會返回 $True。</span><span class="sxs-lookup"><span data-stu-id="ee1fd-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="ee1fd-113">參數</span><span class="sxs-lookup"><span data-stu-id="ee1fd-113">PARAMETERS</span></span>

### <span data-ttu-id="ee1fd-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ee1fd-114">-DataFactory</span></span>
<span data-ttu-id="ee1fd-115">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="ee1fd-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="ee1fd-116">此 Cmdlet 會從此參數指定的資料工廠移除資料集。</span><span class="sxs-lookup"><span data-stu-id="ee1fd-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ee1fd-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ee1fd-117">-DataFactoryName</span></span>
<span data-ttu-id="ee1fd-118">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="ee1fd-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ee1fd-119">此 Cmdlet 會從此參數指定的資料工廠移除資料集。</span><span class="sxs-lookup"><span data-stu-id="ee1fd-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ee1fd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee1fd-120">-DefaultProfile</span></span>
<span data-ttu-id="ee1fd-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="ee1fd-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee1fd-122">-強制</span><span class="sxs-lookup"><span data-stu-id="ee1fd-122">-Force</span></span>
<span data-ttu-id="ee1fd-123">表示此 Cmdlet 會移除資料集，而不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ee1fd-123">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="ee1fd-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="ee1fd-124">-Name</span></span>
<span data-ttu-id="ee1fd-125">指定要移除的資料集名稱。</span><span class="sxs-lookup"><span data-stu-id="ee1fd-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1fd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee1fd-126">-ResourceGroupName</span></span>
<span data-ttu-id="ee1fd-127">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ee1fd-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ee1fd-128">此 Cmdlet 會從此參數指定的群組移除資料集。</span><span class="sxs-lookup"><span data-stu-id="ee1fd-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ee1fd-129">-確認</span><span class="sxs-lookup"><span data-stu-id="ee1fd-129">-Confirm</span></span>
<span data-ttu-id="ee1fd-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ee1fd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee1fd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee1fd-131">-WhatIf</span></span>
<span data-ttu-id="ee1fd-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ee1fd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee1fd-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ee1fd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee1fd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee1fd-134">CommonParameters</span></span>
<span data-ttu-id="ee1fd-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ee1fd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee1fd-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ee1fd-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee1fd-137">輸入</span><span class="sxs-lookup"><span data-stu-id="ee1fd-137">INPUTS</span></span>

### <span data-ttu-id="ee1fd-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ee1fd-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="ee1fd-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ee1fd-139">System.String</span></span>

## <span data-ttu-id="ee1fd-140">輸出</span><span class="sxs-lookup"><span data-stu-id="ee1fd-140">OUTPUTS</span></span>

### <span data-ttu-id="ee1fd-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="ee1fd-141">System.Void</span></span>

## <span data-ttu-id="ee1fd-142">筆記</span><span class="sxs-lookup"><span data-stu-id="ee1fd-142">NOTES</span></span>
* <span data-ttu-id="ee1fd-143">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="ee1fd-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ee1fd-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="ee1fd-144">RELATED LINKS</span></span>

[<span data-ttu-id="ee1fd-145">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="ee1fd-145">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="ee1fd-146">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="ee1fd-146">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)


