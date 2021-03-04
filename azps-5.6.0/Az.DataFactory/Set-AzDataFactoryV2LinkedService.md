---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: 81894fb7aca1cd546988d94d93b14860061863f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916190"
---
# <span data-ttu-id="5fbf6-101">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="5fbf6-101">Set-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="5fbf6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5fbf6-102">SYNOPSIS</span></span>
<span data-ttu-id="5fbf6-103">將資料存放區或雲端服務連結至 Data Factory。</span><span class="sxs-lookup"><span data-stu-id="5fbf6-103">Links a data store or a cloud service to Data Factory.</span></span>

## <span data-ttu-id="5fbf6-104">語法</span><span class="sxs-lookup"><span data-stu-id="5fbf6-104">SYNTAX</span></span>

### <span data-ttu-id="5fbf6-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="5fbf6-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5fbf6-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5fbf6-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fbf6-107">描述</span><span class="sxs-lookup"><span data-stu-id="5fbf6-107">DESCRIPTION</span></span>
<span data-ttu-id="5fbf6-108">Cmdlet Set-AzDataFactoryV2LinkedService連結資料存放區或雲端服務至 Azure Data Factory。</span><span class="sxs-lookup"><span data-stu-id="5fbf6-108">The Set-AzDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="5fbf6-109">如果您為已存在的連結服務指定名稱，此 Cmdlet 會先提示您確認，然後再取代連結的服務。</span><span class="sxs-lookup"><span data-stu-id="5fbf6-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="5fbf6-110">如果您指定 Force 參數，Cmdlet 會取代現有的連結服務，而不需要確認。</span><span class="sxs-lookup"><span data-stu-id="5fbf6-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="5fbf6-111">請以下列循序執行這些作業：建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="5fbf6-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="5fbf6-112">-- 建立連結服務。</span><span class="sxs-lookup"><span data-stu-id="5fbf6-112">-- Create linked services.</span></span>
<span data-ttu-id="5fbf6-113">-- 建立資料集。</span><span class="sxs-lookup"><span data-stu-id="5fbf6-113">-- Create datasets.</span></span>
<span data-ttu-id="5fbf6-114">-- 建立管線。</span><span class="sxs-lookup"><span data-stu-id="5fbf6-114">-- Create a pipeline.</span></span>

## <span data-ttu-id="5fbf6-115">例子</span><span class="sxs-lookup"><span data-stu-id="5fbf6-115">EXAMPLES</span></span>

### <span data-ttu-id="5fbf6-116">範例 1：建立連結服務</span><span class="sxs-lookup"><span data-stu-id="5fbf6-116">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="5fbf6-117">此命令在名為 WikiADF 的資料工廠中，建立一個名為 LinkedServiceCuratedWikiData 的連結服務。</span><span class="sxs-lookup"><span data-stu-id="5fbf6-117">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="5fbf6-118">此連結服務會連結檔案中指定的 Azure Blob 存放區至名為 WikiADF 的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="5fbf6-118">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="5fbf6-119">該命令會使用管線運算子Format-List Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5fbf6-119">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5fbf6-120">Windows PowerShell Cmdlet 會格式化結果。</span><span class="sxs-lookup"><span data-stu-id="5fbf6-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="5fbf6-121">詳細資訊，輸入Get-Help格式清單。</span><span class="sxs-lookup"><span data-stu-id="5fbf6-121">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="5fbf6-122">參數</span><span class="sxs-lookup"><span data-stu-id="5fbf6-122">PARAMETERS</span></span>

### <span data-ttu-id="5fbf6-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5fbf6-123">-DataFactoryName</span></span>
<span data-ttu-id="5fbf6-124">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="5fbf6-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="5fbf6-125">此 Cmdlet 會為此參數指定的資料工廠建立連結服務。</span><span class="sxs-lookup"><span data-stu-id="5fbf6-125">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5fbf6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fbf6-126">-DefaultProfile</span></span>
<span data-ttu-id="5fbf6-127">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5fbf6-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fbf6-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="5fbf6-128">-DefinitionFile</span></span>
<span data-ttu-id="5fbf6-129">JSON 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="5fbf6-129">The JSON file path.</span></span>

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

### <span data-ttu-id="5fbf6-130">-強制</span><span class="sxs-lookup"><span data-stu-id="5fbf6-130">-Force</span></span>
<span data-ttu-id="5fbf6-131">執行 Cmdlet 而不提示確認。</span><span class="sxs-lookup"><span data-stu-id="5fbf6-131">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="5fbf6-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="5fbf6-132">-Name</span></span>
<span data-ttu-id="5fbf6-133">指定要建立的連結服務名稱。</span><span class="sxs-lookup"><span data-stu-id="5fbf6-133">Specifies the name of the linked service to create.</span></span>

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

### <span data-ttu-id="5fbf6-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fbf6-134">-ResourceGroupName</span></span>
<span data-ttu-id="5fbf6-135">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5fbf6-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5fbf6-136">此 Cmdlet 會為此參數指定的群組建立連結服務。</span><span class="sxs-lookup"><span data-stu-id="5fbf6-136">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5fbf6-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fbf6-137">-ResourceId</span></span>
<span data-ttu-id="5fbf6-138">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5fbf6-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5fbf6-139">-確認</span><span class="sxs-lookup"><span data-stu-id="5fbf6-139">-Confirm</span></span>
<span data-ttu-id="5fbf6-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5fbf6-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fbf6-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fbf6-141">-WhatIf</span></span>
<span data-ttu-id="5fbf6-142">顯示如果 Cmdlet 執行，但不執行 Cmdlet 會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5fbf6-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="5fbf6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fbf6-143">CommonParameters</span></span>
<span data-ttu-id="5fbf6-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5fbf6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fbf6-145">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5fbf6-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fbf6-146">輸入</span><span class="sxs-lookup"><span data-stu-id="5fbf6-146">INPUTS</span></span>

### <span data-ttu-id="5fbf6-147">System.String</span><span class="sxs-lookup"><span data-stu-id="5fbf6-147">System.String</span></span>

## <span data-ttu-id="5fbf6-148">輸出</span><span class="sxs-lookup"><span data-stu-id="5fbf6-148">OUTPUTS</span></span>

### <span data-ttu-id="5fbf6-149">Microsoft.Azure.Commands.DataFactoryV2.models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="5fbf6-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="5fbf6-150">筆記</span><span class="sxs-lookup"><span data-stu-id="5fbf6-150">NOTES</span></span>
<span data-ttu-id="5fbf6-151">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="5fbf6-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5fbf6-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="5fbf6-152">RELATED LINKS</span></span>

[<span data-ttu-id="5fbf6-153">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="5fbf6-153">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="5fbf6-154">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="5fbf6-154">Remove-AzDataFactoryV2LinkedService</span></span>]()
