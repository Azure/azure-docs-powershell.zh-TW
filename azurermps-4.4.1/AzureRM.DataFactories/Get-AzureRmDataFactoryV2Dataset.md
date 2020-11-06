---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 01c2849c69cfbdd785fae092aeed63117a07b1ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447132"
---
# <span data-ttu-id="82ffc-101">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="82ffc-101">Get-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="82ffc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="82ffc-102">SYNOPSIS</span></span>
<span data-ttu-id="82ffc-103">取得資料工廠中資料集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="82ffc-103">Gets information about datasets in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82ffc-104">句法</span><span class="sxs-lookup"><span data-stu-id="82ffc-104">SYNTAX</span></span>

### <span data-ttu-id="82ffc-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="82ffc-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82ffc-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="82ffc-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82ffc-107">說明</span><span class="sxs-lookup"><span data-stu-id="82ffc-107">DESCRIPTION</span></span>
<span data-ttu-id="82ffc-108">Get-AzureRmDataFactoryV2Dataset Cmdlet 會取得 Azure 資料工廠中資料集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="82ffc-108">The Get-AzureRmDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="82ffc-109">如果您指定資料集的名稱，此 Cmdlet 會取得該資料集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="82ffc-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="82ffc-110">如果您沒有指定名稱，此 Cmdlet 會取得資料工廠中所有資料集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="82ffc-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="82ffc-111">示例</span><span class="sxs-lookup"><span data-stu-id="82ffc-111">EXAMPLES</span></span>

### <span data-ttu-id="82ffc-112">範例1：取得所有資料集的相關資訊</span><span class="sxs-lookup"><span data-stu-id="82ffc-112">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="82ffc-113">這個命令會取得資料工廠（名為 WikiADF）中所有資料集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="82ffc-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="82ffc-114">範例2：取得特定資料集的相關資訊</span><span class="sxs-lookup"><span data-stu-id="82ffc-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="82ffc-115">這個命令會在名為 WikiADF 的資料工廠中取得名為 DAWikipediaClickEvents 的資料集相關資訊。</span><span class="sxs-lookup"><span data-stu-id="82ffc-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="82ffc-116">參數</span><span class="sxs-lookup"><span data-stu-id="82ffc-116">PARAMETERS</span></span>

### <span data-ttu-id="82ffc-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="82ffc-117">-DataFactory</span></span>
<span data-ttu-id="82ffc-118">指定 PSDataFactory 物件。</span><span class="sxs-lookup"><span data-stu-id="82ffc-118">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="82ffc-119">這個 Cmdlet 會取得屬於此參數指定之資料工廠的資料集。</span><span class="sxs-lookup"><span data-stu-id="82ffc-119">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>


```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82ffc-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="82ffc-120">-DataFactoryName</span></span>
<span data-ttu-id="82ffc-121">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="82ffc-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="82ffc-122">這個 Cmdlet 會取得屬於此參數指定之資料工廠的資料集。</span><span class="sxs-lookup"><span data-stu-id="82ffc-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="82ffc-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="82ffc-123">-Name</span></span>
<span data-ttu-id="82ffc-124">指定要取得資訊之資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="82ffc-124">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ffc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82ffc-125">-ResourceGroupName</span></span>
<span data-ttu-id="82ffc-126">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="82ffc-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="82ffc-127">這個 Cmdlet 會取得屬於此參數指定之群組的資料集。</span><span class="sxs-lookup"><span data-stu-id="82ffc-127">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="82ffc-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82ffc-128">-DefaultProfile</span></span>
<span data-ttu-id="82ffc-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="82ffc-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ffc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82ffc-130">CommonParameters</span></span>
<span data-ttu-id="82ffc-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="82ffc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82ffc-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="82ffc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82ffc-133">輸入</span><span class="sxs-lookup"><span data-stu-id="82ffc-133">INPUTS</span></span>

### <span data-ttu-id="82ffc-134">System.object</span><span class="sxs-lookup"><span data-stu-id="82ffc-134">System.String</span></span>
<span data-ttu-id="82ffc-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="82ffc-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="82ffc-136">輸出</span><span class="sxs-lookup"><span data-stu-id="82ffc-136">OUTPUTS</span></span>

### <span data-ttu-id="82ffc-137">[System.object]。清單 ' 1 [Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset，DataFactoryV2，版本 = 0.1.9.0，Culture = 中性，PublicKeyToken = null）]</span><span class="sxs-lookup"><span data-stu-id="82ffc-137">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="82ffc-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="82ffc-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="82ffc-139">筆記</span><span class="sxs-lookup"><span data-stu-id="82ffc-139">NOTES</span></span>
<span data-ttu-id="82ffc-140">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="82ffc-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="82ffc-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="82ffc-141">RELATED LINKS</span></span>

[<span data-ttu-id="82ffc-142">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="82ffc-142">Set-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="82ffc-143">移除-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="82ffc-143">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
