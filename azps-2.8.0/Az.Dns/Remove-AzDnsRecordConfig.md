---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
ms.openlocfilehash: acf81459fd62e3f86c8e4ad02bfdefd0055db270
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612495"
---
# <span data-ttu-id="9b2d3-101">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="9b2d3-101">Remove-AzDnsRecordConfig</span></span>

## <span data-ttu-id="9b2d3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9b2d3-102">SYNOPSIS</span></span>
<span data-ttu-id="9b2d3-103">從本機記錄集物件中移除 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-103">Removes a DNS record from a local record set object.</span></span>

## <span data-ttu-id="9b2d3-104">句法</span><span class="sxs-lookup"><span data-stu-id="9b2d3-104">SYNTAX</span></span>

### <span data-ttu-id="9b2d3-105">是</span><span class="sxs-lookup"><span data-stu-id="9b2d3-105">A</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b2d3-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="9b2d3-106">AAAA</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b2d3-107">NS</span><span class="sxs-lookup"><span data-stu-id="9b2d3-107">NS</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b2d3-108">MX</span><span class="sxs-lookup"><span data-stu-id="9b2d3-108">MX</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b2d3-109">PTR</span><span class="sxs-lookup"><span data-stu-id="9b2d3-109">PTR</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b2d3-110">文字檔</span><span class="sxs-lookup"><span data-stu-id="9b2d3-110">TXT</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b2d3-111">DNS-SRV</span><span class="sxs-lookup"><span data-stu-id="9b2d3-111">SRV</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b2d3-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="9b2d3-112">CNAME</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b2d3-113">Caa</span><span class="sxs-lookup"><span data-stu-id="9b2d3-113">Caa</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b2d3-114">說明</span><span class="sxs-lookup"><span data-stu-id="9b2d3-114">DESCRIPTION</span></span>
<span data-ttu-id="9b2d3-115">**AzDnsRecordConfig** Cmdlet 會從記錄集中移除 (DNS) 記錄的網域名稱系統。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-115">The **Remove-AzDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="9b2d3-116">**RecordSet** 物件是離線物件，而且在您執行 Set-AzDnsRecordSet Cmdlet 以保留 MICROSOFT Azure DNS 服務的變更之後，才能變更 DNS 回應。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="9b2d3-117">若要移除記錄，該記錄類型的所有欄位都必須完全相符。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-117">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="9b2d3-118">您無法新增或移除 SOA 記錄。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-118">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="9b2d3-119">SOA 記錄會在建立 DNS 區域時自動建立，並在 DNS 區域刪除時自動刪除。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-119">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>
<span data-ttu-id="9b2d3-120">您可以將 **RecordSet** 物件作為參數傳遞給這個 Cmdlet，或使用管線運算子。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-120">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="9b2d3-121">示例</span><span class="sxs-lookup"><span data-stu-id="9b2d3-121">EXAMPLES</span></span>

