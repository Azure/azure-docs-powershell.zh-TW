---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 8CD2BE3E-2FA1-4EAB-BC01-B1E1E3203FF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
ms.openlocfilehash: 09b766ec77b9f915a03bf6f5b20bd53941b66fc9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128260"
---
# <span data-ttu-id="13395-101">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="13395-101">New-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="13395-102">摘要</span><span class="sxs-lookup"><span data-stu-id="13395-102">SYNOPSIS</span></span>
<span data-ttu-id="13395-103">將資料存放區或雲端服務連結至 Azure 資料工廠。</span><span class="sxs-lookup"><span data-stu-id="13395-103">Links a data store or a cloud service to an Azure Data Factory.</span></span>

## <span data-ttu-id="13395-104">句法</span><span class="sxs-lookup"><span data-stu-id="13395-104">SYNTAX</span></span>

### <span data-ttu-id="13395-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="13395-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13395-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="13395-106">ByFactoryObject</span></span>
```
New-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13395-107">說明</span><span class="sxs-lookup"><span data-stu-id="13395-107">DESCRIPTION</span></span>
<span data-ttu-id="13395-108">**新的-AzDataFactoryLinkedService** Cmdlet 會將資料存放區或雲端服務連結至 Azure 資料工廠。</span><span class="sxs-lookup"><span data-stu-id="13395-108">The **New-AzDataFactoryLinkedService** cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="13395-109">如果您指定已存在之連結服務的名稱，此 Cmdlet 會在您替換連結的服務之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="13395-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="13395-110">如果您指定 *Force* 參數，則 Cmdlet 會取代現有的連結服務而不進行確認。</span><span class="sxs-lookup"><span data-stu-id="13395-110">If you specify the *Force* parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="13395-111">依下列循序執行這些作業：</span><span class="sxs-lookup"><span data-stu-id="13395-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="13395-112">建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="13395-112">Create a data factory.</span></span> 
- <span data-ttu-id="13395-113">建立連結的服務。</span><span class="sxs-lookup"><span data-stu-id="13395-113">Create linked services.</span></span> 
- <span data-ttu-id="13395-114">建立資料集。</span><span class="sxs-lookup"><span data-stu-id="13395-114">Create datasets.</span></span> 
- <span data-ttu-id="13395-115">建立管線。</span><span class="sxs-lookup"><span data-stu-id="13395-115">Create a pipeline.</span></span>

## <span data-ttu-id="13395-116">示例</span><span class="sxs-lookup"><span data-stu-id="13395-116">EXAMPLES</span></span>

### <span data-ttu-id="13395-117">範例1：建立連結的服務</span><span class="sxs-lookup"><span data-stu-id="13395-117">Example 1: Create a linked service</span></span>
```
PS C:\>New-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List
LinkedServiceName : LinkedServiceCuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.AzureStorageLinkedService
```

<span data-ttu-id="13395-118">這個命令會在名為 WikiADF 的資料工廠中建立名為 LinkedServiceCuratedWikiData 的連結服務。</span><span class="sxs-lookup"><span data-stu-id="13395-118">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="13395-119">這個連結的服務會將檔案中指定的 Azure blob 存放區連結到名為 WikiADF 的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="13395-119">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="13395-120">命令會使用管線運算子，將結果傳遞到 Format-List Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="13395-120">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="13395-121">該 Windows PowerShell Cmdlet 會格式化結果。</span><span class="sxs-lookup"><span data-stu-id="13395-121">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="13395-122">如需詳細資訊，請輸入 `Get-Help Format-List` 。</span><span class="sxs-lookup"><span data-stu-id="13395-122">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="13395-123">參數</span><span class="sxs-lookup"><span data-stu-id="13395-123">PARAMETERS</span></span>

### <span data-ttu-id="13395-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="13395-124">-DataFactory</span></span>
<span data-ttu-id="13395-125">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="13395-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="13395-126">這個 Cmdlet 會針對此參數指定的資料工廠建立連結的服務。</span><span class="sxs-lookup"><span data-stu-id="13395-126">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="13395-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="13395-127">-DataFactoryName</span></span>
<span data-ttu-id="13395-128">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="13395-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="13395-129">這個 Cmdlet 會針對此參數指定的資料工廠建立連結的服務。</span><span class="sxs-lookup"><span data-stu-id="13395-129">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="13395-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13395-130">-DefaultProfile</span></span>
<span data-ttu-id="13395-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="13395-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13395-132">檔案</span><span class="sxs-lookup"><span data-stu-id="13395-132">-File</span></span>
<span data-ttu-id="13395-133">指定包含連結服務描述的 JavaScript 物件符號 (JSON) 檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="13395-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the linked service.</span></span>

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

### <span data-ttu-id="13395-134">-Force</span><span class="sxs-lookup"><span data-stu-id="13395-134">-Force</span></span>
<span data-ttu-id="13395-135">表示此 Cmdlet 會取代現有的連結服務，而不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="13395-135">Indicates that this cmdlet replaces an existing linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="13395-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="13395-136">-Name</span></span>
<span data-ttu-id="13395-137">指定要建立之連結服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="13395-137">Specifies the name of the linked service to create.</span></span>

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

### <span data-ttu-id="13395-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13395-138">-ResourceGroupName</span></span>
<span data-ttu-id="13395-139">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="13395-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="13395-140">這個 Cmdlet 會針對此參數指定的群組建立連結的服務。</span><span class="sxs-lookup"><span data-stu-id="13395-140">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="13395-141">-確認</span><span class="sxs-lookup"><span data-stu-id="13395-141">-Confirm</span></span>
<span data-ttu-id="13395-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="13395-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13395-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13395-143">-WhatIf</span></span>
<span data-ttu-id="13395-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="13395-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13395-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="13395-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13395-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13395-146">CommonParameters</span></span>
<span data-ttu-id="13395-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="13395-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13395-148">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="13395-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13395-149">輸入</span><span class="sxs-lookup"><span data-stu-id="13395-149">INPUTS</span></span>

### <span data-ttu-id="13395-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="13395-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="13395-151">System.object</span><span class="sxs-lookup"><span data-stu-id="13395-151">System.String</span></span>

## <span data-ttu-id="13395-152">輸出</span><span class="sxs-lookup"><span data-stu-id="13395-152">OUTPUTS</span></span>

### <span data-ttu-id="13395-153">PSLinkedService 中的 DataFactories。</span><span class="sxs-lookup"><span data-stu-id="13395-153">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span></span>

## <span data-ttu-id="13395-154">筆記</span><span class="sxs-lookup"><span data-stu-id="13395-154">NOTES</span></span>
* <span data-ttu-id="13395-155">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="13395-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="13395-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="13395-156">RELATED LINKS</span></span>

[<span data-ttu-id="13395-157">AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="13395-157">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="13395-158">移除-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="13395-158">Remove-AzDataFactoryLinkedService</span></span>](./Remove-AzDataFactoryLinkedService.md)

