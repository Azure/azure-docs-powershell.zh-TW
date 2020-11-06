---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
ms.openlocfilehash: ee4d5980743e5a78205c6e1f78cb55fa9b2f6496
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455079"
---
# <span data-ttu-id="f8057-101">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f8057-101">Get-AzureRmRedisCache</span></span>

## <span data-ttu-id="f8057-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f8057-102">SYNOPSIS</span></span>
<span data-ttu-id="f8057-103">取得 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="f8057-103">Gets a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8057-104">句法</span><span class="sxs-lookup"><span data-stu-id="f8057-104">SYNTAX</span></span>

```
Get-AzureRmRedisCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8057-105">說明</span><span class="sxs-lookup"><span data-stu-id="f8057-105">DESCRIPTION</span></span>
<span data-ttu-id="f8057-106">AzureRmRedisCache Cmdlet 會取得指定的 Azure Redis 快 **取** 。</span><span class="sxs-lookup"><span data-stu-id="f8057-106">The **Get-AzureRmRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="f8057-107">如果您沒有指定參數，此操作會取得目前訂閱的每個 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="f8057-107">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="f8057-108">示例</span><span class="sxs-lookup"><span data-stu-id="f8057-108">EXAMPLES</span></span>

### <span data-ttu-id="f8057-109">範例1：依名稱取得 Redis 快取</span><span class="sxs-lookup"><span data-stu-id="f8057-109">Example 1: Get a Redis Cache by name</span></span>
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

<span data-ttu-id="f8057-110">這個命令會取得名為 myexists 的 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="f8057-110">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="f8057-111">範例2：取得資源群組中的每個 Redis 快取</span><span class="sxs-lookup"><span data-stu-id="f8057-111">Example 2: Get every Redis Cache in a resource group</span></span>
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

<span data-ttu-id="f8057-112">這個命令會取得指定資源群組中的每個 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="f8057-112">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="f8057-113">範例3：在目前的訂閱中取得每個 Redis 快取</span><span class="sxs-lookup"><span data-stu-id="f8057-113">Example 3: Get every Redis Cache in the current subscription</span></span>
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

<span data-ttu-id="f8057-114">這個命令會在目前的訂閱中取得每個 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="f8057-114">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="f8057-115">參數</span><span class="sxs-lookup"><span data-stu-id="f8057-115">PARAMETERS</span></span>

### <span data-ttu-id="f8057-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8057-116">-DefaultProfile</span></span>
<span data-ttu-id="f8057-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f8057-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8057-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="f8057-118">-Name</span></span>
<span data-ttu-id="f8057-119">指定要取得之 Redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8057-119">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="f8057-120">與 *ResourceGroupName* 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="f8057-120">Use with the *ResourceGroupName* parameter.</span></span>

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

### <span data-ttu-id="f8057-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8057-121">-ResourceGroupName</span></span>
<span data-ttu-id="f8057-122">指定包含要取得之 Redis 快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8057-122">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>
<span data-ttu-id="f8057-123">如果您只指定 *ResourceGroupName* 參數，此操作會取得指定資源群組中的每個 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="f8057-123">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

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

### <span data-ttu-id="f8057-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8057-124">CommonParameters</span></span>
<span data-ttu-id="f8057-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f8057-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8057-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f8057-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8057-127">輸入</span><span class="sxs-lookup"><span data-stu-id="f8057-127">INPUTS</span></span>

### <span data-ttu-id="f8057-128">System.object</span><span class="sxs-lookup"><span data-stu-id="f8057-128">System.String</span></span>

## <span data-ttu-id="f8057-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f8057-129">OUTPUTS</span></span>

### <span data-ttu-id="f8057-130">RedisCacheAttributes 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="f8057-130">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="f8057-131">筆記</span><span class="sxs-lookup"><span data-stu-id="f8057-131">NOTES</span></span>

## <span data-ttu-id="f8057-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8057-132">RELATED LINKS</span></span>

[<span data-ttu-id="f8057-133">新-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f8057-133">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="f8057-134">移除-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f8057-134">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="f8057-135">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f8057-135">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


