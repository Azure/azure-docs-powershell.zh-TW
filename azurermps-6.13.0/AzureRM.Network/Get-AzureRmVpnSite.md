---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnSite.md
ms.openlocfilehash: 0277e61a6b1b180691908b2e86c0050eb8d62b1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448357"
---
# <span data-ttu-id="34b39-101">Get-AzureRmVpnSite</span><span class="sxs-lookup"><span data-stu-id="34b39-101">Get-AzureRmVpnSite</span></span>

## <span data-ttu-id="34b39-102">摘要</span><span class="sxs-lookup"><span data-stu-id="34b39-102">SYNOPSIS</span></span>
<span data-ttu-id="34b39-103">依名稱取得 Azure VpnSite 資源，或列出 ResourceGroup 或 SubscriptionId 中的所有 VpnSites。</span><span class="sxs-lookup"><span data-stu-id="34b39-103">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

<span data-ttu-id="34b39-104">這是使用 Cortex 虛擬中樞上傳至 Azure 以進行 S2S 連線的客戶分支的 RM 表示。</span><span class="sxs-lookup"><span data-stu-id="34b39-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34b39-105">句法</span><span class="sxs-lookup"><span data-stu-id="34b39-105">SYNTAX</span></span>

### <span data-ttu-id="34b39-106">ListBySubscriptionId (預設) </span><span class="sxs-lookup"><span data-stu-id="34b39-106">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVpnSite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34b39-107">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34b39-107">ListByResourceGroupName</span></span>
```
Get-AzureRmVpnSite -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="34b39-108">說明</span><span class="sxs-lookup"><span data-stu-id="34b39-108">DESCRIPTION</span></span>
<span data-ttu-id="34b39-109">依名稱取得 Azure VpnSite 資源，或列出 ResourceGroup 或 SubscriptionId 中的所有 VpnSites。</span><span class="sxs-lookup"><span data-stu-id="34b39-109">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

## <span data-ttu-id="34b39-110">示例</span><span class="sxs-lookup"><span data-stu-id="34b39-110">EXAMPLES</span></span>

### <span data-ttu-id="34b39-111">範例1</span><span class="sxs-lookup"><span data-stu-id="34b39-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"

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

<span data-ttu-id="34b39-112">上述將會在 Azure 中的 [testRG] 資源群組中，建立一個資源群組、[西部] 的虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="34b39-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="34b39-113">接著，它會建立代表客戶分支的 VpnSite，並將它連結至虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="34b39-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="34b39-114">網站建立之後，就會使用 Get-AzureRmVpnSite 命令來取得網站。</span><span class="sxs-lookup"><span data-stu-id="34b39-114">Once the site is created, it gets the site using the Get-AzureRmVpnSite command.</span></span>

## <span data-ttu-id="34b39-115">參數</span><span class="sxs-lookup"><span data-stu-id="34b39-115">PARAMETERS</span></span>

### <span data-ttu-id="34b39-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34b39-116">-DefaultProfile</span></span>
<span data-ttu-id="34b39-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="34b39-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34b39-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="34b39-118">-Name</span></span>
<span data-ttu-id="34b39-119">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="34b39-119">The resource name.</span></span>

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

### <span data-ttu-id="34b39-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34b39-120">-ResourceGroupName</span></span>
<span data-ttu-id="34b39-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="34b39-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34b39-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34b39-122">CommonParameters</span></span>
<span data-ttu-id="34b39-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="34b39-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34b39-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="34b39-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34b39-125">輸入</span><span class="sxs-lookup"><span data-stu-id="34b39-125">INPUTS</span></span>

### <span data-ttu-id="34b39-126">所有</span><span class="sxs-lookup"><span data-stu-id="34b39-126">None</span></span>

## <span data-ttu-id="34b39-127">輸出</span><span class="sxs-lookup"><span data-stu-id="34b39-127">OUTPUTS</span></span>

### <span data-ttu-id="34b39-128">PSVpnSite 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="34b39-128">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="34b39-129">筆記</span><span class="sxs-lookup"><span data-stu-id="34b39-129">NOTES</span></span>

## <span data-ttu-id="34b39-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="34b39-130">RELATED LINKS</span></span>
