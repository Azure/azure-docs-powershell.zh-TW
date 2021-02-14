---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.ADDomainServices/new-AzADDomainServiceForestTrust
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceForestTrust.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceForestTrust.md
ms.openlocfilehash: 91d7b92b7b52df20d69f53cddb98d6b9276b0b59
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127314"
---
# <span data-ttu-id="6207e-101">New-AzADDomainServiceForestTrust</span><span class="sxs-lookup"><span data-stu-id="6207e-101">New-AzADDomainServiceForestTrust</span></span>

## <span data-ttu-id="6207e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6207e-102">SYNOPSIS</span></span>
<span data-ttu-id="6207e-103">為 ForestTrust 建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="6207e-103">Create a in-memory object for ForestTrust</span></span>

## <span data-ttu-id="6207e-104">句法</span><span class="sxs-lookup"><span data-stu-id="6207e-104">SYNTAX</span></span>

```
New-AzADDomainServiceForestTrust [-FriendlyName <String>] [-RemoteDnsIP <String>] [-TrustDirection <String>]
 [-TrustedDomainFqdn <String>] [-TrustPassword <SecureString>] [<CommonParameters>]
```

## <span data-ttu-id="6207e-105">說明</span><span class="sxs-lookup"><span data-stu-id="6207e-105">DESCRIPTION</span></span>
<span data-ttu-id="6207e-106">為 ForestTrust 建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="6207e-106">Create a in-memory object for ForestTrust</span></span>

## <span data-ttu-id="6207e-107">示例</span><span class="sxs-lookup"><span data-stu-id="6207e-107">EXAMPLES</span></span>

### <span data-ttu-id="6207e-108">範例1：建立 ADDomain 的 ServiceForestTrust</span><span class="sxs-lookup"><span data-stu-id="6207e-108">Example 1: Create ServiceForestTrust for ADDomain</span></span>
```powershell
PS C:\> New-AzADDomainServiceForestTrust -FriendlyName FriendlyNameTest

FriendlyName     RemoteDnsIP TrustDirection TrustPassword TrustedDomainFqdn
------------     ----------- -------------- ------------- -----------------
FriendlyNameTest
```

<span data-ttu-id="6207e-109">建立 ADDomain 的 ServiceForestTrust</span><span class="sxs-lookup"><span data-stu-id="6207e-109">Create ServiceForestTrust for ADDomain</span></span>

## <span data-ttu-id="6207e-110">參數</span><span class="sxs-lookup"><span data-stu-id="6207e-110">PARAMETERS</span></span>

### <span data-ttu-id="6207e-111">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="6207e-111">-FriendlyName</span></span>
<span data-ttu-id="6207e-112">易記的名稱。</span><span class="sxs-lookup"><span data-stu-id="6207e-112">Friendly Name.</span></span>

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

### <span data-ttu-id="6207e-113">-RemoteDnsIP</span><span class="sxs-lookup"><span data-stu-id="6207e-113">-RemoteDnsIP</span></span>
<span data-ttu-id="6207e-114">遠端 Dns ip。</span><span class="sxs-lookup"><span data-stu-id="6207e-114">Remote Dns ips.</span></span>

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

### <span data-ttu-id="6207e-115">-TrustDirection</span><span class="sxs-lookup"><span data-stu-id="6207e-115">-TrustDirection</span></span>
<span data-ttu-id="6207e-116">信任方向。</span><span class="sxs-lookup"><span data-stu-id="6207e-116">Trust Direction.</span></span>

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

### <span data-ttu-id="6207e-117">-TrustedDomainFqdn</span><span class="sxs-lookup"><span data-stu-id="6207e-117">-TrustedDomainFqdn</span></span>
<span data-ttu-id="6207e-118">受信任的網域 FQDN。</span><span class="sxs-lookup"><span data-stu-id="6207e-118">Trusted Domain FQDN.</span></span>

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

### <span data-ttu-id="6207e-119">-TrustPassword</span><span class="sxs-lookup"><span data-stu-id="6207e-119">-TrustPassword</span></span>
<span data-ttu-id="6207e-120">信任密碼。</span><span class="sxs-lookup"><span data-stu-id="6207e-120">Trust Password.</span></span>

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

### <span data-ttu-id="6207e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6207e-121">CommonParameters</span></span>
<span data-ttu-id="6207e-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6207e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6207e-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6207e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6207e-124">輸入</span><span class="sxs-lookup"><span data-stu-id="6207e-124">INPUTS</span></span>

## <span data-ttu-id="6207e-125">輸出</span><span class="sxs-lookup"><span data-stu-id="6207e-125">OUTPUTS</span></span>

### <span data-ttu-id="6207e-126">ForestTrust （ADDomainServices）。 Api202001。</span><span class="sxs-lookup"><span data-stu-id="6207e-126">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ForestTrust</span></span>

## <span data-ttu-id="6207e-127">筆記</span><span class="sxs-lookup"><span data-stu-id="6207e-127">NOTES</span></span>

<span data-ttu-id="6207e-128">別名</span><span class="sxs-lookup"><span data-stu-id="6207e-128">ALIASES</span></span>

## <span data-ttu-id="6207e-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="6207e-129">RELATED LINKS</span></span>

