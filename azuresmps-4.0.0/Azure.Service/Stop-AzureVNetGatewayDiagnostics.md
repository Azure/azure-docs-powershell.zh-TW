---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 706CBF65-C796-4525-BAEB-AAFAD44C0464
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37c2ce3b32d23f7c5bb682d2116de84cc90f047
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967465"
---
# <span data-ttu-id="f5a21-101">Stop-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="f5a21-101">Stop-AzureVNetGatewayDiagnostics</span></span>

## <span data-ttu-id="f5a21-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f5a21-102">SYNOPSIS</span></span>
<span data-ttu-id="f5a21-103">停止執行中的 VPN 閘道診斷會話。</span><span class="sxs-lookup"><span data-stu-id="f5a21-103">Stops a running VPN gateway diagnostics session.</span></span>

## <span data-ttu-id="f5a21-104">句法</span><span class="sxs-lookup"><span data-stu-id="f5a21-104">SYNTAX</span></span>

```
Stop-AzureVNetGatewayDiagnostics -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f5a21-105">說明</span><span class="sxs-lookup"><span data-stu-id="f5a21-105">DESCRIPTION</span></span>
<span data-ttu-id="f5a21-106">**Stop-AzureVNetGatewayDiagnostics** Cmdlet 會停止執行虛擬私人網路 (VPN) 閘道診斷會話。</span><span class="sxs-lookup"><span data-stu-id="f5a21-106">The **Stop-AzureVNetGatewayDiagnostics** cmdlet stops a running virtual private network (VPN) gateway diagnostics session.</span></span>
<span data-ttu-id="f5a21-107">這個命令會將診斷會話的結果儲存至 **Start AzureVNetGatewayDiagnostics** Cmdlet 指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="f5a21-107">This command saves the results of the diagnostics session to the storage account that the **Start-AzureVNetGatewayDiagnostics** cmdlet specifies.</span></span>

## <span data-ttu-id="f5a21-108">示例</span><span class="sxs-lookup"><span data-stu-id="f5a21-108">EXAMPLES</span></span>

## <span data-ttu-id="f5a21-109">參數</span><span class="sxs-lookup"><span data-stu-id="f5a21-109">PARAMETERS</span></span>

### <span data-ttu-id="f5a21-110">-設定檔</span><span class="sxs-lookup"><span data-stu-id="f5a21-110">-Profile</span></span>
<span data-ttu-id="f5a21-111">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="f5a21-111">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="f5a21-112">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="f5a21-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f5a21-113">-VNetName</span><span class="sxs-lookup"><span data-stu-id="f5a21-113">-VNetName</span></span>
<span data-ttu-id="f5a21-114">指定包含虛擬網路閘道的虛擬網路，此 Cmdlet 會停止診斷。</span><span class="sxs-lookup"><span data-stu-id="f5a21-114">Specifies the virtual network that contains a virtual network gateway for which this cmdlet stops diagnostics.</span></span>

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

### <span data-ttu-id="f5a21-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5a21-115">CommonParameters</span></span>
<span data-ttu-id="f5a21-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f5a21-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5a21-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f5a21-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5a21-118">輸入</span><span class="sxs-lookup"><span data-stu-id="f5a21-118">INPUTS</span></span>

## <span data-ttu-id="f5a21-119">輸出</span><span class="sxs-lookup"><span data-stu-id="f5a21-119">OUTPUTS</span></span>

## <span data-ttu-id="f5a21-120">筆記</span><span class="sxs-lookup"><span data-stu-id="f5a21-120">NOTES</span></span>

## <span data-ttu-id="f5a21-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5a21-121">RELATED LINKS</span></span>

[<span data-ttu-id="f5a21-122">AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="f5a21-122">Get-AzureVNetGatewayDiagnostics</span></span>](./Get-AzureVNetGatewayDiagnostics.md)

[<span data-ttu-id="f5a21-123">開始-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="f5a21-123">Start-AzureVNetGatewayDiagnostics</span></span>](./Start-AzureVNetGatewayDiagnostics.md)


