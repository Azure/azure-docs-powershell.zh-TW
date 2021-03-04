---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 8CD2BE3E-2FA1-4EAB-BC01-B1E1E3203FF1
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
ms.openlocfilehash: 5b11273e61689c515cc7ed72f013514fcd309dcf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906734"
---
# <span data-ttu-id="14742-101">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="14742-101">New-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="14742-102">簡介</span><span class="sxs-lookup"><span data-stu-id="14742-102">SYNOPSIS</span></span>
<span data-ttu-id="14742-103">將資料存放區或雲端服務連結至 Azure Data Factory。</span><span class="sxs-lookup"><span data-stu-id="14742-103">Links a data store or a cloud service to an Azure Data Factory.</span></span>

## <span data-ttu-id="14742-104">語法</span><span class="sxs-lookup"><span data-stu-id="14742-104">SYNTAX</span></span>

### <span data-ttu-id="14742-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="14742-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14742-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="14742-106">ByFactoryObject</span></span>
```
New-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14742-107">描述</span><span class="sxs-lookup"><span data-stu-id="14742-107">DESCRIPTION</span></span>
<span data-ttu-id="14742-108">**New-AzDataFactoryLinkedService** Cmdlet 將資料存放區或雲端服務連結至 Azure Data Factory。</span><span class="sxs-lookup"><span data-stu-id="14742-108">The **New-AzDataFactoryLinkedService** cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="14742-109">如果您為已存在的連結服務指定名稱，此 Cmdlet 會先提示您確認，然後再取代連結的服務。</span><span class="sxs-lookup"><span data-stu-id="14742-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="14742-110">如果您指定 *Force* 參數，Cmdlet 會取代現有的連結服務，而不需要確認。</span><span class="sxs-lookup"><span data-stu-id="14742-110">If you specify the *Force* parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="14742-111">請以下列循序執行這些作業：</span><span class="sxs-lookup"><span data-stu-id="14742-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="14742-112">建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="14742-112">Create a data factory.</span></span> 
- <span data-ttu-id="14742-113">建立連結服務。</span><span class="sxs-lookup"><span data-stu-id="14742-113">Create linked services.</span></span> 
- <span data-ttu-id="14742-114">建立資料集。</span><span class="sxs-lookup"><span data-stu-id="14742-114">Create datasets.</span></span> 
- <span data-ttu-id="14742-115">建立管線。</span><span class="sxs-lookup"><span data-stu-id="14742-115">Create a pipeline.</span></span>

## <span data-ttu-id="14742-116">例子</span><span class="sxs-lookup"><span data-stu-id="14742-116">EXAMPLES</span></span>

### <span data-ttu-id="14742-117">範例 1：建立連結服務</span><span class="sxs-lookup"><span data-stu-id="14742-117">Example 1: Create a linked service</span></span>
```
PS C:\>New-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List
LinkedServiceName : LinkedServiceCuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.AzureStorageLinkedService
```

<span data-ttu-id="14742-118">此命令在名為 WikiADF 的資料工廠中，建立一個名為 LinkedServiceCuratedWikiData 的連結服務。</span><span class="sxs-lookup"><span data-stu-id="14742-118">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="14742-119">此連結服務會連結檔案中指定的 Azure Blob 存放區至名為 WikiADF 的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="14742-119">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="14742-120">該命令會使用管線運算子Format-List Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="14742-120">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="14742-121">Windows PowerShell Cmdlet 會格式化結果。</span><span class="sxs-lookup"><span data-stu-id="14742-121">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="14742-122">如需要詳細資訊，請鍵入 `Get-Help Format-List` 。</span><span class="sxs-lookup"><span data-stu-id="14742-122">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="14742-123">參數</span><span class="sxs-lookup"><span data-stu-id="14742-123">PARAMETERS</span></span>

### <span data-ttu-id="14742-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="14742-124">-DataFactory</span></span>
<span data-ttu-id="14742-125">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="14742-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="14742-126">此 Cmdlet 會為此參數指定的資料工廠建立連結服務。</span><span class="sxs-lookup"><span data-stu-id="14742-126">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="14742-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="14742-127">-DataFactoryName</span></span>
<span data-ttu-id="14742-128">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="14742-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="14742-129">此 Cmdlet 會為此參數指定的資料工廠建立連結服務。</span><span class="sxs-lookup"><span data-stu-id="14742-129">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="14742-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14742-130">-DefaultProfile</span></span>
<span data-ttu-id="14742-131">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="14742-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14742-132">-檔案</span><span class="sxs-lookup"><span data-stu-id="14742-132">-File</span></span>
<span data-ttu-id="14742-133">指定包含連結服務描述之 JSON (JSON) 的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="14742-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the linked service.</span></span>

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

### <span data-ttu-id="14742-134">-強制</span><span class="sxs-lookup"><span data-stu-id="14742-134">-Force</span></span>
<span data-ttu-id="14742-135">表示此 Cmdlet 會取代現有的連結服務，而不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="14742-135">Indicates that this cmdlet replaces an existing linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="14742-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="14742-136">-Name</span></span>
<span data-ttu-id="14742-137">指定要建立的連結服務名稱。</span><span class="sxs-lookup"><span data-stu-id="14742-137">Specifies the name of the linked service to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14742-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14742-138">-ResourceGroupName</span></span>
<span data-ttu-id="14742-139">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="14742-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="14742-140">此 Cmdlet 會為此參數指定的群組建立連結服務。</span><span class="sxs-lookup"><span data-stu-id="14742-140">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="14742-141">-確認</span><span class="sxs-lookup"><span data-stu-id="14742-141">-Confirm</span></span>
<span data-ttu-id="14742-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="14742-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14742-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14742-143">-WhatIf</span></span>
<span data-ttu-id="14742-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="14742-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14742-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="14742-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14742-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14742-146">CommonParameters</span></span>
<span data-ttu-id="14742-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="14742-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14742-148">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="14742-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14742-149">輸入</span><span class="sxs-lookup"><span data-stu-id="14742-149">INPUTS</span></span>

### <span data-ttu-id="14742-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="14742-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="14742-151">System.String</span><span class="sxs-lookup"><span data-stu-id="14742-151">System.String</span></span>

## <span data-ttu-id="14742-152">輸出</span><span class="sxs-lookup"><span data-stu-id="14742-152">OUTPUTS</span></span>

### <span data-ttu-id="14742-153">Microsoft.Azure.Commands.DataFactories.models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="14742-153">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span></span>

## <span data-ttu-id="14742-154">筆記</span><span class="sxs-lookup"><span data-stu-id="14742-154">NOTES</span></span>
* <span data-ttu-id="14742-155">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="14742-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="14742-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="14742-156">RELATED LINKS</span></span>

[<span data-ttu-id="14742-157">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="14742-157">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="14742-158">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="14742-158">Remove-AzDataFactoryLinkedService</span></span>](./Remove-AzDataFactoryLinkedService.md)


