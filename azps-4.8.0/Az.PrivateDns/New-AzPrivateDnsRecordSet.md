---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 1a7042c94457f23302aa8d2899475d7b117e65b4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128145"
---
# <span data-ttu-id="29763-101">New-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="29763-101">New-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="29763-102">摘要</span><span class="sxs-lookup"><span data-stu-id="29763-102">SYNOPSIS</span></span>
<span data-ttu-id="29763-103">在 [私人 DNS 區域] 中建立記錄集。</span><span class="sxs-lookup"><span data-stu-id="29763-103">Creates a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="29763-104">句法</span><span class="sxs-lookup"><span data-stu-id="29763-104">SYNTAX</span></span>

### <span data-ttu-id="29763-105">預設)  (的欄位</span><span class="sxs-lookup"><span data-stu-id="29763-105">Fields (Default)</span></span>
```
New-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> -Ttl <UInt32> [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29763-106">面向</span><span class="sxs-lookup"><span data-stu-id="29763-106">Object</span></span>
```
New-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29763-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="29763-107">ResourceId</span></span>
```
New-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29763-108">說明</span><span class="sxs-lookup"><span data-stu-id="29763-108">DESCRIPTION</span></span>
<span data-ttu-id="29763-109">New-AzPrivateDnsRecordSet Cmdlet 會在指定的私人區域中使用指定的名稱和類型，建立新的私人網域名稱系統 (DNS) 記錄集。</span><span class="sxs-lookup"><span data-stu-id="29763-109">The New-AzPrivateDnsRecordSet cmdlet creates a new Private Domain Name System (DNS) record set with the specified name and type in the specified private zone.</span></span> <span data-ttu-id="29763-110">記錄集物件是一組具有相同名稱和類型的專用 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="29763-110">A RecordSet object is a set of Private DNS records with the same name and type.</span></span> <span data-ttu-id="29763-111">請注意，該名稱是相對於私人區域而非完整名稱。</span><span class="sxs-lookup"><span data-stu-id="29763-111">Note that the name is relative to the private zone and not the fully qualified name.</span></span> <span data-ttu-id="29763-112">PrivateDnsRecord 參數會指定記錄集中的記錄。</span><span class="sxs-lookup"><span data-stu-id="29763-112">The PrivateDnsRecord parameter specifies the records in the record set.</span></span> <span data-ttu-id="29763-113">這個參數會採用一個由 AzPrivateDnsRecordConfig 建立的私用 DNS 記錄陣列。</span><span class="sxs-lookup"><span data-stu-id="29763-113">This parameter takes an array of Private DNS records, constructed using New-AzPrivateDnsRecordConfig.</span></span> <span data-ttu-id="29763-114">您可以使用管線運算子，將 PSPrivateDnsZone 物件傳遞到這個 Cmdlet，或者您可以將 PSPrivateDnsZone 物件作為 Zone 參數傳遞，或者也可以依據名稱指定該區域。</span><span class="sxs-lookup"><span data-stu-id="29763-114">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or you can specify the zone by its ResourceId, or alternatively you can specify the zone by name.</span></span> <span data-ttu-id="29763-115">您可以使用 Confirm 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="29763-115">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="29763-116">如果相符的記錄集已存在 (相同的名稱和記錄類型) ，您必須指定 Overwrite 參數，否則 Cmdlet 不會建立新的記錄集。</span><span class="sxs-lookup"><span data-stu-id="29763-116">If a matching RecordSet already exists (same name and record type), you must specify the Overwrite parameter, otherwise the cmdlet will not create a new RecordSet .</span></span>

## <span data-ttu-id="29763-117">示例</span><span class="sxs-lookup"><span data-stu-id="29763-117">EXAMPLES</span></span>

### <span data-ttu-id="29763-118">範例1：建立 A 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="29763-118">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="29763-119">這個範例會在 [私人區域 myzone.com] 中建立名為「www」的記錄集。</span><span class="sxs-lookup"><span data-stu-id="29763-119">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="29763-120">記錄集的類型是 A，且每個小時的 TTL (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="29763-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="29763-121">它包含單一的私人 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="29763-121">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="29763-122">範例2：建立 AAAA 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="29763-122">Example 2: Create a RecordSet of type AAAA</span></span>
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

<span data-ttu-id="29763-123">這個範例會在 [私人區域 myzone.com] 中建立名為「www」的記錄集。</span><span class="sxs-lookup"><span data-stu-id="29763-123">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="29763-124">記錄集的類型是 AAAA，且每個小時的 TTL (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="29763-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="29763-125">它包含單一的私人 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="29763-125">It contains a single Private DNS record.</span></span> <span data-ttu-id="29763-126">若要建立只使用一行 pn_PowerShell_short 的記錄集，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="29763-126">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="29763-127">範例3：建立 CNAME 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="29763-127">Example 3: Create a RecordSet of type CNAME</span></span>
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

<span data-ttu-id="29763-128">這個範例會在 [私人區域 myzone.com] 中建立名為「www」的記錄集。</span><span class="sxs-lookup"><span data-stu-id="29763-128">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="29763-129">此記錄集的類型為 CNAME，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="29763-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="29763-130">它包含單一的私人 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="29763-130">It contains a single Private DNS record.</span></span> <span data-ttu-id="29763-131">若要建立只使用一行 pn_PowerShell_short 的記錄集，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="29763-131">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="29763-132">範例4：建立 MX 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="29763-132">Example 4: Create a RecordSet of type MX</span></span>
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

<span data-ttu-id="29763-133">這個命令會在 [私人區域 myzone.com] 中建立一個名為「www」的記錄集。</span><span class="sxs-lookup"><span data-stu-id="29763-133">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="29763-134">記錄集的類型是 MX，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="29763-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="29763-135">它包含單一的私人 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="29763-135">It contains a single Private DNS record.</span></span> <span data-ttu-id="29763-136">若要建立只使用一行 pn_PowerShell_short 的記錄集，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="29763-136">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="29763-137">範例5：建立類型指標的記錄集</span><span class="sxs-lookup"><span data-stu-id="29763-137">Example 5: Create a RecordSet of type PTR</span></span>
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

<span data-ttu-id="29763-138">這個命令會在私人區域3.2.1.in （arpa）中建立名為4的記錄集。</span><span class="sxs-lookup"><span data-stu-id="29763-138">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="29763-139">記錄集的類型是 PTR，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="29763-139">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="29763-140">它包含單一的私人 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="29763-140">It contains a single Private DNS record.</span></span> <span data-ttu-id="29763-141">若要建立只使用一行 pn_PowerShell_short 的記錄集，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="29763-141">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="29763-142">範例6：建立 SRV 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="29763-142">Example 6: Create a RecordSet of type SRV</span></span>
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

<span data-ttu-id="29763-143">這個命令會在 [私人區域 myzone.com] 中建立名為 _sip 的記錄集。</span><span class="sxs-lookup"><span data-stu-id="29763-143">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="29763-144">記錄集的類型為 SRV，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="29763-144">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="29763-145">它包含一個私有 DNS 記錄，並指向 IP 位址2001.2.3.4。</span><span class="sxs-lookup"><span data-stu-id="29763-145">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="29763-146">服務 (sip) ，而 (tcp) 的通訊協定，則會指定為記錄集名稱的一部分，而不是記錄資料的一部分。</span><span class="sxs-lookup"><span data-stu-id="29763-146">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="29763-147">若要建立只使用一行 pn_PowerShell_short 的記錄集，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="29763-147">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="29763-148">範例7：建立 TXT 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="29763-148">Example 7: Create a RecordSet of type TXT</span></span>
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

<span data-ttu-id="29763-149">這個命令會在 [私人區域 myzone.com] 中建立名為「文字」的記錄集。</span><span class="sxs-lookup"><span data-stu-id="29763-149">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="29763-150">記錄集的類型為 TXT，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="29763-150">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="29763-151">它包含單一的私人 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="29763-151">It contains a single Private DNS record.</span></span> <span data-ttu-id="29763-152">若要建立只使用一行 pn_PowerShell_short 的記錄集，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="29763-152">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="29763-153">範例8：在區域 apex 建立記錄集</span><span class="sxs-lookup"><span data-stu-id="29763-153">Example 8:  Create a RecordSet at the zone apex</span></span>
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

<span data-ttu-id="29763-154">這個命令會在 apex (或私人區域 myzone.com 的根) 建立記錄集。</span><span class="sxs-lookup"><span data-stu-id="29763-154">This command creates a RecordSet at the apex (or root) of the private zone myzone.com.</span></span> <span data-ttu-id="29763-155">若要這樣做，記錄集名稱會指定為 "@" (包括雙引號) 。</span><span class="sxs-lookup"><span data-stu-id="29763-155">To do this, the record set name is specified as "@" (including the double-quotes).</span></span> <span data-ttu-id="29763-156">您無法在區域的 apex 建立 CNAME 記錄。</span><span class="sxs-lookup"><span data-stu-id="29763-156">You cannot create CNAME records at the apex of a zone.</span></span> <span data-ttu-id="29763-157">這是 DNS 標準的限制式;它不是 Azure 私人 DNS 的限制。</span><span class="sxs-lookup"><span data-stu-id="29763-157">This is a constraint of the DNS standards; it is not a limitation of Azure Private DNS.</span></span> <span data-ttu-id="29763-158">若要建立只使用一行 pn_PowerShell_short 的記錄集，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="29763-158">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="29763-159">範例9：建立萬用字元記錄集</span><span class="sxs-lookup"><span data-stu-id="29763-159">Example 9:  Create a wildcard Record Set</span></span>

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

<span data-ttu-id="29763-160">這個命令會在 [私人區域 myzone.com] 中建立一個名為 \* 的記錄集。</span><span class="sxs-lookup"><span data-stu-id="29763-160">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="29763-161">這是萬用字元記錄集。</span><span class="sxs-lookup"><span data-stu-id="29763-161">This is a wildcard record set.</span></span> <span data-ttu-id="29763-162">若要建立只使用一行 pn_PowerShell_short 的記錄集，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="29763-162">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="29763-163">範例10：建立空白記錄集</span><span class="sxs-lookup"><span data-stu-id="29763-163">Example 10:  Create an empty Record Set</span></span>

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

<span data-ttu-id="29763-164">這個命令會在 [私人區域 myzone.com] 中建立一個名為 \* 的記錄集。</span><span class="sxs-lookup"><span data-stu-id="29763-164">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="29763-165">記錄集的類型是 A，且每個小時的 TTL (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="29763-165">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="29763-166">這是一個空的記錄集，可充當預留位置，您稍後可以在該位置新增記錄。</span><span class="sxs-lookup"><span data-stu-id="29763-166">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="29763-167">範例11：建立記錄集並隱含全部確認</span><span class="sxs-lookup"><span data-stu-id="29763-167">Example 11:  Create a record set and suppress all confirmation</span></span>

```powershell
PS C:\>$RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="29763-168">這個命令會建立記錄集。</span><span class="sxs-lookup"><span data-stu-id="29763-168">This command creates a RecordSet.</span></span> <span data-ttu-id="29763-169">Overwrite 參數可確保此記錄集會覆寫具有相同名稱和類型的任何預先存在的記錄集， (該記錄集中現有的記錄會遺失) 。</span><span class="sxs-lookup"><span data-stu-id="29763-169">The Overwrite parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span> <span data-ttu-id="29763-170">含 $False 值的確認參數會抑制確認提示。</span><span class="sxs-lookup"><span data-stu-id="29763-170">The Confirm parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="29763-171">參數</span><span class="sxs-lookup"><span data-stu-id="29763-171">PARAMETERS</span></span>

