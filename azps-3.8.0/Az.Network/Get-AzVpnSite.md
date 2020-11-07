---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
ms.openlocfilehash: 44a40fb446904c8d1bfa40820ae34e0a4aca2caa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966295"
---
# <span data-ttu-id="56b0c-101">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="56b0c-101">Get-AzVpnSite</span></span>

## <span data-ttu-id="56b0c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="56b0c-102">SYNOPSIS</span></span>
<span data-ttu-id="56b0c-103">依名稱取得 Azure VpnSite 資源，或列出 ResourceGroup 或 SubscriptionId 中的所有 VpnSites。</span><span class="sxs-lookup"><span data-stu-id="56b0c-103">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

<span data-ttu-id="56b0c-104">這是使用 Cortex 虛擬中樞上傳至 Azure 以進行 S2S 連線的客戶分支的 RM 表示。</span><span class="sxs-lookup"><span data-stu-id="56b0c-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="56b0c-105">句法</span><span class="sxs-lookup"><span data-stu-id="56b0c-105">SYNTAX</span></span>

### <span data-ttu-id="56b0c-106">ListBySubscriptionId (預設) </span><span class="sxs-lookup"><span data-stu-id="56b0c-106">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnSite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56b0c-107">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56b0c-107">ListByResourceGroupName</span></span>
```
Get-AzVpnSite [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56b0c-108">說明</span><span class="sxs-lookup"><span data-stu-id="56b0c-108">DESCRIPTION</span></span>
<span data-ttu-id="56b0c-109">依名稱取得 Azure VpnSite 資源，或列出 ResourceGroup 或 SubscriptionId 中的所有 VpnSites。</span><span class="sxs-lookup"><span data-stu-id="56b0c-109">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

## <span data-ttu-id="56b0c-110">示例</span><span class="sxs-lookup"><span data-stu-id="56b0c-110">EXAMPLES</span></span>

### <span data-ttu-id="56b0c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="56b0c-111">Example 1</span></span>

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

<span data-ttu-id="56b0c-112">上述將會在 Azure 中的 [testRG] 資源群組中，建立一個資源群組、[西部] 的虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="56b0c-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="56b0c-113">接著，它會建立代表客戶分支的 VpnSite，並將它連結至虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="56b0c-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="56b0c-114">網站建立之後，就會使用 Get-AzVpnSite 命令來取得網站。</span><span class="sxs-lookup"><span data-stu-id="56b0c-114">Once the site is created, it gets the site using the Get-AzVpnSite command.</span></span>

### <span data-ttu-id="56b0c-115">範例2</span><span class="sxs-lookup"><span data-stu-id="56b0c-115">Example 2</span></span>

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

<span data-ttu-id="56b0c-116">這個 Cmdlet 會取得以「test」開頭的所有網站。</span><span class="sxs-lookup"><span data-stu-id="56b0c-116">This cmdlet gets all Sites that start with "test".</span></span>

## <span data-ttu-id="56b0c-117">參數</span><span class="sxs-lookup"><span data-stu-id="56b0c-117">PARAMETERS</span></span>

### <span data-ttu-id="56b0c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56b0c-118">-DefaultProfile</span></span>
<span data-ttu-id="56b0c-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="56b0c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56b0c-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="56b0c-120">-Name</span></span>
<span data-ttu-id="56b0c-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="56b0c-121">The resource name.</span></span>

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

### <span data-ttu-id="56b0c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56b0c-122">-ResourceGroupName</span></span>
<span data-ttu-id="56b0c-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="56b0c-123">The resource group name.</span></span>

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

### <span data-ttu-id="56b0c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56b0c-124">CommonParameters</span></span>
<span data-ttu-id="56b0c-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="56b0c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56b0c-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="56b0c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56b0c-127">輸入</span><span class="sxs-lookup"><span data-stu-id="56b0c-127">INPUTS</span></span>

### <span data-ttu-id="56b0c-128">所有</span><span class="sxs-lookup"><span data-stu-id="56b0c-128">None</span></span>

## <span data-ttu-id="56b0c-129">輸出</span><span class="sxs-lookup"><span data-stu-id="56b0c-129">OUTPUTS</span></span>

### <span data-ttu-id="56b0c-130">PSVpnSite 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="56b0c-130">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="56b0c-131">筆記</span><span class="sxs-lookup"><span data-stu-id="56b0c-131">NOTES</span></span>

## <span data-ttu-id="56b0c-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="56b0c-132">RELATED LINKS</span></span>

[<span data-ttu-id="56b0c-133">新-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="56b0c-133">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="56b0c-134">移除-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="56b0c-134">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="56b0c-135">更新-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="56b0c-135">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
