---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: ''
schema: 2.0.0
ms.openlocfilehash: ce82a1bae63fafcf0d221d0c2ce6d8e82e8e8e12
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800505"
---
# <span data-ttu-id="24051-101">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="24051-101">New-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="24051-102">摘要</span><span class="sxs-lookup"><span data-stu-id="24051-102">SYNOPSIS</span></span>
<span data-ttu-id="24051-103">建立 DNS 記錄集。</span><span class="sxs-lookup"><span data-stu-id="24051-103">Creates a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24051-104">句法</span><span class="sxs-lookup"><span data-stu-id="24051-104">SYNTAX</span></span>

### <span data-ttu-id="24051-105">區域</span><span class="sxs-lookup"><span data-stu-id="24051-105">Fields</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24051-106">面向</span><span class="sxs-lookup"><span data-stu-id="24051-106">Object</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24051-107">說明</span><span class="sxs-lookup"><span data-stu-id="24051-107">DESCRIPTION</span></span>
<span data-ttu-id="24051-108">**新的 AzureRmDnsRecordSet** Cmdlet 會在指定的區域中使用指定的名稱和類型， (DNS) 記錄集建立新的網域名稱系統。</span><span class="sxs-lookup"><span data-stu-id="24051-108">The **New-AzureRmDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="24051-109">**記錄集** 物件是一組具有相同名稱和類型的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="24051-109">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="24051-110">請注意，該名稱是相對於區域而非完全限定名稱。</span><span class="sxs-lookup"><span data-stu-id="24051-110">Note that the name is relative to the zone and not the fully qualified name.</span></span>

<span data-ttu-id="24051-111">*DnsRecords* 參數會指定記錄集中的記錄。</span><span class="sxs-lookup"><span data-stu-id="24051-111">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="24051-112">這個參數會採用一個 DNS 記錄陣列，並使用新的 AzureRmDnsRecordConfig 來構造。</span><span class="sxs-lookup"><span data-stu-id="24051-112">This parameter takes an array of DNS records, constructed using New-AzureRmDnsRecordConfig.</span></span>

<span data-ttu-id="24051-113">您可以使用管線運算子，將 **DnsZone** 物件傳遞到這個 Cmdlet，或者您可以將 **DnsZone** 物件傳遞為 *zone* 參數，或者也可以依名稱指定該區域。</span><span class="sxs-lookup"><span data-stu-id="24051-113">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>

<span data-ttu-id="24051-114">您可以使用 *Confirm* 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="24051-114">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="24051-115">如果相符的 **記錄集** 已存在 (相同的名稱和記錄類型) ，您必須指定 *Overwrite* 參數，否則 Cmdlet 不會建立新的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="24051-115">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="24051-116">示例</span><span class="sxs-lookup"><span data-stu-id="24051-116">EXAMPLES</span></span>

### <span data-ttu-id="24051-117">範例1：建立 A 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="24051-117">Example 1: Create a RecordSet of type A</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzureRmDnsRecordConfig to add each record to the $Records array,
# then call New-AzureRmDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="24051-118">這個範例會在區域 myzone.com 中建立名為 www 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="24051-118">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="24051-119">記錄集的類型是 A，且每個小時的 TTL (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="24051-119">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="24051-120">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="24051-120">It contains a single DNS record.</span></span>

### <span data-ttu-id="24051-121">範例2：建立 AAAA 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="24051-121">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="24051-122">這個範例會在區域 myzone.com 中建立名為 www 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="24051-122">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="24051-123">記錄集的類型是 AAAA，且每個小時的 TTL (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="24051-123">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="24051-124">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="24051-124">It contains a single DNS record.</span></span>

<span data-ttu-id="24051-125">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="24051-125">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="24051-126">範例3：建立 CNAME 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="24051-126">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="24051-127">這個範例會在區域 myzone.com 中建立名為 www 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="24051-127">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="24051-128">此記錄集的類型為 CNAME，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="24051-128">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="24051-129">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="24051-129">It contains a single DNS record.</span></span>

<span data-ttu-id="24051-130">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="24051-130">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="24051-131">範例4：建立 MX 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="24051-131">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="24051-132">這個命令會在區域 myzone.com 中建立名為 www 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="24051-132">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="24051-133">記錄集的類型是 MX，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="24051-133">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="24051-134">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="24051-134">It contains a single DNS record.</span></span>