### <span data-ttu-id="29763-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29763-172">-DefaultProfile</span></span>
<span data-ttu-id="29763-173">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="29763-173">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29763-174">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="29763-174">-Metadata</span></span>
<span data-ttu-id="29763-175">代表資源標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="29763-175">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="29763-176">-名稱</span><span class="sxs-lookup"><span data-stu-id="29763-176">-Name</span></span>
<span data-ttu-id="29763-177">此記錄集中的記錄名稱 (相對於區域的名稱，且不需要終止點) 。</span><span class="sxs-lookup"><span data-stu-id="29763-177">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

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

### <span data-ttu-id="29763-178">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="29763-178">-Overwrite</span></span>
<span data-ttu-id="29763-179">如果記錄集已存在，請勿失敗。</span><span class="sxs-lookup"><span data-stu-id="29763-179">Do not fail if the record set already exists.</span></span>

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

### <span data-ttu-id="29763-180">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="29763-180">-ParentResourceId</span></span>
<span data-ttu-id="29763-181">私人 DNS 區域 ResourceID。</span><span class="sxs-lookup"><span data-stu-id="29763-181">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="29763-182">-PrivateDnsRecord</span><span class="sxs-lookup"><span data-stu-id="29763-182">-PrivateDnsRecord</span></span>
<span data-ttu-id="29763-183">屬於此記錄集的專用 dns 記錄。</span><span class="sxs-lookup"><span data-stu-id="29763-183">The private dns records that are part of this record set.</span></span>

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

