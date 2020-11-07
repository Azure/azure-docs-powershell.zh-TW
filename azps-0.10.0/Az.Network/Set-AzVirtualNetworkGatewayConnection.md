---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: b38ef9d212ceeb519e29d99391b17099177236a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795388"
---
# <span data-ttu-id="ffb3b-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ffb3b-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="ffb3b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ffb3b-102">SYNOPSIS</span></span>
<span data-ttu-id="ffb3b-103">配置虛擬網路閘道連線。</span><span class="sxs-lookup"><span data-stu-id="ffb3b-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="ffb3b-104">句法</span><span class="sxs-lookup"><span data-stu-id="ffb3b-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffb3b-105">說明</span><span class="sxs-lookup"><span data-stu-id="ffb3b-105">DESCRIPTION</span></span>
<span data-ttu-id="ffb3b-106">AzVirtualNetworkGatewayConnection Cmdlet 會 **設定** 虛擬網路閘道連線。</span><span class="sxs-lookup"><span data-stu-id="ffb3b-106">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="ffb3b-107">示例</span><span class="sxs-lookup"><span data-stu-id="ffb3b-107">EXAMPLES</span></span>

### <span data-ttu-id="ffb3b-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="ffb3b-108">1:</span></span>
```

```

## <span data-ttu-id="ffb3b-109">參數</span><span class="sxs-lookup"><span data-stu-id="ffb3b-109">PARAMETERS</span></span>

### <span data-ttu-id="ffb3b-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ffb3b-110">-AsJob</span></span>
<span data-ttu-id="ffb3b-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ffb3b-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffb3b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffb3b-112">-DefaultProfile</span></span>
<span data-ttu-id="ffb3b-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ffb3b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffb3b-114">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="ffb3b-114">-EnableBgp</span></span>
<span data-ttu-id="ffb3b-115">是否要在 S2S VPN 隧道上使用 BGP 會話</span><span class="sxs-lookup"><span data-stu-id="ffb3b-115">Whether to use a BGP session over a S2S VPN tunnel</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffb3b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ffb3b-116">-Force</span></span>
<span data-ttu-id="ffb3b-117">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ffb3b-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffb3b-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="ffb3b-118">-IpsecPolicies</span></span>
<span data-ttu-id="ffb3b-119">IPSec 原則清單。</span><span class="sxs-lookup"><span data-stu-id="ffb3b-119">A list of IPSec policies.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffb3b-120">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="ffb3b-120">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="ffb3b-121">是否要針對 S2S 連線使用原則流量選擇器</span><span class="sxs-lookup"><span data-stu-id="ffb3b-121">Whether to use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffb3b-122">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ffb3b-122">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="ffb3b-123">指定此 Cmdlet 用來修改虛擬網路閘道連線的 PSVirtualNetworkGatewayConnection 物件。</span><span class="sxs-lookup"><span data-stu-id="ffb3b-123">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffb3b-124">-確認</span><span class="sxs-lookup"><span data-stu-id="ffb3b-124">-Confirm</span></span>
<span data-ttu-id="ffb3b-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ffb3b-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffb3b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffb3b-126">-WhatIf</span></span>
<span data-ttu-id="ffb3b-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ffb3b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffb3b-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ffb3b-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffb3b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffb3b-129">CommonParameters</span></span>
<span data-ttu-id="ffb3b-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ffb3b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffb3b-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ffb3b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffb3b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="ffb3b-132">INPUTS</span></span>

### <span data-ttu-id="ffb3b-133">PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ffb3b-133">PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="ffb3b-134">形參 "VirtualNetworkGatewayConnection" 接受管線中 "PSVirtualNetworkGatewayConnection" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ffb3b-134">Parameter 'VirtualNetworkGatewayConnection' accepts value of type 'PSVirtualNetworkGatewayConnection' from the pipeline</span></span>

## <span data-ttu-id="ffb3b-135">輸出</span><span class="sxs-lookup"><span data-stu-id="ffb3b-135">OUTPUTS</span></span>

### <span data-ttu-id="ffb3b-136">PSVirtualNetworkGatewayConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ffb3b-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="ffb3b-137">筆記</span><span class="sxs-lookup"><span data-stu-id="ffb3b-137">NOTES</span></span>

## <span data-ttu-id="ffb3b-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="ffb3b-138">RELATED LINKS</span></span>

[<span data-ttu-id="ffb3b-139">AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ffb3b-139">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="ffb3b-140">新-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ffb3b-140">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="ffb3b-141">移除-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ffb3b-141">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)


