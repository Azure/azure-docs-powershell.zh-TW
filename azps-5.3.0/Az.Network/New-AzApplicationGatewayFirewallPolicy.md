---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 03e03de70f61672d1246ffeb8469efe0c04b3ea4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98287004"
---
# <span data-ttu-id="bfefa-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="bfefa-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="bfefa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bfefa-102">SYNOPSIS</span></span>
<span data-ttu-id="bfefa-103">建立應用程式閘道防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="bfefa-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="bfefa-104">句法</span><span class="sxs-lookup"><span data-stu-id="bfefa-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfefa-105">說明</span><span class="sxs-lookup"><span data-stu-id="bfefa-105">DESCRIPTION</span></span>
<span data-ttu-id="bfefa-106">**新的-AzApplicationGatewayFirewallPolicy** Cmdlet 會建立應用程式閘道防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="bfefa-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="bfefa-107">示例</span><span class="sxs-lookup"><span data-stu-id="bfefa-107">EXAMPLES</span></span>

### <span data-ttu-id="bfefa-108">範例1</span><span class="sxs-lookup"><span data-stu-id="bfefa-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRule $customRule
```

<span data-ttu-id="bfefa-109">這個命令會在位置 "westus" 的資源群組 "rg1" 中，建立名為 "wafResource1" 的新 Azure 應用程式閘道防火牆原則，並在 $customRule 變數中定義的自訂規則</span><span class="sxs-lookup"><span data-stu-id="bfefa-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="bfefa-110">參數</span><span class="sxs-lookup"><span data-stu-id="bfefa-110">PARAMETERS</span></span>

### <span data-ttu-id="bfefa-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bfefa-111">-AsJob</span></span>
<span data-ttu-id="bfefa-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="bfefa-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bfefa-113">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="bfefa-113">-CustomRule</span></span>
<span data-ttu-id="bfefa-114">CustomRules 清單</span><span class="sxs-lookup"><span data-stu-id="bfefa-114">The list of CustomRules</span></span>

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

### <span data-ttu-id="bfefa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfefa-115">-DefaultProfile</span></span>
<span data-ttu-id="bfefa-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bfefa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfefa-117">-Force</span><span class="sxs-lookup"><span data-stu-id="bfefa-117">-Force</span></span>
<span data-ttu-id="bfefa-118">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="bfefa-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="bfefa-119">-位置</span><span class="sxs-lookup"><span data-stu-id="bfefa-119">-Location</span></span>
<span data-ttu-id="bfefa-120">位於.</span><span class="sxs-lookup"><span data-stu-id="bfefa-120">location.</span></span>

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

### <span data-ttu-id="bfefa-121">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="bfefa-121">-ManagedRule</span></span>
<span data-ttu-id="bfefa-122">受管理規則設定</span><span class="sxs-lookup"><span data-stu-id="bfefa-122">Managed Rule Setting</span></span>

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

### <span data-ttu-id="bfefa-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="bfefa-123">-Name</span></span>
<span data-ttu-id="bfefa-124">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="bfefa-124">The resource name.</span></span>

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

### <span data-ttu-id="bfefa-125">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="bfefa-125">-PolicySetting</span></span>
<span data-ttu-id="bfefa-126">Web 應用程式防火牆的原則設定</span><span class="sxs-lookup"><span data-stu-id="bfefa-126">Policy Settings for Web Application Firewall</span></span>

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

### <span data-ttu-id="bfefa-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfefa-127">-ResourceGroupName</span></span>
<span data-ttu-id="bfefa-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bfefa-128">The resource group name.</span></span>

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

### <span data-ttu-id="bfefa-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="bfefa-129">-Tag</span></span>
<span data-ttu-id="bfefa-130">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="bfefa-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="bfefa-131">-確認</span><span class="sxs-lookup"><span data-stu-id="bfefa-131">-Confirm</span></span>
<span data-ttu-id="bfefa-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bfefa-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfefa-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfefa-133">-WhatIf</span></span>
<span data-ttu-id="bfefa-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bfefa-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfefa-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bfefa-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfefa-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfefa-136">CommonParameters</span></span>
<span data-ttu-id="bfefa-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bfefa-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfefa-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bfefa-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfefa-139">輸入</span><span class="sxs-lookup"><span data-stu-id="bfefa-139">INPUTS</span></span>

### <span data-ttu-id="bfefa-140">System.object</span><span class="sxs-lookup"><span data-stu-id="bfefa-140">System.String</span></span>

### <span data-ttu-id="bfefa-141">PSApplicationGatewayFirewallCustomRule [] （[]）</span><span class="sxs-lookup"><span data-stu-id="bfefa-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="bfefa-142">PSApplicationGatewayFirewallPolicySettings 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bfefa-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

### <span data-ttu-id="bfefa-143">PSApplicationGatewayFirewallPolicyManagedRules 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bfefa-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

### <span data-ttu-id="bfefa-144">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bfefa-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bfefa-145">輸出</span><span class="sxs-lookup"><span data-stu-id="bfefa-145">OUTPUTS</span></span>

### <span data-ttu-id="bfefa-146">PSApplicationGatewayWebApplicationFirewallPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bfefa-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="bfefa-147">筆記</span><span class="sxs-lookup"><span data-stu-id="bfefa-147">NOTES</span></span>

## <span data-ttu-id="bfefa-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="bfefa-148">RELATED LINKS</span></span>