### <span data-ttu-id="29763-184">-RecordType</span><span class="sxs-lookup"><span data-stu-id="29763-184">-RecordType</span></span>
<span data-ttu-id="29763-185">此記錄集中私人 DNS 記錄的類型。</span><span class="sxs-lookup"><span data-stu-id="29763-185">The type of Private DNS records in this record set.</span></span>

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

### <span data-ttu-id="29763-186">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29763-186">-ResourceGroupName</span></span>
<span data-ttu-id="29763-187">該區域所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="29763-187">The resource group to which the zone belongs.</span></span>

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

### <span data-ttu-id="29763-188">-Ttl</span><span class="sxs-lookup"><span data-stu-id="29763-188">-Ttl</span></span>
<span data-ttu-id="29763-189">此記錄集中所有記錄的 [TTL] 值。</span><span class="sxs-lookup"><span data-stu-id="29763-189">The TTL value of all the records in this record set.</span></span>

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

### <span data-ttu-id="29763-190">-Zone</span><span class="sxs-lookup"><span data-stu-id="29763-190">-Zone</span></span>
<span data-ttu-id="29763-191">代表要在其中建立記錄集之區域的 PrivateDnsZone 物件。</span><span class="sxs-lookup"><span data-stu-id="29763-191">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

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

### <span data-ttu-id="29763-192">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="29763-192">-ZoneName</span></span>
<span data-ttu-id="29763-193">在其中建立記錄集的區域 (，不需終止點) 。</span><span class="sxs-lookup"><span data-stu-id="29763-193">The zone in which to create the record set (without a terminating dot).</span></span>

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

