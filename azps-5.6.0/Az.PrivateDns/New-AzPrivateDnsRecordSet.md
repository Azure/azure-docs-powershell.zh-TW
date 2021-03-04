---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/new-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 7779cf8b357bab9480a9b811303bb19f1f0a6799
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905321"
---
# <span data-ttu-id="a77d6-101">New-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a77d6-101">New-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="a77d6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a77d6-102">SYNOPSIS</span></span>
<span data-ttu-id="a77d6-103">在私人 DNS 區域中建立記錄集。</span><span class="sxs-lookup"><span data-stu-id="a77d6-103">Creates a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="a77d6-104">語法</span><span class="sxs-lookup"><span data-stu-id="a77d6-104">SYNTAX</span></span>

### <span data-ttu-id="a77d6-105">欄位 (預設) </span><span class="sxs-lookup"><span data-stu-id="a77d6-105">Fields (Default)</span></span>
```
New-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> -Ttl <UInt32> [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a77d6-106">物件</span><span class="sxs-lookup"><span data-stu-id="a77d6-106">Object</span></span>
```
New-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a77d6-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a77d6-107">ResourceId</span></span>
```
New-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a77d6-108">描述</span><span class="sxs-lookup"><span data-stu-id="a77d6-108">DESCRIPTION</span></span>
<span data-ttu-id="a77d6-109">此New-AzPrivateDnsRecordSet Cmdlet 會建立一個新的私人網域名稱系統 (DNS) 記錄集，並輸入指定的私人區域。</span><span class="sxs-lookup"><span data-stu-id="a77d6-109">The New-AzPrivateDnsRecordSet cmdlet creates a new Private Domain Name System (DNS) record set with the specified name and type in the specified private zone.</span></span> <span data-ttu-id="a77d6-110">RecordSet 物件是一組名稱和類型相同的私人 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="a77d6-110">A RecordSet object is a set of Private DNS records with the same name and type.</span></span> <span data-ttu-id="a77d6-111">請注意，名稱是相對於私人區域，而非完整名稱。</span><span class="sxs-lookup"><span data-stu-id="a77d6-111">Note that the name is relative to the private zone and not the fully qualified name.</span></span> <span data-ttu-id="a77d6-112">PrivateDnsRecord 參數會指定記錄集的記錄。</span><span class="sxs-lookup"><span data-stu-id="a77d6-112">The PrivateDnsRecord parameter specifies the records in the record set.</span></span> <span data-ttu-id="a77d6-113">此參數採用使用 New-AzPrivateDnsRecordConfig 建構的專用 DNS 記錄陣列。</span><span class="sxs-lookup"><span data-stu-id="a77d6-113">This parameter takes an array of Private DNS records, constructed using New-AzPrivateDnsRecordConfig.</span></span> <span data-ttu-id="a77d6-114">您可以使用管線運算子將 PSPrivateDnsZone 物件傳遞至此 Cmdlet，或將 PSPrivateDnsZone 物件傳遞為 Zone 參數，或者您也可以使用其 ResourceId 指定區域，或者您也可以按名稱指定區域。</span><span class="sxs-lookup"><span data-stu-id="a77d6-114">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or you can specify the zone by its ResourceId, or alternatively you can specify the zone by name.</span></span> <span data-ttu-id="a77d6-115">您可以使用確認參數$ConfirmPreference Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a77d6-115">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="a77d6-116">如果符合的 RecordSet 已存在 (相同名稱和記錄類型) ，您必須指定覆寫參數，否則 Cmdlet 不會建立新 RecordSet。</span><span class="sxs-lookup"><span data-stu-id="a77d6-116">If a matching RecordSet already exists (same name and record type), you must specify the Overwrite parameter, otherwise the cmdlet will not create a new RecordSet .</span></span>

## <span data-ttu-id="a77d6-117">例子</span><span class="sxs-lookup"><span data-stu-id="a77d6-117">EXAMPLES</span></span>

### <span data-ttu-id="a77d6-118">範例 1：建立類型 A 的 RecordSet</span><span class="sxs-lookup"><span data-stu-id="a77d6-118">Example 1: Create a RecordSet of type A</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4)

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :


# To create a record set containing multiple records, use New-AzPrivateDnsRecordConfig to add each record to the $Records array,
# then call New-AzPrivateDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4, 5.6.7.8}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="a77d6-119">此範例在私人區域中建立名為 www 的 RecordSet myzone.com。</span><span class="sxs-lookup"><span data-stu-id="a77d6-119">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="a77d6-120">記錄集的類型為 A，TTL 為 1 小時， (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="a77d6-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="a77d6-121">它包含單一私人 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="a77d6-121">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="a77d6-122">範例 2：建立類型 AAAA 的 RecordSet</span><span class="sxs-lookup"><span data-stu-id="a77d6-122">Example 2: Create a RecordSet of type AAAA</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:db8::1}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="a77d6-123">此範例在私人區域中建立名為 www 的 RecordSet myzone.com。</span><span class="sxs-lookup"><span data-stu-id="a77d6-123">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="a77d6-124">記錄集的類型為 AAAA，TTL 為 1 小時， (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="a77d6-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="a77d6-125">它包含單一私人 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="a77d6-125">It contains a single Private DNS record.</span></span> <span data-ttu-id="a77d6-126">若要使用一行記錄來建立記錄集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。</span><span class="sxs-lookup"><span data-stu-id="a77d6-126">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a77d6-127">範例 3：建立類型 CNAME 的 RecordSet</span><span class="sxs-lookup"><span data-stu-id="a77d6-127">Example 3: Create a RecordSet of type CNAME</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/CNAME/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : CNAME
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="a77d6-128">此範例在私人區域中建立名為 www 的 RecordSet myzone.com。</span><span class="sxs-lookup"><span data-stu-id="a77d6-128">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="a77d6-129">記錄集的類型為 CNAME，TTL 為 1 小時， (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="a77d6-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="a77d6-130">它包含單一私人 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="a77d6-130">It contains a single Private DNS record.</span></span> <span data-ttu-id="a77d6-131">若要使用一行記錄來建立記錄集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。</span><span class="sxs-lookup"><span data-stu-id="a77d6-131">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a77d6-132">範例 4：建立類型 MX 的 RecordSet</span><span class="sxs-lookup"><span data-stu-id="a77d6-132">Example 4: Create a RecordSet of type MX</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/MX/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : MX
Records           : {[5,mail.microsoft.com]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="a77d6-133">此命令在私人區域中建立名為 www 的 RecordSet myzone.com。</span><span class="sxs-lookup"><span data-stu-id="a77d6-133">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="a77d6-134">記錄集的類型為 MX，TTL 為 1 小時， (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="a77d6-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="a77d6-135">它包含單一私人 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="a77d6-135">It contains a single Private DNS record.</span></span> <span data-ttu-id="a77d6-136">若要使用一行記錄來建立記錄集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。</span><span class="sxs-lookup"><span data-stu-id="a77d6-136">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a77d6-137">範例 5：建立類型 PTR 的 RecordSet</span><span class="sxs-lookup"><span data-stu-id="a77d6-137">Example 5: Create a RecordSet of type PTR</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/3.2.1.in-addr.arpa/PTR/4
Name              : 4
ZoneName          : 3.2.1.in-addr.arpa
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : PTR
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="a77d6-138">此命令在私人區域中建立名為 4 的 RecordSet 3.2.1.in-addr.arpa。</span><span class="sxs-lookup"><span data-stu-id="a77d6-138">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="a77d6-139">記錄集的類型為 PTR，且 TTL 為 1 小時， (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="a77d6-139">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="a77d6-140">它包含單一私人 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="a77d6-140">It contains a single Private DNS record.</span></span> <span data-ttu-id="a77d6-141">若要使用一行記錄來建立記錄集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。</span><span class="sxs-lookup"><span data-stu-id="a77d6-141">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a77d6-142">範例 6：建立類型 SRV 的 RecordSet</span><span class="sxs-lookup"><span data-stu-id="a77d6-142">Example 6: Create a RecordSet of type SRV</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SRV/_sip._tcp
Name              : _sip._tcp
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SRV
Records           : {[0,5,8080,sipservice.contoso.com]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="a77d6-143">此命令在私人區域中建立名為 _sip._tcp 的 RecordSet myzone.com。</span><span class="sxs-lookup"><span data-stu-id="a77d6-143">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="a77d6-144">記錄集的類型為 SRV，TTL 為 1 小時， (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="a77d6-144">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="a77d6-145">它包含單一私人 DNS 記錄，指向 IP 位址 2001.2.3.4。</span><span class="sxs-lookup"><span data-stu-id="a77d6-145">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="a77d6-146">服務 (sip) 和 (tcp) 會指定為記錄集名稱的一部分，而不是記錄資料的一部分。</span><span class="sxs-lookup"><span data-stu-id="a77d6-146">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="a77d6-147">若要使用一行記錄來建立記錄集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。</span><span class="sxs-lookup"><span data-stu-id="a77d6-147">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a77d6-148">範例 7：建立類型 TXT 的 RecordSet</span><span class="sxs-lookup"><span data-stu-id="a77d6-148">Example 7: Create a RecordSet of type TXT</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/TXT/text
Name              : text
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : TXT
Records           : {This is a TXT Record}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="a77d6-149">此命令在私人區域中建立名為文字的 RecordSet myzone.com。</span><span class="sxs-lookup"><span data-stu-id="a77d6-149">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="a77d6-150">記錄集的類型為 TXT，TTL 為 1 小時， (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="a77d6-150">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="a77d6-151">它包含單一私人 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="a77d6-151">It contains a single Private DNS record.</span></span> <span data-ttu-id="a77d6-152">若要使用一行記錄來建立記錄集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。</span><span class="sxs-lookup"><span data-stu-id="a77d6-152">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a77d6-153">範例 8：在區域頂點建立 RecordSet</span><span class="sxs-lookup"><span data-stu-id="a77d6-153">Example 8:  Create a RecordSet at the zone apex</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : @
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="a77d6-154">此命令在私人區域 (或根) 建立 RecordSet myzone.com。</span><span class="sxs-lookup"><span data-stu-id="a77d6-154">This command creates a RecordSet at the apex (or root) of the private zone myzone.com.</span></span> <span data-ttu-id="a77d6-155">若要這麼做，記錄集名稱會指定為 "@" (包括雙引號) 。</span><span class="sxs-lookup"><span data-stu-id="a77d6-155">To do this, the record set name is specified as "@" (including the double-quotes).</span></span> <span data-ttu-id="a77d6-156">您無法在一個區域的頂點建立 CNAME 記錄。</span><span class="sxs-lookup"><span data-stu-id="a77d6-156">You cannot create CNAME records at the apex of a zone.</span></span> <span data-ttu-id="a77d6-157">這是 DNS 標準的限制;這不是 Azure 專用 DNS 的限制。</span><span class="sxs-lookup"><span data-stu-id="a77d6-157">This is a constraint of the DNS standards; it is not a limitation of Azure Private DNS.</span></span> <span data-ttu-id="a77d6-158">若要使用一行記錄來建立記錄集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。</span><span class="sxs-lookup"><span data-stu-id="a77d6-158">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a77d6-159">範例 9：建立萬用字元記錄集</span><span class="sxs-lookup"><span data-stu-id="a77d6-159">Example 9:  Create a wildcard Record Set</span></span>

```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : *
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="a77d6-160">此命令在私人區域中建立名為 \* 的 RecordSet myzone.com。</span><span class="sxs-lookup"><span data-stu-id="a77d6-160">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="a77d6-161">這是萬用字元記錄集。</span><span class="sxs-lookup"><span data-stu-id="a77d6-161">This is a wildcard record set.</span></span> <span data-ttu-id="a77d6-162">若要使用一行記錄來建立記錄集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。</span><span class="sxs-lookup"><span data-stu-id="a77d6-162">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a77d6-163">範例 10：建立空白記錄集</span><span class="sxs-lookup"><span data-stu-id="a77d6-163">Example 10:  Create an empty Record Set</span></span>

