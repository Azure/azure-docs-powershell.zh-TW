---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 405ec877f139865082d21eb2c05ace17f1100e2e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444580"
---
# <span data-ttu-id="6f930-101">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="6f930-101">Set-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="6f930-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6f930-102">SYNOPSIS</span></span>
<span data-ttu-id="6f930-103">在資料工廠中建立資料集。</span><span class="sxs-lookup"><span data-stu-id="6f930-103">Creates a dataset in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f930-104">句法</span><span class="sxs-lookup"><span data-stu-id="6f930-104">SYNTAX</span></span>

### <span data-ttu-id="6f930-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="6f930-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f930-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6f930-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f930-107">說明</span><span class="sxs-lookup"><span data-stu-id="6f930-107">DESCRIPTION</span></span>
<span data-ttu-id="6f930-108">Set-AzureRmDataFactoryV2Dataset Cmdlet 會建立 Azure 資料工廠中的資料集。</span><span class="sxs-lookup"><span data-stu-id="6f930-108">The Set-AzureRmDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="6f930-109">如果您為已存在的資料集指定名稱，此 Cmdlet 會在您取代資料集之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6f930-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="6f930-110">如果您指定 Force 參數，則 Cmdlet 會取代現有的資料集，而無需確認。</span><span class="sxs-lookup"><span data-stu-id="6f930-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>

<span data-ttu-id="6f930-111">依下列循序執行這些作業：</span><span class="sxs-lookup"><span data-stu-id="6f930-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

<span data-ttu-id="6f930-112">如果資料工廠中已存在具有相同名稱的資料集，此 Cmdlet 會提示您確認是否要使用新的資料集覆寫現有的資料集。</span><span class="sxs-lookup"><span data-stu-id="6f930-112">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="6f930-113">如果您確認覆寫現有的資料集，也會取代資料集定義。</span><span class="sxs-lookup"><span data-stu-id="6f930-113">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="6f930-114">示例</span><span class="sxs-lookup"><span data-stu-id="6f930-114">EXAMPLES</span></span>

### <span data-ttu-id="6f930-115">範例1：建立資料集</span><span class="sxs-lookup"><span data-stu-id="6f930-115">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="6f930-116">這個命令會在名為 WikiADF 的資料工廠中建立名為 DA_WikipediaClickEvents 的資料集。</span><span class="sxs-lookup"><span data-stu-id="6f930-116">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="6f930-117">此命令根據檔案中 DAWikipediaClickEvents.js的資訊來基礎。</span><span class="sxs-lookup"><span data-stu-id="6f930-117">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="6f930-118">參數</span><span class="sxs-lookup"><span data-stu-id="6f930-118">PARAMETERS</span></span>

### <span data-ttu-id="6f930-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6f930-119">-DataFactoryName</span></span>
<span data-ttu-id="6f930-120">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f930-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="6f930-121">這個 Cmdlet 會在此參數指定的資料工廠中建立資料集。</span><span class="sxs-lookup"><span data-stu-id="6f930-121">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6f930-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f930-122">-DefaultProfile</span></span>
<span data-ttu-id="6f930-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6f930-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f930-124">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="6f930-124">-DefinitionFile</span></span>
<span data-ttu-id="6f930-125">JSON 檔路徑。</span><span class="sxs-lookup"><span data-stu-id="6f930-125">The JSON file path.</span></span>

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

### <span data-ttu-id="6f930-126">-Force</span><span class="sxs-lookup"><span data-stu-id="6f930-126">-Force</span></span>
<span data-ttu-id="6f930-127">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6f930-127">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="6f930-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="6f930-128">-Name</span></span>
<span data-ttu-id="6f930-129">指定要建立的資料集名稱。</span><span class="sxs-lookup"><span data-stu-id="6f930-129">Specifies the name of the dataset to create.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f930-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f930-130">-ResourceGroupName</span></span>
<span data-ttu-id="6f930-131">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f930-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="6f930-132">這個 Cmdlet 會在此參數指定的群組中建立資料集。</span><span class="sxs-lookup"><span data-stu-id="6f930-132">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6f930-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f930-133">-ResourceId</span></span>
<span data-ttu-id="6f930-134">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f930-134">The Azure resource ID.</span></span>

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

### <span data-ttu-id="6f930-135">-確認</span><span class="sxs-lookup"><span data-stu-id="6f930-135">-Confirm</span></span>
<span data-ttu-id="6f930-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6f930-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f930-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f930-137">-WhatIf</span></span>
<span data-ttu-id="6f930-138">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6f930-138">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="6f930-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f930-139">CommonParameters</span></span>
<span data-ttu-id="6f930-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6f930-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f930-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6f930-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f930-142">輸入</span><span class="sxs-lookup"><span data-stu-id="6f930-142">INPUTS</span></span>

### <span data-ttu-id="6f930-143">System.object</span><span class="sxs-lookup"><span data-stu-id="6f930-143">System.String</span></span>

## <span data-ttu-id="6f930-144">輸出</span><span class="sxs-lookup"><span data-stu-id="6f930-144">OUTPUTS</span></span>

### <span data-ttu-id="6f930-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="6f930-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="6f930-146">筆記</span><span class="sxs-lookup"><span data-stu-id="6f930-146">NOTES</span></span>
<span data-ttu-id="6f930-147">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="6f930-147">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6f930-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f930-148">RELATED LINKS</span></span>

[<span data-ttu-id="6f930-149">AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="6f930-149">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="6f930-150">移除-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="6f930-150">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
