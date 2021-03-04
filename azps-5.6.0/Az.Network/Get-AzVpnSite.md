---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
ms.openlocfilehash: 444addf1b7f036ffc4fcaae4a1070b9238c29dc0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905342"
---
# <span data-ttu-id="226fd-101">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="226fd-101">Get-AzVpnSite</span></span>

## <span data-ttu-id="226fd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="226fd-102">SYNOPSIS</span></span>
<span data-ttu-id="226fd-103">根據名稱獲得 Azure VpnSite 資源，或列出 ResourceGroup 或 SubscriptionId 中所有的 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="226fd-103">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

<span data-ttu-id="226fd-104">這是已上傳至 Azure 以使用 Cortex 虛擬中樞進行 S2S 連接的客戶分支 RM 表示。</span><span class="sxs-lookup"><span data-stu-id="226fd-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="226fd-105">語法</span><span class="sxs-lookup"><span data-stu-id="226fd-105">SYNTAX</span></span>

### <span data-ttu-id="226fd-106">ListBySubscriptionId (預設) </span><span class="sxs-lookup"><span data-stu-id="226fd-106">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnSite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="226fd-107">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="226fd-107">ListByResourceGroupName</span></span>
```
Get-AzVpnSite [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="226fd-108">描述</span><span class="sxs-lookup"><span data-stu-id="226fd-108">DESCRIPTION</span></span>
<span data-ttu-id="226fd-109">根據名稱獲得 Azure VpnSite 資源，或列出 ResourceGroup 或 SubscriptionId 中所有的 VpnSite。</span><span class="sxs-lookup"><span data-stu-id="226fd-109">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

## <span data-ttu-id="226fd-110">例子</span><span class="sxs-lookup"><span data-stu-id="226fd-110">EXAMPLES</span></span>

### <span data-ttu-id="226fd-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="226fd-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="226fd-112">上述步驟將在 Azure 的「testRG」資源群組中，建立資源群組「美國西部虛擬 WAN」。</span><span class="sxs-lookup"><span data-stu-id="226fd-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="226fd-113">接著，它會建立一個 VpnSite 來代表客戶分支，並連結至虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="226fd-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="226fd-114">網站建立後，會使用 Get-AzVpnSite 命令。</span><span class="sxs-lookup"><span data-stu-id="226fd-114">Once the site is created, it gets the site using the Get-AzVpnSite command.</span></span>

### <span data-ttu-id="226fd-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="226fd-115">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnSite -Name test*

ResourceGroupName : testRG
Name              : testVpnSite1
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite1
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded

ResourceGroupName : testRG
Name              : testVpnSite2
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite2
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="226fd-116">此 Cmdlet 會從「測試」開始獲得所有網站。</span><span class="sxs-lookup"><span data-stu-id="226fd-116">This cmdlet gets all Sites that start with "test".</span></span>

## <span data-ttu-id="226fd-117">參數</span><span class="sxs-lookup"><span data-stu-id="226fd-117">PARAMETERS</span></span>

### <span data-ttu-id="226fd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="226fd-118">-DefaultProfile</span></span>
<span data-ttu-id="226fd-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="226fd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="226fd-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="226fd-120">-Name</span></span>
<span data-ttu-id="226fd-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="226fd-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnSiteName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="226fd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="226fd-122">-ResourceGroupName</span></span>
<span data-ttu-id="226fd-123">資源組名。</span><span class="sxs-lookup"><span data-stu-id="226fd-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="226fd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="226fd-124">CommonParameters</span></span>
<span data-ttu-id="226fd-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="226fd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="226fd-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="226fd-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="226fd-127">輸入</span><span class="sxs-lookup"><span data-stu-id="226fd-127">INPUTS</span></span>

### <span data-ttu-id="226fd-128">沒有</span><span class="sxs-lookup"><span data-stu-id="226fd-128">None</span></span>

## <span data-ttu-id="226fd-129">輸出</span><span class="sxs-lookup"><span data-stu-id="226fd-129">OUTPUTS</span></span>

### <span data-ttu-id="226fd-130">Microsoft.Azure.Commands.Network.models.PS VpnSite</span><span class="sxs-lookup"><span data-stu-id="226fd-130">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="226fd-131">筆記</span><span class="sxs-lookup"><span data-stu-id="226fd-131">NOTES</span></span>

## <span data-ttu-id="226fd-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="226fd-132">RELATED LINKS</span></span>

[<span data-ttu-id="226fd-133">New-Az VpnSite</span><span class="sxs-lookup"><span data-stu-id="226fd-133">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="226fd-134">Remove-Az VpnSite</span><span class="sxs-lookup"><span data-stu-id="226fd-134">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="226fd-135">Update-Az VpnSite</span><span class="sxs-lookup"><span data-stu-id="226fd-135">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
