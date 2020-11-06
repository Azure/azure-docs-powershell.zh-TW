---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
ms.openlocfilehash: e24ea6e0b5bf88b17a6209f2ea69634200a10a62
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620977"
---
# <span data-ttu-id="10f3b-101">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="10f3b-101">Remove-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="10f3b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="10f3b-102">SYNOPSIS</span></span>
<span data-ttu-id="10f3b-103">從 Redis 快取中移除防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="10f3b-103">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="10f3b-104">句法</span><span class="sxs-lookup"><span data-stu-id="10f3b-104">SYNTAX</span></span>

### <span data-ttu-id="10f3b-105">NormalParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="10f3b-105">NormalParameterSet (Default)</span></span>
```
Remove-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10f3b-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="10f3b-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10f3b-107">說明</span><span class="sxs-lookup"><span data-stu-id="10f3b-107">DESCRIPTION</span></span>
<span data-ttu-id="10f3b-108">從 Redis 快取中移除防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="10f3b-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="10f3b-109">示例</span><span class="sxs-lookup"><span data-stu-id="10f3b-109">EXAMPLES</span></span>

### <span data-ttu-id="10f3b-110">範例1：移除單一防火牆規則</span><span class="sxs-lookup"><span data-stu-id="10f3b-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="10f3b-111">這個命令會從名為 mycache 的 Redis Cache 中移除名為 ruleone 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="10f3b-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="10f3b-112">參數</span><span class="sxs-lookup"><span data-stu-id="10f3b-112">PARAMETERS</span></span>

### <span data-ttu-id="10f3b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10f3b-113">-DefaultProfile</span></span>
<span data-ttu-id="10f3b-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="10f3b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10f3b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10f3b-115">-InputObject</span></span>
<span data-ttu-id="10f3b-116">類型 PSRedisFirewallRule 的物件</span><span class="sxs-lookup"><span data-stu-id="10f3b-116">object of type PSRedisFirewallRule</span></span>

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

### <span data-ttu-id="10f3b-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="10f3b-117">-Name</span></span>
<span data-ttu-id="10f3b-118">Redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="10f3b-118">Name of redis cache.</span></span>

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

### <span data-ttu-id="10f3b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10f3b-119">-PassThru</span></span>
<span data-ttu-id="10f3b-120">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="10f3b-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="10f3b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10f3b-121">-ResourceGroupName</span></span>
<span data-ttu-id="10f3b-122">快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="10f3b-122">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="10f3b-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="10f3b-123">-RuleName</span></span>
<span data-ttu-id="10f3b-124">防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="10f3b-124">Name of firewall rule.</span></span>

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

### <span data-ttu-id="10f3b-125">-確認</span><span class="sxs-lookup"><span data-stu-id="10f3b-125">-Confirm</span></span>
<span data-ttu-id="10f3b-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="10f3b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10f3b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10f3b-127">-WhatIf</span></span>
<span data-ttu-id="10f3b-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="10f3b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10f3b-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10f3b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10f3b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10f3b-130">CommonParameters</span></span>
<span data-ttu-id="10f3b-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="10f3b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10f3b-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="10f3b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10f3b-133">輸入</span><span class="sxs-lookup"><span data-stu-id="10f3b-133">INPUTS</span></span>

### <span data-ttu-id="10f3b-134">System.object</span><span class="sxs-lookup"><span data-stu-id="10f3b-134">System.String</span></span>

### <span data-ttu-id="10f3b-135">PSRedisFirewallRule 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="10f3b-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="10f3b-136">輸出</span><span class="sxs-lookup"><span data-stu-id="10f3b-136">OUTPUTS</span></span>

### <span data-ttu-id="10f3b-137">System.object</span><span class="sxs-lookup"><span data-stu-id="10f3b-137">System.Boolean</span></span>

## <span data-ttu-id="10f3b-138">筆記</span><span class="sxs-lookup"><span data-stu-id="10f3b-138">NOTES</span></span>

## <span data-ttu-id="10f3b-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="10f3b-139">RELATED LINKS</span></span>

[<span data-ttu-id="10f3b-140">新-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="10f3b-140">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="10f3b-141">AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="10f3b-141">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="10f3b-142">AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="10f3b-142">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="10f3b-143">新-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="10f3b-143">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="10f3b-144">移除-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="10f3b-144">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="10f3b-145">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="10f3b-145">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)