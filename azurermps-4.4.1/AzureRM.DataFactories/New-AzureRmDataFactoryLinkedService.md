---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 8CD2BE3E-2FA1-4EAB-BC01-B1E1E3203FF1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: 9ae1dfe79361e926325b82199469eaf9a9f5d92b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449620"
---
# <span data-ttu-id="1502a-101">New-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="1502a-101">New-AzureRmDataFactoryLinkedService</span></span>

## <span data-ttu-id="1502a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1502a-102">SYNOPSIS</span></span>
<span data-ttu-id="1502a-103">將資料存放區或雲端服務連結至 Azure 資料工廠。</span><span class="sxs-lookup"><span data-stu-id="1502a-103">Links a data store or a cloud service to an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1502a-104">句法</span><span class="sxs-lookup"><span data-stu-id="1502a-104">SYNTAX</span></span>

### <span data-ttu-id="1502a-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="1502a-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1502a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1502a-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1502a-107">說明</span><span class="sxs-lookup"><span data-stu-id="1502a-107">DESCRIPTION</span></span>
<span data-ttu-id="1502a-108">**新的-AzureRmDataFactoryLinkedService** Cmdlet 會將資料存放區或雲端服務連結至 Azure 資料工廠。</span><span class="sxs-lookup"><span data-stu-id="1502a-108">The **New-AzureRmDataFactoryLinkedService** cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="1502a-109">如果您指定已存在之連結服務的名稱，此 Cmdlet 會在您替換連結的服務之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1502a-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="1502a-110">如果您指定 *Force* 參數，則 Cmdlet 會取代現有的連結服務而不進行確認。</span><span class="sxs-lookup"><span data-stu-id="1502a-110">If you specify the *Force* parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>

<span data-ttu-id="1502a-111">依下列循序執行這些作業：</span><span class="sxs-lookup"><span data-stu-id="1502a-111">Perform these operations in the following order:</span></span> 

- <span data-ttu-id="1502a-112">建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="1502a-112">Create a data factory.</span></span> 
- <span data-ttu-id="1502a-113">建立連結的服務。</span><span class="sxs-lookup"><span data-stu-id="1502a-113">Create linked services.</span></span> 
- <span data-ttu-id="1502a-114">建立資料集。</span><span class="sxs-lookup"><span data-stu-id="1502a-114">Create datasets.</span></span> 
- <span data-ttu-id="1502a-115">建立管線。</span><span class="sxs-lookup"><span data-stu-id="1502a-115">Create a pipeline.</span></span>

## <span data-ttu-id="1502a-116">示例</span><span class="sxs-lookup"><span data-stu-id="1502a-116">EXAMPLES</span></span>

### <span data-ttu-id="1502a-117">範例1：建立連結的服務</span><span class="sxs-lookup"><span data-stu-id="1502a-117">Example 1: Create a linked service</span></span>
```
PS C:\>New-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List
LinkedServiceName : LinkedServiceCuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.AzureStorageLinkedService
```

<span data-ttu-id="1502a-118">這個命令會在名為 WikiADF 的資料工廠中建立名為 LinkedServiceCuratedWikiData 的連結服務。</span><span class="sxs-lookup"><span data-stu-id="1502a-118">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="1502a-119">這個連結的服務會將檔案中指定的 Azure blob 存放區連結到名為 WikiADF 的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="1502a-119">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="1502a-120">命令會使用管線運算子，將結果傳遞到 Format-List Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1502a-120">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1502a-121">該 Windows PowerShell Cmdlet 會格式化結果。</span><span class="sxs-lookup"><span data-stu-id="1502a-121">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="1502a-122">如需詳細資訊，請輸入 `Get-Help Format-List` 。</span><span class="sxs-lookup"><span data-stu-id="1502a-122">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="1502a-123">參數</span><span class="sxs-lookup"><span data-stu-id="1502a-123">PARAMETERS</span></span>

### <span data-ttu-id="1502a-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1502a-124">-DataFactory</span></span>
<span data-ttu-id="1502a-125">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="1502a-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="1502a-126">這個 Cmdlet 會針對此參數指定的資料工廠建立連結的服務。</span><span class="sxs-lookup"><span data-stu-id="1502a-126">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1502a-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1502a-127">-DataFactoryName</span></span>
<span data-ttu-id="1502a-128">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="1502a-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1502a-129">這個 Cmdlet 會針對此參數指定的資料工廠建立連結的服務。</span><span class="sxs-lookup"><span data-stu-id="1502a-129">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1502a-130">檔案</span><span class="sxs-lookup"><span data-stu-id="1502a-130">-File</span></span>
<span data-ttu-id="1502a-131">指定包含連結服務描述的 JavaScript 物件符號 (JSON) 檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="1502a-131">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the linked service.</span></span>

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

### <span data-ttu-id="1502a-132">-Force</span><span class="sxs-lookup"><span data-stu-id="1502a-132">-Force</span></span>
<span data-ttu-id="1502a-133">表示此 Cmdlet 會取代現有的連結服務，而不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1502a-133">Indicates that this cmdlet replaces an existing linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="1502a-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="1502a-134">-Name</span></span>
<span data-ttu-id="1502a-135">指定要建立之連結服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="1502a-135">Specifies the name of the linked service to create.</span></span>

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

### <span data-ttu-id="1502a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1502a-136">-ResourceGroupName</span></span>
<span data-ttu-id="1502a-137">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1502a-137">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1502a-138">這個 Cmdlet 會針對此參數指定的群組建立連結的服務。</span><span class="sxs-lookup"><span data-stu-id="1502a-138">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1502a-139">-確認</span><span class="sxs-lookup"><span data-stu-id="1502a-139">-Confirm</span></span>
<span data-ttu-id="1502a-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1502a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1502a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1502a-141">-WhatIf</span></span>
<span data-ttu-id="1502a-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1502a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1502a-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1502a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1502a-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1502a-144">-DefaultProfile</span></span>
<span data-ttu-id="1502a-145">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1502a-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1502a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1502a-146">CommonParameters</span></span>
<span data-ttu-id="1502a-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1502a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1502a-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1502a-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1502a-149">輸入</span><span class="sxs-lookup"><span data-stu-id="1502a-149">INPUTS</span></span>

## <span data-ttu-id="1502a-150">輸出</span><span class="sxs-lookup"><span data-stu-id="1502a-150">OUTPUTS</span></span>

### <span data-ttu-id="1502a-151">PSLinkedService 中的 WindowsAzure</span><span class="sxs-lookup"><span data-stu-id="1502a-151">Microsoft.WindowsAzure.Commands.Utilities.PSLinkedService</span></span>

## <span data-ttu-id="1502a-152">筆記</span><span class="sxs-lookup"><span data-stu-id="1502a-152">NOTES</span></span>
* <span data-ttu-id="1502a-153">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="1502a-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1502a-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="1502a-154">RELATED LINKS</span></span>

[<span data-ttu-id="1502a-155">AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="1502a-155">Get-AzureRmDataFactoryLinkedService</span></span>](./Get-AzureRmDataFactoryLinkedService.md)

[<span data-ttu-id="1502a-156">移除-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="1502a-156">Remove-AzureRmDataFactoryLinkedService</span></span>](./Remove-AzureRmDataFactoryLinkedService.md)


