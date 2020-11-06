---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
ms.openlocfilehash: 4cdd81b0cf9f83482192fbe6f484fb0b0d1beaf6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455620"
---
# <span data-ttu-id="bca84-101">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="bca84-101">Get-AzureRmRedisCache</span></span>

## <span data-ttu-id="bca84-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bca84-102">SYNOPSIS</span></span>
<span data-ttu-id="bca84-103">取得 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="bca84-103">Gets a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bca84-104">句法</span><span class="sxs-lookup"><span data-stu-id="bca84-104">SYNTAX</span></span>

### <span data-ttu-id="bca84-105">[全部在訂閱] 中 (預設) </span><span class="sxs-lookup"><span data-stu-id="bca84-105">All In Subscription (Default)</span></span>
```
Get-AzureRmRedisCache [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bca84-106">[資源群組] 中的 [全部]</span><span class="sxs-lookup"><span data-stu-id="bca84-106">All In Resource Group</span></span>
```
Get-AzureRmRedisCache -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bca84-107">特定 Redis 快取</span><span class="sxs-lookup"><span data-stu-id="bca84-107">Specific Redis Cache</span></span>
```
Get-AzureRmRedisCache -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bca84-108">說明</span><span class="sxs-lookup"><span data-stu-id="bca84-108">DESCRIPTION</span></span>
<span data-ttu-id="bca84-109">AzureRmRedisCache Cmdlet 會取得指定的 Azure Redis 快 **取** 。</span><span class="sxs-lookup"><span data-stu-id="bca84-109">The **Get-AzureRmRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="bca84-110">如果您沒有指定參數，此操作會取得目前訂閱的每個 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="bca84-110">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="bca84-111">示例</span><span class="sxs-lookup"><span data-stu-id="bca84-111">EXAMPLES</span></span>

### <span data-ttu-id="bca84-112">範例1：依名稱取得 Redis 快取</span><span class="sxs-lookup"><span data-stu-id="bca84-112">Example 1: Get a Redis Cache by name</span></span>
```
PS C:\>Get-AzureRmRedisCache -ResourceGroupName "myGroup" -Name "myexists"

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
```

<span data-ttu-id="bca84-113">這個命令會取得名為 myexists 的 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="bca84-113">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="bca84-114">範例2：取得資源群組中的每個 Redis 快取</span><span class="sxs-lookup"><span data-stu-id="bca84-114">Example 2: Get every Redis Cache in a resource group</span></span>
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
```

<span data-ttu-id="bca84-115">這個命令會取得指定資源群組中的每個 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="bca84-115">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="bca84-116">範例3：在目前的訂閱中取得每個 Redis 快取</span><span class="sxs-lookup"><span data-stu-id="bca84-116">Example 3: Get every Redis Cache in the current subscription</span></span>
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
```

<span data-ttu-id="bca84-117">這個命令會在目前的訂閱中取得每個 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="bca84-117">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="bca84-118">參數</span><span class="sxs-lookup"><span data-stu-id="bca84-118">PARAMETERS</span></span>

### <span data-ttu-id="bca84-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="bca84-119">-Name</span></span>
<span data-ttu-id="bca84-120">指定要取得之 Redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="bca84-120">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="bca84-121">與 *ResourceGroupName* 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="bca84-121">Use with the *ResourceGroupName* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific Redis Cache
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bca84-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bca84-122">-ResourceGroupName</span></span>
<span data-ttu-id="bca84-123">指定包含要取得之 Redis 快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bca84-123">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>

<span data-ttu-id="bca84-124">如果您只指定 *ResourceGroupName* 參數，此操作會取得指定資源群組中的每個 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="bca84-124">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group, Specific Redis Cache
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bca84-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bca84-125">-DefaultProfile</span></span>
<span data-ttu-id="bca84-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bca84-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bca84-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bca84-127">CommonParameters</span></span>
<span data-ttu-id="bca84-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bca84-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bca84-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bca84-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bca84-130">輸入</span><span class="sxs-lookup"><span data-stu-id="bca84-130">INPUTS</span></span>

### <span data-ttu-id="bca84-131">所有</span><span class="sxs-lookup"><span data-stu-id="bca84-131">None</span></span>
<span data-ttu-id="bca84-132">您可以依名稱將輸入管到這個 Cmdlet，但不能依值進行。</span><span class="sxs-lookup"><span data-stu-id="bca84-132">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="bca84-133">輸出</span><span class="sxs-lookup"><span data-stu-id="bca84-133">OUTPUTS</span></span>

### <span data-ttu-id="bca84-134">RedisCacheAttributes 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="bca84-134">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>
<span data-ttu-id="bca84-135">傳回 **RedisCacheAttributes** 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="bca84-135">Returns an array of **RedisCacheAttributes** objects.</span></span>

## <span data-ttu-id="bca84-136">筆記</span><span class="sxs-lookup"><span data-stu-id="bca84-136">NOTES</span></span>

## <span data-ttu-id="bca84-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="bca84-137">RELATED LINKS</span></span>

[<span data-ttu-id="bca84-138">新-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="bca84-138">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="bca84-139">移除-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="bca84-139">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="bca84-140">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="bca84-140">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


