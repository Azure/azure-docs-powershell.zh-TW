---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A34A2B01-A658-410E-8B68-98A6427DFC33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 345d9048ea729b6fe954d2da5e01310be42c79ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967859"
---
# <span data-ttu-id="543e1-101">Set-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="543e1-101">Set-AzureVNetGatewayDefaultSite</span></span>

## <span data-ttu-id="543e1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="543e1-102">SYNOPSIS</span></span>
<span data-ttu-id="543e1-103">設定強制隧道流量的預設網站。</span><span class="sxs-lookup"><span data-stu-id="543e1-103">Sets the default site for forced tunneling traffic.</span></span>

## <span data-ttu-id="543e1-104">句法</span><span class="sxs-lookup"><span data-stu-id="543e1-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayDefaultSite -VNetName <String> -DefaultSite <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="543e1-105">說明</span><span class="sxs-lookup"><span data-stu-id="543e1-105">DESCRIPTION</span></span>
<span data-ttu-id="543e1-106">**AzureVNetGatewayDefaultSite** Cmdlet 會將預設路由設定為可強制進行隧道通訊的內部部署網站。</span><span class="sxs-lookup"><span data-stu-id="543e1-106">The **Set-AzureVNetGatewayDefaultSite** cmdlet sets the default route to the on-premises site for forced tunneling traffic.</span></span>
<span data-ttu-id="543e1-107">這個命令會在虛擬網路 (VPN) 閘道的 Azure 虛擬私人網路絡上，設定路由。</span><span class="sxs-lookup"><span data-stu-id="543e1-107">This command sets the route on an Azure virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="543e1-108">示例</span><span class="sxs-lookup"><span data-stu-id="543e1-108">EXAMPLES</span></span>

## <span data-ttu-id="543e1-109">參數</span><span class="sxs-lookup"><span data-stu-id="543e1-109">PARAMETERS</span></span>

### <span data-ttu-id="543e1-110">-DefaultSite</span><span class="sxs-lookup"><span data-stu-id="543e1-110">-DefaultSite</span></span>
<span data-ttu-id="543e1-111">指定強制隧道流量的內部部署本機網路網站名稱。</span><span class="sxs-lookup"><span data-stu-id="543e1-111">Specifies the name of the on-premises local network site for forced tunneling traffic.</span></span>

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

### <span data-ttu-id="543e1-112">-設定檔</span><span class="sxs-lookup"><span data-stu-id="543e1-112">-Profile</span></span>
<span data-ttu-id="543e1-113">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="543e1-113">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="543e1-114">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="543e1-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="543e1-115">-VNetName</span><span class="sxs-lookup"><span data-stu-id="543e1-115">-VNetName</span></span>
<span data-ttu-id="543e1-116">指定虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="543e1-116">Specifies a virtual network.</span></span>
<span data-ttu-id="543e1-117">此 Cmdlet 會針對此參數指定的虛擬網路設定強制隧道流量的預設路由。</span><span class="sxs-lookup"><span data-stu-id="543e1-117">This cmdlet sets the default route of the VPN gateway for forced tunneling traffic for the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="543e1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="543e1-118">CommonParameters</span></span>
<span data-ttu-id="543e1-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="543e1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="543e1-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="543e1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="543e1-121">輸入</span><span class="sxs-lookup"><span data-stu-id="543e1-121">INPUTS</span></span>

## <span data-ttu-id="543e1-122">輸出</span><span class="sxs-lookup"><span data-stu-id="543e1-122">OUTPUTS</span></span>

## <span data-ttu-id="543e1-123">筆記</span><span class="sxs-lookup"><span data-stu-id="543e1-123">NOTES</span></span>

## <span data-ttu-id="543e1-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="543e1-124">RELATED LINKS</span></span>

[<span data-ttu-id="543e1-125">移除-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="543e1-125">Remove-AzureVNetGatewayDefaultSite</span></span>](./Remove-AzureVNetGatewayDefaultSite.md)
