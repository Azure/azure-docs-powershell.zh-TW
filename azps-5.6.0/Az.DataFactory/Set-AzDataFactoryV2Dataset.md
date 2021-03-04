---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 5ea766b4c35e23a62a0764320a2f0491ea151586
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916193"
---
# <span data-ttu-id="9fcd8-101">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="9fcd8-101">Set-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="9fcd8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9fcd8-102">SYNOPSIS</span></span>
<span data-ttu-id="9fcd8-103">在 Data Factory 中建立資料集。</span><span class="sxs-lookup"><span data-stu-id="9fcd8-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="9fcd8-104">語法</span><span class="sxs-lookup"><span data-stu-id="9fcd8-104">SYNTAX</span></span>

### <span data-ttu-id="9fcd8-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="9fcd8-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9fcd8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9fcd8-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fcd8-107">描述</span><span class="sxs-lookup"><span data-stu-id="9fcd8-107">DESCRIPTION</span></span>
<span data-ttu-id="9fcd8-108">Cmdlet Set-AzDataFactoryV2Dataset Azure Data Factory 中建立資料集。</span><span class="sxs-lookup"><span data-stu-id="9fcd8-108">The Set-AzDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="9fcd8-109">如果您為已存在的資料集指定名稱，此 Cmdlet 會先提示您確認，然後再取代資料集。</span><span class="sxs-lookup"><span data-stu-id="9fcd8-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="9fcd8-110">如果您指定 Force 參數，Cmdlet 會取代現有的資料集而不確認。</span><span class="sxs-lookup"><span data-stu-id="9fcd8-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="9fcd8-111">請以下列循序執行這些作業：建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="9fcd8-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="9fcd8-112">-- 建立連結服務。</span><span class="sxs-lookup"><span data-stu-id="9fcd8-112">-- Create linked services.</span></span>
<span data-ttu-id="9fcd8-113">-- 建立資料集。</span><span class="sxs-lookup"><span data-stu-id="9fcd8-113">-- Create datasets.</span></span>
<span data-ttu-id="9fcd8-114">-- 建立管線。</span><span class="sxs-lookup"><span data-stu-id="9fcd8-114">-- Create a pipeline.</span></span>
<span data-ttu-id="9fcd8-115">如果資料工廠中已存在相同名稱的資料集，此 Cmdlet 會提示您確認是否要以新資料集覆寫現有的資料集。</span><span class="sxs-lookup"><span data-stu-id="9fcd8-115">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="9fcd8-116">如果您確認覆寫現有的資料集，也會取代資料集定義。</span><span class="sxs-lookup"><span data-stu-id="9fcd8-116">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="9fcd8-117">例子</span><span class="sxs-lookup"><span data-stu-id="9fcd8-117">EXAMPLES</span></span>

### <span data-ttu-id="9fcd8-118">範例 1：建立資料集</span><span class="sxs-lookup"><span data-stu-id="9fcd8-118">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="9fcd8-119">此命令在名為 WikiADF 的資料DA_WikipediaClickEvents中建立名為 wikiADF 的資料集。</span><span class="sxs-lookup"><span data-stu-id="9fcd8-119">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="9fcd8-120">命令以檔案中資料DAWikipediaClickEvents.js基礎。</span><span class="sxs-lookup"><span data-stu-id="9fcd8-120">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="9fcd8-121">參數</span><span class="sxs-lookup"><span data-stu-id="9fcd8-121">PARAMETERS</span></span>

### <span data-ttu-id="9fcd8-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9fcd8-122">-DataFactoryName</span></span>
<span data-ttu-id="9fcd8-123">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="9fcd8-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9fcd8-124">此 Cmdlet 會在此參數指定的資料工廠中建立資料集。</span><span class="sxs-lookup"><span data-stu-id="9fcd8-124">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9fcd8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fcd8-125">-DefaultProfile</span></span>
<span data-ttu-id="9fcd8-126">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9fcd8-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fcd8-127">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="9fcd8-127">-DefinitionFile</span></span>
<span data-ttu-id="9fcd8-128">JSON 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="9fcd8-128">The JSON file path.</span></span>

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

### <span data-ttu-id="9fcd8-129">-強制</span><span class="sxs-lookup"><span data-stu-id="9fcd8-129">-Force</span></span>
<span data-ttu-id="9fcd8-130">執行 Cmdlet 而不提示確認。</span><span class="sxs-lookup"><span data-stu-id="9fcd8-130">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="9fcd8-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="9fcd8-131">-Name</span></span>
<span data-ttu-id="9fcd8-132">指定要建立之資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="9fcd8-132">Specifies the name of the dataset to create.</span></span>

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

### <span data-ttu-id="9fcd8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fcd8-133">-ResourceGroupName</span></span>
<span data-ttu-id="9fcd8-134">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9fcd8-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9fcd8-135">此 Cmdlet 會在此參數指定的群組中建立資料集。</span><span class="sxs-lookup"><span data-stu-id="9fcd8-135">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9fcd8-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fcd8-136">-ResourceId</span></span>
<span data-ttu-id="9fcd8-137">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9fcd8-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="9fcd8-138">-確認</span><span class="sxs-lookup"><span data-stu-id="9fcd8-138">-Confirm</span></span>
<span data-ttu-id="9fcd8-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9fcd8-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fcd8-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fcd8-140">-WhatIf</span></span>
<span data-ttu-id="9fcd8-141">顯示如果 Cmdlet 執行，但不執行 Cmdlet 會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9fcd8-141">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="9fcd8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fcd8-142">CommonParameters</span></span>
<span data-ttu-id="9fcd8-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9fcd8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fcd8-144">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="9fcd8-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fcd8-145">輸入</span><span class="sxs-lookup"><span data-stu-id="9fcd8-145">INPUTS</span></span>

### <span data-ttu-id="9fcd8-146">System.String</span><span class="sxs-lookup"><span data-stu-id="9fcd8-146">System.String</span></span>

## <span data-ttu-id="9fcd8-147">輸出</span><span class="sxs-lookup"><span data-stu-id="9fcd8-147">OUTPUTS</span></span>

### <span data-ttu-id="9fcd8-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="9fcd8-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="9fcd8-149">筆記</span><span class="sxs-lookup"><span data-stu-id="9fcd8-149">NOTES</span></span>
<span data-ttu-id="9fcd8-150">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="9fcd8-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9fcd8-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="9fcd8-151">RELATED LINKS</span></span>

[<span data-ttu-id="9fcd8-152">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="9fcd8-152">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="9fcd8-153">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="9fcd8-153">Remove-AzDataFactoryV2Dataset</span></span>]()
