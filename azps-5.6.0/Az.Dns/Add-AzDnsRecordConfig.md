---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: https://docs.microsoft.com/powershell/module/az.dns/add-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
ms.openlocfilehash: 885c7ad64b207f74fa7953050a6ceba9ecc44f43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910161"
---
# <span data-ttu-id="8f95d-101">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="8f95d-101">Add-AzDnsRecordConfig</span></span>

## <span data-ttu-id="8f95d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8f95d-102">SYNOPSIS</span></span>
<span data-ttu-id="8f95d-103">新增 DNS 記錄至本地記錄集物件。</span><span class="sxs-lookup"><span data-stu-id="8f95d-103">Adds a DNS record to a local record set object.</span></span>

## <span data-ttu-id="8f95d-104">語法</span><span class="sxs-lookup"><span data-stu-id="8f95d-104">SYNTAX</span></span>

### <span data-ttu-id="8f95d-105">A</span><span class="sxs-lookup"><span data-stu-id="8f95d-105">A</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f95d-106">Aaaa</span><span class="sxs-lookup"><span data-stu-id="8f95d-106">AAAA</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f95d-107">Ns</span><span class="sxs-lookup"><span data-stu-id="8f95d-107">NS</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f95d-108">Mx</span><span class="sxs-lookup"><span data-stu-id="8f95d-108">MX</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f95d-109">Ptr</span><span class="sxs-lookup"><span data-stu-id="8f95d-109">PTR</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f95d-110">Txt</span><span class="sxs-lookup"><span data-stu-id="8f95d-110">TXT</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f95d-111">SRV</span><span class="sxs-lookup"><span data-stu-id="8f95d-111">SRV</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f95d-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="8f95d-112">CNAME</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f95d-113">Caa</span><span class="sxs-lookup"><span data-stu-id="8f95d-113">Caa</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f95d-114">描述</span><span class="sxs-lookup"><span data-stu-id="8f95d-114">DESCRIPTION</span></span>
<span data-ttu-id="8f95d-115">**Add-AzDnsRecordConfig** Cmdlet 會新增網域名稱系統 (DNS) 記錄至 **RecordSet** 物件。</span><span class="sxs-lookup"><span data-stu-id="8f95d-115">The **Add-AzDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="8f95d-116">**RecordSet** 物件是離線物件，而變更不會變更 DNS 回應，直到您執行 Set-AzDnsRecordSet Cmdlet 以將變更持續變更至 Microsoft Azure DNS 服務之後。</span><span class="sxs-lookup"><span data-stu-id="8f95d-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="8f95d-117">建立 DNS 區域時，會建立 DNS 記錄，而 DNS 區域刪除時，會移除這些記錄。</span><span class="sxs-lookup"><span data-stu-id="8f95d-117">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="8f95d-118">您無法新增或移除 DNS 記錄，但可以編輯記錄。</span><span class="sxs-lookup"><span data-stu-id="8f95d-118">You cannot add or remove SOA records, but you can edit them.</span></span>
<span data-ttu-id="8f95d-119">您可以將 **RecordSet 物件** 以參數或管道運算子傳遞至此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8f95d-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="8f95d-120">例子</span><span class="sxs-lookup"><span data-stu-id="8f95d-120">EXAMPLES</span></span>

### <span data-ttu-id="8f95d-121">範例 1：新增 A 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="8f95d-121">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="8f95d-122">此範例會將 A 記錄新增到現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="8f95d-122">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="8f95d-123">範例 2：新增 AAAA 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="8f95d-123">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="8f95d-124">此範例會新增 AAAA 記錄至現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="8f95d-124">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="8f95d-125">範例 3：新增 CNAME 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="8f95d-125">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="8f95d-126">此範例會將 CNAME 記錄新增到現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="8f95d-126">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="8f95d-127">由於 CNAME 記錄集最多隻能包含一筆記錄，因此一開始它必須是空白記錄集，或必須使用 Remove-AzDnsRecordConfig 移除現有的記錄。</span><span class="sxs-lookup"><span data-stu-id="8f95d-127">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzDnsRecordConfig.</span></span>

### <span data-ttu-id="8f95d-128">範例 4：新增 MX 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="8f95d-128">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="8f95d-129">此範例會將 MX 記錄新增到現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="8f95d-129">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="8f95d-130">記錄名稱 "@" 表示區域頂點的記錄集。</span><span class="sxs-lookup"><span data-stu-id="8f95d-130">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="8f95d-131">範例 5：新增 NS 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="8f95d-131">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzDnsRecordSet
```

<span data-ttu-id="8f95d-132">此範例會將 NS 記錄新增到現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="8f95d-132">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="8f95d-133">範例 6：新增 PTR 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="8f95d-133">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="8f95d-134">此範例會將 PTR 記錄新增到現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="8f95d-134">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="8f95d-135">範例 7：新增 SRV 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="8f95d-135">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="8f95d-136">此範例會將 SRV 記錄新增到現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="8f95d-136">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="8f95d-137">範例 8：新增 TXT 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="8f95d-137">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Value "This is a TXT Record" | Set-AzDnsRecordSet
```

<span data-ttu-id="8f95d-138">此範例會將 TXT 記錄新增到現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="8f95d-138">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="8f95d-139">參數</span><span class="sxs-lookup"><span data-stu-id="8f95d-139">PARAMETERS</span></span>

