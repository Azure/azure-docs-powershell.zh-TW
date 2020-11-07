---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: 25c3d0c72539ecd74e25ed455b4afcf4211c0718
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624884"
---
# <span data-ttu-id="dca21-101">Remove-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dca21-101">Remove-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="dca21-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dca21-102">SYNOPSIS</span></span>
<span data-ttu-id="dca21-103">從 Redis 快取中移除防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="dca21-103">Remove a firewall rule from a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dca21-104">句法</span><span class="sxs-lookup"><span data-stu-id="dca21-104">SYNTAX</span></span>

### <span data-ttu-id="dca21-105">NormalParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dca21-105">NormalParameterSet (Default)</span></span>
```
Remove-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dca21-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="dca21-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzureRmRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dca21-107">說明</span><span class="sxs-lookup"><span data-stu-id="dca21-107">DESCRIPTION</span></span>
<span data-ttu-id="dca21-108">從 Redis 快取中移除防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="dca21-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="dca21-109">示例</span><span class="sxs-lookup"><span data-stu-id="dca21-109">EXAMPLES</span></span>

### <span data-ttu-id="dca21-110">範例1：移除單一防火牆規則</span><span class="sxs-lookup"><span data-stu-id="dca21-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="dca21-111">這個命令會從名為 mycache 的 Redis Cache 中移除名為 ruleone 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="dca21-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="dca21-112">參數</span><span class="sxs-lookup"><span data-stu-id="dca21-112">PARAMETERS</span></span>

### <span data-ttu-id="dca21-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dca21-113">-DefaultProfile</span></span>
<span data-ttu-id="dca21-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dca21-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dca21-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dca21-115">-InputObject</span></span>
<span data-ttu-id="dca21-116">類型 PSRedisFirewallRule 的物件</span><span class="sxs-lookup"><span data-stu-id="dca21-116">object of type PSRedisFirewallRule</span></span>

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

### <span data-ttu-id="dca21-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="dca21-117">-Name</span></span>
<span data-ttu-id="dca21-118">Redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="dca21-118">Name of redis cache.</span></span>

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

### <span data-ttu-id="dca21-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dca21-119">-PassThru</span></span>
<span data-ttu-id="dca21-120">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="dca21-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="dca21-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dca21-121">-ResourceGroupName</span></span>
<span data-ttu-id="dca21-122">快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dca21-122">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="dca21-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="dca21-123">-RuleName</span></span>
<span data-ttu-id="dca21-124">防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="dca21-124">Name of firewall rule.</span></span>

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

### <span data-ttu-id="dca21-125">-確認</span><span class="sxs-lookup"><span data-stu-id="dca21-125">-Confirm</span></span>
<span data-ttu-id="dca21-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dca21-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dca21-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dca21-127">-WhatIf</span></span>
<span data-ttu-id="dca21-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dca21-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dca21-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dca21-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dca21-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dca21-130">CommonParameters</span></span>
<span data-ttu-id="dca21-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dca21-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dca21-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dca21-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dca21-133">輸入</span><span class="sxs-lookup"><span data-stu-id="dca21-133">INPUTS</span></span>

### <span data-ttu-id="dca21-134">System.object</span><span class="sxs-lookup"><span data-stu-id="dca21-134">System.String</span></span>

### <span data-ttu-id="dca21-135">PSRedisFirewallRule 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="dca21-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>
<span data-ttu-id="dca21-136">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="dca21-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="dca21-137">輸出</span><span class="sxs-lookup"><span data-stu-id="dca21-137">OUTPUTS</span></span>

### <span data-ttu-id="dca21-138">System.object</span><span class="sxs-lookup"><span data-stu-id="dca21-138">System.Boolean</span></span>

## <span data-ttu-id="dca21-139">筆記</span><span class="sxs-lookup"><span data-stu-id="dca21-139">NOTES</span></span>

## <span data-ttu-id="dca21-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="dca21-140">RELATED LINKS</span></span>

[<span data-ttu-id="dca21-141">新-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dca21-141">New-AzureRmRedisCacheFirewallRule</span></span>](./New-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="dca21-142">AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dca21-142">Get-AzureRmRedisCacheFirewallRule</span></span>](./Get-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="dca21-143">AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="dca21-143">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="dca21-144">新-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="dca21-144">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="dca21-145">移除-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="dca21-145">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="dca21-146">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="dca21-146">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
