---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: 101440e65fbc0bb21311757a8792a2d45f855364
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612496"
---
# <span data-ttu-id="7f2b0-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="7f2b0-101">New-AzDnsZone</span></span>

## <span data-ttu-id="7f2b0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7f2b0-102">SYNOPSIS</span></span>
<span data-ttu-id="7f2b0-103">建立新的 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="7f2b0-104">句法</span><span class="sxs-lookup"><span data-stu-id="7f2b0-104">SYNTAX</span></span>

### <span data-ttu-id="7f2b0-105">識別碼 (預設) </span><span class="sxs-lookup"><span data-stu-id="7f2b0-105">Ids (Default)</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneId <String>]
 [-Tag <Hashtable>] [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f2b0-106">名稱</span><span class="sxs-lookup"><span data-stu-id="7f2b0-106">Names</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneName <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f2b0-107">物件</span><span class="sxs-lookup"><span data-stu-id="7f2b0-107">Objects</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZone <DnsZone>]
 [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f2b0-108">說明</span><span class="sxs-lookup"><span data-stu-id="7f2b0-108">DESCRIPTION</span></span>
<span data-ttu-id="7f2b0-109">**新的-AzDnsZone** Cmdlet 會在指定的資源群組 (DNS) 區域中建立新的網域名稱系統。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-109">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="7f2b0-110">您必須為 *name* 參數指定唯一的 DNS 區功能變數名稱稱，否則 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-110">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="7f2b0-111">建立區域之後，請使用 New-AzDnsRecordSet Cmdlet 來建立區域中的記錄集。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-111">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="7f2b0-112">您可以使用 *Confirm* 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="7f2b0-113">示例</span><span class="sxs-lookup"><span data-stu-id="7f2b0-113">EXAMPLES</span></span>

### <span data-ttu-id="7f2b0-114">範例1：建立 DNS 區域</span><span class="sxs-lookup"><span data-stu-id="7f2b0-114">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="7f2b0-115">這個命令會在指定的資源群組中建立名為 myzone.com 的新 DNS 區域，然後將它儲存在 $Zone 變數中。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-115">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="7f2b0-116">範例2：透過指定虛擬網路識別碼來建立私人 DNS 區域</span><span class="sxs-lookup"><span data-stu-id="7f2b0-116">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="7f2b0-117">這個命令會在指定的資源群組中，建立一個名為 myprivatezone.com 的新私人 DNS 區域， (指定其識別碼) ，然後將其儲存在 $Zone 變數中。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-117">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="7f2b0-118">範例3：透過指定虛擬網路物件來建立私人 DNS 區域</span><span class="sxs-lookup"><span data-stu-id="7f2b0-118">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="7f2b0-119">這個命令會在指定的資源 (群組中，建立一個名為 myprivatezone.com 的新私人 DNS 區域，並 $ResVirtualNetwork 變數) ，然後將它儲存在 $Zone 變數中。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-119">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="7f2b0-120">範例4：透過指定父區功能變數名稱稱來建立含委派的 DNS 區域</span><span class="sxs-lookup"><span data-stu-id="7f2b0-120">Example 4: Create a DNS zone with delegation by specifying parent zone name</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneName "zone.com"
```

<span data-ttu-id="7f2b0-121">這個命令會在指定的資源群組中建立名為 mychild.zone.com 的新的子 DNS 區域，並將其儲存在 $Zone 變數中。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-121">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="7f2b0-122">它也會在名為 zone.com 的父 DNS 區域中新增委派，且該區域位於與子領域相同的訂閱和資源群組中。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-122">It also adds delegation in the parent DNS zone named zone.com residing in the same subscription and resource group as child zone.</span></span>

### <span data-ttu-id="7f2b0-123">範例5：透過指定父區域識別碼來建立含委派的 DNS 區域</span><span class="sxs-lookup"><span data-stu-id="7f2b0-123">Example 5: Create a DNS zone with delegation by specifying parent zone id</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneId "/subscriptions/**67e2/resourceGroups/other-rg/providers/Microsoft.Network/dnszones/zone.com"
```

<span data-ttu-id="7f2b0-124">這個命令會在指定的資源群組中建立名為 mychild.zone.com 的新的子 DNS 區域，並將其儲存在 $Zone 變數中。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-124">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="7f2b0-125">它也會在資源群組中名為 zone.com 的父 DNS 區域中新增委派，而另一個 rg 提供的訂閱與建立的子領域相同。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-125">It also adds delegation in the parent DNS zone named zone.com in resource group other-rg provided subscription is same as that of child zone created.</span></span>

### <span data-ttu-id="7f2b0-126">範例6：透過指定父區域物件來建立含委派的 DNS 區域</span><span class="sxs-lookup"><span data-stu-id="7f2b0-126">Example 6: Create a DNS zone with delegation by specifying parent zone object</span></span>
```
PS C:\>$PZone = New-AzDnsZone -Name "zone.com" -ResourceGroupName "MyResourceGroup" 
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZone @($PZone)
```

<span data-ttu-id="7f2b0-127">這個命令會在指定的資源群組中建立名為 mychild.zone.com 的新的子 DNS 區域，並將其儲存在 $Zone 變數中。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-127">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="7f2b0-128">它也會在名為 zone.com 的父 DNS 區域中新增委派，就像在 ParentZone 物件中傳遞一樣</span><span class="sxs-lookup"><span data-stu-id="7f2b0-128">It also adds delegation in the parent DNS zone named zone.com as passed in the ParentZone object</span></span>

## <span data-ttu-id="7f2b0-129">參數</span><span class="sxs-lookup"><span data-stu-id="7f2b0-129">PARAMETERS</span></span>

### <span data-ttu-id="7f2b0-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f2b0-130">-DefaultProfile</span></span>
<span data-ttu-id="7f2b0-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="7f2b0-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f2b0-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="7f2b0-132">-Name</span></span>
<span data-ttu-id="7f2b0-133">指定要建立之 DNS 區域的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-133">Specifies the name of the DNS zone to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f2b0-134">-ParentZone</span><span class="sxs-lookup"><span data-stu-id="7f2b0-134">-ParentZone</span></span>
<span data-ttu-id="7f2b0-135">父區域的完整名稱，以新增委派 (，但不需終止點) 。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-135">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f2b0-136">-ParentZoneId</span><span class="sxs-lookup"><span data-stu-id="7f2b0-136">-ParentZoneId</span></span>
<span data-ttu-id="7f2b0-137">要新增 (委派的父區域的資源識別碼，不需終止點) 。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-137">The resource id of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f2b0-138">-ParentZoneName</span><span class="sxs-lookup"><span data-stu-id="7f2b0-138">-ParentZoneName</span></span>
<span data-ttu-id="7f2b0-139">父區域的完整名稱，以新增委派 (，但不需終止點) 。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-139">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Names
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f2b0-140">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7f2b0-140">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="7f2b0-141">將在這個 DNS 區域中註冊虛擬機器主機名稱記錄的虛擬網路清單，只適用于私人區域。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-141">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f2b0-142">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="7f2b0-142">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="7f2b0-143">將在這個 DNS 區域中登錄虛擬機器主機名稱記錄的虛擬網路 Id 清單，只適用于私人區域。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-143">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f2b0-144">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7f2b0-144">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="7f2b0-145">可解析此 DNS 區域中之記錄的虛擬網路清單，只能供私人區域使用。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-145">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f2b0-146">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="7f2b0-146">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="7f2b0-147">可解析此 DNS 區域中之記錄的虛擬網路 Id 清單，只適用于私人區域。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-147">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f2b0-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f2b0-148">-ResourceGroupName</span></span>
<span data-ttu-id="7f2b0-149">指定要在其中建立區域的資源群組。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-149">Specifies the resource group in which to create the zone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f2b0-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="7f2b0-150">-Tag</span></span>
<span data-ttu-id="7f2b0-151">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7f2b0-152">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="7f2b0-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f2b0-153">-ZoneType</span><span class="sxs-lookup"><span data-stu-id="7f2b0-153">-ZoneType</span></span>
<span data-ttu-id="7f2b0-154">該區域的類型為 [公用] 或 [私人]。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-154">The type of the zone, Public or Private.</span></span> <span data-ttu-id="7f2b0-155">在 DNS 階層中使用的公用 DNS 服務平面上提供不含類型或屬於 Public 類型的區域。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-155">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="7f2b0-156">具有私人類型的區域只會與一組關聯的虛擬網路一起顯示 (這項功能在預覽) 中。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-156">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="7f2b0-157">此屬性無法針對區域進行變更。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-157">This property cannot be changed for a zone.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.ZoneType]
Parameter Sets: (All)
Aliases:
Accepted values: Public, Private

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f2b0-158">-確認</span><span class="sxs-lookup"><span data-stu-id="7f2b0-158">-Confirm</span></span>
<span data-ttu-id="7f2b0-159">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f2b0-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f2b0-160">-WhatIf</span></span>
<span data-ttu-id="7f2b0-161">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f2b0-162">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-162">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f2b0-163">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f2b0-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f2b0-164">CommonParameters</span></span>
<span data-ttu-id="7f2b0-165">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f2b0-166">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f2b0-167">輸入</span><span class="sxs-lookup"><span data-stu-id="7f2b0-167">INPUTS</span></span>