### <span data-ttu-id="29763-194">-確認</span><span class="sxs-lookup"><span data-stu-id="29763-194">-Confirm</span></span>
<span data-ttu-id="29763-195">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="29763-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29763-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29763-196">-WhatIf</span></span>
<span data-ttu-id="29763-197">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="29763-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29763-198">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="29763-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29763-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29763-199">CommonParameters</span></span>
<span data-ttu-id="29763-200">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="29763-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29763-201">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="29763-201">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29763-202">輸入</span><span class="sxs-lookup"><span data-stu-id="29763-202">INPUTS</span></span>

### <span data-ttu-id="29763-203">PSPrivateDnsZone 中的 PrivateDns。</span><span class="sxs-lookup"><span data-stu-id="29763-203">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="29763-204">System.object</span><span class="sxs-lookup"><span data-stu-id="29763-204">System.String</span></span>

## <span data-ttu-id="29763-205">輸出</span><span class="sxs-lookup"><span data-stu-id="29763-205">OUTPUTS</span></span>

### <span data-ttu-id="29763-206">PSPrivateDnsRecordSet 中的 PrivateDns。</span><span class="sxs-lookup"><span data-stu-id="29763-206">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="29763-207">筆記</span><span class="sxs-lookup"><span data-stu-id="29763-207">NOTES</span></span>

## <span data-ttu-id="29763-208">相關連結</span><span class="sxs-lookup"><span data-stu-id="29763-208">RELATED LINKS</span></span>
