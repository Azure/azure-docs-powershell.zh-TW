---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
ms.openlocfilehash: 6aad78a873b1eb24f1534c9b8c0b38d1567ee2ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621790"
---
# <span data-ttu-id="95197-101">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="95197-101">New-AzFirewallApplicationRule</span></span>

## <span data-ttu-id="95197-102">摘要</span><span class="sxs-lookup"><span data-stu-id="95197-102">SYNOPSIS</span></span>
<span data-ttu-id="95197-103">建立防火牆應用程式規則。</span><span class="sxs-lookup"><span data-stu-id="95197-103">Creates a Firewall Application Rule.</span></span>

## <span data-ttu-id="95197-104">句法</span><span class="sxs-lookup"><span data-stu-id="95197-104">SYNTAX</span></span>

### <span data-ttu-id="95197-105">TargetFqdn (預設) </span><span class="sxs-lookup"><span data-stu-id="95197-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95197-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="95197-106">FqdnTag</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95197-107">說明</span><span class="sxs-lookup"><span data-stu-id="95197-107">DESCRIPTION</span></span>
<span data-ttu-id="95197-108">**新的-AzFirewallApplicationRule** Cmdlet 會建立 Azure 防火牆的應用程式規則。</span><span class="sxs-lookup"><span data-stu-id="95197-108">The **New-AzFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="95197-109">示例</span><span class="sxs-lookup"><span data-stu-id="95197-109">EXAMPLES</span></span>

### <span data-ttu-id="95197-110">1：建立規則以允許所有來自10.0.0.0 的 HTTPS 流量</span><span class="sxs-lookup"><span data-stu-id="95197-110">1:  Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```
New-AzFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="95197-111">這個範例會建立一個規則，讓埠443上的所有 HTTPS 流量都是10.0.0.0。</span><span class="sxs-lookup"><span data-stu-id="95197-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="95197-112">2：建立規則，允許 WindowsUpdate for 10.0.0.0/24 子網</span><span class="sxs-lookup"><span data-stu-id="95197-112">2:  Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```
New-AzFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="95197-113">這個範例會建立一條規則，以允許針對 10.0.0.0/24 網域的 Windows 更新進行通訊。</span><span class="sxs-lookup"><span data-stu-id="95197-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="95197-114">參數</span><span class="sxs-lookup"><span data-stu-id="95197-114">PARAMETERS</span></span>

### <span data-ttu-id="95197-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95197-115">-DefaultProfile</span></span>
<span data-ttu-id="95197-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="95197-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95197-117">-描述</span><span class="sxs-lookup"><span data-stu-id="95197-117">-Description</span></span>
<span data-ttu-id="95197-118">指定此規則的選擇性描述。</span><span class="sxs-lookup"><span data-stu-id="95197-118">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="95197-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="95197-119">-FqdnTag</span></span>
<span data-ttu-id="95197-120">指定此規則的 FQDN 標記清單。</span><span class="sxs-lookup"><span data-stu-id="95197-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="95197-121">您可以使用 [AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) Cmdlet 來檢索可用的標記。</span><span class="sxs-lookup"><span data-stu-id="95197-121">The available tags can be retrieved using [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) cmdlet.</span></span>

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

### <span data-ttu-id="95197-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="95197-122">-Name</span></span>
<span data-ttu-id="95197-123">指定此應用程式規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="95197-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="95197-124">該名稱在規則集合內必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="95197-124">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="95197-125">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="95197-125">-Protocol</span></span>
<span data-ttu-id="95197-126">指定要依據此規則篩選的流量類型。</span><span class="sxs-lookup"><span data-stu-id="95197-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="95197-127">格式為 <protocol type> ： <port> 。</span><span class="sxs-lookup"><span data-stu-id="95197-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="95197-128">例如，"HTTP： 80" 或 "HTTPs： 443"。</span><span class="sxs-lookup"><span data-stu-id="95197-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="95197-129">使用 TargetFqdn 時，通訊協定是強制性的，但無法與 FqdnTag 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="95197-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="95197-130">支援的通訊協定為 HTTP 和 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="95197-130">The supported protocols are HTTP and HTTPS.</span></span>

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

### <span data-ttu-id="95197-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="95197-131">-SourceAddress</span></span>
<span data-ttu-id="95197-132">規則的來源位址</span><span class="sxs-lookup"><span data-stu-id="95197-132">The source addresses of the rule</span></span>

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

### <span data-ttu-id="95197-133">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="95197-133">-TargetFqdn</span></span>
<span data-ttu-id="95197-134">指定此規則所篩選之功能變數名稱的清單。</span><span class="sxs-lookup"><span data-stu-id="95197-134">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="95197-135">水平線字元 " *" 只接受清單中 FQDN 的第一個字元。當使用時，水平線會與任何數目的字元相符。 (例如，"* msn.com" 將會與 msn.com 及其所有) 子域相符。</span><span class="sxs-lookup"><span data-stu-id="95197-135">The asterik character, ' *', is accepted only as the first character of an FQDN in the list. When used, the asterik matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

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

### <span data-ttu-id="95197-136">-確認</span><span class="sxs-lookup"><span data-stu-id="95197-136">-Confirm</span></span>
<span data-ttu-id="95197-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="95197-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95197-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95197-138">-WhatIf</span></span>
<span data-ttu-id="95197-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="95197-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95197-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95197-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95197-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95197-141">CommonParameters</span></span>
<span data-ttu-id="95197-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="95197-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95197-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="95197-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95197-144">輸入</span><span class="sxs-lookup"><span data-stu-id="95197-144">INPUTS</span></span>

### <span data-ttu-id="95197-145">所有</span><span class="sxs-lookup"><span data-stu-id="95197-145">None</span></span>

## <span data-ttu-id="95197-146">輸出</span><span class="sxs-lookup"><span data-stu-id="95197-146">OUTPUTS</span></span>

### <span data-ttu-id="95197-147">PSAzureFirewallApplicationRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="95197-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule</span></span>

## <span data-ttu-id="95197-148">筆記</span><span class="sxs-lookup"><span data-stu-id="95197-148">NOTES</span></span>

## <span data-ttu-id="95197-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="95197-149">RELATED LINKS</span></span>

[<span data-ttu-id="95197-150">新-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="95197-150">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="95197-151">新-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="95197-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="95197-152">AzFirewall</span><span class="sxs-lookup"><span data-stu-id="95197-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="95197-153">AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="95197-153">Get-AzFirewallFqdnTag</span></span>](./Get-AzFirewallFqdnTag.md)
