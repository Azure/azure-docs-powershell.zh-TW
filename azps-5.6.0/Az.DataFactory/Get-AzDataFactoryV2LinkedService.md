---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: 0312b3d2a5ffa973c4ef2934ea592844850d8018
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907713"
---
# <span data-ttu-id="147fa-101">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="147fa-101">Get-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="147fa-102">簡介</span><span class="sxs-lookup"><span data-stu-id="147fa-102">SYNOPSIS</span></span>
<span data-ttu-id="147fa-103">在 Data Factory 中，獲得連結服務的資訊。</span><span class="sxs-lookup"><span data-stu-id="147fa-103">Gets information about linked services in Data Factory.</span></span>

## <span data-ttu-id="147fa-104">語法</span><span class="sxs-lookup"><span data-stu-id="147fa-104">SYNTAX</span></span>

### <span data-ttu-id="147fa-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="147fa-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="147fa-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="147fa-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="147fa-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="147fa-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2LinkedService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="147fa-108">描述</span><span class="sxs-lookup"><span data-stu-id="147fa-108">DESCRIPTION</span></span>
<span data-ttu-id="147fa-109">Cmdlet Get-AzDataFactoryV2LinkedService Azure Data Factory 中的連結服務相關資訊。</span><span class="sxs-lookup"><span data-stu-id="147fa-109">The Get-AzDataFactoryV2LinkedService cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="147fa-110">如果您指定連結服務的名稱，此 Cmdlet 會獲得該連結服務的資訊。</span><span class="sxs-lookup"><span data-stu-id="147fa-110">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="147fa-111">如果您未指定名稱，此 Cmdlet 會獲得資料工廠中所有連結服務的資訊。</span><span class="sxs-lookup"><span data-stu-id="147fa-111">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="147fa-112">例子</span><span class="sxs-lookup"><span data-stu-id="147fa-112">EXAMPLES</span></span>

### <span data-ttu-id="147fa-113">範例 1：取得所有連結服務的資訊</span><span class="sxs-lookup"><span data-stu-id="147fa-113">Example 1: Get information about all linked services</span></span>
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

<span data-ttu-id="147fa-114">此命令會獲得名稱為 WikiADF 的資料工廠中所有連結服務的資訊，然後使用管線運算子將連結服務Format-List Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="147fa-114">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="147fa-115">Windows PowerShell Cmdlet 會格式化結果。</span><span class="sxs-lookup"><span data-stu-id="147fa-115">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="147fa-116">詳細資訊，輸入Get-Help格式清單。</span><span class="sxs-lookup"><span data-stu-id="147fa-116">For more information, type Get-Help Format-List.</span></span>
<span data-ttu-id="147fa-117">您可以使用下列其中一種方式：</span><span class="sxs-lookup"><span data-stu-id="147fa-117">You can use either one of the following ways:</span></span>

### <span data-ttu-id="147fa-118">範例 2：取得特定連結服務的資訊</span><span class="sxs-lookup"><span data-stu-id="147fa-118">Example 2: Get information about a specific linked service</span></span>
```
PS C:\> Get-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="147fa-119">此命令會獲得名為 WikiADF 的資料工廠中 LinkedServiceCuratedWikiData 的連結服務相關資訊。</span><span class="sxs-lookup"><span data-stu-id="147fa-119">This command gets information about the linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>

### <span data-ttu-id="147fa-120">範例 3：指定 DataFactory 參數以取得特定連結服務的資訊</span><span class="sxs-lookup"><span data-stu-id="147fa-120">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="147fa-121">第一個命令使用 Get-AzDataFactoryV2 Cmdlet 取得名為 ContosoFactory 的資料工廠，然後將它儲存在 $DataFactory 變數中。</span><span class="sxs-lookup"><span data-stu-id="147fa-121">The first command uses the Get-AzDataFactoryV2 cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="147fa-122">第二個命令會獲得儲存在 $DataFactory 之資料工廠的連結服務相關資訊，然後使用管線運算子將該資訊傳遞至 Format-Table Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="147fa-122">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="147fa-123">Cmdlet Format-Table將輸出格式化為資料集，將指定的屬性格式化為資料集欄。</span><span class="sxs-lookup"><span data-stu-id="147fa-123">The Format-Table cmdlet formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="147fa-124">參數</span><span class="sxs-lookup"><span data-stu-id="147fa-124">PARAMETERS</span></span>

### <span data-ttu-id="147fa-125">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="147fa-125">-DataFactory</span></span>
<span data-ttu-id="147fa-126">指定 PSDataFactory 物件。</span><span class="sxs-lookup"><span data-stu-id="147fa-126">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="147fa-127">此 Cmdlet 會獲得屬於此參數指定之資料工廠的連結服務。</span><span class="sxs-lookup"><span data-stu-id="147fa-127">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="147fa-128">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="147fa-128">-DataFactoryName</span></span>
<span data-ttu-id="147fa-129">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="147fa-129">Specifies the name of a data factory.</span></span>
<span data-ttu-id="147fa-130">此 Cmdlet 會獲得屬於此參數指定之資料工廠的連結服務。</span><span class="sxs-lookup"><span data-stu-id="147fa-130">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="147fa-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="147fa-131">-DefaultProfile</span></span>
<span data-ttu-id="147fa-132">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="147fa-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="147fa-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="147fa-133">-Name</span></span>
<span data-ttu-id="147fa-134">指定取得相關資訊之連結服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="147fa-134">Specifies the name of the linked service about which to get information.</span></span>

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

### <span data-ttu-id="147fa-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="147fa-135">-ResourceGroupName</span></span>
<span data-ttu-id="147fa-136">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="147fa-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="147fa-137">此 Cmdlet 會獲得屬於此參數指定之群組的連結服務。</span><span class="sxs-lookup"><span data-stu-id="147fa-137">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="147fa-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="147fa-138">-ResourceId</span></span>
<span data-ttu-id="147fa-139">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="147fa-139">The Azure resource ID.</span></span>

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

### <span data-ttu-id="147fa-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="147fa-140">CommonParameters</span></span>
<span data-ttu-id="147fa-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="147fa-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="147fa-142">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="147fa-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="147fa-143">輸入</span><span class="sxs-lookup"><span data-stu-id="147fa-143">INPUTS</span></span>

### <span data-ttu-id="147fa-144">System.String</span><span class="sxs-lookup"><span data-stu-id="147fa-144">System.String</span></span>

### <span data-ttu-id="147fa-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="147fa-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="147fa-146">輸出</span><span class="sxs-lookup"><span data-stu-id="147fa-146">OUTPUTS</span></span>

### <span data-ttu-id="147fa-147">Microsoft.Azure.Commands.DataFactoryV2.models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="147fa-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="147fa-148">筆記</span><span class="sxs-lookup"><span data-stu-id="147fa-148">NOTES</span></span>
<span data-ttu-id="147fa-149">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="147fa-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="147fa-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="147fa-150">RELATED LINKS</span></span>

[<span data-ttu-id="147fa-151">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="147fa-151">Set-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="147fa-152">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="147fa-152">Remove-AzDataFactoryV2LinkedService</span></span>]()
