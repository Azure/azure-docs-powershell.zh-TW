---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7B749B29-9820-4E23-B5AF-F5535251629A
online version: ''
schema: 2.0.0
ms.openlocfilehash: ec94df29fb23dd7c82d79304c2e48aab225ed224
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967733"
---
# <span data-ttu-id="5c0da-101">Get-AzureVNetConnection</span><span class="sxs-lookup"><span data-stu-id="5c0da-101">Get-AzureVNetConnection</span></span>

## <span data-ttu-id="5c0da-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5c0da-102">SYNOPSIS</span></span>
<span data-ttu-id="5c0da-103">取得 Azure 虛擬網路的連線。</span><span class="sxs-lookup"><span data-stu-id="5c0da-103">Gets connections to an Azure virtual network.</span></span>

## <span data-ttu-id="5c0da-104">句法</span><span class="sxs-lookup"><span data-stu-id="5c0da-104">SYNTAX</span></span>

```
Get-AzureVNetConnection -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5c0da-105">說明</span><span class="sxs-lookup"><span data-stu-id="5c0da-105">DESCRIPTION</span></span>
<span data-ttu-id="5c0da-106">**AzureVNetConnection** Cmdlet 會傳回指定所有活動虛擬私人網路絡的物件， (VPN) 連線至 Azure 虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="5c0da-106">The **Get-AzureVNetConnection** cmdlet returns an object that specifies all active virtual private network (VPN) connections to an Azure virtual network.</span></span>
<span data-ttu-id="5c0da-107">VPN 連線包括跨平臺內部部署點對點 Vpn 和虛擬網路至虛擬網路連線。</span><span class="sxs-lookup"><span data-stu-id="5c0da-107">VPN connections include cross premises site-to-site VPNs and virtual network to virtual network connections.</span></span>

## <span data-ttu-id="5c0da-108">示例</span><span class="sxs-lookup"><span data-stu-id="5c0da-108">EXAMPLES</span></span>

## <span data-ttu-id="5c0da-109">參數</span><span class="sxs-lookup"><span data-stu-id="5c0da-109">PARAMETERS</span></span>

### <span data-ttu-id="5c0da-110">-設定檔</span><span class="sxs-lookup"><span data-stu-id="5c0da-110">-Profile</span></span>
<span data-ttu-id="5c0da-111">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="5c0da-111">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5c0da-112">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="5c0da-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5c0da-113">-VNetName</span><span class="sxs-lookup"><span data-stu-id="5c0da-113">-VNetName</span></span>
<span data-ttu-id="5c0da-114">指定這個 Cmdlet 傳回連線的虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="5c0da-114">Specifies the name of the virtual network from which this cmdlet returns connections.</span></span>

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

### <span data-ttu-id="5c0da-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c0da-115">CommonParameters</span></span>
<span data-ttu-id="5c0da-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5c0da-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c0da-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5c0da-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c0da-118">輸入</span><span class="sxs-lookup"><span data-stu-id="5c0da-118">INPUTS</span></span>

## <span data-ttu-id="5c0da-119">輸出</span><span class="sxs-lookup"><span data-stu-id="5c0da-119">OUTPUTS</span></span>

## <span data-ttu-id="5c0da-120">筆記</span><span class="sxs-lookup"><span data-stu-id="5c0da-120">NOTES</span></span>

## <span data-ttu-id="5c0da-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="5c0da-121">RELATED LINKS</span></span>

