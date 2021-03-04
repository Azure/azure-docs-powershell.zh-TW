---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: 86e15e54a0091839bdce6a66f891c12e6c0376f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916389"
---
# <span data-ttu-id="2333a-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2333a-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="2333a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2333a-102">SYNOPSIS</span></span>
<span data-ttu-id="2333a-103">建立新 Azure 防火牆原則網路規則</span><span class="sxs-lookup"><span data-stu-id="2333a-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="2333a-104">語法</span><span class="sxs-lookup"><span data-stu-id="2333a-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> [-DestinationIpGroup <String[]>]
 -DestinationPort <String[]> [-DestinationFqdn <String[]>] -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2333a-105">描述</span><span class="sxs-lookup"><span data-stu-id="2333a-105">DESCRIPTION</span></span>
<span data-ttu-id="2333a-106">**New-AzFirewallPolicyNetworkRule** Cmdlet 會建立 Azure 防火牆原則的網路規則。</span><span class="sxs-lookup"><span data-stu-id="2333a-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="2333a-107">例子</span><span class="sxs-lookup"><span data-stu-id="2333a-107">EXAMPLES</span></span>

### <span data-ttu-id="2333a-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="2333a-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="2333a-109">此範例會使用來源位址、通訊協定、目的地位址和目的地埠建立網路規則</span><span class="sxs-lookup"><span data-stu-id="2333a-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="2333a-110">參數</span><span class="sxs-lookup"><span data-stu-id="2333a-110">PARAMETERS</span></span>

### <span data-ttu-id="2333a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2333a-111">-DefaultProfile</span></span>
<span data-ttu-id="2333a-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2333a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2333a-113">-描述</span><span class="sxs-lookup"><span data-stu-id="2333a-113">-Description</span></span>
<span data-ttu-id="2333a-114">規則的描述</span><span class="sxs-lookup"><span data-stu-id="2333a-114">The description of the rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2333a-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="2333a-115">-DestinationAddress</span></span>
<span data-ttu-id="2333a-116">規則的目的地位址</span><span class="sxs-lookup"><span data-stu-id="2333a-116">The destination addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2333a-117">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="2333a-117">-DestinationFqdn</span></span>
<span data-ttu-id="2333a-118">規則的目標 FQDN</span><span class="sxs-lookup"><span data-stu-id="2333a-118">The destination FQDN of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2333a-119">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="2333a-119">-DestinationIpGroup</span></span>
<span data-ttu-id="2333a-120">規則的目標 ipgroups</span><span class="sxs-lookup"><span data-stu-id="2333a-120">The destination ipgroups of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2333a-121">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="2333a-121">-DestinationPort</span></span>
<span data-ttu-id="2333a-122">規則的目標埠</span><span class="sxs-lookup"><span data-stu-id="2333a-122">The destination ports of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2333a-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="2333a-123">-Name</span></span>
<span data-ttu-id="2333a-124">網路規則的名稱</span><span class="sxs-lookup"><span data-stu-id="2333a-124">The name of the Network Rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2333a-125">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="2333a-125">-Protocol</span></span>
<span data-ttu-id="2333a-126">規則的通訊協定</span><span class="sxs-lookup"><span data-stu-id="2333a-126">The protocols of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP, ICMP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2333a-127">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="2333a-127">-SourceAddress</span></span>
<span data-ttu-id="2333a-128">規則的來源位址</span><span class="sxs-lookup"><span data-stu-id="2333a-128">The source addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2333a-129">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="2333a-129">-SourceIpGroup</span></span>
<span data-ttu-id="2333a-130">規則的來源 ipgroups</span><span class="sxs-lookup"><span data-stu-id="2333a-130">The source ipgroups of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2333a-131">-確認</span><span class="sxs-lookup"><span data-stu-id="2333a-131">-Confirm</span></span>
<span data-ttu-id="2333a-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2333a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2333a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2333a-133">-WhatIf</span></span>
<span data-ttu-id="2333a-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2333a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2333a-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2333a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2333a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2333a-136">CommonParameters</span></span>
<span data-ttu-id="2333a-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2333a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2333a-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2333a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2333a-139">輸入</span><span class="sxs-lookup"><span data-stu-id="2333a-139">INPUTS</span></span>

### <span data-ttu-id="2333a-140">沒有</span><span class="sxs-lookup"><span data-stu-id="2333a-140">None</span></span>

## <span data-ttu-id="2333a-141">輸出</span><span class="sxs-lookup"><span data-stu-id="2333a-141">OUTPUTS</span></span>

### <span data-ttu-id="2333a-142">Microsoft.Azure.Commands.Network.models.PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2333a-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="2333a-143">筆記</span><span class="sxs-lookup"><span data-stu-id="2333a-143">NOTES</span></span>

## <span data-ttu-id="2333a-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="2333a-144">RELATED LINKS</span></span>
