---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
ms.openlocfilehash: 4800d7d56d03071b57d25cdacfcf271defa9276f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449420"
---
# <span data-ttu-id="27a72-101">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="27a72-101">Set-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="27a72-102">摘要</span><span class="sxs-lookup"><span data-stu-id="27a72-102">SYNOPSIS</span></span>
<span data-ttu-id="27a72-103">設定 API 操作詳細資料。</span><span class="sxs-lookup"><span data-stu-id="27a72-103">Sets API operation details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27a72-104">句法</span><span class="sxs-lookup"><span data-stu-id="27a72-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="27a72-105">說明</span><span class="sxs-lookup"><span data-stu-id="27a72-105">DESCRIPTION</span></span>
<span data-ttu-id="27a72-106">**AzureRmApiManagementOperation** Cmdlet 會設定 API 操作詳細資料。</span><span class="sxs-lookup"><span data-stu-id="27a72-106">The **Set-AzureRmApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="27a72-107">示例</span><span class="sxs-lookup"><span data-stu-id="27a72-107">EXAMPLES</span></span>

### <span data-ttu-id="27a72-108">範例1：設定工序詳細資料</span><span class="sxs-lookup"><span data-stu-id="27a72-108">Example 1: Set the operation details</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="27a72-109">這個命令會設定 API 管理的作業詳細資料。</span><span class="sxs-lookup"><span data-stu-id="27a72-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="27a72-110">參數</span><span class="sxs-lookup"><span data-stu-id="27a72-110">PARAMETERS</span></span>

### <span data-ttu-id="27a72-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="27a72-111">-ApiId</span></span>
<span data-ttu-id="27a72-112">指定 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="27a72-112">Specifies the identifier of the API.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27a72-113">-內容</span><span class="sxs-lookup"><span data-stu-id="27a72-113">-Context</span></span>
<span data-ttu-id="27a72-114">指定 **PsApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="27a72-114">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27a72-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27a72-115">-DefaultProfile</span></span>
<span data-ttu-id="27a72-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="27a72-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="27a72-117">-描述</span><span class="sxs-lookup"><span data-stu-id="27a72-117">-Description</span></span>
<span data-ttu-id="27a72-118">指定新操作的描述。</span><span class="sxs-lookup"><span data-stu-id="27a72-118">Specifies the description of the new operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27a72-119">-方法</span><span class="sxs-lookup"><span data-stu-id="27a72-119">-Method</span></span>
<span data-ttu-id="27a72-120">指定新操作的 HTTP 方法。</span><span class="sxs-lookup"><span data-stu-id="27a72-120">Specifies the HTTP method of the new operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27a72-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="27a72-121">-Name</span></span>
<span data-ttu-id="27a72-122">指定新作業的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="27a72-122">Specifies the display name of the new operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27a72-123">-OperationId</span><span class="sxs-lookup"><span data-stu-id="27a72-123">-OperationId</span></span>
<span data-ttu-id="27a72-124">指定現有作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="27a72-124">Specifies the identifier of the existing operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27a72-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27a72-125">-PassThru</span></span>
<span data-ttu-id="27a72-126">passthru</span><span class="sxs-lookup"><span data-stu-id="27a72-126">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27a72-127">-要求</span><span class="sxs-lookup"><span data-stu-id="27a72-127">-Request</span></span>
<span data-ttu-id="27a72-128">指定操作要求詳細資料。</span><span class="sxs-lookup"><span data-stu-id="27a72-128">Specifies the operation request details.</span></span>

```yaml
Type: PsApiManagementRequest
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27a72-129">-回復</span><span class="sxs-lookup"><span data-stu-id="27a72-129">-Responses</span></span>
<span data-ttu-id="27a72-130">指定可能的運算回應陣列。</span><span class="sxs-lookup"><span data-stu-id="27a72-130">Specifies an array of possible operation responses.</span></span>

```yaml
Type: PsApiManagementResponse[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27a72-131">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="27a72-131">-TemplateParameters</span></span>
<span data-ttu-id="27a72-132">指定 [參數 *UrlTemplate* ] 中定義的陣列或參數。</span><span class="sxs-lookup"><span data-stu-id="27a72-132">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="27a72-133">如果您沒有指定值，系統會根據 UrlTemplate 產生預設值。</span><span class="sxs-lookup"><span data-stu-id="27a72-133">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="27a72-134">使用參數來提供更多有關參數（例如描述、類型及其他可能值）的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="27a72-134">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

```yaml
Type: PsApiManagementParameter[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27a72-135">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="27a72-135">-UrlTemplate</span></span>
<span data-ttu-id="27a72-136">指定 URL 範本。</span><span class="sxs-lookup"><span data-stu-id="27a72-136">Specifies the URL template.</span></span>
<span data-ttu-id="27a72-137">例如：客戶/{cid}/orders/{oid}/？ date = {date}。</span><span class="sxs-lookup"><span data-stu-id="27a72-137">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27a72-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27a72-138">CommonParameters</span></span>
<span data-ttu-id="27a72-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="27a72-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27a72-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="27a72-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27a72-141">輸入</span><span class="sxs-lookup"><span data-stu-id="27a72-141">INPUTS</span></span>

### <span data-ttu-id="27a72-142">所有</span><span class="sxs-lookup"><span data-stu-id="27a72-142">None</span></span>
<span data-ttu-id="27a72-143">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="27a72-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="27a72-144">輸出</span><span class="sxs-lookup"><span data-stu-id="27a72-144">OUTPUTS</span></span>

### <span data-ttu-id="27a72-145">ServiceManagement. PsApiManagementOperation （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="27a72-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="27a72-146">筆記</span><span class="sxs-lookup"><span data-stu-id="27a72-146">NOTES</span></span>

## <span data-ttu-id="27a72-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="27a72-147">RELATED LINKS</span></span>

[<span data-ttu-id="27a72-148">AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="27a72-148">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="27a72-149">新-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="27a72-149">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="27a72-150">移除-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="27a72-150">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)


