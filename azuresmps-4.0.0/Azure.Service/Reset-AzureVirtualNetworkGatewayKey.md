---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4F1E69B8-15FB-495F-B910-04E450D3215F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8a5b53f909b840a761d40f79a311fb61b7e2337b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967534"
---
# <span data-ttu-id="cd749-101">Reset-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="cd749-101">Reset-AzureVirtualNetworkGatewayKey</span></span>

## <span data-ttu-id="cd749-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cd749-102">SYNOPSIS</span></span>
<span data-ttu-id="cd749-103">重設虛擬網路閘道金鑰。</span><span class="sxs-lookup"><span data-stu-id="cd749-103">Resets a virtual network gateway key.</span></span>

## <span data-ttu-id="cd749-104">句法</span><span class="sxs-lookup"><span data-stu-id="cd749-104">SYNTAX</span></span>

```
Reset-AzureVirtualNetworkGatewayKey -GatewayId <String> -ConnectedEntityId <String> -keyLength <Int32>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cd749-105">說明</span><span class="sxs-lookup"><span data-stu-id="cd749-105">DESCRIPTION</span></span>
<span data-ttu-id="cd749-106">**Reset AzureVirtualNetworkGatewayKey** Cmdlet 會重設虛擬網路閘道金鑰。</span><span class="sxs-lookup"><span data-stu-id="cd749-106">The **Reset-AzureVirtualNetworkGatewayKey** cmdlet resets a virtual network gateway key.</span></span>

## <span data-ttu-id="cd749-107">示例</span><span class="sxs-lookup"><span data-stu-id="cd749-107">EXAMPLES</span></span>

## <span data-ttu-id="cd749-108">參數</span><span class="sxs-lookup"><span data-stu-id="cd749-108">PARAMETERS</span></span>

### <span data-ttu-id="cd749-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="cd749-109">-ConnectedEntityId</span></span>
<span data-ttu-id="cd749-110">指定連線實體的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cd749-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="cd749-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="cd749-111">-GatewayId</span></span>
<span data-ttu-id="cd749-112">指定閘道的 ID。</span><span class="sxs-lookup"><span data-stu-id="cd749-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="cd749-113">-keyLength</span><span class="sxs-lookup"><span data-stu-id="cd749-113">-keyLength</span></span>
<span data-ttu-id="cd749-114">指定金鑰長度。</span><span class="sxs-lookup"><span data-stu-id="cd749-114">Specifies the key length.</span></span>

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

### <span data-ttu-id="cd749-115">-設定檔</span><span class="sxs-lookup"><span data-stu-id="cd749-115">-Profile</span></span>
<span data-ttu-id="cd749-116">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="cd749-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cd749-117">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="cd749-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cd749-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd749-118">CommonParameters</span></span>
<span data-ttu-id="cd749-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cd749-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd749-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cd749-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd749-121">輸入</span><span class="sxs-lookup"><span data-stu-id="cd749-121">INPUTS</span></span>

## <span data-ttu-id="cd749-122">輸出</span><span class="sxs-lookup"><span data-stu-id="cd749-122">OUTPUTS</span></span>

## <span data-ttu-id="cd749-123">筆記</span><span class="sxs-lookup"><span data-stu-id="cd749-123">NOTES</span></span>

## <span data-ttu-id="cd749-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="cd749-124">RELATED LINKS</span></span>

[<span data-ttu-id="cd749-125">AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="cd749-125">Get-AzureVirtualNetworkGatewayKey</span></span>](./Get-AzureVirtualNetworkGatewayKey.md)

[<span data-ttu-id="cd749-126">Set-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="cd749-126">Set-AzureVirtualNetworkGatewayKey</span></span>](./Set-AzureVirtualNetworkGatewayKey.md)
