---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/powershell/module/az.rediscache/remove-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 9c68e89d09d386d6071cb639fa77ba740a6da53f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907089"
---
# <span data-ttu-id="2d061-101">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2d061-101">Remove-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="2d061-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2d061-102">SYNOPSIS</span></span>
<span data-ttu-id="2d061-103">從 Redis Cache 移除防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="2d061-103">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="2d061-104">語法</span><span class="sxs-lookup"><span data-stu-id="2d061-104">SYNTAX</span></span>

### <span data-ttu-id="2d061-105">NormalParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2d061-105">NormalParameterSet (Default)</span></span>
```
Remove-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d061-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="2d061-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d061-107">描述</span><span class="sxs-lookup"><span data-stu-id="2d061-107">DESCRIPTION</span></span>
<span data-ttu-id="2d061-108">從 Redis Cache 移除防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="2d061-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="2d061-109">例子</span><span class="sxs-lookup"><span data-stu-id="2d061-109">EXAMPLES</span></span>

### <span data-ttu-id="2d061-110">範例 1：移除單一防火牆規則</span><span class="sxs-lookup"><span data-stu-id="2d061-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="2d061-111">此命令會從名為 mycache 的 Redis Cache 移除名為 ruleone 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="2d061-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="2d061-112">參數</span><span class="sxs-lookup"><span data-stu-id="2d061-112">PARAMETERS</span></span>

### <span data-ttu-id="2d061-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d061-113">-DefaultProfile</span></span>
<span data-ttu-id="2d061-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2d061-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d061-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d061-115">-InputObject</span></span>
<span data-ttu-id="2d061-116">類型 PSRedisFirewallRule 的物件</span><span class="sxs-lookup"><span data-stu-id="2d061-116">object of type PSRedisFirewallRule</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule
Parameter Sets: PSRedisFirewallRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d061-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="2d061-117">-Name</span></span>
<span data-ttu-id="2d061-118">重新具名快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d061-118">Name of redis cache.</span></span>

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

### <span data-ttu-id="2d061-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d061-119">-PassThru</span></span>
<span data-ttu-id="2d061-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="2d061-120">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d061-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d061-121">-ResourceGroupName</span></span>
<span data-ttu-id="2d061-122">存在緩存的資源組名。</span><span class="sxs-lookup"><span data-stu-id="2d061-122">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="2d061-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="2d061-123">-RuleName</span></span>
<span data-ttu-id="2d061-124">防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d061-124">Name of firewall rule.</span></span>

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

### <span data-ttu-id="2d061-125">-確認</span><span class="sxs-lookup"><span data-stu-id="2d061-125">-Confirm</span></span>
<span data-ttu-id="2d061-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2d061-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d061-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d061-127">-WhatIf</span></span>
<span data-ttu-id="2d061-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2d061-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d061-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2d061-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d061-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d061-130">CommonParameters</span></span>
<span data-ttu-id="2d061-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2d061-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d061-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2d061-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d061-133">輸入</span><span class="sxs-lookup"><span data-stu-id="2d061-133">INPUTS</span></span>

### <span data-ttu-id="2d061-134">System.String</span><span class="sxs-lookup"><span data-stu-id="2d061-134">System.String</span></span>

### <span data-ttu-id="2d061-135">Microsoft.Azure.Commands.RedisCache.models.PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2d061-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="2d061-136">輸出</span><span class="sxs-lookup"><span data-stu-id="2d061-136">OUTPUTS</span></span>

### <span data-ttu-id="2d061-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2d061-137">System.Boolean</span></span>

## <span data-ttu-id="2d061-138">筆記</span><span class="sxs-lookup"><span data-stu-id="2d061-138">NOTES</span></span>

## <span data-ttu-id="2d061-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="2d061-139">RELATED LINKS</span></span>

[<span data-ttu-id="2d061-140">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2d061-140">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="2d061-141">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2d061-141">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="2d061-142">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2d061-142">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="2d061-143">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2d061-143">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="2d061-144">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2d061-144">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="2d061-145">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2d061-145">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)