---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9F9E4639-A557-4BD8-88C2-894F6C848C4A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4aa54a7bd236bb561b3de4b9c2a3c0a2710deb61
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967453"
---
# <span data-ttu-id="36cb7-101">New-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="36cb7-101">New-AzureLocalNetworkGateway</span></span>

## <span data-ttu-id="36cb7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="36cb7-102">SYNOPSIS</span></span>
<span data-ttu-id="36cb7-103">建立 Azure 局域網路閘道。</span><span class="sxs-lookup"><span data-stu-id="36cb7-103">creates an Azure local network gateway.</span></span>

## <span data-ttu-id="36cb7-104">句法</span><span class="sxs-lookup"><span data-stu-id="36cb7-104">SYNTAX</span></span>

```
New-AzureLocalNetworkGateway -GatewayName <String> -IpAddress <String>
 -AddressSpace <System.Collections.Generic.List`1[System.String]> [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="36cb7-105">說明</span><span class="sxs-lookup"><span data-stu-id="36cb7-105">DESCRIPTION</span></span>
<span data-ttu-id="36cb7-106">**新的-AzureLocalNetworkGateway** Cmdlet 會建立 Azure 局域網路閘道。</span><span class="sxs-lookup"><span data-stu-id="36cb7-106">The **New-AzureLocalNetworkGateway** cmdlet creates an Azure local network gateway.</span></span>

## <span data-ttu-id="36cb7-107">示例</span><span class="sxs-lookup"><span data-stu-id="36cb7-107">EXAMPLES</span></span>

## <span data-ttu-id="36cb7-108">參數</span><span class="sxs-lookup"><span data-stu-id="36cb7-108">PARAMETERS</span></span>

### <span data-ttu-id="36cb7-109">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="36cb7-109">-AddressSpace</span></span>
<span data-ttu-id="36cb7-110">指定位址空間。</span><span class="sxs-lookup"><span data-stu-id="36cb7-110">Specifies the address space.</span></span>

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

### <span data-ttu-id="36cb7-111">-Asn</span><span class="sxs-lookup"><span data-stu-id="36cb7-111">-Asn</span></span>
<span data-ttu-id="36cb7-112">指定 (ASN) 的自治系統號碼。</span><span class="sxs-lookup"><span data-stu-id="36cb7-112">Specifies the autonomous system number (ASN).</span></span>

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

### <span data-ttu-id="36cb7-113">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="36cb7-113">-BgpPeeringAddress</span></span>
<span data-ttu-id="36cb7-114">指定邊界閘道通訊協定 (BGP) 對等位址。</span><span class="sxs-lookup"><span data-stu-id="36cb7-114">Specifies the Border Gateway Protocol (BGP) peering address.</span></span>

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

### <span data-ttu-id="36cb7-115">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="36cb7-115">-GatewayName</span></span>
<span data-ttu-id="36cb7-116">指定閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="36cb7-116">Specifies the name of the gateway.</span></span>

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

### <span data-ttu-id="36cb7-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="36cb7-117">-IpAddress</span></span>
<span data-ttu-id="36cb7-118">指定 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="36cb7-118">Specifies the IP address.</span></span>

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

### <span data-ttu-id="36cb7-119">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="36cb7-119">-PeerWeight</span></span>
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

### <span data-ttu-id="36cb7-120">-設定檔</span><span class="sxs-lookup"><span data-stu-id="36cb7-120">-Profile</span></span>
<span data-ttu-id="36cb7-121">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="36cb7-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="36cb7-122">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="36cb7-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="36cb7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36cb7-123">CommonParameters</span></span>
<span data-ttu-id="36cb7-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="36cb7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36cb7-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="36cb7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36cb7-126">輸入</span><span class="sxs-lookup"><span data-stu-id="36cb7-126">INPUTS</span></span>

## <span data-ttu-id="36cb7-127">輸出</span><span class="sxs-lookup"><span data-stu-id="36cb7-127">OUTPUTS</span></span>

## <span data-ttu-id="36cb7-128">筆記</span><span class="sxs-lookup"><span data-stu-id="36cb7-128">NOTES</span></span>

## <span data-ttu-id="36cb7-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="36cb7-129">RELATED LINKS</span></span>

[<span data-ttu-id="36cb7-130">AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="36cb7-130">Get-AzureLocalNetworkGateway</span></span>](./Get-AzureLocalNetworkGateway.md)

[<span data-ttu-id="36cb7-131">移除-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="36cb7-131">Remove-AzureLocalNetworkGateway</span></span>](./Remove-AzureLocalNetworkGateway.md)

[<span data-ttu-id="36cb7-132">Reset-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="36cb7-132">Reset-AzureLocalNetworkGateway</span></span>](./Reset-AzureLocalNetworkGateway.md)


