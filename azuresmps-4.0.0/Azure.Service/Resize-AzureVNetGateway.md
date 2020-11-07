---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5765F6BD-38BC-451B-85C5-F5D1A5AF2831
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91e5e226cfe4fc4cb27d2df73eb4da4c12045510
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967533"
---
# <span data-ttu-id="56008-101">Resize-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="56008-101">Resize-AzureVNetGateway</span></span>

## <span data-ttu-id="56008-102">摘要</span><span class="sxs-lookup"><span data-stu-id="56008-102">SYNOPSIS</span></span>
<span data-ttu-id="56008-103">重新調整 VPN 閘道的大小。</span><span class="sxs-lookup"><span data-stu-id="56008-103">Resizes a VPN gateway.</span></span>

## <span data-ttu-id="56008-104">句法</span><span class="sxs-lookup"><span data-stu-id="56008-104">SYNTAX</span></span>

```
Resize-AzureVNetGateway -VNetName <String> -GatewaySKU <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="56008-105">說明</span><span class="sxs-lookup"><span data-stu-id="56008-105">DESCRIPTION</span></span>
<span data-ttu-id="56008-106">重 **設大小 AzureVNetGateway** Cmdlet 會將虛擬網路虛擬私人網路 (VPN) 閘道的大小調整為其他 SKU。</span><span class="sxs-lookup"><span data-stu-id="56008-106">The **Resize-AzureVNetGateway** cmdlet resizes a virtual network virtual private network (VPN) gateway to a different SKU.</span></span>
<span data-ttu-id="56008-107">虛擬網路閘道的有效 Sku 是預設、標準及 HighPerformance。</span><span class="sxs-lookup"><span data-stu-id="56008-107">Valid SKUs for a virtual network gateway are Default, Standard, and HighPerformance.</span></span>

## <span data-ttu-id="56008-108">示例</span><span class="sxs-lookup"><span data-stu-id="56008-108">EXAMPLES</span></span>

### <span data-ttu-id="56008-109">範例1：變更虛擬網路閘道的 SKU</span><span class="sxs-lookup"><span data-stu-id="56008-109">Example 1: Change the SKU for a virtual network gateway</span></span>
```
PS C:\> Resize-AzureVNetGateway -VNetName "ContosoVN07" -GatewaySKU "HighPerformance"
```

<span data-ttu-id="56008-110">這個命令會將名為 ContosoVN07 的虛擬網路閘道的 SKU 變更為 HighPerformance。</span><span class="sxs-lookup"><span data-stu-id="56008-110">This command changes the SKU of the virtual network gateway for the virtual network named ContosoVN07 to HighPerformance.</span></span>

## <span data-ttu-id="56008-111">參數</span><span class="sxs-lookup"><span data-stu-id="56008-111">PARAMETERS</span></span>

### <span data-ttu-id="56008-112">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="56008-112">-GatewaySKU</span></span>
<span data-ttu-id="56008-113">指定此 Cmdlet 調整虛擬網路閘道大小的 SKU。</span><span class="sxs-lookup"><span data-stu-id="56008-113">Specifies the SKU to which this cmdlet resizes virtual network gateway.</span></span>
<span data-ttu-id="56008-114">有效值為：</span><span class="sxs-lookup"><span data-stu-id="56008-114">Valid values are:</span></span> 

- <span data-ttu-id="56008-115">設置</span><span class="sxs-lookup"><span data-stu-id="56008-115">Default</span></span> 
- <span data-ttu-id="56008-116">標準</span><span class="sxs-lookup"><span data-stu-id="56008-116">Standard</span></span> 
- <span data-ttu-id="56008-117">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="56008-117">HighPerformance</span></span>

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

### <span data-ttu-id="56008-118">-設定檔</span><span class="sxs-lookup"><span data-stu-id="56008-118">-Profile</span></span>
<span data-ttu-id="56008-119">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="56008-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="56008-120">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="56008-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="56008-121">-VNetName</span><span class="sxs-lookup"><span data-stu-id="56008-121">-VNetName</span></span>
<span data-ttu-id="56008-122">指定此 Cmdlet 調整虛擬網路閘道大小的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="56008-122">Specifies the virtual network in which this cmdlet resizes a virtual network gateway.</span></span>

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

### <span data-ttu-id="56008-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56008-123">CommonParameters</span></span>
<span data-ttu-id="56008-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="56008-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56008-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="56008-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56008-126">輸入</span><span class="sxs-lookup"><span data-stu-id="56008-126">INPUTS</span></span>

## <span data-ttu-id="56008-127">輸出</span><span class="sxs-lookup"><span data-stu-id="56008-127">OUTPUTS</span></span>

## <span data-ttu-id="56008-128">筆記</span><span class="sxs-lookup"><span data-stu-id="56008-128">NOTES</span></span>

## <span data-ttu-id="56008-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="56008-129">RELATED LINKS</span></span>

[<span data-ttu-id="56008-130">AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="56008-130">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="56008-131">新-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="56008-131">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="56008-132">移除-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="56008-132">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="56008-133">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="56008-133">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="56008-134">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="56008-134">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


