---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: 231787f57061ff4e118510c3dc166915b39da436
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448596"
---
# <span data-ttu-id="83781-101">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="83781-101">Get-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="83781-102">摘要</span><span class="sxs-lookup"><span data-stu-id="83781-102">SYNOPSIS</span></span>
<span data-ttu-id="83781-103">取得在 Redis Cache 上設定的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="83781-103">Get firewall rules set on Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83781-104">句法</span><span class="sxs-lookup"><span data-stu-id="83781-104">SYNTAX</span></span>

```
Get-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83781-105">說明</span><span class="sxs-lookup"><span data-stu-id="83781-105">DESCRIPTION</span></span>
<span data-ttu-id="83781-106">如果提供 **RuleName** 參數，AzureRmRedisCacheFirewallRule Cmdlet 會取得 Azure Redis 快 **取** 上指定防火牆規則的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="83781-106">If **RuleName** parameter if provided, **Get-AzureRmRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="83781-107">如果只指定 **Name** ，此操作會取得該 Redis 快取上所有可用的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="83781-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="83781-108">示例</span><span class="sxs-lookup"><span data-stu-id="83781-108">EXAMPLES</span></span>

### <span data-ttu-id="83781-109">範例1：取得單一防火牆規則</span><span class="sxs-lookup"><span data-stu-id="83781-109">Example 1: Get a single firewall rule</span></span>
```
PS C:\>Get-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="83781-110">這個命令會從名為 mycache 的 Redis Cache 中取得名為 ruleone 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="83781-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="83781-111">範例2：取得所有防火牆規則</span><span class="sxs-lookup"><span data-stu-id="83781-111">Example 2: Get all firewall rules</span></span>
```
PS C:\>Get-AzureRmRedisCacheFirewallRule -Name "mycache"

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

<span data-ttu-id="83781-112">這個命令會從已命名 mycache 的 Redis 快取中取得所有防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="83781-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="83781-113">參數</span><span class="sxs-lookup"><span data-stu-id="83781-113">PARAMETERS</span></span>

### <span data-ttu-id="83781-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83781-114">-DefaultProfile</span></span>
<span data-ttu-id="83781-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="83781-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83781-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="83781-116">-Name</span></span>
<span data-ttu-id="83781-117">Redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="83781-117">Name of redis cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83781-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83781-118">-ResourceGroupName</span></span>
<span data-ttu-id="83781-119">快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="83781-119">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="83781-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="83781-120">-RuleName</span></span>
<span data-ttu-id="83781-121">防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="83781-121">Name of firewall rule.</span></span>

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

### <span data-ttu-id="83781-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83781-122">CommonParameters</span></span>
<span data-ttu-id="83781-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="83781-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83781-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="83781-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83781-125">輸入</span><span class="sxs-lookup"><span data-stu-id="83781-125">INPUTS</span></span>

### <span data-ttu-id="83781-126">System.object</span><span class="sxs-lookup"><span data-stu-id="83781-126">System.String</span></span>
<span data-ttu-id="83781-127">您可以依名稱將輸入管到這個 Cmdlet，但不能依值進行。</span><span class="sxs-lookup"><span data-stu-id="83781-127">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="83781-128">輸出</span><span class="sxs-lookup"><span data-stu-id="83781-128">OUTPUTS</span></span>

### <span data-ttu-id="83781-129">[System.object]。清單 ' 1 [RedisCache. PSRedisFirewallRule，RedisCache，版本 = 4.0.1.0，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="83781-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule, Microsoft.Azure.Commands.RedisCache, Version=4.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="83781-130">筆記</span><span class="sxs-lookup"><span data-stu-id="83781-130">NOTES</span></span>

## <span data-ttu-id="83781-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="83781-131">RELATED LINKS</span></span>

[<span data-ttu-id="83781-132">新-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="83781-132">New-AzureRmRedisCacheFirewallRule</span></span>](./New-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="83781-133">移除-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="83781-133">Remove-AzureRmRedisCacheFirewallRule</span></span>](./Remove-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="83781-134">AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="83781-134">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="83781-135">新-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="83781-135">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="83781-136">移除-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="83781-136">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="83781-137">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="83781-137">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
