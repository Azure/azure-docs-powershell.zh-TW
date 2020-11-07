---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f2ba0cb03b4819c444f43a59f5556cf2ec8c17a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800510"
---
# <span data-ttu-id="749ee-101">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="749ee-101">Add-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="749ee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="749ee-102">SYNOPSIS</span></span>
<span data-ttu-id="749ee-103">將 DNS 記錄新增到本機記錄集物件。</span><span class="sxs-lookup"><span data-stu-id="749ee-103">Adds a DNS record to a local record set object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="749ee-104">句法</span><span class="sxs-lookup"><span data-stu-id="749ee-104">SYNTAX</span></span>

### <span data-ttu-id="749ee-105">是</span><span class="sxs-lookup"><span data-stu-id="749ee-105">A</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="749ee-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="749ee-106">AAAA</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="749ee-107">NS</span><span class="sxs-lookup"><span data-stu-id="749ee-107">NS</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="749ee-108">MX</span><span class="sxs-lookup"><span data-stu-id="749ee-108">MX</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="749ee-109">PTR</span><span class="sxs-lookup"><span data-stu-id="749ee-109">PTR</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="749ee-110">文字檔</span><span class="sxs-lookup"><span data-stu-id="749ee-110">TXT</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="749ee-111">DNS-SRV</span><span class="sxs-lookup"><span data-stu-id="749ee-111">SRV</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="749ee-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="749ee-112">CNAME</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="749ee-113">說明</span><span class="sxs-lookup"><span data-stu-id="749ee-113">DESCRIPTION</span></span>
<span data-ttu-id="749ee-114">**AzureRmDnsRecordConfig** Cmdlet 會將網域名稱系統 (DNS) 記錄新增至 **RecordSet** 物件。</span><span class="sxs-lookup"><span data-stu-id="749ee-114">The **Add-AzureRmDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="749ee-115">**RecordSet** 物件是離線物件，而且在您執行 Set-AzureRmDnsRecordSet Cmdlet 以保留 MICROSOFT Azure DNS 服務的變更之後，才能變更 DNS 回應。</span><span class="sxs-lookup"><span data-stu-id="749ee-115">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="749ee-116">SOA 記錄是在建立 DNS 區域時建立，而且會在刪除 DNS 區域時移除。</span><span class="sxs-lookup"><span data-stu-id="749ee-116">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="749ee-117">您無法新增或移除 SOA 記錄，但您可以進行編輯。</span><span class="sxs-lookup"><span data-stu-id="749ee-117">You cannot add or remove SOA records, but you can edit them.</span></span>

<span data-ttu-id="749ee-118">您可以將 **RecordSet** 物件作為參數傳遞給這個 Cmdlet，或使用管線運算子。</span><span class="sxs-lookup"><span data-stu-id="749ee-118">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="749ee-119">示例</span><span class="sxs-lookup"><span data-stu-id="749ee-119">EXAMPLES</span></span>

### <span data-ttu-id="749ee-120">範例1：將 A 記錄新增至記錄集</span><span class="sxs-lookup"><span data-stu-id="749ee-120">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="749ee-121">這個範例會將 A 記錄新增至現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="749ee-121">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="749ee-122">範例2：新增 AAAA 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="749ee-122">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="749ee-123">這個範例會將 AAAA 記錄新增至現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="749ee-123">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="749ee-124">範例3：新增 CNAME 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="749ee-124">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Cname contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="749ee-125">這個範例會在現有的記錄集中加入 CNAME 記錄。</span><span class="sxs-lookup"><span data-stu-id="749ee-125">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="749ee-126">因為 CNAME 記錄集最多可以包含一筆記錄，所以它必須是空記錄集，或必須使用 AzureRmDnsRecordConfig 移除現有的記錄。</span><span class="sxs-lookup"><span data-stu-id="749ee-126">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzureRmDnsRecordConfig.</span></span>

### <span data-ttu-id="749ee-127">範例4：新增 MX 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="749ee-127">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="749ee-128">這個範例會將 MX 記錄新增至現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="749ee-128">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="749ee-129">記錄名稱 "@" 代表在區域 apex 上設定的記錄。</span><span class="sxs-lookup"><span data-stu-id="749ee-129">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="749ee-130">範例5：將 NS 記錄新增至記錄集</span><span class="sxs-lookup"><span data-stu-id="749ee-130">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="749ee-131">這個範例會將 NS 記錄新增至現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="749ee-131">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="749ee-132">範例6：將 PTR 記錄新增至記錄集</span><span class="sxs-lookup"><span data-stu-id="749ee-132">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="749ee-133">這個範例會將 PTR 記錄新增至現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="749ee-133">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="749ee-134">範例7：將 SRV 記錄新增至記錄集</span><span class="sxs-lookup"><span data-stu-id="749ee-134">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="749ee-135">這個範例會將 SRV 記錄新增至現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="749ee-135">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="749ee-136">範例8：新增 TXT 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="749ee-136">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Value "This is a TXT Record" | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="749ee-137">這個範例會將 TXT 記錄新增至現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="749ee-137">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="749ee-138">參數</span><span class="sxs-lookup"><span data-stu-id="749ee-138">PARAMETERS</span></span>

