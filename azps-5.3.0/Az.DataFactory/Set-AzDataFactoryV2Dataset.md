---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
ms.openlocfilehash: c02ce9b0ba62f7baf4879946bd0ab04efdd5c9e4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449381"
---
# <span data-ttu-id="d3555-101">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="d3555-101">Set-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="d3555-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d3555-102">SYNOPSIS</span></span>
<span data-ttu-id="d3555-103">在資料工廠中建立資料集。</span><span class="sxs-lookup"><span data-stu-id="d3555-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="d3555-104">句法</span><span class="sxs-lookup"><span data-stu-id="d3555-104">SYNTAX</span></span>

### <span data-ttu-id="d3555-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="d3555-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3555-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d3555-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3555-107">說明</span><span class="sxs-lookup"><span data-stu-id="d3555-107">DESCRIPTION</span></span>
<span data-ttu-id="d3555-108">Set-AzDataFactoryV2Dataset Cmdlet 會建立 Azure 資料工廠中的資料集。</span><span class="sxs-lookup"><span data-stu-id="d3555-108">The Set-AzDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="d3555-109">如果您為已存在的資料集指定名稱，此 Cmdlet 會在您取代資料集之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d3555-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="d3555-110">如果您指定 Force 參數，則 Cmdlet 會取代現有的資料集，而無需確認。</span><span class="sxs-lookup"><span data-stu-id="d3555-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="d3555-111">依下列循序執行這些作業：--建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="d3555-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="d3555-112">--建立連結的服務。</span><span class="sxs-lookup"><span data-stu-id="d3555-112">-- Create linked services.</span></span>
<span data-ttu-id="d3555-113">--建立資料集。</span><span class="sxs-lookup"><span data-stu-id="d3555-113">-- Create datasets.</span></span>
<span data-ttu-id="d3555-114">--建立管線。</span><span class="sxs-lookup"><span data-stu-id="d3555-114">-- Create a pipeline.</span></span>
<span data-ttu-id="d3555-115">如果資料工廠中已存在具有相同名稱的資料集，此 Cmdlet 會提示您確認是否要使用新的資料集覆寫現有的資料集。</span><span class="sxs-lookup"><span data-stu-id="d3555-115">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="d3555-116">如果您確認覆寫現有的資料集，也會取代資料集定義。</span><span class="sxs-lookup"><span data-stu-id="d3555-116">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="d3555-117">示例</span><span class="sxs-lookup"><span data-stu-id="d3555-117">EXAMPLES</span></span>

### <span data-ttu-id="d3555-118">範例1：建立資料集</span><span class="sxs-lookup"><span data-stu-id="d3555-118">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="d3555-119">這個命令會在名為 WikiADF 的資料工廠中建立名為 DA_WikipediaClickEvents 的資料集。</span><span class="sxs-lookup"><span data-stu-id="d3555-119">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="d3555-120">此命令根據檔案中 DAWikipediaClickEvents.js的資訊來基礎。</span><span class="sxs-lookup"><span data-stu-id="d3555-120">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="d3555-121">參數</span><span class="sxs-lookup"><span data-stu-id="d3555-121">PARAMETERS</span></span>

### <span data-ttu-id="d3555-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d3555-122">-DataFactoryName</span></span>
<span data-ttu-id="d3555-123">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="d3555-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d3555-124">這個 Cmdlet 會在此參數指定的資料工廠中建立資料集。</span><span class="sxs-lookup"><span data-stu-id="d3555-124">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d3555-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3555-125">-DefaultProfile</span></span>
<span data-ttu-id="d3555-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d3555-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3555-127">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="d3555-127">-DefinitionFile</span></span>
<span data-ttu-id="d3555-128">JSON 檔路徑。</span><span class="sxs-lookup"><span data-stu-id="d3555-128">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3555-129">-Force</span><span class="sxs-lookup"><span data-stu-id="d3555-129">-Force</span></span>
<span data-ttu-id="d3555-130">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d3555-130">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d3555-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="d3555-131">-Name</span></span>
<span data-ttu-id="d3555-132">指定要建立的資料集名稱。</span><span class="sxs-lookup"><span data-stu-id="d3555-132">Specifies the name of the dataset to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3555-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3555-133">-ResourceGroupName</span></span>
<span data-ttu-id="d3555-134">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d3555-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d3555-135">這個 Cmdlet 會在此參數指定的群組中建立資料集。</span><span class="sxs-lookup"><span data-stu-id="d3555-135">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d3555-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3555-136">-ResourceId</span></span>
<span data-ttu-id="d3555-137">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d3555-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d3555-138">-確認</span><span class="sxs-lookup"><span data-stu-id="d3555-138">-Confirm</span></span>
<span data-ttu-id="d3555-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d3555-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3555-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3555-140">-WhatIf</span></span>
<span data-ttu-id="d3555-141">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d3555-141">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3555-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3555-142">CommonParameters</span></span>
<span data-ttu-id="d3555-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d3555-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3555-144">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d3555-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3555-145">輸入</span><span class="sxs-lookup"><span data-stu-id="d3555-145">INPUTS</span></span>

### <span data-ttu-id="d3555-146">System.object</span><span class="sxs-lookup"><span data-stu-id="d3555-146">System.String</span></span>

## <span data-ttu-id="d3555-147">輸出</span><span class="sxs-lookup"><span data-stu-id="d3555-147">OUTPUTS</span></span>

### <span data-ttu-id="d3555-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="d3555-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="d3555-149">筆記</span><span class="sxs-lookup"><span data-stu-id="d3555-149">NOTES</span></span>
<span data-ttu-id="d3555-150">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="d3555-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d3555-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="d3555-151">RELATED LINKS</span></span>

[<span data-ttu-id="d3555-152">AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="d3555-152">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="d3555-153">移除-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="d3555-153">Remove-AzDataFactoryV2Dataset</span></span>]()
