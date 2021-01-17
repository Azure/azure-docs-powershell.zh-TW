---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/add-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
ms.openlocfilehash: c9390514ad7680a047ca145c8fe71feda0ab1b51
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435182"
---
# <span data-ttu-id="2701a-101">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="2701a-101">Add-AzDnsRecordConfig</span></span>

## <span data-ttu-id="2701a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2701a-102">SYNOPSIS</span></span>
<span data-ttu-id="2701a-103">將 DNS 記錄新增到本機記錄集物件。</span><span class="sxs-lookup"><span data-stu-id="2701a-103">Adds a DNS record to a local record set object.</span></span>

## <span data-ttu-id="2701a-104">句法</span><span class="sxs-lookup"><span data-stu-id="2701a-104">SYNTAX</span></span>

### <span data-ttu-id="2701a-105">是</span><span class="sxs-lookup"><span data-stu-id="2701a-105">A</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2701a-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="2701a-106">AAAA</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2701a-107">NS</span><span class="sxs-lookup"><span data-stu-id="2701a-107">NS</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2701a-108">MX</span><span class="sxs-lookup"><span data-stu-id="2701a-108">MX</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2701a-109">PTR</span><span class="sxs-lookup"><span data-stu-id="2701a-109">PTR</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2701a-110">文字檔</span><span class="sxs-lookup"><span data-stu-id="2701a-110">TXT</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2701a-111">DNS-SRV</span><span class="sxs-lookup"><span data-stu-id="2701a-111">SRV</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2701a-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="2701a-112">CNAME</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2701a-113">Caa</span><span class="sxs-lookup"><span data-stu-id="2701a-113">Caa</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2701a-114">說明</span><span class="sxs-lookup"><span data-stu-id="2701a-114">DESCRIPTION</span></span>
<span data-ttu-id="2701a-115">**AzDnsRecordConfig** Cmdlet 會將網域名稱系統 (DNS) 記錄新增至 **RecordSet** 物件。</span><span class="sxs-lookup"><span data-stu-id="2701a-115">The **Add-AzDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="2701a-116">**RecordSet** 物件是離線物件，而且在您執行 Set-AzDnsRecordSet Cmdlet 以保留 MICROSOFT Azure DNS 服務的變更之後，才能變更 DNS 回應。</span><span class="sxs-lookup"><span data-stu-id="2701a-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="2701a-117">SOA 記錄是在建立 DNS 區域時建立，而且會在刪除 DNS 區域時移除。</span><span class="sxs-lookup"><span data-stu-id="2701a-117">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="2701a-118">您無法新增或移除 SOA 記錄，但您可以進行編輯。</span><span class="sxs-lookup"><span data-stu-id="2701a-118">You cannot add or remove SOA records, but you can edit them.</span></span>
<span data-ttu-id="2701a-119">您可以將 **RecordSet** 物件作為參數傳遞給這個 Cmdlet，或使用管線運算子。</span><span class="sxs-lookup"><span data-stu-id="2701a-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="2701a-120">示例</span><span class="sxs-lookup"><span data-stu-id="2701a-120">EXAMPLES</span></span>

### <span data-ttu-id="2701a-121">範例1：將 A 記錄新增至記錄集</span><span class="sxs-lookup"><span data-stu-id="2701a-121">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="2701a-122">這個範例會將 A 記錄新增至現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="2701a-122">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="2701a-123">範例2：新增 AAAA 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="2701a-123">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="2701a-124">這個範例會將 AAAA 記錄新增至現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="2701a-124">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="2701a-125">範例3：新增 CNAME 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="2701a-125">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="2701a-126">這個範例會在現有的記錄集中加入 CNAME 記錄。</span><span class="sxs-lookup"><span data-stu-id="2701a-126">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="2701a-127">因為 CNAME 記錄集最多可以包含一筆記錄，所以它必須是空記錄集，或必須使用 AzDnsRecordConfig 移除現有的記錄。</span><span class="sxs-lookup"><span data-stu-id="2701a-127">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzDnsRecordConfig.</span></span>

