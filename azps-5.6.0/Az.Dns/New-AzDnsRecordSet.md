---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/powershell/module/az.dns/new-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
ms.openlocfilehash: f1731cb0eceb4474c233db859c3f4edb10461fe4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910137"
---
# <span data-ttu-id="49f0e-101">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="49f0e-101">New-AzDnsRecordSet</span></span>

## <span data-ttu-id="49f0e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="49f0e-102">SYNOPSIS</span></span>
<span data-ttu-id="49f0e-103">建立 DNS 記錄集。</span><span class="sxs-lookup"><span data-stu-id="49f0e-103">Creates a DNS record set.</span></span>

## <span data-ttu-id="49f0e-104">語法</span><span class="sxs-lookup"><span data-stu-id="49f0e-104">SYNTAX</span></span>

### <span data-ttu-id="49f0e-105">欄位 (預設) </span><span class="sxs-lookup"><span data-stu-id="49f0e-105">Fields (Default)</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49f0e-106">AliasFields</span><span class="sxs-lookup"><span data-stu-id="49f0e-106">AliasFields</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> [-Ttl <UInt32>]
 -RecordType <RecordType> -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49f0e-107">物件</span><span class="sxs-lookup"><span data-stu-id="49f0e-107">Object</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49f0e-108">AliasObject</span><span class="sxs-lookup"><span data-stu-id="49f0e-108">AliasObject</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> [-Ttl <UInt32>] -RecordType <RecordType>
 -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49f0e-109">描述</span><span class="sxs-lookup"><span data-stu-id="49f0e-109">DESCRIPTION</span></span>
<span data-ttu-id="49f0e-110">**New-AzDnsRecordSet** Cmdlet 會以指定的名稱建立新的網域名稱系統 (DNS) 記錄集，並輸入指定的區域。</span><span class="sxs-lookup"><span data-stu-id="49f0e-110">The **New-AzDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="49f0e-111">**RecordSet** 物件是一組名稱與類型相同的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="49f0e-111">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="49f0e-112">請注意，名稱是相對於區域，而非完整名稱。</span><span class="sxs-lookup"><span data-stu-id="49f0e-112">Note that the name is relative to the zone and not the fully qualified name.</span></span>
<span data-ttu-id="49f0e-113">*DnsRecords* 參數會指定記錄集的記錄。</span><span class="sxs-lookup"><span data-stu-id="49f0e-113">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="49f0e-114">此參數採用使用 New-AzDnsRecordConfig 建構的 DNS 記錄陣列。</span><span class="sxs-lookup"><span data-stu-id="49f0e-114">This parameter takes an array of DNS records, constructed using New-AzDnsRecordConfig.</span></span>
<span data-ttu-id="49f0e-115">您可以使用管線運算子將 **DnsZone** 物件傳遞到此 Cmdlet，或將 **DnsZone** 物件傳遞為 *Zone* 參數，或者您也可以按名稱指定區域。</span><span class="sxs-lookup"><span data-stu-id="49f0e-115">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>
<span data-ttu-id="49f0e-116">您可以使用確認 *參數$ConfirmPreference* Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="49f0e-116">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="49f0e-117">如果符合 **的 RecordSet** 已存在 (名稱和記錄類型) ，您必須指定 *覆* 寫參數，否則 Cmdlet 不會建立 **新的 RecordSet。**</span><span class="sxs-lookup"><span data-stu-id="49f0e-117">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="49f0e-118">例子</span><span class="sxs-lookup"><span data-stu-id="49f0e-118">EXAMPLES</span></span>

### <span data-ttu-id="49f0e-119">範例 1：建立類型 A 的 RecordSet</span><span class="sxs-lookup"><span data-stu-id="49f0e-119">Example 1: Create a RecordSet of type A</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzDnsRecordConfig to add each record to the $Records array,
# then call New-AzDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="49f0e-120">此範例在 myzone.com 區域中建立名為 www 的 **RecordSet。**</span><span class="sxs-lookup"><span data-stu-id="49f0e-120">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="49f0e-121">記錄集的類型為 A，TTL 為 1 小時， (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="49f0e-121">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="49f0e-122">它包含單一 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="49f0e-122">It contains a single DNS record.</span></span>

