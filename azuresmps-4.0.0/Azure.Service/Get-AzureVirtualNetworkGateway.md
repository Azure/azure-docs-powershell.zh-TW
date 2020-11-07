---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C4F876DF-FA9A-4446-8B7B-735137CEFE5D
online version: ''
schema: 2.0.0
ms.openlocfilehash: eccd46bac70cb6555277b66f45cf2e79ad10e1e7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967971"
---
# <span data-ttu-id="a57c3-101">Get-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a57c3-101">Get-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="a57c3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a57c3-102">SYNOPSIS</span></span>
<span data-ttu-id="a57c3-103">取得虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="a57c3-103">Gets a virtual network gateway.</span></span>

## <span data-ttu-id="a57c3-104">句法</span><span class="sxs-lookup"><span data-stu-id="a57c3-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGateway [-GatewayId <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a57c3-105">說明</span><span class="sxs-lookup"><span data-stu-id="a57c3-105">DESCRIPTION</span></span>
<span data-ttu-id="a57c3-106">**AzureVirtualNetworkGateway** Cmdlet 會取得 Azure 虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="a57c3-106">The **Get-AzureVirtualNetworkGateway** cmdlet gets an Azure virtual network gateway.</span></span>

## <span data-ttu-id="a57c3-107">示例</span><span class="sxs-lookup"><span data-stu-id="a57c3-107">EXAMPLES</span></span>

## <span data-ttu-id="a57c3-108">參數</span><span class="sxs-lookup"><span data-stu-id="a57c3-108">PARAMETERS</span></span>

### <span data-ttu-id="a57c3-109">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="a57c3-109">-GatewayId</span></span>
<span data-ttu-id="a57c3-110">指定閘道的 ID。</span><span class="sxs-lookup"><span data-stu-id="a57c3-110">Specifies the ID of the gateway.</span></span>

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

### <span data-ttu-id="a57c3-111">-設定檔</span><span class="sxs-lookup"><span data-stu-id="a57c3-111">-Profile</span></span>
<span data-ttu-id="a57c3-112">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a57c3-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a57c3-113">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="a57c3-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a57c3-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a57c3-114">CommonParameters</span></span>
<span data-ttu-id="a57c3-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a57c3-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a57c3-116">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a57c3-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a57c3-117">輸入</span><span class="sxs-lookup"><span data-stu-id="a57c3-117">INPUTS</span></span>

## <span data-ttu-id="a57c3-118">輸出</span><span class="sxs-lookup"><span data-stu-id="a57c3-118">OUTPUTS</span></span>

## <span data-ttu-id="a57c3-119">筆記</span><span class="sxs-lookup"><span data-stu-id="a57c3-119">NOTES</span></span>

## <span data-ttu-id="a57c3-120">相關連結</span><span class="sxs-lookup"><span data-stu-id="a57c3-120">RELATED LINKS</span></span>

[<span data-ttu-id="a57c3-121">新-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a57c3-121">New-AzureVirtualNetworkGateway</span></span>](./New-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="a57c3-122">移除-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a57c3-122">Remove-AzureVirtualNetworkGateway</span></span>](./Remove-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="a57c3-123">Reset-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a57c3-123">Reset-AzureVirtualNetworkGateway</span></span>](./Reset-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="a57c3-124">調整大小-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a57c3-124">Resize-AzureVirtualNetworkGateway</span></span>](./Resize-AzureVirtualNetworkGateway.md)


