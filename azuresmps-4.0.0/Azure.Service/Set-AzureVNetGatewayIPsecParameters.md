---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C85576C1-182B-467E-9620-A475728E20D2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3715b07c66d76c824e684976f18de4ecea64cdb1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967482"
---
# <span data-ttu-id="bca37-101">Set-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="bca37-101">Set-AzureVNetGatewayIPsecParameters</span></span>

## <span data-ttu-id="bca37-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bca37-102">SYNOPSIS</span></span>
<span data-ttu-id="bca37-103">針對虛擬網路閘道與本機網路網站之間的連線設定 IPsec 參數。</span><span class="sxs-lookup"><span data-stu-id="bca37-103">Sets IPsec parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="bca37-104">句法</span><span class="sxs-lookup"><span data-stu-id="bca37-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayIPsecParameters -VNetName <String> -LocalNetworkSiteName <String>
 [-EncryptionType <String>] [-PfsGroup <String>] [-SADataSizeKilobytes <Int32>] [-SALifetimeSeconds <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bca37-105">說明</span><span class="sxs-lookup"><span data-stu-id="bca37-105">DESCRIPTION</span></span>
<span data-ttu-id="bca37-106">**AzureVNetGatewayIPsecParameters** Cmdlet 會將網際網路通訊協定安全性 (IPsec) 和網際網路金鑰交換 (IKE) 連線到虛擬網路閘道與本機網路網站之間的連線。</span><span class="sxs-lookup"><span data-stu-id="bca37-106">The **Set-AzureVNetGatewayIPsecParameters** cmdlet sets Internet Protocol security (IPsec) and Internet Key Exchange (IKE) parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="bca37-107">示例</span><span class="sxs-lookup"><span data-stu-id="bca37-107">EXAMPLES</span></span>

## <span data-ttu-id="bca37-108">參數</span><span class="sxs-lookup"><span data-stu-id="bca37-108">PARAMETERS</span></span>

### <span data-ttu-id="bca37-109">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="bca37-109">-EncryptionType</span></span>
<span data-ttu-id="bca37-110">指定虛擬網路閘道的加密類型。</span><span class="sxs-lookup"><span data-stu-id="bca37-110">Specifies the encryption type for the virtual network gateway.</span></span>
<span data-ttu-id="bca37-111">有效值為：</span><span class="sxs-lookup"><span data-stu-id="bca37-111">Valid values are:</span></span> 

- <span data-ttu-id="bca37-112">NoEncryption</span><span class="sxs-lookup"><span data-stu-id="bca37-112">NoEncryption</span></span> 
- <span data-ttu-id="bca37-113">RequireEncryption</span><span class="sxs-lookup"><span data-stu-id="bca37-113">RequireEncryption</span></span>

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

### <span data-ttu-id="bca37-114">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="bca37-114">-LocalNetworkSiteName</span></span>
<span data-ttu-id="bca37-115">指定此 Cmdlet 用來設定 IPsec 與 IKE 參數的本機網路網站連線名稱。</span><span class="sxs-lookup"><span data-stu-id="bca37-115">Specifies the name of the local network site connection on which this cmdlet configures the IPsec and IKE parameters.</span></span>

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

### <span data-ttu-id="bca37-116">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="bca37-116">-PfsGroup</span></span>
<span data-ttu-id="bca37-117">指定 [完美轉寄保密 (PFS) ] 群組。</span><span class="sxs-lookup"><span data-stu-id="bca37-117">Specifies the perfect forward secrecy (PFS) group.</span></span>
<span data-ttu-id="bca37-118">有效值為：</span><span class="sxs-lookup"><span data-stu-id="bca37-118">Valid values are:</span></span> 

- <span data-ttu-id="bca37-119">PFS1</span><span class="sxs-lookup"><span data-stu-id="bca37-119">PFS1</span></span> 
- <span data-ttu-id="bca37-120">所有</span><span class="sxs-lookup"><span data-stu-id="bca37-120">None</span></span>

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

### <span data-ttu-id="bca37-121">-設定檔</span><span class="sxs-lookup"><span data-stu-id="bca37-121">-Profile</span></span>
<span data-ttu-id="bca37-122">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="bca37-122">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="bca37-123">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="bca37-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bca37-124">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="bca37-124">-SADataSizeKilobytes</span></span>
<span data-ttu-id="bca37-125">指定安全關聯 (SA) 的大小（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="bca37-125">Specifies the size, in kilobytes, of the security association (SA).</span></span>

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

### <span data-ttu-id="bca37-126">-SALifetimeSeconds</span><span class="sxs-lookup"><span data-stu-id="bca37-126">-SALifetimeSeconds</span></span>
<span data-ttu-id="bca37-127">指定安全關聯的期間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="bca37-127">Specifies the period, in seconds, of the security association.</span></span>

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

### <span data-ttu-id="bca37-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="bca37-128">-VNetName</span></span>
<span data-ttu-id="bca37-129">指定此 Cmdlet 為連接設定 IPsec 參數的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="bca37-129">Specifies the virtual network for which this cmdlet sets IPsec parameters for the connection.</span></span>

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

### <span data-ttu-id="bca37-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bca37-130">CommonParameters</span></span>
<span data-ttu-id="bca37-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bca37-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bca37-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bca37-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bca37-133">輸入</span><span class="sxs-lookup"><span data-stu-id="bca37-133">INPUTS</span></span>

## <span data-ttu-id="bca37-134">輸出</span><span class="sxs-lookup"><span data-stu-id="bca37-134">OUTPUTS</span></span>

## <span data-ttu-id="bca37-135">筆記</span><span class="sxs-lookup"><span data-stu-id="bca37-135">NOTES</span></span>

## <span data-ttu-id="bca37-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="bca37-136">RELATED LINKS</span></span>

[<span data-ttu-id="bca37-137">AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="bca37-137">Get-AzureVNetGatewayIPsecParameters</span></span>](./Get-AzureVNetGatewayIPsecParameters.md)


