---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: 3d9a462a034c5c1e65ff6b22fe92b14421582392
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401261"
---
# <span data-ttu-id="38540-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="38540-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="38540-102">簡介</span><span class="sxs-lookup"><span data-stu-id="38540-102">SYNOPSIS</span></span>
<span data-ttu-id="38540-103">建立新的後端認證合約。</span><span class="sxs-lookup"><span data-stu-id="38540-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="38540-104">語法</span><span class="sxs-lookup"><span data-stu-id="38540-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38540-105">描述</span><span class="sxs-lookup"><span data-stu-id="38540-105">DESCRIPTION</span></span>
<span data-ttu-id="38540-106">建立新的後端認證合約。</span><span class="sxs-lookup"><span data-stu-id="38540-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="38540-107">例子</span><span class="sxs-lookup"><span data-stu-id="38540-107">EXAMPLES</span></span>

### <span data-ttu-id="38540-108">建立物件的後端認證In-Memory認證</span><span class="sxs-lookup"><span data-stu-id="38540-108">Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="38540-109">建立後端認證合約</span><span class="sxs-lookup"><span data-stu-id="38540-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="38540-110">參數</span><span class="sxs-lookup"><span data-stu-id="38540-110">PARAMETERS</span></span>

### <span data-ttu-id="38540-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="38540-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="38540-112">後端使用的授權標頭。</span><span class="sxs-lookup"><span data-stu-id="38540-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="38540-113">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="38540-113">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38540-114">-AuthorizationHeaderS化</span><span class="sxs-lookup"><span data-stu-id="38540-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="38540-115">後端所使用的授權方案。</span><span class="sxs-lookup"><span data-stu-id="38540-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="38540-116">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="38540-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38540-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="38540-117">-CertificateThumbprint</span></span>
<span data-ttu-id="38540-118">用戶端憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="38540-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="38540-119">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="38540-119">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38540-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38540-120">-DefaultProfile</span></span>
<span data-ttu-id="38540-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="38540-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38540-122">-頁眉</span><span class="sxs-lookup"><span data-stu-id="38540-122">-Header</span></span>
<span data-ttu-id="38540-123">後端接受的標題參數值。</span><span class="sxs-lookup"><span data-stu-id="38540-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="38540-124">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="38540-124">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38540-125">-查詢</span><span class="sxs-lookup"><span data-stu-id="38540-125">-Query</span></span>
<span data-ttu-id="38540-126">後端接受的查詢參數值。</span><span class="sxs-lookup"><span data-stu-id="38540-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="38540-127">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="38540-127">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38540-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38540-128">CommonParameters</span></span>
<span data-ttu-id="38540-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="38540-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38540-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38540-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38540-131">輸入</span><span class="sxs-lookup"><span data-stu-id="38540-131">INPUTS</span></span>

### <span data-ttu-id="38540-132">沒有</span><span class="sxs-lookup"><span data-stu-id="38540-132">None</span></span>

## <span data-ttu-id="38540-133">輸出</span><span class="sxs-lookup"><span data-stu-id="38540-133">OUTPUTS</span></span>

### <span data-ttu-id="38540-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="38540-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="38540-135">筆記</span><span class="sxs-lookup"><span data-stu-id="38540-135">NOTES</span></span>

## <span data-ttu-id="38540-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="38540-136">RELATED LINKS</span></span>

[<span data-ttu-id="38540-137">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="38540-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="38540-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="38540-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="38540-139">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="38540-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="38540-140">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="38540-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="38540-141">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="38540-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
