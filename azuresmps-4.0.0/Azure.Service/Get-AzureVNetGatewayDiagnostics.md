---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 22E8CB18-8CDD-4992-AB81-E1BB400E6BC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 294e931529b7de939a6a5c20181d48b18da1e892
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967723"
---
# <span data-ttu-id="9eab5-101">Get-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="9eab5-101">Get-AzureVNetGatewayDiagnostics</span></span>

## <span data-ttu-id="9eab5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9eab5-102">SYNOPSIS</span></span>
<span data-ttu-id="9eab5-103">取得虛擬網路閘道的目前診斷狀態。</span><span class="sxs-lookup"><span data-stu-id="9eab5-103">Gets the current state of diagnostics for a virtual network gateway.</span></span>

## <span data-ttu-id="9eab5-104">句法</span><span class="sxs-lookup"><span data-stu-id="9eab5-104">SYNTAX</span></span>

```
Get-AzureVNetGatewayDiagnostics -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9eab5-105">說明</span><span class="sxs-lookup"><span data-stu-id="9eab5-105">DESCRIPTION</span></span>
<span data-ttu-id="9eab5-106">**AzureVNetGatewayDiagnostics** Cmdlet 會取得虛擬閘道的目前診斷狀態。</span><span class="sxs-lookup"><span data-stu-id="9eab5-106">The **Get-AzureVNetGatewayDiagnostics** cmdlet gets the current state of diagnostics for a virtual network gateway.</span></span>
<span data-ttu-id="9eab5-107">如果 (blob) 存在二進位大型物件，且 **AzureVNetGatewayDiagnostics** 已儲存先前的診斷會話，這個 Cmdlet 也會傳回該 Cmdlet 儲存該診斷會話的 blob URL。</span><span class="sxs-lookup"><span data-stu-id="9eab5-107">If a binary large object (blob) exists where the **Start-AzureVNetGatewayDiagnostics** saved a previous diagnostics session, this cmdlet also returns the URL of the blob where that cmdlet saved that diagnostics session.</span></span>

## <span data-ttu-id="9eab5-108">示例</span><span class="sxs-lookup"><span data-stu-id="9eab5-108">EXAMPLES</span></span>

## <span data-ttu-id="9eab5-109">參數</span><span class="sxs-lookup"><span data-stu-id="9eab5-109">PARAMETERS</span></span>

### <span data-ttu-id="9eab5-110">-設定檔</span><span class="sxs-lookup"><span data-stu-id="9eab5-110">-Profile</span></span>
<span data-ttu-id="9eab5-111">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="9eab5-111">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="9eab5-112">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="9eab5-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9eab5-113">-VNetName</span><span class="sxs-lookup"><span data-stu-id="9eab5-113">-VNetName</span></span>
<span data-ttu-id="9eab5-114">指定包含此 Cmdlet 為其提供診斷的虛擬網路閘道的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="9eab5-114">Specifies the virtual network that contains a virtual network gateway for which this cmdlet gets diagnostics.</span></span>

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

### <span data-ttu-id="9eab5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eab5-115">CommonParameters</span></span>
<span data-ttu-id="9eab5-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9eab5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eab5-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9eab5-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eab5-118">輸入</span><span class="sxs-lookup"><span data-stu-id="9eab5-118">INPUTS</span></span>

## <span data-ttu-id="9eab5-119">輸出</span><span class="sxs-lookup"><span data-stu-id="9eab5-119">OUTPUTS</span></span>

## <span data-ttu-id="9eab5-120">筆記</span><span class="sxs-lookup"><span data-stu-id="9eab5-120">NOTES</span></span>

## <span data-ttu-id="9eab5-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="9eab5-121">RELATED LINKS</span></span>

[<span data-ttu-id="9eab5-122">開始-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="9eab5-122">Start-AzureVNetGatewayDiagnostics</span></span>](./Start-AzureVNetGatewayDiagnostics.md)

[<span data-ttu-id="9eab5-123">停止 AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="9eab5-123">Stop-AzureVNetGatewayDiagnostics</span></span>](./Stop-AzureVNetGatewayDiagnostics.md)


