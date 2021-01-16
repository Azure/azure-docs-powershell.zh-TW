---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
ms.openlocfilehash: c4bc5e9fcc7d0ca405a8031af29d16283f963ad2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435770"
---
# <span data-ttu-id="204e5-101">New-AzFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="204e5-101">New-AzFirewallPublicIpAddress</span></span>

## <span data-ttu-id="204e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="204e5-102">SYNOPSIS</span></span>
<span data-ttu-id="204e5-103">這是 Ip 位址的預留位置，可用於 azure 防火牆上的多重 pip。</span><span class="sxs-lookup"><span data-stu-id="204e5-103">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="204e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="204e5-104">SYNTAX</span></span>

```
New-AzFirewallPublicIpAddress [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="204e5-105">說明</span><span class="sxs-lookup"><span data-stu-id="204e5-105">DESCRIPTION</span></span>
<span data-ttu-id="204e5-106">這是 Ip 位址的預留位置，可用於 azure 防火牆上的多重 pip。</span><span class="sxs-lookup"><span data-stu-id="204e5-106">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="204e5-107">示例</span><span class="sxs-lookup"><span data-stu-id="204e5-107">EXAMPLES</span></span>

### <span data-ttu-id="204e5-108">範例1</span><span class="sxs-lookup"><span data-stu-id="204e5-108">Example 1</span></span>
```powershell
PS C:\> $publicIp = New-AzFirewallPublicIpAddress -Address 20.2.3.4
```

<span data-ttu-id="204e5-109">$publicIp 將是 ip 位址20.2.3.4 的預留位置</span><span class="sxs-lookup"><span data-stu-id="204e5-109">$publicIp will be the placeholder for the ip address 20.2.3.4</span></span>

## <span data-ttu-id="204e5-110">參數</span><span class="sxs-lookup"><span data-stu-id="204e5-110">PARAMETERS</span></span>

### <span data-ttu-id="204e5-111">-位址</span><span class="sxs-lookup"><span data-stu-id="204e5-111">-Address</span></span>
<span data-ttu-id="204e5-112">連接至中樞之防火牆的 IP 位址</span><span class="sxs-lookup"><span data-stu-id="204e5-112">The IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="204e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="204e5-113">-DefaultProfile</span></span>
<span data-ttu-id="204e5-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="204e5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="204e5-115">-確認</span><span class="sxs-lookup"><span data-stu-id="204e5-115">-Confirm</span></span>
<span data-ttu-id="204e5-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="204e5-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="204e5-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="204e5-117">-WhatIf</span></span>
<span data-ttu-id="204e5-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="204e5-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="204e5-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="204e5-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="204e5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="204e5-120">CommonParameters</span></span>
<span data-ttu-id="204e5-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="204e5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="204e5-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="204e5-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="204e5-123">輸入</span><span class="sxs-lookup"><span data-stu-id="204e5-123">INPUTS</span></span>

### <span data-ttu-id="204e5-124">所有</span><span class="sxs-lookup"><span data-stu-id="204e5-124">None</span></span>

## <span data-ttu-id="204e5-125">輸出</span><span class="sxs-lookup"><span data-stu-id="204e5-125">OUTPUTS</span></span>

### <span data-ttu-id="204e5-126">PSAzureFirewallPublicIpAddress 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="204e5-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span></span>

## <span data-ttu-id="204e5-127">筆記</span><span class="sxs-lookup"><span data-stu-id="204e5-127">NOTES</span></span>

## <span data-ttu-id="204e5-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="204e5-128">RELATED LINKS</span></span>
