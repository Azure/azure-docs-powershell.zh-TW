---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
ms.openlocfilehash: efb3641f5c2a06ea64eed8d8b92e5e032a0809df
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139770"
---
# <span data-ttu-id="90d7a-101">New-AzFirewallHubIpAddress</span><span class="sxs-lookup"><span data-stu-id="90d7a-101">New-AzFirewallHubIpAddress</span></span>

## <span data-ttu-id="90d7a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="90d7a-102">SYNOPSIS</span></span>
<span data-ttu-id="90d7a-103">在虛擬中樞上 assoicated 到防火牆的 Ip 位址</span><span class="sxs-lookup"><span data-stu-id="90d7a-103">Ip addresses assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="90d7a-104">句法</span><span class="sxs-lookup"><span data-stu-id="90d7a-104">SYNTAX</span></span>

```
New-AzFirewallHubIpAddress [-PrivateIPAddress <String>] [-PublicIPs <PSAzureFirewallHubPublicIpAddresses>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90d7a-105">說明</span><span class="sxs-lookup"><span data-stu-id="90d7a-105">DESCRIPTION</span></span>
<span data-ttu-id="90d7a-106">Ip 位址 assoicated 至虛擬中樞上的防火牆。</span><span class="sxs-lookup"><span data-stu-id="90d7a-106">Ip addresses assoicated to the firewall on virtual hub.</span></span> <span data-ttu-id="90d7a-107">這些可以是公用和私人位址</span><span class="sxs-lookup"><span data-stu-id="90d7a-107">These can be public and private addresses</span></span>

## <span data-ttu-id="90d7a-108">示例</span><span class="sxs-lookup"><span data-stu-id="90d7a-108">EXAMPLES</span></span>

### <span data-ttu-id="90d7a-109">範例1</span><span class="sxs-lookup"><span data-stu-id="90d7a-109">Example 1</span></span>
```powershell
PS C:\> $fwpips = New-AzFirewallHubPublicIpAddress -Count 2
PS C:\> New-AzFirewallHubIpAddress -PublicIPs $fwpips
```

<span data-ttu-id="90d7a-110">這個範例會建立一個「中樞 Ip 位址」物件，其計數為2個公用 Ip。</span><span class="sxs-lookup"><span data-stu-id="90d7a-110">This example creates a Hub Ip address object with a count of 2 public IPs.</span></span> <span data-ttu-id="90d7a-111">HubIPAddress 物件會 ssociated 至虛擬中樞上的防火牆。</span><span class="sxs-lookup"><span data-stu-id="90d7a-111">The HubIPAddress object is ssociated to the firewall on the virtual hub.</span></span>

## <span data-ttu-id="90d7a-112">參數</span><span class="sxs-lookup"><span data-stu-id="90d7a-112">PARAMETERS</span></span>

### <span data-ttu-id="90d7a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90d7a-113">-DefaultProfile</span></span>
<span data-ttu-id="90d7a-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="90d7a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90d7a-115">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="90d7a-115">-PrivateIPAddress</span></span>
<span data-ttu-id="90d7a-116">連接至中樞之防火牆的專用 Ip 位址</span><span class="sxs-lookup"><span data-stu-id="90d7a-116">The private Ip Address of the Firewall attached to a Hub</span></span>

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

### <span data-ttu-id="90d7a-117">-PublicIPs</span><span class="sxs-lookup"><span data-stu-id="90d7a-117">-PublicIPs</span></span>
<span data-ttu-id="90d7a-118">連接至中樞之防火牆的 IP 位址</span><span class="sxs-lookup"><span data-stu-id="90d7a-118">The IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="90d7a-119">-確認</span><span class="sxs-lookup"><span data-stu-id="90d7a-119">-Confirm</span></span>
<span data-ttu-id="90d7a-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="90d7a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90d7a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90d7a-121">-WhatIf</span></span>
<span data-ttu-id="90d7a-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="90d7a-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90d7a-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90d7a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90d7a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90d7a-124">CommonParameters</span></span>
<span data-ttu-id="90d7a-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="90d7a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90d7a-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="90d7a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90d7a-127">輸入</span><span class="sxs-lookup"><span data-stu-id="90d7a-127">INPUTS</span></span>

### <span data-ttu-id="90d7a-128">所有</span><span class="sxs-lookup"><span data-stu-id="90d7a-128">None</span></span>

## <span data-ttu-id="90d7a-129">輸出</span><span class="sxs-lookup"><span data-stu-id="90d7a-129">OUTPUTS</span></span>

### <span data-ttu-id="90d7a-130">PSAzureFirewallHubIpAddresses 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="90d7a-130">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses</span></span>

## <span data-ttu-id="90d7a-131">筆記</span><span class="sxs-lookup"><span data-stu-id="90d7a-131">NOTES</span></span>

## <span data-ttu-id="90d7a-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="90d7a-132">RELATED LINKS</span></span>