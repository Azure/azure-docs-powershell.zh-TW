---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
ms.openlocfilehash: d34a7666e10fe678d49194887d9b58e7c1ba0aa7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447524"
---
# <span data-ttu-id="cf077-101">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="cf077-101">New-AzureRmApiManagementBackendCredential</span></span>

## <span data-ttu-id="cf077-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cf077-102">SYNOPSIS</span></span>
<span data-ttu-id="cf077-103">建立新的後端認證協定。</span><span class="sxs-lookup"><span data-stu-id="cf077-103">Creates a new Backend Credential contract.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf077-104">句法</span><span class="sxs-lookup"><span data-stu-id="cf077-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf077-105">說明</span><span class="sxs-lookup"><span data-stu-id="cf077-105">DESCRIPTION</span></span>
<span data-ttu-id="cf077-106">建立新的後端認證協定。</span><span class="sxs-lookup"><span data-stu-id="cf077-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="cf077-107">示例</span><span class="sxs-lookup"><span data-stu-id="cf077-107">EXAMPLES</span></span>

### <span data-ttu-id="cf077-108">In-Memory 物件建立後端認證</span><span class="sxs-lookup"><span data-stu-id="cf077-108">Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="cf077-109">建立後端認證合約</span><span class="sxs-lookup"><span data-stu-id="cf077-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="cf077-110">參數</span><span class="sxs-lookup"><span data-stu-id="cf077-110">PARAMETERS</span></span>

### <span data-ttu-id="cf077-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="cf077-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="cf077-112">後端使用的授權標頭。</span><span class="sxs-lookup"><span data-stu-id="cf077-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="cf077-113">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="cf077-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="cf077-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="cf077-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="cf077-115">後端使用的授權配置。</span><span class="sxs-lookup"><span data-stu-id="cf077-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="cf077-116">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="cf077-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="cf077-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="cf077-117">-CertificateThumbprint</span></span>
<span data-ttu-id="cf077-118">用戶端憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="cf077-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="cf077-119">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="cf077-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="cf077-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf077-120">-DefaultProfile</span></span>
<span data-ttu-id="cf077-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf077-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf077-122">-頁首</span><span class="sxs-lookup"><span data-stu-id="cf077-122">-Header</span></span>
<span data-ttu-id="cf077-123">後端接受的標頭參數值。</span><span class="sxs-lookup"><span data-stu-id="cf077-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="cf077-124">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="cf077-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="cf077-125">-Query</span><span class="sxs-lookup"><span data-stu-id="cf077-125">-Query</span></span>
<span data-ttu-id="cf077-126">後端接受的查詢參數值。</span><span class="sxs-lookup"><span data-stu-id="cf077-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="cf077-127">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="cf077-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="cf077-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf077-128">CommonParameters</span></span>
<span data-ttu-id="cf077-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cf077-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf077-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cf077-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf077-131">輸入</span><span class="sxs-lookup"><span data-stu-id="cf077-131">INPUTS</span></span>

### <span data-ttu-id="cf077-132">所有</span><span class="sxs-lookup"><span data-stu-id="cf077-132">None</span></span>

## <span data-ttu-id="cf077-133">輸出</span><span class="sxs-lookup"><span data-stu-id="cf077-133">OUTPUTS</span></span>

### <span data-ttu-id="cf077-134">ServiceManagement. PsApiManagementBackendCredential （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="cf077-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="cf077-135">筆記</span><span class="sxs-lookup"><span data-stu-id="cf077-135">NOTES</span></span>

## <span data-ttu-id="cf077-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf077-136">RELATED LINKS</span></span>

[<span data-ttu-id="cf077-137">AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="cf077-137">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="cf077-138">新-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="cf077-138">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="cf077-139">新-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="cf077-139">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="cf077-140">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="cf077-140">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="cf077-141">移除-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="cf077-141">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
