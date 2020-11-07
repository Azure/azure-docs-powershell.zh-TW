---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: 2f7cfba7db5d675a73d21d6cd1814c13a1998ab1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623827"
---
# <span data-ttu-id="b491f-101">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="b491f-101">Set-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="b491f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b491f-102">SYNOPSIS</span></span>
<span data-ttu-id="b491f-103">將資料存放區或雲端服務連結至資料工廠。</span><span class="sxs-lookup"><span data-stu-id="b491f-103">Links a data store or a cloud service to Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b491f-104">句法</span><span class="sxs-lookup"><span data-stu-id="b491f-104">SYNTAX</span></span>

### <span data-ttu-id="b491f-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="b491f-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b491f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b491f-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b491f-107">說明</span><span class="sxs-lookup"><span data-stu-id="b491f-107">DESCRIPTION</span></span>
<span data-ttu-id="b491f-108">Set-AzureRmDataFactoryV2LinkedService Cmdlet 會將資料存放區或雲端服務連結至 Azure 資料工廠。</span><span class="sxs-lookup"><span data-stu-id="b491f-108">The Set-AzureRmDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="b491f-109">如果您指定已存在之連結服務的名稱，此 Cmdlet 會在您替換連結的服務之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b491f-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="b491f-110">如果您指定 Force 參數，則 Cmdlet 會取代現有的連結服務而不進行確認。</span><span class="sxs-lookup"><span data-stu-id="b491f-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>

<span data-ttu-id="b491f-111">依下列循序執行這些作業：</span><span class="sxs-lookup"><span data-stu-id="b491f-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="b491f-112">示例</span><span class="sxs-lookup"><span data-stu-id="b491f-112">EXAMPLES</span></span>

### <span data-ttu-id="b491f-113">範例1：建立連結的服務</span><span class="sxs-lookup"><span data-stu-id="b491f-113">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="b491f-114">這個命令會在名為 WikiADF 的資料工廠中建立名為 LinkedServiceCuratedWikiData 的連結服務。</span><span class="sxs-lookup"><span data-stu-id="b491f-114">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="b491f-115">這個連結的服務會將檔案中指定的 Azure blob 存放區連結到名為 WikiADF 的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="b491f-115">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="b491f-116">命令會使用管線運算子，將結果傳遞到 Format-List Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b491f-116">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b491f-117">該 Windows PowerShell Cmdlet 會格式化結果。</span><span class="sxs-lookup"><span data-stu-id="b491f-117">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="b491f-118">如需詳細資訊，請輸入 Get-Help 格式-清單。</span><span class="sxs-lookup"><span data-stu-id="b491f-118">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="b491f-119">參數</span><span class="sxs-lookup"><span data-stu-id="b491f-119">PARAMETERS</span></span>

### <span data-ttu-id="b491f-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b491f-120">-DataFactoryName</span></span>
<span data-ttu-id="b491f-121">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="b491f-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b491f-122">這個 Cmdlet 會針對此參數指定的資料工廠建立連結的服務。</span><span class="sxs-lookup"><span data-stu-id="b491f-122">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b491f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b491f-123">-DefaultProfile</span></span>
<span data-ttu-id="b491f-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b491f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b491f-125">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="b491f-125">-DefinitionFile</span></span>
<span data-ttu-id="b491f-126">JSON 檔路徑。</span><span class="sxs-lookup"><span data-stu-id="b491f-126">The JSON file path.</span></span>

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

### <span data-ttu-id="b491f-127">-Force</span><span class="sxs-lookup"><span data-stu-id="b491f-127">-Force</span></span>
<span data-ttu-id="b491f-128">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b491f-128">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b491f-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="b491f-129">-Name</span></span>
<span data-ttu-id="b491f-130">指定要建立之連結服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="b491f-130">Specifies the name of the linked service to create.</span></span>

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

### <span data-ttu-id="b491f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b491f-131">-ResourceGroupName</span></span>
<span data-ttu-id="b491f-132">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b491f-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b491f-133">這個 Cmdlet 會針對此參數指定的群組建立連結的服務。</span><span class="sxs-lookup"><span data-stu-id="b491f-133">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b491f-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b491f-134">-ResourceId</span></span>
<span data-ttu-id="b491f-135">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b491f-135">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b491f-136">-確認</span><span class="sxs-lookup"><span data-stu-id="b491f-136">-Confirm</span></span>
<span data-ttu-id="b491f-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b491f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b491f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b491f-138">-WhatIf</span></span>
<span data-ttu-id="b491f-139">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b491f-139">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="b491f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b491f-140">CommonParameters</span></span>
<span data-ttu-id="b491f-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b491f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b491f-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b491f-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b491f-143">輸入</span><span class="sxs-lookup"><span data-stu-id="b491f-143">INPUTS</span></span>

### <span data-ttu-id="b491f-144">System.object</span><span class="sxs-lookup"><span data-stu-id="b491f-144">System.String</span></span>

## <span data-ttu-id="b491f-145">輸出</span><span class="sxs-lookup"><span data-stu-id="b491f-145">OUTPUTS</span></span>

### <span data-ttu-id="b491f-146">PSLinkedService 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="b491f-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="b491f-147">筆記</span><span class="sxs-lookup"><span data-stu-id="b491f-147">NOTES</span></span>
<span data-ttu-id="b491f-148">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="b491f-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b491f-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="b491f-149">RELATED LINKS</span></span>

[<span data-ttu-id="b491f-150">AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="b491f-150">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="b491f-151">移除-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="b491f-151">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()