### <span data-ttu-id="49f0e-123">範例 2：建立類型 AAAA 的 RecordSet</span><span class="sxs-lookup"><span data-stu-id="49f0e-123">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="49f0e-124">此範例在 myzone.com 區域中建立名為 www 的 **RecordSet。**</span><span class="sxs-lookup"><span data-stu-id="49f0e-124">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="49f0e-125">記錄集的類型為 AAAA，TTL 為 1 小時， (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="49f0e-125">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="49f0e-126">它包含單一 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="49f0e-126">It contains a single DNS record.</span></span>
<span data-ttu-id="49f0e-127">若要使用一行記錄來建立 **記錄** 集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。</span><span class="sxs-lookup"><span data-stu-id="49f0e-127">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="49f0e-128">範例 3：建立類型 CNAME 的 RecordSet</span><span class="sxs-lookup"><span data-stu-id="49f0e-128">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="49f0e-129">此範例在 myzone.com 區域中建立名為 www 的 **RecordSet。**</span><span class="sxs-lookup"><span data-stu-id="49f0e-129">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="49f0e-130">記錄集的類型為 CNAME，TTL 為 1 小時， (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="49f0e-130">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="49f0e-131">它包含單一 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="49f0e-131">It contains a single DNS record.</span></span>
<span data-ttu-id="49f0e-132">若要使用一行記錄來建立 **記錄** 集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。</span><span class="sxs-lookup"><span data-stu-id="49f0e-132">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="49f0e-133">範例 4：建立類型 MX 的 RecordSet</span><span class="sxs-lookup"><span data-stu-id="49f0e-133">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "mail" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="49f0e-134">此命令在 myzone.com 區域中建立名為 www 的 **RecordSet。**</span><span class="sxs-lookup"><span data-stu-id="49f0e-134">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="49f0e-135">記錄集的類型為 MX，TTL 為 1 小時， (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="49f0e-135">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="49f0e-136">它包含單一 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="49f0e-136">It contains a single DNS record.</span></span>
<span data-ttu-id="49f0e-137">若要使用一行記錄來建立 **記錄** 集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。</span><span class="sxs-lookup"><span data-stu-id="49f0e-137">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="49f0e-138">範例 5：建立類型 NS 的 RecordSet</span><span class="sxs-lookup"><span data-stu-id="49f0e-138">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="49f0e-139">此命令在活動區域建立名為 ns1 的 **RecordSet** myzone.com。</span><span class="sxs-lookup"><span data-stu-id="49f0e-139">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="49f0e-140">記錄集的類型為 NS，TTL 為 1 小時， (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="49f0e-140">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="49f0e-141">它包含單一 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="49f0e-141">It contains a single DNS record.</span></span>
<span data-ttu-id="49f0e-142">若要使用一行記錄來建立 **記錄** 集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。</span><span class="sxs-lookup"><span data-stu-id="49f0e-142">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="49f0e-143">範例 6：建立類型 PTR 的 RecordSet</span><span class="sxs-lookup"><span data-stu-id="49f0e-143">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="49f0e-144">此命令在 3.2.1.in-addr.arpa 區域中建立名為 4 的 RecordSet。</span><span class="sxs-lookup"><span data-stu-id="49f0e-144">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="49f0e-145">記錄集的類型為 PTR，且 TTL 為 1 小時， (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="49f0e-145">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="49f0e-146">它包含單一 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="49f0e-146">It contains a single DNS record.</span></span>
<span data-ttu-id="49f0e-147">若要使用一行記錄來建立 **記錄** 集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。</span><span class="sxs-lookup"><span data-stu-id="49f0e-147">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="49f0e-148">範例 7：建立類型 SRV 的 RecordSet</span><span class="sxs-lookup"><span data-stu-id="49f0e-148">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="49f0e-149">此命令會建立一個名為 _sip._tcp 的 **RecordSet，myzone.com。**</span><span class="sxs-lookup"><span data-stu-id="49f0e-149">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="49f0e-150">記錄集的類型為 SRV，TTL 為 1 小時， (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="49f0e-150">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="49f0e-151">它包含指向 IP 位址 2001.2.3.4 的單一 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="49f0e-151">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="49f0e-152">服務 (sip) 和 (tcp) 會指定為記錄集名稱的一部分，而不是記錄資料的一部分。</span><span class="sxs-lookup"><span data-stu-id="49f0e-152">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="49f0e-153">若要使用一行記錄來建立 **記錄** 集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。</span><span class="sxs-lookup"><span data-stu-id="49f0e-153">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="49f0e-154">範例 8：建立類型 TXT 的 RecordSet</span><span class="sxs-lookup"><span data-stu-id="49f0e-154">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="49f0e-155">此命令會在這個區域中建立名為文字的 **RecordSet** myzone.com。</span><span class="sxs-lookup"><span data-stu-id="49f0e-155">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="49f0e-156">記錄集的類型為 TXT，TTL 為 1 小時， (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="49f0e-156">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="49f0e-157">它包含單一 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="49f0e-157">It contains a single DNS record.</span></span>
<span data-ttu-id="49f0e-158">若要使用一行記錄來建立 **記錄** 集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。</span><span class="sxs-lookup"><span data-stu-id="49f0e-158">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="49f0e-159">範例 9：在區域頂點建立 RecordSet</span><span class="sxs-lookup"><span data-stu-id="49f0e-159">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="49f0e-160">此命令會建立 **一個 RecordSet，** 位於 (區域) 的myzone.com。</span><span class="sxs-lookup"><span data-stu-id="49f0e-160">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="49f0e-161">若要這麼做，記錄集名稱會指定為 "@" (包括雙引號) 。</span><span class="sxs-lookup"><span data-stu-id="49f0e-161">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>
<span data-ttu-id="49f0e-162">您無法在一個區域的頂點建立 CNAME 記錄。</span><span class="sxs-lookup"><span data-stu-id="49f0e-162">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="49f0e-163">這是 DNS 標準的限制;這不是 Azure DNS 的限制。</span><span class="sxs-lookup"><span data-stu-id="49f0e-163">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>
<span data-ttu-id="49f0e-164">若要使用一行記錄來建立 **記錄** 集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。</span><span class="sxs-lookup"><span data-stu-id="49f0e-164">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="49f0e-165">範例 10：建立萬用字元記錄集</span><span class="sxs-lookup"><span data-stu-id="49f0e-165">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="49f0e-166">此命令會建立一個名為 \***的 RecordSet，myzone.com。**</span><span class="sxs-lookup"><span data-stu-id="49f0e-166">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="49f0e-167">這是萬用字元記錄集。</span><span class="sxs-lookup"><span data-stu-id="49f0e-167">This is a wildcard record set.</span></span>
<span data-ttu-id="49f0e-168">若要使用一行記錄來建立 **記錄** 集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。</span><span class="sxs-lookup"><span data-stu-id="49f0e-168">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="49f0e-169">範例 11：建立空白記錄集</span><span class="sxs-lookup"><span data-stu-id="49f0e-169">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="49f0e-170">此命令在 myzone.com 區域中建立名為 www 的 **RecordSet。**</span><span class="sxs-lookup"><span data-stu-id="49f0e-170">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="49f0e-171">記錄集的類型為 A，TTL 為 1 小時， (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="49f0e-171">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="49f0e-172">這是空白的記錄集，可做為預留位置，日後您可以新增記錄。</span><span class="sxs-lookup"><span data-stu-id="49f0e-172">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="49f0e-173">範例 12：建立記錄集並隱藏所有確認</span><span class="sxs-lookup"><span data-stu-id="49f0e-173">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="49f0e-174">此命令會建立 **RecordSet。**</span><span class="sxs-lookup"><span data-stu-id="49f0e-174">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="49f0e-175">覆 *寫* 參數可確保此記錄集覆寫任何名稱相同且類型相同的現有記錄集 (該記錄集的現有記錄會遺失) 。</span><span class="sxs-lookup"><span data-stu-id="49f0e-175">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="49f0e-176">包含 *值* $False的確認參數會隱藏確認提示。</span><span class="sxs-lookup"><span data-stu-id="49f0e-176">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="49f0e-177">參數</span><span class="sxs-lookup"><span data-stu-id="49f0e-177">PARAMETERS</span></span>

### <span data-ttu-id="49f0e-178">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49f0e-178">-DefaultProfile</span></span>
<span data-ttu-id="49f0e-179">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="49f0e-179">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49f0e-180">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="49f0e-180">-DnsRecords</span></span>
<span data-ttu-id="49f0e-181">指定要納入記錄集的 DNS 記錄陣列。</span><span class="sxs-lookup"><span data-stu-id="49f0e-181">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="49f0e-182">您可以使用 Cmdlet New-AzDnsRecordConfig建立 DNS 記錄物件。</span><span class="sxs-lookup"><span data-stu-id="49f0e-182">You can use the New-AzDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="49f0e-183">請參閱範例以瞭解更多資訊。</span><span class="sxs-lookup"><span data-stu-id="49f0e-183">See the examples for more information.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordBase[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49f0e-184">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="49f0e-184">-Metadata</span></span>
<span data-ttu-id="49f0e-185">指定要與 RecordSet 建立關聯的中繼資料陣列。</span><span class="sxs-lookup"><span data-stu-id="49f0e-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="49f0e-186">中繼資料是使用以雜湊表格表示的名稱值組來指定，例如 @{"dept"="shopping";"env"="production"}.</span><span class="sxs-lookup"><span data-stu-id="49f0e-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @{"dept"="shopping";"env"="production"}.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49f0e-187">-名稱</span><span class="sxs-lookup"><span data-stu-id="49f0e-187">-Name</span></span>
<span data-ttu-id="49f0e-188">指定要建立 **之 RecordSet** 的名稱。</span><span class="sxs-lookup"><span data-stu-id="49f0e-188">Specifies the name of the **RecordSet** to create.</span></span>

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

### <span data-ttu-id="49f0e-189">-覆寫</span><span class="sxs-lookup"><span data-stu-id="49f0e-189">-Overwrite</span></span>
<span data-ttu-id="49f0e-190">表示此 Cmdlet 會覆寫指定的 **RecordSet** ，如果已經存在。</span><span class="sxs-lookup"><span data-stu-id="49f0e-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

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

### <span data-ttu-id="49f0e-191">-RecordType</span><span class="sxs-lookup"><span data-stu-id="49f0e-191">-RecordType</span></span>
<span data-ttu-id="49f0e-192">指定要建立 DNS 記錄的類型。</span><span class="sxs-lookup"><span data-stu-id="49f0e-192">Specifies the type of DNS record to create.</span></span>
<span data-ttu-id="49f0e-193">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="49f0e-193">Valid values are:</span></span>
- <span data-ttu-id="49f0e-194">A</span><span class="sxs-lookup"><span data-stu-id="49f0e-194">A</span></span>
- <span data-ttu-id="49f0e-195">Aaaa</span><span class="sxs-lookup"><span data-stu-id="49f0e-195">AAAA</span></span>
- <span data-ttu-id="49f0e-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="49f0e-196">CNAME</span></span>
- <span data-ttu-id="49f0e-197">Mx</span><span class="sxs-lookup"><span data-stu-id="49f0e-197">MX</span></span>
- <span data-ttu-id="49f0e-198">Ns</span><span class="sxs-lookup"><span data-stu-id="49f0e-198">NS</span></span>
- <span data-ttu-id="49f0e-199">Ptr</span><span class="sxs-lookup"><span data-stu-id="49f0e-199">PTR</span></span>
- <span data-ttu-id="49f0e-200">SRV</span><span class="sxs-lookup"><span data-stu-id="49f0e-200">SRV</span></span>
- <span data-ttu-id="49f0e-201">當區域建立時，TXT 的 DNS 記錄會自動建立，而且無法手動建立。</span><span class="sxs-lookup"><span data-stu-id="49f0e-201">TXT SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49f0e-202">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49f0e-202">-ResourceGroupName</span></span>
<span data-ttu-id="49f0e-203">指定包含 DNS 區域的資源群組。</span><span class="sxs-lookup"><span data-stu-id="49f0e-203">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="49f0e-204">您也必須指定 *ZoneName* 參數，以指定區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="49f0e-204">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>
<span data-ttu-id="49f0e-205">或者，您也可以使用 Zone 參數傳遞 DNS 區域物件來指定 *區域* 和資源群組。</span><span class="sxs-lookup"><span data-stu-id="49f0e-205">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49f0e-206">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="49f0e-206">-TargetResourceId</span></span>
<span data-ttu-id="49f0e-207">別名目標資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="49f0e-207">Alias Target Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49f0e-208">-Ttl</span><span class="sxs-lookup"><span data-stu-id="49f0e-208">-Ttl</span></span>
<span data-ttu-id="49f0e-209">指定 DNS RecordSet (TTL) 上的時間。</span><span class="sxs-lookup"><span data-stu-id="49f0e-209">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: Fields, Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.UInt32
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49f0e-210">-區域</span><span class="sxs-lookup"><span data-stu-id="49f0e-210">-Zone</span></span>
<span data-ttu-id="49f0e-211">指定要建立 RecordSet 的 **Dns 區域**。</span><span class="sxs-lookup"><span data-stu-id="49f0e-211">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="49f0e-212">或者，您可以使用 *ZoneName* 和 *ResourceGroupName* 參數指定區域。</span><span class="sxs-lookup"><span data-stu-id="49f0e-212">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49f0e-213">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="49f0e-213">-ZoneName</span></span>
<span data-ttu-id="49f0e-214">指定要建立 **RecordSet** 的區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="49f0e-214">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="49f0e-215">您也必須使用 *ResourceGroupName* 參數指定包含區域的資源群組。</span><span class="sxs-lookup"><span data-stu-id="49f0e-215">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="49f0e-216">或者，您也可以使用 Zone 參數傳遞 DNS 區域物件來指定 *區域* 和資源群組。</span><span class="sxs-lookup"><span data-stu-id="49f0e-216">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49f0e-217">-確認</span><span class="sxs-lookup"><span data-stu-id="49f0e-217">-Confirm</span></span>
<span data-ttu-id="49f0e-218">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="49f0e-218">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49f0e-219">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49f0e-219">-WhatIf</span></span>
<span data-ttu-id="49f0e-220">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="49f0e-220">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49f0e-221">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="49f0e-221">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49f0e-222">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49f0e-222">CommonParameters</span></span>
<span data-ttu-id="49f0e-223">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="49f0e-223">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49f0e-224">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="49f0e-224">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49f0e-225">輸入</span><span class="sxs-lookup"><span data-stu-id="49f0e-225">INPUTS</span></span>

### <span data-ttu-id="49f0e-226">System.String</span><span class="sxs-lookup"><span data-stu-id="49f0e-226">System.String</span></span>

### <span data-ttu-id="49f0e-227">Microsoft.Azure.Commands.dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="49f0e-227">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="49f0e-228">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="49f0e-228">System.UInt32</span></span>

### <span data-ttu-id="49f0e-229">Microsoft.Azure.management.dns.models.RecordType</span><span class="sxs-lookup"><span data-stu-id="49f0e-229">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="49f0e-230">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="49f0e-230">System.Collections.Hashtable</span></span>

### <span data-ttu-id="49f0e-231">Microsoft.Azure.Commands.dns.DnsRecordBase[]</span><span class="sxs-lookup"><span data-stu-id="49f0e-231">Microsoft.Azure.Commands.Dns.DnsRecordBase[]</span></span>

## <span data-ttu-id="49f0e-232">輸出</span><span class="sxs-lookup"><span data-stu-id="49f0e-232">OUTPUTS</span></span>

### <span data-ttu-id="49f0e-233">Microsoft.Azure.Commands.dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="49f0e-233">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="49f0e-234">筆記</span><span class="sxs-lookup"><span data-stu-id="49f0e-234">NOTES</span></span>
<span data-ttu-id="49f0e-235">您可以使用 *確認參數來控制* 此 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="49f0e-235">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="49f0e-236">根據預設，如果 Windows PowerShell 變數的 $ConfirmPreference中或較低值，Cmdlet 會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="49f0e-236">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="49f0e-237">如果您 *指定確認或* 確認 *：$True，* 此 Cmdlet 會先提示您確認再執行。</span><span class="sxs-lookup"><span data-stu-id="49f0e-237">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="49f0e-238">如果您指定 *確認：$False，Cmdlet* 不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="49f0e-238">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="49f0e-239">相關連結</span><span class="sxs-lookup"><span data-stu-id="49f0e-239">RELATED LINKS</span></span>

[<span data-ttu-id="49f0e-240">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="49f0e-240">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="49f0e-241">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="49f0e-241">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="49f0e-242">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="49f0e-242">New-AzDnsRecordConfig</span></span>](./New-AzDnsRecordConfig.md)

[<span data-ttu-id="49f0e-243">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="49f0e-243">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="49f0e-244">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="49f0e-244">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
