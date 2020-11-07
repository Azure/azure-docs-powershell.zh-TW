---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermlocalnetworkgateway
schema: 2.0.0
ms.openlocfilehash: f01fd5c1c6694c8d16ab34e6aad9f6a52463c726
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801969"
---
# <span data-ttu-id="db409-101">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="db409-101">Set-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="db409-102">摘要</span><span class="sxs-lookup"><span data-stu-id="db409-102">SYNOPSIS</span></span>
<span data-ttu-id="db409-103">修改本機網路閘道。</span><span class="sxs-lookup"><span data-stu-id="db409-103">Modifies a local network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db409-104">句法</span><span class="sxs-lookup"><span data-stu-id="db409-104">SYNTAX</span></span>

```
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="db409-105">說明</span><span class="sxs-lookup"><span data-stu-id="db409-105">DESCRIPTION</span></span>
<span data-ttu-id="db409-106">**AzureRmLocalNetworkGateway** Cmdlet 會修改本機網路閘道。</span><span class="sxs-lookup"><span data-stu-id="db409-106">The **Set-AzureRmLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="db409-107">示例</span><span class="sxs-lookup"><span data-stu-id="db409-107">EXAMPLES</span></span>

### <span data-ttu-id="db409-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="db409-108">1:</span></span>
```

```

## <span data-ttu-id="db409-109">參數</span><span class="sxs-lookup"><span data-stu-id="db409-109">PARAMETERS</span></span>

### <span data-ttu-id="db409-110">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="db409-110">-AddressPrefix</span></span>
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

### <span data-ttu-id="db409-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db409-111">-AsJob</span></span>
<span data-ttu-id="db409-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db409-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db409-113">-Asn</span><span class="sxs-lookup"><span data-stu-id="db409-113">-Asn</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db409-114">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="db409-114">-BgpPeeringAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db409-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db409-115">-DefaultProfile</span></span>
<span data-ttu-id="db409-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="db409-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db409-117">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="db409-117">-LocalNetworkGateway</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db409-118">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="db409-118">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db409-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db409-119">CommonParameters</span></span>
<span data-ttu-id="db409-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="db409-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db409-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="db409-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db409-122">輸入</span><span class="sxs-lookup"><span data-stu-id="db409-122">INPUTS</span></span>

### <span data-ttu-id="db409-123">PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="db409-123">PSLocalNetworkGateway</span></span>
<span data-ttu-id="db409-124">形參 "LocalNetworkGateway" 接受管線中 "PSLocalNetworkGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="db409-124">Parameter 'LocalNetworkGateway' accepts value of type 'PSLocalNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="db409-125">輸出</span><span class="sxs-lookup"><span data-stu-id="db409-125">OUTPUTS</span></span>

### <span data-ttu-id="db409-126">PSLocalNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="db409-126">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="db409-127">筆記</span><span class="sxs-lookup"><span data-stu-id="db409-127">NOTES</span></span>

## <span data-ttu-id="db409-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="db409-128">RELATED LINKS</span></span>

[<span data-ttu-id="db409-129">AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="db409-129">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="db409-130">新-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="db409-130">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="db409-131">移除-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="db409-131">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)


