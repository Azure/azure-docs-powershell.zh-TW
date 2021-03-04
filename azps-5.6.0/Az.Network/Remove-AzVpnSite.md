---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
ms.openlocfilehash: 50e335825fb43a85286be5f95696c1dd1a537129
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904590"
---
# <span data-ttu-id="4668e-101">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="4668e-101">Remove-AzVpnSite</span></span>

## <span data-ttu-id="4668e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4668e-102">SYNOPSIS</span></span>
<span data-ttu-id="4668e-103">移除 Azure VpnSite 資源。</span><span class="sxs-lookup"><span data-stu-id="4668e-103">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="4668e-104">語法</span><span class="sxs-lookup"><span data-stu-id="4668e-104">SYNTAX</span></span>

### <span data-ttu-id="4668e-105">By VpnSiteName (預設) </span><span class="sxs-lookup"><span data-stu-id="4668e-105">ByVpnSiteName (Default)</span></span>
```
Remove-AzVpnSite -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4668e-106">By VpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="4668e-106">ByVpnSiteObject</span></span>
```
Remove-AzVpnSite -InputObject <PSVpnSite> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4668e-107">By VpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="4668e-107">ByVpnSiteResourceId</span></span>
```
Remove-AzVpnSite -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4668e-108">描述</span><span class="sxs-lookup"><span data-stu-id="4668e-108">DESCRIPTION</span></span>
<span data-ttu-id="4668e-109">移除 Azure VpnSite 資源。</span><span class="sxs-lookup"><span data-stu-id="4668e-109">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="4668e-110">例子</span><span class="sxs-lookup"><span data-stu-id="4668e-110">EXAMPLES</span></span>

### <span data-ttu-id="4668e-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="4668e-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Remove-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"
```

<span data-ttu-id="4668e-112">上述步驟將在 Azure 的「testRG」資源群組中，建立資源群組「美國西部虛擬 WAN」。</span><span class="sxs-lookup"><span data-stu-id="4668e-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="4668e-113">接著，它會建立一個 VpnSite 來代表客戶分支，並連結至虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="4668e-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="4668e-114">網站建立後，會立即使用 Remove-AzVpnSite 移除。</span><span class="sxs-lookup"><span data-stu-id="4668e-114">Once the site is created, it is immediately removed using the Remove-AzVpnSite command.</span></span>

### <span data-ttu-id="4668e-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="4668e-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" | Remove-AzVpnSite
```

<span data-ttu-id="4668e-116">與範例 1 相同，但移除會使用 Get-Az VpnSite 的管道輸出進行。</span><span class="sxs-lookup"><span data-stu-id="4668e-116">Same as example 1 but here the removal happens using the piped output from Get-AzVpnSite.</span></span>

## <span data-ttu-id="4668e-117">參數</span><span class="sxs-lookup"><span data-stu-id="4668e-117">PARAMETERS</span></span>

### <span data-ttu-id="4668e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4668e-118">-DefaultProfile</span></span>
<span data-ttu-id="4668e-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4668e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4668e-120">-強制</span><span class="sxs-lookup"><span data-stu-id="4668e-120">-Force</span></span>
<span data-ttu-id="4668e-121">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="4668e-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4668e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4668e-122">-InputObject</span></span>
<span data-ttu-id="4668e-123">要刪除的 vpnSite 物件。</span><span class="sxs-lookup"><span data-stu-id="4668e-123">The vpnSite object to be deleted.</span></span>

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

### <span data-ttu-id="4668e-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="4668e-124">-Name</span></span>
<span data-ttu-id="4668e-125">vpnSite 名稱。</span><span class="sxs-lookup"><span data-stu-id="4668e-125">The vpnSite name.</span></span>

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

### <span data-ttu-id="4668e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4668e-126">-PassThru</span></span>
<span data-ttu-id="4668e-127">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="4668e-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="4668e-128">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="4668e-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4668e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4668e-129">-ResourceGroupName</span></span>
<span data-ttu-id="4668e-130">資源組名。</span><span class="sxs-lookup"><span data-stu-id="4668e-130">The resource group name.</span></span>

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

### <span data-ttu-id="4668e-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4668e-131">-ResourceId</span></span>
<span data-ttu-id="4668e-132">要刪除 vpnSite 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4668e-132">The Azure resource ID for the vpnSite to be deleted.</span></span>

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

### <span data-ttu-id="4668e-133">-確認</span><span class="sxs-lookup"><span data-stu-id="4668e-133">-Confirm</span></span>
<span data-ttu-id="4668e-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4668e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4668e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4668e-135">-WhatIf</span></span>
<span data-ttu-id="4668e-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4668e-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4668e-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4668e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4668e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4668e-138">CommonParameters</span></span>
<span data-ttu-id="4668e-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4668e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4668e-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4668e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4668e-141">輸入</span><span class="sxs-lookup"><span data-stu-id="4668e-141">INPUTS</span></span>

### <span data-ttu-id="4668e-142">Microsoft.Azure.Commands.Network.models.PS VpnSite</span><span class="sxs-lookup"><span data-stu-id="4668e-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="4668e-143">System.String</span><span class="sxs-lookup"><span data-stu-id="4668e-143">System.String</span></span>

## <span data-ttu-id="4668e-144">輸出</span><span class="sxs-lookup"><span data-stu-id="4668e-144">OUTPUTS</span></span>

### <span data-ttu-id="4668e-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4668e-145">System.Boolean</span></span>

## <span data-ttu-id="4668e-146">筆記</span><span class="sxs-lookup"><span data-stu-id="4668e-146">NOTES</span></span>

## <span data-ttu-id="4668e-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="4668e-147">RELATED LINKS</span></span>

[<span data-ttu-id="4668e-148">Get-Az VpnSite</span><span class="sxs-lookup"><span data-stu-id="4668e-148">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="4668e-149">New-Az VpnSite</span><span class="sxs-lookup"><span data-stu-id="4668e-149">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="4668e-150">Update-Az VpnSite</span><span class="sxs-lookup"><span data-stu-id="4668e-150">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
