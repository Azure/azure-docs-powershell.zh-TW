---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 1bf6394621435293be1d00d4a9e9f435c160e668
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791825"
---
# <span data-ttu-id="29af5-101">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="29af5-101">Get-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="29af5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="29af5-102">SYNOPSIS</span></span>
<span data-ttu-id="29af5-103">取得在 Redis Cache 上設定的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="29af5-103">Get firewall rules set on Redis Cache.</span></span>

## <span data-ttu-id="29af5-104">句法</span><span class="sxs-lookup"><span data-stu-id="29af5-104">SYNTAX</span></span>

```
Get-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29af5-105">說明</span><span class="sxs-lookup"><span data-stu-id="29af5-105">DESCRIPTION</span></span>
<span data-ttu-id="29af5-106">如果提供 **RuleName** 參數，AzRedisCacheFirewallRule Cmdlet 會取得 Azure Redis 快 **取** 上指定防火牆規則的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="29af5-106">If **RuleName** parameter if provided, **Get-AzRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="29af5-107">如果只指定 **Name** ，此操作會取得該 Redis 快取上所有可用的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="29af5-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="29af5-108">示例</span><span class="sxs-lookup"><span data-stu-id="29af5-108">EXAMPLES</span></span>

### <span data-ttu-id="29af5-109">範例1：取得單一防火牆規則</span><span class="sxs-lookup"><span data-stu-id="29af5-109">Example 1: Get a single firewall rule</span></span>
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

<span data-ttu-id="29af5-110">這個命令會從名為 mycache 的 Redis Cache 中取得名為 ruleone 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="29af5-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="29af5-111">範例2：取得所有防火牆規則</span><span class="sxs-lookup"><span data-stu-id="29af5-111">Example 2: Get all firewall rules</span></span>
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

<span data-ttu-id="29af5-112">這個命令會從已命名 mycache 的 Redis 快取中取得所有防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="29af5-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="29af5-113">參數</span><span class="sxs-lookup"><span data-stu-id="29af5-113">PARAMETERS</span></span>

### <span data-ttu-id="29af5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29af5-114">-DefaultProfile</span></span>
<span data-ttu-id="29af5-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="29af5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29af5-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="29af5-116">-Name</span></span>
<span data-ttu-id="29af5-117">Redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="29af5-117">Name of redis cache.</span></span>

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

### <span data-ttu-id="29af5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29af5-118">-ResourceGroupName</span></span>
<span data-ttu-id="29af5-119">快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="29af5-119">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="29af5-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="29af5-120">-RuleName</span></span>
<span data-ttu-id="29af5-121">防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="29af5-121">Name of firewall rule.</span></span>

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

### <span data-ttu-id="29af5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29af5-122">CommonParameters</span></span>
<span data-ttu-id="29af5-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="29af5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29af5-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="29af5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29af5-125">輸入</span><span class="sxs-lookup"><span data-stu-id="29af5-125">INPUTS</span></span>

### <span data-ttu-id="29af5-126">System.object</span><span class="sxs-lookup"><span data-stu-id="29af5-126">System.String</span></span>

## <span data-ttu-id="29af5-127">輸出</span><span class="sxs-lookup"><span data-stu-id="29af5-127">OUTPUTS</span></span>

### <span data-ttu-id="29af5-128">PSRedisFirewallRule 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="29af5-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="29af5-129">筆記</span><span class="sxs-lookup"><span data-stu-id="29af5-129">NOTES</span></span>

## <span data-ttu-id="29af5-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="29af5-130">RELATED LINKS</span></span>

[<span data-ttu-id="29af5-131">新-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="29af5-131">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="29af5-132">移除-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="29af5-132">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="29af5-133">AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="29af5-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="29af5-134">新-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="29af5-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="29af5-135">移除-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="29af5-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="29af5-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="29af5-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)