<span data-ttu-id="24051-135">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="24051-135">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="24051-136">範例5：建立 NS 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="24051-136">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="24051-137">這個命令會在區域 myzone.com 中建立一個名為 ns1 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="24051-137">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="24051-138">記錄集的類型是 NS，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="24051-138">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="24051-139">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="24051-139">It contains a single DNS record.</span></span>

<span data-ttu-id="24051-140">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="24051-140">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="24051-141">範例6：建立類型指標的記錄集</span><span class="sxs-lookup"><span data-stu-id="24051-141">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="24051-142">這個命令會在 zone 3.2.1.in-arpa 中建立名為4的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="24051-142">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="24051-143">記錄集的類型是 PTR，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="24051-143">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="24051-144">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="24051-144">It contains a single DNS record.</span></span>

<span data-ttu-id="24051-145">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="24051-145">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="24051-146">範例7：建立 SRV 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="24051-146">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="24051-147">這個命令會在區域 myzone.com 中建立名為 _sip 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="24051-147">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="24051-148">記錄集的類型為 SRV，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="24051-148">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="24051-149">它包含單一 DNS 記錄，並指向 IP 位址2001.2.3.4。</span><span class="sxs-lookup"><span data-stu-id="24051-149">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>

<span data-ttu-id="24051-150">服務 (sip) ，而 (tcp) 的通訊協定，則會指定為記錄集名稱的一部分，而不是記錄資料的一部分。</span><span class="sxs-lookup"><span data-stu-id="24051-150">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>

<span data-ttu-id="24051-151">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="24051-151">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="24051-152">範例8：建立 TXT 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="24051-152">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="24051-153">這個命令會在區域 myzone.com 中建立名為 text 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="24051-153">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="24051-154">記錄集的類型為 TXT，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="24051-154">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="24051-155">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="24051-155">It contains a single DNS record.</span></span>

<span data-ttu-id="24051-156">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="24051-156">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="24051-157">範例9：在區域 apex 建立記錄集</span><span class="sxs-lookup"><span data-stu-id="24051-157">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="24051-158">這個命令會在區域 myzone.com 的 apex (或根) 建立 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="24051-158">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="24051-159">若要這樣做，記錄集名稱會指定為 "@" (包括雙引號) 。</span><span class="sxs-lookup"><span data-stu-id="24051-159">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>

<span data-ttu-id="24051-160">您無法在區域的 apex 建立 CNAME 記錄。</span><span class="sxs-lookup"><span data-stu-id="24051-160">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="24051-161">這是 DNS 標準的限制式;這不是 Azure DNS 的限制。</span><span class="sxs-lookup"><span data-stu-id="24051-161">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>

<span data-ttu-id="24051-162">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="24051-162">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="24051-163">範例10：建立萬用字元記錄集</span><span class="sxs-lookup"><span data-stu-id="24051-163">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="24051-164">這個命令會在區域 myzone.com 中建立一個名為 \* 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="24051-164">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="24051-165">這是萬用字元記錄集。</span><span class="sxs-lookup"><span data-stu-id="24051-165">This is a wildcard record set.</span></span>

