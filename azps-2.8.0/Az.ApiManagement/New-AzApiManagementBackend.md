---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
ms.openlocfilehash: 5caef678df0aef88f4655c031d53e995920d0379
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614006"
---
# <span data-ttu-id="0a0dc-101">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0a0dc-101">New-AzApiManagementBackend</span></span>

## <span data-ttu-id="0a0dc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0a0dc-102">SYNOPSIS</span></span>
<span data-ttu-id="0a0dc-103">建立新的後端實體。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-103">Creates a new backend entity.</span></span>

## <span data-ttu-id="0a0dc-104">句法</span><span class="sxs-lookup"><span data-stu-id="0a0dc-104">SYNTAX</span></span>

```
New-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a0dc-105">說明</span><span class="sxs-lookup"><span data-stu-id="0a0dc-105">DESCRIPTION</span></span>
<span data-ttu-id="0a0dc-106">在 Api 管理中建立新的後端實體。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="0a0dc-107">示例</span><span class="sxs-lookup"><span data-stu-id="0a0dc-107">EXAMPLES</span></span>

### <span data-ttu-id="0a0dc-108">使用基本授權配置建立後123</span><span class="sxs-lookup"><span data-stu-id="0a0dc-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="0a0dc-109">建立新的後端</span><span class="sxs-lookup"><span data-stu-id="0a0dc-109">Creates a new Backend</span></span>

## <span data-ttu-id="0a0dc-110">參數</span><span class="sxs-lookup"><span data-stu-id="0a0dc-110">PARAMETERS</span></span>

### <span data-ttu-id="0a0dc-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="0a0dc-111">-BackendId</span></span>
<span data-ttu-id="0a0dc-112">新後端的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-112">Identifier of new backend.</span></span>
<span data-ttu-id="0a0dc-113">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-113">This parameter is optional.</span></span>
<span data-ttu-id="0a0dc-114">如果未指定，將會產生。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="0a0dc-115">-內容</span><span class="sxs-lookup"><span data-stu-id="0a0dc-115">-Context</span></span>
<span data-ttu-id="0a0dc-116">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0a0dc-117">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-117">This parameter is required.</span></span>

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

### <span data-ttu-id="0a0dc-118">-認證</span><span class="sxs-lookup"><span data-stu-id="0a0dc-118">-Credential</span></span>
<span data-ttu-id="0a0dc-119">在與後端交談時應使用的認證詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="0a0dc-120">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="0a0dc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a0dc-121">-DefaultProfile</span></span>
<span data-ttu-id="0a0dc-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a0dc-123">-描述</span><span class="sxs-lookup"><span data-stu-id="0a0dc-123">-Description</span></span>
<span data-ttu-id="0a0dc-124">後端描述。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-124">Backend Description.</span></span>
<span data-ttu-id="0a0dc-125">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="0a0dc-126">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="0a0dc-126">-Protocol</span></span>
<span data-ttu-id="0a0dc-127">後端通訊通訊協定。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-127">Backend Communication protocol.</span></span>
<span data-ttu-id="0a0dc-128">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-128">This parameter is required.</span></span>
<span data-ttu-id="0a0dc-129">有效值為 "HTTP" 和 "soap"。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="0a0dc-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="0a0dc-130">-Proxy</span></span>
<span data-ttu-id="0a0dc-131">傳送要求給後所要使用的 Proxy 伺服器詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="0a0dc-132">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="0a0dc-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a0dc-133">-ResourceId</span></span>
<span data-ttu-id="0a0dc-134">外部系統中資源的管理 Uri。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="0a0dc-135">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-135">This parameter is optional.</span></span>
<span data-ttu-id="0a0dc-136">此 url 可以是邏輯 App、函數 App 或 Api App 的 Arm 資源 Id。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="0a0dc-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="0a0dc-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="0a0dc-138">Service Fabric 群集後端詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="0a0dc-139">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="0a0dc-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="0a0dc-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="0a0dc-141">在與後端交談時，是否略過憑證連結驗證。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="0a0dc-142">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="0a0dc-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="0a0dc-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="0a0dc-144">在與後端交談時，是否略過憑證名稱驗證。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="0a0dc-145">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="0a0dc-146">-標題</span><span class="sxs-lookup"><span data-stu-id="0a0dc-146">-Title</span></span>
<span data-ttu-id="0a0dc-147">後端標題。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-147">Backend Title.</span></span>
<span data-ttu-id="0a0dc-148">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="0a0dc-149">-Url</span><span class="sxs-lookup"><span data-stu-id="0a0dc-149">-Url</span></span>
<span data-ttu-id="0a0dc-150">後端的執行時間 Url。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="0a0dc-151">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-151">This parameter is required.</span></span>

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

### <span data-ttu-id="0a0dc-152">-確認</span><span class="sxs-lookup"><span data-stu-id="0a0dc-152">-Confirm</span></span>
<span data-ttu-id="0a0dc-153">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a0dc-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a0dc-154">-WhatIf</span></span>
<span data-ttu-id="0a0dc-155">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a0dc-156">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a0dc-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a0dc-157">CommonParameters</span></span>
<span data-ttu-id="0a0dc-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a0dc-159">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0a0dc-159">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a0dc-160">輸入</span><span class="sxs-lookup"><span data-stu-id="0a0dc-160">INPUTS</span></span>

### <span data-ttu-id="0a0dc-161">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="0a0dc-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0a0dc-162">System.object</span><span class="sxs-lookup"><span data-stu-id="0a0dc-162">System.String</span></span>

### <span data-ttu-id="0a0dc-163">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0a0dc-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0a0dc-164">ServiceManagement. PsApiManagementBackendCredential （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="0a0dc-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="0a0dc-165">ServiceManagement. PsApiManagementBackendProxy （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="0a0dc-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="0a0dc-166">ServiceManagement. PsApiManagementServiceFabric （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="0a0dc-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="0a0dc-167">輸出</span><span class="sxs-lookup"><span data-stu-id="0a0dc-167">OUTPUTS</span></span>

### <span data-ttu-id="0a0dc-168">ServiceManagement. PsApiManagementBackend （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="0a0dc-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="0a0dc-169">筆記</span><span class="sxs-lookup"><span data-stu-id="0a0dc-169">NOTES</span></span>

## <span data-ttu-id="0a0dc-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a0dc-170">RELATED LINKS</span></span>

[<span data-ttu-id="0a0dc-171">AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0a0dc-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="0a0dc-172">新-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="0a0dc-172">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="0a0dc-173">新-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="0a0dc-173">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="0a0dc-174">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0a0dc-174">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="0a0dc-175">移除-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0a0dc-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)

