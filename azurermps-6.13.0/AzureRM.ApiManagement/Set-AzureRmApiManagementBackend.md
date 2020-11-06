---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
ms.openlocfilehash: 52e159ae0f9d1b94b316394ddefe04f0bd8aa1c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444111"
---
# <span data-ttu-id="957db-101">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="957db-101">Set-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="957db-102">摘要</span><span class="sxs-lookup"><span data-stu-id="957db-102">SYNOPSIS</span></span>
<span data-ttu-id="957db-103">更新後端。</span><span class="sxs-lookup"><span data-stu-id="957db-103">Updates a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="957db-104">句法</span><span class="sxs-lookup"><span data-stu-id="957db-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="957db-105">說明</span><span class="sxs-lookup"><span data-stu-id="957db-105">DESCRIPTION</span></span>
<span data-ttu-id="957db-106">在 Api 管理中更新現有的後端。</span><span class="sxs-lookup"><span data-stu-id="957db-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="957db-107">示例</span><span class="sxs-lookup"><span data-stu-id="957db-107">EXAMPLES</span></span>

### <span data-ttu-id="957db-108">更新後端123的描述</span><span class="sxs-lookup"><span data-stu-id="957db-108">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="957db-109">參數</span><span class="sxs-lookup"><span data-stu-id="957db-109">PARAMETERS</span></span>

### <span data-ttu-id="957db-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="957db-110">-BackendId</span></span>
<span data-ttu-id="957db-111">新後端的識別碼。</span><span class="sxs-lookup"><span data-stu-id="957db-111">Identifier of new backend.</span></span>
<span data-ttu-id="957db-112">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="957db-112">This parameter is required.</span></span>

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

### <span data-ttu-id="957db-113">-內容</span><span class="sxs-lookup"><span data-stu-id="957db-113">-Context</span></span>
<span data-ttu-id="957db-114">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="957db-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="957db-115">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="957db-115">This parameter is required.</span></span>

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

### <span data-ttu-id="957db-116">-認證</span><span class="sxs-lookup"><span data-stu-id="957db-116">-Credential</span></span>
<span data-ttu-id="957db-117">在與後端交談時應使用的認證詳細資料。</span><span class="sxs-lookup"><span data-stu-id="957db-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="957db-118">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="957db-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="957db-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="957db-119">-DefaultProfile</span></span>
<span data-ttu-id="957db-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="957db-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="957db-121">-描述</span><span class="sxs-lookup"><span data-stu-id="957db-121">-Description</span></span>
<span data-ttu-id="957db-122">後端描述。</span><span class="sxs-lookup"><span data-stu-id="957db-122">Backend Description.</span></span>
<span data-ttu-id="957db-123">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="957db-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="957db-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="957db-124">-PassThru</span></span>
<span data-ttu-id="957db-125">指示這個 Cmdlet 會傳回這個 Cmdlet 修改的  **PsApiManagementBackend** 。</span><span class="sxs-lookup"><span data-stu-id="957db-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="957db-126">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="957db-126">-Protocol</span></span>
<span data-ttu-id="957db-127">後端通訊通訊協定 (HTTP 或 soap) 。</span><span class="sxs-lookup"><span data-stu-id="957db-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="957db-128">此參數為選用。</span><span class="sxs-lookup"><span data-stu-id="957db-128">This parameter is optional</span></span>

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

### <span data-ttu-id="957db-129">-Proxy</span><span class="sxs-lookup"><span data-stu-id="957db-129">-Proxy</span></span>
<span data-ttu-id="957db-130">傳送要求給後所要使用的 Proxy 伺服器詳細資料。</span><span class="sxs-lookup"><span data-stu-id="957db-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="957db-131">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="957db-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="957db-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="957db-132">-ResourceId</span></span>
<span data-ttu-id="957db-133">外部系統中資源的管理 Uri。</span><span class="sxs-lookup"><span data-stu-id="957db-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="957db-134">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="957db-134">This parameter is optional.</span></span>
<span data-ttu-id="957db-135">此 url 可以是邏輯 App、函數 App 或 Api App 的 Arm 資源 Id。</span><span class="sxs-lookup"><span data-stu-id="957db-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="957db-136">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="957db-136">-ServiceFabricCluster</span></span>
<span data-ttu-id="957db-137">Service Fabric 群集後端詳細資料。</span><span class="sxs-lookup"><span data-stu-id="957db-137">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="957db-138">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="957db-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="957db-139">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="957db-139">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="957db-140">在與後端交談時，是否略過憑證連結驗證。</span><span class="sxs-lookup"><span data-stu-id="957db-140">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="957db-141">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="957db-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="957db-142">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="957db-142">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="957db-143">在與後端交談時，是否略過憑證名稱驗證。</span><span class="sxs-lookup"><span data-stu-id="957db-143">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="957db-144">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="957db-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="957db-145">-標題</span><span class="sxs-lookup"><span data-stu-id="957db-145">-Title</span></span>
<span data-ttu-id="957db-146">後端標題。</span><span class="sxs-lookup"><span data-stu-id="957db-146">Backend Title.</span></span>
<span data-ttu-id="957db-147">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="957db-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="957db-148">-Url</span><span class="sxs-lookup"><span data-stu-id="957db-148">-Url</span></span>
<span data-ttu-id="957db-149">後端的執行時間 Url。</span><span class="sxs-lookup"><span data-stu-id="957db-149">Runtime Url for the Backend.</span></span>
<span data-ttu-id="957db-150">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="957db-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="957db-151">-確認</span><span class="sxs-lookup"><span data-stu-id="957db-151">-Confirm</span></span>
<span data-ttu-id="957db-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="957db-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="957db-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="957db-153">-WhatIf</span></span>
<span data-ttu-id="957db-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="957db-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="957db-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="957db-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="957db-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="957db-156">CommonParameters</span></span>
<span data-ttu-id="957db-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="957db-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="957db-158">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="957db-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="957db-159">輸入</span><span class="sxs-lookup"><span data-stu-id="957db-159">INPUTS</span></span>

### <span data-ttu-id="957db-160">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="957db-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="957db-161">System.object</span><span class="sxs-lookup"><span data-stu-id="957db-161">System.String</span></span>

### <span data-ttu-id="957db-162">系統為 Nullable "1 [[System.object，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="957db-162">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="957db-163">ServiceManagement. PsApiManagementBackendCredential （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="957db-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="957db-164">ServiceManagement. PsApiManagementBackendProxy （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="957db-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="957db-165">ServiceManagement. PsApiManagementServiceFabric （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="957db-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="957db-166">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="957db-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="957db-167">輸出</span><span class="sxs-lookup"><span data-stu-id="957db-167">OUTPUTS</span></span>

### <span data-ttu-id="957db-168">ServiceManagement. PsApiManagementBackend （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="957db-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="957db-169">筆記</span><span class="sxs-lookup"><span data-stu-id="957db-169">NOTES</span></span>

## <span data-ttu-id="957db-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="957db-170">RELATED LINKS</span></span>

[<span data-ttu-id="957db-171">AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="957db-171">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="957db-172">新-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="957db-172">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="957db-173">新-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="957db-173">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="957db-174">新-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="957db-174">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="957db-175">移除-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="957db-175">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
