---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsRecordSet.md
ms.openlocfilehash: 0327837f6e28d7147892669bd77b1aa78747a5c1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795658"
---
# <span data-ttu-id="f1bfe-101">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f1bfe-101">New-AzDnsRecordSet</span></span>

## <span data-ttu-id="f1bfe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f1bfe-102">SYNOPSIS</span></span>
<span data-ttu-id="f1bfe-103">建立 DNS 記錄集。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-103">Creates a DNS record set.</span></span>

## <span data-ttu-id="f1bfe-104">句法</span><span class="sxs-lookup"><span data-stu-id="f1bfe-104">SYNTAX</span></span>

### <span data-ttu-id="f1bfe-105">區域</span><span class="sxs-lookup"><span data-stu-id="f1bfe-105">Fields</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1bfe-106">面向</span><span class="sxs-lookup"><span data-stu-id="f1bfe-106">Object</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1bfe-107">說明</span><span class="sxs-lookup"><span data-stu-id="f1bfe-107">DESCRIPTION</span></span>
<span data-ttu-id="f1bfe-108">**新的 AzDnsRecordSet** Cmdlet 會在指定的區域中使用指定的名稱和類型， (DNS) 記錄集建立新的網域名稱系統。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-108">The **New-AzDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="f1bfe-109">**記錄集** 物件是一組具有相同名稱和類型的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-109">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="f1bfe-110">請注意，該名稱是相對於區域而非完全限定名稱。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-110">Note that the name is relative to the zone and not the fully qualified name.</span></span>

<span data-ttu-id="f1bfe-111">*DnsRecords* 參數會指定記錄集中的記錄。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-111">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="f1bfe-112">這個參數會採用一個 DNS 記錄陣列，並使用新的 AzDnsRecordConfig 來構造。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-112">This parameter takes an array of DNS records, constructed using New-AzDnsRecordConfig.</span></span>

<span data-ttu-id="f1bfe-113">您可以使用管線運算子，將 **DnsZone** 物件傳遞到這個 Cmdlet，或者您可以將 **DnsZone** 物件傳遞為 *zone* 參數，或者也可以依名稱指定該區域。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-113">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>

<span data-ttu-id="f1bfe-114">您可以使用 *Confirm* 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-114">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="f1bfe-115">如果相符的 **記錄集** 已存在 (相同的名稱和記錄類型) ，您必須指定 *Overwrite* 參數，否則 Cmdlet 不會建立新的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-115">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="f1bfe-116">示例</span><span class="sxs-lookup"><span data-stu-id="f1bfe-116">EXAMPLES</span></span>

### <span data-ttu-id="f1bfe-117">範例1：建立 A 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="f1bfe-117">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="f1bfe-118">這個範例會在區域 myzone.com 中建立名為 www 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-118">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="f1bfe-119">記錄集的類型是 A，且每個小時的 TTL (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-119">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="f1bfe-120">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-120">It contains a single DNS record.</span></span>

### <span data-ttu-id="f1bfe-121">範例2：建立 AAAA 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="f1bfe-121">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="f1bfe-122">這個範例會在區域 myzone.com 中建立名為 www 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-122">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="f1bfe-123">記錄集的類型是 AAAA，且每個小時的 TTL (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-123">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="f1bfe-124">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-124">It contains a single DNS record.</span></span>

<span data-ttu-id="f1bfe-125">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-125">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f1bfe-126">範例3：建立 CNAME 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="f1bfe-126">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="f1bfe-127">這個範例會在區域 myzone.com 中建立名為 www 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-127">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="f1bfe-128">此記錄集的類型為 CNAME，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-128">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="f1bfe-129">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-129">It contains a single DNS record.</span></span>

<span data-ttu-id="f1bfe-130">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-130">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f1bfe-131">範例4：建立 MX 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="f1bfe-131">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="f1bfe-132">這個命令會在區域 myzone.com 中建立名為 www 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-132">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="f1bfe-133">記錄集的類型是 MX，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-133">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="f1bfe-134">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-134">It contains a single DNS record.</span></span>

