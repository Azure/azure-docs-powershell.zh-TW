---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 352A4B94-E433-413B-91D1-6AA347563959
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
ms.openlocfilehash: 38af817205f8d80615fa94799eee5a7a54f05e78
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142735"
---
# <span data-ttu-id="21dc8-101">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="21dc8-101">New-AzDataFactoryDataset</span></span>

## <span data-ttu-id="21dc8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="21dc8-102">SYNOPSIS</span></span>
<span data-ttu-id="21dc8-103">在資料工廠中建立資料集。</span><span class="sxs-lookup"><span data-stu-id="21dc8-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="21dc8-104">句法</span><span class="sxs-lookup"><span data-stu-id="21dc8-104">SYNTAX</span></span>

### <span data-ttu-id="21dc8-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="21dc8-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21dc8-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="21dc8-106">ByFactoryObject</span></span>
```
New-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21dc8-107">說明</span><span class="sxs-lookup"><span data-stu-id="21dc8-107">DESCRIPTION</span></span>
<span data-ttu-id="21dc8-108">**新的 AzDataFactoryDataset** Cmdlet 會在 Azure 資料工廠中建立資料集。</span><span class="sxs-lookup"><span data-stu-id="21dc8-108">The **New-AzDataFactoryDataset** cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="21dc8-109">如果您為已存在的資料集指定名稱，此 Cmdlet 會在您取代資料集之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="21dc8-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="21dc8-110">如果您指定 *Force* 參數，則 Cmdlet 會取代現有的資料集，而無需確認。</span><span class="sxs-lookup"><span data-stu-id="21dc8-110">If you specify the *Force* parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="21dc8-111">依下列循序執行這些作業：</span><span class="sxs-lookup"><span data-stu-id="21dc8-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="21dc8-112">建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="21dc8-112">Create a data factory.</span></span> 
- <span data-ttu-id="21dc8-113">建立連結的服務。</span><span class="sxs-lookup"><span data-stu-id="21dc8-113">Create linked services.</span></span> 
- <span data-ttu-id="21dc8-114">建立資料集。</span><span class="sxs-lookup"><span data-stu-id="21dc8-114">Create datasets.</span></span> 
- <span data-ttu-id="21dc8-115">建立管線。</span><span class="sxs-lookup"><span data-stu-id="21dc8-115">Create a pipeline.</span></span>
<span data-ttu-id="21dc8-116">如果資料工廠中已存在具有相同名稱的資料集，此 Cmdlet 會提示您確認是否要使用新的資料集覆寫現有的資料集。</span><span class="sxs-lookup"><span data-stu-id="21dc8-116">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="21dc8-117">如果您確認覆寫現有的資料集，也會取代資料集定義。</span><span class="sxs-lookup"><span data-stu-id="21dc8-117">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="21dc8-118">示例</span><span class="sxs-lookup"><span data-stu-id="21dc8-118">EXAMPLES</span></span>

### <span data-ttu-id="21dc8-119">範例1：建立資料集</span><span class="sxs-lookup"><span data-stu-id="21dc8-119">Example 1: Create a dataset</span></span>
```
PS C:\>New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
DatasetName         : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="21dc8-120">這個命令會在名為 WikiADF 的資料工廠中建立名為 DA_WikipediaClickEvents 的資料集。</span><span class="sxs-lookup"><span data-stu-id="21dc8-120">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="21dc8-121">此命令根據檔案中 DAWikipediaClickEvents.js的資訊來基礎。</span><span class="sxs-lookup"><span data-stu-id="21dc8-121">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

### <span data-ttu-id="21dc8-122">範例2：查看新資料集的可用性</span><span class="sxs-lookup"><span data-stu-id="21dc8-122">Example 2: View availability for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Availability
AnchorDateTime : 
Frequency      : Hour
Interval       : 1
Offset         : 
WaitOnExternal : Microsoft.DataFactories.WaitOnExternal
```

<span data-ttu-id="21dc8-123">第一個命令會建立名為 DA_WikipediaClickEvents 的資料集，就像在前面的範例中一樣，然後將該資料集指派給 $Dataset 變數。</span><span class="sxs-lookup"><span data-stu-id="21dc8-123">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="21dc8-124">第二個命令使用標準點符號來顯示資料集的 Availability 屬性詳細資料。</span><span class="sxs-lookup"><span data-stu-id="21dc8-124">The second command uses standard dot notation to display details about the Availability property of the dataset.</span></span>

### <span data-ttu-id="21dc8-125">範例3：針對新的資料集查看位置</span><span class="sxs-lookup"><span data-stu-id="21dc8-125">Example 3: View location for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="21dc8-126">第一個命令會建立名為 DA_WikipediaClickEvents 的資料集，就像在前面的範例中一樣，然後將該資料集指派給 $Dataset 變數。</span><span class="sxs-lookup"><span data-stu-id="21dc8-126">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="21dc8-127">第二個命令會顯示資料集位置屬性的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="21dc8-127">The second command displays details about the Location property of the dataset.</span></span>

### <span data-ttu-id="21dc8-128">範例4：針對新的資料集查看驗證規則</span><span class="sxs-lookup"><span data-stu-id="21dc8-128">Example 4: View validation rules for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Policy.Validation | Format-List $dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}

MinimumRows   : 
MinimumSizeMB : 1
```

