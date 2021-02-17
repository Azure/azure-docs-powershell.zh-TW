---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
ms.openlocfilehash: 1f78630f195fca7e08ed755dbaeb48e413c8f8d1
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400996"
---
# <span data-ttu-id="b4cd2-101">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b4cd2-101">New-AzApiManagementBackend</span></span>

## <span data-ttu-id="b4cd2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b4cd2-102">SYNOPSIS</span></span>
<span data-ttu-id="b4cd2-103">建立新的後端實體。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-103">Creates a new backend entity.</span></span>

## <span data-ttu-id="b4cd2-104">語法</span><span class="sxs-lookup"><span data-stu-id="b4cd2-104">SYNTAX</span></span>

```
New-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4cd2-105">描述</span><span class="sxs-lookup"><span data-stu-id="b4cd2-105">DESCRIPTION</span></span>
<span data-ttu-id="b4cd2-106">在 Api 管理中建立新的後端實體。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="b4cd2-107">例子</span><span class="sxs-lookup"><span data-stu-id="b4cd2-107">EXAMPLES</span></span>

### <span data-ttu-id="b4cd2-108">使用基本授權方案建立後端 123</span><span class="sxs-lookup"><span data-stu-id="b4cd2-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="b4cd2-109">建立新後端</span><span class="sxs-lookup"><span data-stu-id="b4cd2-109">Creates a new Backend</span></span>

## <span data-ttu-id="b4cd2-110">參數</span><span class="sxs-lookup"><span data-stu-id="b4cd2-110">PARAMETERS</span></span>

### <span data-ttu-id="b4cd2-111">-後端Id</span><span class="sxs-lookup"><span data-stu-id="b4cd2-111">-BackendId</span></span>
<span data-ttu-id="b4cd2-112">新後端的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-112">Identifier of new backend.</span></span>
<span data-ttu-id="b4cd2-113">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-113">This parameter is optional.</span></span>
<span data-ttu-id="b4cd2-114">如果未指定，將會產生。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="b4cd2-115">-內容</span><span class="sxs-lookup"><span data-stu-id="b4cd2-115">-Context</span></span>
<span data-ttu-id="b4cd2-116">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b4cd2-117">此參數為必填專案。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-117">This parameter is required.</span></span>

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

### <span data-ttu-id="b4cd2-118">-認證</span><span class="sxs-lookup"><span data-stu-id="b4cd2-118">-Credential</span></span>
<span data-ttu-id="b4cd2-119">與後端交談時應該使用的認證詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="b4cd2-120">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="b4cd2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4cd2-121">-DefaultProfile</span></span>
<span data-ttu-id="b4cd2-122">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4cd2-123">-描述</span><span class="sxs-lookup"><span data-stu-id="b4cd2-123">-Description</span></span>
<span data-ttu-id="b4cd2-124">後端描述。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-124">Backend Description.</span></span>
<span data-ttu-id="b4cd2-125">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="b4cd2-126">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="b4cd2-126">-Protocol</span></span>
<span data-ttu-id="b4cd2-127">後端通訊通訊通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-127">Backend Communication protocol.</span></span>
<span data-ttu-id="b4cd2-128">此參數為必填專案。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-128">This parameter is required.</span></span>
<span data-ttu-id="b4cd2-129">有效的值為 'HTTP' 和 'soap'。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="b4cd2-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="b4cd2-130">-Proxy</span></span>
<span data-ttu-id="b4cd2-131">傳送要求至後端時所使用的 Proxy 伺服器詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="b4cd2-132">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="b4cd2-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4cd2-133">-ResourceId</span></span>
<span data-ttu-id="b4cd2-134">外部系統中資源的管理 Uri。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="b4cd2-135">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-135">This parameter is optional.</span></span>
<span data-ttu-id="b4cd2-136">此 URL 可以是邏輯應用程式、函數 App 或 Api Apps 的 Arm 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="b4cd2-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="b4cd2-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="b4cd2-138">服務結構組群後端詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="b4cd2-139">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-139">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4cd2-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="b4cd2-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="b4cd2-141">與後端交談時是否要略過憑證鏈驗證。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="b4cd2-142">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="b4cd2-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="b4cd2-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="b4cd2-144">是否要在與後端交談時略過憑證名稱驗證。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="b4cd2-145">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="b4cd2-146">-標題</span><span class="sxs-lookup"><span data-stu-id="b4cd2-146">-Title</span></span>
<span data-ttu-id="b4cd2-147">後端標題。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-147">Backend Title.</span></span>
<span data-ttu-id="b4cd2-148">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="b4cd2-149">-Url</span><span class="sxs-lookup"><span data-stu-id="b4cd2-149">-Url</span></span>
<span data-ttu-id="b4cd2-150">後端的執行時間 URL。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="b4cd2-151">此參數為必填專案。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-151">This parameter is required.</span></span>

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

### <span data-ttu-id="b4cd2-152">-確認</span><span class="sxs-lookup"><span data-stu-id="b4cd2-152">-Confirm</span></span>
<span data-ttu-id="b4cd2-153">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4cd2-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4cd2-154">-WhatIf</span></span>
<span data-ttu-id="b4cd2-155">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4cd2-156">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4cd2-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4cd2-157">CommonParameters</span></span>
<span data-ttu-id="b4cd2-158">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4cd2-159">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b4cd2-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4cd2-160">輸入</span><span class="sxs-lookup"><span data-stu-id="b4cd2-160">INPUTS</span></span>

### <span data-ttu-id="b4cd2-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="b4cd2-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b4cd2-162">System.String</span><span class="sxs-lookup"><span data-stu-id="b4cd2-162">System.String</span></span>

### <span data-ttu-id="b4cd2-163">System.Nullable'1[[System.Boolean， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b4cd2-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b4cd2-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="b4cd2-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="b4cd2-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="b4cd2-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="b4cd2-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b4cd2-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="b4cd2-167">輸出</span><span class="sxs-lookup"><span data-stu-id="b4cd2-167">OUTPUTS</span></span>

### <span data-ttu-id="b4cd2-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b4cd2-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="b4cd2-169">筆記</span><span class="sxs-lookup"><span data-stu-id="b4cd2-169">NOTES</span></span>

## <span data-ttu-id="b4cd2-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="b4cd2-170">RELATED LINKS</span></span>

[<span data-ttu-id="b4cd2-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b4cd2-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="b4cd2-172">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="b4cd2-172">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="b4cd2-173">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="b4cd2-173">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="b4cd2-174">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b4cd2-174">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="b4cd2-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b4cd2-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)

