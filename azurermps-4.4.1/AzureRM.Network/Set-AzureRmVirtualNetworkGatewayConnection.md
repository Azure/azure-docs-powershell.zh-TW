---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 5885f98d66e6226273215dcde856f5fc50d0bd56
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448096"
---
# <span data-ttu-id="184e3-101">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="184e3-101">Set-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="184e3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="184e3-102">SYNOPSIS</span></span>
<span data-ttu-id="184e3-103">配置虛擬網路閘道連線。</span><span class="sxs-lookup"><span data-stu-id="184e3-103">Configures a virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="184e3-104">句法</span><span class="sxs-lookup"><span data-stu-id="184e3-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="184e3-105">說明</span><span class="sxs-lookup"><span data-stu-id="184e3-105">DESCRIPTION</span></span>
<span data-ttu-id="184e3-106">AzureRmVirtualNetworkGatewayConnection Cmdlet 會 **設定** 虛擬網路閘道連線。</span><span class="sxs-lookup"><span data-stu-id="184e3-106">The **Set-AzureRmVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="184e3-107">示例</span><span class="sxs-lookup"><span data-stu-id="184e3-107">EXAMPLES</span></span>

## <span data-ttu-id="184e3-108">參數</span><span class="sxs-lookup"><span data-stu-id="184e3-108">PARAMETERS</span></span>

### <span data-ttu-id="184e3-109">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="184e3-109">-EnableBgp</span></span>
<span data-ttu-id="184e3-110">是否要在 S2S VPN 隧道上使用 BGP 會話</span><span class="sxs-lookup"><span data-stu-id="184e3-110">Whether to use a BGP session over a S2S VPN tunnel</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="184e3-111">-Force</span><span class="sxs-lookup"><span data-stu-id="184e3-111">-Force</span></span>
<span data-ttu-id="184e3-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="184e3-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="184e3-113">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="184e3-113">-IpsecPolicies</span></span>
<span data-ttu-id="184e3-114">IPSec 原則清單。</span><span class="sxs-lookup"><span data-stu-id="184e3-114">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="184e3-115">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="184e3-115">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="184e3-116">是否要針對 S2S 連線使用原則流量選擇器</span><span class="sxs-lookup"><span data-stu-id="184e3-116">Whether to use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="184e3-117">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="184e3-117">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="184e3-118">指定此 Cmdlet 用來修改虛擬網路閘道連線的 PSVirtualNetworkGatewayConnection 物件。</span><span class="sxs-lookup"><span data-stu-id="184e3-118">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="184e3-119">-確認</span><span class="sxs-lookup"><span data-stu-id="184e3-119">-Confirm</span></span>
<span data-ttu-id="184e3-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="184e3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="184e3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="184e3-121">-WhatIf</span></span>
<span data-ttu-id="184e3-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="184e3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="184e3-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="184e3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="184e3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="184e3-124">-DefaultProfile</span></span>
<span data-ttu-id="184e3-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="184e3-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="184e3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="184e3-126">CommonParameters</span></span>
<span data-ttu-id="184e3-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="184e3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="184e3-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="184e3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="184e3-129">輸入</span><span class="sxs-lookup"><span data-stu-id="184e3-129">INPUTS</span></span>

### <span data-ttu-id="184e3-130">PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="184e3-130">PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="184e3-131">形參 "VirtualNetworkGatewayConnection" 接受管線中 "PSVirtualNetworkGatewayConnection" 類型的值</span><span class="sxs-lookup"><span data-stu-id="184e3-131">Parameter 'VirtualNetworkGatewayConnection' accepts value of type 'PSVirtualNetworkGatewayConnection' from the pipeline</span></span>

## <span data-ttu-id="184e3-132">輸出</span><span class="sxs-lookup"><span data-stu-id="184e3-132">OUTPUTS</span></span>

### <span data-ttu-id="184e3-133">PSVirtualNetworkGatewayConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="184e3-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="184e3-134">筆記</span><span class="sxs-lookup"><span data-stu-id="184e3-134">NOTES</span></span>

## <span data-ttu-id="184e3-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="184e3-135">RELATED LINKS</span></span>

[<span data-ttu-id="184e3-136">AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="184e3-136">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="184e3-137">新-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="184e3-137">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="184e3-138">移除-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="184e3-138">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)

