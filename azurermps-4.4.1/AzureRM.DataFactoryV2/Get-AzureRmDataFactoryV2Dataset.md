---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
gitcommit: https://github.com/Azure/azure-powershell/blob/c396953644d237789e0f4e1f726b553913186d34
ms.openlocfilehash: ec66f865c4a511935599b81b672cd60d6da78485
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456759"
---
# <span data-ttu-id="7d680-101">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="7d680-101">Get-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="7d680-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d680-102">SYNOPSIS</span></span>
<span data-ttu-id="7d680-103">取得資料工廠中資料集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7d680-103">Gets information about datasets in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d680-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d680-104">SYNTAX</span></span>

### <span data-ttu-id="7d680-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="7d680-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="7d680-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7d680-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="7d680-107">說明</span><span class="sxs-lookup"><span data-stu-id="7d680-107">DESCRIPTION</span></span>
<span data-ttu-id="7d680-108">Get-AzureRmDataFactoryV2Dataset Cmdlet 會取得 Azure 資料工廠中資料集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7d680-108">The Get-AzureRmDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="7d680-109">如果您指定資料集的名稱，此 Cmdlet 會取得該資料集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7d680-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="7d680-110">如果您沒有指定名稱，此 Cmdlet 會取得資料工廠中所有資料集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7d680-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="7d680-111">示例</span><span class="sxs-lookup"><span data-stu-id="7d680-111">EXAMPLES</span></span>

### <span data-ttu-id="7d680-112">範例1：取得所有資料集的相關資訊</span><span class="sxs-lookup"><span data-stu-id="7d680-112">Example 1: Get information about all datasets</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

    DatasetName       : DACuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

    DatasetName       : DAWikiAggregatedData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

```

<span data-ttu-id="7d680-113">這個命令會取得資料工廠（名為 WikiADF）中所有資料集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7d680-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="7d680-114">範例2：取得特定資料集的相關資訊</span><span class="sxs-lookup"><span data-stu-id="7d680-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

```

<span data-ttu-id="7d680-115">這個命令會在名為 WikiADF 的資料工廠中取得名為 DAWikipediaClickEvents 的資料集相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7d680-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="7d680-116">參數</span><span class="sxs-lookup"><span data-stu-id="7d680-116">PARAMETERS</span></span>

### <span data-ttu-id="7d680-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="7d680-117">-DataFactory</span></span>
<span data-ttu-id="7d680-118">指定 PSDataFactory 物件。</span><span class="sxs-lookup"><span data-stu-id="7d680-118">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="7d680-119">這個 Cmdlet 會取得屬於此參數指定之資料工廠的資料集。</span><span class="sxs-lookup"><span data-stu-id="7d680-119">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>


```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d680-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7d680-120">-DataFactoryName</span></span>
<span data-ttu-id="7d680-121">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="7d680-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="7d680-122">這個 Cmdlet 會取得屬於此參數指定之資料工廠的資料集。</span><span class="sxs-lookup"><span data-stu-id="7d680-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7d680-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="7d680-123">-Name</span></span>
<span data-ttu-id="7d680-124">指定要取得資訊之資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="7d680-124">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d680-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d680-125">-ResourceGroupName</span></span>
<span data-ttu-id="7d680-126">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7d680-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7d680-127">這個 Cmdlet 會取得屬於此參數指定之群組的資料集。</span><span class="sxs-lookup"><span data-stu-id="7d680-127">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

## <span data-ttu-id="7d680-128">輸入</span><span class="sxs-lookup"><span data-stu-id="7d680-128">INPUTS</span></span>

### <span data-ttu-id="7d680-129">System.object</span><span class="sxs-lookup"><span data-stu-id="7d680-129">System.String</span></span>
<span data-ttu-id="7d680-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="7d680-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="7d680-131">輸出</span><span class="sxs-lookup"><span data-stu-id="7d680-131">OUTPUTS</span></span>

### <span data-ttu-id="7d680-132">[System.object]。清單 ' 1 [Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset，DataFactoryV2，版本 = 0.1.9.0，Culture = 中性，PublicKeyToken = null）]</span><span class="sxs-lookup"><span data-stu-id="7d680-132">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="7d680-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="7d680-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>


## <span data-ttu-id="7d680-134">筆記</span><span class="sxs-lookup"><span data-stu-id="7d680-134">NOTES</span></span>
<span data-ttu-id="7d680-135">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="7d680-135">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7d680-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d680-136">RELATED LINKS</span></span>
[<span data-ttu-id="7d680-137">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="7d680-137">Set-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="7d680-138">移除-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="7d680-138">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
