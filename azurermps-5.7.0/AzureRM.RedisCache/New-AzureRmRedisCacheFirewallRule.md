---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: c89589d966c03614255751bf13769689ff875332
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623962"
---
# <span data-ttu-id="207a3-101">New-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="207a3-101">New-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="207a3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="207a3-102">SYNOPSIS</span></span>
<span data-ttu-id="207a3-103">在 Redis 快取上建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="207a3-103">Create a firewall rule on a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="207a3-104">句法</span><span class="sxs-lookup"><span data-stu-id="207a3-104">SYNTAX</span></span>

### <span data-ttu-id="207a3-105">NormalParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="207a3-105">NormalParameterSet (Default)</span></span>
```
New-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String>
 -StartIP <String> -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="207a3-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="207a3-106">RedisCacheAttributesObject</span></span>
```
New-AzureRmRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="207a3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="207a3-107">ResourceIdParameterSet</span></span>
```
New-AzureRmRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="207a3-108">說明</span><span class="sxs-lookup"><span data-stu-id="207a3-108">DESCRIPTION</span></span>
<span data-ttu-id="207a3-109">在 Redis 快取上建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="207a3-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="207a3-110">示例</span><span class="sxs-lookup"><span data-stu-id="207a3-110">EXAMPLES</span></span>

### <span data-ttu-id="207a3-111">範例1：建立防火牆規則</span><span class="sxs-lookup"><span data-stu-id="207a3-111">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -StartIP "10.0.0.1" -EndIP "10.0.0.32"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="207a3-112">這個命令會在名為 mycache 的 Redis Cache 上建立名為 ruleone 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="207a3-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="207a3-113">參數</span><span class="sxs-lookup"><span data-stu-id="207a3-113">PARAMETERS</span></span>

### <span data-ttu-id="207a3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="207a3-114">-DefaultProfile</span></span>
<span data-ttu-id="207a3-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="207a3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="207a3-116">-EndIP</span><span class="sxs-lookup"><span data-stu-id="207a3-116">-EndIP</span></span>
<span data-ttu-id="207a3-117">[結束 IP 位址]。</span><span class="sxs-lookup"><span data-stu-id="207a3-117">Ending IP address.</span></span>

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

### <span data-ttu-id="207a3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="207a3-118">-InputObject</span></span>
<span data-ttu-id="207a3-119">類型 RedisCacheAttributes 的物件</span><span class="sxs-lookup"><span data-stu-id="207a3-119">object of type RedisCacheAttributes</span></span>

```yaml
Type: RedisCacheAttributes
Parameter Sets: RedisCacheAttributesObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="207a3-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="207a3-120">-Name</span></span>
<span data-ttu-id="207a3-121">Redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="207a3-121">Name of redis cache.</span></span>

```yaml
Type: String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="207a3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="207a3-122">-ResourceGroupName</span></span>
<span data-ttu-id="207a3-123">快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="207a3-123">Name of resource group in which cache exists.</span></span>

```yaml
Type: String
Parameter Sets: NormalParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="207a3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="207a3-124">-ResourceId</span></span>
<span data-ttu-id="207a3-125">Redis 快取的 ARM Id。</span><span class="sxs-lookup"><span data-stu-id="207a3-125">ARM Id of Redis Cache.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="207a3-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="207a3-126">-RuleName</span></span>
<span data-ttu-id="207a3-127">防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="207a3-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="207a3-128">-StartIP</span><span class="sxs-lookup"><span data-stu-id="207a3-128">-StartIP</span></span>
<span data-ttu-id="207a3-129">起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="207a3-129">Starting IP address.</span></span>

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

### <span data-ttu-id="207a3-130">-確認</span><span class="sxs-lookup"><span data-stu-id="207a3-130">-Confirm</span></span>
<span data-ttu-id="207a3-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="207a3-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="207a3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="207a3-132">-WhatIf</span></span>
<span data-ttu-id="207a3-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="207a3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="207a3-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="207a3-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="207a3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="207a3-135">CommonParameters</span></span>
<span data-ttu-id="207a3-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="207a3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="207a3-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="207a3-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="207a3-138">輸入</span><span class="sxs-lookup"><span data-stu-id="207a3-138">INPUTS</span></span>

### <span data-ttu-id="207a3-139">System.object</span><span class="sxs-lookup"><span data-stu-id="207a3-139">System.String</span></span>

## <span data-ttu-id="207a3-140">輸出</span><span class="sxs-lookup"><span data-stu-id="207a3-140">OUTPUTS</span></span>

### <span data-ttu-id="207a3-141">PSRedisFirewallRule 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="207a3-141">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="207a3-142">筆記</span><span class="sxs-lookup"><span data-stu-id="207a3-142">NOTES</span></span>

## <span data-ttu-id="207a3-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="207a3-143">RELATED LINKS</span></span>

[<span data-ttu-id="207a3-144">AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="207a3-144">Get-AzureRmRedisCacheFirewallRule</span></span>](./Get-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="207a3-145">移除-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="207a3-145">Remove-AzureRmRedisCacheFirewallRule</span></span>](./Remove-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="207a3-146">AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="207a3-146">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="207a3-147">新-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="207a3-147">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="207a3-148">移除-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="207a3-148">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="207a3-149">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="207a3-149">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