```powershell
PS C:\>$RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords @()

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : *
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="a77d6-164">此命令在私人區域中建立名為 \* 的 RecordSet myzone.com。</span><span class="sxs-lookup"><span data-stu-id="a77d6-164">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="a77d6-165">記錄集的類型為 A，TTL 為 1 小時， (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="a77d6-165">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="a77d6-166">這是空白的記錄集，可做為預留位置，日後您可以新增記錄。</span><span class="sxs-lookup"><span data-stu-id="a77d6-166">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="a77d6-167">範例 11：建立記錄集並隱藏所有確認</span><span class="sxs-lookup"><span data-stu-id="a77d6-167">Example 11:  Create a record set and suppress all confirmation</span></span>

```powershell
PS C:\>$RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="a77d6-168">此命令會建立 RecordSet。</span><span class="sxs-lookup"><span data-stu-id="a77d6-168">This command creates a RecordSet.</span></span> <span data-ttu-id="a77d6-169">覆寫參數可確保此記錄集覆寫任何名稱相同且類型相同的現有記錄集 (該記錄集的現有記錄會遺失) 。</span><span class="sxs-lookup"><span data-stu-id="a77d6-169">The Overwrite parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span> <span data-ttu-id="a77d6-170">包含值 $False的確認參數會隱藏確認提示。</span><span class="sxs-lookup"><span data-stu-id="a77d6-170">The Confirm parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="a77d6-171">參數</span><span class="sxs-lookup"><span data-stu-id="a77d6-171">PARAMETERS</span></span>

