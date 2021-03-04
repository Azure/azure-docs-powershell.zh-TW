---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
ms.openlocfilehash: af892ca6698cb51a16c9e6ec1784c48c9bb19b53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913690"
---
# <span data-ttu-id="38e79-101">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="38e79-101">New-AzFirewallApplicationRule</span></span>

## <span data-ttu-id="38e79-102">簡介</span><span class="sxs-lookup"><span data-stu-id="38e79-102">SYNOPSIS</span></span>
<span data-ttu-id="38e79-103">建立防火牆應用程式規則。</span><span class="sxs-lookup"><span data-stu-id="38e79-103">Creates a Firewall Application Rule.</span></span>

## <span data-ttu-id="38e79-104">語法</span><span class="sxs-lookup"><span data-stu-id="38e79-104">SYNTAX</span></span>

### <span data-ttu-id="38e79-105">TargetFqdn (預設) </span><span class="sxs-lookup"><span data-stu-id="38e79-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -TargetFqdn <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38e79-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="38e79-106">FqdnTag</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38e79-107">描述</span><span class="sxs-lookup"><span data-stu-id="38e79-107">DESCRIPTION</span></span>
<span data-ttu-id="38e79-108">**New-AzFirewallApplicationRule** Cmdlet 會建立 Azure 防火牆的應用程式規則。</span><span class="sxs-lookup"><span data-stu-id="38e79-108">The **New-AzFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="38e79-109">例子</span><span class="sxs-lookup"><span data-stu-id="38e79-109">EXAMPLES</span></span>

### <span data-ttu-id="38e79-110">範例 1：建立規則以允許來自 10.0.0.0 的所有 HTTPS 流量</span><span class="sxs-lookup"><span data-stu-id="38e79-110">Example 1: Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```powershell
New-AzFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="38e79-111">此範例會建立一個規則，允許埠 443 上的所有 HTTPS 流量從 10.0.0.0。</span><span class="sxs-lookup"><span data-stu-id="38e79-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="38e79-112">範例 2：建立規則以允許 10.0.0.0/24 子網使用 WindowsUpdate</span><span class="sxs-lookup"><span data-stu-id="38e79-112">Example 2: Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```powershell
New-AzFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="38e79-113">此範例會建立一個規則，允許 10.0.0.0/24 網域的 Windows Updates 流量。</span><span class="sxs-lookup"><span data-stu-id="38e79-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="38e79-114">參數</span><span class="sxs-lookup"><span data-stu-id="38e79-114">PARAMETERS</span></span>

### <span data-ttu-id="38e79-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38e79-115">-DefaultProfile</span></span>
<span data-ttu-id="38e79-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="38e79-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38e79-117">-描述</span><span class="sxs-lookup"><span data-stu-id="38e79-117">-Description</span></span>
<span data-ttu-id="38e79-118">指定此規則的選擇性描述。</span><span class="sxs-lookup"><span data-stu-id="38e79-118">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="38e79-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="38e79-119">-FqdnTag</span></span>
<span data-ttu-id="38e79-120">指定此規則的 FQDN 標記清單。</span><span class="sxs-lookup"><span data-stu-id="38e79-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="38e79-121">您可以使用 [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) Cmdlet 來取回可用的標籤。</span><span class="sxs-lookup"><span data-stu-id="38e79-121">The available tags can be retrieved using [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) cmdlet.</span></span>

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

### <span data-ttu-id="38e79-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="38e79-122">-Name</span></span>
<span data-ttu-id="38e79-123">指定此應用程式規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="38e79-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="38e79-124">名稱必須在規則集合中是唯一的。</span><span class="sxs-lookup"><span data-stu-id="38e79-124">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="38e79-125">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="38e79-125">-Protocol</span></span>
<span data-ttu-id="38e79-126">指定此規則要篩選的流量類型。</span><span class="sxs-lookup"><span data-stu-id="38e79-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="38e79-127">格式為 <protocol type> ： <port> .</span><span class="sxs-lookup"><span data-stu-id="38e79-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="38e79-128">例如，"HTTP：80" 或 "HTTPs：443"。</span><span class="sxs-lookup"><span data-stu-id="38e79-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="38e79-129">使用 TargetFqdn 時，通訊協定為必填專案，但無法與 FqdnTag 一起使用。</span><span class="sxs-lookup"><span data-stu-id="38e79-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="38e79-130">支援的通訊協定為 HTTP 和 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="38e79-130">The supported protocols are HTTP and HTTPS.</span></span>

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

### <span data-ttu-id="38e79-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="38e79-131">-SourceAddress</span></span>
<span data-ttu-id="38e79-132">規則的來源位址</span><span class="sxs-lookup"><span data-stu-id="38e79-132">The source addresses of the rule</span></span>

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

### <span data-ttu-id="38e79-133">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="38e79-133">-SourceIpGroup</span></span>
<span data-ttu-id="38e79-134">規則的來源 ipgroup</span><span class="sxs-lookup"><span data-stu-id="38e79-134">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="38e79-135">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="38e79-135">-TargetFqdn</span></span>
<span data-ttu-id="38e79-136">指定依此規則篩選的功能變數名稱清單。</span><span class="sxs-lookup"><span data-stu-id="38e79-136">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="38e79-137">星號 '' 字元僅接受做為 *清單中 FQDN 的第一個字元。使用時，星號會比對任意數目的字元。 (例如'msn.com'* 會符合msn.com及其所有子域) </span><span class="sxs-lookup"><span data-stu-id="38e79-137">The asterisk character, '*', is accepted only as the first character of an FQDN in the list. When used, the asterisk matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

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

### <span data-ttu-id="38e79-138">-確認</span><span class="sxs-lookup"><span data-stu-id="38e79-138">-Confirm</span></span>
<span data-ttu-id="38e79-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="38e79-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38e79-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38e79-140">-WhatIf</span></span>
<span data-ttu-id="38e79-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="38e79-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38e79-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="38e79-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38e79-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38e79-143">CommonParameters</span></span>
<span data-ttu-id="38e79-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="38e79-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38e79-145">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="38e79-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38e79-146">輸入</span><span class="sxs-lookup"><span data-stu-id="38e79-146">INPUTS</span></span>

### <span data-ttu-id="38e79-147">沒有</span><span class="sxs-lookup"><span data-stu-id="38e79-147">None</span></span>

## <span data-ttu-id="38e79-148">輸出</span><span class="sxs-lookup"><span data-stu-id="38e79-148">OUTPUTS</span></span>

### <span data-ttu-id="38e79-149">Microsoft.Azure.Commands.Network.models.PSAzureFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="38e79-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule</span></span>

## <span data-ttu-id="38e79-150">筆記</span><span class="sxs-lookup"><span data-stu-id="38e79-150">NOTES</span></span>

## <span data-ttu-id="38e79-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="38e79-151">RELATED LINKS</span></span>

[<span data-ttu-id="38e79-152">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="38e79-152">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="38e79-153">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="38e79-153">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="38e79-154">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="38e79-154">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="38e79-155">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="38e79-155">Get-AzFirewallFqdnTag</span></span>](./Get-AzFirewallFqdnTag.md)
