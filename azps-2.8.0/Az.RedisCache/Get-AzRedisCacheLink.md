---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
ms.openlocfilehash: 8129634e940624fe09dad4a1199f96dbcf5162bb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791823"
---
# <span data-ttu-id="7f64d-101">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="7f64d-101">Get-AzRedisCacheLink</span></span>

## <span data-ttu-id="7f64d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7f64d-102">SYNOPSIS</span></span>
<span data-ttu-id="7f64d-103">取得 Redis 快取的地域複製連結。</span><span class="sxs-lookup"><span data-stu-id="7f64d-103">Get geo replication link for Redis Cache.</span></span>

## <span data-ttu-id="7f64d-104">句法</span><span class="sxs-lookup"><span data-stu-id="7f64d-104">SYNTAX</span></span>

### <span data-ttu-id="7f64d-105">AllLinksForCache (預設) </span><span class="sxs-lookup"><span data-stu-id="7f64d-105">AllLinksForCache (Default)</span></span>
```
Get-AzRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f64d-106">AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="7f64d-106">AllLinksForPrimaryCache</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f64d-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="7f64d-107">SingleLink</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f64d-108">AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="7f64d-108">AllLinksForSecondaryCache</span></span>
```
Get-AzRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f64d-109">說明</span><span class="sxs-lookup"><span data-stu-id="7f64d-109">DESCRIPTION</span></span>
<span data-ttu-id="7f64d-110">有四種不同的方式可以取得異地複製連結的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7f64d-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="7f64d-111">請提供參數名稱或 PrimaryServerName 和/或 SecondaryServerName。</span><span class="sxs-lookup"><span data-stu-id="7f64d-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="7f64d-112">系統會為您提供名稱，則會傳回快取存在的所有連結。</span><span class="sxs-lookup"><span data-stu-id="7f64d-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="7f64d-113">如果只提供 PrimaryServerName，則會傳回快取的所有連結。</span><span class="sxs-lookup"><span data-stu-id="7f64d-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="7f64d-114">如果只提供 SecondaryServerName，則會傳回快取的所有連結。</span><span class="sxs-lookup"><span data-stu-id="7f64d-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="7f64d-115">如果 PrimaryServerName 和 SecondaryServerName 都提供，則會傳回具有正確角色的特定連結。</span><span class="sxs-lookup"><span data-stu-id="7f64d-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="7f64d-116">示例</span><span class="sxs-lookup"><span data-stu-id="7f64d-116">EXAMPLES</span></span>

### <span data-ttu-id="7f64d-117">範例1：使用參數集 AllLinksForCache</span><span class="sxs-lookup"><span data-stu-id="7f64d-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="7f64d-118">這個命令會取得名為 mycache1 之 Redis 快取的所有地域複製連結。</span><span class="sxs-lookup"><span data-stu-id="7f64d-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="7f64d-119">範例2：使用參數集 AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="7f64d-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="7f64d-120">這個命令會取得名為 mycache1 的 Redis 快取主要的異地複製連結。</span><span class="sxs-lookup"><span data-stu-id="7f64d-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="7f64d-121">範例3：取得使用參數集 AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="7f64d-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="7f64d-122">這個命令會取得名為 mycache2 的 Redis 快取的異地複製連結。</span><span class="sxs-lookup"><span data-stu-id="7f64d-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="7f64d-123">範例4：取得使用參數集 SingleLink</span><span class="sxs-lookup"><span data-stu-id="7f64d-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="7f64d-124">這個命令會取得單一地域複製連結，其中名為 mycache1 的 Redis 快取是主要，而名為 mycache2 的 Redis 快取是次要的。</span><span class="sxs-lookup"><span data-stu-id="7f64d-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="7f64d-125">參數</span><span class="sxs-lookup"><span data-stu-id="7f64d-125">PARAMETERS</span></span>

### <span data-ttu-id="7f64d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f64d-126">-DefaultProfile</span></span>
<span data-ttu-id="7f64d-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7f64d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f64d-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="7f64d-128">-Name</span></span>
<span data-ttu-id="7f64d-129">Redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f64d-129">Name of redis cache.</span></span>

```yaml
Type: System.String
Parameter Sets: AllLinksForCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f64d-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="7f64d-130">-PrimaryServerName</span></span>
<span data-ttu-id="7f64d-131">連結中主要 redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f64d-131">Name of primary redis cache in link.</span></span>

```yaml
Type: System.String
Parameter Sets: AllLinksForPrimaryCache, SingleLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f64d-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="7f64d-132">-SecondaryServerName</span></span>
<span data-ttu-id="7f64d-133">連結中次要 redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f64d-133">Name of secondary redis cache in link.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleLink, AllLinksForSecondaryCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f64d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f64d-134">CommonParameters</span></span>
<span data-ttu-id="7f64d-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7f64d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f64d-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7f64d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f64d-137">輸入</span><span class="sxs-lookup"><span data-stu-id="7f64d-137">INPUTS</span></span>

### <span data-ttu-id="7f64d-138">System.object</span><span class="sxs-lookup"><span data-stu-id="7f64d-138">System.String</span></span>

## <span data-ttu-id="7f64d-139">輸出</span><span class="sxs-lookup"><span data-stu-id="7f64d-139">OUTPUTS</span></span>

### <span data-ttu-id="7f64d-140">PSRedisLinkedServer 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="7f64d-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="7f64d-141">筆記</span><span class="sxs-lookup"><span data-stu-id="7f64d-141">NOTES</span></span>

## <span data-ttu-id="7f64d-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="7f64d-142">RELATED LINKS</span></span>

[<span data-ttu-id="7f64d-143">新-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="7f64d-143">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="7f64d-144">移除-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="7f64d-144">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="7f64d-145">AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7f64d-145">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="7f64d-146">新-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7f64d-146">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="7f64d-147">移除-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7f64d-147">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="7f64d-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7f64d-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)