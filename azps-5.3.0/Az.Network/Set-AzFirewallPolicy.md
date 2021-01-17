---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
ms.openlocfilehash: 3cffe65b1b8e4ba811ee00b7537dc95d9d6dfb72
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436302"
---
# <span data-ttu-id="62d82-101">Set-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="62d82-101">Set-AzFirewallPolicy</span></span>

## <span data-ttu-id="62d82-102">摘要</span><span class="sxs-lookup"><span data-stu-id="62d82-102">SYNOPSIS</span></span>
<span data-ttu-id="62d82-103">儲存已修改的 azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="62d82-103">Saves a modified azure firewall policy</span></span>

## <span data-ttu-id="62d82-104">句法</span><span class="sxs-lookup"><span data-stu-id="62d82-104">SYNTAX</span></span>

### <span data-ttu-id="62d82-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="62d82-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62d82-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="62d82-106">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicy [-Name <String>] -InputObject <PSAzureFirewallPolicy> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Location <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62d82-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62d82-107">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicy [-AsJob] -ResourceId <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62d82-108">說明</span><span class="sxs-lookup"><span data-stu-id="62d82-108">DESCRIPTION</span></span>
<span data-ttu-id="62d82-109">**AzFirewallPolicy** Cmdlet 會更新 Azure 防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="62d82-109">The **Set-AzFirewallPolicy** cmdlet updates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="62d82-110">示例</span><span class="sxs-lookup"><span data-stu-id="62d82-110">EXAMPLES</span></span>

### <span data-ttu-id="62d82-111">範例1</span><span class="sxs-lookup"><span data-stu-id="62d82-111">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="62d82-112">這個範例會將防火牆原則設定為新的防火牆原則值</span><span class="sxs-lookup"><span data-stu-id="62d82-112">This example sets the firewall policy with the new firewall policy value</span></span>

### <span data-ttu-id="62d82-113">範例2</span><span class="sxs-lookup"><span data-stu-id="62d82-113">Example 2</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelMode "Alert"
```

<span data-ttu-id="62d82-114">這個範例會將防火牆原則設定為新的威脅（英特爾）模式</span><span class="sxs-lookup"><span data-stu-id="62d82-114">This example sets the firewall policy with the new threat intel mode</span></span>

### <span data-ttu-id="62d82-115">範例3</span><span class="sxs-lookup"><span data-stu-id="62d82-115">Example 3</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="62d82-116">這個範例會設定防火牆原則與新的威脅英特爾白名單</span><span class="sxs-lookup"><span data-stu-id="62d82-116">This example sets the firewall policy with the new threat intel whitelist</span></span>

## <span data-ttu-id="62d82-117">參數</span><span class="sxs-lookup"><span data-stu-id="62d82-117">PARAMETERS</span></span>

### <span data-ttu-id="62d82-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62d82-118">-AsJob</span></span>
<span data-ttu-id="62d82-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="62d82-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="62d82-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="62d82-120">-BasePolicy</span></span>
<span data-ttu-id="62d82-121">要從其繼承的基本原則</span><span class="sxs-lookup"><span data-stu-id="62d82-121">The base policy to inherit from</span></span>

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

### <span data-ttu-id="62d82-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62d82-122">-DefaultProfile</span></span>
<span data-ttu-id="62d82-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="62d82-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62d82-124">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="62d82-124">-DnsSetting</span></span>
<span data-ttu-id="62d82-125">DNS 設定</span><span class="sxs-lookup"><span data-stu-id="62d82-125">The DNS Setting</span></span>

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

### <span data-ttu-id="62d82-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62d82-126">-InputObject</span></span>
<span data-ttu-id="62d82-127">AzureFirewall 原則</span><span class="sxs-lookup"><span data-stu-id="62d82-127">The AzureFirewall Policy</span></span>

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

### <span data-ttu-id="62d82-128">-位置</span><span class="sxs-lookup"><span data-stu-id="62d82-128">-Location</span></span>
<span data-ttu-id="62d82-129">位於.</span><span class="sxs-lookup"><span data-stu-id="62d82-129">location.</span></span>

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

### <span data-ttu-id="62d82-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="62d82-130">-Name</span></span>
<span data-ttu-id="62d82-131">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="62d82-131">The resource name.</span></span>

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

### <span data-ttu-id="62d82-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62d82-132">-ResourceGroupName</span></span>
<span data-ttu-id="62d82-133">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="62d82-133">The resource group name.</span></span>

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

### <span data-ttu-id="62d82-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62d82-134">-ResourceId</span></span>
<span data-ttu-id="62d82-135">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="62d82-135">The resource Id.</span></span>

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

### <span data-ttu-id="62d82-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="62d82-136">-Tag</span></span>
<span data-ttu-id="62d82-137">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="62d82-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="62d82-138">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="62d82-138">-ThreatIntelMode</span></span>
<span data-ttu-id="62d82-139">威脅情報的操作模式。</span><span class="sxs-lookup"><span data-stu-id="62d82-139">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="62d82-140">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="62d82-140">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="62d82-141">威脅情報的白名單</span><span class="sxs-lookup"><span data-stu-id="62d82-141">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="62d82-142">-確認</span><span class="sxs-lookup"><span data-stu-id="62d82-142">-Confirm</span></span>
<span data-ttu-id="62d82-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="62d82-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62d82-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62d82-144">-WhatIf</span></span>
<span data-ttu-id="62d82-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="62d82-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62d82-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="62d82-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62d82-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62d82-147">CommonParameters</span></span>
<span data-ttu-id="62d82-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="62d82-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62d82-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="62d82-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62d82-150">輸入</span><span class="sxs-lookup"><span data-stu-id="62d82-150">INPUTS</span></span>

### <span data-ttu-id="62d82-151">System.object</span><span class="sxs-lookup"><span data-stu-id="62d82-151">System.String</span></span>

### <span data-ttu-id="62d82-152">PSAzureFirewallPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="62d82-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="62d82-153">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="62d82-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="62d82-154">輸出</span><span class="sxs-lookup"><span data-stu-id="62d82-154">OUTPUTS</span></span>

### <span data-ttu-id="62d82-155">PSAzureFirewall 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="62d82-155">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="62d82-156">筆記</span><span class="sxs-lookup"><span data-stu-id="62d82-156">NOTES</span></span>

## <span data-ttu-id="62d82-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="62d82-157">RELATED LINKS</span></span>
