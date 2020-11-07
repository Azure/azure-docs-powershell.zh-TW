---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AD5F4D69-45AF-46FB-ADF0-59CEF9908EF7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d63ac418d2dcee97afef9ae5f351fb2c1eebece0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967532"
---
# <span data-ttu-id="eacac-101">Resize-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="eacac-101">Resize-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="eacac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eacac-102">SYNOPSIS</span></span>
<span data-ttu-id="eacac-103">重新調整虛擬閘道的大小。</span><span class="sxs-lookup"><span data-stu-id="eacac-103">Resizes a virtual network gateway.</span></span>

## <span data-ttu-id="eacac-104">句法</span><span class="sxs-lookup"><span data-stu-id="eacac-104">SYNTAX</span></span>

```
Resize-AzureVirtualNetworkGateway -GatewayId <String> -GatewaySKU <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="eacac-105">說明</span><span class="sxs-lookup"><span data-stu-id="eacac-105">DESCRIPTION</span></span>
<span data-ttu-id="eacac-106">Resize-AzureVirtualNetworkGateway Cmdlet 會調整虛擬網路閘道的大小。</span><span class="sxs-lookup"><span data-stu-id="eacac-106">The Resize-AzureVirtualNetworkGateway cmdlet resizes a virtual network gateway.</span></span>

## <span data-ttu-id="eacac-107">示例</span><span class="sxs-lookup"><span data-stu-id="eacac-107">EXAMPLES</span></span>

## <span data-ttu-id="eacac-108">參數</span><span class="sxs-lookup"><span data-stu-id="eacac-108">PARAMETERS</span></span>

### <span data-ttu-id="eacac-109">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="eacac-109">-GatewayId</span></span>
<span data-ttu-id="eacac-110">指定閘道的 ID。</span><span class="sxs-lookup"><span data-stu-id="eacac-110">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="eacac-111">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="eacac-111">-GatewaySKU</span></span>
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

### <span data-ttu-id="eacac-112">-設定檔</span><span class="sxs-lookup"><span data-stu-id="eacac-112">-Profile</span></span>
<span data-ttu-id="eacac-113">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="eacac-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="eacac-114">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="eacac-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="eacac-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eacac-115">CommonParameters</span></span>
<span data-ttu-id="eacac-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eacac-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eacac-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eacac-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eacac-118">輸入</span><span class="sxs-lookup"><span data-stu-id="eacac-118">INPUTS</span></span>

## <span data-ttu-id="eacac-119">輸出</span><span class="sxs-lookup"><span data-stu-id="eacac-119">OUTPUTS</span></span>

## <span data-ttu-id="eacac-120">筆記</span><span class="sxs-lookup"><span data-stu-id="eacac-120">NOTES</span></span>

## <span data-ttu-id="eacac-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="eacac-121">RELATED LINKS</span></span>

[<span data-ttu-id="eacac-122">AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="eacac-122">Get-AzureVirtualNetworkGateway</span></span>](./Get-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="eacac-123">新-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="eacac-123">New-AzureVirtualNetworkGateway</span></span>](./New-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="eacac-124">移除-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="eacac-124">Remove-AzureVirtualNetworkGateway</span></span>](./Remove-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="eacac-125">Reset-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="eacac-125">Reset-AzureVirtualNetworkGateway</span></span>](./Reset-AzureVirtualNetworkGateway.md)


