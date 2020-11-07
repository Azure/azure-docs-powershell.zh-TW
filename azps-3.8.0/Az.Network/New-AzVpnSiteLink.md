---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
ms.openlocfilehash: 68df4cd7dc1149b7bb62a148ff7c649ed2418db8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956957"
---
# <span data-ttu-id="d31e0-101">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="d31e0-101">New-AzVpnSiteLink</span></span>

## <span data-ttu-id="d31e0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d31e0-102">SYNOPSIS</span></span>
<span data-ttu-id="d31e0-103">建立 Azure VpnSiteLink 物件。</span><span class="sxs-lookup"><span data-stu-id="d31e0-103">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="d31e0-104">句法</span><span class="sxs-lookup"><span data-stu-id="d31e0-104">SYNTAX</span></span>

### <span data-ttu-id="d31e0-105">ByVpnSiteLinkIpAddress</span><span class="sxs-lookup"><span data-stu-id="d31e0-105">ByVpnSiteLinkIpAddress</span></span>
```
New-AzVpnSiteLink -Name <String> -IPAddress <String> [-LinkProviderName <String>] [-LinkSpeedInMbps <UInt32>]
 [-BGPAsn <UInt32>] [-BGPPeeringAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d31e0-106">ByVpnSiteLinkFqdn</span><span class="sxs-lookup"><span data-stu-id="d31e0-106">ByVpnSiteLinkFqdn</span></span>
```
New-AzVpnSiteLink -Name <String> -Fqdn <String> [-LinkProviderName <String>] [-LinkSpeedInMbps <UInt32>]
 [-BGPAsn <UInt32>] [-BGPPeeringAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d31e0-107">說明</span><span class="sxs-lookup"><span data-stu-id="d31e0-107">DESCRIPTION</span></span>
<span data-ttu-id="d31e0-108">建立 Azure VpnSiteLink 物件。</span><span class="sxs-lookup"><span data-stu-id="d31e0-108">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="d31e0-109">示例</span><span class="sxs-lookup"><span data-stu-id="d31e0-109">EXAMPLES</span></span>

### <span data-ttu-id="d31e0-110">範例1</span><span class="sxs-lookup"><span data-stu-id="d31e0-110">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink)
```

<span data-ttu-id="d31e0-111">上述將會建立一個資源群組、虛擬 WAN，以及在 Azure 中的 [testRG] 資源群組中，有 1 VpnSiteLinks 的 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="d31e0-111">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>

## <span data-ttu-id="d31e0-112">參數</span><span class="sxs-lookup"><span data-stu-id="d31e0-112">PARAMETERS</span></span>

### <span data-ttu-id="d31e0-113">-BGPAsn</span><span class="sxs-lookup"><span data-stu-id="d31e0-113">-BGPAsn</span></span>
<span data-ttu-id="d31e0-114">此 VpnSiteLink 的 BGP ASN。</span><span class="sxs-lookup"><span data-stu-id="d31e0-114">The BGP ASN for this VpnSiteLink.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d31e0-115">-BGPPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="d31e0-115">-BGPPeeringAddress</span></span>
<span data-ttu-id="d31e0-116">此 VpnSiteLink 的 BGP 對等位址。</span><span class="sxs-lookup"><span data-stu-id="d31e0-116">The BGP Peering Address for this VpnSiteLink.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d31e0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d31e0-117">-DefaultProfile</span></span>
<span data-ttu-id="d31e0-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d31e0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d31e0-119">-Fqdn</span><span class="sxs-lookup"><span data-stu-id="d31e0-119">-Fqdn</span></span>
<span data-ttu-id="d31e0-120">下一個躍點 Fqdn。</span><span class="sxs-lookup"><span data-stu-id="d31e0-120">The Next Hop Fqdn.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteLinkFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d31e0-121">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="d31e0-121">-IPAddress</span></span>
<span data-ttu-id="d31e0-122">下一個躍點 Ip 位址。</span><span class="sxs-lookup"><span data-stu-id="d31e0-122">The Next Hop IpAddress.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteLinkIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d31e0-123">-LinkProviderName</span><span class="sxs-lookup"><span data-stu-id="d31e0-123">-LinkProviderName</span></span>
<span data-ttu-id="d31e0-124">連結提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="d31e0-124">Link Provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d31e0-125">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="d31e0-125">-LinkSpeedInMbps</span></span>
<span data-ttu-id="d31e0-126">連結速度（以 Mbps 為單位）。</span><span class="sxs-lookup"><span data-stu-id="d31e0-126">Link Speed In Mbps.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d31e0-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="d31e0-127">-Name</span></span>
<span data-ttu-id="d31e0-128">列名</span><span class="sxs-lookup"><span data-stu-id="d31e0-128">Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d31e0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d31e0-129">CommonParameters</span></span>
<span data-ttu-id="d31e0-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d31e0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d31e0-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d31e0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d31e0-132">輸入</span><span class="sxs-lookup"><span data-stu-id="d31e0-132">INPUTS</span></span>

### <span data-ttu-id="d31e0-133">所有</span><span class="sxs-lookup"><span data-stu-id="d31e0-133">None</span></span>

## <span data-ttu-id="d31e0-134">輸出</span><span class="sxs-lookup"><span data-stu-id="d31e0-134">OUTPUTS</span></span>

### <span data-ttu-id="d31e0-135">PSVpnSiteLink 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d31e0-135">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="d31e0-136">筆記</span><span class="sxs-lookup"><span data-stu-id="d31e0-136">NOTES</span></span>

## <span data-ttu-id="d31e0-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="d31e0-137">RELATED LINKS</span></span>

[<span data-ttu-id="d31e0-138">新-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="d31e0-138">New-AzVpnSite</span></span>](./New-AzVpnSite.md)