### <span data-ttu-id="749ee-139">-Cname</span><span class="sxs-lookup"><span data-stu-id="749ee-139">-Cname</span></span>
<span data-ttu-id="749ee-140">指定正常化) 記錄 (CNAME 名稱的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="749ee-140">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="749ee-141">-Exchange</span><span class="sxs-lookup"><span data-stu-id="749ee-141">-Exchange</span></span>
<span data-ttu-id="749ee-142">指定郵件交換 (MX) 記錄的郵件交換伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="749ee-142">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="749ee-143">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="749ee-143">-Ipv4Address</span></span>
<span data-ttu-id="749ee-144">指定 A 記錄的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="749ee-144">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="749ee-145">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="749ee-145">-Ipv6Address</span></span>
<span data-ttu-id="749ee-146">指定 AAAA 記錄的 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="749ee-146">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="749ee-147">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="749ee-147">-Nsdname</span></span>
<span data-ttu-id="749ee-148">指定 name server (NS) 記錄的名稱伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="749ee-148">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="749ee-149">-埠</span><span class="sxs-lookup"><span data-stu-id="749ee-149">-Port</span></span>
<span data-ttu-id="749ee-150">指定服務 (SRV) 記錄的埠。</span><span class="sxs-lookup"><span data-stu-id="749ee-150">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="749ee-151">-喜好設定</span><span class="sxs-lookup"><span data-stu-id="749ee-151">-Preference</span></span>
<span data-ttu-id="749ee-152">指定 MX 記錄的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="749ee-152">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="749ee-153">-優先順序</span><span class="sxs-lookup"><span data-stu-id="749ee-153">-Priority</span></span>
<span data-ttu-id="749ee-154">指定 SRV 記錄的優先順序。</span><span class="sxs-lookup"><span data-stu-id="749ee-154">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="749ee-155">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="749ee-155">-Ptrdname</span></span>
<span data-ttu-id="749ee-156">指定指標資源的目標功能變數名稱 (PTR) 記錄。</span><span class="sxs-lookup"><span data-stu-id="749ee-156">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="749ee-157">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="749ee-157">-RecordSet</span></span>
<span data-ttu-id="749ee-158">指定要編輯的 **記錄集** 物件。</span><span class="sxs-lookup"><span data-stu-id="749ee-158">Specifies the **RecordSet** object to edit.</span></span>

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

### <span data-ttu-id="749ee-159">-目標</span><span class="sxs-lookup"><span data-stu-id="749ee-159">-Target</span></span>
<span data-ttu-id="749ee-160">指定 SRV 記錄的目標。</span><span class="sxs-lookup"><span data-stu-id="749ee-160">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="749ee-161">-值</span><span class="sxs-lookup"><span data-stu-id="749ee-161">-Value</span></span>
<span data-ttu-id="749ee-162">指定 TXT 記錄的值。</span><span class="sxs-lookup"><span data-stu-id="749ee-162">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="749ee-163">寬度</span><span class="sxs-lookup"><span data-stu-id="749ee-163">-Weight</span></span>
<span data-ttu-id="749ee-164">指定 SRV 記錄的權重。</span><span class="sxs-lookup"><span data-stu-id="749ee-164">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="749ee-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="749ee-165">CommonParameters</span></span>
<span data-ttu-id="749ee-166">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="749ee-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="749ee-167">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="749ee-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="749ee-168">輸入</span><span class="sxs-lookup"><span data-stu-id="749ee-168">INPUTS</span></span>

### <span data-ttu-id="749ee-169">DnsRecordSet （）</span><span class="sxs-lookup"><span data-stu-id="749ee-169">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="749ee-170">您可以將 **RecordSet** 物件輸送到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="749ee-170">You can pipe a **RecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="749ee-171">這是 **記錄集** 的離線表示形式，在您執行 Set-AzureRmDnsRecordSet Cmdlet 之後，才能變更 DNS 回應。</span><span class="sxs-lookup"><span data-stu-id="749ee-171">This is an offline representation of the **RecordSet** , and changes to it do not change DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet.</span></span>

## <span data-ttu-id="749ee-172">輸出</span><span class="sxs-lookup"><span data-stu-id="749ee-172">OUTPUTS</span></span>

### <span data-ttu-id="749ee-173">DnsRecordSet （）</span><span class="sxs-lookup"><span data-stu-id="749ee-173">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="749ee-174">這個 Cmdlet 會傳回修改過的 **RecordSet** 物件。</span><span class="sxs-lookup"><span data-stu-id="749ee-174">This cmdlet returns the modified **RecordSet** object.</span></span>
<span data-ttu-id="749ee-175">此外，會直接修改傳入的物件。</span><span class="sxs-lookup"><span data-stu-id="749ee-175">In addition, the object passed in is modified directly.</span></span>

## <span data-ttu-id="749ee-176">筆記</span><span class="sxs-lookup"><span data-stu-id="749ee-176">NOTES</span></span>

## <span data-ttu-id="749ee-177">相關連結</span><span class="sxs-lookup"><span data-stu-id="749ee-177">RELATED LINKS</span></span>

[<span data-ttu-id="749ee-178">AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="749ee-178">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="749ee-179">移除-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="749ee-179">Remove-AzureRmDnsRecordConfig</span></span>](./Remove-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="749ee-180">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="749ee-180">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
