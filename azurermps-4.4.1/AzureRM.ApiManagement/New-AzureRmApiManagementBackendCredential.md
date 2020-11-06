---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
ms.openlocfilehash: 58f80b6ff1742bfc6360844648d6ad18d12d8389
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450114"
---
# <span data-ttu-id="d80e1-101">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="d80e1-101">New-AzureRmApiManagementBackendCredential</span></span>

## <span data-ttu-id="d80e1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d80e1-102">SYNOPSIS</span></span>
<span data-ttu-id="d80e1-103">建立新的後端認證協定。</span><span class="sxs-lookup"><span data-stu-id="d80e1-103">Creates a new Backend Credential contract.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d80e1-104">句法</span><span class="sxs-lookup"><span data-stu-id="d80e1-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d80e1-105">說明</span><span class="sxs-lookup"><span data-stu-id="d80e1-105">DESCRIPTION</span></span>
<span data-ttu-id="d80e1-106">建立新的後端認證協定。</span><span class="sxs-lookup"><span data-stu-id="d80e1-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="d80e1-107">示例</span><span class="sxs-lookup"><span data-stu-id="d80e1-107">EXAMPLES</span></span>

### <span data-ttu-id="d80e1-108">In-Memory 物件建立後端認證</span><span class="sxs-lookup"><span data-stu-id="d80e1-108">Create a Backend Credentials In-Memory Object</span></span>
```
$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}
```

<span data-ttu-id="d80e1-109">建立後端認證合約</span><span class="sxs-lookup"><span data-stu-id="d80e1-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="d80e1-110">參數</span><span class="sxs-lookup"><span data-stu-id="d80e1-110">PARAMETERS</span></span>

### <span data-ttu-id="d80e1-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="d80e1-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="d80e1-112">後端使用的授權標頭。</span><span class="sxs-lookup"><span data-stu-id="d80e1-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="d80e1-113">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="d80e1-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="d80e1-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="d80e1-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="d80e1-115">後端使用的授權配置。</span><span class="sxs-lookup"><span data-stu-id="d80e1-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="d80e1-116">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="d80e1-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="d80e1-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="d80e1-117">-CertificateThumbprint</span></span>
<span data-ttu-id="d80e1-118">用戶端憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="d80e1-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="d80e1-119">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="d80e1-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="d80e1-120">-頁首</span><span class="sxs-lookup"><span data-stu-id="d80e1-120">-Header</span></span>
<span data-ttu-id="d80e1-121">後端接受的標頭參數值。</span><span class="sxs-lookup"><span data-stu-id="d80e1-121">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="d80e1-122">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="d80e1-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="d80e1-123">-Query</span><span class="sxs-lookup"><span data-stu-id="d80e1-123">-Query</span></span>
<span data-ttu-id="d80e1-124">後端接受的查詢參數值。</span><span class="sxs-lookup"><span data-stu-id="d80e1-124">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="d80e1-125">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="d80e1-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="d80e1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d80e1-126">-DefaultProfile</span></span>
<span data-ttu-id="d80e1-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d80e1-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d80e1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d80e1-128">CommonParameters</span></span>
<span data-ttu-id="d80e1-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d80e1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d80e1-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d80e1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d80e1-131">輸入</span><span class="sxs-lookup"><span data-stu-id="d80e1-131">INPUTS</span></span>

## <span data-ttu-id="d80e1-132">輸出</span><span class="sxs-lookup"><span data-stu-id="d80e1-132">OUTPUTS</span></span>

### <span data-ttu-id="d80e1-133">ServiceManagement. PsApiManagementBackendCredential （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="d80e1-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="d80e1-134">筆記</span><span class="sxs-lookup"><span data-stu-id="d80e1-134">NOTES</span></span>

## <span data-ttu-id="d80e1-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="d80e1-135">RELATED LINKS</span></span>

[<span data-ttu-id="d80e1-136">AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d80e1-136">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="d80e1-137">新-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d80e1-137">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="d80e1-138">新-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="d80e1-138">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="d80e1-139">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d80e1-139">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="d80e1-140">移除-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d80e1-140">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
