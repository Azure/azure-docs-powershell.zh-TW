---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2LinkedService.md
gitcommit: https://github.com/Azure/azure-powershell/blob/c396953644d237789e0f4e1f726b553913186d34
ms.openlocfilehash: 7466ad5617fb78d48deb92ac2d623fc05ad90634
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456747"
---
# <span data-ttu-id="c4ac2-101">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="c4ac2-101">Get-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="c4ac2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c4ac2-102">SYNOPSIS</span></span>
<span data-ttu-id="c4ac2-103">取得資料工廠中連結服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c4ac2-103">Gets information about linked services in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4ac2-104">句法</span><span class="sxs-lookup"><span data-stu-id="c4ac2-104">SYNTAX</span></span>

### <span data-ttu-id="c4ac2-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="c4ac2-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### <span data-ttu-id="c4ac2-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c4ac2-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
```
## <span data-ttu-id="c4ac2-107">說明</span><span class="sxs-lookup"><span data-stu-id="c4ac2-107">DESCRIPTION</span></span>
<span data-ttu-id="c4ac2-108">Get-AzureRmDataFactoryV2LinkedService Cmdlet 會取得 Azure 資料工廠中連結服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c4ac2-108">The Get-AzureRmDataFactoryV2LinkedService cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="c4ac2-109">如果您指定連結服務的名稱，此 Cmdlet 會取得該連結服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c4ac2-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="c4ac2-110">如果您沒有指定名稱，此 Cmdlet 會取得資料工廠中所有連結服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c4ac2-110">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="c4ac2-111">示例</span><span class="sxs-lookup"><span data-stu-id="c4ac2-111">EXAMPLES</span></span>

### <span data-ttu-id="c4ac2-112">範例1：取得所有連結服務的相關資訊</span><span class="sxs-lookup"><span data-stu-id="c4ac2-112">Example 1: Get information about all linked services</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceHDIStorage
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="c4ac2-113">這個命令會取得資料工廠（名為 WikiADF）中所有連結服務的相關資訊，然後使用管線運算子將連結的服務傳送到 Format-List Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c4ac2-113">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c4ac2-114">該 Windows PowerShell Cmdlet 會格式化結果。</span><span class="sxs-lookup"><span data-stu-id="c4ac2-114">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="c4ac2-115">如需詳細資訊，請輸入 Get-Help 格式-清單。</span><span class="sxs-lookup"><span data-stu-id="c4ac2-115">For more information, type Get-Help Format-List.</span></span>

<span data-ttu-id="c4ac2-116">您可以使用下列其中一種方法：</span><span class="sxs-lookup"><span data-stu-id="c4ac2-116">You can use either one of the following ways:</span></span>

### <span data-ttu-id="c4ac2-117">範例2：取得特定連結服務的相關資訊</span><span class="sxs-lookup"><span data-stu-id="c4ac2-117">Example 2: Get information about a specific linked service</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="c4ac2-118">這個命令會在名為 WikiADF 的資料工廠中，取得名為 LinkedServiceCuratedWikiData 的連結服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c4ac2-118">This command gets information about the linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>

### <span data-ttu-id="c4ac2-119">範例3：指定 DataFactory 參數，以取得特定連結服務的相關資訊</span><span class="sxs-lookup"><span data-stu-id="c4ac2-119">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzureRmDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="c4ac2-120">第一個命令使用 Get-AzureRmDataFactoryV2 Cmdlet 來取得名為 ContosoFactory 的資料工廠，然後將它儲存在 $DataFactory 變數中。</span><span class="sxs-lookup"><span data-stu-id="c4ac2-120">The first command uses the Get-AzureRmDataFactoryV2 cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>

<span data-ttu-id="c4ac2-121">第二個命令會針對儲存在 $DataFactory 中的資料工廠，取得連結服務的相關資訊，然後使用管線運算子將該資訊傳送到 Format-Table Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c4ac2-121">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c4ac2-122">Format-Table Cmdlet 會將輸出格式化成資料集，並將指定屬性做為資料集資料行。</span><span class="sxs-lookup"><span data-stu-id="c4ac2-122">The Format-Table cmdlet formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="c4ac2-123">參數</span><span class="sxs-lookup"><span data-stu-id="c4ac2-123">PARAMETERS</span></span>

### <span data-ttu-id="c4ac2-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="c4ac2-124">-DataFactory</span></span>
<span data-ttu-id="c4ac2-125">指定 PSDataFactory 物件。</span><span class="sxs-lookup"><span data-stu-id="c4ac2-125">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="c4ac2-126">這個 Cmdlet 會取得屬於此參數所指定之資料工廠的連結服務。</span><span class="sxs-lookup"><span data-stu-id="c4ac2-126">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c4ac2-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c4ac2-127">-DataFactoryName</span></span>
<span data-ttu-id="c4ac2-128">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4ac2-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="c4ac2-129">這個 Cmdlet 會取得屬於此參數所指定之資料工廠的連結服務。</span><span class="sxs-lookup"><span data-stu-id="c4ac2-129">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c4ac2-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="c4ac2-130">-Name</span></span>
<span data-ttu-id="c4ac2-131">指定要取得資訊之連結服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4ac2-131">Specifies the name of the linked service about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ac2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4ac2-132">-ResourceGroupName</span></span>
<span data-ttu-id="c4ac2-133">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4ac2-133">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c4ac2-134">這個 Cmdlet 會取得屬於此參數指定之群組的連結服務。</span><span class="sxs-lookup"><span data-stu-id="c4ac2-134">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

## <span data-ttu-id="c4ac2-135">輸入</span><span class="sxs-lookup"><span data-stu-id="c4ac2-135">INPUTS</span></span>

### <span data-ttu-id="c4ac2-136">System.object</span><span class="sxs-lookup"><span data-stu-id="c4ac2-136">System.String</span></span>
<span data-ttu-id="c4ac2-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c4ac2-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="c4ac2-138">輸出</span><span class="sxs-lookup"><span data-stu-id="c4ac2-138">OUTPUTS</span></span>

### <span data-ttu-id="c4ac2-139">[System.object]。清單 ' 1 [DataFactoryV2. PSLinkedService，DataFactoryV2，版本 = 0.1.9.0，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="c4ac2-139">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="c4ac2-140">PSLinkedService 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="c4ac2-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>


## <span data-ttu-id="c4ac2-141">筆記</span><span class="sxs-lookup"><span data-stu-id="c4ac2-141">NOTES</span></span>
<span data-ttu-id="c4ac2-142">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="c4ac2-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c4ac2-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="c4ac2-143">RELATED LINKS</span></span>
[<span data-ttu-id="c4ac2-144">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="c4ac2-144">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="c4ac2-145">移除-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="c4ac2-145">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()
