---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: F3D44471-50F0-4737-9AF5-3DE7222EAF9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: b9aa386b47c02ed945cad63c00425534d68e66f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966931"
---
# <span data-ttu-id="1391c-101">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="1391c-101">Remove-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="1391c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1391c-102">SYNOPSIS</span></span>
<span data-ttu-id="1391c-103">移除虛擬網路閘道連線。</span><span class="sxs-lookup"><span data-stu-id="1391c-103">Removes a virtual network gateway connection.</span></span>

## <span data-ttu-id="1391c-104">句法</span><span class="sxs-lookup"><span data-stu-id="1391c-104">SYNTAX</span></span>

```
Remove-AzureVirtualNetworkGatewayConnection -GatewayId <String> -ConnectedEntityId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1391c-105">說明</span><span class="sxs-lookup"><span data-stu-id="1391c-105">DESCRIPTION</span></span>
<span data-ttu-id="1391c-106">**AzureVirtualNetworkGatewayConnection** Cmdlet 會移除虛擬網路閘道連線。</span><span class="sxs-lookup"><span data-stu-id="1391c-106">The **Remove-AzureVirtualNetworkGatewayConnection** cmdlet removes a virtual network gateway connection.</span></span>

## <span data-ttu-id="1391c-107">示例</span><span class="sxs-lookup"><span data-stu-id="1391c-107">EXAMPLES</span></span>

## <span data-ttu-id="1391c-108">參數</span><span class="sxs-lookup"><span data-stu-id="1391c-108">PARAMETERS</span></span>

### <span data-ttu-id="1391c-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="1391c-109">-ConnectedEntityId</span></span>
<span data-ttu-id="1391c-110">指定連線實體的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1391c-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="1391c-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="1391c-111">-GatewayId</span></span>
<span data-ttu-id="1391c-112">指定閘道的 ID。</span><span class="sxs-lookup"><span data-stu-id="1391c-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="1391c-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="1391c-113">-Profile</span></span>
<span data-ttu-id="1391c-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="1391c-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="1391c-115">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="1391c-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1391c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1391c-116">CommonParameters</span></span>
<span data-ttu-id="1391c-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1391c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1391c-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1391c-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1391c-119">輸入</span><span class="sxs-lookup"><span data-stu-id="1391c-119">INPUTS</span></span>

## <span data-ttu-id="1391c-120">輸出</span><span class="sxs-lookup"><span data-stu-id="1391c-120">OUTPUTS</span></span>

## <span data-ttu-id="1391c-121">筆記</span><span class="sxs-lookup"><span data-stu-id="1391c-121">NOTES</span></span>

## <span data-ttu-id="1391c-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="1391c-122">RELATED LINKS</span></span>

[<span data-ttu-id="1391c-123">AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="1391c-123">Get-AzureVirtualNetworkGatewayConnection</span></span>](./Get-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="1391c-124">新-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="1391c-124">New-AzureVirtualNetworkGatewayConnection</span></span>](./New-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="1391c-125">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="1391c-125">Reset-AzureVirtualNetworkGatewayConnection</span></span>](./Reset-AzureVirtualNetworkGatewayConnection.md)