<span data-ttu-id="21dc8-129">第一個命令會建立名為 DA_WikipediaClickEvents 的資料集，就像在前面的範例中一樣，然後將該資料集指派給 $Dataset 變數。</span><span class="sxs-lookup"><span data-stu-id="21dc8-129">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="21dc8-130">第二個命令會取得資料集驗證規則的詳細資料，然後使用管線運算子將它們傳遞到 Format-List Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="21dc8-130">The second command gets details about the validation rules for the dataset, and then passes them to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="21dc8-131">該 Windows PowerShell Cmdlet 會格式化結果。</span><span class="sxs-lookup"><span data-stu-id="21dc8-131">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="21dc8-132">如需詳細資訊，請輸入 `Get-Help Format-List` 。</span><span class="sxs-lookup"><span data-stu-id="21dc8-132">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="21dc8-133">參數</span><span class="sxs-lookup"><span data-stu-id="21dc8-133">PARAMETERS</span></span>

### <span data-ttu-id="21dc8-134">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="21dc8-134">-DataFactory</span></span>
<span data-ttu-id="21dc8-135">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="21dc8-135">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="21dc8-136">這個 Cmdlet 會在此參數指定的資料工廠中建立資料集。</span><span class="sxs-lookup"><span data-stu-id="21dc8-136">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="21dc8-137">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="21dc8-137">-DataFactoryName</span></span>
<span data-ttu-id="21dc8-138">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="21dc8-138">Specifies the name of a data factory.</span></span>
<span data-ttu-id="21dc8-139">這個 Cmdlet 會在此參數指定的資料工廠中建立資料集。</span><span class="sxs-lookup"><span data-stu-id="21dc8-139">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="21dc8-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21dc8-140">-DefaultProfile</span></span>
<span data-ttu-id="21dc8-141">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="21dc8-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21dc8-142">檔案</span><span class="sxs-lookup"><span data-stu-id="21dc8-142">-File</span></span>
<span data-ttu-id="21dc8-143">指定包含資料集描述的 JavaScript 物件符號 (JSON) 檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="21dc8-143">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the dataset.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21dc8-144">-Force</span><span class="sxs-lookup"><span data-stu-id="21dc8-144">-Force</span></span>
<span data-ttu-id="21dc8-145">表示此 Cmdlet 會取代現有的資料集，而不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="21dc8-145">Indicates that this cmdlet replaces an existing dataset without prompting you for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21dc8-146">-名稱</span><span class="sxs-lookup"><span data-stu-id="21dc8-146">-Name</span></span>
<span data-ttu-id="21dc8-147">指定要建立的資料集名稱。</span><span class="sxs-lookup"><span data-stu-id="21dc8-147">Specifies the name of the dataset to create.</span></span>

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

### <span data-ttu-id="21dc8-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21dc8-148">-ResourceGroupName</span></span>
<span data-ttu-id="21dc8-149">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="21dc8-149">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="21dc8-150">這個 Cmdlet 會在此參數指定的群組中建立資料集。</span><span class="sxs-lookup"><span data-stu-id="21dc8-150">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="21dc8-151">-確認</span><span class="sxs-lookup"><span data-stu-id="21dc8-151">-Confirm</span></span>
<span data-ttu-id="21dc8-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="21dc8-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21dc8-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21dc8-153">-WhatIf</span></span>
<span data-ttu-id="21dc8-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="21dc8-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21dc8-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="21dc8-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21dc8-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21dc8-156">CommonParameters</span></span>
<span data-ttu-id="21dc8-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="21dc8-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21dc8-158">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="21dc8-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21dc8-159">輸入</span><span class="sxs-lookup"><span data-stu-id="21dc8-159">INPUTS</span></span>

### <span data-ttu-id="21dc8-160">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="21dc8-160">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="21dc8-161">System.object</span><span class="sxs-lookup"><span data-stu-id="21dc8-161">System.String</span></span>

## <span data-ttu-id="21dc8-162">輸出</span><span class="sxs-lookup"><span data-stu-id="21dc8-162">OUTPUTS</span></span>

### <span data-ttu-id="21dc8-163">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="21dc8-163">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="21dc8-164">筆記</span><span class="sxs-lookup"><span data-stu-id="21dc8-164">NOTES</span></span>
* <span data-ttu-id="21dc8-165">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="21dc8-165">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="21dc8-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="21dc8-166">RELATED LINKS</span></span>

[<span data-ttu-id="21dc8-167">AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="21dc8-167">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="21dc8-168">移除-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="21dc8-168">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)


