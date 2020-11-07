---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: E3C0C3AA-3941-469E-A6CC-A92ADD7377B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bf6824219879af52549d7815d65dcb502a2a752
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967631"
---
# <span data-ttu-id="c51e2-101">New-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c51e2-101">New-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="c51e2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c51e2-102">SYNOPSIS</span></span>
<span data-ttu-id="c51e2-103">建立 Azure 虛擬閘道網路連線。</span><span class="sxs-lookup"><span data-stu-id="c51e2-103">Creates an Azure virtual gateway network connection.</span></span>

## <span data-ttu-id="c51e2-104">句法</span><span class="sxs-lookup"><span data-stu-id="c51e2-104">SYNTAX</span></span>

```
New-AzureVirtualNetworkGatewayConnection -ConnectedEntityId <String> -GatewayConnectionName <String>
 -GatewayConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>]
 -VirtualNetworkGatewayId <String> [-EnableBgp <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c51e2-105">說明</span><span class="sxs-lookup"><span data-stu-id="c51e2-105">DESCRIPTION</span></span>
<span data-ttu-id="c51e2-106">**新的-AzureVirtualNetworkGatewayConnection** Cmdlet 會建立 Azure 虛擬閘道網路連線。</span><span class="sxs-lookup"><span data-stu-id="c51e2-106">The **New-AzureVirtualNetworkGatewayConnection** cmdlet creates an Azure virtual gateway network connection.</span></span>

## <span data-ttu-id="c51e2-107">示例</span><span class="sxs-lookup"><span data-stu-id="c51e2-107">EXAMPLES</span></span>

## <span data-ttu-id="c51e2-108">參數</span><span class="sxs-lookup"><span data-stu-id="c51e2-108">PARAMETERS</span></span>

### <span data-ttu-id="c51e2-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="c51e2-109">-ConnectedEntityId</span></span>
<span data-ttu-id="c51e2-110">指定連線實體的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c51e2-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="c51e2-111">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="c51e2-111">-EnableBgp</span></span>
<span data-ttu-id="c51e2-112">啟用邊界閘道通訊協定 (BGP) 。</span><span class="sxs-lookup"><span data-stu-id="c51e2-112">Enables Border Gateway Protocol (BGP).</span></span>

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

### <span data-ttu-id="c51e2-113">-GatewayConnectionName</span><span class="sxs-lookup"><span data-stu-id="c51e2-113">-GatewayConnectionName</span></span>
<span data-ttu-id="c51e2-114">指定閘道連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="c51e2-114">Specifies a name for the gateway connection.</span></span>

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

### <span data-ttu-id="c51e2-115">-GatewayConnectionType</span><span class="sxs-lookup"><span data-stu-id="c51e2-115">-GatewayConnectionType</span></span>
<span data-ttu-id="c51e2-116">指定閘道連線的類型。</span><span class="sxs-lookup"><span data-stu-id="c51e2-116">Specifies the type of gateway connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c51e2-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="c51e2-117">-Profile</span></span>
<span data-ttu-id="c51e2-118">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="c51e2-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c51e2-119">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="c51e2-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c51e2-120">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="c51e2-120">-RoutingWeight</span></span>
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

### <span data-ttu-id="c51e2-121">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="c51e2-121">-SharedKey</span></span>
<span data-ttu-id="c51e2-122">指定共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="c51e2-122">Specifies a shared key.</span></span>

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

### <span data-ttu-id="c51e2-123">-VirtualNetworkGatewayId</span><span class="sxs-lookup"><span data-stu-id="c51e2-123">-VirtualNetworkGatewayId</span></span>
<span data-ttu-id="c51e2-124">指定虛擬網路閘道的 ID。</span><span class="sxs-lookup"><span data-stu-id="c51e2-124">Specifies the ID of a virtual network gateway.</span></span>

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

### <span data-ttu-id="c51e2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c51e2-125">CommonParameters</span></span>
<span data-ttu-id="c51e2-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c51e2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c51e2-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c51e2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c51e2-128">輸入</span><span class="sxs-lookup"><span data-stu-id="c51e2-128">INPUTS</span></span>

## <span data-ttu-id="c51e2-129">輸出</span><span class="sxs-lookup"><span data-stu-id="c51e2-129">OUTPUTS</span></span>

## <span data-ttu-id="c51e2-130">筆記</span><span class="sxs-lookup"><span data-stu-id="c51e2-130">NOTES</span></span>

## <span data-ttu-id="c51e2-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="c51e2-131">RELATED LINKS</span></span>

[<span data-ttu-id="c51e2-132">AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c51e2-132">Get-AzureVirtualNetworkGatewayConnection</span></span>](./Get-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="c51e2-133">移除-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c51e2-133">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="c51e2-134">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c51e2-134">Reset-AzureVirtualNetworkGatewayConnection</span></span>](./Reset-AzureVirtualNetworkGatewayConnection.md)


