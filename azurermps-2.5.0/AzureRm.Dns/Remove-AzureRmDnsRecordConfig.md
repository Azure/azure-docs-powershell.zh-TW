---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4b0e8642feb208c9ed7ab0a91a31ebe7bd0f7cf8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801670"
---
# <span data-ttu-id="a430c-101">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="a430c-101">Remove-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="a430c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a430c-102">SYNOPSIS</span></span>
<span data-ttu-id="a430c-103">從本機記錄集物件中移除 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="a430c-103">Removes a DNS record from a local record set object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a430c-104">句法</span><span class="sxs-lookup"><span data-stu-id="a430c-104">SYNTAX</span></span>

### <span data-ttu-id="a430c-105">是</span><span class="sxs-lookup"><span data-stu-id="a430c-105">A</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="a430c-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="a430c-106">AAAA</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="a430c-107">NS</span><span class="sxs-lookup"><span data-stu-id="a430c-107">NS</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="a430c-108">MX</span><span class="sxs-lookup"><span data-stu-id="a430c-108">MX</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="a430c-109">PTR</span><span class="sxs-lookup"><span data-stu-id="a430c-109">PTR</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="a430c-110">文字檔</span><span class="sxs-lookup"><span data-stu-id="a430c-110">TXT</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="a430c-111">DNS-SRV</span><span class="sxs-lookup"><span data-stu-id="a430c-111">SRV</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="a430c-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="a430c-112">CNAME</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="a430c-113">說明</span><span class="sxs-lookup"><span data-stu-id="a430c-113">DESCRIPTION</span></span>
<span data-ttu-id="a430c-114">**AzureRmDnsRecordConfig** Cmdlet 會從記錄集中移除 (DNS) 記錄的網域名稱系統。</span><span class="sxs-lookup"><span data-stu-id="a430c-114">The **Remove-AzureRmDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="a430c-115">**RecordSet** 物件是離線物件，而且在您執行 Set-AzureRmDnsRecordSet Cmdlet 以保留 MICROSOFT Azure DNS 服務的變更之後，才能變更 DNS 回應。</span><span class="sxs-lookup"><span data-stu-id="a430c-115">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="a430c-116">若要移除記錄，該記錄類型的所有欄位都必須完全相符。</span><span class="sxs-lookup"><span data-stu-id="a430c-116">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="a430c-117">您無法新增或移除 SOA 記錄。</span><span class="sxs-lookup"><span data-stu-id="a430c-117">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="a430c-118">SOA 記錄會在建立 DNS 區域時自動建立，並在 DNS 區域刪除時自動刪除。</span><span class="sxs-lookup"><span data-stu-id="a430c-118">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>

<span data-ttu-id="a430c-119">您可以將 **RecordSet** 物件作為參數傳遞給這個 Cmdlet，或使用管線運算子。</span><span class="sxs-lookup"><span data-stu-id="a430c-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="a430c-120">示例</span><span class="sxs-lookup"><span data-stu-id="a430c-120">EXAMPLES</span></span>

