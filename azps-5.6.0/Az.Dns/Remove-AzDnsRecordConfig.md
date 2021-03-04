---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/powershell/module/az.dns/remove-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
ms.openlocfilehash: 07af143e1a1582670d15a15c356f673fef1f7590
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910133"
---
# <span data-ttu-id="612ac-101">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="612ac-101">Remove-AzDnsRecordConfig</span></span>

## <span data-ttu-id="612ac-102">簡介</span><span class="sxs-lookup"><span data-stu-id="612ac-102">SYNOPSIS</span></span>
<span data-ttu-id="612ac-103">從本地記錄集物件移除 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="612ac-103">Removes a DNS record from a local record set object.</span></span>

## <span data-ttu-id="612ac-104">語法</span><span class="sxs-lookup"><span data-stu-id="612ac-104">SYNTAX</span></span>

### <span data-ttu-id="612ac-105">A</span><span class="sxs-lookup"><span data-stu-id="612ac-105">A</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="612ac-106">Aaaa</span><span class="sxs-lookup"><span data-stu-id="612ac-106">AAAA</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="612ac-107">Ns</span><span class="sxs-lookup"><span data-stu-id="612ac-107">NS</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="612ac-108">Mx</span><span class="sxs-lookup"><span data-stu-id="612ac-108">MX</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="612ac-109">Ptr</span><span class="sxs-lookup"><span data-stu-id="612ac-109">PTR</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="612ac-110">Txt</span><span class="sxs-lookup"><span data-stu-id="612ac-110">TXT</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="612ac-111">SRV</span><span class="sxs-lookup"><span data-stu-id="612ac-111">SRV</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="612ac-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="612ac-112">CNAME</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="612ac-113">Caa</span><span class="sxs-lookup"><span data-stu-id="612ac-113">Caa</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="612ac-114">描述</span><span class="sxs-lookup"><span data-stu-id="612ac-114">DESCRIPTION</span></span>
<span data-ttu-id="612ac-115">**Remove-AzDnsRecordConfig Cmdlet** 會從記錄集 (DNS) 網域名稱系統。</span><span class="sxs-lookup"><span data-stu-id="612ac-115">The **Remove-AzDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="612ac-116">**RecordSet** 物件是離線物件，而變更不會變更 DNS 回應，直到您執行 Set-AzDnsRecordSet Cmdlet 以將變更持續變更至 Microsoft Azure DNS 服務之後。</span><span class="sxs-lookup"><span data-stu-id="612ac-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="612ac-117">若要移除記錄，該記錄類型的所有欄位必須完全相符。</span><span class="sxs-lookup"><span data-stu-id="612ac-117">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="612ac-118">您無法新增或移除 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="612ac-118">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="612ac-119">建立 DNS 區域時會自動建立 DNS 記錄，並會在刪除 DNS 區域時自動刪除。</span><span class="sxs-lookup"><span data-stu-id="612ac-119">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>
<span data-ttu-id="612ac-120">您可以將 **RecordSet 物件** 以參數或管道運算子傳遞至此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="612ac-120">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="612ac-121">例子</span><span class="sxs-lookup"><span data-stu-id="612ac-121">EXAMPLES</span></span>

