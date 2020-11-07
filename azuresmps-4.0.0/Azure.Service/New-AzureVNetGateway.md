---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 36DA2BF9-091E-4A2C-B5E1-07B4D2E482FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: b73626681e4d089b3b4f20c72080159c31b1bf81
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967633"
---
# <span data-ttu-id="a0eaf-101">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="a0eaf-101">New-AzureVNetGateway</span></span>

## <span data-ttu-id="a0eaf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a0eaf-102">SYNOPSIS</span></span>
<span data-ttu-id="a0eaf-103">在虛擬網路中建立 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="a0eaf-103">Creates a VPN gateway in a virtual network.</span></span>

## <span data-ttu-id="a0eaf-104">句法</span><span class="sxs-lookup"><span data-stu-id="a0eaf-104">SYNTAX</span></span>

```
New-AzureVNetGateway -VNetName <String> [-GatewayType <String>] [-GatewaySKU <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a0eaf-105">說明</span><span class="sxs-lookup"><span data-stu-id="a0eaf-105">DESCRIPTION</span></span>
<span data-ttu-id="a0eaf-106">**新的-AzureVNetGateway** Cmdlet 會在虛擬網路中 (VPN) 閘道建立虛擬私人網路絡。</span><span class="sxs-lookup"><span data-stu-id="a0eaf-106">The **New-AzureVNetGateway** cmdlet creates a virtual private network (VPN) gateway in a virtual network.</span></span>
<span data-ttu-id="a0eaf-107">您也可以指定閘道的 SKU，不論是預設、標準或 HighPerformance。</span><span class="sxs-lookup"><span data-stu-id="a0eaf-107">You can also specify the SKU of the gateway, either Default, Standard, or HighPerformance.</span></span>
<span data-ttu-id="a0eaf-108">您可以指定類型（無論是 StaticRouting 或 DynamicRouting）。</span><span class="sxs-lookup"><span data-stu-id="a0eaf-108">You can specify the type, either StaticRouting or DynamicRouting.</span></span>

## <span data-ttu-id="a0eaf-109">示例</span><span class="sxs-lookup"><span data-stu-id="a0eaf-109">EXAMPLES</span></span>

### <span data-ttu-id="a0eaf-110">範例1：建立虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="a0eaf-110">Example 1: Create a virtual network gateway</span></span>
```
PS C:\> New-AzureVNetGateway -VNetName "ContosoVN07" -GatewayType "DynamicRouting" -GatewaySKU "Default"
```

<span data-ttu-id="a0eaf-111">這個命令會建立名為 ContosoVN07 的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="a0eaf-111">This command creates a virtual network gateway for the virtual network named ContosoVN07.</span></span>
<span data-ttu-id="a0eaf-112">閘道是預設的 SKU，並使用動態路由。</span><span class="sxs-lookup"><span data-stu-id="a0eaf-112">The gateway is the Default SKU and uses dynamic routing.</span></span>

## <span data-ttu-id="a0eaf-113">參數</span><span class="sxs-lookup"><span data-stu-id="a0eaf-113">PARAMETERS</span></span>

### <span data-ttu-id="a0eaf-114">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="a0eaf-114">-GatewaySKU</span></span>
<span data-ttu-id="a0eaf-115">指定此 Cmdlet 所建立之虛擬網路閘道的 SKU。</span><span class="sxs-lookup"><span data-stu-id="a0eaf-115">Specifies the SKU of the virtual network gateway that this cmdlet creates.</span></span>
<span data-ttu-id="a0eaf-116">有效值為：</span><span class="sxs-lookup"><span data-stu-id="a0eaf-116">Valid values are:</span></span> 

- <span data-ttu-id="a0eaf-117">設置</span><span class="sxs-lookup"><span data-stu-id="a0eaf-117">Default</span></span> 
- <span data-ttu-id="a0eaf-118">標準</span><span class="sxs-lookup"><span data-stu-id="a0eaf-118">Standard</span></span> 
- <span data-ttu-id="a0eaf-119">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="a0eaf-119">HighPerformance</span></span>

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

### <span data-ttu-id="a0eaf-120">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="a0eaf-120">-GatewayType</span></span>
<span data-ttu-id="a0eaf-121">指定此 Cmdlet 所建立的閘道類型。</span><span class="sxs-lookup"><span data-stu-id="a0eaf-121">Specifies the type of gateway that this cmdlet creates.</span></span>
<span data-ttu-id="a0eaf-122">有效值為：</span><span class="sxs-lookup"><span data-stu-id="a0eaf-122">Valid values are:</span></span> 

- <span data-ttu-id="a0eaf-123">StaticRouting</span><span class="sxs-lookup"><span data-stu-id="a0eaf-123">StaticRouting</span></span> 
- <span data-ttu-id="a0eaf-124">DynamicRouting</span><span class="sxs-lookup"><span data-stu-id="a0eaf-124">DynamicRouting</span></span>

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

### <span data-ttu-id="a0eaf-125">-設定檔</span><span class="sxs-lookup"><span data-stu-id="a0eaf-125">-Profile</span></span>
<span data-ttu-id="a0eaf-126">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a0eaf-126">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a0eaf-127">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="a0eaf-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a0eaf-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="a0eaf-128">-VNetName</span></span>
<span data-ttu-id="a0eaf-129">指定此 Cmdlet 新增虛擬網路閘道的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="a0eaf-129">Specifies the virtual network in which this cmdlet adds a virtual network gateway.</span></span>

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

### <span data-ttu-id="a0eaf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0eaf-130">CommonParameters</span></span>
<span data-ttu-id="a0eaf-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a0eaf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0eaf-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a0eaf-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0eaf-133">輸入</span><span class="sxs-lookup"><span data-stu-id="a0eaf-133">INPUTS</span></span>

## <span data-ttu-id="a0eaf-134">輸出</span><span class="sxs-lookup"><span data-stu-id="a0eaf-134">OUTPUTS</span></span>

## <span data-ttu-id="a0eaf-135">筆記</span><span class="sxs-lookup"><span data-stu-id="a0eaf-135">NOTES</span></span>

## <span data-ttu-id="a0eaf-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0eaf-136">RELATED LINKS</span></span>

[<span data-ttu-id="a0eaf-137">AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="a0eaf-137">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="a0eaf-138">移除-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="a0eaf-138">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="a0eaf-139">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="a0eaf-139">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="a0eaf-140">調整大小-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="a0eaf-140">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="a0eaf-141">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="a0eaf-141">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


