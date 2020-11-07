---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: ce27a151ebb6d778ed647fb81909c44c11edbf8e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788774"
---
# <span data-ttu-id="d0606-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d0606-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="d0606-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d0606-102">SYNOPSIS</span></span>
<span data-ttu-id="d0606-103">更新後端。</span><span class="sxs-lookup"><span data-stu-id="d0606-103">Updates a Backend.</span></span>

## <span data-ttu-id="d0606-104">句法</span><span class="sxs-lookup"><span data-stu-id="d0606-104">SYNTAX</span></span>

```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0606-105">說明</span><span class="sxs-lookup"><span data-stu-id="d0606-105">DESCRIPTION</span></span>
<span data-ttu-id="d0606-106">在 Api 管理中更新現有的後端。</span><span class="sxs-lookup"><span data-stu-id="d0606-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="d0606-107">示例</span><span class="sxs-lookup"><span data-stu-id="d0606-107">EXAMPLES</span></span>

### <span data-ttu-id="d0606-108">更新後端123的描述</span><span class="sxs-lookup"><span data-stu-id="d0606-108">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="d0606-109">參數</span><span class="sxs-lookup"><span data-stu-id="d0606-109">PARAMETERS</span></span>

### <span data-ttu-id="d0606-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="d0606-110">-BackendId</span></span>
<span data-ttu-id="d0606-111">新後端的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d0606-111">Identifier of new backend.</span></span>
<span data-ttu-id="d0606-112">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="d0606-112">This parameter is required.</span></span>

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

### <span data-ttu-id="d0606-113">-內容</span><span class="sxs-lookup"><span data-stu-id="d0606-113">-Context</span></span>
<span data-ttu-id="d0606-114">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="d0606-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d0606-115">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="d0606-115">This parameter is required.</span></span>

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

### <span data-ttu-id="d0606-116">-認證</span><span class="sxs-lookup"><span data-stu-id="d0606-116">-Credential</span></span>
<span data-ttu-id="d0606-117">在與後端交談時應使用的認證詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d0606-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="d0606-118">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="d0606-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="d0606-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0606-119">-DefaultProfile</span></span>
<span data-ttu-id="d0606-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d0606-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0606-121">-描述</span><span class="sxs-lookup"><span data-stu-id="d0606-121">-Description</span></span>
<span data-ttu-id="d0606-122">後端描述。</span><span class="sxs-lookup"><span data-stu-id="d0606-122">Backend Description.</span></span>
<span data-ttu-id="d0606-123">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="d0606-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="d0606-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0606-124">-PassThru</span></span>
<span data-ttu-id="d0606-125">指示這個 Cmdlet 會傳回這個 Cmdlet 修改的  **PsApiManagementBackend** 。</span><span class="sxs-lookup"><span data-stu-id="d0606-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d0606-126">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="d0606-126">-Protocol</span></span>
<span data-ttu-id="d0606-127">後端通訊通訊協定 (HTTP 或 soap) 。</span><span class="sxs-lookup"><span data-stu-id="d0606-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="d0606-128">此參數為選用。</span><span class="sxs-lookup"><span data-stu-id="d0606-128">This parameter is optional</span></span>

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

### <span data-ttu-id="d0606-129">-Proxy</span><span class="sxs-lookup"><span data-stu-id="d0606-129">-Proxy</span></span>
<span data-ttu-id="d0606-130">傳送要求給後所要使用的 Proxy 伺服器詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d0606-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="d0606-131">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="d0606-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="d0606-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0606-132">-ResourceId</span></span>
<span data-ttu-id="d0606-133">外部系統中資源的管理 Uri。</span><span class="sxs-lookup"><span data-stu-id="d0606-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="d0606-134">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="d0606-134">This parameter is optional.</span></span>
<span data-ttu-id="d0606-135">此 url 可以是邏輯 App、函數 App 或 Api App 的 Arm 資源 Id。</span><span class="sxs-lookup"><span data-stu-id="d0606-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="d0606-136">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="d0606-136">-ServiceFabricCluster</span></span>
<span data-ttu-id="d0606-137">Service Fabric 群集後端詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d0606-137">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="d0606-138">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="d0606-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="d0606-139">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="d0606-139">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="d0606-140">在與後端交談時，是否略過憑證連結驗證。</span><span class="sxs-lookup"><span data-stu-id="d0606-140">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="d0606-141">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="d0606-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="d0606-142">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="d0606-142">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="d0606-143">在與後端交談時，是否略過憑證名稱驗證。</span><span class="sxs-lookup"><span data-stu-id="d0606-143">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="d0606-144">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="d0606-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="d0606-145">-標題</span><span class="sxs-lookup"><span data-stu-id="d0606-145">-Title</span></span>
<span data-ttu-id="d0606-146">後端標題。</span><span class="sxs-lookup"><span data-stu-id="d0606-146">Backend Title.</span></span>
<span data-ttu-id="d0606-147">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="d0606-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="d0606-148">-Url</span><span class="sxs-lookup"><span data-stu-id="d0606-148">-Url</span></span>
<span data-ttu-id="d0606-149">後端的執行時間 Url。</span><span class="sxs-lookup"><span data-stu-id="d0606-149">Runtime Url for the Backend.</span></span>
<span data-ttu-id="d0606-150">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="d0606-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="d0606-151">-確認</span><span class="sxs-lookup"><span data-stu-id="d0606-151">-Confirm</span></span>
<span data-ttu-id="d0606-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d0606-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0606-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0606-153">-WhatIf</span></span>
<span data-ttu-id="d0606-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d0606-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0606-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d0606-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0606-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0606-156">CommonParameters</span></span>
<span data-ttu-id="d0606-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d0606-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0606-158">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d0606-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0606-159">輸入</span><span class="sxs-lookup"><span data-stu-id="d0606-159">INPUTS</span></span>

### <span data-ttu-id="d0606-160">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="d0606-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d0606-161">System.object</span><span class="sxs-lookup"><span data-stu-id="d0606-161">System.String</span></span>

### <span data-ttu-id="d0606-162">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d0606-162">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d0606-163">ServiceManagement. PsApiManagementBackendCredential （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="d0606-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="d0606-164">ServiceManagement. PsApiManagementBackendProxy （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="d0606-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="d0606-165">ServiceManagement. PsApiManagementServiceFabric （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="d0606-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="d0606-166">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="d0606-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d0606-167">輸出</span><span class="sxs-lookup"><span data-stu-id="d0606-167">OUTPUTS</span></span>

### <span data-ttu-id="d0606-168">ServiceManagement. PsApiManagementBackend （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="d0606-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="d0606-169">筆記</span><span class="sxs-lookup"><span data-stu-id="d0606-169">NOTES</span></span>

## <span data-ttu-id="d0606-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="d0606-170">RELATED LINKS</span></span>

[<span data-ttu-id="d0606-171">AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d0606-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="d0606-172">新-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d0606-172">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="d0606-173">新-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="d0606-173">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="d0606-174">新-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="d0606-174">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="d0606-175">移除-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d0606-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