### <span data-ttu-id="612ac-122">範例 1：從記錄集移除記錄</span><span class="sxs-lookup"><span data-stu-id="612ac-122">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="612ac-123">此範例會從現有的記錄集移除 A 記錄。</span><span class="sxs-lookup"><span data-stu-id="612ac-123">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="612ac-124">如果這是記錄集的唯一記錄，結果就會是空白的記錄集。</span><span class="sxs-lookup"><span data-stu-id="612ac-124">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="612ac-125">若要完全移除記錄集，請參閱 Remove-AzDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="612ac-125">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="612ac-126">範例 2：從記錄集移除 AAAA 記錄</span><span class="sxs-lookup"><span data-stu-id="612ac-126">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="612ac-127">此範例會從現有的記錄集移除 AAAA 記錄。</span><span class="sxs-lookup"><span data-stu-id="612ac-127">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="612ac-128">如果這是記錄集的唯一記錄，結果就會是空白的記錄集。</span><span class="sxs-lookup"><span data-stu-id="612ac-128">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="612ac-129">若要完全移除記錄集，請參閱 Remove-AzDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="612ac-129">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="612ac-130">範例 3：從記錄集移除 CNAME 記錄</span><span class="sxs-lookup"><span data-stu-id="612ac-130">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="612ac-131">此範例會從現有的記錄集移除 CNAME 記錄。</span><span class="sxs-lookup"><span data-stu-id="612ac-131">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="612ac-132">由於 CNAME 記錄集最多隻能包含一筆記錄，因此結果為空白的記錄集。</span><span class="sxs-lookup"><span data-stu-id="612ac-132">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="612ac-133">範例 4：從記錄集移除 MX 記錄</span><span class="sxs-lookup"><span data-stu-id="612ac-133">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="612ac-134">此範例會從現有的記錄集移除 MX 記錄。</span><span class="sxs-lookup"><span data-stu-id="612ac-134">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="612ac-135">記錄名稱 "@" 表示區域頂點的記錄集。</span><span class="sxs-lookup"><span data-stu-id="612ac-135">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="612ac-136">如果這是記錄集的唯一記錄，則結果為空白的記錄集。</span><span class="sxs-lookup"><span data-stu-id="612ac-136">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="612ac-137">若要完全移除記錄集，請參閱 Remove-AzDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="612ac-137">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="612ac-138">範例 5：從記錄集移除 NS 記錄</span><span class="sxs-lookup"><span data-stu-id="612ac-138">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzDnsRecordSet
```

<span data-ttu-id="612ac-139">此範例會從現有的記錄集移除 NS 記錄。</span><span class="sxs-lookup"><span data-stu-id="612ac-139">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="612ac-140">如果這是記錄集的唯一記錄，則結果為空白的記錄集。</span><span class="sxs-lookup"><span data-stu-id="612ac-140">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="612ac-141">若要完全移除記錄集，請參閱 Remove-AzDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="612ac-141">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="612ac-142">範例 6：從記錄集移除 PTR 記錄</span><span class="sxs-lookup"><span data-stu-id="612ac-142">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="612ac-143">此範例會從現有的記錄集移除 PTR 記錄。</span><span class="sxs-lookup"><span data-stu-id="612ac-143">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="612ac-144">如果這是記錄集的唯一記錄，則結果為空白的記錄集。</span><span class="sxs-lookup"><span data-stu-id="612ac-144">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="612ac-145">若要完全移除記錄集，請參閱 Remove-AzDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="612ac-145">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="612ac-146">範例 7：從記錄集移除 SRV 記錄</span><span class="sxs-lookup"><span data-stu-id="612ac-146">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="612ac-147">此範例會從現有的記錄集移除 SRV 記錄。</span><span class="sxs-lookup"><span data-stu-id="612ac-147">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="612ac-148">如果這是記錄集的唯一記錄，則結果為空白的記錄集。</span><span class="sxs-lookup"><span data-stu-id="612ac-148">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="612ac-149">若要完全移除記錄集，請參閱 Remove-AzDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="612ac-149">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="612ac-150">範例 8：從記錄集移除 TXT 記錄</span><span class="sxs-lookup"><span data-stu-id="612ac-150">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Value "This is a TXT Record"  | Set-AzDnsRecordSet
```

<span data-ttu-id="612ac-151">此範例會從現有的記錄集移除 TXT 記錄。</span><span class="sxs-lookup"><span data-stu-id="612ac-151">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="612ac-152">如果這是記錄集的唯一記錄，則結果為空白的記錄集。</span><span class="sxs-lookup"><span data-stu-id="612ac-152">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="612ac-153">若要完全移除記錄集，請參閱 Remove-AzDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="612ac-153">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

## <span data-ttu-id="612ac-154">參數</span><span class="sxs-lookup"><span data-stu-id="612ac-154">PARAMETERS</span></span>

### <span data-ttu-id="612ac-155">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="612ac-155">-CaaFlags</span></span>
<span data-ttu-id="612ac-156">要新增之 CAA 記錄的標標。</span><span class="sxs-lookup"><span data-stu-id="612ac-156">The flags for the CAA record to add.</span></span> <span data-ttu-id="612ac-157">必須是介於 0 到 255 之間的數位。</span><span class="sxs-lookup"><span data-stu-id="612ac-157">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="612ac-158">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="612ac-158">-CaaTag</span></span>
<span data-ttu-id="612ac-159">要新增之 CAA 記錄的標記欄位。</span><span class="sxs-lookup"><span data-stu-id="612ac-159">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="612ac-160">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="612ac-160">-CaaValue</span></span>
<span data-ttu-id="612ac-161">要新增之 CAA 記錄的值欄位。</span><span class="sxs-lookup"><span data-stu-id="612ac-161">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="612ac-162">-Cname</span><span class="sxs-lookup"><span data-stu-id="612ac-162">-Cname</span></span>
<span data-ttu-id="612ac-163">指定 CNAME 記錄中標準名稱 (功能變數名稱) 名稱。</span><span class="sxs-lookup"><span data-stu-id="612ac-163">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="612ac-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="612ac-164">-DefaultProfile</span></span>
<span data-ttu-id="612ac-165">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="612ac-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="612ac-166">-Exchange</span><span class="sxs-lookup"><span data-stu-id="612ac-166">-Exchange</span></span>
<span data-ttu-id="612ac-167">指定 MX 記錄中郵件交換 (伺服器) 名稱。</span><span class="sxs-lookup"><span data-stu-id="612ac-167">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="612ac-168">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="612ac-168">-Ipv4Address</span></span>
<span data-ttu-id="612ac-169">指定 A 記錄的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="612ac-169">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="612ac-170">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="612ac-170">-Ipv6Address</span></span>
<span data-ttu-id="612ac-171">指定 AAAA 記錄的 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="612ac-171">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="612ac-172">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="612ac-172">-Nsdname</span></span>
<span data-ttu-id="612ac-173">指定名稱伺服器的名稱伺服器 (NS) 記錄。</span><span class="sxs-lookup"><span data-stu-id="612ac-173">Specifies the name server for a name server (NS) record.</span></span>

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

