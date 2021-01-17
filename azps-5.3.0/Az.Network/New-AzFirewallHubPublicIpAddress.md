---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
ms.openlocfilehash: fc60a983e06e632912e43291f7b60980ff34a8cd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437668"
---
# <span data-ttu-id="6ff01-101">New-AzFirewallHubPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6ff01-101">New-AzFirewallHubPublicIpAddress</span></span>

## <span data-ttu-id="6ff01-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6ff01-102">SYNOPSIS</span></span>
<span data-ttu-id="6ff01-103">公用 Ip assoicated 至虛擬中樞上的防火牆</span><span class="sxs-lookup"><span data-stu-id="6ff01-103">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="6ff01-104">句法</span><span class="sxs-lookup"><span data-stu-id="6ff01-104">SYNTAX</span></span>

```
New-AzFirewallHubPublicIpAddress [-Count <Int32>] [-Addresses <PSAzureFirewallPublicIpAddress[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ff01-105">說明</span><span class="sxs-lookup"><span data-stu-id="6ff01-105">DESCRIPTION</span></span>
<span data-ttu-id="6ff01-106">公用 Ip assoicated 至虛擬中樞上的防火牆</span><span class="sxs-lookup"><span data-stu-id="6ff01-106">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="6ff01-107">示例</span><span class="sxs-lookup"><span data-stu-id="6ff01-107">EXAMPLES</span></span>

### <span data-ttu-id="6ff01-108">範例1</span><span class="sxs-lookup"><span data-stu-id="6ff01-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallHubPublicIpAddress -Count 2
```

<span data-ttu-id="6ff01-109">這會在附加至虛擬中樞的防火牆上建立兩個公用 ip。</span><span class="sxs-lookup"><span data-stu-id="6ff01-109">This will create 2 public ips on the firewall attached to the virtual hub.</span></span> <span data-ttu-id="6ff01-110">這會在後端建立 ip 位址。我們無法針對新的防火牆明確提供 ipaddresses。</span><span class="sxs-lookup"><span data-stu-id="6ff01-110">This will create the ip address in the backend.We cannot provide the ipaddresses explicitly for a new firewall.</span></span>

### <span data-ttu-id="6ff01-111">範例2</span><span class="sxs-lookup"><span data-stu-id="6ff01-111">Example 2</span></span>
```powershell
PS C:\> $publicIp1 = New-AzFirewallPublicIpAddress -Address 10.2.3.4
PS C:\> $publicIp2 = New-AzFirewallPublicIpAddress -Address 20.56.37.46
PS C:\> New-AzFirewallHubPublicIpAddress -Count 3 -Addresses $publicIp1, $publicIp2
```

<span data-ttu-id="6ff01-112">這將會保留防火牆上已存在 $publicIp 1、$publicIp 2，以在防火牆上建立1個新的公用 ip。</span><span class="sxs-lookup"><span data-stu-id="6ff01-112">This will create 1 new public ip on the firewall by retain $publicIp1, $publicIp2 which are already exist on the firewall.</span></span>

## <span data-ttu-id="6ff01-113">參數</span><span class="sxs-lookup"><span data-stu-id="6ff01-113">PARAMETERS</span></span>

### <span data-ttu-id="6ff01-114">-位址</span><span class="sxs-lookup"><span data-stu-id="6ff01-114">-Addresses</span></span>
<span data-ttu-id="6ff01-115">連接至中樞之防火牆的公用 IP 位址</span><span class="sxs-lookup"><span data-stu-id="6ff01-115">The Public IP Addresses of the Firewall attached to a hub</span></span>

```yaml
Type: PSAzureFirewallPublicIpAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff01-116">-Count</span><span class="sxs-lookup"><span data-stu-id="6ff01-116">-Count</span></span>
<span data-ttu-id="6ff01-117">公用 Ip 位址計數</span><span class="sxs-lookup"><span data-stu-id="6ff01-117">The count of public Ip addresses</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff01-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ff01-118">-DefaultProfile</span></span>
<span data-ttu-id="6ff01-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6ff01-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ff01-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ff01-120">CommonParameters</span></span>
<span data-ttu-id="6ff01-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6ff01-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ff01-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6ff01-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ff01-123">輸入</span><span class="sxs-lookup"><span data-stu-id="6ff01-123">INPUTS</span></span>

### <span data-ttu-id="6ff01-124">所有</span><span class="sxs-lookup"><span data-stu-id="6ff01-124">None</span></span>

## <span data-ttu-id="6ff01-125">輸出</span><span class="sxs-lookup"><span data-stu-id="6ff01-125">OUTPUTS</span></span>

### <span data-ttu-id="6ff01-126">PSAzureFirewallHubPublicIpAddresses 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6ff01-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span></span>

## <span data-ttu-id="6ff01-127">筆記</span><span class="sxs-lookup"><span data-stu-id="6ff01-127">NOTES</span></span>

## <span data-ttu-id="6ff01-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ff01-128">RELATED LINKS</span></span>