### <span data-ttu-id="a77d6-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a77d6-172">-DefaultProfile</span></span>
<span data-ttu-id="a77d6-173">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a77d6-173">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a77d6-174">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="a77d6-174">-Metadata</span></span>
<span data-ttu-id="a77d6-175">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a77d6-175">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a77d6-176">-名稱</span><span class="sxs-lookup"><span data-stu-id="a77d6-176">-Name</span></span>
<span data-ttu-id="a77d6-177">此記錄集的記錄名稱會 (區功能變數名稱稱相關，且不含終止點) 。</span><span class="sxs-lookup"><span data-stu-id="a77d6-177">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

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

### <span data-ttu-id="a77d6-178">-覆寫</span><span class="sxs-lookup"><span data-stu-id="a77d6-178">-Overwrite</span></span>
<span data-ttu-id="a77d6-179">如果記錄集已存在，請勿失敗。</span><span class="sxs-lookup"><span data-stu-id="a77d6-179">Do not fail if the record set already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a77d6-180">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a77d6-180">-ParentResourceId</span></span>
<span data-ttu-id="a77d6-181">私人 DNS 區域資源ID。</span><span class="sxs-lookup"><span data-stu-id="a77d6-181">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a77d6-182">-PrivateDnsRecord</span><span class="sxs-lookup"><span data-stu-id="a77d6-182">-PrivateDnsRecord</span></span>
<span data-ttu-id="a77d6-183">屬於此記錄集的私人 dns 記錄。</span><span class="sxs-lookup"><span data-stu-id="a77d6-183">The private dns records that are part of this record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordBase[]
Parameter Sets: (All)
Aliases: PrivateDnsRecords

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a77d6-184">-RecordType</span><span class="sxs-lookup"><span data-stu-id="a77d6-184">-RecordType</span></span>
<span data-ttu-id="a77d6-185">此記錄集的私人 DNS 記錄類型。</span><span class="sxs-lookup"><span data-stu-id="a77d6-185">The type of Private DNS records in this record set.</span></span>

