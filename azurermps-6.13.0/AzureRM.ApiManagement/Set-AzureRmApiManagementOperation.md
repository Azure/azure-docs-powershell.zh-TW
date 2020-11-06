---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
ms.openlocfilehash: e50e912c55a09ef5d036bee668bc45f58fc42c19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445815"
---
# <span data-ttu-id="b8963-101">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="b8963-101">Set-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="b8963-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b8963-102">SYNOPSIS</span></span>
<span data-ttu-id="b8963-103">設定 API 操作詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b8963-103">Sets API operation details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8963-104">句法</span><span class="sxs-lookup"><span data-stu-id="b8963-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8963-105">說明</span><span class="sxs-lookup"><span data-stu-id="b8963-105">DESCRIPTION</span></span>
<span data-ttu-id="b8963-106">**AzureRmApiManagementOperation** Cmdlet 會設定 API 操作詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b8963-106">The **Set-AzureRmApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="b8963-107">示例</span><span class="sxs-lookup"><span data-stu-id="b8963-107">EXAMPLES</span></span>

### <span data-ttu-id="b8963-108">範例1：設定工序詳細資料</span><span class="sxs-lookup"><span data-stu-id="b8963-108">Example 1: Set the operation details</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="b8963-109">這個命令會設定 API 管理的作業詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b8963-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="b8963-110">參數</span><span class="sxs-lookup"><span data-stu-id="b8963-110">PARAMETERS</span></span>

### <span data-ttu-id="b8963-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="b8963-111">-ApiId</span></span>
<span data-ttu-id="b8963-112">指定 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b8963-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="b8963-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="b8963-113">-ApiRevision</span></span>
<span data-ttu-id="b8963-114">API 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b8963-114">Identifier of API Revision.</span></span> <span data-ttu-id="b8963-115">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="b8963-115">This parameter is optional.</span></span> <span data-ttu-id="b8963-116">如果未指定，該作業將會在目前使用中的 api 修正程式中更新。</span><span class="sxs-lookup"><span data-stu-id="b8963-116">If not specified, the operation will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="b8963-117">-內容</span><span class="sxs-lookup"><span data-stu-id="b8963-117">-Context</span></span>
<span data-ttu-id="b8963-118">指定 **PsApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="b8963-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="b8963-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8963-119">-DefaultProfile</span></span>
<span data-ttu-id="b8963-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b8963-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8963-121">-描述</span><span class="sxs-lookup"><span data-stu-id="b8963-121">-Description</span></span>
<span data-ttu-id="b8963-122">指定新操作的描述。</span><span class="sxs-lookup"><span data-stu-id="b8963-122">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="b8963-123">-方法</span><span class="sxs-lookup"><span data-stu-id="b8963-123">-Method</span></span>
<span data-ttu-id="b8963-124">指定新操作的 HTTP 方法。</span><span class="sxs-lookup"><span data-stu-id="b8963-124">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="b8963-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="b8963-125">-Name</span></span>
<span data-ttu-id="b8963-126">指定新作業的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="b8963-126">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="b8963-127">-OperationId</span><span class="sxs-lookup"><span data-stu-id="b8963-127">-OperationId</span></span>
<span data-ttu-id="b8963-128">指定現有作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b8963-128">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="b8963-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8963-129">-PassThru</span></span>
<span data-ttu-id="b8963-130">passthru</span><span class="sxs-lookup"><span data-stu-id="b8963-130">passthru</span></span>

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

### <span data-ttu-id="b8963-131">-要求</span><span class="sxs-lookup"><span data-stu-id="b8963-131">-Request</span></span>
<span data-ttu-id="b8963-132">指定操作要求詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b8963-132">Specifies the operation request details.</span></span>

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

### <span data-ttu-id="b8963-133">-回復</span><span class="sxs-lookup"><span data-stu-id="b8963-133">-Responses</span></span>
<span data-ttu-id="b8963-134">指定可能的運算回應陣列。</span><span class="sxs-lookup"><span data-stu-id="b8963-134">Specifies an array of possible operation responses.</span></span>

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

### <span data-ttu-id="b8963-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="b8963-135">-TemplateParameters</span></span>
<span data-ttu-id="b8963-136">指定 [參數 *UrlTemplate* ] 中定義的陣列或參數。</span><span class="sxs-lookup"><span data-stu-id="b8963-136">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="b8963-137">如果您沒有指定值，系統會根據 UrlTemplate 產生預設值。</span><span class="sxs-lookup"><span data-stu-id="b8963-137">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="b8963-138">使用參數來提供更多有關參數（例如描述、類型及其他可能值）的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b8963-138">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

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

### <span data-ttu-id="b8963-139">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="b8963-139">-UrlTemplate</span></span>
<span data-ttu-id="b8963-140">指定 URL 範本。</span><span class="sxs-lookup"><span data-stu-id="b8963-140">Specifies the URL template.</span></span>
<span data-ttu-id="b8963-141">例如：客戶/{cid}/orders/{oid}/？ date = {date}。</span><span class="sxs-lookup"><span data-stu-id="b8963-141">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="b8963-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8963-142">CommonParameters</span></span>
<span data-ttu-id="b8963-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b8963-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8963-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b8963-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8963-145">輸入</span><span class="sxs-lookup"><span data-stu-id="b8963-145">INPUTS</span></span>

### <span data-ttu-id="b8963-146">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="b8963-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b8963-147">System.object</span><span class="sxs-lookup"><span data-stu-id="b8963-147">System.String</span></span>

### <span data-ttu-id="b8963-148">PsApiManagementParameter []. ApiManagement [ServiceManagement]</span><span class="sxs-lookup"><span data-stu-id="b8963-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="b8963-149">ServiceManagement. PsApiManagementRequest （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="b8963-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="b8963-150">PsApiManagementResponse []. ApiManagement [ServiceManagement]</span><span class="sxs-lookup"><span data-stu-id="b8963-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

### <span data-ttu-id="b8963-151">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="b8963-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b8963-152">輸出</span><span class="sxs-lookup"><span data-stu-id="b8963-152">OUTPUTS</span></span>

### <span data-ttu-id="b8963-153">ServiceManagement. PsApiManagementOperation （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="b8963-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="b8963-154">筆記</span><span class="sxs-lookup"><span data-stu-id="b8963-154">NOTES</span></span>

## <span data-ttu-id="b8963-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8963-155">RELATED LINKS</span></span>

[<span data-ttu-id="b8963-156">AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="b8963-156">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="b8963-157">新-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="b8963-157">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="b8963-158">移除-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="b8963-158">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)


