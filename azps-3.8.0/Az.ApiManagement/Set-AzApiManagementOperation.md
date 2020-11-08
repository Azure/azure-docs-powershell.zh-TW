---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOperation.md
ms.openlocfilehash: 92848cb2daa0976d8206549fc16d1a6f039199a6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965624"
---
# <span data-ttu-id="7013f-101">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="7013f-101">Set-AzApiManagementOperation</span></span>

## <span data-ttu-id="7013f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7013f-102">SYNOPSIS</span></span>
<span data-ttu-id="7013f-103">設定 API 操作詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7013f-103">Sets API operation details.</span></span>

## <span data-ttu-id="7013f-104">句法</span><span class="sxs-lookup"><span data-stu-id="7013f-104">SYNTAX</span></span>

```
Set-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7013f-105">說明</span><span class="sxs-lookup"><span data-stu-id="7013f-105">DESCRIPTION</span></span>
<span data-ttu-id="7013f-106">**AzApiManagementOperation** Cmdlet 會設定 API 操作詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7013f-106">The **Set-AzApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="7013f-107">示例</span><span class="sxs-lookup"><span data-stu-id="7013f-107">EXAMPLES</span></span>

### <span data-ttu-id="7013f-108">範例1：設定工序詳細資料</span><span class="sxs-lookup"><span data-stu-id="7013f-108">Example 1: Set the operation details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="7013f-109">這個命令會設定 API 管理的作業詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7013f-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="7013f-110">參數</span><span class="sxs-lookup"><span data-stu-id="7013f-110">PARAMETERS</span></span>

### <span data-ttu-id="7013f-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="7013f-111">-ApiId</span></span>
<span data-ttu-id="7013f-112">指定 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7013f-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="7013f-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="7013f-113">-ApiRevision</span></span>
<span data-ttu-id="7013f-114">API 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7013f-114">Identifier of API Revision.</span></span> <span data-ttu-id="7013f-115">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="7013f-115">This parameter is optional.</span></span> <span data-ttu-id="7013f-116">如果未指定，該作業將會在目前使用中的 api 修正程式中更新。</span><span class="sxs-lookup"><span data-stu-id="7013f-116">If not specified, the operation will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="7013f-117">-內容</span><span class="sxs-lookup"><span data-stu-id="7013f-117">-Context</span></span>
<span data-ttu-id="7013f-118">指定 **PsApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="7013f-118">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7013f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7013f-119">-DefaultProfile</span></span>
<span data-ttu-id="7013f-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7013f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7013f-121">-描述</span><span class="sxs-lookup"><span data-stu-id="7013f-121">-Description</span></span>
<span data-ttu-id="7013f-122">指定新操作的描述。</span><span class="sxs-lookup"><span data-stu-id="7013f-122">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="7013f-123">-方法</span><span class="sxs-lookup"><span data-stu-id="7013f-123">-Method</span></span>
<span data-ttu-id="7013f-124">指定新操作的 HTTP 方法。</span><span class="sxs-lookup"><span data-stu-id="7013f-124">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="7013f-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="7013f-125">-Name</span></span>
<span data-ttu-id="7013f-126">指定新作業的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="7013f-126">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="7013f-127">-OperationId</span><span class="sxs-lookup"><span data-stu-id="7013f-127">-OperationId</span></span>
<span data-ttu-id="7013f-128">指定現有作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7013f-128">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="7013f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7013f-129">-PassThru</span></span>
<span data-ttu-id="7013f-130">passthru</span><span class="sxs-lookup"><span data-stu-id="7013f-130">passthru</span></span>

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

### <span data-ttu-id="7013f-131">-要求</span><span class="sxs-lookup"><span data-stu-id="7013f-131">-Request</span></span>
<span data-ttu-id="7013f-132">指定操作要求詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7013f-132">Specifies the operation request details.</span></span>

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

### <span data-ttu-id="7013f-133">-回復</span><span class="sxs-lookup"><span data-stu-id="7013f-133">-Responses</span></span>
<span data-ttu-id="7013f-134">指定可能的運算回應陣列。</span><span class="sxs-lookup"><span data-stu-id="7013f-134">Specifies an array of possible operation responses.</span></span>

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

### <span data-ttu-id="7013f-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="7013f-135">-TemplateParameters</span></span>
<span data-ttu-id="7013f-136">指定 [參數 *UrlTemplate* ] 中定義的陣列或參數。</span><span class="sxs-lookup"><span data-stu-id="7013f-136">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="7013f-137">如果您沒有指定值，系統會根據 UrlTemplate 產生預設值。</span><span class="sxs-lookup"><span data-stu-id="7013f-137">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="7013f-138">使用參數來提供更多有關參數（例如描述、類型及其他可能值）的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7013f-138">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

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

### <span data-ttu-id="7013f-139">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="7013f-139">-UrlTemplate</span></span>
<span data-ttu-id="7013f-140">指定 URL 範本。</span><span class="sxs-lookup"><span data-stu-id="7013f-140">Specifies the URL template.</span></span>
<span data-ttu-id="7013f-141">例如：客戶/{cid}/orders/{oid}/？ date = {date}。</span><span class="sxs-lookup"><span data-stu-id="7013f-141">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="7013f-142">-確認</span><span class="sxs-lookup"><span data-stu-id="7013f-142">-Confirm</span></span>
<span data-ttu-id="7013f-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7013f-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7013f-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7013f-144">-WhatIf</span></span>
<span data-ttu-id="7013f-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7013f-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7013f-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7013f-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7013f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7013f-147">CommonParameters</span></span>
<span data-ttu-id="7013f-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7013f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7013f-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7013f-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7013f-150">輸入</span><span class="sxs-lookup"><span data-stu-id="7013f-150">INPUTS</span></span>

### <span data-ttu-id="7013f-151">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="7013f-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7013f-152">System.object</span><span class="sxs-lookup"><span data-stu-id="7013f-152">System.String</span></span>

### <span data-ttu-id="7013f-153">PsApiManagementParameter []. ApiManagement [ServiceManagement]</span><span class="sxs-lookup"><span data-stu-id="7013f-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="7013f-154">ServiceManagement. PsApiManagementRequest （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="7013f-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="7013f-155">PsApiManagementResponse []. ApiManagement [ServiceManagement]</span><span class="sxs-lookup"><span data-stu-id="7013f-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

### <span data-ttu-id="7013f-156">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="7013f-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7013f-157">輸出</span><span class="sxs-lookup"><span data-stu-id="7013f-157">OUTPUTS</span></span>

### <span data-ttu-id="7013f-158">ServiceManagement. PsApiManagementOperation （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="7013f-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="7013f-159">筆記</span><span class="sxs-lookup"><span data-stu-id="7013f-159">NOTES</span></span>

## <span data-ttu-id="7013f-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="7013f-160">RELATED LINKS</span></span>

[<span data-ttu-id="7013f-161">AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="7013f-161">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="7013f-162">新-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="7013f-162">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="7013f-163">移除-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="7013f-163">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

