---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
ms.openlocfilehash: 4e328d28ebe7faafa942d4f3448108a174f2aa71
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902846"
---
# <span data-ttu-id="1e913-101">Set-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="1e913-101">Set-AzFirewallPolicy</span></span>

## <span data-ttu-id="1e913-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1e913-102">SYNOPSIS</span></span>
<span data-ttu-id="1e913-103">會保存已修改的 Azure 防火牆政策</span><span class="sxs-lookup"><span data-stu-id="1e913-103">Saves a modified azure firewall policy</span></span>

## <span data-ttu-id="1e913-104">語法</span><span class="sxs-lookup"><span data-stu-id="1e913-104">SYNTAX</span></span>

### <span data-ttu-id="1e913-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1e913-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e913-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e913-106">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicy [-Name <String>] -InputObject <PSAzureFirewallPolicy> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Location <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e913-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e913-107">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicy [-AsJob] -ResourceId <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e913-108">描述</span><span class="sxs-lookup"><span data-stu-id="1e913-108">DESCRIPTION</span></span>
<span data-ttu-id="1e913-109">**Set-AzFirewallPolicy** Cmdlet 會更新 Azure 防火牆政策。</span><span class="sxs-lookup"><span data-stu-id="1e913-109">The **Set-AzFirewallPolicy** cmdlet updates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="1e913-110">例子</span><span class="sxs-lookup"><span data-stu-id="1e913-110">EXAMPLES</span></span>

### <span data-ttu-id="1e913-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="1e913-111">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="1e913-112">此範例會以新的防火牆策略值設定防火牆政策</span><span class="sxs-lookup"><span data-stu-id="1e913-112">This example sets the firewall policy with the new firewall policy value</span></span>

### <span data-ttu-id="1e913-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="1e913-113">Example 2</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelMode "Alert"
```

<span data-ttu-id="1e913-114">此範例使用新的威脅 Intel 模式設定防火牆政策</span><span class="sxs-lookup"><span data-stu-id="1e913-114">This example sets the firewall policy with the new threat intel mode</span></span>

### <span data-ttu-id="1e913-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="1e913-115">Example 3</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="1e913-116">此範例使用新的威脅 intel Whitelist 設定防火牆政策</span><span class="sxs-lookup"><span data-stu-id="1e913-116">This example sets the firewall policy with the new threat intel whitelist</span></span>

## <span data-ttu-id="1e913-117">參數</span><span class="sxs-lookup"><span data-stu-id="1e913-117">PARAMETERS</span></span>

### <span data-ttu-id="1e913-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e913-118">-AsJob</span></span>
<span data-ttu-id="1e913-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1e913-119">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e913-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="1e913-120">-BasePolicy</span></span>
<span data-ttu-id="1e913-121">繼承基礎策略</span><span class="sxs-lookup"><span data-stu-id="1e913-121">The base policy to inherit from</span></span>

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

### <span data-ttu-id="1e913-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e913-122">-DefaultProfile</span></span>
<span data-ttu-id="1e913-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1e913-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e913-124">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="1e913-124">-DnsSetting</span></span>
<span data-ttu-id="1e913-125">DNS 設定</span><span class="sxs-lookup"><span data-stu-id="1e913-125">The DNS Setting</span></span>

```yaml
Type: PSAzureFirewallPolicyDnsSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e913-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e913-126">-InputObject</span></span>
<span data-ttu-id="1e913-127">AzureFirewall 政策</span><span class="sxs-lookup"><span data-stu-id="1e913-127">The AzureFirewall Policy</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e913-128">-位置</span><span class="sxs-lookup"><span data-stu-id="1e913-128">-Location</span></span>
<span data-ttu-id="1e913-129">位置。</span><span class="sxs-lookup"><span data-stu-id="1e913-129">location.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e913-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="1e913-130">-Name</span></span>
<span data-ttu-id="1e913-131">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="1e913-131">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e913-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e913-132">-ResourceGroupName</span></span>
<span data-ttu-id="1e913-133">資源組名。</span><span class="sxs-lookup"><span data-stu-id="1e913-133">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e913-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e913-134">-ResourceId</span></span>
<span data-ttu-id="1e913-135">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1e913-135">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e913-136">-標記</span><span class="sxs-lookup"><span data-stu-id="1e913-136">-Tag</span></span>
<span data-ttu-id="1e913-137">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="1e913-137">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e913-138">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="1e913-138">-ThreatIntelMode</span></span>
<span data-ttu-id="1e913-139">威脅情報的作業模式。</span><span class="sxs-lookup"><span data-stu-id="1e913-139">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e913-140">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="1e913-140">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="1e913-141">威脅情報的白名單</span><span class="sxs-lookup"><span data-stu-id="1e913-141">The whitelist for Threat Intelligence</span></span>

```yaml
Type: PSAzureFirewallPolicyThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e913-142">-確認</span><span class="sxs-lookup"><span data-stu-id="1e913-142">-Confirm</span></span>
<span data-ttu-id="1e913-143">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1e913-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e913-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e913-144">-WhatIf</span></span>
<span data-ttu-id="1e913-145">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1e913-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e913-146">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e913-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e913-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e913-147">CommonParameters</span></span>
<span data-ttu-id="1e913-148">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1e913-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e913-149">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e913-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e913-150">輸入</span><span class="sxs-lookup"><span data-stu-id="1e913-150">INPUTS</span></span>

### <span data-ttu-id="1e913-151">System.String</span><span class="sxs-lookup"><span data-stu-id="1e913-151">System.String</span></span>

### <span data-ttu-id="1e913-152">Microsoft.Azure.Commands.Network.models.PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="1e913-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="1e913-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1e913-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1e913-154">輸出</span><span class="sxs-lookup"><span data-stu-id="1e913-154">OUTPUTS</span></span>

### <span data-ttu-id="1e913-155">Microsoft.Azure.Commands.Network.models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="1e913-155">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="1e913-156">筆記</span><span class="sxs-lookup"><span data-stu-id="1e913-156">NOTES</span></span>

## <span data-ttu-id="1e913-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e913-157">RELATED LINKS</span></span>
