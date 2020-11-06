---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: dc6315c16072a736c0db10df6615efb1696b78f2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612994"
---
# <span data-ttu-id="d5d29-101">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="d5d29-101">Get-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="d5d29-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d5d29-102">SYNOPSIS</span></span>
<span data-ttu-id="d5d29-103">取得資料工廠中連結服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d5d29-103">Gets information about linked services in Data Factory.</span></span>

## <span data-ttu-id="d5d29-104">句法</span><span class="sxs-lookup"><span data-stu-id="d5d29-104">SYNTAX</span></span>

### <span data-ttu-id="d5d29-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="d5d29-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5d29-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d5d29-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5d29-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d5d29-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2LinkedService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5d29-108">說明</span><span class="sxs-lookup"><span data-stu-id="d5d29-108">DESCRIPTION</span></span>
<span data-ttu-id="d5d29-109">Get-AzDataFactoryV2LinkedService Cmdlet 會取得 Azure 資料工廠中連結服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d5d29-109">The Get-AzDataFactoryV2LinkedService cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="d5d29-110">如果您指定連結服務的名稱，此 Cmdlet 會取得該連結服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d5d29-110">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="d5d29-111">如果您沒有指定名稱，此 Cmdlet 會取得資料工廠中所有連結服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d5d29-111">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="d5d29-112">示例</span><span class="sxs-lookup"><span data-stu-id="d5d29-112">EXAMPLES</span></span>

### <span data-ttu-id="d5d29-113">範例1：取得所有連結服務的相關資訊</span><span class="sxs-lookup"><span data-stu-id="d5d29-113">Example 1: Get information about all linked services</span></span>
```
PS C:\> Get-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List

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

<span data-ttu-id="d5d29-114">這個命令會取得資料工廠（名為 WikiADF）中所有連結服務的相關資訊，然後使用管線運算子將連結的服務傳送到 Format-List Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d5d29-114">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d5d29-115">該 Windows PowerShell Cmdlet 會格式化結果。</span><span class="sxs-lookup"><span data-stu-id="d5d29-115">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="d5d29-116">如需詳細資訊，請輸入 Get-Help 格式-清單。</span><span class="sxs-lookup"><span data-stu-id="d5d29-116">For more information, type Get-Help Format-List.</span></span>
<span data-ttu-id="d5d29-117">您可以使用下列其中一種方法：</span><span class="sxs-lookup"><span data-stu-id="d5d29-117">You can use either one of the following ways:</span></span>

### <span data-ttu-id="d5d29-118">範例2：取得特定連結服務的相關資訊</span><span class="sxs-lookup"><span data-stu-id="d5d29-118">Example 2: Get information about a specific linked service</span></span>
```
PS C:\> Get-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="d5d29-119">這個命令會在名為 WikiADF 的資料工廠中，取得名為 LinkedServiceCuratedWikiData 的連結服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d5d29-119">This command gets information about the linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>

### <span data-ttu-id="d5d29-120">範例3：指定 DataFactory 參數，以取得特定連結服務的相關資訊</span><span class="sxs-lookup"><span data-stu-id="d5d29-120">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="d5d29-121">第一個命令使用 Get-AzDataFactoryV2 Cmdlet 來取得名為 ContosoFactory 的資料工廠，然後將它儲存在 $DataFactory 變數中。</span><span class="sxs-lookup"><span data-stu-id="d5d29-121">The first command uses the Get-AzDataFactoryV2 cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="d5d29-122">第二個命令會針對儲存在 $DataFactory 中的資料工廠，取得連結服務的相關資訊，然後使用管線運算子將該資訊傳送到 Format-Table Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d5d29-122">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d5d29-123">Format-Table Cmdlet 會將輸出格式化成資料集，並將指定屬性做為資料集資料行。</span><span class="sxs-lookup"><span data-stu-id="d5d29-123">The Format-Table cmdlet formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="d5d29-124">參數</span><span class="sxs-lookup"><span data-stu-id="d5d29-124">PARAMETERS</span></span>

### <span data-ttu-id="d5d29-125">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d5d29-125">-DataFactory</span></span>
<span data-ttu-id="d5d29-126">指定 PSDataFactory 物件。</span><span class="sxs-lookup"><span data-stu-id="d5d29-126">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="d5d29-127">這個 Cmdlet 會取得屬於此參數所指定之資料工廠的連結服務。</span><span class="sxs-lookup"><span data-stu-id="d5d29-127">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d5d29-128">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d5d29-128">-DataFactoryName</span></span>
<span data-ttu-id="d5d29-129">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5d29-129">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d5d29-130">這個 Cmdlet 會取得屬於此參數所指定之資料工廠的連結服務。</span><span class="sxs-lookup"><span data-stu-id="d5d29-130">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d5d29-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5d29-131">-DefaultProfile</span></span>
<span data-ttu-id="d5d29-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d5d29-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5d29-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="d5d29-133">-Name</span></span>
<span data-ttu-id="d5d29-134">指定要取得資訊之連結服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5d29-134">Specifies the name of the linked service about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: LinkedServiceName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5d29-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5d29-135">-ResourceGroupName</span></span>
<span data-ttu-id="d5d29-136">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5d29-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d5d29-137">這個 Cmdlet 會取得屬於此參數指定之群組的連結服務。</span><span class="sxs-lookup"><span data-stu-id="d5d29-137">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d5d29-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5d29-138">-ResourceId</span></span>
<span data-ttu-id="d5d29-139">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d5d29-139">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d5d29-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5d29-140">CommonParameters</span></span>
<span data-ttu-id="d5d29-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d5d29-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5d29-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d5d29-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5d29-143">輸入</span><span class="sxs-lookup"><span data-stu-id="d5d29-143">INPUTS</span></span>

### <span data-ttu-id="d5d29-144">System.object</span><span class="sxs-lookup"><span data-stu-id="d5d29-144">System.String</span></span>

### <span data-ttu-id="d5d29-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d5d29-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="d5d29-146">輸出</span><span class="sxs-lookup"><span data-stu-id="d5d29-146">OUTPUTS</span></span>

### <span data-ttu-id="d5d29-147">PSLinkedService 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="d5d29-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="d5d29-148">筆記</span><span class="sxs-lookup"><span data-stu-id="d5d29-148">NOTES</span></span>
<span data-ttu-id="d5d29-149">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="d5d29-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d5d29-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="d5d29-150">RELATED LINKS</span></span>

[<span data-ttu-id="d5d29-151">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="d5d29-151">Set-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="d5d29-152">移除-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="d5d29-152">Remove-AzDataFactoryV2LinkedService</span></span>]()