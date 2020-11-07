---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRule.md
ms.openlocfilehash: 8a59f09184c7042b12abbd549398ca4690ace235
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626062"
---
# <span data-ttu-id="35b11-101">New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="35b11-101">New-AzureRmFirewallApplicationRule</span></span>

## <span data-ttu-id="35b11-102">摘要</span><span class="sxs-lookup"><span data-stu-id="35b11-102">SYNOPSIS</span></span>
<span data-ttu-id="35b11-103">建立防火牆應用程式規則。</span><span class="sxs-lookup"><span data-stu-id="35b11-103">Creates a Firewall Application Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35b11-104">句法</span><span class="sxs-lookup"><span data-stu-id="35b11-104">SYNTAX</span></span>

### <span data-ttu-id="35b11-105">TargetFqdn (預設) </span><span class="sxs-lookup"><span data-stu-id="35b11-105">TargetFqdn (Default)</span></span>
```
New-AzureRmFirewallApplicationRule -Name <String> [-Description <String>]
 [-SourceAddress <System.Collections.Generic.List`1[System.String]>]
 -TargetFqdn <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35b11-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="35b11-106">FqdnTag</span></span>
```
New-AzureRmFirewallApplicationRule -Name <String> [-Description <String>]
 [-SourceAddress <System.Collections.Generic.List`1[System.String]>]
 -FqdnTag <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35b11-107">說明</span><span class="sxs-lookup"><span data-stu-id="35b11-107">DESCRIPTION</span></span>
<span data-ttu-id="35b11-108">**新的-AzureRmFirewallApplicationRule** Cmdlet 會建立 Azure 防火牆的應用程式規則。</span><span class="sxs-lookup"><span data-stu-id="35b11-108">The **New-AzureRmFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="35b11-109">示例</span><span class="sxs-lookup"><span data-stu-id="35b11-109">EXAMPLES</span></span>

### <span data-ttu-id="35b11-110">1：建立規則以允許所有來自10.0.0.0 的 HTTPS 流量</span><span class="sxs-lookup"><span data-stu-id="35b11-110">1:  Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```
New-AzureRmFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="35b11-111">這個範例會建立一個規則，讓埠443上的所有 HTTPS 流量都是10.0.0.0。</span><span class="sxs-lookup"><span data-stu-id="35b11-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="35b11-112">2：建立規則，允許 WindowsUpdate for 10.0.0.0/24 子網</span><span class="sxs-lookup"><span data-stu-id="35b11-112">2:  Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```
New-AzureRmFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="35b11-113">這個範例會建立一條規則，以允許針對 10.0.0.0/24 網域的 Windows 更新進行通訊。</span><span class="sxs-lookup"><span data-stu-id="35b11-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="35b11-114">參數</span><span class="sxs-lookup"><span data-stu-id="35b11-114">PARAMETERS</span></span>

### <span data-ttu-id="35b11-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35b11-115">-DefaultProfile</span></span>
<span data-ttu-id="35b11-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="35b11-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35b11-117">-描述</span><span class="sxs-lookup"><span data-stu-id="35b11-117">-Description</span></span>
<span data-ttu-id="35b11-118">指定此規則的選擇性描述。</span><span class="sxs-lookup"><span data-stu-id="35b11-118">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="35b11-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="35b11-119">-FqdnTag</span></span>
<span data-ttu-id="35b11-120">指定此規則的 FQDN 標記清單。</span><span class="sxs-lookup"><span data-stu-id="35b11-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="35b11-121">您可以使用 [AzureRmFirewallFqdnTag](./Get-AzureRmFirewallFqdnTag.md) Cmdlet 來檢索可用的標記。</span><span class="sxs-lookup"><span data-stu-id="35b11-121">The available tags can be retrieved using [Get-AzureRmFirewallFqdnTag](./Get-AzureRmFirewallFqdnTag.md) cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b11-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="35b11-122">-Name</span></span>
<span data-ttu-id="35b11-123">指定此應用程式規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="35b11-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="35b11-124">該名稱在規則集合內必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="35b11-124">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="35b11-125">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="35b11-125">-Protocol</span></span>
<span data-ttu-id="35b11-126">指定要依據此規則篩選的流量類型。</span><span class="sxs-lookup"><span data-stu-id="35b11-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="35b11-127">格式為 <protocol type> ： <port> 。</span><span class="sxs-lookup"><span data-stu-id="35b11-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="35b11-128">例如，"HTTP： 80" 或 "HTTPs： 443"。</span><span class="sxs-lookup"><span data-stu-id="35b11-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="35b11-129">使用 TargetFqdn 時，通訊協定是強制性的，但無法與 FqdnTag 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="35b11-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="35b11-130">支援的通訊協定為 HTTP 和 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="35b11-130">The supported protocols are HTTP and HTTPS.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b11-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="35b11-131">-SourceAddress</span></span>
<span data-ttu-id="35b11-132">規則的來源位址</span><span class="sxs-lookup"><span data-stu-id="35b11-132">The source addresses of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b11-133">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="35b11-133">-TargetFqdn</span></span>
<span data-ttu-id="35b11-134">指定此規則所篩選之功能變數名稱的清單。</span><span class="sxs-lookup"><span data-stu-id="35b11-134">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="35b11-135">水平線字元 " *" 只接受清單中 FQDN 的第一個字元。當使用時，水平線會與任何數目的字元相符。 (例如，"* msn.com" 將會與 msn.com 及其所有) 子域相符。</span><span class="sxs-lookup"><span data-stu-id="35b11-135">The asterik character, ' *', is accepted only as the first character of an FQDN in the list. When used, the asterik matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b11-136">-確認</span><span class="sxs-lookup"><span data-stu-id="35b11-136">-Confirm</span></span>
<span data-ttu-id="35b11-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="35b11-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35b11-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35b11-138">-WhatIf</span></span>
<span data-ttu-id="35b11-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="35b11-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35b11-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="35b11-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35b11-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35b11-141">CommonParameters</span></span>
<span data-ttu-id="35b11-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="35b11-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35b11-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="35b11-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35b11-144">輸入</span><span class="sxs-lookup"><span data-stu-id="35b11-144">INPUTS</span></span>

### <span data-ttu-id="35b11-145">所有</span><span class="sxs-lookup"><span data-stu-id="35b11-145">None</span></span>
<span data-ttu-id="35b11-146">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="35b11-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="35b11-147">輸出</span><span class="sxs-lookup"><span data-stu-id="35b11-147">OUTPUTS</span></span>

### <span data-ttu-id="35b11-148">PSFirewallApplicationRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="35b11-148">Microsoft.Azure.Commands.Network.Models.PSFirewallApplicationRule</span></span>

## <span data-ttu-id="35b11-149">筆記</span><span class="sxs-lookup"><span data-stu-id="35b11-149">NOTES</span></span>

## <span data-ttu-id="35b11-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="35b11-150">RELATED LINKS</span></span>

[<span data-ttu-id="35b11-151">新-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="35b11-151">New-AzureRmFirewallApplicationRuleCollection</span></span>](./New-AzureRmFirewallApplicationRuleCollection.md)

[<span data-ttu-id="35b11-152">新-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="35b11-152">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="35b11-153">AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="35b11-153">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="35b11-154">AzureRmFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="35b11-154">Get-AzureRmFirewallFqdnTag</span></span>](./Get-AzureRmFirewallFqdnTag.md)
