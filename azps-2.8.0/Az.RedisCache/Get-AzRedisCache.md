---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
ms.openlocfilehash: 1e7f57ce251c6f95a74b2ca0a55aa1caa92349a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792301"
---
# <span data-ttu-id="2af69-101">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2af69-101">Get-AzRedisCache</span></span>

## <span data-ttu-id="2af69-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2af69-102">SYNOPSIS</span></span>
<span data-ttu-id="2af69-103">取得 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="2af69-103">Gets a Redis Cache.</span></span>

## <span data-ttu-id="2af69-104">句法</span><span class="sxs-lookup"><span data-stu-id="2af69-104">SYNTAX</span></span>

```
Get-AzRedisCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2af69-105">說明</span><span class="sxs-lookup"><span data-stu-id="2af69-105">DESCRIPTION</span></span>
<span data-ttu-id="2af69-106">AzRedisCache Cmdlet 會取得指定的 Azure Redis 快 **取** 。</span><span class="sxs-lookup"><span data-stu-id="2af69-106">The **Get-AzRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="2af69-107">如果您沒有指定參數，此操作會取得目前訂閱的每個 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="2af69-107">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="2af69-108">示例</span><span class="sxs-lookup"><span data-stu-id="2af69-108">EXAMPLES</span></span>

### <span data-ttu-id="2af69-109">範例1：依名稱取得 Redis 快取</span><span class="sxs-lookup"><span data-stu-id="2af69-109">Example 1: Get a Redis Cache by name</span></span>
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

<span data-ttu-id="2af69-110">這個命令會取得名為 myexists 的 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="2af69-110">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="2af69-111">範例2：取得資源群組中的每個 Redis 快取</span><span class="sxs-lookup"><span data-stu-id="2af69-111">Example 2: Get every Redis Cache in a resource group</span></span>
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

<span data-ttu-id="2af69-112">這個命令會取得指定資源群組中的每個 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="2af69-112">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="2af69-113">範例3：在目前的訂閱中取得每個 Redis 快取</span><span class="sxs-lookup"><span data-stu-id="2af69-113">Example 3: Get every Redis Cache in the current subscription</span></span>
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

<span data-ttu-id="2af69-114">這個命令會在目前的訂閱中取得每個 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="2af69-114">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="2af69-115">參數</span><span class="sxs-lookup"><span data-stu-id="2af69-115">PARAMETERS</span></span>

### <span data-ttu-id="2af69-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2af69-116">-DefaultProfile</span></span>
<span data-ttu-id="2af69-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2af69-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2af69-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="2af69-118">-Name</span></span>
<span data-ttu-id="2af69-119">指定要取得之 Redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="2af69-119">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="2af69-120">與 *ResourceGroupName* 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="2af69-120">Use with the *ResourceGroupName* parameter.</span></span>

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

### <span data-ttu-id="2af69-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2af69-121">-ResourceGroupName</span></span>
<span data-ttu-id="2af69-122">指定包含要取得之 Redis 快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2af69-122">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>
<span data-ttu-id="2af69-123">如果您只指定 *ResourceGroupName* 參數，此操作會取得指定資源群組中的每個 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="2af69-123">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

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

### <span data-ttu-id="2af69-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2af69-124">CommonParameters</span></span>
<span data-ttu-id="2af69-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2af69-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2af69-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2af69-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2af69-127">輸入</span><span class="sxs-lookup"><span data-stu-id="2af69-127">INPUTS</span></span>

### <span data-ttu-id="2af69-128">System.object</span><span class="sxs-lookup"><span data-stu-id="2af69-128">System.String</span></span>

## <span data-ttu-id="2af69-129">輸出</span><span class="sxs-lookup"><span data-stu-id="2af69-129">OUTPUTS</span></span>

### <span data-ttu-id="2af69-130">RedisCacheAttributes 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="2af69-130">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="2af69-131">筆記</span><span class="sxs-lookup"><span data-stu-id="2af69-131">NOTES</span></span>

## <span data-ttu-id="2af69-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="2af69-132">RELATED LINKS</span></span>

[<span data-ttu-id="2af69-133">新-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2af69-133">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="2af69-134">移除-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2af69-134">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="2af69-135">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2af69-135">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


