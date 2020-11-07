---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsRecordConfig.md
ms.openlocfilehash: 0bc25aecae445ba18634df578de590f514640c07
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795662"
---
# <span data-ttu-id="24722-101">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="24722-101">New-AzDnsRecordConfig</span></span>

## <span data-ttu-id="24722-102">摘要</span><span class="sxs-lookup"><span data-stu-id="24722-102">SYNOPSIS</span></span>
<span data-ttu-id="24722-103">建立新的 DNS 記錄本機物件。</span><span class="sxs-lookup"><span data-stu-id="24722-103">Creates a new DNS record local object.</span></span>

## <span data-ttu-id="24722-104">句法</span><span class="sxs-lookup"><span data-stu-id="24722-104">SYNTAX</span></span>

### <span data-ttu-id="24722-105">是</span><span class="sxs-lookup"><span data-stu-id="24722-105">A</span></span>
```
New-AzDnsRecordConfig -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="24722-106">Aaaa</span><span class="sxs-lookup"><span data-stu-id="24722-106">Aaaa</span></span>
```
New-AzDnsRecordConfig -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="24722-107">Ns</span><span class="sxs-lookup"><span data-stu-id="24722-107">Ns</span></span>
```
New-AzDnsRecordConfig -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="24722-108">Mx</span><span class="sxs-lookup"><span data-stu-id="24722-108">Mx</span></span>
```
New-AzDnsRecordConfig -Exchange <String> -Preference <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="24722-109">Ptr</span><span class="sxs-lookup"><span data-stu-id="24722-109">Ptr</span></span>
```
New-AzDnsRecordConfig -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="24722-110">文字檔</span><span class="sxs-lookup"><span data-stu-id="24722-110">Txt</span></span>
```
New-AzDnsRecordConfig -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="24722-111">Dns-srv</span><span class="sxs-lookup"><span data-stu-id="24722-111">Srv</span></span>
```
New-AzDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="24722-112">CName</span><span class="sxs-lookup"><span data-stu-id="24722-112">CName</span></span>
```
New-AzDnsRecordConfig -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="24722-113">說明</span><span class="sxs-lookup"><span data-stu-id="24722-113">DESCRIPTION</span></span>
<span data-ttu-id="24722-114">**新的-AzDnsRecordConfig** Cmdlet 會建立本機 **DnsRecord** 物件。</span><span class="sxs-lookup"><span data-stu-id="24722-114">The **New-AzDnsRecordConfig** cmdlet creates a local **DnsRecord** object.</span></span>
<span data-ttu-id="24722-115">這些物件的陣列會使用 *DnsRecords* 參數傳遞到 New-AzDnsRecordSet Cmdlet，以指定要在記錄集中建立的記錄。</span><span class="sxs-lookup"><span data-stu-id="24722-115">An array of these objects is passed to the New-AzDnsRecordSet cmdlet using the *DnsRecords* parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="24722-116">示例</span><span class="sxs-lookup"><span data-stu-id="24722-116">EXAMPLES</span></span>

### <span data-ttu-id="24722-117">範例1：建立 A 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="24722-117">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="24722-118">這個範例會在區域 myzone.com 中建立名為 www 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="24722-118">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="24722-119">記錄集的類型是 A，且每個小時的 TTL (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="24722-119">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="24722-120">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="24722-120">It contains a single DNS record.</span></span>

### <span data-ttu-id="24722-121">範例2：建立 AAAA 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="24722-121">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="24722-122">這個範例會在區域 myzone.com 中建立名為 www 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="24722-122">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="24722-123">記錄集的類型是 AAAA，且每個小時的 TTL (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="24722-123">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="24722-124">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="24722-124">It contains a single DNS record.</span></span>

<span data-ttu-id="24722-125">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="24722-125">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="24722-126">範例3：建立 CNAME 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="24722-126">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="24722-127">這個範例會在區域 myzone.com 中建立名為 www 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="24722-127">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="24722-128">此記錄集的類型為 CNAME，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="24722-128">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="24722-129">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="24722-129">It contains a single DNS record.</span></span>

<span data-ttu-id="24722-130">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="24722-130">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="24722-131">範例4：建立 MX 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="24722-131">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="24722-132">這個命令會在區域 myzone.com 中建立名為 www 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="24722-132">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="24722-133">記錄集的類型是 MX，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="24722-133">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="24722-134">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="24722-134">It contains a single DNS record.</span></span>

<span data-ttu-id="24722-135">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="24722-135">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="24722-136">範例5：建立 NS 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="24722-136">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="24722-137">這個命令會在區域 myzone.com 中建立一個名為 ns1 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="24722-137">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="24722-138">記錄集的類型是 NS，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="24722-138">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="24722-139">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="24722-139">It contains a single DNS record.</span></span>

<span data-ttu-id="24722-140">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="24722-140">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="24722-141">範例6：建立類型指標的記錄集</span><span class="sxs-lookup"><span data-stu-id="24722-141">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="24722-142">這個命令會在 zone 3.2.1.in-arpa 中建立名為4的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="24722-142">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="24722-143">記錄集的類型是 PTR，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="24722-143">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="24722-144">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="24722-144">It contains a single DNS record.</span></span>

<span data-ttu-id="24722-145">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="24722-145">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="24722-146">範例7：建立 SRV 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="24722-146">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="24722-147">這個命令會在區域 myzone.com 中建立名為 _sip 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="24722-147">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="24722-148">記錄集的類型為 SRV，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="24722-148">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="24722-149">它包含單一 DNS 記錄，並指向 IP 位址2001.2.3.4。</span><span class="sxs-lookup"><span data-stu-id="24722-149">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>

