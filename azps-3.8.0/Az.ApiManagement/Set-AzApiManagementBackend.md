---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: 8631120178a256aa1ec5b817727f9362f6d8f076
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407279"
---
# <span data-ttu-id="517ff-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="517ff-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="517ff-102">簡介</span><span class="sxs-lookup"><span data-stu-id="517ff-102">SYNOPSIS</span></span>
<span data-ttu-id="517ff-103">更新後端。</span><span class="sxs-lookup"><span data-stu-id="517ff-103">Updates a Backend.</span></span>

## <span data-ttu-id="517ff-104">語法</span><span class="sxs-lookup"><span data-stu-id="517ff-104">SYNTAX</span></span>

### <span data-ttu-id="517ff-105">CoNtextParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="517ff-105">ContextParameterSet (Default)</span></span>
```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="517ff-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="517ff-106">ByInputObject</span></span>
```
Set-AzApiManagementBackend -InputObject <PsApiManagementBackend> [-Protocol <String>] [-Url <String>]
 [-ResourceId <String>] [-Title <String>] [-Description <String>] [-SkipCertificateChainValidation <Boolean>]
 [-SkipCertificateNameValidation <Boolean>] [-Credential <PsApiManagementBackendCredential>]
 [-Proxy <PsApiManagementBackendProxy>] [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="517ff-107">描述</span><span class="sxs-lookup"><span data-stu-id="517ff-107">DESCRIPTION</span></span>
<span data-ttu-id="517ff-108">更新 Api 管理中現有的後端。</span><span class="sxs-lookup"><span data-stu-id="517ff-108">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="517ff-109">例子</span><span class="sxs-lookup"><span data-stu-id="517ff-109">EXAMPLES</span></span>

### <span data-ttu-id="517ff-110">更新後端 123 的描述</span><span class="sxs-lookup"><span data-stu-id="517ff-110">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="517ff-111">參數</span><span class="sxs-lookup"><span data-stu-id="517ff-111">PARAMETERS</span></span>

### <span data-ttu-id="517ff-112">-後端Id</span><span class="sxs-lookup"><span data-stu-id="517ff-112">-BackendId</span></span>
<span data-ttu-id="517ff-113">新後端的識別碼。</span><span class="sxs-lookup"><span data-stu-id="517ff-113">Identifier of new backend.</span></span>
<span data-ttu-id="517ff-114">此參數為必填專案。</span><span class="sxs-lookup"><span data-stu-id="517ff-114">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="517ff-115">-內容</span><span class="sxs-lookup"><span data-stu-id="517ff-115">-Context</span></span>
<span data-ttu-id="517ff-116">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="517ff-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="517ff-117">此參數為必填專案。</span><span class="sxs-lookup"><span data-stu-id="517ff-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="517ff-118">-認證</span><span class="sxs-lookup"><span data-stu-id="517ff-118">-Credential</span></span>
<span data-ttu-id="517ff-119">與後端交談時應該使用的認證詳細資料。</span><span class="sxs-lookup"><span data-stu-id="517ff-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="517ff-120">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="517ff-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="517ff-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="517ff-121">-DefaultProfile</span></span>
<span data-ttu-id="517ff-122">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="517ff-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="517ff-123">-描述</span><span class="sxs-lookup"><span data-stu-id="517ff-123">-Description</span></span>
<span data-ttu-id="517ff-124">後端描述。</span><span class="sxs-lookup"><span data-stu-id="517ff-124">Backend Description.</span></span>
<span data-ttu-id="517ff-125">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="517ff-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="517ff-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="517ff-126">-InputObject</span></span>
<span data-ttu-id="517ff-127">PsApiManagementBackend 實例。</span><span class="sxs-lookup"><span data-stu-id="517ff-127">Instance of PsApiManagementBackend.</span></span> <span data-ttu-id="517ff-128">此參數為必填專案。</span><span class="sxs-lookup"><span data-stu-id="517ff-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="517ff-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="517ff-129">-PassThru</span></span>
<span data-ttu-id="517ff-130">表示此 Cmdlet 會返回 **此 Cmdlet 修改的 PsApiManagementBackend。**</span><span class="sxs-lookup"><span data-stu-id="517ff-130">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="517ff-131">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="517ff-131">-Protocol</span></span>
<span data-ttu-id="517ff-132">後端通訊通訊協定 (HTTP 或 soap) 。</span><span class="sxs-lookup"><span data-stu-id="517ff-132">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="517ff-133">此參數為選擇性</span><span class="sxs-lookup"><span data-stu-id="517ff-133">This parameter is optional</span></span>

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

### <span data-ttu-id="517ff-134">-Proxy</span><span class="sxs-lookup"><span data-stu-id="517ff-134">-Proxy</span></span>
<span data-ttu-id="517ff-135">傳送要求至後端時所使用的 Proxy 伺服器詳細資料。</span><span class="sxs-lookup"><span data-stu-id="517ff-135">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="517ff-136">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="517ff-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="517ff-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="517ff-137">-ResourceId</span></span>
<span data-ttu-id="517ff-138">外部系統中資源的管理 Uri。</span><span class="sxs-lookup"><span data-stu-id="517ff-138">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="517ff-139">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="517ff-139">This parameter is optional.</span></span>
<span data-ttu-id="517ff-140">此 URL 可以是邏輯應用程式、函數 App 或 Api Apps 的 Arm 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="517ff-140">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="517ff-141">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="517ff-141">-ServiceFabricCluster</span></span>
<span data-ttu-id="517ff-142">服務結構組群後端詳細資料。</span><span class="sxs-lookup"><span data-stu-id="517ff-142">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="517ff-143">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="517ff-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="517ff-144">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="517ff-144">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="517ff-145">與後端交談時是否要略過憑證鏈驗證。</span><span class="sxs-lookup"><span data-stu-id="517ff-145">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="517ff-146">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="517ff-146">This parameter is optional.</span></span>

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

### <span data-ttu-id="517ff-147">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="517ff-147">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="517ff-148">是否要在與後端交談時略過憑證名稱驗證。</span><span class="sxs-lookup"><span data-stu-id="517ff-148">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="517ff-149">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="517ff-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="517ff-150">-標題</span><span class="sxs-lookup"><span data-stu-id="517ff-150">-Title</span></span>
<span data-ttu-id="517ff-151">後端標題。</span><span class="sxs-lookup"><span data-stu-id="517ff-151">Backend Title.</span></span>
<span data-ttu-id="517ff-152">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="517ff-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="517ff-153">-Url</span><span class="sxs-lookup"><span data-stu-id="517ff-153">-Url</span></span>
<span data-ttu-id="517ff-154">後端的執行時間 URL。</span><span class="sxs-lookup"><span data-stu-id="517ff-154">Runtime Url for the Backend.</span></span>
<span data-ttu-id="517ff-155">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="517ff-155">This parameter is optional.</span></span>

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

### <span data-ttu-id="517ff-156">-確認</span><span class="sxs-lookup"><span data-stu-id="517ff-156">-Confirm</span></span>
<span data-ttu-id="517ff-157">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="517ff-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="517ff-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="517ff-158">-WhatIf</span></span>
<span data-ttu-id="517ff-159">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="517ff-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="517ff-160">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="517ff-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="517ff-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="517ff-161">CommonParameters</span></span>
<span data-ttu-id="517ff-162">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="517ff-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="517ff-163">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="517ff-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="517ff-164">輸入</span><span class="sxs-lookup"><span data-stu-id="517ff-164">INPUTS</span></span>

### <span data-ttu-id="517ff-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="517ff-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="517ff-166">System.String</span><span class="sxs-lookup"><span data-stu-id="517ff-166">System.String</span></span>

### <span data-ttu-id="517ff-167">System.Nullable'1[[System.Boolean， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="517ff-167">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="517ff-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="517ff-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="517ff-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="517ff-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="517ff-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="517ff-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="517ff-171">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="517ff-171">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="517ff-172">輸出</span><span class="sxs-lookup"><span data-stu-id="517ff-172">OUTPUTS</span></span>

### <span data-ttu-id="517ff-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="517ff-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="517ff-174">筆記</span><span class="sxs-lookup"><span data-stu-id="517ff-174">NOTES</span></span>

## <span data-ttu-id="517ff-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="517ff-175">RELATED LINKS</span></span>

[<span data-ttu-id="517ff-176">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="517ff-176">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="517ff-177">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="517ff-177">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="517ff-178">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="517ff-178">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="517ff-179">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="517ff-179">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="517ff-180">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="517ff-180">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
