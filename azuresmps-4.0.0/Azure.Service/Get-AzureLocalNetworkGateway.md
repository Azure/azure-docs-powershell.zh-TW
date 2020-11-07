---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D7A50D71-1D23-431E-9ACD-3A0D1BDC2B17
online version: ''
schema: 2.0.0
ms.openlocfilehash: e6c1bfbf98b1d53d9c5ba5867b2948625f8a5f3b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967785"
---
# <span data-ttu-id="a6d37-101">Get-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a6d37-101">Get-AzureLocalNetworkGateway</span></span>

## <span data-ttu-id="a6d37-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a6d37-102">SYNOPSIS</span></span>
<span data-ttu-id="a6d37-103">取得局域網路閘道。</span><span class="sxs-lookup"><span data-stu-id="a6d37-103">Gets a local network gateway.</span></span>

## <span data-ttu-id="a6d37-104">句法</span><span class="sxs-lookup"><span data-stu-id="a6d37-104">SYNTAX</span></span>

```
Get-AzureLocalNetworkGateway [-GatewayId <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a6d37-105">說明</span><span class="sxs-lookup"><span data-stu-id="a6d37-105">DESCRIPTION</span></span>
<span data-ttu-id="a6d37-106">**AzureLocalNetworkGateway** Cmdlet 會取得本機網路閘道。</span><span class="sxs-lookup"><span data-stu-id="a6d37-106">The **Get-AzureLocalNetworkGateway** cmdlet gets a local network gateway.</span></span>

## <span data-ttu-id="a6d37-107">示例</span><span class="sxs-lookup"><span data-stu-id="a6d37-107">EXAMPLES</span></span>

## <span data-ttu-id="a6d37-108">參數</span><span class="sxs-lookup"><span data-stu-id="a6d37-108">PARAMETERS</span></span>

### <span data-ttu-id="a6d37-109">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="a6d37-109">-GatewayId</span></span>
<span data-ttu-id="a6d37-110">指定要取得的閘道識別碼。</span><span class="sxs-lookup"><span data-stu-id="a6d37-110">Specifies the ID of the gateway to get.</span></span>

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

### <span data-ttu-id="a6d37-111">-設定檔</span><span class="sxs-lookup"><span data-stu-id="a6d37-111">-Profile</span></span>
<span data-ttu-id="a6d37-112">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a6d37-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a6d37-113">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="a6d37-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a6d37-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6d37-114">CommonParameters</span></span>
<span data-ttu-id="a6d37-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a6d37-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6d37-116">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a6d37-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6d37-117">輸入</span><span class="sxs-lookup"><span data-stu-id="a6d37-117">INPUTS</span></span>

## <span data-ttu-id="a6d37-118">輸出</span><span class="sxs-lookup"><span data-stu-id="a6d37-118">OUTPUTS</span></span>

## <span data-ttu-id="a6d37-119">筆記</span><span class="sxs-lookup"><span data-stu-id="a6d37-119">NOTES</span></span>

## <span data-ttu-id="a6d37-120">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6d37-120">RELATED LINKS</span></span>

[<span data-ttu-id="a6d37-121">新-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a6d37-121">New-AzureLocalNetworkGateway</span></span>](./New-AzureLocalNetworkGateway.md)

[<span data-ttu-id="a6d37-122">移除-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a6d37-122">Remove-AzureLocalNetworkGateway</span></span>](./Remove-AzureLocalNetworkGateway.md)

[<span data-ttu-id="a6d37-123">Reset-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a6d37-123">Reset-AzureLocalNetworkGateway</span></span>](./Reset-AzureLocalNetworkGateway.md)
