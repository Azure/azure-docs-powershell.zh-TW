---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 50a2df73d6cfa1e9d34f2c5c4b426f601c9d9309
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140925"
---
# <span data-ttu-id="7fe38-101">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7fe38-101">New-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="7fe38-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7fe38-102">SYNOPSIS</span></span>
<span data-ttu-id="7fe38-103">在 Redis 快取上建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="7fe38-103">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="7fe38-104">句法</span><span class="sxs-lookup"><span data-stu-id="7fe38-104">SYNTAX</span></span>

### <span data-ttu-id="7fe38-105">NormalParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7fe38-105">NormalParameterSet (Default)</span></span>
```
New-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fe38-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="7fe38-106">RedisCacheAttributesObject</span></span>
```
New-AzRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fe38-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fe38-107">ResourceIdParameterSet</span></span>
```
New-AzRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fe38-108">說明</span><span class="sxs-lookup"><span data-stu-id="7fe38-108">DESCRIPTION</span></span>
<span data-ttu-id="7fe38-109">在 Redis 快取上建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="7fe38-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="7fe38-110">示例</span><span class="sxs-lookup"><span data-stu-id="7fe38-110">EXAMPLES</span></span>

### <span data-ttu-id="7fe38-111">範例1：建立防火牆規則</span><span class="sxs-lookup"><span data-stu-id="7fe38-111">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -StartIP "10.0.0.1" -EndIP "10.0.0.32"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="7fe38-112">這個命令會在名為 mycache 的 Redis Cache 上建立名為 ruleone 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="7fe38-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="7fe38-113">參數</span><span class="sxs-lookup"><span data-stu-id="7fe38-113">PARAMETERS</span></span>

### <span data-ttu-id="7fe38-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fe38-114">-DefaultProfile</span></span>
<span data-ttu-id="7fe38-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7fe38-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fe38-116">-EndIP</span><span class="sxs-lookup"><span data-stu-id="7fe38-116">-EndIP</span></span>
<span data-ttu-id="7fe38-117">[結束 IP 位址]。</span><span class="sxs-lookup"><span data-stu-id="7fe38-117">Ending IP address.</span></span>

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

### <span data-ttu-id="7fe38-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fe38-118">-InputObject</span></span>
<span data-ttu-id="7fe38-119">類型 RedisCacheAttributes 的物件</span><span class="sxs-lookup"><span data-stu-id="7fe38-119">object of type RedisCacheAttributes</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes
Parameter Sets: RedisCacheAttributesObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fe38-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="7fe38-120">-Name</span></span>
<span data-ttu-id="7fe38-121">Redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="7fe38-121">Name of redis cache.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fe38-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fe38-122">-ResourceGroupName</span></span>
<span data-ttu-id="7fe38-123">快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7fe38-123">Name of resource group in which cache exists.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fe38-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fe38-124">-ResourceId</span></span>
<span data-ttu-id="7fe38-125">Redis 快取的 ARM Id。</span><span class="sxs-lookup"><span data-stu-id="7fe38-125">ARM Id of Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fe38-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="7fe38-126">-RuleName</span></span>
<span data-ttu-id="7fe38-127">防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="7fe38-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="7fe38-128">-StartIP</span><span class="sxs-lookup"><span data-stu-id="7fe38-128">-StartIP</span></span>
<span data-ttu-id="7fe38-129">起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="7fe38-129">Starting IP address.</span></span>

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

### <span data-ttu-id="7fe38-130">-確認</span><span class="sxs-lookup"><span data-stu-id="7fe38-130">-Confirm</span></span>
<span data-ttu-id="7fe38-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7fe38-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fe38-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fe38-132">-WhatIf</span></span>
<span data-ttu-id="7fe38-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7fe38-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fe38-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7fe38-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fe38-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fe38-135">CommonParameters</span></span>
<span data-ttu-id="7fe38-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7fe38-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fe38-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7fe38-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fe38-138">輸入</span><span class="sxs-lookup"><span data-stu-id="7fe38-138">INPUTS</span></span>

### <span data-ttu-id="7fe38-139">System.object</span><span class="sxs-lookup"><span data-stu-id="7fe38-139">System.String</span></span>

### <span data-ttu-id="7fe38-140">RedisCacheAttributes 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="7fe38-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="7fe38-141">輸出</span><span class="sxs-lookup"><span data-stu-id="7fe38-141">OUTPUTS</span></span>

### <span data-ttu-id="7fe38-142">PSRedisFirewallRule 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="7fe38-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="7fe38-143">筆記</span><span class="sxs-lookup"><span data-stu-id="7fe38-143">NOTES</span></span>

## <span data-ttu-id="7fe38-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="7fe38-144">RELATED LINKS</span></span>

[<span data-ttu-id="7fe38-145">AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7fe38-145">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="7fe38-146">移除-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7fe38-146">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="7fe38-147">AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7fe38-147">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="7fe38-148">新-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7fe38-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="7fe38-149">移除-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7fe38-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="7fe38-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7fe38-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)