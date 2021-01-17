---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
ms.openlocfilehash: bb2e9a9729ed911902e493422109cae764ad6d5f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436526"
---
# <span data-ttu-id="79b09-101">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="79b09-101">New-AzDnsRecordSet</span></span>

## <span data-ttu-id="79b09-102">摘要</span><span class="sxs-lookup"><span data-stu-id="79b09-102">SYNOPSIS</span></span>
<span data-ttu-id="79b09-103">建立 DNS 記錄集。</span><span class="sxs-lookup"><span data-stu-id="79b09-103">Creates a DNS record set.</span></span>

## <span data-ttu-id="79b09-104">句法</span><span class="sxs-lookup"><span data-stu-id="79b09-104">SYNTAX</span></span>

### <span data-ttu-id="79b09-105">預設)  (的欄位</span><span class="sxs-lookup"><span data-stu-id="79b09-105">Fields (Default)</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79b09-106">AliasFields</span><span class="sxs-lookup"><span data-stu-id="79b09-106">AliasFields</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> [-Ttl <UInt32>]
 -RecordType <RecordType> -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79b09-107">面向</span><span class="sxs-lookup"><span data-stu-id="79b09-107">Object</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79b09-108">AliasObject</span><span class="sxs-lookup"><span data-stu-id="79b09-108">AliasObject</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> [-Ttl <UInt32>] -RecordType <RecordType>
 -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79b09-109">說明</span><span class="sxs-lookup"><span data-stu-id="79b09-109">DESCRIPTION</span></span>
<span data-ttu-id="79b09-110">**新的 AzDnsRecordSet** Cmdlet 會在指定的區域中使用指定的名稱和類型， (DNS) 記錄集建立新的網域名稱系統。</span><span class="sxs-lookup"><span data-stu-id="79b09-110">The **New-AzDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="79b09-111">**記錄集** 物件是一組具有相同名稱和類型的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="79b09-111">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="79b09-112">請注意，該名稱是相對於區域而非完全限定名稱。</span><span class="sxs-lookup"><span data-stu-id="79b09-112">Note that the name is relative to the zone and not the fully qualified name.</span></span>
<span data-ttu-id="79b09-113">*DnsRecords* 參數會指定記錄集中的記錄。</span><span class="sxs-lookup"><span data-stu-id="79b09-113">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="79b09-114">這個參數會採用一個 DNS 記錄陣列，並使用新的 AzDnsRecordConfig 來構造。</span><span class="sxs-lookup"><span data-stu-id="79b09-114">This parameter takes an array of DNS records, constructed using New-AzDnsRecordConfig.</span></span>
<span data-ttu-id="79b09-115">您可以使用管線運算子，將 **DnsZone** 物件傳遞到這個 Cmdlet，或者您可以將 **DnsZone** 物件傳遞為 *zone* 參數，或者也可以依名稱指定該區域。</span><span class="sxs-lookup"><span data-stu-id="79b09-115">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>
<span data-ttu-id="79b09-116">您可以使用 *Confirm* 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="79b09-116">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="79b09-117">如果相符的 **記錄集** 已存在 (相同的名稱和記錄類型) ，您必須指定 *Overwrite* 參數，否則 Cmdlet 不會建立新的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="79b09-117">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="79b09-118">示例</span><span class="sxs-lookup"><span data-stu-id="79b09-118">EXAMPLES</span></span>

### <span data-ttu-id="79b09-119">範例1：建立 A 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="79b09-119">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="79b09-120">這個範例會在區域 myzone.com 中建立名為 www 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="79b09-120">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="79b09-121">記錄集的類型是 A，且每個小時的 TTL (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="79b09-121">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="79b09-122">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="79b09-122">It contains a single DNS record.</span></span>

