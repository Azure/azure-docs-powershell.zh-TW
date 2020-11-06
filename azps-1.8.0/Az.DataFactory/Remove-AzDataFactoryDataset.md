---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
ms.openlocfilehash: ac17206073ff9992c8569da884d1d53c385bccbf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622580"
---
# <span data-ttu-id="88b66-101">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="88b66-101">Remove-AzDataFactoryDataset</span></span>

## <span data-ttu-id="88b66-102">摘要</span><span class="sxs-lookup"><span data-stu-id="88b66-102">SYNOPSIS</span></span>
<span data-ttu-id="88b66-103">從 Azure 資料工廠移除資料集。</span><span class="sxs-lookup"><span data-stu-id="88b66-103">Removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="88b66-104">句法</span><span class="sxs-lookup"><span data-stu-id="88b66-104">SYNTAX</span></span>

### <span data-ttu-id="88b66-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="88b66-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88b66-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="88b66-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88b66-107">說明</span><span class="sxs-lookup"><span data-stu-id="88b66-107">DESCRIPTION</span></span>
<span data-ttu-id="88b66-108">**AzDataFactoryDataset** Cmdlet 會從 Azure 資料工廠中移除資料集。</span><span class="sxs-lookup"><span data-stu-id="88b66-108">The **Remove-AzDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="88b66-109">示例</span><span class="sxs-lookup"><span data-stu-id="88b66-109">EXAMPLES</span></span>

### <span data-ttu-id="88b66-110">範例1：移除資料集</span><span class="sxs-lookup"><span data-stu-id="88b66-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="88b66-111">這個命令會從名為 WikiADF 的資料工廠中移除名為 DAWikiAggregatedData 的資料集。</span><span class="sxs-lookup"><span data-stu-id="88b66-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="88b66-112">命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="88b66-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="88b66-113">參數</span><span class="sxs-lookup"><span data-stu-id="88b66-113">PARAMETERS</span></span>

### <span data-ttu-id="88b66-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="88b66-114">-DataFactory</span></span>
<span data-ttu-id="88b66-115">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="88b66-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="88b66-116">這個 Cmdlet 會從資料工廠中移除此參數指定的資料集。</span><span class="sxs-lookup"><span data-stu-id="88b66-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="88b66-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="88b66-117">-DataFactoryName</span></span>
<span data-ttu-id="88b66-118">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="88b66-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="88b66-119">這個 Cmdlet 會從資料工廠中移除此參數指定的資料集。</span><span class="sxs-lookup"><span data-stu-id="88b66-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="88b66-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88b66-120">-DefaultProfile</span></span>
<span data-ttu-id="88b66-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="88b66-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88b66-122">-Force</span><span class="sxs-lookup"><span data-stu-id="88b66-122">-Force</span></span>
<span data-ttu-id="88b66-123">指示此 Cmdlet 移除資料集，但不提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="88b66-123">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="88b66-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="88b66-124">-Name</span></span>
<span data-ttu-id="88b66-125">指定要移除的資料集名稱。</span><span class="sxs-lookup"><span data-stu-id="88b66-125">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="88b66-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88b66-126">-ResourceGroupName</span></span>
<span data-ttu-id="88b66-127">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="88b66-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="88b66-128">這個 Cmdlet 會從這個參數指定的群組中移除資料集。</span><span class="sxs-lookup"><span data-stu-id="88b66-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="88b66-129">-確認</span><span class="sxs-lookup"><span data-stu-id="88b66-129">-Confirm</span></span>
<span data-ttu-id="88b66-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="88b66-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88b66-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88b66-131">-WhatIf</span></span>
<span data-ttu-id="88b66-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="88b66-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88b66-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="88b66-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88b66-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88b66-134">CommonParameters</span></span>
<span data-ttu-id="88b66-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="88b66-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88b66-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="88b66-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88b66-137">輸入</span><span class="sxs-lookup"><span data-stu-id="88b66-137">INPUTS</span></span>

### <span data-ttu-id="88b66-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="88b66-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="88b66-139">System.object</span><span class="sxs-lookup"><span data-stu-id="88b66-139">System.String</span></span>

## <span data-ttu-id="88b66-140">輸出</span><span class="sxs-lookup"><span data-stu-id="88b66-140">OUTPUTS</span></span>

### <span data-ttu-id="88b66-141">System.void</span><span class="sxs-lookup"><span data-stu-id="88b66-141">System.Void</span></span>

## <span data-ttu-id="88b66-142">筆記</span><span class="sxs-lookup"><span data-stu-id="88b66-142">NOTES</span></span>
* <span data-ttu-id="88b66-143">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="88b66-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="88b66-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="88b66-144">RELATED LINKS</span></span>

[<span data-ttu-id="88b66-145">AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="88b66-145">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="88b66-146">新-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="88b66-146">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)


