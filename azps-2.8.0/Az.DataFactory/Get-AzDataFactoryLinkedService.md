---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
ms.openlocfilehash: a54cdb0a30d0249ccb8fd177646e218e0fe604c2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613020"
---
# <span data-ttu-id="26af9-101">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="26af9-101">Get-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="26af9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="26af9-102">SYNOPSIS</span></span>
<span data-ttu-id="26af9-103">取得 Azure 資料工廠中連結服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="26af9-103">Gets information about linked services in Azure Data Factory.</span></span>

## <span data-ttu-id="26af9-104">句法</span><span class="sxs-lookup"><span data-stu-id="26af9-104">SYNTAX</span></span>

### <span data-ttu-id="26af9-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="26af9-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26af9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="26af9-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26af9-107">說明</span><span class="sxs-lookup"><span data-stu-id="26af9-107">DESCRIPTION</span></span>
<span data-ttu-id="26af9-108">**AzDataFactoryLinkedService** Cmdlet 會取得 Azure 資料工廠中連結服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="26af9-108">The **Get-AzDataFactoryLinkedService** cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="26af9-109">如果您指定連結服務的名稱，此 Cmdlet 會取得該連結服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="26af9-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="26af9-110">如果您沒有指定名稱，此 Cmdlet 會取得資料工廠中所有連結服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="26af9-110">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="26af9-111">示例</span><span class="sxs-lookup"><span data-stu-id="26af9-111">EXAMPLES</span></span>

### <span data-ttu-id="26af9-112">範例1：取得所有連結服務的相關資訊</span><span class="sxs-lookup"><span data-stu-id="26af9-112">Example 1: Get information about all linked services</span></span>
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

<span data-ttu-id="26af9-113">這個命令會取得資料工廠（名為 WikiADF）中所有連結服務的相關資訊，然後使用管線運算子將連結的服務傳送到 Format-List Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26af9-113">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="26af9-114">該 Cmdlet 會格式化結果。</span><span class="sxs-lookup"><span data-stu-id="26af9-114">That cmdlet formats the results.</span></span>
<span data-ttu-id="26af9-115">如需詳細資訊，請輸入 `Get-Help Format-List` 。</span><span class="sxs-lookup"><span data-stu-id="26af9-115">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="26af9-116">範例2：取得特定連結服務的相關資訊</span><span class="sxs-lookup"><span data-stu-id="26af9-116">Example 2: Get information about a specific linked service</span></span>
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

<span data-ttu-id="26af9-117">這個命令會在名為 WikiADF 的資料工廠中，取得名為 HDILinkedService 的連結服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="26af9-117">This command gets information about the linked service named HDILinkedService in the data factory named WikiADF.</span></span>

### <span data-ttu-id="26af9-118">範例3：指定 DataFactory 參數，以取得特定連結服務的相關資訊</span><span class="sxs-lookup"><span data-stu-id="26af9-118">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="26af9-119">第一個命令使用 Get-AzDataFactory Cmdlet 來取得名為 ContosoFactory 的資料工廠，然後將它儲存在 $DataFactory 變數中。</span><span class="sxs-lookup"><span data-stu-id="26af9-119">The first command uses the Get-AzDataFactory cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="26af9-120">第二個命令會針對儲存在 $DataFactory 中的資料工廠，取得連結服務的相關資訊，然後使用管線運算子將該資訊傳送到 Format-Table Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26af9-120">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="26af9-121">[ **格式]-表格** 將輸出格式設定為資料集，並將指定屬性做為資料集資料行。</span><span class="sxs-lookup"><span data-stu-id="26af9-121">**Format-Table** formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="26af9-122">參數</span><span class="sxs-lookup"><span data-stu-id="26af9-122">PARAMETERS</span></span>

### <span data-ttu-id="26af9-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="26af9-123">-DataFactory</span></span>
<span data-ttu-id="26af9-124">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="26af9-124">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="26af9-125">這個 Cmdlet 會取得屬於此參數所指定之資料工廠的連結服務。</span><span class="sxs-lookup"><span data-stu-id="26af9-125">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="26af9-126">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="26af9-126">-DataFactoryName</span></span>
<span data-ttu-id="26af9-127">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="26af9-127">Specifies the name of a data factory.</span></span>
<span data-ttu-id="26af9-128">這個 Cmdlet 會取得屬於此參數所指定之資料工廠的連結服務。</span><span class="sxs-lookup"><span data-stu-id="26af9-128">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="26af9-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26af9-129">-DefaultProfile</span></span>
<span data-ttu-id="26af9-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="26af9-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26af9-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="26af9-131">-Name</span></span>
<span data-ttu-id="26af9-132">指定要取得資訊之連結服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="26af9-132">Specifies the name of the linked service about which to get information.</span></span>

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

### <span data-ttu-id="26af9-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26af9-133">-ResourceGroupName</span></span>
<span data-ttu-id="26af9-134">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="26af9-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="26af9-135">這個 Cmdlet 會取得屬於此參數指定之群組的連結服務。</span><span class="sxs-lookup"><span data-stu-id="26af9-135">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="26af9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26af9-136">CommonParameters</span></span>
<span data-ttu-id="26af9-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="26af9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26af9-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="26af9-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26af9-139">輸入</span><span class="sxs-lookup"><span data-stu-id="26af9-139">INPUTS</span></span>

### <span data-ttu-id="26af9-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="26af9-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="26af9-141">System.object</span><span class="sxs-lookup"><span data-stu-id="26af9-141">System.String</span></span>

## <span data-ttu-id="26af9-142">輸出</span><span class="sxs-lookup"><span data-stu-id="26af9-142">OUTPUTS</span></span>

### <span data-ttu-id="26af9-143">PSLinkedService 中的 DataFactories。</span><span class="sxs-lookup"><span data-stu-id="26af9-143">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span></span>

## <span data-ttu-id="26af9-144">筆記</span><span class="sxs-lookup"><span data-stu-id="26af9-144">NOTES</span></span>
* <span data-ttu-id="26af9-145">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="26af9-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="26af9-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="26af9-146">RELATED LINKS</span></span>

[<span data-ttu-id="26af9-147">新-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="26af9-147">New-AzDataFactoryLinkedService</span></span>](./New-AzDataFactoryLinkedService.md)

[<span data-ttu-id="26af9-148">移除-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="26af9-148">Remove-AzDataFactoryLinkedService</span></span>](./Remove-AzDataFactoryLinkedService.md)