### <span data-ttu-id="79b09-123">範例2：建立 AAAA 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="79b09-123">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="79b09-124">這個範例會在區域 myzone.com 中建立名為 www 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="79b09-124">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="79b09-125">記錄集的類型是 AAAA，且每個小時的 TTL (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="79b09-125">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="79b09-126">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="79b09-126">It contains a single DNS record.</span></span>
<span data-ttu-id="79b09-127">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="79b09-127">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="79b09-128">範例3：建立 CNAME 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="79b09-128">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="79b09-129">這個範例會在區域 myzone.com 中建立名為 www 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="79b09-129">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="79b09-130">此記錄集的類型為 CNAME，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="79b09-130">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="79b09-131">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="79b09-131">It contains a single DNS record.</span></span>
<span data-ttu-id="79b09-132">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="79b09-132">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="79b09-133">範例4：建立 MX 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="79b09-133">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "mail" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="79b09-134">這個命令會在區域 myzone.com 中建立名為 www 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="79b09-134">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="79b09-135">記錄集的類型是 MX，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="79b09-135">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="79b09-136">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="79b09-136">It contains a single DNS record.</span></span>
<span data-ttu-id="79b09-137">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="79b09-137">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="79b09-138">範例5：建立 NS 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="79b09-138">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="79b09-139">這個命令會在區域 myzone.com 中建立一個名為 ns1 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="79b09-139">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="79b09-140">記錄集的類型是 NS，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="79b09-140">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="79b09-141">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="79b09-141">It contains a single DNS record.</span></span>
<span data-ttu-id="79b09-142">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="79b09-142">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="79b09-143">範例6：建立類型指標的記錄集</span><span class="sxs-lookup"><span data-stu-id="79b09-143">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="79b09-144">這個命令會在 zone 3.2.1.in-arpa 中建立名為4的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="79b09-144">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="79b09-145">記錄集的類型是 PTR，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="79b09-145">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="79b09-146">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="79b09-146">It contains a single DNS record.</span></span>
<span data-ttu-id="79b09-147">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="79b09-147">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="79b09-148">範例7：建立 SRV 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="79b09-148">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="79b09-149">這個命令會在區域 myzone.com 中建立名為 _sip 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="79b09-149">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="79b09-150">記錄集的類型為 SRV，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="79b09-150">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="79b09-151">它包含單一 DNS 記錄，並指向 IP 位址2001.2.3.4。</span><span class="sxs-lookup"><span data-stu-id="79b09-151">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="79b09-152">服務 (sip) ，而 (tcp) 的通訊協定，則會指定為記錄集名稱的一部分，而不是記錄資料的一部分。</span><span class="sxs-lookup"><span data-stu-id="79b09-152">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="79b09-153">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="79b09-153">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="79b09-154">範例8：建立 TXT 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="79b09-154">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="79b09-155">這個命令會在區域 myzone.com 中建立名為 text 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="79b09-155">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="79b09-156">記錄集的類型為 TXT，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="79b09-156">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="79b09-157">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="79b09-157">It contains a single DNS record.</span></span>
<span data-ttu-id="79b09-158">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="79b09-158">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="79b09-159">範例9：在區域 apex 建立記錄集</span><span class="sxs-lookup"><span data-stu-id="79b09-159">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="79b09-160">這個命令會在區域 myzone.com 的 apex (或根) 建立 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="79b09-160">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="79b09-161">若要這樣做，記錄集名稱會指定為 "@" (包括雙引號) 。</span><span class="sxs-lookup"><span data-stu-id="79b09-161">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>
<span data-ttu-id="79b09-162">您無法在區域的 apex 建立 CNAME 記錄。</span><span class="sxs-lookup"><span data-stu-id="79b09-162">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="79b09-163">這是 DNS 標準的限制式;這不是 Azure DNS 的限制。</span><span class="sxs-lookup"><span data-stu-id="79b09-163">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>
<span data-ttu-id="79b09-164">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="79b09-164">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="79b09-165">範例10：建立萬用字元記錄集</span><span class="sxs-lookup"><span data-stu-id="79b09-165">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="79b09-166">這個命令會在區域 myzone.com 中建立一個名為 \* 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="79b09-166">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="79b09-167">這是萬用字元記錄集。</span><span class="sxs-lookup"><span data-stu-id="79b09-167">This is a wildcard record set.</span></span>
<span data-ttu-id="79b09-168">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="79b09-168">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="79b09-169">範例11：建立空白記錄集</span><span class="sxs-lookup"><span data-stu-id="79b09-169">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="79b09-170">這個命令會在區域 myzone.com 中建立名為 www 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="79b09-170">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="79b09-171">記錄集的類型是 A，且每個小時的 TTL (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="79b09-171">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="79b09-172">這是一個空的記錄集，可充當預留位置，您稍後可以在該位置新增記錄。</span><span class="sxs-lookup"><span data-stu-id="79b09-172">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="79b09-173">範例12：建立記錄集並隱含所有確認</span><span class="sxs-lookup"><span data-stu-id="79b09-173">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="79b09-174">這個命令會建立 **記錄集**。</span><span class="sxs-lookup"><span data-stu-id="79b09-174">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="79b09-175">*Overwrite* 參數可確保此記錄集會覆寫具有相同名稱和類型的任何預先存在的記錄集， (該記錄集中現有的記錄會遺失) 。</span><span class="sxs-lookup"><span data-stu-id="79b09-175">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="79b09-176">含 $False 值的 *確認* 參數會抑制確認提示。</span><span class="sxs-lookup"><span data-stu-id="79b09-176">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="79b09-177">參數</span><span class="sxs-lookup"><span data-stu-id="79b09-177">PARAMETERS</span></span>

### <span data-ttu-id="79b09-178">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79b09-178">-DefaultProfile</span></span>
<span data-ttu-id="79b09-179">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="79b09-179">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79b09-180">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="79b09-180">-DnsRecords</span></span>
<span data-ttu-id="79b09-181">指定要包含在記錄集中的 DNS 記錄陣列。</span><span class="sxs-lookup"><span data-stu-id="79b09-181">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="79b09-182">您可以使用 New-AzDnsRecordConfig Cmdlet 來建立 DNS 記錄物件。</span><span class="sxs-lookup"><span data-stu-id="79b09-182">You can use the New-AzDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="79b09-183">如需詳細資訊，請參閱範例。</span><span class="sxs-lookup"><span data-stu-id="79b09-183">See the examples for more information.</span></span>

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

### <span data-ttu-id="79b09-184">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="79b09-184">-Metadata</span></span>
<span data-ttu-id="79b09-185">指定要與記錄集相關聯的中繼資料陣列。</span><span class="sxs-lookup"><span data-stu-id="79b09-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="79b09-186">中繼資料是使用以雜湊資料表表示的名稱值對指定，例如 @ {"部門" = "購物"; "env "=" 生產 "}。</span><span class="sxs-lookup"><span data-stu-id="79b09-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @{"dept"="shopping";"env"="production"}.</span></span>

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

### <span data-ttu-id="79b09-187">-名稱</span><span class="sxs-lookup"><span data-stu-id="79b09-187">-Name</span></span>
<span data-ttu-id="79b09-188">指定要建立的 **記錄集** 的名稱。</span><span class="sxs-lookup"><span data-stu-id="79b09-188">Specifies the name of the **RecordSet** to create.</span></span>

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

### <span data-ttu-id="79b09-189">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="79b09-189">-Overwrite</span></span>
<span data-ttu-id="79b09-190">表示此 Cmdlet 會覆寫指定的 **記錄集** （如果已存在）。</span><span class="sxs-lookup"><span data-stu-id="79b09-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

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

### <span data-ttu-id="79b09-191">-RecordType</span><span class="sxs-lookup"><span data-stu-id="79b09-191">-RecordType</span></span>
<span data-ttu-id="79b09-192">指定要建立的 DNS 記錄類型。</span><span class="sxs-lookup"><span data-stu-id="79b09-192">Specifies the type of DNS record to create.</span></span>
<span data-ttu-id="79b09-193">有效值為：</span><span class="sxs-lookup"><span data-stu-id="79b09-193">Valid values are:</span></span>
- <span data-ttu-id="79b09-194">是</span><span class="sxs-lookup"><span data-stu-id="79b09-194">A</span></span>
- <span data-ttu-id="79b09-195">AAAA</span><span class="sxs-lookup"><span data-stu-id="79b09-195">AAAA</span></span>
- <span data-ttu-id="79b09-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="79b09-196">CNAME</span></span>
- <span data-ttu-id="79b09-197">MX</span><span class="sxs-lookup"><span data-stu-id="79b09-197">MX</span></span>
- <span data-ttu-id="79b09-198">NS</span><span class="sxs-lookup"><span data-stu-id="79b09-198">NS</span></span>
- <span data-ttu-id="79b09-199">PTR</span><span class="sxs-lookup"><span data-stu-id="79b09-199">PTR</span></span>
- <span data-ttu-id="79b09-200">DNS-SRV</span><span class="sxs-lookup"><span data-stu-id="79b09-200">SRV</span></span>
- <span data-ttu-id="79b09-201">TXT SOA 記錄是在建立區域時自動建立，而且不能手動建立。</span><span class="sxs-lookup"><span data-stu-id="79b09-201">TXT SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

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

### <span data-ttu-id="79b09-202">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79b09-202">-ResourceGroupName</span></span>
<span data-ttu-id="79b09-203">指定包含 DNS 區域的資源群組。</span><span class="sxs-lookup"><span data-stu-id="79b09-203">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="79b09-204">您也必須指定 *ZoneName* 參數來指定區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="79b09-204">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>
<span data-ttu-id="79b09-205">或者，您也可以使用 *zone* 參數傳入 DNS 區域物件來指定區域和資源群組。</span><span class="sxs-lookup"><span data-stu-id="79b09-205">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="79b09-206">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="79b09-206">-TargetResourceId</span></span>
<span data-ttu-id="79b09-207">別名目標資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="79b09-207">Alias Target Resource Id.</span></span>

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

### <span data-ttu-id="79b09-208">-Ttl</span><span class="sxs-lookup"><span data-stu-id="79b09-208">-Ttl</span></span>
<span data-ttu-id="79b09-209">指定 DNS 記錄集的實際 (TTL) 時間。</span><span class="sxs-lookup"><span data-stu-id="79b09-209">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

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

### <span data-ttu-id="79b09-210">-Zone</span><span class="sxs-lookup"><span data-stu-id="79b09-210">-Zone</span></span>
<span data-ttu-id="79b09-211">指定要在其中建立 **記錄集** 的 DnsZone。</span><span class="sxs-lookup"><span data-stu-id="79b09-211">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="79b09-212">或者，您也可以使用 *ZoneName* 和 *ResourceGroupName* 參數指定區域。</span><span class="sxs-lookup"><span data-stu-id="79b09-212">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="79b09-213">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="79b09-213">-ZoneName</span></span>
<span data-ttu-id="79b09-214">指定要在其中建立 **記錄集** 的區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="79b09-214">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="79b09-215">您也必須使用 *ResourceGroupName* 參數指定包含該區域的資源群組。</span><span class="sxs-lookup"><span data-stu-id="79b09-215">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="79b09-216">或者，您也可以使用 *zone* 參數傳入 DNS 區域物件來指定區域和資源群組。</span><span class="sxs-lookup"><span data-stu-id="79b09-216">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="79b09-217">-確認</span><span class="sxs-lookup"><span data-stu-id="79b09-217">-Confirm</span></span>
<span data-ttu-id="79b09-218">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="79b09-218">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79b09-219">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79b09-219">-WhatIf</span></span>
<span data-ttu-id="79b09-220">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="79b09-220">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79b09-221">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="79b09-221">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79b09-222">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79b09-222">CommonParameters</span></span>
<span data-ttu-id="79b09-223">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="79b09-223">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79b09-224">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="79b09-224">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79b09-225">輸入</span><span class="sxs-lookup"><span data-stu-id="79b09-225">INPUTS</span></span>

### <span data-ttu-id="79b09-226">System.object</span><span class="sxs-lookup"><span data-stu-id="79b09-226">System.String</span></span>

### <span data-ttu-id="79b09-227">DnsZone （）</span><span class="sxs-lookup"><span data-stu-id="79b09-227">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="79b09-228">UInt32</span><span class="sxs-lookup"><span data-stu-id="79b09-228">System.UInt32</span></span>

### <span data-ttu-id="79b09-229">RecordType 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="79b09-229">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="79b09-230">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="79b09-230">System.Collections.Hashtable</span></span>

### <span data-ttu-id="79b09-231">DnsRecordBase [] （[]）</span><span class="sxs-lookup"><span data-stu-id="79b09-231">Microsoft.Azure.Commands.Dns.DnsRecordBase[]</span></span>

## <span data-ttu-id="79b09-232">輸出</span><span class="sxs-lookup"><span data-stu-id="79b09-232">OUTPUTS</span></span>

### <span data-ttu-id="79b09-233">DnsRecordSet （）</span><span class="sxs-lookup"><span data-stu-id="79b09-233">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="79b09-234">筆記</span><span class="sxs-lookup"><span data-stu-id="79b09-234">NOTES</span></span>
<span data-ttu-id="79b09-235">您可以使用 *Confirm* 參數來控制此 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="79b09-235">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="79b09-236">根據預設，如果 $ConfirmPreference 的 Windows PowerShell 變數的值為 [中] 或 [低]，則該 Cmdlet 會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="79b09-236">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="79b09-237">如果您指定 [ *確認* ] 或 [ *確認]： $True*，此 Cmdlet 會在您執行之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="79b09-237">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="79b09-238">如果您指定 [ *確認： $False*]，則 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="79b09-238">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="79b09-239">相關連結</span><span class="sxs-lookup"><span data-stu-id="79b09-239">RELATED LINKS</span></span>

[<span data-ttu-id="79b09-240">附加 AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="79b09-240">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="79b09-241">AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="79b09-241">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="79b09-242">新-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="79b09-242">New-AzDnsRecordConfig</span></span>](./New-AzDnsRecordConfig.md)

[<span data-ttu-id="79b09-243">移除-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="79b09-243">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="79b09-244">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="79b09-244">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
