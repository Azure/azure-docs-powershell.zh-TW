---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
ms.openlocfilehash: 1e91aa946e89b8231ea2c58b28c686d603855ada
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448598"
---
# <span data-ttu-id="4e2fe-101">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4e2fe-101">Get-AzureRmRedisCache</span></span>

## <span data-ttu-id="4e2fe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e2fe-102">SYNOPSIS</span></span>
<span data-ttu-id="4e2fe-103">取得 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="4e2fe-103">Gets a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e2fe-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e2fe-104">SYNTAX</span></span>

```
Get-AzureRmRedisCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e2fe-105">說明</span><span class="sxs-lookup"><span data-stu-id="4e2fe-105">DESCRIPTION</span></span>
<span data-ttu-id="4e2fe-106">AzureRmRedisCache Cmdlet 會取得指定的 Azure Redis 快 **取** 。</span><span class="sxs-lookup"><span data-stu-id="4e2fe-106">The **Get-AzureRmRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="4e2fe-107">如果您沒有指定參數，此操作會取得目前訂閱的每個 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="4e2fe-107">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="4e2fe-108">示例</span><span class="sxs-lookup"><span data-stu-id="4e2fe-108">EXAMPLES</span></span>

### <span data-ttu-id="4e2fe-109">範例1：依名稱取得 Redis 快取</span><span class="sxs-lookup"><span data-stu-id="4e2fe-109">Example 1: Get a Redis Cache by name</span></span>
```
PS C:\>Get-AzureRmRedisCache -Name "myexists"

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

<span data-ttu-id="4e2fe-110">這個命令會取得名為 myexists 的 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="4e2fe-110">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="4e2fe-111">範例2：取得資源群組中的每個 Redis 快取</span><span class="sxs-lookup"><span data-stu-id="4e2fe-111">Example 2: Get every Redis Cache in a resource group</span></span>
```
PS C:\>Get-AzureRmRedisCache -ResourceGroupName "myGroup"

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

<span data-ttu-id="4e2fe-112">這個命令會取得指定資源群組中的每個 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="4e2fe-112">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="4e2fe-113">範例3：在目前的訂閱中取得每個 Redis 快取</span><span class="sxs-lookup"><span data-stu-id="4e2fe-113">Example 3: Get every Redis Cache in the current subscription</span></span>
```
PS C:\>Get-AzureRmRedisCache

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

<span data-ttu-id="4e2fe-114">這個命令會在目前的訂閱中取得每個 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="4e2fe-114">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="4e2fe-115">參數</span><span class="sxs-lookup"><span data-stu-id="4e2fe-115">PARAMETERS</span></span>

### <span data-ttu-id="4e2fe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e2fe-116">-DefaultProfile</span></span>
<span data-ttu-id="4e2fe-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e2fe-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e2fe-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="4e2fe-118">-Name</span></span>
<span data-ttu-id="4e2fe-119">指定要取得之 Redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e2fe-119">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="4e2fe-120">與 *ResourceGroupName* 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="4e2fe-120">Use with the *ResourceGroupName* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e2fe-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e2fe-121">-ResourceGroupName</span></span>
<span data-ttu-id="4e2fe-122">指定包含要取得之 Redis 快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e2fe-122">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>

<span data-ttu-id="4e2fe-123">如果您只指定 *ResourceGroupName* 參數，此操作會取得指定資源群組中的每個 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="4e2fe-123">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e2fe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e2fe-124">CommonParameters</span></span>
<span data-ttu-id="4e2fe-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e2fe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e2fe-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4e2fe-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e2fe-127">輸入</span><span class="sxs-lookup"><span data-stu-id="4e2fe-127">INPUTS</span></span>

### <span data-ttu-id="4e2fe-128">所有</span><span class="sxs-lookup"><span data-stu-id="4e2fe-128">None</span></span>
<span data-ttu-id="4e2fe-129">您可以依名稱將輸入管到這個 Cmdlet，但不能依值進行。</span><span class="sxs-lookup"><span data-stu-id="4e2fe-129">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="4e2fe-130">輸出</span><span class="sxs-lookup"><span data-stu-id="4e2fe-130">OUTPUTS</span></span>

### <span data-ttu-id="4e2fe-131">RedisCacheAttributes 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="4e2fe-131">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>
<span data-ttu-id="4e2fe-132">傳回 **RedisCacheAttributes** 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="4e2fe-132">Returns an array of **RedisCacheAttributes** objects.</span></span>

## <span data-ttu-id="4e2fe-133">筆記</span><span class="sxs-lookup"><span data-stu-id="4e2fe-133">NOTES</span></span>

## <span data-ttu-id="4e2fe-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e2fe-134">RELATED LINKS</span></span>

[<span data-ttu-id="4e2fe-135">新-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4e2fe-135">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="4e2fe-136">移除-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4e2fe-136">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="4e2fe-137">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4e2fe-137">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


