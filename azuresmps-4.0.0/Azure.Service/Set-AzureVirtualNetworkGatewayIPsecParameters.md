---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 150EE0DC-07CD-4E24-AF70-0C1A7BB61433
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8b663ced66318335afb1fe4c3bf0e6a1520ede7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967858"
---
# <span data-ttu-id="47b0c-101">Set-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="47b0c-101">Set-AzureVirtualNetworkGatewayIPsecParameters</span></span>

## <span data-ttu-id="47b0c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="47b0c-102">SYNOPSIS</span></span>
<span data-ttu-id="47b0c-103">設定虛擬網路閘道的 IPsec 參數。</span><span class="sxs-lookup"><span data-stu-id="47b0c-103">Sets IPsec parameters for a virtual network gateway.</span></span>

## <span data-ttu-id="47b0c-104">句法</span><span class="sxs-lookup"><span data-stu-id="47b0c-104">SYNTAX</span></span>

```
Set-AzureVirtualNetworkGatewayIPsecParameters -GatewayId <String> -ConnectedEntityId <String>
 [-EncryptionType <String>] [-PfsGroup <String>] [-SADataSizeKilobytes <Int32>] [-SALifetimeSeconds <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="47b0c-105">說明</span><span class="sxs-lookup"><span data-stu-id="47b0c-105">DESCRIPTION</span></span>
<span data-ttu-id="47b0c-106">**AzureVirtualNetworkGatewayIPsecParameters** Cmdlet 會為虛擬網路閘道設定 IPsec 參數。</span><span class="sxs-lookup"><span data-stu-id="47b0c-106">The **Set-AzureVirtualNetworkGatewayIPsecParameters** cmdlet sets IPsec parameters for a virtual network gateway.</span></span>

## <span data-ttu-id="47b0c-107">示例</span><span class="sxs-lookup"><span data-stu-id="47b0c-107">EXAMPLES</span></span>

## <span data-ttu-id="47b0c-108">參數</span><span class="sxs-lookup"><span data-stu-id="47b0c-108">PARAMETERS</span></span>

### <span data-ttu-id="47b0c-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="47b0c-109">-ConnectedEntityId</span></span>
<span data-ttu-id="47b0c-110">指定連線實體的識別碼。</span><span class="sxs-lookup"><span data-stu-id="47b0c-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="47b0c-111">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="47b0c-111">-EncryptionType</span></span>
<span data-ttu-id="47b0c-112">指定虛擬網路閘道的加密類型。</span><span class="sxs-lookup"><span data-stu-id="47b0c-112">Specifies the encryption type for the virtual network gateway.</span></span>
<span data-ttu-id="47b0c-113">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="47b0c-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="47b0c-114">NoEncryption</span><span class="sxs-lookup"><span data-stu-id="47b0c-114">NoEncryption</span></span>
- <span data-ttu-id="47b0c-115">RequireEncryption</span><span class="sxs-lookup"><span data-stu-id="47b0c-115">RequireEncryption</span></span>

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

### <span data-ttu-id="47b0c-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="47b0c-116">-GatewayId</span></span>
<span data-ttu-id="47b0c-117">指定閘道的 ID。</span><span class="sxs-lookup"><span data-stu-id="47b0c-117">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="47b0c-118">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="47b0c-118">-PfsGroup</span></span>
<span data-ttu-id="47b0c-119">指定 [完美轉寄保密 (PFS) ] 群組。</span><span class="sxs-lookup"><span data-stu-id="47b0c-119">Specifies the perfect forward secrecy (PFS) group.</span></span>
<span data-ttu-id="47b0c-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="47b0c-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="47b0c-121">PFS1</span><span class="sxs-lookup"><span data-stu-id="47b0c-121">PFS1</span></span>
- <span data-ttu-id="47b0c-122">所有</span><span class="sxs-lookup"><span data-stu-id="47b0c-122">None</span></span>

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

### <span data-ttu-id="47b0c-123">-設定檔</span><span class="sxs-lookup"><span data-stu-id="47b0c-123">-Profile</span></span>
<span data-ttu-id="47b0c-124">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="47b0c-124">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="47b0c-125">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="47b0c-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="47b0c-126">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="47b0c-126">-SADataSizeKilobytes</span></span>
<span data-ttu-id="47b0c-127">指定安全關聯 (SA) 的大小（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="47b0c-127">Specifies the size, in kilobytes, of the security association (SA).</span></span>

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

### <span data-ttu-id="47b0c-128">-SALifetimeSeconds</span><span class="sxs-lookup"><span data-stu-id="47b0c-128">-SALifetimeSeconds</span></span>
<span data-ttu-id="47b0c-129">指定安全關聯的期間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="47b0c-129">Specifies the period, in seconds, of the security association.</span></span>

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

### <span data-ttu-id="47b0c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47b0c-130">CommonParameters</span></span>
<span data-ttu-id="47b0c-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="47b0c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47b0c-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="47b0c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47b0c-133">輸入</span><span class="sxs-lookup"><span data-stu-id="47b0c-133">INPUTS</span></span>

## <span data-ttu-id="47b0c-134">輸出</span><span class="sxs-lookup"><span data-stu-id="47b0c-134">OUTPUTS</span></span>

## <span data-ttu-id="47b0c-135">筆記</span><span class="sxs-lookup"><span data-stu-id="47b0c-135">NOTES</span></span>

## <span data-ttu-id="47b0c-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="47b0c-136">RELATED LINKS</span></span>

[<span data-ttu-id="47b0c-137">AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="47b0c-137">Get-AzureVirtualNetworkGatewayIPsecParameters</span></span>](./Get-AzureVirtualNetworkGatewayIPsecParameters.md)


