---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8099942A-B6EB-4C01-9F57-378B0EB7B3C9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67c933b716095392a215543cfc61d334cd347835
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966883"
---
# <span data-ttu-id="e2635-101">Set-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="e2635-101">Set-AzureVirtualNetworkGatewayKey</span></span>

## <span data-ttu-id="e2635-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e2635-102">SYNOPSIS</span></span>
<span data-ttu-id="e2635-103">設定 Azure 虛擬網路閘道的金鑰。</span><span class="sxs-lookup"><span data-stu-id="e2635-103">Sets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="e2635-104">句法</span><span class="sxs-lookup"><span data-stu-id="e2635-104">SYNTAX</span></span>

```
Set-AzureVirtualNetworkGatewayKey -GatewayId <String> -ConnectedEntityId <String> -SharedKey <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e2635-105">說明</span><span class="sxs-lookup"><span data-stu-id="e2635-105">DESCRIPTION</span></span>
<span data-ttu-id="e2635-106">**AzureVirtualNetworkGatewayKey** Cmdlet 會設定 Azure 虛擬閘道的金鑰。</span><span class="sxs-lookup"><span data-stu-id="e2635-106">The **Set-AzureVirtualNetworkGatewayKey** cmdlet sets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="e2635-107">示例</span><span class="sxs-lookup"><span data-stu-id="e2635-107">EXAMPLES</span></span>

## <span data-ttu-id="e2635-108">參數</span><span class="sxs-lookup"><span data-stu-id="e2635-108">PARAMETERS</span></span>

### <span data-ttu-id="e2635-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="e2635-109">-ConnectedEntityId</span></span>
<span data-ttu-id="e2635-110">指定連線實體的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e2635-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="e2635-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="e2635-111">-GatewayId</span></span>
<span data-ttu-id="e2635-112">指定閘道的 ID。</span><span class="sxs-lookup"><span data-stu-id="e2635-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="e2635-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="e2635-113">-Profile</span></span>
<span data-ttu-id="e2635-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e2635-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="e2635-115">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="e2635-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e2635-116">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="e2635-116">-SharedKey</span></span>
<span data-ttu-id="e2635-117">指定共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="e2635-117">Specifies a shared key.</span></span>

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

### <span data-ttu-id="e2635-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2635-118">CommonParameters</span></span>
<span data-ttu-id="e2635-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e2635-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2635-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e2635-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2635-121">輸入</span><span class="sxs-lookup"><span data-stu-id="e2635-121">INPUTS</span></span>

## <span data-ttu-id="e2635-122">輸出</span><span class="sxs-lookup"><span data-stu-id="e2635-122">OUTPUTS</span></span>

## <span data-ttu-id="e2635-123">筆記</span><span class="sxs-lookup"><span data-stu-id="e2635-123">NOTES</span></span>

## <span data-ttu-id="e2635-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="e2635-124">RELATED LINKS</span></span>

[<span data-ttu-id="e2635-125">AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="e2635-125">Get-AzureVirtualNetworkGatewayKey</span></span>](./Get-AzureVirtualNetworkGatewayKey.md)

[<span data-ttu-id="e2635-126">Reset-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="e2635-126">Reset-AzureVirtualNetworkGatewayKey</span></span>](./Reset-AzureVirtualNetworkGatewayKey.md)

