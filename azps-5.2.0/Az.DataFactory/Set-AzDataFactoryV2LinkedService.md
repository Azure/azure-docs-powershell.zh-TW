---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: d6fd12e96a98d0771a984aa5234013dbe4a548af
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281444"
---
# <span data-ttu-id="ecd44-101">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="ecd44-101">Set-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="ecd44-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ecd44-102">SYNOPSIS</span></span>
<span data-ttu-id="ecd44-103">將資料存放區或雲端服務連結至資料工廠。</span><span class="sxs-lookup"><span data-stu-id="ecd44-103">Links a data store or a cloud service to Data Factory.</span></span>

## <span data-ttu-id="ecd44-104">句法</span><span class="sxs-lookup"><span data-stu-id="ecd44-104">SYNTAX</span></span>

### <span data-ttu-id="ecd44-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="ecd44-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ecd44-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ecd44-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecd44-107">說明</span><span class="sxs-lookup"><span data-stu-id="ecd44-107">DESCRIPTION</span></span>
<span data-ttu-id="ecd44-108">Set-AzDataFactoryV2LinkedService Cmdlet 會將資料存放區或雲端服務連結至 Azure 資料工廠。</span><span class="sxs-lookup"><span data-stu-id="ecd44-108">The Set-AzDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="ecd44-109">如果您指定已存在之連結服務的名稱，此 Cmdlet 會在您替換連結的服務之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ecd44-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="ecd44-110">如果您指定 Force 參數，則 Cmdlet 會取代現有的連結服務而不進行確認。</span><span class="sxs-lookup"><span data-stu-id="ecd44-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="ecd44-111">依下列循序執行這些作業：--建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="ecd44-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="ecd44-112">--建立連結的服務。</span><span class="sxs-lookup"><span data-stu-id="ecd44-112">-- Create linked services.</span></span>
<span data-ttu-id="ecd44-113">--建立資料集。</span><span class="sxs-lookup"><span data-stu-id="ecd44-113">-- Create datasets.</span></span>
<span data-ttu-id="ecd44-114">--建立管線。</span><span class="sxs-lookup"><span data-stu-id="ecd44-114">-- Create a pipeline.</span></span>

## <span data-ttu-id="ecd44-115">示例</span><span class="sxs-lookup"><span data-stu-id="ecd44-115">EXAMPLES</span></span>

### <span data-ttu-id="ecd44-116">範例1：建立連結的服務</span><span class="sxs-lookup"><span data-stu-id="ecd44-116">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="ecd44-117">這個命令會在名為 WikiADF 的資料工廠中建立名為 LinkedServiceCuratedWikiData 的連結服務。</span><span class="sxs-lookup"><span data-stu-id="ecd44-117">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="ecd44-118">這個連結的服務會將檔案中指定的 Azure blob 存放區連結到名為 WikiADF 的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="ecd44-118">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="ecd44-119">命令會使用管線運算子，將結果傳遞到 Format-List Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ecd44-119">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ecd44-120">該 Windows PowerShell Cmdlet 會格式化結果。</span><span class="sxs-lookup"><span data-stu-id="ecd44-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="ecd44-121">如需詳細資訊，請輸入 Get-Help 格式-清單。</span><span class="sxs-lookup"><span data-stu-id="ecd44-121">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="ecd44-122">參數</span><span class="sxs-lookup"><span data-stu-id="ecd44-122">PARAMETERS</span></span>

### <span data-ttu-id="ecd44-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ecd44-123">-DataFactoryName</span></span>
<span data-ttu-id="ecd44-124">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="ecd44-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ecd44-125">這個 Cmdlet 會針對此參數指定的資料工廠建立連結的服務。</span><span class="sxs-lookup"><span data-stu-id="ecd44-125">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ecd44-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecd44-126">-DefaultProfile</span></span>
<span data-ttu-id="ecd44-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ecd44-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecd44-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="ecd44-128">-DefinitionFile</span></span>
<span data-ttu-id="ecd44-129">JSON 檔路徑。</span><span class="sxs-lookup"><span data-stu-id="ecd44-129">The JSON file path.</span></span>

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

### <span data-ttu-id="ecd44-130">-Force</span><span class="sxs-lookup"><span data-stu-id="ecd44-130">-Force</span></span>
<span data-ttu-id="ecd44-131">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ecd44-131">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ecd44-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="ecd44-132">-Name</span></span>
<span data-ttu-id="ecd44-133">指定要建立之連結服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="ecd44-133">Specifies the name of the linked service to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecd44-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecd44-134">-ResourceGroupName</span></span>
<span data-ttu-id="ecd44-135">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ecd44-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ecd44-136">這個 Cmdlet 會針對此參數指定的群組建立連結的服務。</span><span class="sxs-lookup"><span data-stu-id="ecd44-136">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ecd44-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecd44-137">-ResourceId</span></span>
<span data-ttu-id="ecd44-138">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ecd44-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ecd44-139">-確認</span><span class="sxs-lookup"><span data-stu-id="ecd44-139">-Confirm</span></span>
<span data-ttu-id="ecd44-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ecd44-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecd44-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecd44-141">-WhatIf</span></span>
<span data-ttu-id="ecd44-142">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ecd44-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ecd44-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecd44-143">CommonParameters</span></span>
<span data-ttu-id="ecd44-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ecd44-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecd44-145">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ecd44-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecd44-146">輸入</span><span class="sxs-lookup"><span data-stu-id="ecd44-146">INPUTS</span></span>

### <span data-ttu-id="ecd44-147">System.object</span><span class="sxs-lookup"><span data-stu-id="ecd44-147">System.String</span></span>

## <span data-ttu-id="ecd44-148">輸出</span><span class="sxs-lookup"><span data-stu-id="ecd44-148">OUTPUTS</span></span>

### <span data-ttu-id="ecd44-149">PSLinkedService 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="ecd44-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="ecd44-150">筆記</span><span class="sxs-lookup"><span data-stu-id="ecd44-150">NOTES</span></span>
<span data-ttu-id="ecd44-151">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="ecd44-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ecd44-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="ecd44-152">RELATED LINKS</span></span>

[<span data-ttu-id="ecd44-153">AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="ecd44-153">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="ecd44-154">移除-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="ecd44-154">Remove-AzDataFactoryV2LinkedService</span></span>]()