<span data-ttu-id="24722-150">服務 (sip) ，而 (tcp) 的通訊協定，則會指定為記錄集名稱的一部分，而不是記錄資料的一部分。</span><span class="sxs-lookup"><span data-stu-id="24722-150">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>

<span data-ttu-id="24722-151">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="24722-151">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="24722-152">範例8：建立 TXT 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="24722-152">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="24722-153">這個命令會在區域 myzone.com 中建立名為 text 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="24722-153">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="24722-154">記錄集的類型為 TXT，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="24722-154">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="24722-155">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="24722-155">It contains a single DNS record.</span></span>

<span data-ttu-id="24722-156">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="24722-156">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="24722-157">參數</span><span class="sxs-lookup"><span data-stu-id="24722-157">PARAMETERS</span></span>

### <span data-ttu-id="24722-158">-Cname</span><span class="sxs-lookup"><span data-stu-id="24722-158">-Cname</span></span>
<span data-ttu-id="24722-159">指定正常化) 記錄 (CNAME 名稱的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="24722-159">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: String
Parameter Sets: CName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24722-160">-Exchange</span><span class="sxs-lookup"><span data-stu-id="24722-160">-Exchange</span></span>
<span data-ttu-id="24722-161">指定郵件交換 (MX) 記錄的郵件交換伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="24722-161">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: String
Parameter Sets: Mx
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24722-162">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="24722-162">-Ipv4Address</span></span>
<span data-ttu-id="24722-163">指定 A 記錄的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="24722-163">Specifies an IPv4 address for an A record.</span></span>

```yaml
Type: String
Parameter Sets: A
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24722-164">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="24722-164">-Ipv6Address</span></span>
<span data-ttu-id="24722-165">指定 AAAA 記錄的 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="24722-165">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: String
Parameter Sets: Aaaa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24722-166">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="24722-166">-Nsdname</span></span>
<span data-ttu-id="24722-167">指定 name server (NS) 記錄的名稱伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="24722-167">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: String
Parameter Sets: Ns
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24722-168">-埠</span><span class="sxs-lookup"><span data-stu-id="24722-168">-Port</span></span>
<span data-ttu-id="24722-169">指定服務 (SRV) 記錄的埠。</span><span class="sxs-lookup"><span data-stu-id="24722-169">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24722-170">-喜好設定</span><span class="sxs-lookup"><span data-stu-id="24722-170">-Preference</span></span>
<span data-ttu-id="24722-171">指定 MX 記錄的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="24722-171">Specifies the preference for an MX record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Mx
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24722-172">-優先順序</span><span class="sxs-lookup"><span data-stu-id="24722-172">-Priority</span></span>
<span data-ttu-id="24722-173">指定 SRV 記錄的優先順序。</span><span class="sxs-lookup"><span data-stu-id="24722-173">Specifies the priority for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24722-174">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="24722-174">-Ptrdname</span></span>
<span data-ttu-id="24722-175">指定指標資源的目標功能變數名稱 (PTR) 記錄。</span><span class="sxs-lookup"><span data-stu-id="24722-175">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: String
Parameter Sets: Ptr
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24722-176">-目標</span><span class="sxs-lookup"><span data-stu-id="24722-176">-Target</span></span>
<span data-ttu-id="24722-177">指定 SRV 記錄的目標。</span><span class="sxs-lookup"><span data-stu-id="24722-177">Specifies the target for an SRV record.</span></span>

```yaml
Type: String
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24722-178">-值</span><span class="sxs-lookup"><span data-stu-id="24722-178">-Value</span></span>
<span data-ttu-id="24722-179">指定 TXT 記錄的值。</span><span class="sxs-lookup"><span data-stu-id="24722-179">Specifies the value for a TXT record.</span></span>

```yaml
Type: String
Parameter Sets: Txt
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24722-180">寬度</span><span class="sxs-lookup"><span data-stu-id="24722-180">-Weight</span></span>
<span data-ttu-id="24722-181">指定 SRV 記錄的權重。</span><span class="sxs-lookup"><span data-stu-id="24722-181">Specifies the weight for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24722-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24722-182">CommonParameters</span></span>
<span data-ttu-id="24722-183">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="24722-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24722-184">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="24722-184">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24722-185">輸入</span><span class="sxs-lookup"><span data-stu-id="24722-185">INPUTS</span></span>

### <span data-ttu-id="24722-186">所有.</span><span class="sxs-lookup"><span data-stu-id="24722-186">None.</span></span>

## <span data-ttu-id="24722-187">輸出</span><span class="sxs-lookup"><span data-stu-id="24722-187">OUTPUTS</span></span>

### <span data-ttu-id="24722-188">DnsRecordBase （）</span><span class="sxs-lookup"><span data-stu-id="24722-188">Microsoft.Azure.Commands.Dns.DnsRecordBase</span></span>

## <span data-ttu-id="24722-189">筆記</span><span class="sxs-lookup"><span data-stu-id="24722-189">NOTES</span></span>

## <span data-ttu-id="24722-190">相關連結</span><span class="sxs-lookup"><span data-stu-id="24722-190">RELATED LINKS</span></span>

[<span data-ttu-id="24722-191">附加 AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="24722-191">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="24722-192">新-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="24722-192">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="24722-193">移除-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="24722-193">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)
