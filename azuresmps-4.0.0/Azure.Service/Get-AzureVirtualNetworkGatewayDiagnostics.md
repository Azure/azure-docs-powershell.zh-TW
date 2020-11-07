---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: F6A89D39-18AD-4087-823C-63FA0A3690E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 36c51d0ceae42aab50e2df9e0532c98dd6800747
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967966"
---
# <span data-ttu-id="05a4c-101">Get-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="05a4c-101">Get-AzureVirtualNetworkGatewayDiagnostics</span></span>

## <span data-ttu-id="05a4c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="05a4c-102">SYNOPSIS</span></span>
<span data-ttu-id="05a4c-103">取得 Azure 虛擬網路閘道診斷的結果。</span><span class="sxs-lookup"><span data-stu-id="05a4c-103">Gets the results of Azure virtual network gateway diagnostics.</span></span>

## <span data-ttu-id="05a4c-104">句法</span><span class="sxs-lookup"><span data-stu-id="05a4c-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="05a4c-105">說明</span><span class="sxs-lookup"><span data-stu-id="05a4c-105">DESCRIPTION</span></span>
<span data-ttu-id="05a4c-106">**AzureVirtualNetworkGatewayDiagnostics** Cmdlet 會取得 Azure 虛擬網路閘道診斷的結果。</span><span class="sxs-lookup"><span data-stu-id="05a4c-106">The **Get-AzureVirtualNetworkGatewayDiagnostics** cmdlet gets the results of Azure virtual network gateway diagnostics.</span></span>

## <span data-ttu-id="05a4c-107">示例</span><span class="sxs-lookup"><span data-stu-id="05a4c-107">EXAMPLES</span></span>

## <span data-ttu-id="05a4c-108">參數</span><span class="sxs-lookup"><span data-stu-id="05a4c-108">PARAMETERS</span></span>

### <span data-ttu-id="05a4c-109">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="05a4c-109">-GatewayId</span></span>
<span data-ttu-id="05a4c-110">指定閘道的 ID。</span><span class="sxs-lookup"><span data-stu-id="05a4c-110">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="05a4c-111">-設定檔</span><span class="sxs-lookup"><span data-stu-id="05a4c-111">-Profile</span></span>
<span data-ttu-id="05a4c-112">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="05a4c-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="05a4c-113">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="05a4c-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="05a4c-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05a4c-114">CommonParameters</span></span>
<span data-ttu-id="05a4c-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="05a4c-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05a4c-116">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="05a4c-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05a4c-117">輸入</span><span class="sxs-lookup"><span data-stu-id="05a4c-117">INPUTS</span></span>

## <span data-ttu-id="05a4c-118">輸出</span><span class="sxs-lookup"><span data-stu-id="05a4c-118">OUTPUTS</span></span>

## <span data-ttu-id="05a4c-119">筆記</span><span class="sxs-lookup"><span data-stu-id="05a4c-119">NOTES</span></span>

## <span data-ttu-id="05a4c-120">相關連結</span><span class="sxs-lookup"><span data-stu-id="05a4c-120">RELATED LINKS</span></span>

[<span data-ttu-id="05a4c-121">開始-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="05a4c-121">Start-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Start-AzureVirtualNetworkGatewayDiagnostics.md)

[<span data-ttu-id="05a4c-122">停止 AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="05a4c-122">Stop-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Stop-AzureVirtualNetworkGatewayDiagnostics.md)


