---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.ADDomainServices/new-AzADDomainServiceForestTrust
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceForestTrust.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceForestTrust.md
ms.openlocfilehash: aaf3fa74000bd5ab7264386b28fe20588235c951
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910570"
---
# <span data-ttu-id="4c9f3-101">New-AzADDomainServiceForestTrust</span><span class="sxs-lookup"><span data-stu-id="4c9f3-101">New-AzADDomainServiceForestTrust</span></span>

## <span data-ttu-id="4c9f3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4c9f3-102">SYNOPSIS</span></span>
<span data-ttu-id="4c9f3-103">為 ForestTrust 建立記憶體中的物件</span><span class="sxs-lookup"><span data-stu-id="4c9f3-103">Create a in-memory object for ForestTrust</span></span>

## <span data-ttu-id="4c9f3-104">語法</span><span class="sxs-lookup"><span data-stu-id="4c9f3-104">SYNTAX</span></span>

```
New-AzADDomainServiceForestTrust [-FriendlyName <String>] [-RemoteDnsIP <String>] [-TrustDirection <String>]
 [-TrustedDomainFqdn <String>] [-TrustPassword <SecureString>] [<CommonParameters>]
```

## <span data-ttu-id="4c9f3-105">描述</span><span class="sxs-lookup"><span data-stu-id="4c9f3-105">DESCRIPTION</span></span>
<span data-ttu-id="4c9f3-106">為 ForestTrust 建立記憶體中的物件</span><span class="sxs-lookup"><span data-stu-id="4c9f3-106">Create a in-memory object for ForestTrust</span></span>

## <span data-ttu-id="4c9f3-107">例子</span><span class="sxs-lookup"><span data-stu-id="4c9f3-107">EXAMPLES</span></span>

### <span data-ttu-id="4c9f3-108">範例 1：建立 ADDomain 的 ServiceForestTrust</span><span class="sxs-lookup"><span data-stu-id="4c9f3-108">Example 1: Create ServiceForestTrust for ADDomain</span></span>
```powershell
PS C:\> New-AzADDomainServiceForestTrust -FriendlyName FriendlyNameTest

FriendlyName     RemoteDnsIP TrustDirection TrustPassword TrustedDomainFqdn
------------     ----------- -------------- ------------- -----------------
FriendlyNameTest
```

<span data-ttu-id="4c9f3-109">建立 ServiceForestTrust for ADDomain</span><span class="sxs-lookup"><span data-stu-id="4c9f3-109">Create ServiceForestTrust for ADDomain</span></span>

## <span data-ttu-id="4c9f3-110">參數</span><span class="sxs-lookup"><span data-stu-id="4c9f3-110">PARAMETERS</span></span>

### <span data-ttu-id="4c9f3-111">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4c9f3-111">-FriendlyName</span></span>
<span data-ttu-id="4c9f3-112">好用名稱。</span><span class="sxs-lookup"><span data-stu-id="4c9f3-112">Friendly Name.</span></span>

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

### <span data-ttu-id="4c9f3-113">-RemoteDnsIP</span><span class="sxs-lookup"><span data-stu-id="4c9f3-113">-RemoteDnsIP</span></span>
<span data-ttu-id="4c9f3-114">遠端 Dns ips。</span><span class="sxs-lookup"><span data-stu-id="4c9f3-114">Remote Dns ips.</span></span>

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

### <span data-ttu-id="4c9f3-115">-TrustDirection</span><span class="sxs-lookup"><span data-stu-id="4c9f3-115">-TrustDirection</span></span>
<span data-ttu-id="4c9f3-116">信任方向。</span><span class="sxs-lookup"><span data-stu-id="4c9f3-116">Trust Direction.</span></span>

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

### <span data-ttu-id="4c9f3-117">-TrustedDomainFqdn</span><span class="sxs-lookup"><span data-stu-id="4c9f3-117">-TrustedDomainFqdn</span></span>
<span data-ttu-id="4c9f3-118">信任的網域 FQDN。</span><span class="sxs-lookup"><span data-stu-id="4c9f3-118">Trusted Domain FQDN.</span></span>

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

### <span data-ttu-id="4c9f3-119">-TrustPassword</span><span class="sxs-lookup"><span data-stu-id="4c9f3-119">-TrustPassword</span></span>
<span data-ttu-id="4c9f3-120">信任密碼。</span><span class="sxs-lookup"><span data-stu-id="4c9f3-120">Trust Password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c9f3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c9f3-121">CommonParameters</span></span>
<span data-ttu-id="4c9f3-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4c9f3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c9f3-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c9f3-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c9f3-124">輸入</span><span class="sxs-lookup"><span data-stu-id="4c9f3-124">INPUTS</span></span>

## <span data-ttu-id="4c9f3-125">輸出</span><span class="sxs-lookup"><span data-stu-id="4c9f3-125">OUTPUTS</span></span>

### <span data-ttu-id="4c9f3-126">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.models.Api202001.ForestTrust</span><span class="sxs-lookup"><span data-stu-id="4c9f3-126">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ForestTrust</span></span>

## <span data-ttu-id="4c9f3-127">筆記</span><span class="sxs-lookup"><span data-stu-id="4c9f3-127">NOTES</span></span>

<span data-ttu-id="4c9f3-128">別名</span><span class="sxs-lookup"><span data-stu-id="4c9f3-128">ALIASES</span></span>

## <span data-ttu-id="4c9f3-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="4c9f3-129">RELATED LINKS</span></span>

