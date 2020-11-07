---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
ms.openlocfilehash: 7e53c6828fa5c7bae40037f2fd64bb06ddf0be45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789218"
---
# <span data-ttu-id="a0c6d-101">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="a0c6d-101">New-AzVpnSiteLink</span></span>

## <span data-ttu-id="a0c6d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a0c6d-102">SYNOPSIS</span></span>
<span data-ttu-id="a0c6d-103">建立 Azure VpnSiteLink 物件。</span><span class="sxs-lookup"><span data-stu-id="a0c6d-103">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="a0c6d-104">句法</span><span class="sxs-lookup"><span data-stu-id="a0c6d-104">SYNTAX</span></span>

```
New-AzVpnSiteLink -Name <String> -IPAddress <String> [-LinkProviderName <String>] [-LinkSpeedInMbps <UInt32>]
 [-BGPAsn <UInt32>] [-BGPPeeringAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a0c6d-105">說明</span><span class="sxs-lookup"><span data-stu-id="a0c6d-105">DESCRIPTION</span></span>
<span data-ttu-id="a0c6d-106">建立 Azure VpnSiteLink 物件。</span><span class="sxs-lookup"><span data-stu-id="a0c6d-106">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="a0c6d-107">示例</span><span class="sxs-lookup"><span data-stu-id="a0c6d-107">EXAMPLES</span></span>

### <span data-ttu-id="a0c6d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a0c6d-108">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink)
```

<span data-ttu-id="a0c6d-109">上述將會建立一個資源群組、虛擬 WAN，以及在 Azure 中的 [testRG] 資源群組中，有 1 VpnSiteLinks 的 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="a0c6d-109">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>

## <span data-ttu-id="a0c6d-110">參數</span><span class="sxs-lookup"><span data-stu-id="a0c6d-110">PARAMETERS</span></span>

### <span data-ttu-id="a0c6d-111">-BGPAsn</span><span class="sxs-lookup"><span data-stu-id="a0c6d-111">-BGPAsn</span></span>
<span data-ttu-id="a0c6d-112">此 VpnSiteLink 的 BGP ASN。</span><span class="sxs-lookup"><span data-stu-id="a0c6d-112">The BGP ASN for this VpnSiteLink.</span></span>

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

### <span data-ttu-id="a0c6d-113">-BGPPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="a0c6d-113">-BGPPeeringAddress</span></span>
<span data-ttu-id="a0c6d-114">此 VpnSiteLink 的 BGP 對等位址。</span><span class="sxs-lookup"><span data-stu-id="a0c6d-114">The BGP Peering Address for this VpnSiteLink.</span></span>

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

### <span data-ttu-id="a0c6d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0c6d-115">-DefaultProfile</span></span>
<span data-ttu-id="a0c6d-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a0c6d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0c6d-117">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="a0c6d-117">-IPAddress</span></span>
<span data-ttu-id="a0c6d-118">下一個躍點 Ip 位址。</span><span class="sxs-lookup"><span data-stu-id="a0c6d-118">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="a0c6d-119">-LinkProviderName</span><span class="sxs-lookup"><span data-stu-id="a0c6d-119">-LinkProviderName</span></span>
<span data-ttu-id="a0c6d-120">連結提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="a0c6d-120">Link Provider Name.</span></span>

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

### <span data-ttu-id="a0c6d-121">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="a0c6d-121">-LinkSpeedInMbps</span></span>
<span data-ttu-id="a0c6d-122">連結速度（以 Mbps 為單位）。</span><span class="sxs-lookup"><span data-stu-id="a0c6d-122">Link Speed In Mbps.</span></span>

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

### <span data-ttu-id="a0c6d-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="a0c6d-123">-Name</span></span>
<span data-ttu-id="a0c6d-124">列名</span><span class="sxs-lookup"><span data-stu-id="a0c6d-124">Name</span></span>

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

### <span data-ttu-id="a0c6d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0c6d-125">CommonParameters</span></span>
<span data-ttu-id="a0c6d-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a0c6d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0c6d-127">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a0c6d-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0c6d-128">輸入</span><span class="sxs-lookup"><span data-stu-id="a0c6d-128">INPUTS</span></span>

### <span data-ttu-id="a0c6d-129">所有</span><span class="sxs-lookup"><span data-stu-id="a0c6d-129">None</span></span>

## <span data-ttu-id="a0c6d-130">輸出</span><span class="sxs-lookup"><span data-stu-id="a0c6d-130">OUTPUTS</span></span>

### <span data-ttu-id="a0c6d-131">PSVpnSiteLink 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a0c6d-131">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="a0c6d-132">筆記</span><span class="sxs-lookup"><span data-stu-id="a0c6d-132">NOTES</span></span>

## <span data-ttu-id="a0c6d-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0c6d-133">RELATED LINKS</span></span>

[<span data-ttu-id="a0c6d-134">新-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="a0c6d-134">New-AzVpnSite</span></span>](./New-AzVpnSite.md)