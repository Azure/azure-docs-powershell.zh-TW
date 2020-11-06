---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
ms.openlocfilehash: a45407fc7f25e2c7bee5c591ab3110b0620a2c0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448949"
---
# <span data-ttu-id="a36c5-101">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="a36c5-101">Get-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="a36c5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a36c5-102">SYNOPSIS</span></span>
<span data-ttu-id="a36c5-103">取得 Redis 快取的地域複製連結。</span><span class="sxs-lookup"><span data-stu-id="a36c5-103">Get geo replication link for Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a36c5-104">句法</span><span class="sxs-lookup"><span data-stu-id="a36c5-104">SYNTAX</span></span>

### <span data-ttu-id="a36c5-105">AllLinksForCache (預設) </span><span class="sxs-lookup"><span data-stu-id="a36c5-105">AllLinksForCache (Default)</span></span>
```
Get-AzureRmRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a36c5-106">AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="a36c5-106">AllLinksForPrimaryCache</span></span>
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a36c5-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="a36c5-107">SingleLink</span></span>
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a36c5-108">AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="a36c5-108">AllLinksForSecondaryCache</span></span>
```
Get-AzureRmRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a36c5-109">說明</span><span class="sxs-lookup"><span data-stu-id="a36c5-109">DESCRIPTION</span></span>
<span data-ttu-id="a36c5-110">有四種不同的方式可以取得異地複製連結的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a36c5-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="a36c5-111">請提供參數名稱或 PrimaryServerName 和/或 SecondaryServerName。</span><span class="sxs-lookup"><span data-stu-id="a36c5-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="a36c5-112">系統會為您提供名稱，則會傳回快取存在的所有連結。</span><span class="sxs-lookup"><span data-stu-id="a36c5-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="a36c5-113">如果只提供 PrimaryServerName，則會傳回快取的所有連結。</span><span class="sxs-lookup"><span data-stu-id="a36c5-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="a36c5-114">如果只提供 SecondaryServerName，則會傳回快取的所有連結。</span><span class="sxs-lookup"><span data-stu-id="a36c5-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="a36c5-115">如果 PrimaryServerName 和 SecondaryServerName 都提供，則會傳回具有正確角色的特定連結。</span><span class="sxs-lookup"><span data-stu-id="a36c5-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="a36c5-116">示例</span><span class="sxs-lookup"><span data-stu-id="a36c5-116">EXAMPLES</span></span>

### <span data-ttu-id="a36c5-117">範例1：使用參數集 AllLinksForCache</span><span class="sxs-lookup"><span data-stu-id="a36c5-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="a36c5-118">這個命令會取得名為 mycache1 之 Redis 快取的所有地域複製連結。</span><span class="sxs-lookup"><span data-stu-id="a36c5-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="a36c5-119">範例2：使用參數集 AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="a36c5-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="a36c5-120">這個命令會取得名為 mycache1 的 Redis 快取主要的異地複製連結。</span><span class="sxs-lookup"><span data-stu-id="a36c5-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="a36c5-121">範例3：取得使用參數集 AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="a36c5-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="a36c5-122">這個命令會取得名為 mycache2 的 Redis 快取的異地複製連結。</span><span class="sxs-lookup"><span data-stu-id="a36c5-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="a36c5-123">範例4：取得使用參數集 SingleLink</span><span class="sxs-lookup"><span data-stu-id="a36c5-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="a36c5-124">這個命令會取得單一地域複製連結，其中名為 mycache1 的 Redis 快取是主要，而名為 mycache2 的 Redis 快取是次要的。</span><span class="sxs-lookup"><span data-stu-id="a36c5-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="a36c5-125">參數</span><span class="sxs-lookup"><span data-stu-id="a36c5-125">PARAMETERS</span></span>

### <span data-ttu-id="a36c5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a36c5-126">-DefaultProfile</span></span>
<span data-ttu-id="a36c5-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a36c5-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a36c5-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="a36c5-128">-Name</span></span>
<span data-ttu-id="a36c5-129">Redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="a36c5-129">Name of redis cache.</span></span>

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

### <span data-ttu-id="a36c5-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="a36c5-130">-PrimaryServerName</span></span>
<span data-ttu-id="a36c5-131">連結中主要 redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="a36c5-131">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="a36c5-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="a36c5-132">-SecondaryServerName</span></span>
<span data-ttu-id="a36c5-133">連結中次要 redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="a36c5-133">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="a36c5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a36c5-134">CommonParameters</span></span>
<span data-ttu-id="a36c5-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a36c5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a36c5-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a36c5-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a36c5-137">輸入</span><span class="sxs-lookup"><span data-stu-id="a36c5-137">INPUTS</span></span>

### <span data-ttu-id="a36c5-138">System.object</span><span class="sxs-lookup"><span data-stu-id="a36c5-138">System.String</span></span>

## <span data-ttu-id="a36c5-139">輸出</span><span class="sxs-lookup"><span data-stu-id="a36c5-139">OUTPUTS</span></span>

### <span data-ttu-id="a36c5-140">PSRedisLinkedServer 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="a36c5-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="a36c5-141">筆記</span><span class="sxs-lookup"><span data-stu-id="a36c5-141">NOTES</span></span>

## <span data-ttu-id="a36c5-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="a36c5-142">RELATED LINKS</span></span>

[<span data-ttu-id="a36c5-143">新-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="a36c5-143">New-AzureRmRedisCacheLink</span></span>](./New-AzureRmRedisCacheLink.md)

[<span data-ttu-id="a36c5-144">移除-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="a36c5-144">Remove-AzureRmRedisCacheLink</span></span>](./Remove-AzureRmRedisCacheLink.md)

[<span data-ttu-id="a36c5-145">AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a36c5-145">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="a36c5-146">新-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a36c5-146">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="a36c5-147">移除-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a36c5-147">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="a36c5-148">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a36c5-148">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
