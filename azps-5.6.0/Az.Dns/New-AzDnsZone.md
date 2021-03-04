---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: 40f1b40bbb5546e1d38b9c2916ea635aab80c144
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910134"
---
# <span data-ttu-id="6f9c9-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="6f9c9-101">New-AzDnsZone</span></span>

## <span data-ttu-id="6f9c9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6f9c9-102">SYNOPSIS</span></span>
<span data-ttu-id="6f9c9-103">建立新 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="6f9c9-104">語法</span><span class="sxs-lookup"><span data-stu-id="6f9c9-104">SYNTAX</span></span>

### <span data-ttu-id="6f9c9-105">識別碼 (預設) </span><span class="sxs-lookup"><span data-stu-id="6f9c9-105">Ids (Default)</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneId <String>]
 [-Tag <Hashtable>] [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f9c9-106">名字</span><span class="sxs-lookup"><span data-stu-id="6f9c9-106">Names</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneName <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f9c9-107">物件</span><span class="sxs-lookup"><span data-stu-id="6f9c9-107">Objects</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZone <DnsZone>]
 [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f9c9-108">描述</span><span class="sxs-lookup"><span data-stu-id="6f9c9-108">DESCRIPTION</span></span>
<span data-ttu-id="6f9c9-109">**New-AzDnsZone** Cmdlet 會建立一個新的網域名稱系統 (指定資源群組) DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-109">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="6f9c9-110">您必須為 Name 參數指定唯一的DNS 區功能變數名稱稱，否則 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-110">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="6f9c9-111">建立區域之後，請使用 New-AzDnsRecordSet Cmdlet 在區域中建立記錄集。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-111">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="6f9c9-112">您可以使用確認 *參數$ConfirmPreference* Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="6f9c9-113">例子</span><span class="sxs-lookup"><span data-stu-id="6f9c9-113">EXAMPLES</span></span>

### <span data-ttu-id="6f9c9-114">範例 1：建立 DNS 區域</span><span class="sxs-lookup"><span data-stu-id="6f9c9-114">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="6f9c9-115">此命令會建立一個名為 myzone.com 指定資源群組的新 DNS 區域，然後將它儲存在 $Zone 變數中。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-115">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="6f9c9-116">範例 2：指定虛擬網路識別碼 以建立私人 DNS 區域</span><span class="sxs-lookup"><span data-stu-id="6f9c9-116">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="6f9c9-117">此命令會建立指定資源群組中名為 myprivatezone.com 的新私人 DNS 區域，並且使用相關聯的解析虛擬網路 (指定其識別碼) ，然後將它儲存在 $Zone 變數中。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-117">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="6f9c9-118">範例 3：指定虛擬網路物件以建立私人 DNS 區域</span><span class="sxs-lookup"><span data-stu-id="6f9c9-118">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="6f9c9-119">此命令會建立指定資源群組中名為 myprivatezone.com 的新私人 DNS 區域，其關聯解析虛擬網路 (由 $ResVirtualNetwork 變數) 所參考，然後將它儲存在 $Zone 變數中。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-119">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="6f9c9-120">範例 4：指定父區功能變數名稱稱以建立具有委派的 DNS 區域</span><span class="sxs-lookup"><span data-stu-id="6f9c9-120">Example 4: Create a DNS zone with delegation by specifying parent zone name</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneName "zone.com"
```

<span data-ttu-id="6f9c9-121">此命令會建立名為 mychild.zone.com 指定資源群組的新子 DNS 區域，並儲存在$Zone變數中。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-121">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="6f9c9-122">它也會將委派新增到父 DNS 區域中，zone.com位於與子領域相同的訂閱和資源群組中。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-122">It also adds delegation in the parent DNS zone named zone.com residing in the same subscription and resource group as child zone.</span></span>

### <span data-ttu-id="6f9c9-123">範例 5：指定父區域識別碼以建立具有委派的 DNS 區域</span><span class="sxs-lookup"><span data-stu-id="6f9c9-123">Example 5: Create a DNS zone with delegation by specifying parent zone id</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneId "/subscriptions/**67e2/resourceGroups/other-rg/providers/Microsoft.Network/dnszones/zone.com"
```

<span data-ttu-id="6f9c9-124">此命令會建立名為 mychild.zone.com 指定資源群組的新子 DNS 區域，並儲存在$Zone變數中。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-124">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="6f9c9-125">它也新增了在父 DNS 區域中名為 zone.com 的資源群組中，其他 rg 提供的訂閱與建立之子領域中的委派相同。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-125">It also adds delegation in the parent DNS zone named zone.com in resource group other-rg provided subscription is same as that of child zone created.</span></span>

### <span data-ttu-id="6f9c9-126">範例 6：指定父區域物件以建立具有委派的 DNS 區域</span><span class="sxs-lookup"><span data-stu-id="6f9c9-126">Example 6: Create a DNS zone with delegation by specifying parent zone object</span></span>
```
PS C:\>$PZone = New-AzDnsZone -Name "zone.com" -ResourceGroupName "MyResourceGroup" 
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZone @($PZone)
```

<span data-ttu-id="6f9c9-127">此命令會建立名為 mychild.zone.com 指定資源群組的新子 DNS 區域，並儲存在$Zone變數中。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-127">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="6f9c9-128">它也在父 DNS 區域中新增委派，zone.com在 ParentZone 物件中傳遞</span><span class="sxs-lookup"><span data-stu-id="6f9c9-128">It also adds delegation in the parent DNS zone named zone.com as passed in the ParentZone object</span></span>

## <span data-ttu-id="6f9c9-129">參數</span><span class="sxs-lookup"><span data-stu-id="6f9c9-129">PARAMETERS</span></span>

### <span data-ttu-id="6f9c9-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f9c9-130">-DefaultProfile</span></span>
<span data-ttu-id="6f9c9-131">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="6f9c9-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f9c9-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="6f9c9-132">-Name</span></span>
<span data-ttu-id="6f9c9-133">指定要建立 DNS 區域的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-133">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="6f9c9-134">-父區域</span><span class="sxs-lookup"><span data-stu-id="6f9c9-134">-ParentZone</span></span>
<span data-ttu-id="6f9c9-135">父區域的完整名稱，以新增委派 (終止點) 。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-135">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

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

### <span data-ttu-id="6f9c9-136">-ParentZoneId</span><span class="sxs-lookup"><span data-stu-id="6f9c9-136">-ParentZoneId</span></span>
<span data-ttu-id="6f9c9-137">父區域的資源識別碼，可新增委派 (終止點) 。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-137">The resource id of the parent zone to add delegation (without a terminating dot).</span></span>

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

### <span data-ttu-id="6f9c9-138">-ParentZoneName</span><span class="sxs-lookup"><span data-stu-id="6f9c9-138">-ParentZoneName</span></span>
<span data-ttu-id="6f9c9-139">父區域的完整名稱，以新增委派 (終止點) 。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-139">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

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

### <span data-ttu-id="6f9c9-140">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6f9c9-140">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="6f9c9-141">在此 DNS 區域中註冊虛擬機器主機名稱記錄的虛擬網路清單，僅適用于私人區域。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-141">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="6f9c9-142">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="6f9c9-142">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="6f9c9-143">在此 DNS 區域中註冊虛擬機器主機名稱記錄的虛擬網路識別碼 清單，僅適用于私人區域。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-143">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="6f9c9-144">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6f9c9-144">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="6f9c9-145">可解析此 DNS 區域中記錄的虛擬網路清單，僅適用于私人區域。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-145">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="6f9c9-146">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="6f9c9-146">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="6f9c9-147">可解析此 DNS 區域中記錄的虛擬網路識別碼 清單，僅適用于私人區域。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-147">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="6f9c9-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f9c9-148">-ResourceGroupName</span></span>
<span data-ttu-id="6f9c9-149">指定要建立區域的資源群組。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-149">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="6f9c9-150">-標記</span><span class="sxs-lookup"><span data-stu-id="6f9c9-150">-Tag</span></span>
<span data-ttu-id="6f9c9-151">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6f9c9-152">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="6f9c9-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6f9c9-153">-ZoneType</span><span class="sxs-lookup"><span data-stu-id="6f9c9-153">-ZoneType</span></span>
<span data-ttu-id="6f9c9-154">區欄位型別，公用或私人。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-154">The type of the zone, Public or Private.</span></span> <span data-ttu-id="6f9c9-155">沒有類型或具有公用類型的區域可在公用 DNS 服務平面上提供，以用於 DNS 階層。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-155">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="6f9c9-156">只有一組相關聯的虛擬網路才能看到具有私人類型的區域， (此功能是在預覽) 。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-156">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="6f9c9-157">無法針對區域變更此屬性。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-157">This property cannot be changed for a zone.</span></span>

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

### <span data-ttu-id="6f9c9-158">-確認</span><span class="sxs-lookup"><span data-stu-id="6f9c9-158">-Confirm</span></span>
<span data-ttu-id="6f9c9-159">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f9c9-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f9c9-160">-WhatIf</span></span>
<span data-ttu-id="6f9c9-161">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f9c9-162">不會執行 Cmdlet。顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-162">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f9c9-163">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f9c9-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f9c9-164">CommonParameters</span></span>
<span data-ttu-id="6f9c9-165">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f9c9-166">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f9c9-167">輸入</span><span class="sxs-lookup"><span data-stu-id="6f9c9-167">INPUTS</span></span>

### <span data-ttu-id="6f9c9-168">System.String</span><span class="sxs-lookup"><span data-stu-id="6f9c9-168">System.String</span></span>

### <span data-ttu-id="6f9c9-169">System.Nullable'1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="6f9c9-169">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="6f9c9-170">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="6f9c9-170">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6f9c9-171">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6f9c9-171">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6f9c9-172">System.Collections.generic.List'1[[Microsoft.Azure.management.Internal.Network.Common.IResourceReference，Microsoft.Azure.PowerShell.Clients.Network， Version=1.0.0.0， Culture=neutral， PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="6f9c9-172">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="6f9c9-173">輸出</span><span class="sxs-lookup"><span data-stu-id="6f9c9-173">OUTPUTS</span></span>

### <span data-ttu-id="6f9c9-174">Microsoft.Azure.Commands.dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="6f9c9-174">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="6f9c9-175">筆記</span><span class="sxs-lookup"><span data-stu-id="6f9c9-175">NOTES</span></span>
<span data-ttu-id="6f9c9-176">您可以使用 *確認參數來控制* 此 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-176">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="6f9c9-177">根據預設，如果 Windows PowerShell 變數的 $ConfirmPreference中或較低值，Cmdlet 會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-177">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="6f9c9-178">如果您 *指定確認或* 確認 *：$True，* 此 Cmdlet 會先提示您確認再執行。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-178">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="6f9c9-179">如果您指定 *確認：$False，Cmdlet* 不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6f9c9-179">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6f9c9-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f9c9-180">RELATED LINKS</span></span>

[<span data-ttu-id="6f9c9-181">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="6f9c9-181">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="6f9c9-182">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6f9c9-182">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="6f9c9-183">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="6f9c9-183">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)
