---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: BB18EEF3-570A-4667-AF0E-FCEEE17B4905
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
ms.openlocfilehash: 44db491986f42bc37df250f5949690efe874c997
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280957"
---
# <span data-ttu-id="5e9dc-101">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="5e9dc-101">Get-AzDataFactoryDataset</span></span>

## <span data-ttu-id="5e9dc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5e9dc-102">SYNOPSIS</span></span>
<span data-ttu-id="5e9dc-103">取得有關 Azure 資料工廠中的資料集的資訊。</span><span class="sxs-lookup"><span data-stu-id="5e9dc-103">Gets information about datasets in Azure Data Factory.</span></span>

## <span data-ttu-id="5e9dc-104">句法</span><span class="sxs-lookup"><span data-stu-id="5e9dc-104">SYNTAX</span></span>

### <span data-ttu-id="5e9dc-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="5e9dc-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e9dc-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5e9dc-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e9dc-107">說明</span><span class="sxs-lookup"><span data-stu-id="5e9dc-107">DESCRIPTION</span></span>
<span data-ttu-id="5e9dc-108">**AzDataFactoryDataset** Cmdlet 會取得 Azure 資料工廠中資料集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5e9dc-108">The **Get-AzDataFactoryDataset** cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="5e9dc-109">如果您指定資料集的名稱，此 Cmdlet 會取得該資料集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5e9dc-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="5e9dc-110">如果您沒有指定名稱，此 Cmdlet 會取得資料工廠中所有資料集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5e9dc-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="5e9dc-111">示例</span><span class="sxs-lookup"><span data-stu-id="5e9dc-111">EXAMPLES</span></span>

### <span data-ttu-id="5e9dc-112">範例1：取得所有資料集的相關資訊</span><span class="sxs-lookup"><span data-stu-id="5e9dc-112">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="5e9dc-113">這個命令會取得資料工廠（名為 WikiADF）中所有資料集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5e9dc-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="5e9dc-114">範例2：取得特定資料集的相關資訊</span><span class="sxs-lookup"><span data-stu-id="5e9dc-114">Example 2: Get information about a specific dataset</span></span>
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

<span data-ttu-id="5e9dc-115">這個命令會在名為 WikiADF 的資料工廠中取得名為 DAWikipediaClickEvents 的資料集相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5e9dc-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

### <span data-ttu-id="5e9dc-116">範例3：取得特定資料集的位置</span><span class="sxs-lookup"><span data-stu-id="5e9dc-116">Example 3: Get the location for a specific dataset</span></span>
```
PS C:\>(Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents").Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="5e9dc-117">這個命令會在名為 WikiADF 的資料工廠中取得名為 DAWikipediaClickEvents 的資料集資訊，然後使用標準點符號來查看與該資料集相關聯的 **位置** 。</span><span class="sxs-lookup"><span data-stu-id="5e9dc-117">This command gets information for the dataset named DAWikipediaClickEvents in the data factory named WikiADF, and then uses standard dot notation to view the **Location** associated with that dataset.</span></span>
<span data-ttu-id="5e9dc-118">或者，您也可以將 **AzDataFactoryDataset** Cmdlet 的輸出指派給某個變數，然後使用點符來查看與該變數中儲存的資料集物件相關聯的 Location 屬性。</span><span class="sxs-lookup"><span data-stu-id="5e9dc-118">Alternatively, assign the output of the **Get-AzDataFactoryDataset** cmdlet to a variable, and then use dot notation to view the Location property associated with the dataset object stored in that variable.</span></span>

## <span data-ttu-id="5e9dc-119">參數</span><span class="sxs-lookup"><span data-stu-id="5e9dc-119">PARAMETERS</span></span>

### <span data-ttu-id="5e9dc-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="5e9dc-120">-DataFactory</span></span>
<span data-ttu-id="5e9dc-121">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="5e9dc-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="5e9dc-122">這個 Cmdlet 會取得屬於此參數指定之資料工廠的資料集。</span><span class="sxs-lookup"><span data-stu-id="5e9dc-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5e9dc-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5e9dc-123">-DataFactoryName</span></span>
<span data-ttu-id="5e9dc-124">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="5e9dc-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="5e9dc-125">這個 Cmdlet 會取得屬於此參數指定之資料工廠的資料集。</span><span class="sxs-lookup"><span data-stu-id="5e9dc-125">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5e9dc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e9dc-126">-DefaultProfile</span></span>
<span data-ttu-id="5e9dc-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5e9dc-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e9dc-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="5e9dc-128">-Name</span></span>
<span data-ttu-id="5e9dc-129">指定此 Cmdlet 取得資訊的資料集名稱。</span><span class="sxs-lookup"><span data-stu-id="5e9dc-129">Specifies the name of the dataset about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="5e9dc-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e9dc-130">-ResourceGroupName</span></span>
<span data-ttu-id="5e9dc-131">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5e9dc-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5e9dc-132">這個 Cmdlet 會取得屬於此參數指定之群組的資料集。</span><span class="sxs-lookup"><span data-stu-id="5e9dc-132">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5e9dc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e9dc-133">CommonParameters</span></span>
<span data-ttu-id="5e9dc-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5e9dc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e9dc-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5e9dc-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e9dc-136">輸入</span><span class="sxs-lookup"><span data-stu-id="5e9dc-136">INPUTS</span></span>

### <span data-ttu-id="5e9dc-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="5e9dc-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="5e9dc-138">System.object</span><span class="sxs-lookup"><span data-stu-id="5e9dc-138">System.String</span></span>

## <span data-ttu-id="5e9dc-139">輸出</span><span class="sxs-lookup"><span data-stu-id="5e9dc-139">OUTPUTS</span></span>

### <span data-ttu-id="5e9dc-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="5e9dc-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="5e9dc-141">筆記</span><span class="sxs-lookup"><span data-stu-id="5e9dc-141">NOTES</span></span>
* <span data-ttu-id="5e9dc-142">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="5e9dc-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5e9dc-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e9dc-143">RELATED LINKS</span></span>

[<span data-ttu-id="5e9dc-144">新-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="5e9dc-144">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)

[<span data-ttu-id="5e9dc-145">移除-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="5e9dc-145">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)


