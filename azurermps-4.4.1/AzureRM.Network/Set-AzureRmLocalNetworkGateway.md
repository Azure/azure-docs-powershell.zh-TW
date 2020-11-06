---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: 8d2b3c6c15a48407b138fa26778bdf906b5a7a2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448112"
---
# <span data-ttu-id="eaa1a-101">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="eaa1a-101">Set-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="eaa1a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eaa1a-102">SYNOPSIS</span></span>
<span data-ttu-id="eaa1a-103">修改本機網路閘道。</span><span class="sxs-lookup"><span data-stu-id="eaa1a-103">Modifies a local network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eaa1a-104">句法</span><span class="sxs-lookup"><span data-stu-id="eaa1a-104">SYNTAX</span></span>

```
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eaa1a-105">說明</span><span class="sxs-lookup"><span data-stu-id="eaa1a-105">DESCRIPTION</span></span>
<span data-ttu-id="eaa1a-106">**AzureRmLocalNetworkGateway** Cmdlet 會修改本機網路閘道。</span><span class="sxs-lookup"><span data-stu-id="eaa1a-106">The **Set-AzureRmLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="eaa1a-107">示例</span><span class="sxs-lookup"><span data-stu-id="eaa1a-107">EXAMPLES</span></span>

## <span data-ttu-id="eaa1a-108">參數</span><span class="sxs-lookup"><span data-stu-id="eaa1a-108">PARAMETERS</span></span>

### <span data-ttu-id="eaa1a-109">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="eaa1a-109">-AddressPrefix</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaa1a-110">-Asn</span><span class="sxs-lookup"><span data-stu-id="eaa1a-110">-Asn</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaa1a-111">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="eaa1a-111">-BgpPeeringAddress</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaa1a-112">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="eaa1a-112">-LocalNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eaa1a-113">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="eaa1a-113">-PeerWeight</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaa1a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaa1a-114">-DefaultProfile</span></span>
<span data-ttu-id="eaa1a-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eaa1a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eaa1a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaa1a-116">CommonParameters</span></span>
<span data-ttu-id="eaa1a-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eaa1a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaa1a-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eaa1a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaa1a-119">輸入</span><span class="sxs-lookup"><span data-stu-id="eaa1a-119">INPUTS</span></span>

### <span data-ttu-id="eaa1a-120">PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="eaa1a-120">PSLocalNetworkGateway</span></span>
<span data-ttu-id="eaa1a-121">形參 "LocalNetworkGateway" 接受管線中 "PSLocalNetworkGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="eaa1a-121">Parameter 'LocalNetworkGateway' accepts value of type 'PSLocalNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="eaa1a-122">輸出</span><span class="sxs-lookup"><span data-stu-id="eaa1a-122">OUTPUTS</span></span>

### <span data-ttu-id="eaa1a-123">PSLocalNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="eaa1a-123">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="eaa1a-124">筆記</span><span class="sxs-lookup"><span data-stu-id="eaa1a-124">NOTES</span></span>

## <span data-ttu-id="eaa1a-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="eaa1a-125">RELATED LINKS</span></span>

[<span data-ttu-id="eaa1a-126">AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="eaa1a-126">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="eaa1a-127">新-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="eaa1a-127">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="eaa1a-128">移除-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="eaa1a-128">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)