### <span data-ttu-id="9b2d3-122">範例1：從記錄集中移除 A 記錄</span><span class="sxs-lookup"><span data-stu-id="9b2d3-122">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="9b2d3-123">這個範例會從現有的記錄集中移除 A 記錄。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-123">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="9b2d3-124">如果這是記錄集中的唯一記錄，結果就會是一個空的記錄集。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-124">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="9b2d3-125">若要完全移除記錄集，請參閱移除-AzDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-125">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="9b2d3-126">範例2：從記錄集中移除 AAAA 記錄</span><span class="sxs-lookup"><span data-stu-id="9b2d3-126">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="9b2d3-127">這個範例會從現有的記錄集中移除 AAAA 記錄。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-127">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="9b2d3-128">如果這是記錄集中的唯一記錄，結果就會是一個空的記錄集。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-128">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="9b2d3-129">若要完全移除記錄集，請參閱移除-AzDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-129">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="9b2d3-130">範例3：從記錄集中移除 CNAME 記錄</span><span class="sxs-lookup"><span data-stu-id="9b2d3-130">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="9b2d3-131">這個範例會從現有的記錄集中移除 CNAME 記錄。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-131">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="9b2d3-132">因為 CNAME 記錄集最多可以包含一筆記錄，所以結果是一個空的記錄集。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-132">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="9b2d3-133">範例4：從記錄集中移除 MX 記錄</span><span class="sxs-lookup"><span data-stu-id="9b2d3-133">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="9b2d3-134">這個範例會從現有的記錄集中移除 MX 記錄。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-134">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="9b2d3-135">記錄名稱 "@" 代表在區域 apex 上設定的記錄。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-135">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="9b2d3-136">如果這是記錄集中的唯一記錄，則結果是一個空的記錄集。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-136">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="9b2d3-137">若要完全移除記錄集，請參閱移除-AzDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-137">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="9b2d3-138">範例5：從記錄集中移除 NS 記錄</span><span class="sxs-lookup"><span data-stu-id="9b2d3-138">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzDnsRecordSet
```

<span data-ttu-id="9b2d3-139">這個範例會從現有的記錄集中移除 NS 記錄。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-139">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="9b2d3-140">如果這是記錄集中的唯一記錄，則結果是一個空的記錄集。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-140">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="9b2d3-141">若要完全移除記錄集，請參閱移除-AzDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-141">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="9b2d3-142">範例6：從記錄集中移除 PTR 記錄</span><span class="sxs-lookup"><span data-stu-id="9b2d3-142">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="9b2d3-143">這個範例會從現有的記錄集中移除 PTR 記錄。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-143">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="9b2d3-144">如果這是記錄集中的唯一記錄，則結果是一個空的記錄集。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-144">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="9b2d3-145">若要完全移除記錄集，請參閱移除-AzDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-145">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="9b2d3-146">範例7：從記錄集中移除 SRV 記錄</span><span class="sxs-lookup"><span data-stu-id="9b2d3-146">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="9b2d3-147">這個範例會從現有的記錄集中移除 SRV 記錄。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-147">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="9b2d3-148">如果這是記錄集中的唯一記錄，則結果是一個空的記錄集。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-148">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="9b2d3-149">若要完全移除記錄集，請參閱移除-AzDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-149">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="9b2d3-150">範例8：從記錄集中移除 TXT 記錄</span><span class="sxs-lookup"><span data-stu-id="9b2d3-150">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Value "This is a TXT Record"  | Set-AzDnsRecordSet
```

<span data-ttu-id="9b2d3-151">這個範例會從現有的記錄集中移除 TXT 記錄。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-151">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="9b2d3-152">如果這是記錄集中的唯一記錄，則結果是一個空的記錄集。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-152">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="9b2d3-153">若要完全移除記錄集，請參閱移除-AzDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-153">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

## <span data-ttu-id="9b2d3-154">參數</span><span class="sxs-lookup"><span data-stu-id="9b2d3-154">PARAMETERS</span></span>

