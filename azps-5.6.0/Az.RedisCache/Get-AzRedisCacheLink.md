---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/powershell/module/az.rediscache/get-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
ms.openlocfilehash: 9b1957054c243de8776f0063e236f9e19980af54
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909494"
---
# <span data-ttu-id="545fd-101">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="545fd-101">Get-AzRedisCacheLink</span></span>

## <span data-ttu-id="545fd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="545fd-102">SYNOPSIS</span></span>
<span data-ttu-id="545fd-103">取得 Redis Cache 的地理位置複製連結。</span><span class="sxs-lookup"><span data-stu-id="545fd-103">Get geo replication link for Redis Cache.</span></span>

## <span data-ttu-id="545fd-104">語法</span><span class="sxs-lookup"><span data-stu-id="545fd-104">SYNTAX</span></span>

### <span data-ttu-id="545fd-105">AllLinksForCache (預設) </span><span class="sxs-lookup"><span data-stu-id="545fd-105">AllLinksForCache (Default)</span></span>
```
Get-AzRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="545fd-106">AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="545fd-106">AllLinksForPrimaryCache</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="545fd-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="545fd-107">SingleLink</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="545fd-108">AllLinksFor舍利Cache</span><span class="sxs-lookup"><span data-stu-id="545fd-108">AllLinksForSecondaryCache</span></span>
```
Get-AzRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="545fd-109">描述</span><span class="sxs-lookup"><span data-stu-id="545fd-109">DESCRIPTION</span></span>
<span data-ttu-id="545fd-110">有四種不同的方法可以取得異地複製連結的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="545fd-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="545fd-111">提供參數名稱或 PrimaryServerName 和/或 SecondaryServerName。</span><span class="sxs-lookup"><span data-stu-id="545fd-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="545fd-112">系統隨即會提供名稱，然後會返回所有有緩存存在的連結。</span><span class="sxs-lookup"><span data-stu-id="545fd-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="545fd-113">如果只提供 PrimaryServerName，則所有以緩存為主要的連結都會被退回。</span><span class="sxs-lookup"><span data-stu-id="545fd-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="545fd-114">如果只提供次要ServerName，則所有位於次要緩存的連結都會被退回。</span><span class="sxs-lookup"><span data-stu-id="545fd-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="545fd-115">如果同時提供 PrimaryServerName 和 SecondaryServerName，則會返回具有正確角色的特定連結。</span><span class="sxs-lookup"><span data-stu-id="545fd-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="545fd-116">例子</span><span class="sxs-lookup"><span data-stu-id="545fd-116">EXAMPLES</span></span>

### <span data-ttu-id="545fd-117">範例 1：使用參數集 AllLinksForCache</span><span class="sxs-lookup"><span data-stu-id="545fd-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="545fd-118">此命令會針對名為 mycache1 的 Redis Cache 獲得所有地理位置複製連結。</span><span class="sxs-lookup"><span data-stu-id="545fd-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="545fd-119">範例 2：使用參數集 AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="545fd-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="545fd-120">此命令會獲得名為 mycache1 的 Redis Cache 為主要位置複製連結。</span><span class="sxs-lookup"><span data-stu-id="545fd-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="545fd-121">範例 3：Get using parameter set AllLinksFor舍aryCache</span><span class="sxs-lookup"><span data-stu-id="545fd-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="545fd-122">此命令會獲得名為 mycache2 的 Redis Cache 次要位置複製連結。</span><span class="sxs-lookup"><span data-stu-id="545fd-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="545fd-123">範例 4：使用參數集 SingleLink</span><span class="sxs-lookup"><span data-stu-id="545fd-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="545fd-124">此命令會獲得單一地理位置複製連結，其中名稱為 mycache1 的 Redis Cache 為主要，而 Redis Cache 名稱為 mycache2 為次要。</span><span class="sxs-lookup"><span data-stu-id="545fd-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="545fd-125">參數</span><span class="sxs-lookup"><span data-stu-id="545fd-125">PARAMETERS</span></span>

### <span data-ttu-id="545fd-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="545fd-126">-DefaultProfile</span></span>
<span data-ttu-id="545fd-127">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="545fd-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="545fd-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="545fd-128">-Name</span></span>
<span data-ttu-id="545fd-129">重新具名快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="545fd-129">Name of redis cache.</span></span>

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

### <span data-ttu-id="545fd-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="545fd-130">-PrimaryServerName</span></span>
<span data-ttu-id="545fd-131">連結中主要重新顯示緩存的名稱。</span><span class="sxs-lookup"><span data-stu-id="545fd-131">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="545fd-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="545fd-132">-SecondaryServerName</span></span>
<span data-ttu-id="545fd-133">連結中次要重新顯示緩存的名稱。</span><span class="sxs-lookup"><span data-stu-id="545fd-133">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="545fd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="545fd-134">CommonParameters</span></span>
<span data-ttu-id="545fd-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="545fd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="545fd-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="545fd-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="545fd-137">輸入</span><span class="sxs-lookup"><span data-stu-id="545fd-137">INPUTS</span></span>

### <span data-ttu-id="545fd-138">System.String</span><span class="sxs-lookup"><span data-stu-id="545fd-138">System.String</span></span>

## <span data-ttu-id="545fd-139">輸出</span><span class="sxs-lookup"><span data-stu-id="545fd-139">OUTPUTS</span></span>

### <span data-ttu-id="545fd-140">Microsoft.Azure.Commands.RedisCache.models.PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="545fd-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="545fd-141">筆記</span><span class="sxs-lookup"><span data-stu-id="545fd-141">NOTES</span></span>

## <span data-ttu-id="545fd-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="545fd-142">RELATED LINKS</span></span>

[<span data-ttu-id="545fd-143">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="545fd-143">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="545fd-144">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="545fd-144">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="545fd-145">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="545fd-145">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="545fd-146">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="545fd-146">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="545fd-147">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="545fd-147">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="545fd-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="545fd-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)