---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5F016D72-80EB-462D-9646-25EC4E33293E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 485b29130fd4b54c378f3ec19389b6c24ba86c63
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967959"
---
# <span data-ttu-id="d6f19-101">Get-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="d6f19-101">Get-AzureVirtualNetworkGatewayKey</span></span>

## <span data-ttu-id="d6f19-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d6f19-102">SYNOPSIS</span></span>
<span data-ttu-id="d6f19-103">取得 Azure 虛擬網路閘道的金鑰。</span><span class="sxs-lookup"><span data-stu-id="d6f19-103">Gets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="d6f19-104">句法</span><span class="sxs-lookup"><span data-stu-id="d6f19-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayKey -GatewayId <String> -ConnectedEntityId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d6f19-105">說明</span><span class="sxs-lookup"><span data-stu-id="d6f19-105">DESCRIPTION</span></span>
<span data-ttu-id="d6f19-106">**AzureVirtualNetworkGatewayKey** Cmdlet 會取得 Azure 虛擬網路閘道的金鑰。</span><span class="sxs-lookup"><span data-stu-id="d6f19-106">The **Get-AzureVirtualNetworkGatewayKey** cmdlet gets the key for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="d6f19-107">示例</span><span class="sxs-lookup"><span data-stu-id="d6f19-107">EXAMPLES</span></span>

## <span data-ttu-id="d6f19-108">參數</span><span class="sxs-lookup"><span data-stu-id="d6f19-108">PARAMETERS</span></span>

### <span data-ttu-id="d6f19-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="d6f19-109">-ConnectedEntityId</span></span>
<span data-ttu-id="d6f19-110">指定連線實體的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d6f19-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="d6f19-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="d6f19-111">-GatewayId</span></span>
<span data-ttu-id="d6f19-112">指定閘道的 ID。</span><span class="sxs-lookup"><span data-stu-id="d6f19-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="d6f19-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="d6f19-113">-Profile</span></span>
<span data-ttu-id="d6f19-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="d6f19-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d6f19-115">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="d6f19-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d6f19-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6f19-116">CommonParameters</span></span>
<span data-ttu-id="d6f19-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d6f19-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6f19-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d6f19-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6f19-119">輸入</span><span class="sxs-lookup"><span data-stu-id="d6f19-119">INPUTS</span></span>

## <span data-ttu-id="d6f19-120">輸出</span><span class="sxs-lookup"><span data-stu-id="d6f19-120">OUTPUTS</span></span>

## <span data-ttu-id="d6f19-121">筆記</span><span class="sxs-lookup"><span data-stu-id="d6f19-121">NOTES</span></span>

## <span data-ttu-id="d6f19-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="d6f19-122">RELATED LINKS</span></span>

[<span data-ttu-id="d6f19-123">Reset-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="d6f19-123">Reset-AzureVirtualNetworkGatewayKey</span></span>](./Reset-AzureVirtualNetworkGatewayKey.md)

[<span data-ttu-id="d6f19-124">Set-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="d6f19-124">Set-AzureVirtualNetworkGatewayKey</span></span>](./Set-AzureVirtualNetworkGatewayKey.md)


