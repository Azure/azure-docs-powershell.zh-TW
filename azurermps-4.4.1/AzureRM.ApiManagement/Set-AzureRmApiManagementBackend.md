---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
ms.openlocfilehash: 85545777f5a76f3f75e81648a009ffcdcad8ab30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625725"
---
# <span data-ttu-id="2590c-101">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2590c-101">Set-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="2590c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2590c-102">SYNOPSIS</span></span>
<span data-ttu-id="2590c-103">更新後端。</span><span class="sxs-lookup"><span data-stu-id="2590c-103">Updates a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2590c-104">句法</span><span class="sxs-lookup"><span data-stu-id="2590c-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2590c-105">說明</span><span class="sxs-lookup"><span data-stu-id="2590c-105">DESCRIPTION</span></span>
<span data-ttu-id="2590c-106">在 Api 管理中更新現有的後端。</span><span class="sxs-lookup"><span data-stu-id="2590c-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="2590c-107">示例</span><span class="sxs-lookup"><span data-stu-id="2590c-107">EXAMPLES</span></span>

### <span data-ttu-id="2590c-108">更新後端123的描述</span><span class="sxs-lookup"><span data-stu-id="2590c-108">Updates the Description of the Backend 123</span></span>
```
Set-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="2590c-109">參數</span><span class="sxs-lookup"><span data-stu-id="2590c-109">PARAMETERS</span></span>

### <span data-ttu-id="2590c-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="2590c-110">-BackendId</span></span>
<span data-ttu-id="2590c-111">新後端的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2590c-111">Identifier of new backend.</span></span>
<span data-ttu-id="2590c-112">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="2590c-112">This parameter is required.</span></span>

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

### <span data-ttu-id="2590c-113">-內容</span><span class="sxs-lookup"><span data-stu-id="2590c-113">-Context</span></span>
<span data-ttu-id="2590c-114">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="2590c-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2590c-115">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="2590c-115">This parameter is required.</span></span>

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

### <span data-ttu-id="2590c-116">-認證</span><span class="sxs-lookup"><span data-stu-id="2590c-116">-Credential</span></span>
<span data-ttu-id="2590c-117">在與後端交談時應使用的認證詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2590c-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="2590c-118">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="2590c-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="2590c-119">-描述</span><span class="sxs-lookup"><span data-stu-id="2590c-119">-Description</span></span>
<span data-ttu-id="2590c-120">後端描述。</span><span class="sxs-lookup"><span data-stu-id="2590c-120">Backend Description.</span></span>
<span data-ttu-id="2590c-121">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="2590c-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="2590c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2590c-122">-PassThru</span></span>
<span data-ttu-id="2590c-123">指示這個 Cmdlet 會傳回這個 Cmdlet 修改的  **PsApiManagementBackend** 。</span><span class="sxs-lookup"><span data-stu-id="2590c-123">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2590c-124">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="2590c-124">-Protocol</span></span>
<span data-ttu-id="2590c-125">後端通訊通訊協定 (HTTP 或 soap) 。</span><span class="sxs-lookup"><span data-stu-id="2590c-125">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="2590c-126">此參數為選用。</span><span class="sxs-lookup"><span data-stu-id="2590c-126">This parameter is optional</span></span>

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

### <span data-ttu-id="2590c-127">-Proxy</span><span class="sxs-lookup"><span data-stu-id="2590c-127">-Proxy</span></span>
<span data-ttu-id="2590c-128">傳送要求給後所要使用的 Proxy 伺服器詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2590c-128">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="2590c-129">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="2590c-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="2590c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2590c-130">-ResourceId</span></span>
<span data-ttu-id="2590c-131">外部系統中資源的管理 Uri。</span><span class="sxs-lookup"><span data-stu-id="2590c-131">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="2590c-132">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="2590c-132">This parameter is optional.</span></span>
<span data-ttu-id="2590c-133">此 url 可以是邏輯 App、函數 App 或 Api App 的 Arm 資源 Id。</span><span class="sxs-lookup"><span data-stu-id="2590c-133">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="2590c-134">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="2590c-134">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="2590c-135">在與後端交談時，是否略過憑證連結驗證。</span><span class="sxs-lookup"><span data-stu-id="2590c-135">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="2590c-136">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="2590c-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="2590c-137">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="2590c-137">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="2590c-138">在與後端交談時，是否略過憑證名稱驗證。</span><span class="sxs-lookup"><span data-stu-id="2590c-138">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="2590c-139">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="2590c-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="2590c-140">-標題</span><span class="sxs-lookup"><span data-stu-id="2590c-140">-Title</span></span>
<span data-ttu-id="2590c-141">後端標題。</span><span class="sxs-lookup"><span data-stu-id="2590c-141">Backend Title.</span></span>
<span data-ttu-id="2590c-142">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="2590c-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="2590c-143">-Url</span><span class="sxs-lookup"><span data-stu-id="2590c-143">-Url</span></span>
<span data-ttu-id="2590c-144">後端的執行時間 Url。</span><span class="sxs-lookup"><span data-stu-id="2590c-144">Runtime Url for the Backend.</span></span>
<span data-ttu-id="2590c-145">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="2590c-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="2590c-146">-確認</span><span class="sxs-lookup"><span data-stu-id="2590c-146">-Confirm</span></span>
<span data-ttu-id="2590c-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2590c-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2590c-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2590c-148">-WhatIf</span></span>
<span data-ttu-id="2590c-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2590c-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2590c-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2590c-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2590c-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2590c-151">-DefaultProfile</span></span>
<span data-ttu-id="2590c-152">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2590c-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2590c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2590c-153">CommonParameters</span></span>
<span data-ttu-id="2590c-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2590c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2590c-155">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2590c-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2590c-156">輸入</span><span class="sxs-lookup"><span data-stu-id="2590c-156">INPUTS</span></span>

## <span data-ttu-id="2590c-157">輸出</span><span class="sxs-lookup"><span data-stu-id="2590c-157">OUTPUTS</span></span>

### <span data-ttu-id="2590c-158">ServiceManagement. PsApiManagementBackend （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="2590c-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="2590c-159">筆記</span><span class="sxs-lookup"><span data-stu-id="2590c-159">NOTES</span></span>

## <span data-ttu-id="2590c-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="2590c-160">RELATED LINKS</span></span>

[<span data-ttu-id="2590c-161">AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2590c-161">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="2590c-162">新-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2590c-162">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="2590c-163">新-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="2590c-163">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="2590c-164">新-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="2590c-164">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="2590c-165">移除-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2590c-165">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