### <span data-ttu-id="2701a-128">範例4：新增 MX 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="2701a-128">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="2701a-129">這個範例會將 MX 記錄新增至現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="2701a-129">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="2701a-130">記錄名稱 "@" 代表在區域 apex 上設定的記錄。</span><span class="sxs-lookup"><span data-stu-id="2701a-130">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="2701a-131">範例5：將 NS 記錄新增至記錄集</span><span class="sxs-lookup"><span data-stu-id="2701a-131">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzDnsRecordSet
```

<span data-ttu-id="2701a-132">這個範例會將 NS 記錄新增至現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="2701a-132">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="2701a-133">範例6：將 PTR 記錄新增至記錄集</span><span class="sxs-lookup"><span data-stu-id="2701a-133">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="2701a-134">這個範例會將 PTR 記錄新增至現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="2701a-134">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="2701a-135">範例7：將 SRV 記錄新增至記錄集</span><span class="sxs-lookup"><span data-stu-id="2701a-135">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="2701a-136">這個範例會將 SRV 記錄新增至現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="2701a-136">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="2701a-137">範例8：新增 TXT 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="2701a-137">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Value "This is a TXT Record" | Set-AzDnsRecordSet
```

<span data-ttu-id="2701a-138">這個範例會將 TXT 記錄新增至現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="2701a-138">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="2701a-139">參數</span><span class="sxs-lookup"><span data-stu-id="2701a-139">PARAMETERS</span></span>

### <span data-ttu-id="2701a-140">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="2701a-140">-CaaFlags</span></span>
<span data-ttu-id="2701a-141">要新增之 CAA 記錄的旗標。</span><span class="sxs-lookup"><span data-stu-id="2701a-141">The flags for the CAA record to add.</span></span> <span data-ttu-id="2701a-142">必須是介於0與255之間的數位。</span><span class="sxs-lookup"><span data-stu-id="2701a-142">Must be a number between 0 and 255.</span></span>

```yaml
Type: System.Byte
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2701a-143">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="2701a-143">-CaaTag</span></span>
<span data-ttu-id="2701a-144">要新增之 CAA 記錄的 tag 欄位。</span><span class="sxs-lookup"><span data-stu-id="2701a-144">The tag field of the CAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2701a-145">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="2701a-145">-CaaValue</span></span>
<span data-ttu-id="2701a-146">要新增之 CAA 記錄的 [值] 欄位。</span><span class="sxs-lookup"><span data-stu-id="2701a-146">The value field for the CAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2701a-147">-Cname</span><span class="sxs-lookup"><span data-stu-id="2701a-147">-Cname</span></span>
<span data-ttu-id="2701a-148">指定正常化) 記錄 (CNAME 名稱的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="2701a-148">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: System.String
Parameter Sets: CNAME
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2701a-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2701a-149">-DefaultProfile</span></span>
<span data-ttu-id="2701a-150">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2701a-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2701a-151">-Exchange</span><span class="sxs-lookup"><span data-stu-id="2701a-151">-Exchange</span></span>
<span data-ttu-id="2701a-152">指定郵件交換 (MX) 記錄的郵件交換伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="2701a-152">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: System.String
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2701a-153">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="2701a-153">-Ipv4Address</span></span>
<span data-ttu-id="2701a-154">指定 A 記錄的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="2701a-154">Specifies an IPv4 address for an A record.</span></span>

```yaml
Type: System.String
Parameter Sets: A
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2701a-155">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="2701a-155">-Ipv6Address</span></span>
<span data-ttu-id="2701a-156">指定 AAAA 記錄的 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="2701a-156">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: System.String
Parameter Sets: AAAA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2701a-157">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="2701a-157">-Nsdname</span></span>
<span data-ttu-id="2701a-158">指定 name server (NS) 記錄的名稱伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="2701a-158">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: System.String
Parameter Sets: NS
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2701a-159">-埠</span><span class="sxs-lookup"><span data-stu-id="2701a-159">-Port</span></span>
<span data-ttu-id="2701a-160">指定服務 (SRV) 記錄的埠。</span><span class="sxs-lookup"><span data-stu-id="2701a-160">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2701a-161">-喜好設定</span><span class="sxs-lookup"><span data-stu-id="2701a-161">-Preference</span></span>
<span data-ttu-id="2701a-162">指定 MX 記錄的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="2701a-162">Specifies the preference for an MX record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2701a-163">-優先順序</span><span class="sxs-lookup"><span data-stu-id="2701a-163">-Priority</span></span>
<span data-ttu-id="2701a-164">指定 SRV 記錄的優先順序。</span><span class="sxs-lookup"><span data-stu-id="2701a-164">Specifies the priority for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2701a-165">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="2701a-165">-Ptrdname</span></span>
<span data-ttu-id="2701a-166">指定指標資源的目標功能變數名稱 (PTR) 記錄。</span><span class="sxs-lookup"><span data-stu-id="2701a-166">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: System.String
Parameter Sets: PTR
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2701a-167">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="2701a-167">-RecordSet</span></span>
<span data-ttu-id="2701a-168">指定要編輯的 **記錄集** 物件。</span><span class="sxs-lookup"><span data-stu-id="2701a-168">Specifies the **RecordSet** object to edit.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2701a-169">-目標</span><span class="sxs-lookup"><span data-stu-id="2701a-169">-Target</span></span>
<span data-ttu-id="2701a-170">指定 SRV 記錄的目標。</span><span class="sxs-lookup"><span data-stu-id="2701a-170">Specifies the target for an SRV record.</span></span>

