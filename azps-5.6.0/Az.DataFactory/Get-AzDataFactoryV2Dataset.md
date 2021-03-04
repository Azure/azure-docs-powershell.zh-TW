---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 938b51b6025a420570ad62b4e9ce815fe832c4cb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907741"
---
# <span data-ttu-id="13693-101">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="13693-101">Get-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="13693-102">簡介</span><span class="sxs-lookup"><span data-stu-id="13693-102">SYNOPSIS</span></span>
<span data-ttu-id="13693-103">在 Data Factory 中獲取資料集相關資訊。</span><span class="sxs-lookup"><span data-stu-id="13693-103">Gets information about datasets in Data Factory.</span></span>

## <span data-ttu-id="13693-104">語法</span><span class="sxs-lookup"><span data-stu-id="13693-104">SYNTAX</span></span>

### <span data-ttu-id="13693-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="13693-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13693-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="13693-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13693-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="13693-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Dataset [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13693-108">描述</span><span class="sxs-lookup"><span data-stu-id="13693-108">DESCRIPTION</span></span>
<span data-ttu-id="13693-109">Cmdlet Get-AzDataFactoryV2Dataset Azure Data Factory 中資料集相關資訊。</span><span class="sxs-lookup"><span data-stu-id="13693-109">The Get-AzDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="13693-110">如果您指定資料集的名稱，此 Cmdlet 會獲得該資料集的資訊。</span><span class="sxs-lookup"><span data-stu-id="13693-110">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="13693-111">如果您未指定名稱，此 Cmdlet 會獲得資料工廠中所有資料集的資訊。</span><span class="sxs-lookup"><span data-stu-id="13693-111">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="13693-112">例子</span><span class="sxs-lookup"><span data-stu-id="13693-112">EXAMPLES</span></span>

### <span data-ttu-id="13693-113">範例 1：取得所有資料集的資訊</span><span class="sxs-lookup"><span data-stu-id="13693-113">Example 1: Get information about all datasets</span></span>
```
PS C:\> Get-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

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

<span data-ttu-id="13693-114">此命令會獲得名稱為 WikiADF 的資料工廠中所有資料集的資訊。</span><span class="sxs-lookup"><span data-stu-id="13693-114">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="13693-115">範例 2：取得特定資料集的資訊</span><span class="sxs-lookup"><span data-stu-id="13693-115">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="13693-116">此命令會從名為 WikiADF 的資料工廠中，獲得名為 DAWikipediaClickEvents 的資料集相關資訊。</span><span class="sxs-lookup"><span data-stu-id="13693-116">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="13693-117">參數</span><span class="sxs-lookup"><span data-stu-id="13693-117">PARAMETERS</span></span>

### <span data-ttu-id="13693-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="13693-118">-DataFactory</span></span>
<span data-ttu-id="13693-119">指定 PSDataFactory 物件。</span><span class="sxs-lookup"><span data-stu-id="13693-119">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="13693-120">此 Cmdlet 會獲得屬於此參數指定之資料工廠的資料集。</span><span class="sxs-lookup"><span data-stu-id="13693-120">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="13693-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="13693-121">-DataFactoryName</span></span>
<span data-ttu-id="13693-122">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="13693-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="13693-123">此 Cmdlet 會獲得屬於此參數指定之資料工廠的資料集。</span><span class="sxs-lookup"><span data-stu-id="13693-123">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="13693-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13693-124">-DefaultProfile</span></span>
<span data-ttu-id="13693-125">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="13693-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13693-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="13693-126">-Name</span></span>
<span data-ttu-id="13693-127">指定要取得資訊的資料集名稱。</span><span class="sxs-lookup"><span data-stu-id="13693-127">Specifies the name of the dataset about which to get information.</span></span>

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

### <span data-ttu-id="13693-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13693-128">-ResourceGroupName</span></span>
<span data-ttu-id="13693-129">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="13693-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="13693-130">此 Cmdlet 會獲得屬於此參數指定之群組的資料集。</span><span class="sxs-lookup"><span data-stu-id="13693-130">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="13693-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13693-131">-ResourceId</span></span>
<span data-ttu-id="13693-132">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="13693-132">The Azure resource ID.</span></span>

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

### <span data-ttu-id="13693-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13693-133">CommonParameters</span></span>
<span data-ttu-id="13693-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="13693-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13693-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="13693-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13693-136">輸入</span><span class="sxs-lookup"><span data-stu-id="13693-136">INPUTS</span></span>

### <span data-ttu-id="13693-137">System.String</span><span class="sxs-lookup"><span data-stu-id="13693-137">System.String</span></span>

### <span data-ttu-id="13693-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="13693-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="13693-139">輸出</span><span class="sxs-lookup"><span data-stu-id="13693-139">OUTPUTS</span></span>

### <span data-ttu-id="13693-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="13693-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="13693-141">筆記</span><span class="sxs-lookup"><span data-stu-id="13693-141">NOTES</span></span>
<span data-ttu-id="13693-142">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="13693-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="13693-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="13693-143">RELATED LINKS</span></span>

[<span data-ttu-id="13693-144">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="13693-144">Set-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="13693-145">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="13693-145">Remove-AzDataFactoryV2Dataset</span></span>]()
