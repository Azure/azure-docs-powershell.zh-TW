---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: 0ac89ed099029fbbabe90e07da7ba9c204449db9
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400734"
---
# <span data-ttu-id="46a77-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="46a77-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="46a77-102">簡介</span><span class="sxs-lookup"><span data-stu-id="46a77-102">SYNOPSIS</span></span>
<span data-ttu-id="46a77-103">更新後端。</span><span class="sxs-lookup"><span data-stu-id="46a77-103">Updates a Backend.</span></span>

## <span data-ttu-id="46a77-104">語法</span><span class="sxs-lookup"><span data-stu-id="46a77-104">SYNTAX</span></span>

```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46a77-105">描述</span><span class="sxs-lookup"><span data-stu-id="46a77-105">DESCRIPTION</span></span>
<span data-ttu-id="46a77-106">更新 Api 管理中現有的後端。</span><span class="sxs-lookup"><span data-stu-id="46a77-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="46a77-107">例子</span><span class="sxs-lookup"><span data-stu-id="46a77-107">EXAMPLES</span></span>

### <span data-ttu-id="46a77-108">更新後端 123 的描述</span><span class="sxs-lookup"><span data-stu-id="46a77-108">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="46a77-109">參數</span><span class="sxs-lookup"><span data-stu-id="46a77-109">PARAMETERS</span></span>

### <span data-ttu-id="46a77-110">-後端Id</span><span class="sxs-lookup"><span data-stu-id="46a77-110">-BackendId</span></span>
<span data-ttu-id="46a77-111">新後端的識別碼。</span><span class="sxs-lookup"><span data-stu-id="46a77-111">Identifier of new backend.</span></span>
<span data-ttu-id="46a77-112">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="46a77-112">This parameter is required.</span></span>

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

### <span data-ttu-id="46a77-113">-內容</span><span class="sxs-lookup"><span data-stu-id="46a77-113">-Context</span></span>
<span data-ttu-id="46a77-114">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="46a77-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="46a77-115">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="46a77-115">This parameter is required.</span></span>

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

### <span data-ttu-id="46a77-116">-認證</span><span class="sxs-lookup"><span data-stu-id="46a77-116">-Credential</span></span>
<span data-ttu-id="46a77-117">與後端交談時應該使用的認證詳細資料。</span><span class="sxs-lookup"><span data-stu-id="46a77-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="46a77-118">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="46a77-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="46a77-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46a77-119">-DefaultProfile</span></span>
<span data-ttu-id="46a77-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="46a77-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46a77-121">-描述</span><span class="sxs-lookup"><span data-stu-id="46a77-121">-Description</span></span>
<span data-ttu-id="46a77-122">後端描述。</span><span class="sxs-lookup"><span data-stu-id="46a77-122">Backend Description.</span></span>
<span data-ttu-id="46a77-123">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="46a77-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="46a77-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46a77-124">-PassThru</span></span>
<span data-ttu-id="46a77-125">表示此 Cmdlet 會返回 **此 Cmdlet 修改的 PsApiManagementBackend。**</span><span class="sxs-lookup"><span data-stu-id="46a77-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="46a77-126">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="46a77-126">-Protocol</span></span>
<span data-ttu-id="46a77-127">後端通訊通訊通訊 (HTTP 或 soap) 。</span><span class="sxs-lookup"><span data-stu-id="46a77-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="46a77-128">此參數為選擇性</span><span class="sxs-lookup"><span data-stu-id="46a77-128">This parameter is optional</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: http, soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46a77-129">-Proxy</span><span class="sxs-lookup"><span data-stu-id="46a77-129">-Proxy</span></span>
<span data-ttu-id="46a77-130">傳送要求至後端時所使用的 Proxy 伺服器詳細資料。</span><span class="sxs-lookup"><span data-stu-id="46a77-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="46a77-131">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="46a77-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="46a77-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46a77-132">-ResourceId</span></span>
<span data-ttu-id="46a77-133">外部系統中資源的管理 Uri。</span><span class="sxs-lookup"><span data-stu-id="46a77-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="46a77-134">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="46a77-134">This parameter is optional.</span></span>
<span data-ttu-id="46a77-135">此 URL 可以是邏輯應用程式、函數 App 或 Api Apps 的 Arm 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="46a77-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="46a77-136">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="46a77-136">-ServiceFabricCluster</span></span>
<span data-ttu-id="46a77-137">服務結構組群後端詳細資料。</span><span class="sxs-lookup"><span data-stu-id="46a77-137">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="46a77-138">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="46a77-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="46a77-139">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="46a77-139">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="46a77-140">與後端交談時是否要略過憑證鏈驗證。</span><span class="sxs-lookup"><span data-stu-id="46a77-140">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="46a77-141">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="46a77-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="46a77-142">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="46a77-142">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="46a77-143">是否要在與後端交談時略過憑證名稱驗證。</span><span class="sxs-lookup"><span data-stu-id="46a77-143">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="46a77-144">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="46a77-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="46a77-145">-標題</span><span class="sxs-lookup"><span data-stu-id="46a77-145">-Title</span></span>
<span data-ttu-id="46a77-146">後端標題。</span><span class="sxs-lookup"><span data-stu-id="46a77-146">Backend Title.</span></span>
<span data-ttu-id="46a77-147">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="46a77-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="46a77-148">-Url</span><span class="sxs-lookup"><span data-stu-id="46a77-148">-Url</span></span>
<span data-ttu-id="46a77-149">後端的執行時間 URL。</span><span class="sxs-lookup"><span data-stu-id="46a77-149">Runtime Url for the Backend.</span></span>
<span data-ttu-id="46a77-150">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="46a77-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="46a77-151">-確認</span><span class="sxs-lookup"><span data-stu-id="46a77-151">-Confirm</span></span>
<span data-ttu-id="46a77-152">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="46a77-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46a77-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46a77-153">-WhatIf</span></span>
<span data-ttu-id="46a77-154">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="46a77-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46a77-155">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46a77-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46a77-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46a77-156">CommonParameters</span></span>
<span data-ttu-id="46a77-157">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="46a77-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46a77-158">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="46a77-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46a77-159">輸入</span><span class="sxs-lookup"><span data-stu-id="46a77-159">INPUTS</span></span>

### <span data-ttu-id="46a77-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="46a77-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="46a77-161">System.String</span><span class="sxs-lookup"><span data-stu-id="46a77-161">System.String</span></span>

### <span data-ttu-id="46a77-162">System.Nullable'1[[System.Boolean， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="46a77-162">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="46a77-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="46a77-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="46a77-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="46a77-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="46a77-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46a77-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="46a77-166">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="46a77-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="46a77-167">輸出</span><span class="sxs-lookup"><span data-stu-id="46a77-167">OUTPUTS</span></span>

### <span data-ttu-id="46a77-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="46a77-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="46a77-169">筆記</span><span class="sxs-lookup"><span data-stu-id="46a77-169">NOTES</span></span>

## <span data-ttu-id="46a77-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="46a77-170">RELATED LINKS</span></span>

[<span data-ttu-id="46a77-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="46a77-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="46a77-172">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="46a77-172">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="46a77-173">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="46a77-173">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="46a77-174">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="46a77-174">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="46a77-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="46a77-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
