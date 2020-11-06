---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
ms.openlocfilehash: c337e82c88c7fdbbc1f8a3663249126c9d92b19f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456291"
---
# <span data-ttu-id="4ae1c-101">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="4ae1c-101">New-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="4ae1c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4ae1c-102">SYNOPSIS</span></span>
<span data-ttu-id="4ae1c-103">建立新的後端實體。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-103">Creates a new backend entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ae1c-104">句法</span><span class="sxs-lookup"><span data-stu-id="4ae1c-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ae1c-105">說明</span><span class="sxs-lookup"><span data-stu-id="4ae1c-105">DESCRIPTION</span></span>
<span data-ttu-id="4ae1c-106">在 Api 管理中建立新的後端實體。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="4ae1c-107">示例</span><span class="sxs-lookup"><span data-stu-id="4ae1c-107">EXAMPLES</span></span>

### <span data-ttu-id="4ae1c-108">使用基本授權配置建立後123</span><span class="sxs-lookup"><span data-stu-id="4ae1c-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="4ae1c-109">建立新的後端</span><span class="sxs-lookup"><span data-stu-id="4ae1c-109">Creates a new Backend</span></span>

## <span data-ttu-id="4ae1c-110">參數</span><span class="sxs-lookup"><span data-stu-id="4ae1c-110">PARAMETERS</span></span>

### <span data-ttu-id="4ae1c-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="4ae1c-111">-BackendId</span></span>
<span data-ttu-id="4ae1c-112">新後端的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-112">Identifier of new backend.</span></span>
<span data-ttu-id="4ae1c-113">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-113">This parameter is optional.</span></span>
<span data-ttu-id="4ae1c-114">如果未指定，將會產生。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-114">If not specified will be generated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae1c-115">-內容</span><span class="sxs-lookup"><span data-stu-id="4ae1c-115">-Context</span></span>
<span data-ttu-id="4ae1c-116">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4ae1c-117">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-117">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae1c-118">-認證</span><span class="sxs-lookup"><span data-stu-id="4ae1c-118">-Credential</span></span>
<span data-ttu-id="4ae1c-119">在與後端交談時應使用的認證詳細資料。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="4ae1c-120">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-120">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementBackendCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae1c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ae1c-121">-DefaultProfile</span></span>
<span data-ttu-id="4ae1c-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ae1c-123">-描述</span><span class="sxs-lookup"><span data-stu-id="4ae1c-123">-Description</span></span>
<span data-ttu-id="4ae1c-124">後端描述。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-124">Backend Description.</span></span>
<span data-ttu-id="4ae1c-125">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-125">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae1c-126">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="4ae1c-126">-Protocol</span></span>
<span data-ttu-id="4ae1c-127">後端通訊通訊協定。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-127">Backend Communication protocol.</span></span>
<span data-ttu-id="4ae1c-128">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-128">This parameter is required.</span></span>
<span data-ttu-id="4ae1c-129">有效值為 "HTTP" 和 "soap"。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-129">Valid values are 'http' and 'soap'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae1c-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="4ae1c-130">-Proxy</span></span>
<span data-ttu-id="4ae1c-131">傳送要求給後所要使用的 Proxy 伺服器詳細資料。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="4ae1c-132">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-132">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementBackendProxy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae1c-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ae1c-133">-ResourceId</span></span>
<span data-ttu-id="4ae1c-134">外部系統中資源的管理 Uri。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="4ae1c-135">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-135">This parameter is optional.</span></span>
<span data-ttu-id="4ae1c-136">此 url 可以是邏輯 App、函數 App 或 Api App 的 Arm 資源 Id。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae1c-137">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="4ae1c-137">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="4ae1c-138">在與後端交談時，是否略過憑證連結驗證。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-138">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="4ae1c-139">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-139">This parameter is optional.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae1c-140">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="4ae1c-140">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="4ae1c-141">在與後端交談時，是否略過憑證名稱驗證。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-141">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="4ae1c-142">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-142">This parameter is optional.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae1c-143">-標題</span><span class="sxs-lookup"><span data-stu-id="4ae1c-143">-Title</span></span>
<span data-ttu-id="4ae1c-144">後端標題。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-144">Backend Title.</span></span>
<span data-ttu-id="4ae1c-145">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-145">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae1c-146">-Url</span><span class="sxs-lookup"><span data-stu-id="4ae1c-146">-Url</span></span>
<span data-ttu-id="4ae1c-147">後端的執行時間 Url。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-147">Runtime Url for the Backend.</span></span>
<span data-ttu-id="4ae1c-148">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-148">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae1c-149">-確認</span><span class="sxs-lookup"><span data-stu-id="4ae1c-149">-Confirm</span></span>
<span data-ttu-id="4ae1c-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ae1c-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ae1c-151">-WhatIf</span></span>
<span data-ttu-id="4ae1c-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ae1c-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ae1c-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ae1c-154">CommonParameters</span></span>
<span data-ttu-id="4ae1c-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ae1c-156">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ae1c-157">輸入</span><span class="sxs-lookup"><span data-stu-id="4ae1c-157">INPUTS</span></span>

### <span data-ttu-id="4ae1c-158">所有</span><span class="sxs-lookup"><span data-stu-id="4ae1c-158">None</span></span>
<span data-ttu-id="4ae1c-159">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="4ae1c-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4ae1c-160">輸出</span><span class="sxs-lookup"><span data-stu-id="4ae1c-160">OUTPUTS</span></span>

### <span data-ttu-id="4ae1c-161">ServiceManagement. PsApiManagementBackend （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="4ae1c-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="4ae1c-162">筆記</span><span class="sxs-lookup"><span data-stu-id="4ae1c-162">NOTES</span></span>

## <span data-ttu-id="4ae1c-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ae1c-163">RELATED LINKS</span></span>

[<span data-ttu-id="4ae1c-164">AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="4ae1c-164">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="4ae1c-165">新-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="4ae1c-165">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="4ae1c-166">新-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="4ae1c-166">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="4ae1c-167">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="4ae1c-167">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="4ae1c-168">移除-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="4ae1c-168">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)

