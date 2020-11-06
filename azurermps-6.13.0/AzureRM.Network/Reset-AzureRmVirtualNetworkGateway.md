---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: c5d77619fa5f89c60ce20a097e096709e9a48bae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455139"
---
# <span data-ttu-id="fe271-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fe271-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="fe271-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe271-102">SYNOPSIS</span></span>
<span data-ttu-id="fe271-103">重設虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="fe271-103">Resets the Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe271-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe271-104">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe271-105">說明</span><span class="sxs-lookup"><span data-stu-id="fe271-105">DESCRIPTION</span></span>
<span data-ttu-id="fe271-106">重設虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="fe271-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="fe271-107">示例</span><span class="sxs-lookup"><span data-stu-id="fe271-107">EXAMPLES</span></span>

### <span data-ttu-id="fe271-108">範例1：</span><span class="sxs-lookup"><span data-stu-id="fe271-108">Example 1:</span></span>
```
$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="fe271-109">參數</span><span class="sxs-lookup"><span data-stu-id="fe271-109">PARAMETERS</span></span>

### <span data-ttu-id="fe271-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe271-110">-AsJob</span></span>
<span data-ttu-id="fe271-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fe271-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe271-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe271-112">-DefaultProfile</span></span>
<span data-ttu-id="fe271-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe271-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe271-114">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="fe271-114">-GatewayVip</span></span>
<span data-ttu-id="fe271-115">閘道 vip，以重設特定閘道實例 (例如，在 Active-Active 功能啟用閘道的情況下。 ) 根據預設，如果沒有傳遞任何值，就會重設閘道主要實例。</span><span class="sxs-lookup"><span data-stu-id="fe271-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="fe271-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fe271-116">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="fe271-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe271-117">CommonParameters</span></span>
<span data-ttu-id="fe271-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe271-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe271-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fe271-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe271-120">輸入</span><span class="sxs-lookup"><span data-stu-id="fe271-120">INPUTS</span></span>

### <span data-ttu-id="fe271-121">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fe271-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="fe271-122">參數： VirtualNetworkGateway (ByValue) </span><span class="sxs-lookup"><span data-stu-id="fe271-122">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="fe271-123">System.object</span><span class="sxs-lookup"><span data-stu-id="fe271-123">System.String</span></span>
<span data-ttu-id="fe271-124">參數： GatewayVip (ByValue) </span><span class="sxs-lookup"><span data-stu-id="fe271-124">Parameters: GatewayVip (ByValue)</span></span>

## <span data-ttu-id="fe271-125">輸出</span><span class="sxs-lookup"><span data-stu-id="fe271-125">OUTPUTS</span></span>

### <span data-ttu-id="fe271-126">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fe271-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="fe271-127">筆記</span><span class="sxs-lookup"><span data-stu-id="fe271-127">NOTES</span></span>

## <span data-ttu-id="fe271-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe271-128">RELATED LINKS</span></span>

[<span data-ttu-id="fe271-129">AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fe271-129">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="fe271-130">新-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fe271-130">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="fe271-131">移除-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fe271-131">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="fe271-132">調整大小-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fe271-132">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="fe271-133">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fe271-133">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


