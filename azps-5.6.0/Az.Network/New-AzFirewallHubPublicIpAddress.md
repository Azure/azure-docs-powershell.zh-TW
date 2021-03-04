---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallhubpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
ms.openlocfilehash: 43a92375126411d392623095a6753072757f49a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910426"
---
# <span data-ttu-id="a5969-101">New-AzFirewallHubPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a5969-101">New-AzFirewallHubPublicIpAddress</span></span>

## <span data-ttu-id="a5969-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a5969-102">SYNOPSIS</span></span>
<span data-ttu-id="a5969-103">將公用 Ip 套用至虛擬中樞上的防火牆</span><span class="sxs-lookup"><span data-stu-id="a5969-103">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="a5969-104">語法</span><span class="sxs-lookup"><span data-stu-id="a5969-104">SYNTAX</span></span>

```
New-AzFirewallHubPublicIpAddress [-Count <Int32>] [-Addresses <PSAzureFirewallPublicIpAddress[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5969-105">描述</span><span class="sxs-lookup"><span data-stu-id="a5969-105">DESCRIPTION</span></span>
<span data-ttu-id="a5969-106">將公用 Ip 套用至虛擬中樞上的防火牆</span><span class="sxs-lookup"><span data-stu-id="a5969-106">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="a5969-107">例子</span><span class="sxs-lookup"><span data-stu-id="a5969-107">EXAMPLES</span></span>

### <span data-ttu-id="a5969-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="a5969-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallHubPublicIpAddress -Count 2
```

<span data-ttu-id="a5969-109">這會在附加至虛擬中樞的防火牆上建立 2 個公用 IP。</span><span class="sxs-lookup"><span data-stu-id="a5969-109">This will create 2 public ips on the firewall attached to the virtual hub.</span></span> <span data-ttu-id="a5969-110">這會在後端建立 IP 位址。我們無法為新的防火牆明確提供 ipaddress。</span><span class="sxs-lookup"><span data-stu-id="a5969-110">This will create the ip address in the backend.We cannot provide the ipaddresses explicitly for a new firewall.</span></span>

### <span data-ttu-id="a5969-111">範例 2</span><span class="sxs-lookup"><span data-stu-id="a5969-111">Example 2</span></span>
```powershell
PS C:\> $publicIp1 = New-AzFirewallPublicIpAddress -Address 10.2.3.4
PS C:\> $publicIp2 = New-AzFirewallPublicIpAddress -Address 20.56.37.46
PS C:\> New-AzFirewallHubPublicIpAddress -Count 3 -Addresses $publicIp1, $publicIp2
```

<span data-ttu-id="a5969-112">這會保留防火牆上已存在的 $publicIp 1，$publicIp 2，在防火牆上建立 1 個新的公用 IP。</span><span class="sxs-lookup"><span data-stu-id="a5969-112">This will create 1 new public ip on the firewall by retain $publicIp1, $publicIp2 which are already exist on the firewall.</span></span>

## <span data-ttu-id="a5969-113">參數</span><span class="sxs-lookup"><span data-stu-id="a5969-113">PARAMETERS</span></span>

### <span data-ttu-id="a5969-114">-Addresses</span><span class="sxs-lookup"><span data-stu-id="a5969-114">-Addresses</span></span>
<span data-ttu-id="a5969-115">附加至中樞之防火牆的公用 IP 位址</span><span class="sxs-lookup"><span data-stu-id="a5969-115">The Public IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="a5969-116">-Count</span><span class="sxs-lookup"><span data-stu-id="a5969-116">-Count</span></span>
<span data-ttu-id="a5969-117">公用 Ip 位址的計數</span><span class="sxs-lookup"><span data-stu-id="a5969-117">The count of public Ip addresses</span></span>

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

### <span data-ttu-id="a5969-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5969-118">-DefaultProfile</span></span>
<span data-ttu-id="a5969-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a5969-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5969-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5969-120">CommonParameters</span></span>
<span data-ttu-id="a5969-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a5969-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5969-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5969-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5969-123">輸入</span><span class="sxs-lookup"><span data-stu-id="a5969-123">INPUTS</span></span>

### <span data-ttu-id="a5969-124">沒有</span><span class="sxs-lookup"><span data-stu-id="a5969-124">None</span></span>

## <span data-ttu-id="a5969-125">輸出</span><span class="sxs-lookup"><span data-stu-id="a5969-125">OUTPUTS</span></span>

### <span data-ttu-id="a5969-126">Microsoft.Azure.Commands.Network.models.PSAzureFirewallHubPublicIpAddresses</span><span class="sxs-lookup"><span data-stu-id="a5969-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span></span>

## <span data-ttu-id="a5969-127">筆記</span><span class="sxs-lookup"><span data-stu-id="a5969-127">NOTES</span></span>

## <span data-ttu-id="a5969-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5969-128">RELATED LINKS</span></span>