### <span data-ttu-id="8f95d-140">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="8f95d-140">-CaaFlags</span></span>
<span data-ttu-id="8f95d-141">要新增之 CAA 記錄的標標。</span><span class="sxs-lookup"><span data-stu-id="8f95d-141">The flags for the CAA record to add.</span></span> <span data-ttu-id="8f95d-142">必須是介於 0 到 255 之間的數位。</span><span class="sxs-lookup"><span data-stu-id="8f95d-142">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="8f95d-143">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="8f95d-143">-CaaTag</span></span>
<span data-ttu-id="8f95d-144">要新增之 CAA 記錄的標記欄位。</span><span class="sxs-lookup"><span data-stu-id="8f95d-144">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="8f95d-145">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="8f95d-145">-CaaValue</span></span>
<span data-ttu-id="8f95d-146">要新增之 CAA 記錄的值欄位。</span><span class="sxs-lookup"><span data-stu-id="8f95d-146">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="8f95d-147">-Cname</span><span class="sxs-lookup"><span data-stu-id="8f95d-147">-Cname</span></span>
<span data-ttu-id="8f95d-148">指定 CNAME 記錄中標準名稱 (功能變數名稱) 名稱。</span><span class="sxs-lookup"><span data-stu-id="8f95d-148">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="8f95d-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f95d-149">-DefaultProfile</span></span>
<span data-ttu-id="8f95d-150">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="8f95d-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f95d-151">-Exchange</span><span class="sxs-lookup"><span data-stu-id="8f95d-151">-Exchange</span></span>
<span data-ttu-id="8f95d-152">指定 MX 記錄中郵件交換 (伺服器) 名稱。</span><span class="sxs-lookup"><span data-stu-id="8f95d-152">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="8f95d-153">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="8f95d-153">-Ipv4Address</span></span>
<span data-ttu-id="8f95d-154">指定 A 記錄的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="8f95d-154">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="8f95d-155">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="8f95d-155">-Ipv6Address</span></span>
<span data-ttu-id="8f95d-156">指定 AAAA 記錄的 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="8f95d-156">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="8f95d-157">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="8f95d-157">-Nsdname</span></span>
<span data-ttu-id="8f95d-158">指定名稱伺服器的名稱伺服器名稱 (NS) 記錄。</span><span class="sxs-lookup"><span data-stu-id="8f95d-158">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="8f95d-159">-埠</span><span class="sxs-lookup"><span data-stu-id="8f95d-159">-Port</span></span>
<span data-ttu-id="8f95d-160">指定 SRV 記錄中 (的) 埠。</span><span class="sxs-lookup"><span data-stu-id="8f95d-160">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="8f95d-161">-喜好設定</span><span class="sxs-lookup"><span data-stu-id="8f95d-161">-Preference</span></span>
<span data-ttu-id="8f95d-162">指定 MX 記錄的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="8f95d-162">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="8f95d-163">-優先順序</span><span class="sxs-lookup"><span data-stu-id="8f95d-163">-Priority</span></span>
<span data-ttu-id="8f95d-164">指定 SRV 記錄的優先順序。</span><span class="sxs-lookup"><span data-stu-id="8f95d-164">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="8f95d-165">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="8f95d-165">-Ptrdname</span></span>
<span data-ttu-id="8f95d-166">指定 PTR 記錄中指標資源 (功能變數名稱) 名稱。</span><span class="sxs-lookup"><span data-stu-id="8f95d-166">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="8f95d-167">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="8f95d-167">-RecordSet</span></span>
<span data-ttu-id="8f95d-168">指定 **要編輯的 RecordSet** 物件。</span><span class="sxs-lookup"><span data-stu-id="8f95d-168">Specifies the **RecordSet** object to edit.</span></span>

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

### <span data-ttu-id="8f95d-169">-目標</span><span class="sxs-lookup"><span data-stu-id="8f95d-169">-Target</span></span>
<span data-ttu-id="8f95d-170">指定 SRV 記錄的目標。</span><span class="sxs-lookup"><span data-stu-id="8f95d-170">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="8f95d-171">-值</span><span class="sxs-lookup"><span data-stu-id="8f95d-171">-Value</span></span>
<span data-ttu-id="8f95d-172">指定 TXT 記錄的值。</span><span class="sxs-lookup"><span data-stu-id="8f95d-172">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="8f95d-173">-重量</span><span class="sxs-lookup"><span data-stu-id="8f95d-173">-Weight</span></span>
<span data-ttu-id="8f95d-174">指定 SRV 記錄的粗細。</span><span class="sxs-lookup"><span data-stu-id="8f95d-174">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="8f95d-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f95d-175">CommonParameters</span></span>
<span data-ttu-id="8f95d-176">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8f95d-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f95d-177">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="8f95d-177">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f95d-178">輸入</span><span class="sxs-lookup"><span data-stu-id="8f95d-178">INPUTS</span></span>

### <span data-ttu-id="8f95d-179">Microsoft.Azure.Commands.dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8f95d-179">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

### <span data-ttu-id="8f95d-180">System.String</span><span class="sxs-lookup"><span data-stu-id="8f95d-180">System.String</span></span>

### <span data-ttu-id="8f95d-181">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="8f95d-181">System.UInt16</span></span>

### <span data-ttu-id="8f95d-182">System.Byte</span><span class="sxs-lookup"><span data-stu-id="8f95d-182">System.Byte</span></span>

## <span data-ttu-id="8f95d-183">輸出</span><span class="sxs-lookup"><span data-stu-id="8f95d-183">OUTPUTS</span></span>

### <span data-ttu-id="8f95d-184">Microsoft.Azure.Commands.dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8f95d-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="8f95d-185">筆記</span><span class="sxs-lookup"><span data-stu-id="8f95d-185">NOTES</span></span>

## <span data-ttu-id="8f95d-186">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f95d-186">RELATED LINKS</span></span>

[<span data-ttu-id="8f95d-187">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8f95d-187">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="8f95d-188">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="8f95d-188">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)

[<span data-ttu-id="8f95d-189">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8f95d-189">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