```yaml
Type: Microsoft.Azure.Management.PrivateDns.Models.RecordType
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a77d6-186">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a77d6-186">-ResourceGroupName</span></span>
<span data-ttu-id="a77d6-187">區域所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="a77d6-187">The resource group to which the zone belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a77d6-188">-Ttl</span><span class="sxs-lookup"><span data-stu-id="a77d6-188">-Ttl</span></span>
<span data-ttu-id="a77d6-189">此記錄集內所有記錄的 TTL 值。</span><span class="sxs-lookup"><span data-stu-id="a77d6-189">The TTL value of all the records in this record set.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a77d6-190">-區域</span><span class="sxs-lookup"><span data-stu-id="a77d6-190">-Zone</span></span>
<span data-ttu-id="a77d6-191">PrivateDnsZone 物件代表要建立記錄集的區域。</span><span class="sxs-lookup"><span data-stu-id="a77d6-191">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a77d6-192">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="a77d6-192">-ZoneName</span></span>
<span data-ttu-id="a77d6-193">建立記錄集的區域 (終止點) 。</span><span class="sxs-lookup"><span data-stu-id="a77d6-193">The zone in which to create the record set (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a77d6-194">-確認</span><span class="sxs-lookup"><span data-stu-id="a77d6-194">-Confirm</span></span>
<span data-ttu-id="a77d6-195">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a77d6-195">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a77d6-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a77d6-196">-WhatIf</span></span>
<span data-ttu-id="a77d6-197">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a77d6-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a77d6-198">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a77d6-198">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a77d6-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a77d6-199">CommonParameters</span></span>
<span data-ttu-id="a77d6-200">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a77d6-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a77d6-201">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a77d6-201">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a77d6-202">輸入</span><span class="sxs-lookup"><span data-stu-id="a77d6-202">INPUTS</span></span>

### <span data-ttu-id="a77d6-203">Microsoft.Azure.Commands.PrivateDns.models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="a77d6-203">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="a77d6-204">System.String</span><span class="sxs-lookup"><span data-stu-id="a77d6-204">System.String</span></span>

## <span data-ttu-id="a77d6-205">輸出</span><span class="sxs-lookup"><span data-stu-id="a77d6-205">OUTPUTS</span></span>

### <span data-ttu-id="a77d6-206">Microsoft.Azure.Commands.PrivateDns.models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a77d6-206">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="a77d6-207">筆記</span><span class="sxs-lookup"><span data-stu-id="a77d6-207">NOTES</span></span>

## <span data-ttu-id="a77d6-208">相關連結</span><span class="sxs-lookup"><span data-stu-id="a77d6-208">RELATED LINKS</span></span>
