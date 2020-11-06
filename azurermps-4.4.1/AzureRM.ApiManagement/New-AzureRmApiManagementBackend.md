---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
ms.openlocfilehash: 144830c2155379683c8568eda6e0d1bc021b38fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450119"
---
# <span data-ttu-id="66001-101">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="66001-101">New-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="66001-102">摘要</span><span class="sxs-lookup"><span data-stu-id="66001-102">SYNOPSIS</span></span>
<span data-ttu-id="66001-103">建立新的後端實體。</span><span class="sxs-lookup"><span data-stu-id="66001-103">Creates a new backend entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66001-104">句法</span><span class="sxs-lookup"><span data-stu-id="66001-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66001-105">說明</span><span class="sxs-lookup"><span data-stu-id="66001-105">DESCRIPTION</span></span>
<span data-ttu-id="66001-106">在 Api 管理中建立新的後端實體。</span><span class="sxs-lookup"><span data-stu-id="66001-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="66001-107">示例</span><span class="sxs-lookup"><span data-stu-id="66001-107">EXAMPLES</span></span>

### <span data-ttu-id="66001-108">使用基本授權配置建立後123</span><span class="sxs-lookup"><span data-stu-id="66001-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```
$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="66001-109">建立新的後端</span><span class="sxs-lookup"><span data-stu-id="66001-109">Creates a new Backend</span></span>

## <span data-ttu-id="66001-110">參數</span><span class="sxs-lookup"><span data-stu-id="66001-110">PARAMETERS</span></span>

### <span data-ttu-id="66001-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="66001-111">-BackendId</span></span>
<span data-ttu-id="66001-112">新後端的識別碼。</span><span class="sxs-lookup"><span data-stu-id="66001-112">Identifier of new backend.</span></span>
<span data-ttu-id="66001-113">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="66001-113">This parameter is optional.</span></span>
<span data-ttu-id="66001-114">如果未指定，將會產生。</span><span class="sxs-lookup"><span data-stu-id="66001-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="66001-115">-內容</span><span class="sxs-lookup"><span data-stu-id="66001-115">-Context</span></span>
<span data-ttu-id="66001-116">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="66001-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="66001-117">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="66001-117">This parameter is required.</span></span>

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

### <span data-ttu-id="66001-118">-認證</span><span class="sxs-lookup"><span data-stu-id="66001-118">-Credential</span></span>
<span data-ttu-id="66001-119">在與後端交談時應使用的認證詳細資料。</span><span class="sxs-lookup"><span data-stu-id="66001-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="66001-120">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="66001-120">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66001-121">-描述</span><span class="sxs-lookup"><span data-stu-id="66001-121">-Description</span></span>
<span data-ttu-id="66001-122">後端描述。</span><span class="sxs-lookup"><span data-stu-id="66001-122">Backend Description.</span></span>
<span data-ttu-id="66001-123">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="66001-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="66001-124">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="66001-124">-Protocol</span></span>
<span data-ttu-id="66001-125">後端通訊通訊協定。</span><span class="sxs-lookup"><span data-stu-id="66001-125">Backend Communication protocol.</span></span>
<span data-ttu-id="66001-126">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="66001-126">This parameter is required.</span></span>
<span data-ttu-id="66001-127">有效值為 "HTTP" 和 "soap"。</span><span class="sxs-lookup"><span data-stu-id="66001-127">Valid values are 'http' and 'soap'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66001-128">-Proxy</span><span class="sxs-lookup"><span data-stu-id="66001-128">-Proxy</span></span>
<span data-ttu-id="66001-129">傳送要求給後所要使用的 Proxy 伺服器詳細資料。</span><span class="sxs-lookup"><span data-stu-id="66001-129">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="66001-130">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="66001-130">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66001-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66001-131">-ResourceId</span></span>
<span data-ttu-id="66001-132">外部系統中資源的管理 Uri。</span><span class="sxs-lookup"><span data-stu-id="66001-132">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="66001-133">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="66001-133">This parameter is optional.</span></span>
<span data-ttu-id="66001-134">此 url 可以是邏輯 App、函數 App 或 Api App 的 Arm 資源 Id。</span><span class="sxs-lookup"><span data-stu-id="66001-134">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="66001-135">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="66001-135">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="66001-136">在與後端交談時，是否略過憑證連結驗證。</span><span class="sxs-lookup"><span data-stu-id="66001-136">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="66001-137">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="66001-137">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66001-138">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="66001-138">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="66001-139">在與後端交談時，是否略過憑證名稱驗證。</span><span class="sxs-lookup"><span data-stu-id="66001-139">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="66001-140">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="66001-140">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66001-141">-標題</span><span class="sxs-lookup"><span data-stu-id="66001-141">-Title</span></span>
<span data-ttu-id="66001-142">後端標題。</span><span class="sxs-lookup"><span data-stu-id="66001-142">Backend Title.</span></span>
<span data-ttu-id="66001-143">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="66001-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="66001-144">-Url</span><span class="sxs-lookup"><span data-stu-id="66001-144">-Url</span></span>
<span data-ttu-id="66001-145">後端的執行時間 Url。</span><span class="sxs-lookup"><span data-stu-id="66001-145">Runtime Url for the Backend.</span></span>
<span data-ttu-id="66001-146">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="66001-146">This parameter is required.</span></span>

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

### <span data-ttu-id="66001-147">-確認</span><span class="sxs-lookup"><span data-stu-id="66001-147">-Confirm</span></span>
<span data-ttu-id="66001-148">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="66001-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66001-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66001-149">-WhatIf</span></span>
<span data-ttu-id="66001-150">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="66001-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="66001-151">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="66001-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66001-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66001-152">-DefaultProfile</span></span>
<span data-ttu-id="66001-153">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="66001-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66001-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66001-154">CommonParameters</span></span>
<span data-ttu-id="66001-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="66001-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66001-156">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="66001-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66001-157">輸入</span><span class="sxs-lookup"><span data-stu-id="66001-157">INPUTS</span></span>

## <span data-ttu-id="66001-158">輸出</span><span class="sxs-lookup"><span data-stu-id="66001-158">OUTPUTS</span></span>

### <span data-ttu-id="66001-159">ServiceManagement. PsApiManagementBackend （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="66001-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="66001-160">筆記</span><span class="sxs-lookup"><span data-stu-id="66001-160">NOTES</span></span>

## <span data-ttu-id="66001-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="66001-161">RELATED LINKS</span></span>

[<span data-ttu-id="66001-162">AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="66001-162">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="66001-163">新-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="66001-163">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="66001-164">新-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="66001-164">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="66001-165">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="66001-165">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="66001-166">移除-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="66001-166">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)

