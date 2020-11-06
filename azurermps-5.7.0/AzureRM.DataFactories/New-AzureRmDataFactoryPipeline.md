---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: dbdefb2e6fa419898447c17053f58631b35a906d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449895"
---
# <span data-ttu-id="a803d-101">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a803d-101">New-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="a803d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a803d-102">SYNOPSIS</span></span>
<span data-ttu-id="a803d-103">在資料工廠中建立管線。</span><span class="sxs-lookup"><span data-stu-id="a803d-103">Creates a pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a803d-104">句法</span><span class="sxs-lookup"><span data-stu-id="a803d-104">SYNTAX</span></span>

### <span data-ttu-id="a803d-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="a803d-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a803d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a803d-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a803d-107">說明</span><span class="sxs-lookup"><span data-stu-id="a803d-107">DESCRIPTION</span></span>
<span data-ttu-id="a803d-108">**新的-AzureRmDataFactoryPipeline** Cmdlet 會在 Azure 資料工廠中建立管線。</span><span class="sxs-lookup"><span data-stu-id="a803d-108">The **New-AzureRmDataFactoryPipeline** cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="a803d-109">如果您為已存在的管線指定名稱，則此 Cmdlet 會在您取代管線之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a803d-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="a803d-110">如果您指定 *Force* 參數，則 Cmdlet 會取代現有的管線，而無需確認。</span><span class="sxs-lookup"><span data-stu-id="a803d-110">If you specify the *Force* parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>

<span data-ttu-id="a803d-111">依下列循序執行這些作業：</span><span class="sxs-lookup"><span data-stu-id="a803d-111">Perform these operations in the following order:</span></span> 

- <span data-ttu-id="a803d-112">建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="a803d-112">Create a data factory.</span></span> 
- <span data-ttu-id="a803d-113">建立連結的服務。</span><span class="sxs-lookup"><span data-stu-id="a803d-113">Create linked services.</span></span> 
- <span data-ttu-id="a803d-114">建立資料集。</span><span class="sxs-lookup"><span data-stu-id="a803d-114">Create datasets.</span></span> 
- <span data-ttu-id="a803d-115">建立管線。</span><span class="sxs-lookup"><span data-stu-id="a803d-115">Create a pipeline.</span></span>

<span data-ttu-id="a803d-116">如果資料工廠中已經有相同名稱的管線，這個 Cmdlet 會提示您確認是否要使用新的管線覆寫現有管線。</span><span class="sxs-lookup"><span data-stu-id="a803d-116">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="a803d-117">如果您確認覆寫現有的管線，也會取代管線定義。</span><span class="sxs-lookup"><span data-stu-id="a803d-117">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="a803d-118">示例</span><span class="sxs-lookup"><span data-stu-id="a803d-118">EXAMPLES</span></span>

### <span data-ttu-id="a803d-119">範例1：建立管線</span><span class="sxs-lookup"><span data-stu-id="a803d-119">Example 1: Create a pipeline</span></span>
```
PS C:\>New-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="a803d-120">這個命令會在名為 [ADF] 的資料工廠中建立名為 DPWikisample 的管線。</span><span class="sxs-lookup"><span data-stu-id="a803d-120">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="a803d-121">該命令根據檔案中 DPWikisample.js的資訊來基礎。</span><span class="sxs-lookup"><span data-stu-id="a803d-121">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="a803d-122">此檔案包含有關活動的資訊，例如在管線中複製活動和 HDInsight 活動。</span><span class="sxs-lookup"><span data-stu-id="a803d-122">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="a803d-123">參數</span><span class="sxs-lookup"><span data-stu-id="a803d-123">PARAMETERS</span></span>

### <span data-ttu-id="a803d-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a803d-124">-DataFactory</span></span>
<span data-ttu-id="a803d-125">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="a803d-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="a803d-126">這個 Cmdlet 會針對此參數指定的資料工廠建立管線。</span><span class="sxs-lookup"><span data-stu-id="a803d-126">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a803d-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a803d-127">-DataFactoryName</span></span>
<span data-ttu-id="a803d-128">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="a803d-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a803d-129">這個 Cmdlet 會針對此參數指定的資料工廠建立管線。</span><span class="sxs-lookup"><span data-stu-id="a803d-129">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a803d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a803d-130">-DefaultProfile</span></span>
<span data-ttu-id="a803d-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a803d-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a803d-132">檔案</span><span class="sxs-lookup"><span data-stu-id="a803d-132">-File</span></span>
<span data-ttu-id="a803d-133">指定包含管線描述的 JavaScript 物件符號 (JSON) 檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="a803d-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a803d-134">-Force</span><span class="sxs-lookup"><span data-stu-id="a803d-134">-Force</span></span>
<span data-ttu-id="a803d-135">表示此 Cmdlet 會取代現有的管線，而不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a803d-135">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="a803d-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="a803d-136">-Name</span></span>
<span data-ttu-id="a803d-137">指定要建立的管線名稱。</span><span class="sxs-lookup"><span data-stu-id="a803d-137">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a803d-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a803d-138">-ResourceGroupName</span></span>
<span data-ttu-id="a803d-139">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a803d-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a803d-140">這個 Cmdlet 會針對此參數指定的群組建立管線。</span><span class="sxs-lookup"><span data-stu-id="a803d-140">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a803d-141">-確認</span><span class="sxs-lookup"><span data-stu-id="a803d-141">-Confirm</span></span>
<span data-ttu-id="a803d-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a803d-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a803d-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a803d-143">-WhatIf</span></span>
<span data-ttu-id="a803d-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a803d-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a803d-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a803d-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a803d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a803d-146">CommonParameters</span></span>
<span data-ttu-id="a803d-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a803d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a803d-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a803d-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a803d-149">輸入</span><span class="sxs-lookup"><span data-stu-id="a803d-149">INPUTS</span></span>

### <span data-ttu-id="a803d-150">所有</span><span class="sxs-lookup"><span data-stu-id="a803d-150">None</span></span>
<span data-ttu-id="a803d-151">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="a803d-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a803d-152">輸出</span><span class="sxs-lookup"><span data-stu-id="a803d-152">OUTPUTS</span></span>

### <span data-ttu-id="a803d-153">PSPipeline 中的 WindowsAzure</span><span class="sxs-lookup"><span data-stu-id="a803d-153">Microsoft.WindowsAzure.Commands.Utilities.PSPipeline</span></span>

## <span data-ttu-id="a803d-154">筆記</span><span class="sxs-lookup"><span data-stu-id="a803d-154">NOTES</span></span>
* <span data-ttu-id="a803d-155">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="a803d-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a803d-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="a803d-156">RELATED LINKS</span></span>

[<span data-ttu-id="a803d-157">AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a803d-157">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="a803d-158">移除-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a803d-158">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="a803d-159">Resume-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a803d-159">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="a803d-160">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="a803d-160">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="a803d-161">暫停-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a803d-161">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