<span data-ttu-id="f1bfe-135">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-135">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f1bfe-136">範例5：建立 NS 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="f1bfe-136">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="f1bfe-137">這個命令會在區域 myzone.com 中建立一個名為 ns1 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-137">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="f1bfe-138">記錄集的類型是 NS，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-138">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="f1bfe-139">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-139">It contains a single DNS record.</span></span>

<span data-ttu-id="f1bfe-140">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-140">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f1bfe-141">範例6：建立類型指標的記錄集</span><span class="sxs-lookup"><span data-stu-id="f1bfe-141">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="f1bfe-142">這個命令會在 zone 3.2.1.in-arpa 中建立名為4的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-142">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="f1bfe-143">記錄集的類型是 PTR，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-143">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="f1bfe-144">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-144">It contains a single DNS record.</span></span>

<span data-ttu-id="f1bfe-145">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-145">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f1bfe-146">範例7：建立 SRV 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="f1bfe-146">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="f1bfe-147">這個命令會在區域 myzone.com 中建立名為 _sip 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-147">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="f1bfe-148">記錄集的類型為 SRV，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-148">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="f1bfe-149">它包含單一 DNS 記錄，並指向 IP 位址2001.2.3.4。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-149">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>

<span data-ttu-id="f1bfe-150">服務 (sip) ，而 (tcp) 的通訊協定，則會指定為記錄集名稱的一部分，而不是記錄資料的一部分。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-150">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>

<span data-ttu-id="f1bfe-151">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-151">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f1bfe-152">範例8：建立 TXT 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="f1bfe-152">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="f1bfe-153">這個命令會在區域 myzone.com 中建立名為 text 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-153">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="f1bfe-154">記錄集的類型為 TXT，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-154">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="f1bfe-155">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-155">It contains a single DNS record.</span></span>

<span data-ttu-id="f1bfe-156">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-156">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f1bfe-157">範例9：在區域 apex 建立記錄集</span><span class="sxs-lookup"><span data-stu-id="f1bfe-157">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="f1bfe-158">這個命令會在區域 myzone.com 的 apex (或根) 建立 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-158">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="f1bfe-159">若要這樣做，記錄集名稱會指定為 "@" (包括雙引號) 。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-159">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>

<span data-ttu-id="f1bfe-160">您無法在區域的 apex 建立 CNAME 記錄。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-160">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="f1bfe-161">這是 DNS 標準的限制式;這不是 Azure DNS 的限制。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-161">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>

<span data-ttu-id="f1bfe-162">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-162">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f1bfe-163">範例10：建立萬用字元記錄集</span><span class="sxs-lookup"><span data-stu-id="f1bfe-163">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="f1bfe-164">這個命令會在區域 myzone.com 中建立一個名為 \* 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-164">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="f1bfe-165">這是萬用字元記錄集。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-165">This is a wildcard record set.</span></span>

<span data-ttu-id="f1bfe-166">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-166">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f1bfe-167">範例11：建立空白記錄集</span><span class="sxs-lookup"><span data-stu-id="f1bfe-167">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="f1bfe-168">這個命令會在區域 myzone.com 中建立名為 www 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-168">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="f1bfe-169">記錄集的類型是 A，且每個小時的 TTL (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-169">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="f1bfe-170">這是一個空的記錄集，可充當預留位置，您稍後可以在該位置新增記錄。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-170">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="f1bfe-171">範例12：建立記錄集並隱含所有確認</span><span class="sxs-lookup"><span data-stu-id="f1bfe-171">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="f1bfe-172">這個命令會建立 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-172">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="f1bfe-173">*Overwrite* 參數可確保此記錄集會覆寫具有相同名稱和類型的任何預先存在的記錄集， (該記錄集中現有的記錄會遺失) 。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-173">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="f1bfe-174">含 $False 值的 *確認* 參數會抑制確認提示。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-174">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="f1bfe-175">參數</span><span class="sxs-lookup"><span data-stu-id="f1bfe-175">PARAMETERS</span></span>

