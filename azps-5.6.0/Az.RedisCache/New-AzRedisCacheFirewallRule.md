---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/powershell/module/az.rediscache/new-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
ms.openlocfilehash: bd0d6995cae0d32a7fb0ce46d42f87a480c275f8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903090"
---
# <span data-ttu-id="b48a4-101">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b48a4-101">New-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="b48a4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b48a4-102">SYNOPSIS</span></span>
<span data-ttu-id="b48a4-103">在 Redis Cache 上建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="b48a4-103">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="b48a4-104">語法</span><span class="sxs-lookup"><span data-stu-id="b48a4-104">SYNTAX</span></span>

### <span data-ttu-id="b48a4-105">NormalParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b48a4-105">NormalParameterSet (Default)</span></span>
```
New-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b48a4-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="b48a4-106">RedisCacheAttributesObject</span></span>
```
New-AzRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b48a4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b48a4-107">ResourceIdParameterSet</span></span>
```
New-AzRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b48a4-108">描述</span><span class="sxs-lookup"><span data-stu-id="b48a4-108">DESCRIPTION</span></span>
<span data-ttu-id="b48a4-109">在 Redis Cache 上建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="b48a4-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="b48a4-110">例子</span><span class="sxs-lookup"><span data-stu-id="b48a4-110">EXAMPLES</span></span>

### <span data-ttu-id="b48a4-111">範例 1：建立防火牆規則</span><span class="sxs-lookup"><span data-stu-id="b48a4-111">Example 1: Create a firewall rule</span></span>
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

<span data-ttu-id="b48a4-112">此命令在 Redis Cache 名為 mycache 上建立名為 ruleone 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="b48a4-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="b48a4-113">參數</span><span class="sxs-lookup"><span data-stu-id="b48a4-113">PARAMETERS</span></span>

### <span data-ttu-id="b48a4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b48a4-114">-DefaultProfile</span></span>
<span data-ttu-id="b48a4-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b48a4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b48a4-116">-EndIP</span><span class="sxs-lookup"><span data-stu-id="b48a4-116">-EndIP</span></span>
<span data-ttu-id="b48a4-117">結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b48a4-117">Ending IP address.</span></span>

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

### <span data-ttu-id="b48a4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b48a4-118">-InputObject</span></span>
<span data-ttu-id="b48a4-119">類型為 RedisCacheAttributes 的物件</span><span class="sxs-lookup"><span data-stu-id="b48a4-119">object of type RedisCacheAttributes</span></span>

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

### <span data-ttu-id="b48a4-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="b48a4-120">-Name</span></span>
<span data-ttu-id="b48a4-121">重新具名快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="b48a4-121">Name of redis cache.</span></span>

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

### <span data-ttu-id="b48a4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b48a4-122">-ResourceGroupName</span></span>
<span data-ttu-id="b48a4-123">存在緩存的資源組名。</span><span class="sxs-lookup"><span data-stu-id="b48a4-123">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="b48a4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b48a4-124">-ResourceId</span></span>
<span data-ttu-id="b48a4-125">REDis Cache 的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="b48a4-125">ARM Id of Redis Cache.</span></span>

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

### <span data-ttu-id="b48a4-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="b48a4-126">-RuleName</span></span>
<span data-ttu-id="b48a4-127">防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="b48a4-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="b48a4-128">-StartIP</span><span class="sxs-lookup"><span data-stu-id="b48a4-128">-StartIP</span></span>
<span data-ttu-id="b48a4-129">正在啟動 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b48a4-129">Starting IP address.</span></span>

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

### <span data-ttu-id="b48a4-130">-確認</span><span class="sxs-lookup"><span data-stu-id="b48a4-130">-Confirm</span></span>
<span data-ttu-id="b48a4-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b48a4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b48a4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b48a4-132">-WhatIf</span></span>
<span data-ttu-id="b48a4-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b48a4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b48a4-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b48a4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b48a4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b48a4-135">CommonParameters</span></span>
<span data-ttu-id="b48a4-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b48a4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b48a4-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b48a4-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b48a4-138">輸入</span><span class="sxs-lookup"><span data-stu-id="b48a4-138">INPUTS</span></span>

### <span data-ttu-id="b48a4-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b48a4-139">System.String</span></span>

### <span data-ttu-id="b48a4-140">Microsoft.Azure.Commands.RedisCache.models.RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="b48a4-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="b48a4-141">輸出</span><span class="sxs-lookup"><span data-stu-id="b48a4-141">OUTPUTS</span></span>

### <span data-ttu-id="b48a4-142">Microsoft.Azure.Commands.RedisCache.models.PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b48a4-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="b48a4-143">筆記</span><span class="sxs-lookup"><span data-stu-id="b48a4-143">NOTES</span></span>

## <span data-ttu-id="b48a4-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="b48a4-144">RELATED LINKS</span></span>

[<span data-ttu-id="b48a4-145">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b48a4-145">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="b48a4-146">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b48a4-146">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="b48a4-147">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="b48a4-147">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="b48a4-148">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="b48a4-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="b48a4-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="b48a4-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="b48a4-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="b48a4-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)