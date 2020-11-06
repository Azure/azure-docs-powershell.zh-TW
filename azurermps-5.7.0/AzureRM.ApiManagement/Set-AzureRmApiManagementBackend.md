---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
ms.openlocfilehash: b5e51891f82b2a12f42fac3a1535f974912ca1dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449423"
---
# <span data-ttu-id="71fdd-101">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="71fdd-101">Set-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="71fdd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="71fdd-102">SYNOPSIS</span></span>
<span data-ttu-id="71fdd-103">更新後端。</span><span class="sxs-lookup"><span data-stu-id="71fdd-103">Updates a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71fdd-104">句法</span><span class="sxs-lookup"><span data-stu-id="71fdd-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71fdd-105">說明</span><span class="sxs-lookup"><span data-stu-id="71fdd-105">DESCRIPTION</span></span>
<span data-ttu-id="71fdd-106">在 Api 管理中更新現有的後端。</span><span class="sxs-lookup"><span data-stu-id="71fdd-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="71fdd-107">示例</span><span class="sxs-lookup"><span data-stu-id="71fdd-107">EXAMPLES</span></span>

### <span data-ttu-id="71fdd-108">更新後端123的描述</span><span class="sxs-lookup"><span data-stu-id="71fdd-108">Updates the Description of the Backend 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="71fdd-109">參數</span><span class="sxs-lookup"><span data-stu-id="71fdd-109">PARAMETERS</span></span>

### <span data-ttu-id="71fdd-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="71fdd-110">-BackendId</span></span>
<span data-ttu-id="71fdd-111">新後端的識別碼。</span><span class="sxs-lookup"><span data-stu-id="71fdd-111">Identifier of new backend.</span></span>
<span data-ttu-id="71fdd-112">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="71fdd-112">This parameter is required.</span></span>

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

### <span data-ttu-id="71fdd-113">-內容</span><span class="sxs-lookup"><span data-stu-id="71fdd-113">-Context</span></span>
<span data-ttu-id="71fdd-114">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="71fdd-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="71fdd-115">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="71fdd-115">This parameter is required.</span></span>

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

### <span data-ttu-id="71fdd-116">-認證</span><span class="sxs-lookup"><span data-stu-id="71fdd-116">-Credential</span></span>
<span data-ttu-id="71fdd-117">在與後端交談時應使用的認證詳細資料。</span><span class="sxs-lookup"><span data-stu-id="71fdd-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="71fdd-118">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="71fdd-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="71fdd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71fdd-119">-DefaultProfile</span></span>
<span data-ttu-id="71fdd-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="71fdd-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="71fdd-121">-描述</span><span class="sxs-lookup"><span data-stu-id="71fdd-121">-Description</span></span>
<span data-ttu-id="71fdd-122">後端描述。</span><span class="sxs-lookup"><span data-stu-id="71fdd-122">Backend Description.</span></span>
<span data-ttu-id="71fdd-123">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="71fdd-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="71fdd-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71fdd-124">-PassThru</span></span>
<span data-ttu-id="71fdd-125">指示這個 Cmdlet 會傳回這個 Cmdlet 修改的  **PsApiManagementBackend** 。</span><span class="sxs-lookup"><span data-stu-id="71fdd-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71fdd-126">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="71fdd-126">-Protocol</span></span>
<span data-ttu-id="71fdd-127">後端通訊通訊協定 (HTTP 或 soap) 。</span><span class="sxs-lookup"><span data-stu-id="71fdd-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="71fdd-128">此參數為選用。</span><span class="sxs-lookup"><span data-stu-id="71fdd-128">This parameter is optional</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71fdd-129">-Proxy</span><span class="sxs-lookup"><span data-stu-id="71fdd-129">-Proxy</span></span>
<span data-ttu-id="71fdd-130">傳送要求給後所要使用的 Proxy 伺服器詳細資料。</span><span class="sxs-lookup"><span data-stu-id="71fdd-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="71fdd-131">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="71fdd-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="71fdd-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71fdd-132">-ResourceId</span></span>
<span data-ttu-id="71fdd-133">外部系統中資源的管理 Uri。</span><span class="sxs-lookup"><span data-stu-id="71fdd-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="71fdd-134">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="71fdd-134">This parameter is optional.</span></span>
<span data-ttu-id="71fdd-135">此 url 可以是邏輯 App、函數 App 或 Api App 的 Arm 資源 Id。</span><span class="sxs-lookup"><span data-stu-id="71fdd-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="71fdd-136">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="71fdd-136">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="71fdd-137">在與後端交談時，是否略過憑證連結驗證。</span><span class="sxs-lookup"><span data-stu-id="71fdd-137">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="71fdd-138">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="71fdd-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="71fdd-139">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="71fdd-139">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="71fdd-140">在與後端交談時，是否略過憑證名稱驗證。</span><span class="sxs-lookup"><span data-stu-id="71fdd-140">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="71fdd-141">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="71fdd-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="71fdd-142">-標題</span><span class="sxs-lookup"><span data-stu-id="71fdd-142">-Title</span></span>
<span data-ttu-id="71fdd-143">後端標題。</span><span class="sxs-lookup"><span data-stu-id="71fdd-143">Backend Title.</span></span>
<span data-ttu-id="71fdd-144">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="71fdd-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="71fdd-145">-Url</span><span class="sxs-lookup"><span data-stu-id="71fdd-145">-Url</span></span>
<span data-ttu-id="71fdd-146">後端的執行時間 Url。</span><span class="sxs-lookup"><span data-stu-id="71fdd-146">Runtime Url for the Backend.</span></span>
<span data-ttu-id="71fdd-147">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="71fdd-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="71fdd-148">-確認</span><span class="sxs-lookup"><span data-stu-id="71fdd-148">-Confirm</span></span>
<span data-ttu-id="71fdd-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="71fdd-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71fdd-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71fdd-150">-WhatIf</span></span>
<span data-ttu-id="71fdd-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="71fdd-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71fdd-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="71fdd-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71fdd-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71fdd-153">CommonParameters</span></span>
<span data-ttu-id="71fdd-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="71fdd-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71fdd-155">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="71fdd-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71fdd-156">輸入</span><span class="sxs-lookup"><span data-stu-id="71fdd-156">INPUTS</span></span>

### <span data-ttu-id="71fdd-157">所有</span><span class="sxs-lookup"><span data-stu-id="71fdd-157">None</span></span>
<span data-ttu-id="71fdd-158">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="71fdd-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="71fdd-159">輸出</span><span class="sxs-lookup"><span data-stu-id="71fdd-159">OUTPUTS</span></span>

### <span data-ttu-id="71fdd-160">ServiceManagement. PsApiManagementBackend （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="71fdd-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="71fdd-161">筆記</span><span class="sxs-lookup"><span data-stu-id="71fdd-161">NOTES</span></span>

## <span data-ttu-id="71fdd-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="71fdd-162">RELATED LINKS</span></span>

[<span data-ttu-id="71fdd-163">AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="71fdd-163">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="71fdd-164">新-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="71fdd-164">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="71fdd-165">新-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="71fdd-165">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="71fdd-166">新-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="71fdd-166">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="71fdd-167">移除-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="71fdd-167">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
