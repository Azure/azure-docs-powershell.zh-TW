---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnSite.md
ms.openlocfilehash: ac0513b7d411c2c95864aa6f619e80d2373a3554
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449013"
---
# <span data-ttu-id="82dce-101">Remove-AzureRmVpnSite</span><span class="sxs-lookup"><span data-stu-id="82dce-101">Remove-AzureRmVpnSite</span></span>

## <span data-ttu-id="82dce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="82dce-102">SYNOPSIS</span></span>
<span data-ttu-id="82dce-103">移除 Azure VpnSite 資源。</span><span class="sxs-lookup"><span data-stu-id="82dce-103">Removes an Azure VpnSite resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82dce-104">句法</span><span class="sxs-lookup"><span data-stu-id="82dce-104">SYNTAX</span></span>

### <span data-ttu-id="82dce-105">ByVpnSiteName (預設) </span><span class="sxs-lookup"><span data-stu-id="82dce-105">ByVpnSiteName (Default)</span></span>
```
Remove-AzureRmVpnSite -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82dce-106">ByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="82dce-106">ByVpnSiteObject</span></span>
```
Remove-AzureRmVpnSite -InputObject <PSVpnSite> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82dce-107">ByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="82dce-107">ByVpnSiteResourceId</span></span>
```
Remove-AzureRmVpnSite -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82dce-108">說明</span><span class="sxs-lookup"><span data-stu-id="82dce-108">DESCRIPTION</span></span>
<span data-ttu-id="82dce-109">移除 Azure VpnSite 資源。</span><span class="sxs-lookup"><span data-stu-id="82dce-109">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="82dce-110">示例</span><span class="sxs-lookup"><span data-stu-id="82dce-110">EXAMPLES</span></span>

### <span data-ttu-id="82dce-111">範例1</span><span class="sxs-lookup"><span data-stu-id="82dce-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Remove-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"
```

<span data-ttu-id="82dce-112">上述將會在 Azure 中的 [testRG] 資源群組中，建立一個資源群組、[西部] 的虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="82dce-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="82dce-113">接著，它會建立代表客戶分支的 VpnSite，並將它連結至虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="82dce-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="82dce-114">網站建立之後，就會立即使用 [Remove-AzureRmVpnSite] 命令移除。</span><span class="sxs-lookup"><span data-stu-id="82dce-114">Once the site is created, it is immediately removed using the Remove-AzureRmVpnSite command.</span></span>

### <span data-ttu-id="82dce-115">範例2</span><span class="sxs-lookup"><span data-stu-id="82dce-115">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" | Remove-AzureRmVpnSite
```

<span data-ttu-id="82dce-116">與範例1相同，但在這裡，會使用從 AzureRmVpnSite 的管道輸出進行移除。</span><span class="sxs-lookup"><span data-stu-id="82dce-116">Same as example 1 but here the removal happens using the piped output from Get-AzureRmVpnSite.</span></span>

## <span data-ttu-id="82dce-117">參數</span><span class="sxs-lookup"><span data-stu-id="82dce-117">PARAMETERS</span></span>

### <span data-ttu-id="82dce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82dce-118">-DefaultProfile</span></span>
<span data-ttu-id="82dce-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="82dce-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82dce-120">-Force</span><span class="sxs-lookup"><span data-stu-id="82dce-120">-Force</span></span>
<span data-ttu-id="82dce-121">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="82dce-121">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82dce-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82dce-122">-InputObject</span></span>
<span data-ttu-id="82dce-123">要刪除的 vpnSite 物件。</span><span class="sxs-lookup"><span data-stu-id="82dce-123">The vpnSite object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite
Parameter Sets: ByVpnSiteObject
Aliases: VpnSite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82dce-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="82dce-124">-Name</span></span>
<span data-ttu-id="82dce-125">VpnSite 的名稱。</span><span class="sxs-lookup"><span data-stu-id="82dce-125">The vpnSite name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteName
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82dce-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82dce-126">-PassThru</span></span>
<span data-ttu-id="82dce-127">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="82dce-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="82dce-128">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="82dce-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82dce-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82dce-129">-ResourceGroupName</span></span>
<span data-ttu-id="82dce-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="82dce-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82dce-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82dce-131">-ResourceId</span></span>
<span data-ttu-id="82dce-132">要刪除之 vpnSite 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="82dce-132">The Azure resource ID for the vpnSite to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteResourceId
Aliases: VpnSiteId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82dce-133">-確認</span><span class="sxs-lookup"><span data-stu-id="82dce-133">-Confirm</span></span>
<span data-ttu-id="82dce-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="82dce-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82dce-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82dce-135">-WhatIf</span></span>
<span data-ttu-id="82dce-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="82dce-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="82dce-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="82dce-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82dce-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82dce-138">CommonParameters</span></span>
<span data-ttu-id="82dce-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="82dce-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82dce-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="82dce-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82dce-141">輸入</span><span class="sxs-lookup"><span data-stu-id="82dce-141">INPUTS</span></span>

### <span data-ttu-id="82dce-142">PSVpnSite 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="82dce-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="82dce-143">System.object</span><span class="sxs-lookup"><span data-stu-id="82dce-143">System.String</span></span>

## <span data-ttu-id="82dce-144">輸出</span><span class="sxs-lookup"><span data-stu-id="82dce-144">OUTPUTS</span></span>

### <span data-ttu-id="82dce-145">System.object</span><span class="sxs-lookup"><span data-stu-id="82dce-145">System.Boolean</span></span>

## <span data-ttu-id="82dce-146">筆記</span><span class="sxs-lookup"><span data-stu-id="82dce-146">NOTES</span></span>

## <span data-ttu-id="82dce-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="82dce-147">RELATED LINKS</span></span>
