---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
ms.openlocfilehash: d5c3a560f0afcfb28224cf4681af78d6bd5249ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133858"
---
# <span data-ttu-id="9515f-101">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="9515f-101">New-AzFirewallApplicationRule</span></span>

## <span data-ttu-id="9515f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9515f-102">SYNOPSIS</span></span>
<span data-ttu-id="9515f-103">建立防火牆應用程式規則。</span><span class="sxs-lookup"><span data-stu-id="9515f-103">Creates a Firewall Application Rule.</span></span>

## <span data-ttu-id="9515f-104">句法</span><span class="sxs-lookup"><span data-stu-id="9515f-104">SYNTAX</span></span>

### <span data-ttu-id="9515f-105">TargetFqdn (預設) </span><span class="sxs-lookup"><span data-stu-id="9515f-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -TargetFqdn <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9515f-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="9515f-106">FqdnTag</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9515f-107">說明</span><span class="sxs-lookup"><span data-stu-id="9515f-107">DESCRIPTION</span></span>
<span data-ttu-id="9515f-108">**新的-AzFirewallApplicationRule** Cmdlet 會建立 Azure 防火牆的應用程式規則。</span><span class="sxs-lookup"><span data-stu-id="9515f-108">The **New-AzFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="9515f-109">示例</span><span class="sxs-lookup"><span data-stu-id="9515f-109">EXAMPLES</span></span>

### <span data-ttu-id="9515f-110">範例1：建立規則以允許所有來自10.0.0.0 的 HTTPS 流量</span><span class="sxs-lookup"><span data-stu-id="9515f-110">Example 1: Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```powershell
New-AzFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="9515f-111">這個範例會建立一個規則，讓埠443上的所有 HTTPS 流量都是10.0.0.0。</span><span class="sxs-lookup"><span data-stu-id="9515f-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="9515f-112">範例2：建立規則以允許 WindowsUpdate for 10.0.0.0/24 子網</span><span class="sxs-lookup"><span data-stu-id="9515f-112">Example 2: Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```powershell
New-AzFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="9515f-113">這個範例會建立一條規則，以允許針對 10.0.0.0/24 網域的 Windows 更新進行通訊。</span><span class="sxs-lookup"><span data-stu-id="9515f-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="9515f-114">參數</span><span class="sxs-lookup"><span data-stu-id="9515f-114">PARAMETERS</span></span>

### <span data-ttu-id="9515f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9515f-115">-DefaultProfile</span></span>
<span data-ttu-id="9515f-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9515f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9515f-117">-描述</span><span class="sxs-lookup"><span data-stu-id="9515f-117">-Description</span></span>
<span data-ttu-id="9515f-118">指定此規則的選擇性描述。</span><span class="sxs-lookup"><span data-stu-id="9515f-118">Specifies an optional description of this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9515f-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="9515f-119">-FqdnTag</span></span>
<span data-ttu-id="9515f-120">指定此規則的 FQDN 標記清單。</span><span class="sxs-lookup"><span data-stu-id="9515f-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="9515f-121">您可以使用 [AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) Cmdlet 來檢索可用的標記。</span><span class="sxs-lookup"><span data-stu-id="9515f-121">The available tags can be retrieved using [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) cmdlet.</span></span>

```yaml
Type: System.String[]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9515f-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="9515f-122">-Name</span></span>
<span data-ttu-id="9515f-123">指定此應用程式規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="9515f-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="9515f-124">該名稱在規則集合內必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="9515f-124">The name must be unique inside a rule collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9515f-125">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="9515f-125">-Protocol</span></span>
<span data-ttu-id="9515f-126">指定要依據此規則篩選的流量類型。</span><span class="sxs-lookup"><span data-stu-id="9515f-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="9515f-127">格式為 <protocol type> ： <port> 。</span><span class="sxs-lookup"><span data-stu-id="9515f-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="9515f-128">例如，"HTTP： 80" 或 "HTTPs： 443"。</span><span class="sxs-lookup"><span data-stu-id="9515f-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="9515f-129">使用 TargetFqdn 時，通訊協定是強制性的，但無法與 FqdnTag 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="9515f-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="9515f-130">支援的通訊協定為 HTTP 和 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="9515f-130">The supported protocols are HTTP and HTTPS.</span></span>

```yaml
Type: System.String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9515f-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="9515f-131">-SourceAddress</span></span>
<span data-ttu-id="9515f-132">規則的來源位址</span><span class="sxs-lookup"><span data-stu-id="9515f-132">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9515f-133">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="9515f-133">-SourceIpGroup</span></span>
<span data-ttu-id="9515f-134">規則的來源 ipgroup</span><span class="sxs-lookup"><span data-stu-id="9515f-134">The source ipgroup of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9515f-135">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="9515f-135">-TargetFqdn</span></span>
<span data-ttu-id="9515f-136">指定此規則所篩選之功能變數名稱的清單。</span><span class="sxs-lookup"><span data-stu-id="9515f-136">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="9515f-137">星號字元 ""*只接受為清單中 FQDN 的第一個字元。當使用時，星號會與任何數目的字元相符。 (例如，"* msn.com" 將會與 msn.com 及其所有) 子域相符。</span><span class="sxs-lookup"><span data-stu-id="9515f-137">The asterisk character, '*', is accepted only as the first character of an FQDN in the list. When used, the asterisk matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

```yaml
Type: System.String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9515f-138">-確認</span><span class="sxs-lookup"><span data-stu-id="9515f-138">-Confirm</span></span>
<span data-ttu-id="9515f-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9515f-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9515f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9515f-140">-WhatIf</span></span>
<span data-ttu-id="9515f-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9515f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9515f-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9515f-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9515f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9515f-143">CommonParameters</span></span>
<span data-ttu-id="9515f-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9515f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9515f-145">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9515f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9515f-146">輸入</span><span class="sxs-lookup"><span data-stu-id="9515f-146">INPUTS</span></span>

### <span data-ttu-id="9515f-147">所有</span><span class="sxs-lookup"><span data-stu-id="9515f-147">None</span></span>

## <span data-ttu-id="9515f-148">輸出</span><span class="sxs-lookup"><span data-stu-id="9515f-148">OUTPUTS</span></span>

### <span data-ttu-id="9515f-149">PSAzureFirewallApplicationRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9515f-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule</span></span>

## <span data-ttu-id="9515f-150">筆記</span><span class="sxs-lookup"><span data-stu-id="9515f-150">NOTES</span></span>

## <span data-ttu-id="9515f-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="9515f-151">RELATED LINKS</span></span>

[<span data-ttu-id="9515f-152">新-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="9515f-152">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="9515f-153">新-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="9515f-153">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="9515f-154">AzFirewall</span><span class="sxs-lookup"><span data-stu-id="9515f-154">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="9515f-155">AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="9515f-155">Get-AzFirewallFqdnTag</span></span>](./Get-AzFirewallFqdnTag.md)
