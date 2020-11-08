---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
ms.openlocfilehash: 15f918214a71fe38c850126b31f93d14940fa602
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970883"
---
# <span data-ttu-id="a1b8f-101">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a1b8f-101">Reset-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="a1b8f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a1b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b8f-103">重設虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="a1b8f-103">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="a1b8f-104">句法</span><span class="sxs-lookup"><span data-stu-id="a1b8f-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1b8f-105">說明</span><span class="sxs-lookup"><span data-stu-id="a1b8f-105">DESCRIPTION</span></span>
<span data-ttu-id="a1b8f-106">重設虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="a1b8f-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="a1b8f-107">示例</span><span class="sxs-lookup"><span data-stu-id="a1b8f-107">EXAMPLES</span></span>

### <span data-ttu-id="a1b8f-108">範例1：</span><span class="sxs-lookup"><span data-stu-id="a1b8f-108">Example 1:</span></span>
```
$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="a1b8f-109">參數</span><span class="sxs-lookup"><span data-stu-id="a1b8f-109">PARAMETERS</span></span>

### <span data-ttu-id="a1b8f-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1b8f-110">-AsJob</span></span>
<span data-ttu-id="a1b8f-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a1b8f-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1b8f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b8f-112">-DefaultProfile</span></span>
<span data-ttu-id="a1b8f-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a1b8f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1b8f-114">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="a1b8f-114">-GatewayVip</span></span>
<span data-ttu-id="a1b8f-115">閘道 vip，以重設特定閘道實例 (例如，在 Active-Active 功能啟用閘道的情況下。 ) 根據預設，如果沒有傳遞任何值，就會重設閘道主要實例。</span><span class="sxs-lookup"><span data-stu-id="a1b8f-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b8f-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a1b8f-116">-VirtualNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b8f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b8f-117">CommonParameters</span></span>
<span data-ttu-id="a1b8f-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a1b8f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b8f-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a1b8f-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b8f-120">輸入</span><span class="sxs-lookup"><span data-stu-id="a1b8f-120">INPUTS</span></span>

### <span data-ttu-id="a1b8f-121">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a1b8f-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="a1b8f-122">System.object</span><span class="sxs-lookup"><span data-stu-id="a1b8f-122">System.String</span></span>

## <span data-ttu-id="a1b8f-123">輸出</span><span class="sxs-lookup"><span data-stu-id="a1b8f-123">OUTPUTS</span></span>

### <span data-ttu-id="a1b8f-124">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a1b8f-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="a1b8f-125">筆記</span><span class="sxs-lookup"><span data-stu-id="a1b8f-125">NOTES</span></span>

## <span data-ttu-id="a1b8f-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1b8f-126">RELATED LINKS</span></span>

[<span data-ttu-id="a1b8f-127">AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a1b8f-127">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="a1b8f-128">新-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a1b8f-128">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="a1b8f-129">移除-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a1b8f-129">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="a1b8f-130">調整大小-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a1b8f-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="a1b8f-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a1b8f-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)