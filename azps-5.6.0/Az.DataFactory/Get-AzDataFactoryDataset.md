---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: BB18EEF3-570A-4667-AF0E-FCEEE17B4905
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
ms.openlocfilehash: c31a8bb3ef09eb190a7a4c77aef0c44fadbf8960
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912422"
---
# <span data-ttu-id="95832-101">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="95832-101">Get-AzDataFactoryDataset</span></span>

## <span data-ttu-id="95832-102">簡介</span><span class="sxs-lookup"><span data-stu-id="95832-102">SYNOPSIS</span></span>
<span data-ttu-id="95832-103">在 Azure Data Factory 中收集資料集相關資訊。</span><span class="sxs-lookup"><span data-stu-id="95832-103">Gets information about datasets in Azure Data Factory.</span></span>

## <span data-ttu-id="95832-104">語法</span><span class="sxs-lookup"><span data-stu-id="95832-104">SYNTAX</span></span>

### <span data-ttu-id="95832-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="95832-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95832-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="95832-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95832-107">描述</span><span class="sxs-lookup"><span data-stu-id="95832-107">DESCRIPTION</span></span>
<span data-ttu-id="95832-108">**Get-AzDataFactoryDataset** Cmdlet 會取得 Azure Data Factory 中資料集的資訊。</span><span class="sxs-lookup"><span data-stu-id="95832-108">The **Get-AzDataFactoryDataset** cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="95832-109">如果您指定資料集的名稱，此 Cmdlet 會獲得該資料集的資訊。</span><span class="sxs-lookup"><span data-stu-id="95832-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="95832-110">如果您未指定名稱，此 Cmdlet 會獲得資料工廠中所有資料集的資訊。</span><span class="sxs-lookup"><span data-stu-id="95832-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="95832-111">例子</span><span class="sxs-lookup"><span data-stu-id="95832-111">EXAMPLES</span></span>

### <span data-ttu-id="95832-112">範例 1：取得所有資料集的資訊</span><span class="sxs-lookup"><span data-stu-id="95832-112">Example 1: Get information about all datasets</span></span>
```
PS C:\>Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 
DatasetName       : DACuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}

DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}

DatasetName         : DAWikiAggregatedData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}
```

<span data-ttu-id="95832-113">此命令會獲得名稱為 WikiADF 的資料工廠中所有資料集的資訊。</span><span class="sxs-lookup"><span data-stu-id="95832-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="95832-114">範例 2：取得特定資料集的資訊</span><span class="sxs-lookup"><span data-stu-id="95832-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\>Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" 
DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="95832-115">此命令會從名為 WikiADF 的資料工廠中，獲得名為 DAWikipediaClickEvents 的資料集相關資訊。</span><span class="sxs-lookup"><span data-stu-id="95832-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

### <span data-ttu-id="95832-116">範例 3：取得特定資料集的位置</span><span class="sxs-lookup"><span data-stu-id="95832-116">Example 3: Get the location for a specific dataset</span></span>
```
PS C:\>(Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents").Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="95832-117">此命令會獲得資料工廠中名為 DAWikipediaClickEvents 之資料集的資訊，然後使用標準點標記法來查看與該資料集相關聯的位置。 </span><span class="sxs-lookup"><span data-stu-id="95832-117">This command gets information for the dataset named DAWikipediaClickEvents in the data factory named WikiADF, and then uses standard dot notation to view the **Location** associated with that dataset.</span></span>
<span data-ttu-id="95832-118">或者，將 **Get-AzDataFactoryDataset** Cmdlet 的輸出指派給變數，然後使用點標記法來查看與儲存在該變數中之資料集物件相關聯的 Location 屬性。</span><span class="sxs-lookup"><span data-stu-id="95832-118">Alternatively, assign the output of the **Get-AzDataFactoryDataset** cmdlet to a variable, and then use dot notation to view the Location property associated with the dataset object stored in that variable.</span></span>

## <span data-ttu-id="95832-119">參數</span><span class="sxs-lookup"><span data-stu-id="95832-119">PARAMETERS</span></span>

### <span data-ttu-id="95832-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="95832-120">-DataFactory</span></span>
<span data-ttu-id="95832-121">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="95832-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="95832-122">此 Cmdlet 會獲得屬於此參數指定之資料工廠的資料集。</span><span class="sxs-lookup"><span data-stu-id="95832-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="95832-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="95832-123">-DataFactoryName</span></span>
<span data-ttu-id="95832-124">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="95832-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="95832-125">此 Cmdlet 會獲得屬於此參數指定之資料工廠的資料集。</span><span class="sxs-lookup"><span data-stu-id="95832-125">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="95832-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95832-126">-DefaultProfile</span></span>
<span data-ttu-id="95832-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="95832-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95832-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="95832-128">-Name</span></span>
<span data-ttu-id="95832-129">指定此 Cmdlet 會獲得相關資訊的資料集名稱。</span><span class="sxs-lookup"><span data-stu-id="95832-129">Specifies the name of the dataset about which this cmdlet gets information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95832-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95832-130">-ResourceGroupName</span></span>
<span data-ttu-id="95832-131">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="95832-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="95832-132">此 Cmdlet 會獲得屬於此參數指定之群組的資料集。</span><span class="sxs-lookup"><span data-stu-id="95832-132">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="95832-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95832-133">CommonParameters</span></span>
<span data-ttu-id="95832-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="95832-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95832-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="95832-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95832-136">輸入</span><span class="sxs-lookup"><span data-stu-id="95832-136">INPUTS</span></span>

### <span data-ttu-id="95832-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="95832-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="95832-138">System.String</span><span class="sxs-lookup"><span data-stu-id="95832-138">System.String</span></span>

## <span data-ttu-id="95832-139">輸出</span><span class="sxs-lookup"><span data-stu-id="95832-139">OUTPUTS</span></span>

### <span data-ttu-id="95832-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="95832-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="95832-141">筆記</span><span class="sxs-lookup"><span data-stu-id="95832-141">NOTES</span></span>
* <span data-ttu-id="95832-142">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="95832-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="95832-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="95832-143">RELATED LINKS</span></span>

[<span data-ttu-id="95832-144">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="95832-144">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)

[<span data-ttu-id="95832-145">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="95832-145">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)