### <span data-ttu-id="f1bfe-176">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="f1bfe-176">-DnsRecords</span></span>
<span data-ttu-id="f1bfe-177">指定要包含在記錄集中的 DNS 記錄陣列。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-177">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="f1bfe-178">您可以使用 New-AzDnsRecordConfig Cmdlet 來建立 DNS 記錄物件。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-178">You can use the New-AzDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="f1bfe-179">如需詳細資訊，請參閱範例。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-179">See the examples for more information.</span></span>

```yaml
Type: DnsRecordBase[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1bfe-180">-Force</span><span class="sxs-lookup"><span data-stu-id="f1bfe-180">-Force</span></span>
<span data-ttu-id="f1bfe-181">此 Cmdlet 已棄用此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-181">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="f1bfe-182">在未來版本中將會移除它。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-182">It will be removed in a future release.</span></span>

<span data-ttu-id="f1bfe-183">若要控制此 Cmdlet 是否提示您 comfirmation，請使用 *Confirm* 參數。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-183">To control whether this cmdlet prompts you for comfirmation, use the *Confirm* parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1bfe-184">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="f1bfe-184">-Metadata</span></span>
<span data-ttu-id="f1bfe-185">指定要與記錄集相關聯的中繼資料陣列。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="f1bfe-186">中繼資料是使用以雜湊資料表表示的名稱值對指定，例如 @ ( @ {"Name" = "部門";"值" = "購物"}，@ {"Name" = "env";"Value" = "生產"} ) 。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @(@{"Name"="dept"; "Value"="shopping"}, @{"Name"="env"; "Value"="production"}).</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1bfe-187">-名稱</span><span class="sxs-lookup"><span data-stu-id="f1bfe-187">-Name</span></span>
<span data-ttu-id="f1bfe-188">指定要建立的 **記錄集** 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-188">Specifies the name of the **RecordSet** to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1bfe-189">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="f1bfe-189">-Overwrite</span></span>
<span data-ttu-id="f1bfe-190">表示此 Cmdlet 會覆寫指定的 **記錄集** （如果已存在）。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1bfe-191">-RecordType</span><span class="sxs-lookup"><span data-stu-id="f1bfe-191">-RecordType</span></span>
<span data-ttu-id="f1bfe-192">指定要建立的 DNS 記錄類型。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-192">Specifies the type of DNS record to create.</span></span>

<span data-ttu-id="f1bfe-193">有效值為：</span><span class="sxs-lookup"><span data-stu-id="f1bfe-193">Valid values are:</span></span>

- <span data-ttu-id="f1bfe-194">是</span><span class="sxs-lookup"><span data-stu-id="f1bfe-194">A</span></span>
- <span data-ttu-id="f1bfe-195">AAAA</span><span class="sxs-lookup"><span data-stu-id="f1bfe-195">AAAA</span></span>
- <span data-ttu-id="f1bfe-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="f1bfe-196">CNAME</span></span>
- <span data-ttu-id="f1bfe-197">MX</span><span class="sxs-lookup"><span data-stu-id="f1bfe-197">MX</span></span>
- <span data-ttu-id="f1bfe-198">NS</span><span class="sxs-lookup"><span data-stu-id="f1bfe-198">NS</span></span>
- <span data-ttu-id="f1bfe-199">PTR</span><span class="sxs-lookup"><span data-stu-id="f1bfe-199">PTR</span></span>
- <span data-ttu-id="f1bfe-200">DNS-SRV</span><span class="sxs-lookup"><span data-stu-id="f1bfe-200">SRV</span></span>
- <span data-ttu-id="f1bfe-201">文字檔</span><span class="sxs-lookup"><span data-stu-id="f1bfe-201">TXT</span></span>

<span data-ttu-id="f1bfe-202">在建立區域時，系統會自動建立 SOA 記錄，而且不能手動建立。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-202">SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

```yaml
Type: RecordType
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1bfe-203">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1bfe-203">-ResourceGroupName</span></span>
<span data-ttu-id="f1bfe-204">指定包含 DNS 區域的資源群組。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-204">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="f1bfe-205">您也必須指定 *ZoneName* 參數來指定區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-205">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>

