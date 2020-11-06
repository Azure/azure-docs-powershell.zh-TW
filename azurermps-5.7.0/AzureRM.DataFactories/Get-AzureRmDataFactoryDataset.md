---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: BB18EEF3-570A-4667-AF0E-FCEEE17B4905
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryDataset.md
ms.openlocfilehash: 10e4af67d76e6c9d367de4d9b512d003e211ddae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449914"
---
# <span data-ttu-id="8fffa-101">Get-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="8fffa-101">Get-AzureRmDataFactoryDataset</span></span>

## <span data-ttu-id="8fffa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8fffa-102">SYNOPSIS</span></span>
<span data-ttu-id="8fffa-103">取得有關 Azure 資料工廠中的資料集的資訊。</span><span class="sxs-lookup"><span data-stu-id="8fffa-103">Gets information about datasets in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fffa-104">句法</span><span class="sxs-lookup"><span data-stu-id="8fffa-104">SYNTAX</span></span>

### <span data-ttu-id="8fffa-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="8fffa-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fffa-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8fffa-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fffa-107">說明</span><span class="sxs-lookup"><span data-stu-id="8fffa-107">DESCRIPTION</span></span>
<span data-ttu-id="8fffa-108">**AzureRmDataFactoryDataset** Cmdlet 會取得 Azure 資料工廠中資料集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8fffa-108">The **Get-AzureRmDataFactoryDataset** cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="8fffa-109">如果您指定資料集的名稱，此 Cmdlet 會取得該資料集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8fffa-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="8fffa-110">如果您沒有指定名稱，此 Cmdlet 會取得資料工廠中所有資料集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8fffa-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="8fffa-111">示例</span><span class="sxs-lookup"><span data-stu-id="8fffa-111">EXAMPLES</span></span>

### <span data-ttu-id="8fffa-112">範例1：取得所有資料集的相關資訊</span><span class="sxs-lookup"><span data-stu-id="8fffa-112">Example 1: Get information about all datasets</span></span>
```
PS C:\>Get-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 
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

<span data-ttu-id="8fffa-113">這個命令會取得資料工廠（名為 WikiADF）中所有資料集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8fffa-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="8fffa-114">範例2：取得特定資料集的相關資訊</span><span class="sxs-lookup"><span data-stu-id="8fffa-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\>Get-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" 
DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="8fffa-115">這個命令會在名為 WikiADF 的資料工廠中取得名為 DAWikipediaClickEvents 的資料集相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8fffa-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

### <span data-ttu-id="8fffa-116">範例3：取得特定資料集的位置</span><span class="sxs-lookup"><span data-stu-id="8fffa-116">Example 3: Get the location for a specific dataset</span></span>
```
PS C:\>(Get-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents").Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="8fffa-117">這個命令會在名為 WikiADF 的資料工廠中取得名為 DAWikipediaClickEvents 的資料集資訊，然後使用標準點符號來查看與該資料集相關聯的 **位置** 。</span><span class="sxs-lookup"><span data-stu-id="8fffa-117">This command gets information for the dataset named DAWikipediaClickEvents in the data factory named WikiADF, and then uses standard dot notation to view the **Location** associated with that dataset.</span></span>
<span data-ttu-id="8fffa-118">或者，您也可以將 **AzureRmDataFactoryDataset** Cmdlet 的輸出指派給某個變數，然後使用點符來查看與該變數中儲存的資料集物件相關聯的 Location 屬性。</span><span class="sxs-lookup"><span data-stu-id="8fffa-118">Alternatively, assign the output of the **Get-AzureRmDataFactoryDataset** cmdlet to a variable, and then use dot notation to view the Location property associated with the dataset object stored in that variable.</span></span>

## <span data-ttu-id="8fffa-119">參數</span><span class="sxs-lookup"><span data-stu-id="8fffa-119">PARAMETERS</span></span>

### <span data-ttu-id="8fffa-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8fffa-120">-DataFactory</span></span>
<span data-ttu-id="8fffa-121">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="8fffa-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="8fffa-122">這個 Cmdlet 會取得屬於此參數指定之資料工廠的資料集。</span><span class="sxs-lookup"><span data-stu-id="8fffa-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8fffa-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8fffa-123">-DataFactoryName</span></span>
<span data-ttu-id="8fffa-124">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="8fffa-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="8fffa-125">這個 Cmdlet 會取得屬於此參數指定之資料工廠的資料集。</span><span class="sxs-lookup"><span data-stu-id="8fffa-125">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8fffa-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fffa-126">-DefaultProfile</span></span>
<span data-ttu-id="8fffa-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8fffa-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8fffa-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="8fffa-128">-Name</span></span>
<span data-ttu-id="8fffa-129">指定此 Cmdlet 取得資訊的資料集名稱。</span><span class="sxs-lookup"><span data-stu-id="8fffa-129">Specifies the name of the dataset about which this cmdlet gets information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fffa-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fffa-130">-ResourceGroupName</span></span>
<span data-ttu-id="8fffa-131">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8fffa-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8fffa-132">這個 Cmdlet 會取得屬於此參數指定之群組的資料集。</span><span class="sxs-lookup"><span data-stu-id="8fffa-132">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8fffa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fffa-133">CommonParameters</span></span>
<span data-ttu-id="8fffa-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8fffa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fffa-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8fffa-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fffa-136">輸入</span><span class="sxs-lookup"><span data-stu-id="8fffa-136">INPUTS</span></span>

### <span data-ttu-id="8fffa-137">所有</span><span class="sxs-lookup"><span data-stu-id="8fffa-137">None</span></span>
<span data-ttu-id="8fffa-138">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="8fffa-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8fffa-139">輸出</span><span class="sxs-lookup"><span data-stu-id="8fffa-139">OUTPUTS</span></span>

### <span data-ttu-id="8fffa-140">[System.object]。清單 ' 1 [Microsoft.WindowsAzure.Commands.Utilities.PSDataset，WindowsAzure. 實用程式，版本 = 0.8.2.0，Culture = 中性，PublicKeyToken = 31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataset</span><span class="sxs-lookup"><span data-stu-id="8fffa-140">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataset, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataset</span></span>

## <span data-ttu-id="8fffa-141">筆記</span><span class="sxs-lookup"><span data-stu-id="8fffa-141">NOTES</span></span>
* <span data-ttu-id="8fffa-142">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="8fffa-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8fffa-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="8fffa-143">RELATED LINKS</span></span>

[<span data-ttu-id="8fffa-144">新-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="8fffa-144">New-AzureRmDataFactoryDataset</span></span>](./New-AzureRmDataFactoryDataset.md)

[<span data-ttu-id="8fffa-145">移除-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="8fffa-145">Remove-AzureRmDataFactoryDataset</span></span>](./Remove-AzureRmDataFactoryDataset.md)


