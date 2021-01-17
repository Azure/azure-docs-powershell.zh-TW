---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
ms.openlocfilehash: 9b9ab59496ff52be2dc8ca538ea044ec34c34970
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98450158"
---
# <span data-ttu-id="f99f1-101">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="f99f1-101">Remove-AzVpnSite</span></span>

## <span data-ttu-id="f99f1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f99f1-102">SYNOPSIS</span></span>
<span data-ttu-id="f99f1-103">移除 Azure VpnSite 資源。</span><span class="sxs-lookup"><span data-stu-id="f99f1-103">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="f99f1-104">句法</span><span class="sxs-lookup"><span data-stu-id="f99f1-104">SYNTAX</span></span>

### <span data-ttu-id="f99f1-105">ByVpnSiteName (預設) </span><span class="sxs-lookup"><span data-stu-id="f99f1-105">ByVpnSiteName (Default)</span></span>
```
Remove-AzVpnSite -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f99f1-106">ByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="f99f1-106">ByVpnSiteObject</span></span>
```
Remove-AzVpnSite -InputObject <PSVpnSite> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f99f1-107">ByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="f99f1-107">ByVpnSiteResourceId</span></span>
```
Remove-AzVpnSite -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f99f1-108">說明</span><span class="sxs-lookup"><span data-stu-id="f99f1-108">DESCRIPTION</span></span>
<span data-ttu-id="f99f1-109">移除 Azure VpnSite 資源。</span><span class="sxs-lookup"><span data-stu-id="f99f1-109">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="f99f1-110">示例</span><span class="sxs-lookup"><span data-stu-id="f99f1-110">EXAMPLES</span></span>

### <span data-ttu-id="f99f1-111">範例1</span><span class="sxs-lookup"><span data-stu-id="f99f1-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Remove-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"
```

<span data-ttu-id="f99f1-112">上述將會在 Azure 中的 [testRG] 資源群組中，建立一個資源群組、[西部] 的虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="f99f1-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="f99f1-113">接著，它會建立代表客戶分支的 VpnSite，並將它連結至虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="f99f1-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="f99f1-114">網站建立之後，就會立即使用 [Remove-AzVpnSite] 命令移除。</span><span class="sxs-lookup"><span data-stu-id="f99f1-114">Once the site is created, it is immediately removed using the Remove-AzVpnSite command.</span></span>

### <span data-ttu-id="f99f1-115">範例2</span><span class="sxs-lookup"><span data-stu-id="f99f1-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" | Remove-AzVpnSite
```

<span data-ttu-id="f99f1-116">與範例1相同，但在這裡，會使用從 AzVpnSite 的管道輸出進行移除。</span><span class="sxs-lookup"><span data-stu-id="f99f1-116">Same as example 1 but here the removal happens using the piped output from Get-AzVpnSite.</span></span>

## <span data-ttu-id="f99f1-117">參數</span><span class="sxs-lookup"><span data-stu-id="f99f1-117">PARAMETERS</span></span>

### <span data-ttu-id="f99f1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f99f1-118">-DefaultProfile</span></span>
<span data-ttu-id="f99f1-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f99f1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f99f1-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f99f1-120">-Force</span></span>
<span data-ttu-id="f99f1-121">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="f99f1-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f99f1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f99f1-122">-InputObject</span></span>
<span data-ttu-id="f99f1-123">要刪除的 vpnSite 物件。</span><span class="sxs-lookup"><span data-stu-id="f99f1-123">The vpnSite object to be deleted.</span></span>

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

### <span data-ttu-id="f99f1-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="f99f1-124">-Name</span></span>
<span data-ttu-id="f99f1-125">VpnSite 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f99f1-125">The vpnSite name.</span></span>

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

### <span data-ttu-id="f99f1-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f99f1-126">-PassThru</span></span>
<span data-ttu-id="f99f1-127">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="f99f1-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="f99f1-128">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="f99f1-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f99f1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f99f1-129">-ResourceGroupName</span></span>
<span data-ttu-id="f99f1-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f99f1-130">The resource group name.</span></span>

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

### <span data-ttu-id="f99f1-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f99f1-131">-ResourceId</span></span>
<span data-ttu-id="f99f1-132">要刪除之 vpnSite 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f99f1-132">The Azure resource ID for the vpnSite to be deleted.</span></span>

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

### <span data-ttu-id="f99f1-133">-確認</span><span class="sxs-lookup"><span data-stu-id="f99f1-133">-Confirm</span></span>
<span data-ttu-id="f99f1-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f99f1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f99f1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f99f1-135">-WhatIf</span></span>
<span data-ttu-id="f99f1-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f99f1-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f99f1-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f99f1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f99f1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f99f1-138">CommonParameters</span></span>
<span data-ttu-id="f99f1-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f99f1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f99f1-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f99f1-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f99f1-141">輸入</span><span class="sxs-lookup"><span data-stu-id="f99f1-141">INPUTS</span></span>

### <span data-ttu-id="f99f1-142">PSVpnSite 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f99f1-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="f99f1-143">System.object</span><span class="sxs-lookup"><span data-stu-id="f99f1-143">System.String</span></span>

## <span data-ttu-id="f99f1-144">輸出</span><span class="sxs-lookup"><span data-stu-id="f99f1-144">OUTPUTS</span></span>

### <span data-ttu-id="f99f1-145">System.object</span><span class="sxs-lookup"><span data-stu-id="f99f1-145">System.Boolean</span></span>

## <span data-ttu-id="f99f1-146">筆記</span><span class="sxs-lookup"><span data-stu-id="f99f1-146">NOTES</span></span>

## <span data-ttu-id="f99f1-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="f99f1-147">RELATED LINKS</span></span>

[<span data-ttu-id="f99f1-148">AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="f99f1-148">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="f99f1-149">新-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="f99f1-149">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="f99f1-150">更新-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="f99f1-150">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
