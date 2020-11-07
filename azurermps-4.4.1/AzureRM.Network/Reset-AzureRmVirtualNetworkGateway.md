---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 2b2947ec86e928506624aea49b380db3c4f24bc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625713"
---
# <span data-ttu-id="c089c-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c089c-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="c089c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c089c-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c089c-103">句法</span><span class="sxs-lookup"><span data-stu-id="c089c-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c089c-104">說明</span><span class="sxs-lookup"><span data-stu-id="c089c-104">DESCRIPTION</span></span>

## <span data-ttu-id="c089c-105">示例</span><span class="sxs-lookup"><span data-stu-id="c089c-105">EXAMPLES</span></span>

## <span data-ttu-id="c089c-106">參數</span><span class="sxs-lookup"><span data-stu-id="c089c-106">PARAMETERS</span></span>

### <span data-ttu-id="c089c-107">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="c089c-107">-GatewayVip</span></span>
<span data-ttu-id="c089c-108">閘道 vip，以重設特定閘道實例 (例如，在 Active-Active 功能啟用閘道的情況下。 ) 根據預設，如果沒有傳遞任何值，就會重設閘道主要實例。</span><span class="sxs-lookup"><span data-stu-id="c089c-108">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="c089c-109">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c089c-109">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="c089c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c089c-110">-DefaultProfile</span></span>
<span data-ttu-id="c089c-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c089c-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c089c-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c089c-112">CommonParameters</span></span>
<span data-ttu-id="c089c-113">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c089c-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c089c-114">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c089c-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c089c-115">輸入</span><span class="sxs-lookup"><span data-stu-id="c089c-115">INPUTS</span></span>

### <span data-ttu-id="c089c-116">字串</span><span class="sxs-lookup"><span data-stu-id="c089c-116">String</span></span>
<span data-ttu-id="c089c-117">"GatewayVip" 參數從管線接受類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="c089c-117">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="c089c-118">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c089c-118">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="c089c-119">形參 "VirtualNetworkGateway" 接受管線中 "PSVirtualNetworkGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="c089c-119">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="c089c-120">輸出</span><span class="sxs-lookup"><span data-stu-id="c089c-120">OUTPUTS</span></span>

### <span data-ttu-id="c089c-121">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c089c-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="c089c-122">筆記</span><span class="sxs-lookup"><span data-stu-id="c089c-122">NOTES</span></span>

## <span data-ttu-id="c089c-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="c089c-123">RELATED LINKS</span></span>

[<span data-ttu-id="c089c-124">AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c089c-124">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="c089c-125">新-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c089c-125">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="c089c-126">移除-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c089c-126">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="c089c-127">調整大小-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c089c-127">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="c089c-128">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c089c-128">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


