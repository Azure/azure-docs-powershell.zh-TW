---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 09642B94-E888-4A22-9E8E-62109DB9394E
online version: ''
schema: 2.0.0
ms.openlocfilehash: f42a788f29f8546e6f402f1685f4c91aa3d7e5cb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967535"
---
# <span data-ttu-id="bb575-101">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="bb575-101">Reset-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="bb575-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bb575-102">SYNOPSIS</span></span>
<span data-ttu-id="bb575-103">重設虛擬網路閘道連線。</span><span class="sxs-lookup"><span data-stu-id="bb575-103">Resets a virtual network gateway connection.</span></span>

## <span data-ttu-id="bb575-104">句法</span><span class="sxs-lookup"><span data-stu-id="bb575-104">SYNTAX</span></span>

```
Reset-AzureVirtualNetworkGatewayConnection -GatewayId <String> -ConnectedEntityId <String>
 -RoutingWeight <Int32> [-SharedKey <String>] [-EnableBgp <Boolean>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb575-105">說明</span><span class="sxs-lookup"><span data-stu-id="bb575-105">DESCRIPTION</span></span>
<span data-ttu-id="bb575-106">**Reset AzureVirtualNetworkGatewayConnection** Cmdlet 會重設虛擬網路閘道連線。</span><span class="sxs-lookup"><span data-stu-id="bb575-106">The **Reset-AzureVirtualNetworkGatewayConnection** cmdlet resets a virtual network gateway connection.</span></span>

## <span data-ttu-id="bb575-107">示例</span><span class="sxs-lookup"><span data-stu-id="bb575-107">EXAMPLES</span></span>

## <span data-ttu-id="bb575-108">參數</span><span class="sxs-lookup"><span data-stu-id="bb575-108">PARAMETERS</span></span>

### <span data-ttu-id="bb575-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="bb575-109">-ConnectedEntityId</span></span>
<span data-ttu-id="bb575-110">指定連線實體的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bb575-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="bb575-111">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="bb575-111">-EnableBgp</span></span>
<span data-ttu-id="bb575-112">啟用邊界閘道通訊協定 (BGP) 。</span><span class="sxs-lookup"><span data-stu-id="bb575-112">Enables Border Gateway Protocol (BGP).</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb575-113">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="bb575-113">-GatewayId</span></span>
<span data-ttu-id="bb575-114">指定閘道的 ID。</span><span class="sxs-lookup"><span data-stu-id="bb575-114">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="bb575-115">-設定檔</span><span class="sxs-lookup"><span data-stu-id="bb575-115">-Profile</span></span>
<span data-ttu-id="bb575-116">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="bb575-116">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="bb575-117">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="bb575-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bb575-118">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="bb575-118">-RoutingWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb575-119">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="bb575-119">-SharedKey</span></span>
<span data-ttu-id="bb575-120">指定共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="bb575-120">Specifies a shared key.</span></span>

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

### <span data-ttu-id="bb575-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb575-121">CommonParameters</span></span>
<span data-ttu-id="bb575-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bb575-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb575-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bb575-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb575-124">輸入</span><span class="sxs-lookup"><span data-stu-id="bb575-124">INPUTS</span></span>

## <span data-ttu-id="bb575-125">輸出</span><span class="sxs-lookup"><span data-stu-id="bb575-125">OUTPUTS</span></span>

## <span data-ttu-id="bb575-126">筆記</span><span class="sxs-lookup"><span data-stu-id="bb575-126">NOTES</span></span>

## <span data-ttu-id="bb575-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="bb575-127">RELATED LINKS</span></span>

[<span data-ttu-id="bb575-128">AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="bb575-128">Get-AzureVirtualNetworkGatewayConnection</span></span>](./Get-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="bb575-129">新-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="bb575-129">New-AzureVirtualNetworkGatewayConnection</span></span>](./New-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="bb575-130">移除-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="bb575-130">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)