### <span data-ttu-id="612ac-174">-埠</span><span class="sxs-lookup"><span data-stu-id="612ac-174">-Port</span></span>
<span data-ttu-id="612ac-175">指定 SRV 記錄中 (的) 埠。</span><span class="sxs-lookup"><span data-stu-id="612ac-175">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="612ac-176">-喜好設定</span><span class="sxs-lookup"><span data-stu-id="612ac-176">-Preference</span></span>
<span data-ttu-id="612ac-177">指定 MX 記錄的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="612ac-177">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="612ac-178">-優先順序</span><span class="sxs-lookup"><span data-stu-id="612ac-178">-Priority</span></span>
<span data-ttu-id="612ac-179">指定 SRV 記錄的優先順序。</span><span class="sxs-lookup"><span data-stu-id="612ac-179">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="612ac-180">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="612ac-180">-Ptrdname</span></span>
<span data-ttu-id="612ac-181">指定 PTR 記錄中指標 (功能變數名稱) 名稱。</span><span class="sxs-lookup"><span data-stu-id="612ac-181">Specifies the target domain name of a pointer (PTR) record.</span></span>

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

### <span data-ttu-id="612ac-182">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="612ac-182">-RecordSet</span></span>
<span data-ttu-id="612ac-183">指定 **包含要移除** 之記錄的 RecordSet 物件。</span><span class="sxs-lookup"><span data-stu-id="612ac-183">Specifies the **RecordSet** object that contains the record to remove.</span></span>

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

### <span data-ttu-id="612ac-184">-目標</span><span class="sxs-lookup"><span data-stu-id="612ac-184">-Target</span></span>
<span data-ttu-id="612ac-185">指定 SRV 記錄的目標。</span><span class="sxs-lookup"><span data-stu-id="612ac-185">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="612ac-186">-值</span><span class="sxs-lookup"><span data-stu-id="612ac-186">-Value</span></span>
<span data-ttu-id="612ac-187">指定 TXT 記錄的值。</span><span class="sxs-lookup"><span data-stu-id="612ac-187">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="612ac-188">-重量</span><span class="sxs-lookup"><span data-stu-id="612ac-188">-Weight</span></span>
<span data-ttu-id="612ac-189">指定 SRV 記錄的粗細。</span><span class="sxs-lookup"><span data-stu-id="612ac-189">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="612ac-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="612ac-190">CommonParameters</span></span>
<span data-ttu-id="612ac-191">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="612ac-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="612ac-192">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="612ac-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="612ac-193">輸入</span><span class="sxs-lookup"><span data-stu-id="612ac-193">INPUTS</span></span>

### <span data-ttu-id="612ac-194">Microsoft.Azure.Commands.dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="612ac-194">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

### <span data-ttu-id="612ac-195">System.String</span><span class="sxs-lookup"><span data-stu-id="612ac-195">System.String</span></span>

### <span data-ttu-id="612ac-196">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="612ac-196">System.UInt16</span></span>

### <span data-ttu-id="612ac-197">System.Byte</span><span class="sxs-lookup"><span data-stu-id="612ac-197">System.Byte</span></span>

## <span data-ttu-id="612ac-198">輸出</span><span class="sxs-lookup"><span data-stu-id="612ac-198">OUTPUTS</span></span>

### <span data-ttu-id="612ac-199">Microsoft.Azure.Commands.dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="612ac-199">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="612ac-200">筆記</span><span class="sxs-lookup"><span data-stu-id="612ac-200">NOTES</span></span>

## <span data-ttu-id="612ac-201">相關連結</span><span class="sxs-lookup"><span data-stu-id="612ac-201">RELATED LINKS</span></span>

[<span data-ttu-id="612ac-202">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="612ac-202">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="612ac-203">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="612ac-203">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="612ac-204">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="612ac-204">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
