---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
ms.openlocfilehash: dff5f565e27f89360465ede3eb8fbe2c3d5620a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447699"
---
# <span data-ttu-id="2f327-101">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="2f327-101">Get-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="2f327-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2f327-102">SYNOPSIS</span></span>
<span data-ttu-id="2f327-103">取得 Redis 快取的地域複製連結。</span><span class="sxs-lookup"><span data-stu-id="2f327-103">Get geo replication link for Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f327-104">句法</span><span class="sxs-lookup"><span data-stu-id="2f327-104">SYNTAX</span></span>

### <span data-ttu-id="2f327-105">AllLinksForCache (預設) </span><span class="sxs-lookup"><span data-stu-id="2f327-105">AllLinksForCache (Default)</span></span>
```
Get-AzureRmRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f327-106">AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="2f327-106">AllLinksForPrimaryCache</span></span>
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f327-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="2f327-107">SingleLink</span></span>
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f327-108">AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="2f327-108">AllLinksForSecondaryCache</span></span>
```
Get-AzureRmRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2f327-109">說明</span><span class="sxs-lookup"><span data-stu-id="2f327-109">DESCRIPTION</span></span>
<span data-ttu-id="2f327-110">有四種不同的方式可以取得異地複製連結的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2f327-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="2f327-111">請提供參數名稱或 PrimaryServerName 和/或 SecondaryServerName。</span><span class="sxs-lookup"><span data-stu-id="2f327-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="2f327-112">系統會為您提供名稱，則會傳回快取存在的所有連結。</span><span class="sxs-lookup"><span data-stu-id="2f327-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="2f327-113">如果只提供 PrimaryServerName，則會傳回快取的所有連結。</span><span class="sxs-lookup"><span data-stu-id="2f327-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="2f327-114">如果只提供 SecondaryServerName，則會傳回快取的所有連結。</span><span class="sxs-lookup"><span data-stu-id="2f327-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="2f327-115">如果 PrimaryServerName 和 SecondaryServerName 都提供，則會傳回具有正確角色的特定連結。</span><span class="sxs-lookup"><span data-stu-id="2f327-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="2f327-116">示例</span><span class="sxs-lookup"><span data-stu-id="2f327-116">EXAMPLES</span></span>

### <span data-ttu-id="2f327-117">範例1：使用參數集 AllLinksForCache</span><span class="sxs-lookup"><span data-stu-id="2f327-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="2f327-118">這個命令會取得名為 mycache1 之 Redis 快取的所有地域複製連結。</span><span class="sxs-lookup"><span data-stu-id="2f327-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="2f327-119">範例2：使用參數集 AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="2f327-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="2f327-120">這個命令會取得名為 mycache1 的 Redis 快取主要的異地複製連結。</span><span class="sxs-lookup"><span data-stu-id="2f327-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="2f327-121">範例3：取得使用參數集 AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="2f327-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="2f327-122">這個命令會取得名為 mycache2 的 Redis 快取的異地複製連結。</span><span class="sxs-lookup"><span data-stu-id="2f327-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="2f327-123">範例4：取得使用參數集 SingleLink</span><span class="sxs-lookup"><span data-stu-id="2f327-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="2f327-124">這個命令會取得單一地域複製連結，其中名為 mycache1 的 Redis 快取是主要，而名為 mycache2 的 Redis 快取是次要的。</span><span class="sxs-lookup"><span data-stu-id="2f327-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="2f327-125">參數</span><span class="sxs-lookup"><span data-stu-id="2f327-125">PARAMETERS</span></span>

### <span data-ttu-id="2f327-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f327-126">-DefaultProfile</span></span>
<span data-ttu-id="2f327-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f327-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f327-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="2f327-128">-Name</span></span>
<span data-ttu-id="2f327-129">Redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f327-129">Name of redis cache.</span></span>

```yaml
Type: String
Parameter Sets: AllLinksForCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f327-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="2f327-130">-PrimaryServerName</span></span>
<span data-ttu-id="2f327-131">連結中主要 redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f327-131">Name of primary redis cache in link.</span></span>

```yaml
Type: String
Parameter Sets: AllLinksForPrimaryCache, SingleLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f327-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="2f327-132">-SecondaryServerName</span></span>
<span data-ttu-id="2f327-133">連結中次要 redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f327-133">Name of secondary redis cache in link.</span></span>

```yaml
Type: String
Parameter Sets: SingleLink, AllLinksForSecondaryCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f327-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f327-134">CommonParameters</span></span>
<span data-ttu-id="2f327-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2f327-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f327-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2f327-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f327-137">輸入</span><span class="sxs-lookup"><span data-stu-id="2f327-137">INPUTS</span></span>

### <span data-ttu-id="2f327-138">System.object</span><span class="sxs-lookup"><span data-stu-id="2f327-138">System.String</span></span>
<span data-ttu-id="2f327-139">您可以依名稱將輸入管到這個 Cmdlet，但不能依值進行。</span><span class="sxs-lookup"><span data-stu-id="2f327-139">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="2f327-140">輸出</span><span class="sxs-lookup"><span data-stu-id="2f327-140">OUTPUTS</span></span>

### <span data-ttu-id="2f327-141">[System.object]。清單 ' 1 [RedisCache. PSRedisLinkedServer，RedisCache，版本 = 4.0.1.0，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="2f327-141">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer, Microsoft.Azure.Commands.RedisCache, Version=4.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2f327-142">筆記</span><span class="sxs-lookup"><span data-stu-id="2f327-142">NOTES</span></span>

## <span data-ttu-id="2f327-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f327-143">RELATED LINKS</span></span>

[<span data-ttu-id="2f327-144">新-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="2f327-144">New-AzureRmRedisCacheLink</span></span>](./New-AzureRmRedisCacheLink.md)

[<span data-ttu-id="2f327-145">移除-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="2f327-145">Remove-AzureRmRedisCacheLink</span></span>](./Remove-AzureRmRedisCacheLink.md)

[<span data-ttu-id="2f327-146">AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2f327-146">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="2f327-147">新-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2f327-147">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="2f327-148">移除-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2f327-148">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="2f327-149">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2f327-149">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