<span data-ttu-id="24051-166">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="24051-166">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="24051-167">範例11：建立空白記錄集</span><span class="sxs-lookup"><span data-stu-id="24051-167">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="24051-168">這個命令會在區域 myzone.com 中建立名為 www 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="24051-168">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="24051-169">記錄集的類型是 A，且每個小時的 TTL (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="24051-169">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="24051-170">這是一個空的記錄集，可充當預留位置，您稍後可以在該位置新增記錄。</span><span class="sxs-lookup"><span data-stu-id="24051-170">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="24051-171">範例12：建立記錄集並隱含所有確認</span><span class="sxs-lookup"><span data-stu-id="24051-171">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="24051-172">這個命令會建立 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="24051-172">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="24051-173">*Overwrite* 參數可確保此記錄集會覆寫具有相同名稱和類型的任何預先存在的記錄集， (該記錄集中現有的記錄會遺失) 。</span><span class="sxs-lookup"><span data-stu-id="24051-173">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="24051-174">含 $False 值的 *確認* 參數會抑制確認提示。</span><span class="sxs-lookup"><span data-stu-id="24051-174">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="24051-175">參數</span><span class="sxs-lookup"><span data-stu-id="24051-175">PARAMETERS</span></span>

### <span data-ttu-id="24051-176">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="24051-176">-DnsRecords</span></span>
<span data-ttu-id="24051-177">指定要包含在記錄集中的 DNS 記錄陣列。</span><span class="sxs-lookup"><span data-stu-id="24051-177">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="24051-178">您可以使用 New-AzureRmDnsRecordConfig Cmdlet 來建立 DNS 記錄物件。</span><span class="sxs-lookup"><span data-stu-id="24051-178">You can use the New-AzureRmDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="24051-179">如需詳細資訊，請參閱範例。</span><span class="sxs-lookup"><span data-stu-id="24051-179">See the examples for more information.</span></span>

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

### <span data-ttu-id="24051-180">-Force</span><span class="sxs-lookup"><span data-stu-id="24051-180">-Force</span></span>
<span data-ttu-id="24051-181">此 Cmdlet 已棄用此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24051-181">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="24051-182">在未來版本中將會移除它。</span><span class="sxs-lookup"><span data-stu-id="24051-182">It will be removed in a future release.</span></span>

<span data-ttu-id="24051-183">若要控制此 Cmdlet 是否提示您 comfirmation，請使用 *Confirm* 參數。</span><span class="sxs-lookup"><span data-stu-id="24051-183">To control whether this cmdlet prompts you for comfirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="24051-184">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="24051-184">-Metadata</span></span>
<span data-ttu-id="24051-185">指定要與記錄集相關聯的中繼資料陣列。</span><span class="sxs-lookup"><span data-stu-id="24051-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="24051-186">中繼資料是使用以雜湊資料表表示的名稱值對指定，例如 @ ( @ {"Name" = "部門";"值" = "購物"}，@ {"Name" = "env";"Value" = "生產"} ) 。</span><span class="sxs-lookup"><span data-stu-id="24051-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @(@{"Name"="dept"; "Value"="shopping"}, @{"Name"="env"; "Value"="production"}).</span></span>

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

### <span data-ttu-id="24051-187">-名稱</span><span class="sxs-lookup"><span data-stu-id="24051-187">-Name</span></span>
<span data-ttu-id="24051-188">指定要建立的 **記錄集** 的名稱。</span><span class="sxs-lookup"><span data-stu-id="24051-188">Specifies the name of the **RecordSet** to create.</span></span>

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

### <span data-ttu-id="24051-189">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="24051-189">-Overwrite</span></span>
<span data-ttu-id="24051-190">表示此 Cmdlet 會覆寫指定的 **記錄集** （如果已存在）。</span><span class="sxs-lookup"><span data-stu-id="24051-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

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

### <span data-ttu-id="24051-191">-RecordType</span><span class="sxs-lookup"><span data-stu-id="24051-191">-RecordType</span></span>
<span data-ttu-id="24051-192">指定要建立的 DNS 記錄類型。</span><span class="sxs-lookup"><span data-stu-id="24051-192">Specifies the type of DNS record to create.</span></span>

<span data-ttu-id="24051-193">有效值為：</span><span class="sxs-lookup"><span data-stu-id="24051-193">Valid values are:</span></span>

- <span data-ttu-id="24051-194">是</span><span class="sxs-lookup"><span data-stu-id="24051-194">A</span></span>
- <span data-ttu-id="24051-195">AAAA</span><span class="sxs-lookup"><span data-stu-id="24051-195">AAAA</span></span>
- <span data-ttu-id="24051-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="24051-196">CNAME</span></span>
- <span data-ttu-id="24051-197">MX</span><span class="sxs-lookup"><span data-stu-id="24051-197">MX</span></span>
- <span data-ttu-id="24051-198">NS</span><span class="sxs-lookup"><span data-stu-id="24051-198">NS</span></span>
- <span data-ttu-id="24051-199">PTR</span><span class="sxs-lookup"><span data-stu-id="24051-199">PTR</span></span>
- <span data-ttu-id="24051-200">DNS-SRV</span><span class="sxs-lookup"><span data-stu-id="24051-200">SRV</span></span>
- <span data-ttu-id="24051-201">文字檔</span><span class="sxs-lookup"><span data-stu-id="24051-201">TXT</span></span>

<span data-ttu-id="24051-202">在建立區域時，系統會自動建立 SOA 記錄，而且不能手動建立。</span><span class="sxs-lookup"><span data-stu-id="24051-202">SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

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

### <span data-ttu-id="24051-203">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24051-203">-ResourceGroupName</span></span>
<span data-ttu-id="24051-204">指定包含 DNS 區域的資源群組。</span><span class="sxs-lookup"><span data-stu-id="24051-204">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="24051-205">您也必須指定 *ZoneName* 參數來指定區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="24051-205">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>

<span data-ttu-id="24051-206">或者，您也可以使用 *zone* 參數傳入 DNS 區域物件來指定區域和資源群組。</span><span class="sxs-lookup"><span data-stu-id="24051-206">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="24051-207">-Ttl</span><span class="sxs-lookup"><span data-stu-id="24051-207">-Ttl</span></span>
<span data-ttu-id="24051-208">指定 DNS 記錄集的實際 (TTL) 時間。</span><span class="sxs-lookup"><span data-stu-id="24051-208">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

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

### <span data-ttu-id="24051-209">-Zone</span><span class="sxs-lookup"><span data-stu-id="24051-209">-Zone</span></span>
<span data-ttu-id="24051-210">指定要在其中建立 **記錄集** 的 DnsZone。</span><span class="sxs-lookup"><span data-stu-id="24051-210">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="24051-211">或者，您也可以使用 *ZoneName* 和 *ResourceGroupName* 參數指定區域。</span><span class="sxs-lookup"><span data-stu-id="24051-211">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="24051-212">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="24051-212">-ZoneName</span></span>
<span data-ttu-id="24051-213">指定要在其中建立 **記錄集** 的區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="24051-213">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="24051-214">您也必須使用 *ResourceGroupName* 參數指定包含該區域的資源群組。</span><span class="sxs-lookup"><span data-stu-id="24051-214">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="24051-215">或者，您也可以使用 *zone* 參數傳入 DNS 區域物件來指定區域和資源群組。</span><span class="sxs-lookup"><span data-stu-id="24051-215">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="24051-216">-確認</span><span class="sxs-lookup"><span data-stu-id="24051-216">-Confirm</span></span>
<span data-ttu-id="24051-217">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="24051-217">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24051-218">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24051-218">-WhatIf</span></span>
<span data-ttu-id="24051-219">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="24051-219">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24051-220">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24051-220">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24051-221">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24051-221">CommonParameters</span></span>
<span data-ttu-id="24051-222">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="24051-222">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24051-223">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="24051-223">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24051-224">輸入</span><span class="sxs-lookup"><span data-stu-id="24051-224">INPUTS</span></span>

### <span data-ttu-id="24051-225">DnsZone （）</span><span class="sxs-lookup"><span data-stu-id="24051-225">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="24051-226">您可以將 DnsZone 物件輸送到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24051-226">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="24051-227">輸出</span><span class="sxs-lookup"><span data-stu-id="24051-227">OUTPUTS</span></span>

### <span data-ttu-id="24051-228">DnsRecordSet （）</span><span class="sxs-lookup"><span data-stu-id="24051-228">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="24051-229">這個 Cmdlet 會傳回 **RecordSet** 物件。</span><span class="sxs-lookup"><span data-stu-id="24051-229">This cmdlet returns a **RecordSet** object.</span></span>

## <span data-ttu-id="24051-230">筆記</span><span class="sxs-lookup"><span data-stu-id="24051-230">NOTES</span></span>
<span data-ttu-id="24051-231">您可以使用 *Confirm* 參數來控制此 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="24051-231">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="24051-232">根據預設，如果 $ConfirmPreference 的 Windows PowerShell 變數的值為 [中] 或 [低]，則該 Cmdlet 會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="24051-232">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="24051-233">如果您指定 [ *確認* ] 或 [ *確認]： $True* ，此 Cmdlet 會在您執行之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="24051-233">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="24051-234">如果您指定 [ *確認： $False* ]，則 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="24051-234">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="24051-235">相關連結</span><span class="sxs-lookup"><span data-stu-id="24051-235">RELATED LINKS</span></span>

[<span data-ttu-id="24051-236">附加 AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="24051-236">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="24051-237">AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="24051-237">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="24051-238">新-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="24051-238">New-AzureRmDnsRecordConfig</span></span>](./New-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="24051-239">移除-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="24051-239">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)

[<span data-ttu-id="24051-240">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="24051-240">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
