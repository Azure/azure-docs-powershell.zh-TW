---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9E7A170D-512A-4117-85C3-3AA4D6341C6B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 97fe847fd183caa7de281b358da579e8df4d5831
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967186"
---
# <span data-ttu-id="7a599-101">Stop-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="7a599-101">Stop-AzureVirtualNetworkGatewayDiagnostics</span></span>

## <span data-ttu-id="7a599-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7a599-102">SYNOPSIS</span></span>
<span data-ttu-id="7a599-103">停止正在執行的虛擬網路閘道診斷會話。</span><span class="sxs-lookup"><span data-stu-id="7a599-103">Stops a running virtual network gateway diagnostics session.</span></span>

## <span data-ttu-id="7a599-104">句法</span><span class="sxs-lookup"><span data-stu-id="7a599-104">SYNTAX</span></span>

```
Stop-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7a599-105">說明</span><span class="sxs-lookup"><span data-stu-id="7a599-105">DESCRIPTION</span></span>
<span data-ttu-id="7a599-106">**AzureVirtualNetworkGatewayDiagnostics** Cmdlet 會停止正在執行的虛擬網路閘道診斷會話。</span><span class="sxs-lookup"><span data-stu-id="7a599-106">The **Stop-AzureVirtualNetworkGatewayDiagnostics** cmdlet stops a running virtual network gateway diagnostics session.</span></span>
<span data-ttu-id="7a599-107">這個命令會將診斷會話的結果儲存至 Start-AzureVirtualNetworkGatewayDiagnostics Cmdlet 所指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="7a599-107">This command saves the results of the diagnostics session to the storage account that the Start-AzureVirtualNetworkGatewayDiagnostics cmdlet specifies.</span></span>

## <span data-ttu-id="7a599-108">示例</span><span class="sxs-lookup"><span data-stu-id="7a599-108">EXAMPLES</span></span>

## <span data-ttu-id="7a599-109">參數</span><span class="sxs-lookup"><span data-stu-id="7a599-109">PARAMETERS</span></span>

### <span data-ttu-id="7a599-110">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="7a599-110">-GatewayId</span></span>
<span data-ttu-id="7a599-111">指定閘道的 ID。</span><span class="sxs-lookup"><span data-stu-id="7a599-111">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="7a599-112">-設定檔</span><span class="sxs-lookup"><span data-stu-id="7a599-112">-Profile</span></span>
<span data-ttu-id="7a599-113">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="7a599-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="7a599-114">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="7a599-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7a599-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a599-115">CommonParameters</span></span>
<span data-ttu-id="7a599-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7a599-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a599-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7a599-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a599-118">輸入</span><span class="sxs-lookup"><span data-stu-id="7a599-118">INPUTS</span></span>

## <span data-ttu-id="7a599-119">輸出</span><span class="sxs-lookup"><span data-stu-id="7a599-119">OUTPUTS</span></span>

## <span data-ttu-id="7a599-120">筆記</span><span class="sxs-lookup"><span data-stu-id="7a599-120">NOTES</span></span>

## <span data-ttu-id="7a599-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="7a599-121">RELATED LINKS</span></span>

[<span data-ttu-id="7a599-122">AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="7a599-122">Get-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Get-AzureVirtualNetworkGatewayDiagnostics.md)

[<span data-ttu-id="7a599-123">開始-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="7a599-123">Start-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Start-AzureVirtualNetworkGatewayDiagnostics.md)


