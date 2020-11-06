---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: 2cde898622c870dc0598639addb1e8b30e438076
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614003"
---
# <span data-ttu-id="a5678-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="a5678-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="a5678-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a5678-102">SYNOPSIS</span></span>
<span data-ttu-id="a5678-103">建立新的後端認證協定。</span><span class="sxs-lookup"><span data-stu-id="a5678-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="a5678-104">句法</span><span class="sxs-lookup"><span data-stu-id="a5678-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5678-105">說明</span><span class="sxs-lookup"><span data-stu-id="a5678-105">DESCRIPTION</span></span>
<span data-ttu-id="a5678-106">建立新的後端認證協定。</span><span class="sxs-lookup"><span data-stu-id="a5678-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="a5678-107">示例</span><span class="sxs-lookup"><span data-stu-id="a5678-107">EXAMPLES</span></span>

### <span data-ttu-id="a5678-108">In-Memory 物件建立後端認證</span><span class="sxs-lookup"><span data-stu-id="a5678-108">Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="a5678-109">建立後端認證合約</span><span class="sxs-lookup"><span data-stu-id="a5678-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="a5678-110">參數</span><span class="sxs-lookup"><span data-stu-id="a5678-110">PARAMETERS</span></span>

### <span data-ttu-id="a5678-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="a5678-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="a5678-112">後端使用的授權標頭。</span><span class="sxs-lookup"><span data-stu-id="a5678-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="a5678-113">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="a5678-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="a5678-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="a5678-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="a5678-115">後端使用的授權配置。</span><span class="sxs-lookup"><span data-stu-id="a5678-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="a5678-116">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="a5678-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="a5678-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="a5678-117">-CertificateThumbprint</span></span>
<span data-ttu-id="a5678-118">用戶端憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="a5678-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="a5678-119">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="a5678-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="a5678-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5678-120">-DefaultProfile</span></span>
<span data-ttu-id="a5678-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a5678-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5678-122">-頁首</span><span class="sxs-lookup"><span data-stu-id="a5678-122">-Header</span></span>
<span data-ttu-id="a5678-123">後端接受的標頭參數值。</span><span class="sxs-lookup"><span data-stu-id="a5678-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="a5678-124">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="a5678-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="a5678-125">-Query</span><span class="sxs-lookup"><span data-stu-id="a5678-125">-Query</span></span>
<span data-ttu-id="a5678-126">後端接受的查詢參數值。</span><span class="sxs-lookup"><span data-stu-id="a5678-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="a5678-127">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="a5678-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="a5678-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5678-128">CommonParameters</span></span>
<span data-ttu-id="a5678-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a5678-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5678-130">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a5678-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5678-131">輸入</span><span class="sxs-lookup"><span data-stu-id="a5678-131">INPUTS</span></span>

### <span data-ttu-id="a5678-132">所有</span><span class="sxs-lookup"><span data-stu-id="a5678-132">None</span></span>

## <span data-ttu-id="a5678-133">輸出</span><span class="sxs-lookup"><span data-stu-id="a5678-133">OUTPUTS</span></span>

### <span data-ttu-id="a5678-134">ServiceManagement. PsApiManagementBackendCredential （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="a5678-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="a5678-135">筆記</span><span class="sxs-lookup"><span data-stu-id="a5678-135">NOTES</span></span>

## <span data-ttu-id="a5678-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5678-136">RELATED LINKS</span></span>

[<span data-ttu-id="a5678-137">AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a5678-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="a5678-138">新-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a5678-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="a5678-139">新-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="a5678-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="a5678-140">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a5678-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="a5678-141">移除-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a5678-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
