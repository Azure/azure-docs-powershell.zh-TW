---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
ms.openlocfilehash: 28bbc9158639faf066fa9a623f5dfacd6566d236
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625722"
---
# <span data-ttu-id="500c7-101">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="500c7-101">Set-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="500c7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="500c7-102">SYNOPSIS</span></span>
<span data-ttu-id="500c7-103">設定 API 操作詳細資料。</span><span class="sxs-lookup"><span data-stu-id="500c7-103">Sets API operation details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="500c7-104">句法</span><span class="sxs-lookup"><span data-stu-id="500c7-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="500c7-105">說明</span><span class="sxs-lookup"><span data-stu-id="500c7-105">DESCRIPTION</span></span>
<span data-ttu-id="500c7-106">**AzureRmApiManagementOperation** Cmdlet 會設定 API 操作詳細資料。</span><span class="sxs-lookup"><span data-stu-id="500c7-106">The **Set-AzureRmApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="500c7-107">示例</span><span class="sxs-lookup"><span data-stu-id="500c7-107">EXAMPLES</span></span>

### <span data-ttu-id="500c7-108">範例1：設定工序詳細資料</span><span class="sxs-lookup"><span data-stu-id="500c7-108">Example 1: Set the operation details</span></span>
```
PS C:\>New-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="500c7-109">這個命令會設定 API 管理的作業詳細資料。</span><span class="sxs-lookup"><span data-stu-id="500c7-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="500c7-110">參數</span><span class="sxs-lookup"><span data-stu-id="500c7-110">PARAMETERS</span></span>

### <span data-ttu-id="500c7-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="500c7-111">-ApiId</span></span>
<span data-ttu-id="500c7-112">指定 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="500c7-112">Specifies the identifier of the API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="500c7-113">-內容</span><span class="sxs-lookup"><span data-stu-id="500c7-113">-Context</span></span>
<span data-ttu-id="500c7-114">指定 **PsApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="500c7-114">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="500c7-115">-描述</span><span class="sxs-lookup"><span data-stu-id="500c7-115">-Description</span></span>
<span data-ttu-id="500c7-116">指定新操作的描述。</span><span class="sxs-lookup"><span data-stu-id="500c7-116">Specifies the description of the new operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="500c7-117">-方法</span><span class="sxs-lookup"><span data-stu-id="500c7-117">-Method</span></span>
<span data-ttu-id="500c7-118">指定新操作的 HTTP 方法。</span><span class="sxs-lookup"><span data-stu-id="500c7-118">Specifies the HTTP method of the new operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="500c7-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="500c7-119">-Name</span></span>
<span data-ttu-id="500c7-120">指定新作業的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="500c7-120">Specifies the display name of the new operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="500c7-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="500c7-121">-OperationId</span></span>
<span data-ttu-id="500c7-122">指定現有作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="500c7-122">Specifies the identifier of the existing operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="500c7-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="500c7-123">-PassThru</span></span>
<span data-ttu-id="500c7-124">passthru</span><span class="sxs-lookup"><span data-stu-id="500c7-124">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="500c7-125">-要求</span><span class="sxs-lookup"><span data-stu-id="500c7-125">-Request</span></span>
<span data-ttu-id="500c7-126">指定操作要求詳細資料。</span><span class="sxs-lookup"><span data-stu-id="500c7-126">Specifies the operation request details.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="500c7-127">-回復</span><span class="sxs-lookup"><span data-stu-id="500c7-127">-Responses</span></span>
<span data-ttu-id="500c7-128">指定可能的運算回應陣列。</span><span class="sxs-lookup"><span data-stu-id="500c7-128">Specifies an array of possible operation responses.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="500c7-129">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="500c7-129">-TemplateParameters</span></span>
<span data-ttu-id="500c7-130">指定 [參數 *UrlTemplate* ] 中定義的陣列或參數。</span><span class="sxs-lookup"><span data-stu-id="500c7-130">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="500c7-131">如果您沒有指定值，系統會根據 UrlTemplate 產生預設值。</span><span class="sxs-lookup"><span data-stu-id="500c7-131">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="500c7-132">使用參數來提供更多有關參數（例如描述、類型及其他可能值）的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="500c7-132">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="500c7-133">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="500c7-133">-UrlTemplate</span></span>
<span data-ttu-id="500c7-134">指定 URL 範本。</span><span class="sxs-lookup"><span data-stu-id="500c7-134">Specifies the URL template.</span></span>
<span data-ttu-id="500c7-135">例如：客戶/{cid}/orders/{oid}/？ date = {date}。</span><span class="sxs-lookup"><span data-stu-id="500c7-135">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="500c7-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="500c7-136">-DefaultProfile</span></span>
<span data-ttu-id="500c7-137">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="500c7-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="500c7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="500c7-138">CommonParameters</span></span>
<span data-ttu-id="500c7-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="500c7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="500c7-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="500c7-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="500c7-141">輸入</span><span class="sxs-lookup"><span data-stu-id="500c7-141">INPUTS</span></span>

## <span data-ttu-id="500c7-142">輸出</span><span class="sxs-lookup"><span data-stu-id="500c7-142">OUTPUTS</span></span>

### <span data-ttu-id="500c7-143">ServiceManagement. PsApiManagementOperation （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="500c7-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="500c7-144">筆記</span><span class="sxs-lookup"><span data-stu-id="500c7-144">NOTES</span></span>

## <span data-ttu-id="500c7-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="500c7-145">RELATED LINKS</span></span>

[<span data-ttu-id="500c7-146">AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="500c7-146">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="500c7-147">新-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="500c7-147">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="500c7-148">移除-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="500c7-148">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)