<span data-ttu-id="f1bfe-206">或者，您也可以使用 *zone* 參數傳入 DNS 區域物件來指定區域和資源群組。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-206">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1bfe-207">-Ttl</span><span class="sxs-lookup"><span data-stu-id="f1bfe-207">-Ttl</span></span>
<span data-ttu-id="f1bfe-208">指定 DNS 記錄集的實際 (TTL) 時間。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-208">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1bfe-209">-Zone</span><span class="sxs-lookup"><span data-stu-id="f1bfe-209">-Zone</span></span>
<span data-ttu-id="f1bfe-210">指定要在其中建立 **記錄集** 的 DnsZone。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-210">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="f1bfe-211">或者，您也可以使用 *ZoneName* 和 *ResourceGroupName* 參數指定區域。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-211">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsZone
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1bfe-212">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="f1bfe-212">-ZoneName</span></span>
<span data-ttu-id="f1bfe-213">指定要在其中建立 **記錄集** 的區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-213">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="f1bfe-214">您也必須使用 *ResourceGroupName* 參數指定包含該區域的資源群組。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-214">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="f1bfe-215">或者，您也可以使用 *zone* 參數傳入 DNS 區域物件來指定區域和資源群組。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-215">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1bfe-216">-確認</span><span class="sxs-lookup"><span data-stu-id="f1bfe-216">-Confirm</span></span>
<span data-ttu-id="f1bfe-217">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-217">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1bfe-218">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1bfe-218">-WhatIf</span></span>
<span data-ttu-id="f1bfe-219">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-219">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1bfe-220">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-220">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1bfe-221">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1bfe-221">CommonParameters</span></span>
<span data-ttu-id="f1bfe-222">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-222">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1bfe-223">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-223">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1bfe-224">輸入</span><span class="sxs-lookup"><span data-stu-id="f1bfe-224">INPUTS</span></span>

### <span data-ttu-id="f1bfe-225">DnsZone （）</span><span class="sxs-lookup"><span data-stu-id="f1bfe-225">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="f1bfe-226">您可以將 DnsZone 物件輸送到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-226">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="f1bfe-227">輸出</span><span class="sxs-lookup"><span data-stu-id="f1bfe-227">OUTPUTS</span></span>

### <span data-ttu-id="f1bfe-228">DnsRecordSet （）</span><span class="sxs-lookup"><span data-stu-id="f1bfe-228">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="f1bfe-229">這個 Cmdlet 會傳回 **RecordSet** 物件。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-229">This cmdlet returns a **RecordSet** object.</span></span>

## <span data-ttu-id="f1bfe-230">筆記</span><span class="sxs-lookup"><span data-stu-id="f1bfe-230">NOTES</span></span>
<span data-ttu-id="f1bfe-231">您可以使用 *Confirm* 參數來控制此 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-231">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="f1bfe-232">根據預設，如果 $ConfirmPreference 的 Windows PowerShell 變數的值為 [中] 或 [低]，則該 Cmdlet 會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-232">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="f1bfe-233">如果您指定 [ *確認* ] 或 [ *確認]： $True* ，此 Cmdlet 會在您執行之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-233">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="f1bfe-234">如果您指定 [ *確認： $False* ]，則 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f1bfe-234">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f1bfe-235">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1bfe-235">RELATED LINKS</span></span>

[<span data-ttu-id="f1bfe-236">附加 AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="f1bfe-236">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="f1bfe-237">AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f1bfe-237">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="f1bfe-238">新-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="f1bfe-238">New-AzDnsRecordConfig</span></span>](./New-AzDnsRecordConfig.md)

[<span data-ttu-id="f1bfe-239">移除-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f1bfe-239">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="f1bfe-240">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f1bfe-240">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
