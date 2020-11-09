---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 17aea8ab38582373420107df87e2b6837a83a1a4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286916"
---
# <span data-ttu-id="b05b1-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b05b1-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="b05b1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b05b1-102">SYNOPSIS</span></span>
<span data-ttu-id="b05b1-103">建立新的 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="b05b1-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="b05b1-104">句法</span><span class="sxs-lookup"><span data-stu-id="b05b1-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b05b1-105">說明</span><span class="sxs-lookup"><span data-stu-id="b05b1-105">DESCRIPTION</span></span>
<span data-ttu-id="b05b1-106">**新的-AzFirewallPolicy** Cmdlet 會建立 Azure 防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="b05b1-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="b05b1-107">示例</span><span class="sxs-lookup"><span data-stu-id="b05b1-107">EXAMPLES</span></span>

### <span data-ttu-id="b05b1-108">範例 1: 1。</span><span class="sxs-lookup"><span data-stu-id="b05b1-108">Example 1: 1.</span></span> <span data-ttu-id="b05b1-109">建立空白原則</span><span class="sxs-lookup"><span data-stu-id="b05b1-109">Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="b05b1-110">這個範例會建立 azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="b05b1-110">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="b05b1-111">範例 2: 2。</span><span class="sxs-lookup"><span data-stu-id="b05b1-111">Example 2: 2.</span></span> <span data-ttu-id="b05b1-112">使用 ThreatIntel 模式建立空原則</span><span class="sxs-lookup"><span data-stu-id="b05b1-112">Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="b05b1-113">這個範例會建立含威脅英特爾模式的 azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="b05b1-113">This example creates an azure firewall policy with a threat intel mode</span></span>

### <span data-ttu-id="b05b1-114">範例 3: 3。</span><span class="sxs-lookup"><span data-stu-id="b05b1-114">Example 3: 3.</span></span> <span data-ttu-id="b05b1-115">使用 ThreatIntel 白名單建立空白原則</span><span class="sxs-lookup"><span data-stu-id="b05b1-115">Create an empty policy with ThreatIntel Whitelist</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="b05b1-116">這個範例會建立一個含有威脅英特爾白名單的 azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="b05b1-116">This example creates an azure firewall policy with a threat intel whitelist</span></span>

## <span data-ttu-id="b05b1-117">參數</span><span class="sxs-lookup"><span data-stu-id="b05b1-117">PARAMETERS</span></span>

### <span data-ttu-id="b05b1-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b05b1-118">-AsJob</span></span>
<span data-ttu-id="b05b1-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b05b1-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b05b1-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="b05b1-120">-BasePolicy</span></span>
<span data-ttu-id="b05b1-121">要從其繼承的基本原則</span><span class="sxs-lookup"><span data-stu-id="b05b1-121">The base policy to inherit from</span></span>

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

### <span data-ttu-id="b05b1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b05b1-122">-DefaultProfile</span></span>
<span data-ttu-id="b05b1-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b05b1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b05b1-124">-Force</span><span class="sxs-lookup"><span data-stu-id="b05b1-124">-Force</span></span>
<span data-ttu-id="b05b1-125">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="b05b1-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b05b1-126">-位置</span><span class="sxs-lookup"><span data-stu-id="b05b1-126">-Location</span></span>
<span data-ttu-id="b05b1-127">位於.</span><span class="sxs-lookup"><span data-stu-id="b05b1-127">location.</span></span>

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

### <span data-ttu-id="b05b1-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="b05b1-128">-Name</span></span>
<span data-ttu-id="b05b1-129">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="b05b1-129">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b05b1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b05b1-130">-ResourceGroupName</span></span>
<span data-ttu-id="b05b1-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b05b1-131">The resource group name.</span></span>

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

### <span data-ttu-id="b05b1-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="b05b1-132">-Tag</span></span>
<span data-ttu-id="b05b1-133">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="b05b1-133">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b05b1-134">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="b05b1-134">-ThreatIntelMode</span></span>
<span data-ttu-id="b05b1-135">威脅情報的操作模式。</span><span class="sxs-lookup"><span data-stu-id="b05b1-135">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="b05b1-136">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="b05b1-136">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="b05b1-137">威脅情報的白名單</span><span class="sxs-lookup"><span data-stu-id="b05b1-137">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="b05b1-138">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="b05b1-138">-DnsSetting</span></span>
<span data-ttu-id="b05b1-139">DNS 設定</span><span class="sxs-lookup"><span data-stu-id="b05b1-139">The DNS Setting</span></span>

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

### <span data-ttu-id="b05b1-140">-確認</span><span class="sxs-lookup"><span data-stu-id="b05b1-140">-Confirm</span></span>
<span data-ttu-id="b05b1-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b05b1-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b05b1-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b05b1-142">-WhatIf</span></span>
<span data-ttu-id="b05b1-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b05b1-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b05b1-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b05b1-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b05b1-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b05b1-145">CommonParameters</span></span>
<span data-ttu-id="b05b1-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b05b1-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b05b1-147">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b05b1-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b05b1-148">輸入</span><span class="sxs-lookup"><span data-stu-id="b05b1-148">INPUTS</span></span>

### <span data-ttu-id="b05b1-149">System.object</span><span class="sxs-lookup"><span data-stu-id="b05b1-149">System.String</span></span>

### <span data-ttu-id="b05b1-150">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b05b1-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b05b1-151">輸出</span><span class="sxs-lookup"><span data-stu-id="b05b1-151">OUTPUTS</span></span>

### <span data-ttu-id="b05b1-152">PSAzureFirewall 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b05b1-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="b05b1-153">筆記</span><span class="sxs-lookup"><span data-stu-id="b05b1-153">NOTES</span></span>

## <span data-ttu-id="b05b1-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="b05b1-154">RELATED LINKS</span></span>
