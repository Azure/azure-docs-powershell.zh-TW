---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: https://docs.microsoft.com/powershell/module/az.rediscache/get-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
ms.openlocfilehash: 8423c098542a621ec66a5de3255ccf62c3e8ec94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901669"
---
# <span data-ttu-id="ec2b5-101">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ec2b5-101">Get-AzRedisCache</span></span>

## <span data-ttu-id="ec2b5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ec2b5-102">SYNOPSIS</span></span>
<span data-ttu-id="ec2b5-103">獲得 Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="ec2b5-103">Gets a Redis Cache.</span></span>

## <span data-ttu-id="ec2b5-104">語法</span><span class="sxs-lookup"><span data-stu-id="ec2b5-104">SYNTAX</span></span>

```
Get-AzRedisCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec2b5-105">描述</span><span class="sxs-lookup"><span data-stu-id="ec2b5-105">DESCRIPTION</span></span>
<span data-ttu-id="ec2b5-106">**Get-AzRedisCache** Cmdlet 會取得指定的 Azure Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="ec2b5-106">The **Get-AzRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="ec2b5-107">如果您未指定參數，此作業會針對目前的訂閱獲得每個 Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="ec2b5-107">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="ec2b5-108">例子</span><span class="sxs-lookup"><span data-stu-id="ec2b5-108">EXAMPLES</span></span>

### <span data-ttu-id="ec2b5-109">範例 1：取得 Redis Cache by name</span><span class="sxs-lookup"><span data-stu-id="ec2b5-109">Example 1: Get a Redis Cache by name</span></span>
```
PS C:\>Get-AzRedisCache -Name "myexists"

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
        Location           : North Central US
        Name               : myexists
        Type               : Microsoft.Cache/Redis
        HostName           : myexists.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 1GB
        Sku                : Basic
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="ec2b5-110">此命令會獲得名為 myexists 的 Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="ec2b5-110">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="ec2b5-111">範例 2：在資源群組中取得每個 Redis Cache</span><span class="sxs-lookup"><span data-stu-id="ec2b5-111">Example 2: Get every Redis Cache in a resource group</span></span>
```
PS C:\>Get-AzRedisCache -ResourceGroupName "myGroup"

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
        Location           : North Central US
        Name               : myexists
        Type               : Microsoft.Cache/Redis
        HostName           : myexists.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 1GB
        Sku                : Basic
        Tag                : {}
        Zone               : []

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myearlier
        Location           : North Central US
        Name               : myearlier
        Type               : Microsoft.Cache/Redis
        HostName           : myearlier.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : True
        RedisVersion       : 2.8
        Size               : 250MB
        Sku                : Standard
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="ec2b5-112">此命令會獲得指定資源群組中每個 Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="ec2b5-112">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="ec2b5-113">範例 3：取得目前訂閱中每個 Redis Cache</span><span class="sxs-lookup"><span data-stu-id="ec2b5-113">Example 3: Get every Redis Cache in the current subscription</span></span>
```
PS C:\>Get-AzRedisCache

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
        Location           : North Central US
        Name               : myexists
        Type               : Microsoft.Cache/Redis
        HostName           : myexists.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 1GB
        Sku                : Basic
        Tag                : {}
        Zone               : []

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myearlier
        Location           : North Central US
        Name               : myearlier
        Type               : Microsoft.Cache/Redis
        HostName           : myearlier.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : True
        RedisVersion       : 2.8
        Size               : 250MB
        Sku                : Standard
        Tag                : {}
        Zone               : []

        ResourceGroupName  : myGroup2
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup2/providers/Microsoft.Cache/Redis/myearlier2
        Location           : North Central US
        Name               : myearlier2
        Type               : Microsoft.Cache/Redis
        HostName           : myearlier2.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 250MB
        Sku                : Basic
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="ec2b5-114">此命令會獲得目前訂閱中每個 Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="ec2b5-114">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="ec2b5-115">參數</span><span class="sxs-lookup"><span data-stu-id="ec2b5-115">PARAMETERS</span></span>

### <span data-ttu-id="ec2b5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec2b5-116">-DefaultProfile</span></span>
<span data-ttu-id="ec2b5-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ec2b5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec2b5-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="ec2b5-118">-Name</span></span>
<span data-ttu-id="ec2b5-119">指定要取得 Redis Cache 的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec2b5-119">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="ec2b5-120">使用 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="ec2b5-120">Use with the *ResourceGroupName* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec2b5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec2b5-121">-ResourceGroupName</span></span>
<span data-ttu-id="ec2b5-122">指定要取得包含 Redis Cache 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="ec2b5-122">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>
<span data-ttu-id="ec2b5-123">如果您只指定 *ResourceGroupName* 參數，此作業會獲得指定資源群組中每個 Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="ec2b5-123">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec2b5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec2b5-124">CommonParameters</span></span>
<span data-ttu-id="ec2b5-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ec2b5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec2b5-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ec2b5-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec2b5-127">輸入</span><span class="sxs-lookup"><span data-stu-id="ec2b5-127">INPUTS</span></span>

### <span data-ttu-id="ec2b5-128">System.String</span><span class="sxs-lookup"><span data-stu-id="ec2b5-128">System.String</span></span>

## <span data-ttu-id="ec2b5-129">輸出</span><span class="sxs-lookup"><span data-stu-id="ec2b5-129">OUTPUTS</span></span>

### <span data-ttu-id="ec2b5-130">Microsoft.Azure.Commands.RedisCache.models.RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="ec2b5-130">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="ec2b5-131">筆記</span><span class="sxs-lookup"><span data-stu-id="ec2b5-131">NOTES</span></span>

## <span data-ttu-id="ec2b5-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec2b5-132">RELATED LINKS</span></span>

[<span data-ttu-id="ec2b5-133">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ec2b5-133">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="ec2b5-134">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ec2b5-134">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="ec2b5-135">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ec2b5-135">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


