---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 2479336e2c646f82b6868ee2382af508d0404a59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449214"
---
# <span data-ttu-id="7c88b-101">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="7c88b-101">Get-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="7c88b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7c88b-102">SYNOPSIS</span></span>
<span data-ttu-id="7c88b-103">取得資料工廠中資料集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7c88b-103">Gets information about datasets in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c88b-104">句法</span><span class="sxs-lookup"><span data-stu-id="7c88b-104">SYNTAX</span></span>

### <span data-ttu-id="7c88b-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="7c88b-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c88b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7c88b-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c88b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7c88b-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2Dataset [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c88b-108">說明</span><span class="sxs-lookup"><span data-stu-id="7c88b-108">DESCRIPTION</span></span>
<span data-ttu-id="7c88b-109">Get-AzureRmDataFactoryV2Dataset Cmdlet 會取得 Azure 資料工廠中資料集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7c88b-109">The Get-AzureRmDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="7c88b-110">如果您指定資料集的名稱，此 Cmdlet 會取得該資料集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7c88b-110">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="7c88b-111">如果您沒有指定名稱，此 Cmdlet 會取得資料工廠中所有資料集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7c88b-111">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="7c88b-112">示例</span><span class="sxs-lookup"><span data-stu-id="7c88b-112">EXAMPLES</span></span>

### <span data-ttu-id="7c88b-113">範例1：取得所有資料集的相關資訊</span><span class="sxs-lookup"><span data-stu-id="7c88b-113">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="7c88b-114">這個命令會取得資料工廠（名為 WikiADF）中所有資料集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7c88b-114">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="7c88b-115">範例2：取得特定資料集的相關資訊</span><span class="sxs-lookup"><span data-stu-id="7c88b-115">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="7c88b-116">這個命令會在名為 WikiADF 的資料工廠中取得名為 DAWikipediaClickEvents 的資料集相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7c88b-116">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="7c88b-117">參數</span><span class="sxs-lookup"><span data-stu-id="7c88b-117">PARAMETERS</span></span>

### <span data-ttu-id="7c88b-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="7c88b-118">-DataFactory</span></span>
<span data-ttu-id="7c88b-119">指定 PSDataFactory 物件。</span><span class="sxs-lookup"><span data-stu-id="7c88b-119">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="7c88b-120">這個 Cmdlet 會取得屬於此參數指定之資料工廠的資料集。</span><span class="sxs-lookup"><span data-stu-id="7c88b-120">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7c88b-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7c88b-121">-DataFactoryName</span></span>
<span data-ttu-id="7c88b-122">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c88b-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="7c88b-123">這個 Cmdlet 會取得屬於此參數指定之資料工廠的資料集。</span><span class="sxs-lookup"><span data-stu-id="7c88b-123">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7c88b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c88b-124">-DefaultProfile</span></span>
<span data-ttu-id="7c88b-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7c88b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c88b-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="7c88b-126">-Name</span></span>
<span data-ttu-id="7c88b-127">指定要取得資訊之資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c88b-127">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c88b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c88b-128">-ResourceGroupName</span></span>
<span data-ttu-id="7c88b-129">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c88b-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7c88b-130">這個 Cmdlet 會取得屬於此參數指定之群組的資料集。</span><span class="sxs-lookup"><span data-stu-id="7c88b-130">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7c88b-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c88b-131">-ResourceId</span></span>
<span data-ttu-id="7c88b-132">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7c88b-132">The Azure resource ID.</span></span>

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

### <span data-ttu-id="7c88b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c88b-133">CommonParameters</span></span>
<span data-ttu-id="7c88b-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7c88b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c88b-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7c88b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c88b-136">輸入</span><span class="sxs-lookup"><span data-stu-id="7c88b-136">INPUTS</span></span>

### <span data-ttu-id="7c88b-137">System.object</span><span class="sxs-lookup"><span data-stu-id="7c88b-137">System.String</span></span>

### <span data-ttu-id="7c88b-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="7c88b-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="7c88b-139">參數： DataFactory (ByValue) </span><span class="sxs-lookup"><span data-stu-id="7c88b-139">Parameters: DataFactory (ByValue)</span></span>

## <span data-ttu-id="7c88b-140">輸出</span><span class="sxs-lookup"><span data-stu-id="7c88b-140">OUTPUTS</span></span>

### <span data-ttu-id="7c88b-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="7c88b-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="7c88b-142">筆記</span><span class="sxs-lookup"><span data-stu-id="7c88b-142">NOTES</span></span>
<span data-ttu-id="7c88b-143">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="7c88b-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7c88b-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="7c88b-144">RELATED LINKS</span></span>

[<span data-ttu-id="7c88b-145">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="7c88b-145">Set-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="7c88b-146">移除-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="7c88b-146">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
