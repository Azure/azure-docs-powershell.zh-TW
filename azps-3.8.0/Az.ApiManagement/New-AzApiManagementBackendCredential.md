---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: c1495c505653470f4aa6b818162d57e02893c5e0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958201"
---
# <span data-ttu-id="9b1fa-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="9b1fa-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="9b1fa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9b1fa-102">SYNOPSIS</span></span>
<span data-ttu-id="9b1fa-103">建立新的後端認證協定。</span><span class="sxs-lookup"><span data-stu-id="9b1fa-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="9b1fa-104">句法</span><span class="sxs-lookup"><span data-stu-id="9b1fa-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b1fa-105">說明</span><span class="sxs-lookup"><span data-stu-id="9b1fa-105">DESCRIPTION</span></span>
<span data-ttu-id="9b1fa-106">建立新的後端認證協定。</span><span class="sxs-lookup"><span data-stu-id="9b1fa-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="9b1fa-107">示例</span><span class="sxs-lookup"><span data-stu-id="9b1fa-107">EXAMPLES</span></span>

### <span data-ttu-id="9b1fa-108">In-Memory 物件建立後端認證</span><span class="sxs-lookup"><span data-stu-id="9b1fa-108">Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="9b1fa-109">建立後端認證合約</span><span class="sxs-lookup"><span data-stu-id="9b1fa-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="9b1fa-110">參數</span><span class="sxs-lookup"><span data-stu-id="9b1fa-110">PARAMETERS</span></span>

### <span data-ttu-id="9b1fa-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="9b1fa-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="9b1fa-112">後端使用的授權標頭。</span><span class="sxs-lookup"><span data-stu-id="9b1fa-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="9b1fa-113">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="9b1fa-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="9b1fa-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="9b1fa-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="9b1fa-115">後端使用的授權配置。</span><span class="sxs-lookup"><span data-stu-id="9b1fa-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="9b1fa-116">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="9b1fa-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="9b1fa-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="9b1fa-117">-CertificateThumbprint</span></span>
<span data-ttu-id="9b1fa-118">用戶端憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="9b1fa-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="9b1fa-119">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="9b1fa-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="9b1fa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b1fa-120">-DefaultProfile</span></span>
<span data-ttu-id="9b1fa-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b1fa-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b1fa-122">-頁首</span><span class="sxs-lookup"><span data-stu-id="9b1fa-122">-Header</span></span>
<span data-ttu-id="9b1fa-123">後端接受的標頭參數值。</span><span class="sxs-lookup"><span data-stu-id="9b1fa-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="9b1fa-124">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="9b1fa-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="9b1fa-125">-Query</span><span class="sxs-lookup"><span data-stu-id="9b1fa-125">-Query</span></span>
<span data-ttu-id="9b1fa-126">後端接受的查詢參數值。</span><span class="sxs-lookup"><span data-stu-id="9b1fa-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="9b1fa-127">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="9b1fa-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="9b1fa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b1fa-128">CommonParameters</span></span>
<span data-ttu-id="9b1fa-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9b1fa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b1fa-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9b1fa-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b1fa-131">輸入</span><span class="sxs-lookup"><span data-stu-id="9b1fa-131">INPUTS</span></span>

### <span data-ttu-id="9b1fa-132">所有</span><span class="sxs-lookup"><span data-stu-id="9b1fa-132">None</span></span>

## <span data-ttu-id="9b1fa-133">輸出</span><span class="sxs-lookup"><span data-stu-id="9b1fa-133">OUTPUTS</span></span>

### <span data-ttu-id="9b1fa-134">ServiceManagement. PsApiManagementBackendCredential （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="9b1fa-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="9b1fa-135">筆記</span><span class="sxs-lookup"><span data-stu-id="9b1fa-135">NOTES</span></span>

## <span data-ttu-id="9b1fa-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b1fa-136">RELATED LINKS</span></span>

[<span data-ttu-id="9b1fa-137">AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9b1fa-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="9b1fa-138">新-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9b1fa-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="9b1fa-139">新-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="9b1fa-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="9b1fa-140">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9b1fa-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="9b1fa-141">移除-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9b1fa-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
