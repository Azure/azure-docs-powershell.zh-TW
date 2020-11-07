---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 70899AAC-BF64-4FFA-9DAF-92E859D0B271
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3b30172f947c1c8bf39a8be84039d9166d6ea290
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967860"
---
# <span data-ttu-id="052f4-101">Set-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="052f4-101">Set-AzureVNetGateway</span></span>

## <span data-ttu-id="052f4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="052f4-102">SYNOPSIS</span></span>
<span data-ttu-id="052f4-103">啟用或停用 Azure 虛擬網路的 VPN 閘道。</span><span class="sxs-lookup"><span data-stu-id="052f4-103">Enables or disables a VPN gateway for an Azure virtual network.</span></span>

## <span data-ttu-id="052f4-104">句法</span><span class="sxs-lookup"><span data-stu-id="052f4-104">SYNTAX</span></span>

### <span data-ttu-id="052f4-105">連接 (預設) </span><span class="sxs-lookup"><span data-stu-id="052f4-105">Connect (Default)</span></span>
```
Set-AzureVNetGateway [-Connect] -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="052f4-106">卸下</span><span class="sxs-lookup"><span data-stu-id="052f4-106">Disconnect</span></span>
```
Set-AzureVNetGateway [-Disconnect] -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="052f4-107">說明</span><span class="sxs-lookup"><span data-stu-id="052f4-107">DESCRIPTION</span></span>
<span data-ttu-id="052f4-108">**AzureVNetGateway** Cmdlet 可啟用或停用 Azure 虛擬網路 (VPN) 閘道的虛擬私人網路絡。</span><span class="sxs-lookup"><span data-stu-id="052f4-108">The **Set-AzureVNetGateway** cmdlet enables or disables a virtual private network (VPN) gateway for an Azure virtual network.</span></span>
<span data-ttu-id="052f4-109">虛擬網路閘道是用來連線至虛擬網路的 VPN 端點。</span><span class="sxs-lookup"><span data-stu-id="052f4-109">A virtual network gateway is a VPN endpoint for connecting to a virtual network.</span></span>
<span data-ttu-id="052f4-110">指定 [連線 *]* 或 *[中斷連接]* 參數，以啟用或停用內部部署本機網路網站與虛擬網路之間的 VPN 連線。</span><span class="sxs-lookup"><span data-stu-id="052f4-110">Specify the *Connect* or *Disconnect* parameter to enable or disable the VPN connection between an on-premises local network site and a virtual network.</span></span>

## <span data-ttu-id="052f4-111">示例</span><span class="sxs-lookup"><span data-stu-id="052f4-111">EXAMPLES</span></span>

### <span data-ttu-id="052f4-112">範例1：為虛擬網路啟用虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="052f4-112">Example 1: Enable a virtual network gateway for a virtual network</span></span>
```
PS C:\> Set-AzureVNetGateway -Connect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

<span data-ttu-id="052f4-113">這個命令會在名為 ContosoProdNet 的 Azure 虛擬網路或名為 ContosoBranchOffice 的本機網路網站的 VPN 裝置之間啟用虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="052f4-113">This command enables the virtual network gateway between the Azure virtual network named ContosoProdNet and the VPN device for the local network site named ContosoBranchOffice.</span></span>

### <span data-ttu-id="052f4-114">範例2：停用虛擬網路的虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="052f4-114">Example 2: Disable a virtual network gateway for a virtual network</span></span>
```
PS C:\> Set-AzureVNetGateway -Disconnect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

<span data-ttu-id="052f4-115">這個命令會停用名為 ContosoProdNet 的 Azure 虛擬網路閘道與名為 ContosoBranchOffice 之區域網路網站之 VPN 裝置之間的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="052f4-115">This command disables the virtual network gateway between the Azure virtual network named ContosoProdNet and the VPN device for the local network site named ContosoBranchOffice.</span></span>

## <span data-ttu-id="052f4-116">參數</span><span class="sxs-lookup"><span data-stu-id="052f4-116">PARAMETERS</span></span>

### <span data-ttu-id="052f4-117">-連接</span><span class="sxs-lookup"><span data-stu-id="052f4-117">-Connect</span></span>
<span data-ttu-id="052f4-118">表示此 Cmdlet 啟用虛擬網路與本機網路網站之間的 VPN 連線。</span><span class="sxs-lookup"><span data-stu-id="052f4-118">Indicates that this cmdlet enables the VPN connection between a virtual network and a local network site.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Connect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="052f4-119">中斷連線</span><span class="sxs-lookup"><span data-stu-id="052f4-119">-Disconnect</span></span>
<span data-ttu-id="052f4-120">表示此 Cmdlet 會停用虛擬網路與本機網路網站之間的 VPN 連線。</span><span class="sxs-lookup"><span data-stu-id="052f4-120">Indicates that this cmdlet disables the VPN connection between a virtual network and a local network site.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disconnect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="052f4-121">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="052f4-121">-LocalNetworkSiteName</span></span>
<span data-ttu-id="052f4-122">指定此 Cmdlet 啟用或停用 VPN 連線之內部部署本機網路網站的名稱。</span><span class="sxs-lookup"><span data-stu-id="052f4-122">Specifies the name of the on-premises local network site for which this cmdlet enables or disables the VPN connection.</span></span>

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

### <span data-ttu-id="052f4-123">-設定檔</span><span class="sxs-lookup"><span data-stu-id="052f4-123">-Profile</span></span>
<span data-ttu-id="052f4-124">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="052f4-124">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="052f4-125">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="052f4-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="052f4-126">-VNetName</span><span class="sxs-lookup"><span data-stu-id="052f4-126">-VNetName</span></span>
<span data-ttu-id="052f4-127">指定此 Cmdlet 啟用或停用 VPN 連線的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="052f4-127">Specifies the virtual network for which this cmdlet enables or disables the VPN connection.</span></span>

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

### <span data-ttu-id="052f4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="052f4-128">CommonParameters</span></span>
<span data-ttu-id="052f4-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="052f4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="052f4-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="052f4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="052f4-131">輸入</span><span class="sxs-lookup"><span data-stu-id="052f4-131">INPUTS</span></span>

## <span data-ttu-id="052f4-132">輸出</span><span class="sxs-lookup"><span data-stu-id="052f4-132">OUTPUTS</span></span>

## <span data-ttu-id="052f4-133">筆記</span><span class="sxs-lookup"><span data-stu-id="052f4-133">NOTES</span></span>

## <span data-ttu-id="052f4-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="052f4-134">RELATED LINKS</span></span>

[<span data-ttu-id="052f4-135">AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="052f4-135">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="052f4-136">新-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="052f4-136">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="052f4-137">移除-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="052f4-137">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="052f4-138">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="052f4-138">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="052f4-139">調整大小-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="052f4-139">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)