### <span data-ttu-id="a430c-121">範例1：從記錄集中移除 A 記錄</span><span class="sxs-lookup"><span data-stu-id="a430c-121">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="a430c-122">這個範例會從現有的記錄集中移除 A 記錄。</span><span class="sxs-lookup"><span data-stu-id="a430c-122">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="a430c-123">如果這是記錄集中的唯一記錄，結果就會是一個空的記錄集。</span><span class="sxs-lookup"><span data-stu-id="a430c-123">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="a430c-124">若要完全移除記錄集，請參閱移除-AzureRmDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="a430c-124">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="a430c-125">範例2：從記錄集中移除 AAAA 記錄</span><span class="sxs-lookup"><span data-stu-id="a430c-125">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="a430c-126">這個範例會從現有的記錄集中移除 AAAA 記錄。</span><span class="sxs-lookup"><span data-stu-id="a430c-126">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="a430c-127">如果這是記錄集中的唯一記錄，結果就會是一個空的記錄集。</span><span class="sxs-lookup"><span data-stu-id="a430c-127">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="a430c-128">若要完全移除記錄集，請參閱移除-AzureRmDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="a430c-128">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="a430c-129">範例3：從記錄集中移除 CNAME 記錄</span><span class="sxs-lookup"><span data-stu-id="a430c-129">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Cname contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="a430c-130">這個範例會從現有的記錄集中移除 CNAME 記錄。</span><span class="sxs-lookup"><span data-stu-id="a430c-130">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="a430c-131">因為 CNAME 記錄集最多可以包含一筆記錄，所以結果是一個空的記錄集。</span><span class="sxs-lookup"><span data-stu-id="a430c-131">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="a430c-132">範例4：從記錄集中移除 MX 記錄</span><span class="sxs-lookup"><span data-stu-id="a430c-132">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="a430c-133">這個範例會從現有的記錄集中移除 MX 記錄。</span><span class="sxs-lookup"><span data-stu-id="a430c-133">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="a430c-134">記錄名稱 "@" 代表在區域 apex 上設定的記錄。</span><span class="sxs-lookup"><span data-stu-id="a430c-134">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="a430c-135">如果這是記錄集中的唯一記錄，則結果是一個空的記錄集。</span><span class="sxs-lookup"><span data-stu-id="a430c-135">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="a430c-136">若要完全移除記錄集，請參閱移除-AzureRmDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="a430c-136">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="a430c-137">範例5：從記錄集中移除 NS 記錄</span><span class="sxs-lookup"><span data-stu-id="a430c-137">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="a430c-138">這個範例會從現有的記錄集中移除 NS 記錄。</span><span class="sxs-lookup"><span data-stu-id="a430c-138">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="a430c-139">如果這是記錄集中的唯一記錄，則結果是一個空的記錄集。</span><span class="sxs-lookup"><span data-stu-id="a430c-139">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="a430c-140">若要完全移除記錄集，請參閱移除-AzureRmDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="a430c-140">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="a430c-141">範例6：從記錄集中移除 PTR 記錄</span><span class="sxs-lookup"><span data-stu-id="a430c-141">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzureRmDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzureRmDnsRecordConfig -Ptrdname www.contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="a430c-142">這個範例會從現有的記錄集中移除 PTR 記錄。</span><span class="sxs-lookup"><span data-stu-id="a430c-142">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="a430c-143">如果這是記錄集中的唯一記錄，則結果是一個空的記錄集。</span><span class="sxs-lookup"><span data-stu-id="a430c-143">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="a430c-144">若要完全移除記錄集，請參閱移除-AzureRmDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="a430c-144">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="a430c-145">範例7：從記錄集中移除 SRV 記錄</span><span class="sxs-lookup"><span data-stu-id="a430c-145">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="a430c-146">這個範例會從現有的記錄集中移除 SRV 記錄。</span><span class="sxs-lookup"><span data-stu-id="a430c-146">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="a430c-147">如果這是記錄集中的唯一記錄，則結果是一個空的記錄集。</span><span class="sxs-lookup"><span data-stu-id="a430c-147">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="a430c-148">若要完全移除記錄集，請參閱移除-AzureRmDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="a430c-148">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="a430c-149">範例8：從記錄集中移除 TXT 記錄</span><span class="sxs-lookup"><span data-stu-id="a430c-149">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Value "This is a TXT Record"  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="a430c-150">這個範例會從現有的記錄集中移除 TXT 記錄。</span><span class="sxs-lookup"><span data-stu-id="a430c-150">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="a430c-151">如果這是記錄集中的唯一記錄，則結果是一個空的記錄集。</span><span class="sxs-lookup"><span data-stu-id="a430c-151">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="a430c-152">若要完全移除記錄集，請參閱移除-AzureRmDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="a430c-152">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

## <span data-ttu-id="a430c-153">參數</span><span class="sxs-lookup"><span data-stu-id="a430c-153">PARAMETERS</span></span>

