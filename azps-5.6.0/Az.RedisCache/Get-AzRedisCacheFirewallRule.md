---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/powershell/module/az.rediscache/get-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 5e17eced3525a7aa318cbba19b632d3ae11d79a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917654"
---
# <span data-ttu-id="df793-101">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="df793-101">Get-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="df793-102">簡介</span><span class="sxs-lookup"><span data-stu-id="df793-102">SYNOPSIS</span></span>
<span data-ttu-id="df793-103">在 Redis Cache 上設定防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="df793-103">Get firewall rules set on Redis Cache.</span></span>

## <span data-ttu-id="df793-104">語法</span><span class="sxs-lookup"><span data-stu-id="df793-104">SYNTAX</span></span>

```
Get-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df793-105">描述</span><span class="sxs-lookup"><span data-stu-id="df793-105">DESCRIPTION</span></span>
<span data-ttu-id="df793-106">如果 **提供 RuleName** 參數 **，Get-AzRedisCacheFirewallRule** Cmdlet 會取得 Azure Redis Cache 上指定防火牆規則的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="df793-106">If **RuleName** parameter if provided, **Get-AzRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="df793-107">如果只 **指定名稱** ，此作業會獲得該 Redis Cache 上所有可用的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="df793-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="df793-108">例子</span><span class="sxs-lookup"><span data-stu-id="df793-108">EXAMPLES</span></span>

### <span data-ttu-id="df793-109">範例 1：取得單一防火牆規則</span><span class="sxs-lookup"><span data-stu-id="df793-109">Example 1: Get a single firewall rule</span></span>
```
PS C:\>Get-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="df793-110">此命令會從 Redis Cache 中名為 mycache 的防火牆規則命名為 ruleone。</span><span class="sxs-lookup"><span data-stu-id="df793-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="df793-111">範例 2：取得所有防火牆規則</span><span class="sxs-lookup"><span data-stu-id="df793-111">Example 2: Get all firewall rules</span></span>
```
PS C:\>Get-AzRedisCacheFirewallRule -Name "mycache"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruletwo
        RuleName          : ruletwo
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.33
        EndIP             : 10.0.0.64
```

<span data-ttu-id="df793-112">此命令會從 Redis Cache 中所有名為 mycache 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="df793-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="df793-113">參數</span><span class="sxs-lookup"><span data-stu-id="df793-113">PARAMETERS</span></span>

### <span data-ttu-id="df793-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df793-114">-DefaultProfile</span></span>
<span data-ttu-id="df793-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="df793-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df793-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="df793-116">-Name</span></span>
<span data-ttu-id="df793-117">重新具名快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="df793-117">Name of redis cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df793-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df793-118">-ResourceGroupName</span></span>
<span data-ttu-id="df793-119">存在緩存的資源組名。</span><span class="sxs-lookup"><span data-stu-id="df793-119">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="df793-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="df793-120">-RuleName</span></span>
<span data-ttu-id="df793-121">防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="df793-121">Name of firewall rule.</span></span>

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

### <span data-ttu-id="df793-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df793-122">CommonParameters</span></span>
<span data-ttu-id="df793-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="df793-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df793-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="df793-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df793-125">輸入</span><span class="sxs-lookup"><span data-stu-id="df793-125">INPUTS</span></span>

### <span data-ttu-id="df793-126">System.String</span><span class="sxs-lookup"><span data-stu-id="df793-126">System.String</span></span>

## <span data-ttu-id="df793-127">輸出</span><span class="sxs-lookup"><span data-stu-id="df793-127">OUTPUTS</span></span>

### <span data-ttu-id="df793-128">Microsoft.Azure.Commands.RedisCache.models.PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="df793-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="df793-129">筆記</span><span class="sxs-lookup"><span data-stu-id="df793-129">NOTES</span></span>

## <span data-ttu-id="df793-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="df793-130">RELATED LINKS</span></span>

[<span data-ttu-id="df793-131">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="df793-131">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="df793-132">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="df793-132">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="df793-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="df793-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="df793-134">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="df793-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="df793-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="df793-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="df793-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="df793-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)