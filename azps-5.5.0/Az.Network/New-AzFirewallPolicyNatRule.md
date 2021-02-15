---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
ms.openlocfilehash: 05b89c164b8a6cd3f91880edac1536d22817ea57
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134946"
---
# <span data-ttu-id="b64ba-101">New-AzFirewallPolicyNatRule</span><span class="sxs-lookup"><span data-stu-id="b64ba-101">New-AzFirewallPolicyNatRule</span></span>

## <span data-ttu-id="b64ba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b64ba-102">SYNOPSIS</span></span>
<span data-ttu-id="b64ba-103">建立新的 Azure 防火牆原則 NAT 規則</span><span class="sxs-lookup"><span data-stu-id="b64ba-103">Create a new Azure Firewall Policy NAT Rule</span></span>

## <span data-ttu-id="b64ba-104">句法</span><span class="sxs-lookup"><span data-stu-id="b64ba-104">SYNTAX</span></span>

### <span data-ttu-id="b64ba-105">SourceAddressAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="b64ba-105">SourceAddressAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b64ba-106">SourceAddressAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="b64ba-106">SourceAddressAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b64ba-107">SourceIpGroupAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="b64ba-107">SourceIpGroupAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b64ba-108">SourceIpGroupAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="b64ba-108">SourceIpGroupAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b64ba-109">說明</span><span class="sxs-lookup"><span data-stu-id="b64ba-109">DESCRIPTION</span></span>
<span data-ttu-id="b64ba-110">**新的-AzFirewallPolicyNatRule** Cmdlet 會建立 Azure 防火牆原則的 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="b64ba-110">The **New-AzFirewallPolicyNatRule** cmdlet creates a NAT rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="b64ba-111">示例</span><span class="sxs-lookup"><span data-stu-id="b64ba-111">EXAMPLES</span></span>

### <span data-ttu-id="b64ba-112">範例1</span><span class="sxs-lookup"><span data-stu-id="b64ba-112">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="b64ba-113">這個範例會建立一個 NAT 規則，其中包含來源位址、通訊協定、目的地位址、目的地埠、翻譯位址，以及已翻譯的埠。</span><span class="sxs-lookup"><span data-stu-id="b64ba-113">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated address, and translated port.</span></span>

### <span data-ttu-id="b64ba-114">範例2</span><span class="sxs-lookup"><span data-stu-id="b64ba-114">Example 2</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedFqdn "internalhttp.server.net" -TranslatedPort "100"
```

<span data-ttu-id="b64ba-115">這個範例會建立一個 NAT 規則，其中包含來源位址、通訊協定、目的地位址、目的地埠、翻譯的 fqdn，以及已翻譯的埠。</span><span class="sxs-lookup"><span data-stu-id="b64ba-115">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated fqdn, and translated port.</span></span>

## <span data-ttu-id="b64ba-116">參數</span><span class="sxs-lookup"><span data-stu-id="b64ba-116">PARAMETERS</span></span>

### <span data-ttu-id="b64ba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b64ba-117">-DefaultProfile</span></span>
<span data-ttu-id="b64ba-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b64ba-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b64ba-119">-描述</span><span class="sxs-lookup"><span data-stu-id="b64ba-119">-Description</span></span>
<span data-ttu-id="b64ba-120">規則的描述</span><span class="sxs-lookup"><span data-stu-id="b64ba-120">The description of the rule</span></span>

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

### <span data-ttu-id="b64ba-121">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="b64ba-121">-DestinationAddress</span></span>
<span data-ttu-id="b64ba-122">規則的目的地位址。</span><span class="sxs-lookup"><span data-stu-id="b64ba-122">The destination addresses of the rule.</span></span> <span data-ttu-id="b64ba-123">這必須是防火牆的公用 IP。</span><span class="sxs-lookup"><span data-stu-id="b64ba-123">This has to be Public IP of the Firewall.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b64ba-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="b64ba-124">-DestinationPort</span></span>
<span data-ttu-id="b64ba-125">規則的目的地埠</span><span class="sxs-lookup"><span data-stu-id="b64ba-125">The destination ports of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b64ba-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="b64ba-126">-Name</span></span>
<span data-ttu-id="b64ba-127">NAT 規則集合的名稱</span><span class="sxs-lookup"><span data-stu-id="b64ba-127">The name of the NAT Rule Collection</span></span>

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

### <span data-ttu-id="b64ba-128">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="b64ba-128">-Protocol</span></span>
<span data-ttu-id="b64ba-129">規則的通訊協定</span><span class="sxs-lookup"><span data-stu-id="b64ba-129">The protocols of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b64ba-130">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="b64ba-130">-SourceAddress</span></span>
<span data-ttu-id="b64ba-131">規則的來源位址</span><span class="sxs-lookup"><span data-stu-id="b64ba-131">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTranslatedAddress, SourceAddressAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b64ba-132">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="b64ba-132">-SourceIpGroup</span></span>
<span data-ttu-id="b64ba-133">規則的來源 ipgroups</span><span class="sxs-lookup"><span data-stu-id="b64ba-133">The source ipgroups of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceIpGroupAndTranslatedAddress, SourceIpGroupAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b64ba-134">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="b64ba-134">-TranslatedAddress</span></span>
<span data-ttu-id="b64ba-135">此 NAT 規則的翻譯位址</span><span class="sxs-lookup"><span data-stu-id="b64ba-135">The translated address for this NAT rule</span></span>

```yaml
Type: System.String
Parameter Sets: SourceAddressAndTranslatedAddress, SourceIpGroupAndTranslatedAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b64ba-136">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="b64ba-136">-TranslatedFqdn</span></span>
<span data-ttu-id="b64ba-137">此 NAT 規則的已翻譯的 FQDN</span><span class="sxs-lookup"><span data-stu-id="b64ba-137">The translated FQDN for this NAT rule</span></span>

```yaml
Type: System.String
Parameter Sets: SourceAddressAndTranslatedFqdn, SourceIpGroupAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b64ba-138">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="b64ba-138">-TranslatedPort</span></span>
<span data-ttu-id="b64ba-139">此 NAT 規則的已翻譯埠</span><span class="sxs-lookup"><span data-stu-id="b64ba-139">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="b64ba-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b64ba-140">CommonParameters</span></span>
<span data-ttu-id="b64ba-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b64ba-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b64ba-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b64ba-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b64ba-143">輸入</span><span class="sxs-lookup"><span data-stu-id="b64ba-143">INPUTS</span></span>

### <span data-ttu-id="b64ba-144">所有</span><span class="sxs-lookup"><span data-stu-id="b64ba-144">None</span></span>

## <span data-ttu-id="b64ba-145">輸出</span><span class="sxs-lookup"><span data-stu-id="b64ba-145">OUTPUTS</span></span>

### <span data-ttu-id="b64ba-146">PSAzureFirewallNatRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b64ba-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="b64ba-147">筆記</span><span class="sxs-lookup"><span data-stu-id="b64ba-147">NOTES</span></span>

## <span data-ttu-id="b64ba-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="b64ba-148">RELATED LINKS</span></span>
