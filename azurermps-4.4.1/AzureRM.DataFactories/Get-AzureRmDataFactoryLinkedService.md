---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: 7503d775b7241bbb1be6196db153e41587c0e736
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626329"
---
# <span data-ttu-id="6181c-101">Get-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="6181c-101">Get-AzureRmDataFactoryLinkedService</span></span>

## <span data-ttu-id="6181c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6181c-102">SYNOPSIS</span></span>
<span data-ttu-id="6181c-103">取得 Azure 資料工廠中連結服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6181c-103">Gets information about linked services in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6181c-104">句法</span><span class="sxs-lookup"><span data-stu-id="6181c-104">SYNTAX</span></span>

### <span data-ttu-id="6181c-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="6181c-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6181c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6181c-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6181c-107">說明</span><span class="sxs-lookup"><span data-stu-id="6181c-107">DESCRIPTION</span></span>
<span data-ttu-id="6181c-108">**AzureRmDataFactoryLinkedService** Cmdlet 會取得 Azure 資料工廠中連結服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6181c-108">The **Get-AzureRmDataFactoryLinkedService** cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="6181c-109">如果您指定連結服務的名稱，此 Cmdlet 會取得該連結服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6181c-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="6181c-110">如果您沒有指定名稱，此 Cmdlet 會取得資料工廠中所有連結服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6181c-110">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="6181c-111">示例</span><span class="sxs-lookup"><span data-stu-id="6181c-111">EXAMPLES</span></span>

### <span data-ttu-id="6181c-112">範例1：取得所有連結服務的相關資訊</span><span class="sxs-lookup"><span data-stu-id="6181c-112">Example 1: Get information about all linked services</span></span>
```
PS C:\>Get-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

<span data-ttu-id="6181c-113">這個命令會取得資料工廠（名為 WikiADF）中所有連結服務的相關資訊，然後使用管線運算子將連結的服務傳送到 Format-List Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6181c-113">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6181c-114">該 Cmdlet 會格式化結果。</span><span class="sxs-lookup"><span data-stu-id="6181c-114">That cmdlet formats the results.</span></span>
<span data-ttu-id="6181c-115">如需詳細資訊，請輸入 `Get-Help Format-List` 。</span><span class="sxs-lookup"><span data-stu-id="6181c-115">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="6181c-116">範例2：取得特定連結服務的相關資訊</span><span class="sxs-lookup"><span data-stu-id="6181c-116">Example 2: Get information about a specific linked service</span></span>
```
PS C:\>Get-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

<span data-ttu-id="6181c-117">這個命令會在名為 WikiADF 的資料工廠中，取得名為 HDILinkedService 的連結服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6181c-117">This command gets information about the linked service named HDILinkedService in the data factory named WikiADF.</span></span>

### <span data-ttu-id="6181c-118">範例3：指定 DataFactory 參數，以取得特定連結服務的相關資訊</span><span class="sxs-lookup"><span data-stu-id="6181c-118">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzureRmDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="6181c-119">第一個命令使用 Get-AzureRmDataFactory Cmdlet 來取得名為 ContosoFactory 的資料工廠，然後將它儲存在 $DataFactory 變數中。</span><span class="sxs-lookup"><span data-stu-id="6181c-119">The first command uses the Get-AzureRmDataFactory cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>

<span data-ttu-id="6181c-120">第二個命令會針對儲存在 $DataFactory 中的資料工廠，取得連結服務的相關資訊，然後使用管線運算子將該資訊傳送到 Format-Table Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6181c-120">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6181c-121">[ **格式]-表格** 將輸出格式設定為資料集，並將指定屬性做為資料集資料行。</span><span class="sxs-lookup"><span data-stu-id="6181c-121">**Format-Table** formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="6181c-122">參數</span><span class="sxs-lookup"><span data-stu-id="6181c-122">PARAMETERS</span></span>

### <span data-ttu-id="6181c-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="6181c-123">-DataFactory</span></span>
<span data-ttu-id="6181c-124">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="6181c-124">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="6181c-125">這個 Cmdlet 會取得屬於此參數所指定之資料工廠的連結服務。</span><span class="sxs-lookup"><span data-stu-id="6181c-125">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6181c-126">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6181c-126">-DataFactoryName</span></span>
<span data-ttu-id="6181c-127">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="6181c-127">Specifies the name of a data factory.</span></span>
<span data-ttu-id="6181c-128">這個 Cmdlet 會取得屬於此參數所指定之資料工廠的連結服務。</span><span class="sxs-lookup"><span data-stu-id="6181c-128">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6181c-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="6181c-129">-Name</span></span>
<span data-ttu-id="6181c-130">指定要取得資訊之連結服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="6181c-130">Specifies the name of the linked service about which to get information.</span></span>

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

### <span data-ttu-id="6181c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6181c-131">-ResourceGroupName</span></span>
<span data-ttu-id="6181c-132">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6181c-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="6181c-133">這個 Cmdlet 會取得屬於此參數指定之群組的連結服務。</span><span class="sxs-lookup"><span data-stu-id="6181c-133">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6181c-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6181c-134">-DefaultProfile</span></span>
<span data-ttu-id="6181c-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6181c-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6181c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6181c-136">CommonParameters</span></span>
<span data-ttu-id="6181c-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6181c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6181c-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6181c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6181c-139">輸入</span><span class="sxs-lookup"><span data-stu-id="6181c-139">INPUTS</span></span>

## <span data-ttu-id="6181c-140">輸出</span><span class="sxs-lookup"><span data-stu-id="6181c-140">OUTPUTS</span></span>

### <span data-ttu-id="6181c-141">[System.object]. 清單 ' 1 [PSLinkedService，WindowsAzure. WindowsAzure = 0.8.2.0，Culture = 中立，PublicKeyToken = 31bf3856ad364e35]]. WindowsAzure. PSLinkedService.）的。。</span><span class="sxs-lookup"><span data-stu-id="6181c-141">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSLinkedService, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSLinkedService</span></span>

## <span data-ttu-id="6181c-142">筆記</span><span class="sxs-lookup"><span data-stu-id="6181c-142">NOTES</span></span>
* <span data-ttu-id="6181c-143">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="6181c-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6181c-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="6181c-144">RELATED LINKS</span></span>

[<span data-ttu-id="6181c-145">新-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="6181c-145">New-AzureRmDataFactoryLinkedService</span></span>](./New-AzureRmDataFactoryLinkedService.md)

[<span data-ttu-id="6181c-146">移除-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="6181c-146">Remove-AzureRmDataFactoryLinkedService</span></span>](./Remove-AzureRmDataFactoryLinkedService.md)

