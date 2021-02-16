---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
ms.openlocfilehash: 4ed63d0e3b801572698b123038a2022e89672a88
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141699"
---
# <span data-ttu-id="3bf7d-101">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3bf7d-101">New-AzApiManagementBackend</span></span>

## <span data-ttu-id="3bf7d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3bf7d-102">SYNOPSIS</span></span>
<span data-ttu-id="3bf7d-103">建立新的後端實體。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-103">Creates a new backend entity.</span></span>

## <span data-ttu-id="3bf7d-104">句法</span><span class="sxs-lookup"><span data-stu-id="3bf7d-104">SYNTAX</span></span>

```
New-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bf7d-105">說明</span><span class="sxs-lookup"><span data-stu-id="3bf7d-105">DESCRIPTION</span></span>
<span data-ttu-id="3bf7d-106">在 Api 管理中建立新的後端實體。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="3bf7d-107">示例</span><span class="sxs-lookup"><span data-stu-id="3bf7d-107">EXAMPLES</span></span>

### <span data-ttu-id="3bf7d-108">範例1：使用基本授權配置建立後123</span><span class="sxs-lookup"><span data-stu-id="3bf7d-108">Example 1: Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="3bf7d-109">建立新的後端</span><span class="sxs-lookup"><span data-stu-id="3bf7d-109">Creates a new Backend</span></span>

## <span data-ttu-id="3bf7d-110">參數</span><span class="sxs-lookup"><span data-stu-id="3bf7d-110">PARAMETERS</span></span>

### <span data-ttu-id="3bf7d-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="3bf7d-111">-BackendId</span></span>
<span data-ttu-id="3bf7d-112">新後端的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-112">Identifier of new backend.</span></span>
<span data-ttu-id="3bf7d-113">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-113">This parameter is optional.</span></span>
<span data-ttu-id="3bf7d-114">如果未指定，將會產生。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="3bf7d-115">-內容</span><span class="sxs-lookup"><span data-stu-id="3bf7d-115">-Context</span></span>
<span data-ttu-id="3bf7d-116">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3bf7d-117">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-117">This parameter is required.</span></span>

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

### <span data-ttu-id="3bf7d-118">-認證</span><span class="sxs-lookup"><span data-stu-id="3bf7d-118">-Credential</span></span>
<span data-ttu-id="3bf7d-119">在與後端交談時應使用的認證詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="3bf7d-120">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="3bf7d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bf7d-121">-DefaultProfile</span></span>
<span data-ttu-id="3bf7d-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3bf7d-123">-描述</span><span class="sxs-lookup"><span data-stu-id="3bf7d-123">-Description</span></span>
<span data-ttu-id="3bf7d-124">後端描述。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-124">Backend Description.</span></span>
<span data-ttu-id="3bf7d-125">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="3bf7d-126">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="3bf7d-126">-Protocol</span></span>
<span data-ttu-id="3bf7d-127">後端通訊通訊協定。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-127">Backend Communication protocol.</span></span>
<span data-ttu-id="3bf7d-128">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-128">This parameter is required.</span></span>
<span data-ttu-id="3bf7d-129">有效值為 "HTTP" 和 "soap"。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="3bf7d-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="3bf7d-130">-Proxy</span></span>
<span data-ttu-id="3bf7d-131">傳送要求給後所要使用的 Proxy 伺服器詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="3bf7d-132">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="3bf7d-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3bf7d-133">-ResourceId</span></span>
<span data-ttu-id="3bf7d-134">外部系統中資源的管理 Uri。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="3bf7d-135">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-135">This parameter is optional.</span></span>
<span data-ttu-id="3bf7d-136">此 url 可以是邏輯 App、函數 App 或 Api App 的 Arm 資源 Id。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="3bf7d-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="3bf7d-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="3bf7d-138">Service Fabric 群集後端詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="3bf7d-139">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="3bf7d-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="3bf7d-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="3bf7d-141">在與後端交談時，是否略過憑證連結驗證。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="3bf7d-142">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="3bf7d-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="3bf7d-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="3bf7d-144">在與後端交談時，是否略過憑證名稱驗證。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="3bf7d-145">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="3bf7d-146">-標題</span><span class="sxs-lookup"><span data-stu-id="3bf7d-146">-Title</span></span>
<span data-ttu-id="3bf7d-147">後端標題。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-147">Backend Title.</span></span>
<span data-ttu-id="3bf7d-148">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="3bf7d-149">-Url</span><span class="sxs-lookup"><span data-stu-id="3bf7d-149">-Url</span></span>
<span data-ttu-id="3bf7d-150">後端的執行時間 Url。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="3bf7d-151">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-151">This parameter is required.</span></span>

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

### <span data-ttu-id="3bf7d-152">-確認</span><span class="sxs-lookup"><span data-stu-id="3bf7d-152">-Confirm</span></span>
<span data-ttu-id="3bf7d-153">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bf7d-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bf7d-154">-WhatIf</span></span>
<span data-ttu-id="3bf7d-155">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3bf7d-156">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bf7d-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bf7d-157">CommonParameters</span></span>
<span data-ttu-id="3bf7d-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bf7d-159">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3bf7d-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bf7d-160">輸入</span><span class="sxs-lookup"><span data-stu-id="3bf7d-160">INPUTS</span></span>

### <span data-ttu-id="3bf7d-161">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="3bf7d-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3bf7d-162">System.object</span><span class="sxs-lookup"><span data-stu-id="3bf7d-162">System.String</span></span>

### <span data-ttu-id="3bf7d-163">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3bf7d-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3bf7d-164">ServiceManagement. PsApiManagementBackendCredential （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="3bf7d-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="3bf7d-165">ServiceManagement. PsApiManagementBackendProxy （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="3bf7d-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="3bf7d-166">ServiceManagement. PsApiManagementServiceFabric （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="3bf7d-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="3bf7d-167">輸出</span><span class="sxs-lookup"><span data-stu-id="3bf7d-167">OUTPUTS</span></span>

### <span data-ttu-id="3bf7d-168">ServiceManagement. PsApiManagementBackend （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="3bf7d-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="3bf7d-169">筆記</span><span class="sxs-lookup"><span data-stu-id="3bf7d-169">NOTES</span></span>

## <span data-ttu-id="3bf7d-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="3bf7d-170">RELATED LINKS</span></span>

[<span data-ttu-id="3bf7d-171">AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3bf7d-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="3bf7d-172">新-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="3bf7d-172">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="3bf7d-173">新-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="3bf7d-173">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="3bf7d-174">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3bf7d-174">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="3bf7d-175">移除-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3bf7d-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)

