---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
ms.openlocfilehash: c3b15f198002ff11c936ad9e45a4dc87557329ab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622563"
---
# <span data-ttu-id="7d8bd-101">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="7d8bd-101">Set-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="7d8bd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d8bd-102">SYNOPSIS</span></span>
<span data-ttu-id="7d8bd-103">在資料工廠中建立資料集。</span><span class="sxs-lookup"><span data-stu-id="7d8bd-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="7d8bd-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d8bd-104">SYNTAX</span></span>

### <span data-ttu-id="7d8bd-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="7d8bd-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d8bd-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7d8bd-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d8bd-107">說明</span><span class="sxs-lookup"><span data-stu-id="7d8bd-107">DESCRIPTION</span></span>
<span data-ttu-id="7d8bd-108">Set-AzDataFactoryV2Dataset Cmdlet 會建立 Azure 資料工廠中的資料集。</span><span class="sxs-lookup"><span data-stu-id="7d8bd-108">The Set-AzDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="7d8bd-109">如果您為已存在的資料集指定名稱，此 Cmdlet 會在您取代資料集之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7d8bd-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="7d8bd-110">如果您指定 Force 參數，則 Cmdlet 會取代現有的資料集，而無需確認。</span><span class="sxs-lookup"><span data-stu-id="7d8bd-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="7d8bd-111">依下列循序執行這些作業：--建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="7d8bd-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="7d8bd-112">--建立連結的服務。</span><span class="sxs-lookup"><span data-stu-id="7d8bd-112">-- Create linked services.</span></span>
<span data-ttu-id="7d8bd-113">--建立資料集。</span><span class="sxs-lookup"><span data-stu-id="7d8bd-113">-- Create datasets.</span></span>
<span data-ttu-id="7d8bd-114">--建立管線。</span><span class="sxs-lookup"><span data-stu-id="7d8bd-114">-- Create a pipeline.</span></span>
<span data-ttu-id="7d8bd-115">如果資料工廠中已存在具有相同名稱的資料集，此 Cmdlet 會提示您確認是否要使用新的資料集覆寫現有的資料集。</span><span class="sxs-lookup"><span data-stu-id="7d8bd-115">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="7d8bd-116">如果您確認覆寫現有的資料集，也會取代資料集定義。</span><span class="sxs-lookup"><span data-stu-id="7d8bd-116">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="7d8bd-117">示例</span><span class="sxs-lookup"><span data-stu-id="7d8bd-117">EXAMPLES</span></span>

### <span data-ttu-id="7d8bd-118">範例1：建立資料集</span><span class="sxs-lookup"><span data-stu-id="7d8bd-118">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="7d8bd-119">這個命令會在名為 WikiADF 的資料工廠中建立名為 DA_WikipediaClickEvents 的資料集。</span><span class="sxs-lookup"><span data-stu-id="7d8bd-119">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="7d8bd-120">此命令根據檔案中 DAWikipediaClickEvents.js的資訊來基礎。</span><span class="sxs-lookup"><span data-stu-id="7d8bd-120">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="7d8bd-121">參數</span><span class="sxs-lookup"><span data-stu-id="7d8bd-121">PARAMETERS</span></span>

### <span data-ttu-id="7d8bd-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7d8bd-122">-DataFactoryName</span></span>
<span data-ttu-id="7d8bd-123">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="7d8bd-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="7d8bd-124">這個 Cmdlet 會在此參數指定的資料工廠中建立資料集。</span><span class="sxs-lookup"><span data-stu-id="7d8bd-124">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7d8bd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d8bd-125">-DefaultProfile</span></span>
<span data-ttu-id="7d8bd-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d8bd-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d8bd-127">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="7d8bd-127">-DefinitionFile</span></span>
<span data-ttu-id="7d8bd-128">JSON 檔路徑。</span><span class="sxs-lookup"><span data-stu-id="7d8bd-128">The JSON file path.</span></span>

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

### <span data-ttu-id="7d8bd-129">-Force</span><span class="sxs-lookup"><span data-stu-id="7d8bd-129">-Force</span></span>
<span data-ttu-id="7d8bd-130">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7d8bd-130">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="7d8bd-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="7d8bd-131">-Name</span></span>
<span data-ttu-id="7d8bd-132">指定要建立的資料集名稱。</span><span class="sxs-lookup"><span data-stu-id="7d8bd-132">Specifies the name of the dataset to create.</span></span>

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

### <span data-ttu-id="7d8bd-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d8bd-133">-ResourceGroupName</span></span>
<span data-ttu-id="7d8bd-134">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7d8bd-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7d8bd-135">這個 Cmdlet 會在此參數指定的群組中建立資料集。</span><span class="sxs-lookup"><span data-stu-id="7d8bd-135">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7d8bd-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d8bd-136">-ResourceId</span></span>
<span data-ttu-id="7d8bd-137">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7d8bd-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="7d8bd-138">-確認</span><span class="sxs-lookup"><span data-stu-id="7d8bd-138">-Confirm</span></span>
<span data-ttu-id="7d8bd-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7d8bd-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d8bd-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d8bd-140">-WhatIf</span></span>
<span data-ttu-id="7d8bd-141">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7d8bd-141">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="7d8bd-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d8bd-142">CommonParameters</span></span>
<span data-ttu-id="7d8bd-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d8bd-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d8bd-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7d8bd-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d8bd-145">輸入</span><span class="sxs-lookup"><span data-stu-id="7d8bd-145">INPUTS</span></span>

### <span data-ttu-id="7d8bd-146">System.object</span><span class="sxs-lookup"><span data-stu-id="7d8bd-146">System.String</span></span>

## <span data-ttu-id="7d8bd-147">輸出</span><span class="sxs-lookup"><span data-stu-id="7d8bd-147">OUTPUTS</span></span>

### <span data-ttu-id="7d8bd-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="7d8bd-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="7d8bd-149">筆記</span><span class="sxs-lookup"><span data-stu-id="7d8bd-149">NOTES</span></span>
<span data-ttu-id="7d8bd-150">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="7d8bd-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7d8bd-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d8bd-151">RELATED LINKS</span></span>

[<span data-ttu-id="7d8bd-152">AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="7d8bd-152">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="7d8bd-153">移除-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="7d8bd-153">Remove-AzDataFactoryV2Dataset</span></span>]()