### <span data-ttu-id="a430c-154">-Cname</span><span class="sxs-lookup"><span data-stu-id="a430c-154">-Cname</span></span>
<span data-ttu-id="a430c-155">指定正常化) 記錄 (CNAME 名稱的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="a430c-155">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: String
Parameter Sets: CNAME
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a430c-156">-Exchange</span><span class="sxs-lookup"><span data-stu-id="a430c-156">-Exchange</span></span>
<span data-ttu-id="a430c-157">指定郵件交換 (MX) 記錄的郵件交換伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="a430c-157">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: String
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a430c-158">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="a430c-158">-Ipv4Address</span></span>
<span data-ttu-id="a430c-159">指定 A 記錄的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="a430c-159">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="a430c-160">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="a430c-160">-Ipv6Address</span></span>
<span data-ttu-id="a430c-161">指定 AAAA 記錄的 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="a430c-161">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: String
Parameter Sets: AAAA
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a430c-162">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="a430c-162">-Nsdname</span></span>
<span data-ttu-id="a430c-163">指定 name server (NS) 記錄的名稱伺服器。</span><span class="sxs-lookup"><span data-stu-id="a430c-163">Specifies the name server for a name server (NS) record.</span></span>

```yaml
Type: String
Parameter Sets: NS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a430c-164">-埠</span><span class="sxs-lookup"><span data-stu-id="a430c-164">-Port</span></span>
<span data-ttu-id="a430c-165">指定服務 (SRV) 記錄的埠。</span><span class="sxs-lookup"><span data-stu-id="a430c-165">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a430c-166">-喜好設定</span><span class="sxs-lookup"><span data-stu-id="a430c-166">-Preference</span></span>
<span data-ttu-id="a430c-167">指定 MX 記錄的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="a430c-167">Specifies the preference for an MX record.</span></span>

```yaml
Type: UInt16
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a430c-168">-優先順序</span><span class="sxs-lookup"><span data-stu-id="a430c-168">-Priority</span></span>
<span data-ttu-id="a430c-169">指定 SRV 記錄的優先順序。</span><span class="sxs-lookup"><span data-stu-id="a430c-169">Specifies the priority for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a430c-170">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="a430c-170">-Ptrdname</span></span>
<span data-ttu-id="a430c-171">指定指標 (PTR) 記錄的目標功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="a430c-171">Specifies the target domain name of a pointer (PTR) record.</span></span>

```yaml
Type: String
Parameter Sets: PTR
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a430c-172">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="a430c-172">-RecordSet</span></span>
<span data-ttu-id="a430c-173">指定包含要移除之記錄的 **記錄集** 物件。</span><span class="sxs-lookup"><span data-stu-id="a430c-173">Specifies the **RecordSet** object that contains the record to remove.</span></span>

```yaml
Type: DnsRecordSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a430c-174">-目標</span><span class="sxs-lookup"><span data-stu-id="a430c-174">-Target</span></span>
<span data-ttu-id="a430c-175">指定 SRV 記錄的目標。</span><span class="sxs-lookup"><span data-stu-id="a430c-175">Specifies the target for an SRV record.</span></span>

```yaml
Type: String
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a430c-176">-值</span><span class="sxs-lookup"><span data-stu-id="a430c-176">-Value</span></span>
<span data-ttu-id="a430c-177">指定 TXT 記錄的值。</span><span class="sxs-lookup"><span data-stu-id="a430c-177">Specifies the value for a TXT record.</span></span>

```yaml
Type: String
Parameter Sets: TXT
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a430c-178">寬度</span><span class="sxs-lookup"><span data-stu-id="a430c-178">-Weight</span></span>
<span data-ttu-id="a430c-179">指定 SRV 記錄的權重。</span><span class="sxs-lookup"><span data-stu-id="a430c-179">Specifies the weight for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a430c-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a430c-180">CommonParameters</span></span>
<span data-ttu-id="a430c-181">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a430c-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a430c-182">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a430c-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a430c-183">輸入</span><span class="sxs-lookup"><span data-stu-id="a430c-183">INPUTS</span></span>

### <span data-ttu-id="a430c-184">DnsRecordSet （）</span><span class="sxs-lookup"><span data-stu-id="a430c-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="a430c-185">您可以將 **DnsRecordSet** 物件輸送到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a430c-185">You can pipe a **DnsRecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="a430c-186">這是記錄集的離線標記法，在您執行 AzureRmDnsRecordSet 之後，不會變更 DNS 回應。</span><span class="sxs-lookup"><span data-stu-id="a430c-186">This is an offline representation of the record set and updates to it do not change DNS responses until after you run Set-AzureRmDnsRecordSet.</span></span>

## <span data-ttu-id="a430c-187">輸出</span><span class="sxs-lookup"><span data-stu-id="a430c-187">OUTPUTS</span></span>

### <span data-ttu-id="a430c-188">DnsRecordSet （）</span><span class="sxs-lookup"><span data-stu-id="a430c-188">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="a430c-189">這個 Cmdlet 會傳回修改過的 **RecordSet** 物件。</span><span class="sxs-lookup"><span data-stu-id="a430c-189">This cmdlet returns the modified **RecordSet** object.</span></span>

## <span data-ttu-id="a430c-190">筆記</span><span class="sxs-lookup"><span data-stu-id="a430c-190">NOTES</span></span>

## <span data-ttu-id="a430c-191">相關連結</span><span class="sxs-lookup"><span data-stu-id="a430c-191">RELATED LINKS</span></span>

[<span data-ttu-id="a430c-192">附加 AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="a430c-192">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="a430c-193">AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a430c-193">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="a430c-194">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a430c-194">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
