---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: f4039fb8a616a474a858728b6e222537c2d75c66
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802258"
---
# <span data-ttu-id="f0cbd-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f0cbd-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="f0cbd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f0cbd-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0cbd-103">句法</span><span class="sxs-lookup"><span data-stu-id="f0cbd-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0cbd-104">說明</span><span class="sxs-lookup"><span data-stu-id="f0cbd-104">DESCRIPTION</span></span>

## <span data-ttu-id="f0cbd-105">示例</span><span class="sxs-lookup"><span data-stu-id="f0cbd-105">EXAMPLES</span></span>

### <span data-ttu-id="f0cbd-106">sr-1</span><span class="sxs-lookup"><span data-stu-id="f0cbd-106">1:</span></span>
```

```

## <span data-ttu-id="f0cbd-107">參數</span><span class="sxs-lookup"><span data-stu-id="f0cbd-107">PARAMETERS</span></span>

### <span data-ttu-id="f0cbd-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0cbd-108">-AsJob</span></span>
<span data-ttu-id="f0cbd-109">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f0cbd-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f0cbd-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0cbd-110">-DefaultProfile</span></span>
<span data-ttu-id="f0cbd-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f0cbd-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0cbd-112">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="f0cbd-112">-GatewayVip</span></span>
<span data-ttu-id="f0cbd-113">閘道 vip，以重設特定閘道實例 (例如，在 Active-Active 功能啟用閘道的情況下。 ) 根據預設，如果沒有傳遞任何值，就會重設閘道主要實例。</span><span class="sxs-lookup"><span data-stu-id="f0cbd-113">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0cbd-114">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f0cbd-114">-VirtualNetworkGateway</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0cbd-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0cbd-115">CommonParameters</span></span>
<span data-ttu-id="f0cbd-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f0cbd-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0cbd-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f0cbd-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0cbd-118">輸入</span><span class="sxs-lookup"><span data-stu-id="f0cbd-118">INPUTS</span></span>

### <span data-ttu-id="f0cbd-119">字串</span><span class="sxs-lookup"><span data-stu-id="f0cbd-119">String</span></span>
<span data-ttu-id="f0cbd-120">"GatewayVip" 參數從管線接受類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="f0cbd-120">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="f0cbd-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f0cbd-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="f0cbd-122">形參 "VirtualNetworkGateway" 接受管線中 "PSVirtualNetworkGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="f0cbd-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="f0cbd-123">輸出</span><span class="sxs-lookup"><span data-stu-id="f0cbd-123">OUTPUTS</span></span>

### <span data-ttu-id="f0cbd-124">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f0cbd-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="f0cbd-125">筆記</span><span class="sxs-lookup"><span data-stu-id="f0cbd-125">NOTES</span></span>

## <span data-ttu-id="f0cbd-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0cbd-126">RELATED LINKS</span></span>

[<span data-ttu-id="f0cbd-127">AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f0cbd-127">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="f0cbd-128">新-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f0cbd-128">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="f0cbd-129">移除-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f0cbd-129">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="f0cbd-130">調整大小-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f0cbd-130">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="f0cbd-131">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f0cbd-131">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


