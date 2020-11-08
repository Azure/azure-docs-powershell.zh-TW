---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
ms.openlocfilehash: e8917b9c68cb0708d34faa0e0dfec8e0e912f54b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128786"
---
# <span data-ttu-id="e5eac-101">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="e5eac-101">New-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="e5eac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5eac-102">SYNOPSIS</span></span>
<span data-ttu-id="e5eac-103">在資料工廠中建立管線。</span><span class="sxs-lookup"><span data-stu-id="e5eac-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="e5eac-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5eac-104">SYNTAX</span></span>

### <span data-ttu-id="e5eac-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="e5eac-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5eac-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e5eac-106">ByFactoryObject</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5eac-107">說明</span><span class="sxs-lookup"><span data-stu-id="e5eac-107">DESCRIPTION</span></span>
<span data-ttu-id="e5eac-108">**新的-AzDataFactoryPipeline** Cmdlet 會在 Azure 資料工廠中建立管線。</span><span class="sxs-lookup"><span data-stu-id="e5eac-108">The **New-AzDataFactoryPipeline** cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="e5eac-109">如果您為已存在的管線指定名稱，則此 Cmdlet 會在您取代管線之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e5eac-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="e5eac-110">如果您指定 *Force* 參數，則 Cmdlet 會取代現有的管線，而無需確認。</span><span class="sxs-lookup"><span data-stu-id="e5eac-110">If you specify the *Force* parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="e5eac-111">依下列循序執行這些作業：</span><span class="sxs-lookup"><span data-stu-id="e5eac-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="e5eac-112">建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="e5eac-112">Create a data factory.</span></span> 
- <span data-ttu-id="e5eac-113">建立連結的服務。</span><span class="sxs-lookup"><span data-stu-id="e5eac-113">Create linked services.</span></span> 
- <span data-ttu-id="e5eac-114">建立資料集。</span><span class="sxs-lookup"><span data-stu-id="e5eac-114">Create datasets.</span></span> 
- <span data-ttu-id="e5eac-115">建立管線。</span><span class="sxs-lookup"><span data-stu-id="e5eac-115">Create a pipeline.</span></span>
<span data-ttu-id="e5eac-116">如果資料工廠中已經有相同名稱的管線，這個 Cmdlet 會提示您確認是否要使用新的管線覆寫現有管線。</span><span class="sxs-lookup"><span data-stu-id="e5eac-116">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="e5eac-117">如果您確認覆寫現有的管線，也會取代管線定義。</span><span class="sxs-lookup"><span data-stu-id="e5eac-117">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="e5eac-118">示例</span><span class="sxs-lookup"><span data-stu-id="e5eac-118">EXAMPLES</span></span>

### <span data-ttu-id="e5eac-119">範例1：建立管線</span><span class="sxs-lookup"><span data-stu-id="e5eac-119">Example 1: Create a pipeline</span></span>
```
PS C:\>New-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="e5eac-120">這個命令會在名為 [ADF] 的資料工廠中建立名為 DPWikisample 的管線。</span><span class="sxs-lookup"><span data-stu-id="e5eac-120">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="e5eac-121">該命令根據檔案中 DPWikisample.js的資訊來基礎。</span><span class="sxs-lookup"><span data-stu-id="e5eac-121">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="e5eac-122">此檔案包含有關活動的資訊，例如在管線中複製活動和 HDInsight 活動。</span><span class="sxs-lookup"><span data-stu-id="e5eac-122">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="e5eac-123">參數</span><span class="sxs-lookup"><span data-stu-id="e5eac-123">PARAMETERS</span></span>

### <span data-ttu-id="e5eac-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e5eac-124">-DataFactory</span></span>
<span data-ttu-id="e5eac-125">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="e5eac-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="e5eac-126">這個 Cmdlet 會針對此參數指定的資料工廠建立管線。</span><span class="sxs-lookup"><span data-stu-id="e5eac-126">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e5eac-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e5eac-127">-DataFactoryName</span></span>
<span data-ttu-id="e5eac-128">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5eac-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e5eac-129">這個 Cmdlet 會針對此參數指定的資料工廠建立管線。</span><span class="sxs-lookup"><span data-stu-id="e5eac-129">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e5eac-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5eac-130">-DefaultProfile</span></span>
<span data-ttu-id="e5eac-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e5eac-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5eac-132">檔案</span><span class="sxs-lookup"><span data-stu-id="e5eac-132">-File</span></span>
<span data-ttu-id="e5eac-133">指定包含管線描述的 JavaScript 物件符號 (JSON) 檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="e5eac-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the pipeline.</span></span>

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

### <span data-ttu-id="e5eac-134">-Force</span><span class="sxs-lookup"><span data-stu-id="e5eac-134">-Force</span></span>
<span data-ttu-id="e5eac-135">表示此 Cmdlet 會取代現有的管線，而不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e5eac-135">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="e5eac-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="e5eac-136">-Name</span></span>
<span data-ttu-id="e5eac-137">指定要建立的管線名稱。</span><span class="sxs-lookup"><span data-stu-id="e5eac-137">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5eac-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5eac-138">-ResourceGroupName</span></span>
<span data-ttu-id="e5eac-139">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5eac-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e5eac-140">這個 Cmdlet 會針對此參數指定的群組建立管線。</span><span class="sxs-lookup"><span data-stu-id="e5eac-140">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e5eac-141">-確認</span><span class="sxs-lookup"><span data-stu-id="e5eac-141">-Confirm</span></span>
<span data-ttu-id="e5eac-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e5eac-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5eac-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5eac-143">-WhatIf</span></span>
<span data-ttu-id="e5eac-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e5eac-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5eac-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5eac-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5eac-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5eac-146">CommonParameters</span></span>
<span data-ttu-id="e5eac-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5eac-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5eac-148">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e5eac-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5eac-149">輸入</span><span class="sxs-lookup"><span data-stu-id="e5eac-149">INPUTS</span></span>

### <span data-ttu-id="e5eac-150">System.object</span><span class="sxs-lookup"><span data-stu-id="e5eac-150">System.String</span></span>

### <span data-ttu-id="e5eac-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e5eac-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="e5eac-152">輸出</span><span class="sxs-lookup"><span data-stu-id="e5eac-152">OUTPUTS</span></span>

### <span data-ttu-id="e5eac-153">PSPipeline 中的 DataFactories。</span><span class="sxs-lookup"><span data-stu-id="e5eac-153">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="e5eac-154">筆記</span><span class="sxs-lookup"><span data-stu-id="e5eac-154">NOTES</span></span>
* <span data-ttu-id="e5eac-155">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="e5eac-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e5eac-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5eac-156">RELATED LINKS</span></span>

[<span data-ttu-id="e5eac-157">AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="e5eac-157">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="e5eac-158">移除-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="e5eac-158">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="e5eac-159">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="e5eac-159">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="e5eac-160">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="e5eac-160">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="e5eac-161">暫停-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="e5eac-161">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)