### <span data-ttu-id="9b2d3-155">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="9b2d3-155">-CaaFlags</span></span>
<span data-ttu-id="9b2d3-156">要新增之 CAA 記錄的旗標。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-156">The flags for the CAA record to add.</span></span> <span data-ttu-id="9b2d3-157">必須是介於0與255之間的數位。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-157">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="9b2d3-158">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="9b2d3-158">-CaaTag</span></span>
<span data-ttu-id="9b2d3-159">要新增之 CAA 記錄的 tag 欄位。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-159">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="9b2d3-160">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="9b2d3-160">-CaaValue</span></span>
<span data-ttu-id="9b2d3-161">要新增之 CAA 記錄的 [值] 欄位。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-161">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="9b2d3-162">-Cname</span><span class="sxs-lookup"><span data-stu-id="9b2d3-162">-Cname</span></span>
<span data-ttu-id="9b2d3-163">指定正常化) 記錄 (CNAME 名稱的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-163">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="9b2d3-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b2d3-164">-DefaultProfile</span></span>
<span data-ttu-id="9b2d3-165">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9b2d3-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b2d3-166">-Exchange</span><span class="sxs-lookup"><span data-stu-id="9b2d3-166">-Exchange</span></span>
<span data-ttu-id="9b2d3-167">指定郵件交換 (MX) 記錄的郵件交換伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-167">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="9b2d3-168">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="9b2d3-168">-Ipv4Address</span></span>
<span data-ttu-id="9b2d3-169">指定 A 記錄的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-169">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="9b2d3-170">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="9b2d3-170">-Ipv6Address</span></span>
<span data-ttu-id="9b2d3-171">指定 AAAA 記錄的 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-171">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="9b2d3-172">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="9b2d3-172">-Nsdname</span></span>
<span data-ttu-id="9b2d3-173">指定 name server (NS) 記錄的名稱伺服器。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-173">Specifies the name server for a name server (NS) record.</span></span>

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

### <span data-ttu-id="9b2d3-174">-埠</span><span class="sxs-lookup"><span data-stu-id="9b2d3-174">-Port</span></span>
<span data-ttu-id="9b2d3-175">指定服務 (SRV) 記錄的埠。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-175">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="9b2d3-176">-喜好設定</span><span class="sxs-lookup"><span data-stu-id="9b2d3-176">-Preference</span></span>
<span data-ttu-id="9b2d3-177">指定 MX 記錄的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-177">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="9b2d3-178">-優先順序</span><span class="sxs-lookup"><span data-stu-id="9b2d3-178">-Priority</span></span>
<span data-ttu-id="9b2d3-179">指定 SRV 記錄的優先順序。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-179">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="9b2d3-180">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="9b2d3-180">-Ptrdname</span></span>
<span data-ttu-id="9b2d3-181">指定指標 (PTR) 記錄的目標功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-181">Specifies the target domain name of a pointer (PTR) record.</span></span>

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

### <span data-ttu-id="9b2d3-182">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="9b2d3-182">-RecordSet</span></span>
<span data-ttu-id="9b2d3-183">指定包含要移除之記錄的 **記錄集** 物件。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-183">Specifies the **RecordSet** object that contains the record to remove.</span></span>

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

### <span data-ttu-id="9b2d3-184">-目標</span><span class="sxs-lookup"><span data-stu-id="9b2d3-184">-Target</span></span>
<span data-ttu-id="9b2d3-185">指定 SRV 記錄的目標。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-185">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="9b2d3-186">-值</span><span class="sxs-lookup"><span data-stu-id="9b2d3-186">-Value</span></span>
<span data-ttu-id="9b2d3-187">指定 TXT 記錄的值。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-187">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="9b2d3-188">寬度</span><span class="sxs-lookup"><span data-stu-id="9b2d3-188">-Weight</span></span>
<span data-ttu-id="9b2d3-189">指定 SRV 記錄的權重。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-189">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="9b2d3-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b2d3-190">CommonParameters</span></span>
<span data-ttu-id="9b2d3-191">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b2d3-192">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9b2d3-192">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b2d3-193">輸入</span><span class="sxs-lookup"><span data-stu-id="9b2d3-193">INPUTS</span></span>

### <span data-ttu-id="9b2d3-194">DnsRecordSet （）</span><span class="sxs-lookup"><span data-stu-id="9b2d3-194">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

### <span data-ttu-id="9b2d3-195">System.object</span><span class="sxs-lookup"><span data-stu-id="9b2d3-195">System.String</span></span>

### <span data-ttu-id="9b2d3-196">System.object</span><span class="sxs-lookup"><span data-stu-id="9b2d3-196">System.UInt16</span></span>

### <span data-ttu-id="9b2d3-197">System.object</span><span class="sxs-lookup"><span data-stu-id="9b2d3-197">System.Byte</span></span>

## <span data-ttu-id="9b2d3-198">輸出</span><span class="sxs-lookup"><span data-stu-id="9b2d3-198">OUTPUTS</span></span>

### <span data-ttu-id="9b2d3-199">DnsRecordSet （）</span><span class="sxs-lookup"><span data-stu-id="9b2d3-199">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="9b2d3-200">筆記</span><span class="sxs-lookup"><span data-stu-id="9b2d3-200">NOTES</span></span>

## <span data-ttu-id="9b2d3-201">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b2d3-201">RELATED LINKS</span></span>

[<span data-ttu-id="9b2d3-202">附加 AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="9b2d3-202">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="9b2d3-203">AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9b2d3-203">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="9b2d3-204">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9b2d3-204">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
