---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallhubipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
ms.openlocfilehash: 333e245b77869903b74973a4f851d020d70c0943
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910430"
---
# <span data-ttu-id="e1d44-101">New-AzFirewallHubIpAddress</span><span class="sxs-lookup"><span data-stu-id="e1d44-101">New-AzFirewallHubIpAddress</span></span>

## <span data-ttu-id="e1d44-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e1d44-102">SYNOPSIS</span></span>
<span data-ttu-id="e1d44-103">已連接虛擬中樞上防火牆的 Ip 位址</span><span class="sxs-lookup"><span data-stu-id="e1d44-103">Ip addresses assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="e1d44-104">語法</span><span class="sxs-lookup"><span data-stu-id="e1d44-104">SYNTAX</span></span>

```
New-AzFirewallHubIpAddress [-PrivateIPAddress <String>] [-PublicIPs <PSAzureFirewallHubPublicIpAddresses>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1d44-105">描述</span><span class="sxs-lookup"><span data-stu-id="e1d44-105">DESCRIPTION</span></span>
<span data-ttu-id="e1d44-106">將 Ip 位址與虛擬中樞上的防火牆連接。</span><span class="sxs-lookup"><span data-stu-id="e1d44-106">Ip addresses assoicated to the firewall on virtual hub.</span></span> <span data-ttu-id="e1d44-107">這些可以是公用位址和私人位址</span><span class="sxs-lookup"><span data-stu-id="e1d44-107">These can be public and private addresses</span></span>

## <span data-ttu-id="e1d44-108">例子</span><span class="sxs-lookup"><span data-stu-id="e1d44-108">EXAMPLES</span></span>

### <span data-ttu-id="e1d44-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="e1d44-109">Example 1</span></span>
```powershell
PS C:\> $fwpips = New-AzFirewallHubPublicIpAddress -Count 2
PS C:\> New-AzFirewallHubIpAddress -PublicIPs $fwpips
```

<span data-ttu-id="e1d44-110">此範例會建立一個計算為 2 個公用 IP 的 Hub Ip 位址物件。</span><span class="sxs-lookup"><span data-stu-id="e1d44-110">This example creates a Hub Ip address object with a count of 2 public IPs.</span></span> <span data-ttu-id="e1d44-111">HubIPAddress 物件會與虛擬中樞上的防火牆關聯。</span><span class="sxs-lookup"><span data-stu-id="e1d44-111">The HubIPAddress object is ssociated to the firewall on the virtual hub.</span></span>

## <span data-ttu-id="e1d44-112">參數</span><span class="sxs-lookup"><span data-stu-id="e1d44-112">PARAMETERS</span></span>

### <span data-ttu-id="e1d44-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1d44-113">-DefaultProfile</span></span>
<span data-ttu-id="e1d44-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e1d44-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1d44-115">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="e1d44-115">-PrivateIPAddress</span></span>
<span data-ttu-id="e1d44-116">附加至中樞之防火牆的私人 Ip 位址</span><span class="sxs-lookup"><span data-stu-id="e1d44-116">The private Ip Address of the Firewall attached to a Hub</span></span>

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

### <span data-ttu-id="e1d44-117">-公用 IP</span><span class="sxs-lookup"><span data-stu-id="e1d44-117">-PublicIPs</span></span>
<span data-ttu-id="e1d44-118">附加至中樞之防火牆的 IP 位址</span><span class="sxs-lookup"><span data-stu-id="e1d44-118">The IP Addresses of the Firewall attached to a hub</span></span>

```yaml
Type: PSAzureFirewallHubPublicIpAddresses
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1d44-119">-確認</span><span class="sxs-lookup"><span data-stu-id="e1d44-119">-Confirm</span></span>
<span data-ttu-id="e1d44-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e1d44-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1d44-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1d44-121">-WhatIf</span></span>
<span data-ttu-id="e1d44-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e1d44-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1d44-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e1d44-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1d44-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d44-124">CommonParameters</span></span>
<span data-ttu-id="e1d44-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e1d44-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d44-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1d44-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d44-127">輸入</span><span class="sxs-lookup"><span data-stu-id="e1d44-127">INPUTS</span></span>

### <span data-ttu-id="e1d44-128">沒有</span><span class="sxs-lookup"><span data-stu-id="e1d44-128">None</span></span>

## <span data-ttu-id="e1d44-129">輸出</span><span class="sxs-lookup"><span data-stu-id="e1d44-129">OUTPUTS</span></span>

### <span data-ttu-id="e1d44-130">Microsoft.Azure.Commands.Network.models.PSAzureFirewallHubIpAddresses</span><span class="sxs-lookup"><span data-stu-id="e1d44-130">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses</span></span>

## <span data-ttu-id="e1d44-131">筆記</span><span class="sxs-lookup"><span data-stu-id="e1d44-131">NOTES</span></span>

## <span data-ttu-id="e1d44-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1d44-132">RELATED LINKS</span></span>
