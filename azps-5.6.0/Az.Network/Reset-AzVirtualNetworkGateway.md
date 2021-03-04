---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/powershell/module/az.network/reset-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
ms.openlocfilehash: de9d7d23a60d24fca6c383ab3db1208a5eae6864
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908814"
---
# <span data-ttu-id="3c9c9-101">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3c9c9-101">Reset-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="3c9c9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3c9c9-102">SYNOPSIS</span></span>
<span data-ttu-id="3c9c9-103">重設虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="3c9c9-103">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="3c9c9-104">語法</span><span class="sxs-lookup"><span data-stu-id="3c9c9-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c9c9-105">描述</span><span class="sxs-lookup"><span data-stu-id="3c9c9-105">DESCRIPTION</span></span>
<span data-ttu-id="3c9c9-106">重設虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="3c9c9-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="3c9c9-107">例子</span><span class="sxs-lookup"><span data-stu-id="3c9c9-107">EXAMPLES</span></span>

### <span data-ttu-id="3c9c9-108">範例 1：</span><span class="sxs-lookup"><span data-stu-id="3c9c9-108">Example 1:</span></span>
```
$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="3c9c9-109">參數</span><span class="sxs-lookup"><span data-stu-id="3c9c9-109">PARAMETERS</span></span>

### <span data-ttu-id="3c9c9-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c9c9-110">-AsJob</span></span>
<span data-ttu-id="3c9c9-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3c9c9-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c9c9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c9c9-112">-DefaultProfile</span></span>
<span data-ttu-id="3c9c9-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3c9c9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c9c9-114">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="3c9c9-114">-GatewayVip</span></span>
<span data-ttu-id="3c9c9-115">要重設特定閘道實例的閘道 (例如啟用 Active-Active 功能的閘道。) 根據預設，如果未傳遞值，閘道主實例會重設。</span><span class="sxs-lookup"><span data-stu-id="3c9c9-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="3c9c9-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3c9c9-116">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="3c9c9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c9c9-117">CommonParameters</span></span>
<span data-ttu-id="3c9c9-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3c9c9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c9c9-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="3c9c9-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c9c9-120">輸入</span><span class="sxs-lookup"><span data-stu-id="3c9c9-120">INPUTS</span></span>

### <span data-ttu-id="3c9c9-121">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3c9c9-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="3c9c9-122">System.String</span><span class="sxs-lookup"><span data-stu-id="3c9c9-122">System.String</span></span>

## <span data-ttu-id="3c9c9-123">輸出</span><span class="sxs-lookup"><span data-stu-id="3c9c9-123">OUTPUTS</span></span>

### <span data-ttu-id="3c9c9-124">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3c9c9-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="3c9c9-125">筆記</span><span class="sxs-lookup"><span data-stu-id="3c9c9-125">NOTES</span></span>

## <span data-ttu-id="3c9c9-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="3c9c9-126">RELATED LINKS</span></span>

[<span data-ttu-id="3c9c9-127">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3c9c9-127">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="3c9c9-128">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3c9c9-128">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="3c9c9-129">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3c9c9-129">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="3c9c9-130">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3c9c9-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="3c9c9-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3c9c9-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
