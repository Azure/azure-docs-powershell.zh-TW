---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 0E4D44EE-BF28-46FE-B2FA-D35C1651016F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3940a5e6fc69ebee02f3e0de963bc87f790f8860
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966918"
---
# <span data-ttu-id="9a3a1-101">Reset-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9a3a1-101">Reset-AzureLocalNetworkGateway</span></span>

## <span data-ttu-id="9a3a1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9a3a1-102">SYNOPSIS</span></span>
<span data-ttu-id="9a3a1-103">重設局域網路閘道。</span><span class="sxs-lookup"><span data-stu-id="9a3a1-103">Resets a local network gateway.</span></span>

## <span data-ttu-id="9a3a1-104">句法</span><span class="sxs-lookup"><span data-stu-id="9a3a1-104">SYNTAX</span></span>

```
Reset-AzureLocalNetworkGateway -GatewayId <String>
 -AddressSpace <System.Collections.Generic.List`1[System.String]> [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9a3a1-105">說明</span><span class="sxs-lookup"><span data-stu-id="9a3a1-105">DESCRIPTION</span></span>
<span data-ttu-id="9a3a1-106">**Reset AzureLocalNetworkGateway** Cmdlet 會重設局域網路閘道。</span><span class="sxs-lookup"><span data-stu-id="9a3a1-106">The **Reset-AzureLocalNetworkGateway** cmdlet resets a local network gateway.</span></span>

## <span data-ttu-id="9a3a1-107">示例</span><span class="sxs-lookup"><span data-stu-id="9a3a1-107">EXAMPLES</span></span>

## <span data-ttu-id="9a3a1-108">參數</span><span class="sxs-lookup"><span data-stu-id="9a3a1-108">PARAMETERS</span></span>

### <span data-ttu-id="9a3a1-109">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="9a3a1-109">-AddressSpace</span></span>
<span data-ttu-id="9a3a1-110">指定位址空間。</span><span class="sxs-lookup"><span data-stu-id="9a3a1-110">Specifies the address space.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a3a1-111">-Asn</span><span class="sxs-lookup"><span data-stu-id="9a3a1-111">-Asn</span></span>
<span data-ttu-id="9a3a1-112">指定 (ASN) 的自治系統號碼。</span><span class="sxs-lookup"><span data-stu-id="9a3a1-112">Specifies the autonomous system number (ASN).</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a3a1-113">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="9a3a1-113">-BgpPeeringAddress</span></span>
<span data-ttu-id="9a3a1-114">指定邊界閘道通訊協定 (BGP) 對等位址。</span><span class="sxs-lookup"><span data-stu-id="9a3a1-114">Specifies the Border Gateway Protocol (BGP) peering address.</span></span>

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

### <span data-ttu-id="9a3a1-115">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="9a3a1-115">-GatewayId</span></span>
<span data-ttu-id="9a3a1-116">指定閘道的 ID。</span><span class="sxs-lookup"><span data-stu-id="9a3a1-116">Specifies the ID of the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a3a1-117">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="9a3a1-117">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a3a1-118">-設定檔</span><span class="sxs-lookup"><span data-stu-id="9a3a1-118">-Profile</span></span>
<span data-ttu-id="9a3a1-119">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="9a3a1-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="9a3a1-120">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="9a3a1-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a3a1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a3a1-121">CommonParameters</span></span>
<span data-ttu-id="9a3a1-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9a3a1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a3a1-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9a3a1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a3a1-124">輸入</span><span class="sxs-lookup"><span data-stu-id="9a3a1-124">INPUTS</span></span>

## <span data-ttu-id="9a3a1-125">輸出</span><span class="sxs-lookup"><span data-stu-id="9a3a1-125">OUTPUTS</span></span>

## <span data-ttu-id="9a3a1-126">筆記</span><span class="sxs-lookup"><span data-stu-id="9a3a1-126">NOTES</span></span>

## <span data-ttu-id="9a3a1-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="9a3a1-127">RELATED LINKS</span></span>

[<span data-ttu-id="9a3a1-128">AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9a3a1-128">Get-AzureLocalNetworkGateway</span></span>](./Get-AzureLocalNetworkGateway.md)

[<span data-ttu-id="9a3a1-129">新-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9a3a1-129">New-AzureLocalNetworkGateway</span></span>](./New-AzureLocalNetworkGateway.md)

[<span data-ttu-id="9a3a1-130">移除-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9a3a1-130">Remove-AzureLocalNetworkGateway</span></span>](./Remove-AzureLocalNetworkGateway.md)


