---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: f977344f2beabe8352a7417130063c3e9d4d3e1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626634"
---
# <span data-ttu-id="75bbd-101">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="75bbd-101">Set-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="75bbd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="75bbd-102">SYNOPSIS</span></span>
<span data-ttu-id="75bbd-103">將資料存放區或雲端服務連結至資料工廠。</span><span class="sxs-lookup"><span data-stu-id="75bbd-103">Links a data store or a cloud service to Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75bbd-104">句法</span><span class="sxs-lookup"><span data-stu-id="75bbd-104">SYNTAX</span></span>

### <span data-ttu-id="75bbd-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="75bbd-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="75bbd-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="75bbd-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force] [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="75bbd-107">說明</span><span class="sxs-lookup"><span data-stu-id="75bbd-107">DESCRIPTION</span></span>
<span data-ttu-id="75bbd-108">Set-AzureRmDataFactoryV2LinkedService Cmdlet 會將資料存放區或雲端服務連結至 Azure 資料工廠。</span><span class="sxs-lookup"><span data-stu-id="75bbd-108">The Set-AzureRmDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="75bbd-109">如果您指定已存在之連結服務的名稱，此 Cmdlet 會在您替換連結的服務之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="75bbd-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="75bbd-110">如果您指定 Force 參數，則 Cmdlet 會取代現有的連結服務而不進行確認。</span><span class="sxs-lookup"><span data-stu-id="75bbd-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>

<span data-ttu-id="75bbd-111">依下列循序執行這些作業：</span><span class="sxs-lookup"><span data-stu-id="75bbd-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="75bbd-112">示例</span><span class="sxs-lookup"><span data-stu-id="75bbd-112">EXAMPLES</span></span>

### <span data-ttu-id="75bbd-113">範例1：建立連結的服務</span><span class="sxs-lookup"><span data-stu-id="75bbd-113">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

```

<span data-ttu-id="75bbd-114">這個命令會在名為 WikiADF 的資料工廠中建立名為 LinkedServiceCuratedWikiData 的連結服務。</span><span class="sxs-lookup"><span data-stu-id="75bbd-114">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="75bbd-115">這個連結的服務會將檔案中指定的 Azure blob 存放區連結到名為 WikiADF 的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="75bbd-115">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="75bbd-116">命令會使用管線運算子，將結果傳遞到 Format-List Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="75bbd-116">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="75bbd-117">該 Windows PowerShell Cmdlet 會格式化結果。</span><span class="sxs-lookup"><span data-stu-id="75bbd-117">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="75bbd-118">如需詳細資訊，請輸入 Get-Help 格式-清單。</span><span class="sxs-lookup"><span data-stu-id="75bbd-118">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="75bbd-119">參數</span><span class="sxs-lookup"><span data-stu-id="75bbd-119">PARAMETERS</span></span>

### <span data-ttu-id="75bbd-120">-確認</span><span class="sxs-lookup"><span data-stu-id="75bbd-120">-Confirm</span></span>
<span data-ttu-id="75bbd-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="75bbd-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75bbd-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="75bbd-122">-DataFactoryName</span></span>
<span data-ttu-id="75bbd-123">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="75bbd-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="75bbd-124">這個 Cmdlet 會針對此參數指定的資料工廠建立連結的服務。</span><span class="sxs-lookup"><span data-stu-id="75bbd-124">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="75bbd-125">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="75bbd-125">-DefinitionFile</span></span>
<span data-ttu-id="75bbd-126">JSON 檔路徑。</span><span class="sxs-lookup"><span data-stu-id="75bbd-126">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75bbd-127">-Force</span><span class="sxs-lookup"><span data-stu-id="75bbd-127">-Force</span></span>
<span data-ttu-id="75bbd-128">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="75bbd-128">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75bbd-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="75bbd-129">-Name</span></span>
<span data-ttu-id="75bbd-130">指定要建立之連結服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="75bbd-130">Specifies the name of the linked service to create.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75bbd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75bbd-131">-ResourceGroupName</span></span>
<span data-ttu-id="75bbd-132">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="75bbd-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="75bbd-133">這個 Cmdlet 會針對此參數指定的群組建立連結的服務。</span><span class="sxs-lookup"><span data-stu-id="75bbd-133">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="75bbd-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75bbd-134">-ResourceId</span></span>
<span data-ttu-id="75bbd-135">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="75bbd-135">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75bbd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75bbd-136">-WhatIf</span></span>
<span data-ttu-id="75bbd-137">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="75bbd-137">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="75bbd-138">輸入</span><span class="sxs-lookup"><span data-stu-id="75bbd-138">INPUTS</span></span>

### <span data-ttu-id="75bbd-139">System.object</span><span class="sxs-lookup"><span data-stu-id="75bbd-139">System.String</span></span>


## <span data-ttu-id="75bbd-140">輸出</span><span class="sxs-lookup"><span data-stu-id="75bbd-140">OUTPUTS</span></span>

### <span data-ttu-id="75bbd-141">PSLinkedService 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="75bbd-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>


## <span data-ttu-id="75bbd-142">筆記</span><span class="sxs-lookup"><span data-stu-id="75bbd-142">NOTES</span></span>
<span data-ttu-id="75bbd-143">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="75bbd-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="75bbd-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="75bbd-144">RELATED LINKS</span></span>
[<span data-ttu-id="75bbd-145">AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="75bbd-145">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="75bbd-146">移除-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="75bbd-146">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()