```yaml
Type: System.String
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2701a-171">-值</span><span class="sxs-lookup"><span data-stu-id="2701a-171">-Value</span></span>
<span data-ttu-id="2701a-172">指定 TXT 記錄的值。</span><span class="sxs-lookup"><span data-stu-id="2701a-172">Specifies the value for a TXT record.</span></span>

```yaml
Type: System.String
Parameter Sets: TXT
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2701a-173">寬度</span><span class="sxs-lookup"><span data-stu-id="2701a-173">-Weight</span></span>
<span data-ttu-id="2701a-174">指定 SRV 記錄的權重。</span><span class="sxs-lookup"><span data-stu-id="2701a-174">Specifies the weight for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2701a-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2701a-175">CommonParameters</span></span>
<span data-ttu-id="2701a-176">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2701a-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2701a-177">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2701a-177">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2701a-178">輸入</span><span class="sxs-lookup"><span data-stu-id="2701a-178">INPUTS</span></span>

### <span data-ttu-id="2701a-179">DnsRecordSet （）</span><span class="sxs-lookup"><span data-stu-id="2701a-179">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

### <span data-ttu-id="2701a-180">System.object</span><span class="sxs-lookup"><span data-stu-id="2701a-180">System.String</span></span>

### <span data-ttu-id="2701a-181">System.object</span><span class="sxs-lookup"><span data-stu-id="2701a-181">System.UInt16</span></span>

### <span data-ttu-id="2701a-182">System.object</span><span class="sxs-lookup"><span data-stu-id="2701a-182">System.Byte</span></span>

## <span data-ttu-id="2701a-183">輸出</span><span class="sxs-lookup"><span data-stu-id="2701a-183">OUTPUTS</span></span>

### <span data-ttu-id="2701a-184">DnsRecordSet （）</span><span class="sxs-lookup"><span data-stu-id="2701a-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="2701a-185">筆記</span><span class="sxs-lookup"><span data-stu-id="2701a-185">NOTES</span></span>

## <span data-ttu-id="2701a-186">相關連結</span><span class="sxs-lookup"><span data-stu-id="2701a-186">RELATED LINKS</span></span>

[<span data-ttu-id="2701a-187">AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2701a-187">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="2701a-188">移除-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="2701a-188">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)

[<span data-ttu-id="2701a-189">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2701a-189">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
