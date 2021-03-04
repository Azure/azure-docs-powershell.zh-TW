---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: e643bf488073f6da685265cea4a2a0c6cb7cebf5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906550"
---
# <span data-ttu-id="41807-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="41807-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="41807-102">簡介</span><span class="sxs-lookup"><span data-stu-id="41807-102">SYNOPSIS</span></span>
<span data-ttu-id="41807-103">建立應用程式閘道防火牆策略。</span><span class="sxs-lookup"><span data-stu-id="41807-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="41807-104">語法</span><span class="sxs-lookup"><span data-stu-id="41807-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41807-105">描述</span><span class="sxs-lookup"><span data-stu-id="41807-105">DESCRIPTION</span></span>
<span data-ttu-id="41807-106">**New-AzApplicationGatewayFirewallPolicy** Cmdlet 會建立應用程式閘道防火牆策略。</span><span class="sxs-lookup"><span data-stu-id="41807-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="41807-107">例子</span><span class="sxs-lookup"><span data-stu-id="41807-107">EXAMPLES</span></span>

### <span data-ttu-id="41807-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="41807-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRule $customRule
```

<span data-ttu-id="41807-109">此命令在位置 "westus" 的資源群組 "rg1" 中，使用在 $customRule 變數中定義的自訂規則，建立名為 "wafResource1" 的新 Azure 應用程式閘道防火牆原則</span><span class="sxs-lookup"><span data-stu-id="41807-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="41807-110">參數</span><span class="sxs-lookup"><span data-stu-id="41807-110">PARAMETERS</span></span>

### <span data-ttu-id="41807-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41807-111">-AsJob</span></span>
<span data-ttu-id="41807-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41807-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41807-113">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="41807-113">-CustomRule</span></span>
<span data-ttu-id="41807-114">自訂規則清單</span><span class="sxs-lookup"><span data-stu-id="41807-114">The list of CustomRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41807-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41807-115">-DefaultProfile</span></span>
<span data-ttu-id="41807-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="41807-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41807-117">-強制</span><span class="sxs-lookup"><span data-stu-id="41807-117">-Force</span></span>
<span data-ttu-id="41807-118">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="41807-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="41807-119">-位置</span><span class="sxs-lookup"><span data-stu-id="41807-119">-Location</span></span>
<span data-ttu-id="41807-120">位置。</span><span class="sxs-lookup"><span data-stu-id="41807-120">location.</span></span>

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

### <span data-ttu-id="41807-121">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="41807-121">-ManagedRule</span></span>
<span data-ttu-id="41807-122">受管理規則設定</span><span class="sxs-lookup"><span data-stu-id="41807-122">Managed Rule Setting</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41807-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="41807-123">-Name</span></span>
<span data-ttu-id="41807-124">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="41807-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41807-125">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="41807-125">-PolicySetting</span></span>
<span data-ttu-id="41807-126">Web 應用程式防火牆的設定</span><span class="sxs-lookup"><span data-stu-id="41807-126">Policy Settings for Web Application Firewall</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41807-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41807-127">-ResourceGroupName</span></span>
<span data-ttu-id="41807-128">資源組名。</span><span class="sxs-lookup"><span data-stu-id="41807-128">The resource group name.</span></span>

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

### <span data-ttu-id="41807-129">-標記</span><span class="sxs-lookup"><span data-stu-id="41807-129">-Tag</span></span>
<span data-ttu-id="41807-130">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="41807-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41807-131">-確認</span><span class="sxs-lookup"><span data-stu-id="41807-131">-Confirm</span></span>
<span data-ttu-id="41807-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="41807-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41807-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41807-133">-WhatIf</span></span>
<span data-ttu-id="41807-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="41807-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41807-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41807-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41807-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41807-136">CommonParameters</span></span>
<span data-ttu-id="41807-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="41807-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41807-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41807-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41807-139">輸入</span><span class="sxs-lookup"><span data-stu-id="41807-139">INPUTS</span></span>

### <span data-ttu-id="41807-140">System.String</span><span class="sxs-lookup"><span data-stu-id="41807-140">System.String</span></span>

### <span data-ttu-id="41807-141">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayFirewallCustomRule[]</span><span class="sxs-lookup"><span data-stu-id="41807-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="41807-142">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="41807-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

### <span data-ttu-id="41807-143">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="41807-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

### <span data-ttu-id="41807-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="41807-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="41807-145">輸出</span><span class="sxs-lookup"><span data-stu-id="41807-145">OUTPUTS</span></span>

### <span data-ttu-id="41807-146">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="41807-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="41807-147">筆記</span><span class="sxs-lookup"><span data-stu-id="41807-147">NOTES</span></span>

## <span data-ttu-id="41807-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="41807-148">RELATED LINKS</span></span>