### <span data-ttu-id="7f2b0-168">System.object</span><span class="sxs-lookup"><span data-stu-id="7f2b0-168">System.String</span></span>

### <span data-ttu-id="7f2b0-169">"ZoneType" 1 [[3.0.0.0 版]。 Dns，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]] （"）]</span><span class="sxs-lookup"><span data-stu-id="7f2b0-169">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="7f2b0-170">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7f2b0-170">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7f2b0-171">[System.object]。清單 ' 1 [CoreLib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7f2b0-171">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7f2b0-172">[System.object]. 清單 ' 1 [IResourceReference] （31bf3856ad364e35）。網路，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = "]] （區域性 = 中立）</span><span class="sxs-lookup"><span data-stu-id="7f2b0-172">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="7f2b0-173">輸出</span><span class="sxs-lookup"><span data-stu-id="7f2b0-173">OUTPUTS</span></span>

### <span data-ttu-id="7f2b0-174">DnsZone （）</span><span class="sxs-lookup"><span data-stu-id="7f2b0-174">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="7f2b0-175">筆記</span><span class="sxs-lookup"><span data-stu-id="7f2b0-175">NOTES</span></span>
<span data-ttu-id="7f2b0-176">您可以使用 *Confirm* 參數來控制此 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-176">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="7f2b0-177">根據預設，如果 $ConfirmPreference 的 Windows PowerShell 變數的值為 [中] 或 [低]，則該 Cmdlet 會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-177">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="7f2b0-178">如果您指定 [ *確認* ] 或 [ *確認]： $True* ，此 Cmdlet 會在您執行之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-178">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="7f2b0-179">如果您指定 [ *確認： $False* ]，則 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7f2b0-179">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="7f2b0-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="7f2b0-180">RELATED LINKS</span></span>

[<span data-ttu-id="7f2b0-181">AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="7f2b0-181">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="7f2b0-182">新-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="7f2b0-182">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="7f2b0-183">移除-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="7f2b0-183">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)
