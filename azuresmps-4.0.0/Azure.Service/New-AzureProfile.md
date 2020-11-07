---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 159CAD26-710A-4E65-B015-015A2C336A91
online version: ''
schema: 2.0.0
ms.openlocfilehash: a224ac58e6a8344953e29164de6ac6cfe0d00d97
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967446"
---
# <span data-ttu-id="2f3ee-101">New-AzureProfile</span><span class="sxs-lookup"><span data-stu-id="2f3ee-101">New-AzureProfile</span></span>

## <span data-ttu-id="2f3ee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2f3ee-102">SYNOPSIS</span></span>

## <span data-ttu-id="2f3ee-103">句法</span><span class="sxs-lookup"><span data-stu-id="2f3ee-103">SYNTAX</span></span>

### <span data-ttu-id="2f3ee-104">憑證</span><span class="sxs-lookup"><span data-stu-id="2f3ee-104">Certificate</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -Certificate <X509Certificate2> [<CommonParameters>]
```

### <span data-ttu-id="2f3ee-105">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2f3ee-105">ServicePrincipal</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -Credential <PSCredential> -Tenant <String> [-ServicePrincipal] [<CommonParameters>]
```

### <span data-ttu-id="2f3ee-106">牌</span><span class="sxs-lookup"><span data-stu-id="2f3ee-106">Token</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -AccessToken <String> -AccountId <String> [<CommonParameters>]
```

### <span data-ttu-id="2f3ee-107">憑證</span><span class="sxs-lookup"><span data-stu-id="2f3ee-107">Credentials</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -Credential <PSCredential> [-Tenant <String>] [<CommonParameters>]
```

### <span data-ttu-id="2f3ee-108">有空</span><span class="sxs-lookup"><span data-stu-id="2f3ee-108">Empty</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] [<CommonParameters>]
```

### <span data-ttu-id="2f3ee-109">檔案</span><span class="sxs-lookup"><span data-stu-id="2f3ee-109">File</span></span>
```
New-AzureProfile -Path <String> [<CommonParameters>]
```

### <span data-ttu-id="2f3ee-110">PropertyBag</span><span class="sxs-lookup"><span data-stu-id="2f3ee-110">PropertyBag</span></span>
```
New-AzureProfile -Properties <Hashtable> [<CommonParameters>]
```

## <span data-ttu-id="2f3ee-111">說明</span><span class="sxs-lookup"><span data-stu-id="2f3ee-111">DESCRIPTION</span></span>

## <span data-ttu-id="2f3ee-112">示例</span><span class="sxs-lookup"><span data-stu-id="2f3ee-112">EXAMPLES</span></span>

### <span data-ttu-id="2f3ee-113">sr-1</span><span class="sxs-lookup"><span data-stu-id="2f3ee-113">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="2f3ee-114">參數</span><span class="sxs-lookup"><span data-stu-id="2f3ee-114">PARAMETERS</span></span>

### <span data-ttu-id="2f3ee-115">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="2f3ee-115">-AccessToken</span></span>
```yaml
Type: String
Parameter Sets: Token
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f3ee-116">-AccountId</span><span class="sxs-lookup"><span data-stu-id="2f3ee-116">-AccountId</span></span>
```yaml
Type: String
Parameter Sets: Token
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f3ee-117">-Certificate</span><span class="sxs-lookup"><span data-stu-id="2f3ee-117">-Certificate</span></span>
```yaml
Type: X509Certificate2
Parameter Sets: Certificate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f3ee-118">-認證</span><span class="sxs-lookup"><span data-stu-id="2f3ee-118">-Credential</span></span>
```yaml
Type: PSCredential
Parameter Sets: ServicePrincipal, Credentials
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f3ee-119">-環境</span><span class="sxs-lookup"><span data-stu-id="2f3ee-119">-Environment</span></span>
```yaml
Type: AzureEnvironment
Parameter Sets: Certificate, ServicePrincipal, Token, Credentials, Empty
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f3ee-120">-Path</span><span class="sxs-lookup"><span data-stu-id="2f3ee-120">-Path</span></span>
```yaml
Type: String
Parameter Sets: File
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f3ee-121">-屬性</span><span class="sxs-lookup"><span data-stu-id="2f3ee-121">-Properties</span></span>
```yaml
Type: Hashtable
Parameter Sets: PropertyBag
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f3ee-122">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2f3ee-122">-ServicePrincipal</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f3ee-123">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="2f3ee-123">-StorageAccount</span></span>
```yaml
Type: String
Parameter Sets: Certificate, ServicePrincipal, Token, Credentials
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f3ee-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2f3ee-124">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: Certificate, ServicePrincipal, Token, Credentials
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f3ee-125">-租使用者</span><span class="sxs-lookup"><span data-stu-id="2f3ee-125">-Tenant</span></span>
```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Credentials
Aliases: TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f3ee-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f3ee-126">CommonParameters</span></span>
<span data-ttu-id="2f3ee-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2f3ee-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f3ee-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2f3ee-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f3ee-129">輸入</span><span class="sxs-lookup"><span data-stu-id="2f3ee-129">INPUTS</span></span>

## <span data-ttu-id="2f3ee-130">輸出</span><span class="sxs-lookup"><span data-stu-id="2f3ee-130">OUTPUTS</span></span>

## <span data-ttu-id="2f3ee-131">筆記</span><span class="sxs-lookup"><span data-stu-id="2f3ee-131">NOTES</span></span>

## <span data-ttu-id="2f3ee-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f3ee-132">RELATED LINKS</span></span>

