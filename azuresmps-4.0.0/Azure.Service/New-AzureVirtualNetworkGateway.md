---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A40F3BBB-4DC6-452E-A939-ED610F541EB1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7797c916813c985802a0a2f63a5a43e033009a06
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967632"
---
# <span data-ttu-id="3a550-101">New-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3a550-101">New-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="3a550-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3a550-102">SYNOPSIS</span></span>
<span data-ttu-id="3a550-103">建立 Azure 虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="3a550-103">Creates an Azure virtual network gateway.</span></span>

## <span data-ttu-id="3a550-104">句法</span><span class="sxs-lookup"><span data-stu-id="3a550-104">SYNTAX</span></span>

```
New-AzureVirtualNetworkGateway -VNetName <String> -GatewayName <String> [-GatewayType <String>]
 [-GatewaySKU <String>] [-Location <String>] [-VnetId <String>] [-Asn <UInt32>] [-PeerWeight <Int32>] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3a550-105">說明</span><span class="sxs-lookup"><span data-stu-id="3a550-105">DESCRIPTION</span></span>
<span data-ttu-id="3a550-106">**新的-AzureVirtualNetworkGateway** Cmdlet 會建立 Azure 虛擬閘道。</span><span class="sxs-lookup"><span data-stu-id="3a550-106">The **New-AzureVirtualNetworkGateway** cmdlet creates an Azure virtual network gateway.</span></span>

## <span data-ttu-id="3a550-107">示例</span><span class="sxs-lookup"><span data-stu-id="3a550-107">EXAMPLES</span></span>

## <span data-ttu-id="3a550-108">參數</span><span class="sxs-lookup"><span data-stu-id="3a550-108">PARAMETERS</span></span>

### <span data-ttu-id="3a550-109">-Asn</span><span class="sxs-lookup"><span data-stu-id="3a550-109">-Asn</span></span>
<span data-ttu-id="3a550-110">指定 (ASN) 的自治系統號碼。</span><span class="sxs-lookup"><span data-stu-id="3a550-110">Specifies the autonomous system number (ASN).</span></span>

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

### <span data-ttu-id="3a550-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3a550-111">-Force</span></span>
<span data-ttu-id="3a550-112">不要確認 Azure 虛擬網路閘道建立</span><span class="sxs-lookup"><span data-stu-id="3a550-112">Do not confirm Azure Virtual Network Gateway Creation</span></span>

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

### <span data-ttu-id="3a550-113">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="3a550-113">-GatewayName</span></span>
<span data-ttu-id="3a550-114">指定閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a550-114">Specifies the name of the gateway.</span></span>

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

### <span data-ttu-id="3a550-115">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="3a550-115">-GatewaySKU</span></span>
<span data-ttu-id="3a550-116">指定此 Cmdlet 所建立之虛擬網路閘道的 SKU。</span><span class="sxs-lookup"><span data-stu-id="3a550-116">Specifies the SKU of the virtual network gateway that this cmdlet creates.</span></span>
<span data-ttu-id="3a550-117">有效值為：</span><span class="sxs-lookup"><span data-stu-id="3a550-117">Valid values are:</span></span>

- <span data-ttu-id="3a550-118">設置</span><span class="sxs-lookup"><span data-stu-id="3a550-118">Default</span></span>
- <span data-ttu-id="3a550-119">標準</span><span class="sxs-lookup"><span data-stu-id="3a550-119">Standard</span></span>
- <span data-ttu-id="3a550-120">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="3a550-120">HighPerformance</span></span>

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

### <span data-ttu-id="3a550-121">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="3a550-121">-GatewayType</span></span>
<span data-ttu-id="3a550-122">指定閘道類型。</span><span class="sxs-lookup"><span data-stu-id="3a550-122">Specifies the type of gateway.</span></span>

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

### <span data-ttu-id="3a550-123">-位置</span><span class="sxs-lookup"><span data-stu-id="3a550-123">-Location</span></span>
<span data-ttu-id="3a550-124">指定位置。</span><span class="sxs-lookup"><span data-stu-id="3a550-124">Specifies the location.</span></span>

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

### <span data-ttu-id="3a550-125">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="3a550-125">-PeerWeight</span></span>
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

### <span data-ttu-id="3a550-126">-設定檔</span><span class="sxs-lookup"><span data-stu-id="3a550-126">-Profile</span></span>
<span data-ttu-id="3a550-127">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="3a550-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3a550-128">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="3a550-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3a550-129">-VnetId</span><span class="sxs-lookup"><span data-stu-id="3a550-129">-VnetId</span></span>
<span data-ttu-id="3a550-130">指定虛擬網路的 ID。</span><span class="sxs-lookup"><span data-stu-id="3a550-130">Specifies the ID of a virtual network.</span></span>

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

### <span data-ttu-id="3a550-131">-VNetName</span><span class="sxs-lookup"><span data-stu-id="3a550-131">-VNetName</span></span>
<span data-ttu-id="3a550-132">指定虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="3a550-132">Specifies a virtual network.</span></span>

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

### <span data-ttu-id="3a550-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a550-133">CommonParameters</span></span>
<span data-ttu-id="3a550-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3a550-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a550-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3a550-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a550-136">輸入</span><span class="sxs-lookup"><span data-stu-id="3a550-136">INPUTS</span></span>

## <span data-ttu-id="3a550-137">輸出</span><span class="sxs-lookup"><span data-stu-id="3a550-137">OUTPUTS</span></span>

## <span data-ttu-id="3a550-138">筆記</span><span class="sxs-lookup"><span data-stu-id="3a550-138">NOTES</span></span>

## <span data-ttu-id="3a550-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a550-139">RELATED LINKS</span></span>

[<span data-ttu-id="3a550-140">AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3a550-140">Get-AzureVirtualNetworkGateway</span></span>](./Get-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="3a550-141">移除-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3a550-141">Remove-AzureVirtualNetworkGateway</span></span>](./Remove-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="3a550-142">調整大小-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3a550-142">Resize-AzureVirtualNetworkGateway</span></span>](./Resize-AzureVirtualNetworkGateway.md)
