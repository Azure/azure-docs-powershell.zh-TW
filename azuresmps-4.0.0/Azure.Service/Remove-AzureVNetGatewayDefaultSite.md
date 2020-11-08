---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 67260128-D57B-4587-BB61-2475703ABA66
online version: ''
schema: 2.0.0
ms.openlocfilehash: 38aca36799c57dd5a135af99e4b99ab713d2b1ca
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966935"
---
# <span data-ttu-id="c7bd3-101">Remove-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="c7bd3-101">Remove-AzureVNetGatewayDefaultSite</span></span>

## <span data-ttu-id="c7bd3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c7bd3-102">SYNOPSIS</span></span>
<span data-ttu-id="c7bd3-103">移除強制隧道流量的預設路由。</span><span class="sxs-lookup"><span data-stu-id="c7bd3-103">Removes the default route for forced tunneling traffic.</span></span>

## <span data-ttu-id="c7bd3-104">句法</span><span class="sxs-lookup"><span data-stu-id="c7bd3-104">SYNTAX</span></span>

```
Remove-AzureVNetGatewayDefaultSite -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c7bd3-105">說明</span><span class="sxs-lookup"><span data-stu-id="c7bd3-105">DESCRIPTION</span></span>
<span data-ttu-id="c7bd3-106">**AzureVNetGatewayDefaultSite** Cmdlet 會移除預設路由至內部部署網站，以強制進行隧道流量。</span><span class="sxs-lookup"><span data-stu-id="c7bd3-106">The **Remove-AzureVNetGatewayDefaultSite** cmdlet removes the default route to the on-premises site for forced tunneling traffic.</span></span>
<span data-ttu-id="c7bd3-107">這個 Cmdlet 會從 Azure 虛擬私人網路 (VPN) 閘道（針對虛擬網路）移除路由。</span><span class="sxs-lookup"><span data-stu-id="c7bd3-107">This cmdlet removes the route from an Azure virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="c7bd3-108">示例</span><span class="sxs-lookup"><span data-stu-id="c7bd3-108">EXAMPLES</span></span>

### <span data-ttu-id="c7bd3-109">範例1：移除預設網站的路由</span><span class="sxs-lookup"><span data-stu-id="c7bd3-109">Example 1: Remove a route to the default site</span></span>
```
PS C:\> Remove-AzureVNetGatewayDefaultSite -VnetName "ContosoVNet01"
```

<span data-ttu-id="c7bd3-110">這個命令會從名為 ContosoVNet01 的虛擬網路 VPN 移除預設網站的路由。</span><span class="sxs-lookup"><span data-stu-id="c7bd3-110">This command removes the route to the default site from the VPN of the virtual network named ContosoVNet01.</span></span>

## <span data-ttu-id="c7bd3-111">參數</span><span class="sxs-lookup"><span data-stu-id="c7bd3-111">PARAMETERS</span></span>

### <span data-ttu-id="c7bd3-112">-設定檔</span><span class="sxs-lookup"><span data-stu-id="c7bd3-112">-Profile</span></span>
<span data-ttu-id="c7bd3-113">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="c7bd3-113">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c7bd3-114">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="c7bd3-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c7bd3-115">-VNetName</span><span class="sxs-lookup"><span data-stu-id="c7bd3-115">-VNetName</span></span>
<span data-ttu-id="c7bd3-116">指定虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="c7bd3-116">Specifies a virtual network.</span></span>
<span data-ttu-id="c7bd3-117">這個 Cmdlet 會移除此參數指定之虛擬網路之 VPN 閘道的預設路由。</span><span class="sxs-lookup"><span data-stu-id="c7bd3-117">This cmdlet removes the default route from the VPN gateway for the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="c7bd3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7bd3-118">CommonParameters</span></span>
<span data-ttu-id="c7bd3-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c7bd3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7bd3-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c7bd3-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7bd3-121">輸入</span><span class="sxs-lookup"><span data-stu-id="c7bd3-121">INPUTS</span></span>

## <span data-ttu-id="c7bd3-122">輸出</span><span class="sxs-lookup"><span data-stu-id="c7bd3-122">OUTPUTS</span></span>

## <span data-ttu-id="c7bd3-123">筆記</span><span class="sxs-lookup"><span data-stu-id="c7bd3-123">NOTES</span></span>

## <span data-ttu-id="c7bd3-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="c7bd3-124">RELATED LINKS</span></span>

[<span data-ttu-id="c7bd3-125">Set-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="c7bd3-125">Set-AzureVNetGatewayDefaultSite</span></span>](./Set-AzureVNetGatewayDefaultSite.md)