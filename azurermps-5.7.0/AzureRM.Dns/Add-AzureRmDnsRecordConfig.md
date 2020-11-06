---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/add-azurermdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Add-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Add-AzureRmDnsRecordConfig.md
ms.openlocfilehash: c9e824160b04b183414c6b99fce4b09b6d70766a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447095"
---
# <span data-ttu-id="dcbc9-101">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="dcbc9-101">Add-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="dcbc9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dcbc9-102">SYNOPSIS</span></span>
<span data-ttu-id="dcbc9-103">將 DNS 記錄新增到本機記錄集物件。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-103">Adds a DNS record to a local record set object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcbc9-104">句法</span><span class="sxs-lookup"><span data-stu-id="dcbc9-104">SYNTAX</span></span>

### <span data-ttu-id="dcbc9-105">是</span><span class="sxs-lookup"><span data-stu-id="dcbc9-105">A</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcbc9-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="dcbc9-106">AAAA</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcbc9-107">NS</span><span class="sxs-lookup"><span data-stu-id="dcbc9-107">NS</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcbc9-108">MX</span><span class="sxs-lookup"><span data-stu-id="dcbc9-108">MX</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcbc9-109">PTR</span><span class="sxs-lookup"><span data-stu-id="dcbc9-109">PTR</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcbc9-110">文字檔</span><span class="sxs-lookup"><span data-stu-id="dcbc9-110">TXT</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dcbc9-111">DNS-SRV</span><span class="sxs-lookup"><span data-stu-id="dcbc9-111">SRV</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcbc9-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="dcbc9-112">CNAME</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dcbc9-113">Caa</span><span class="sxs-lookup"><span data-stu-id="dcbc9-113">Caa</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcbc9-114">說明</span><span class="sxs-lookup"><span data-stu-id="dcbc9-114">DESCRIPTION</span></span>
<span data-ttu-id="dcbc9-115">**AzureRmDnsRecordConfig** Cmdlet 會將網域名稱系統 (DNS) 記錄新增至 **RecordSet** 物件。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-115">The **Add-AzureRmDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="dcbc9-116">**RecordSet** 物件是離線物件，而且在您執行 Set-AzureRmDnsRecordSet Cmdlet 以保留 MICROSOFT Azure DNS 服務的變更之後，才能變更 DNS 回應。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="dcbc9-117">SOA 記錄是在建立 DNS 區域時建立，而且會在刪除 DNS 區域時移除。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-117">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="dcbc9-118">您無法新增或移除 SOA 記錄，但您可以進行編輯。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-118">You cannot add or remove SOA records, but you can edit them.</span></span>

<span data-ttu-id="dcbc9-119">您可以將 **RecordSet** 物件作為參數傳遞給這個 Cmdlet，或使用管線運算子。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="dcbc9-120">示例</span><span class="sxs-lookup"><span data-stu-id="dcbc9-120">EXAMPLES</span></span>

### <span data-ttu-id="dcbc9-121">範例1：將 A 記錄新增至記錄集</span><span class="sxs-lookup"><span data-stu-id="dcbc9-121">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="dcbc9-122">這個範例會將 A 記錄新增至現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-122">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="dcbc9-123">範例2：新增 AAAA 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="dcbc9-123">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="dcbc9-124">這個範例會將 AAAA 記錄新增至現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-124">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="dcbc9-125">範例3：新增 CNAME 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="dcbc9-125">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Cname contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="dcbc9-126">這個範例會在現有的記錄集中加入 CNAME 記錄。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-126">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="dcbc9-127">因為 CNAME 記錄集最多可以包含一筆記錄，所以它必須是空記錄集，或必須使用 AzureRmDnsRecordConfig 移除現有的記錄。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-127">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzureRmDnsRecordConfig.</span></span>

### <span data-ttu-id="dcbc9-128">範例4：新增 MX 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="dcbc9-128">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="dcbc9-129">這個範例會將 MX 記錄新增至現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-129">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="dcbc9-130">記錄名稱 "@" 代表在區域 apex 上設定的記錄。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-130">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="dcbc9-131">範例5：將 NS 記錄新增至記錄集</span><span class="sxs-lookup"><span data-stu-id="dcbc9-131">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="dcbc9-132">這個範例會將 NS 記錄新增至現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-132">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="dcbc9-133">範例6：將 PTR 記錄新增至記錄集</span><span class="sxs-lookup"><span data-stu-id="dcbc9-133">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="dcbc9-134">這個範例會將 PTR 記錄新增至現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-134">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="dcbc9-135">範例7：將 SRV 記錄新增至記錄集</span><span class="sxs-lookup"><span data-stu-id="dcbc9-135">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="dcbc9-136">這個範例會將 SRV 記錄新增至現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-136">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="dcbc9-137">範例8：新增 TXT 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="dcbc9-137">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Value "This is a TXT Record" | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="dcbc9-138">這個範例會將 TXT 記錄新增至現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-138">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="dcbc9-139">參數</span><span class="sxs-lookup"><span data-stu-id="dcbc9-139">PARAMETERS</span></span>

### <span data-ttu-id="dcbc9-140">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="dcbc9-140">-CaaFlags</span></span>
<span data-ttu-id="dcbc9-141">要新增之 CAA 記錄的旗標。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-141">The flags for the CAA record to add.</span></span> <span data-ttu-id="dcbc9-142">必須是介於0與255之間的數位。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-142">Must be a number between 0 and 255.</span></span>

```yaml
Type: Byte
Parameter Sets: Caa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcbc9-143">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="dcbc9-143">-CaaTag</span></span>
<span data-ttu-id="dcbc9-144">要新增之 CAA 記錄的 tag 欄位。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-144">The tag field of the CAA record to add.</span></span>

```yaml
Type: String
Parameter Sets: Caa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcbc9-145">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="dcbc9-145">-CaaValue</span></span>
<span data-ttu-id="dcbc9-146">要新增之 CAA 記錄的 [值] 欄位。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-146">The value field for the CAA record to add.</span></span>

```yaml
Type: String
Parameter Sets: Caa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcbc9-147">-Cname</span><span class="sxs-lookup"><span data-stu-id="dcbc9-147">-Cname</span></span>
<span data-ttu-id="dcbc9-148">指定正常化) 記錄 (CNAME 名稱的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-148">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="dcbc9-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcbc9-149">-DefaultProfile</span></span>
<span data-ttu-id="dcbc9-150">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="dcbc9-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcbc9-151">-Exchange</span><span class="sxs-lookup"><span data-stu-id="dcbc9-151">-Exchange</span></span>
<span data-ttu-id="dcbc9-152">指定郵件交換 (MX) 記錄的郵件交換伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-152">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="dcbc9-153">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="dcbc9-153">-Ipv4Address</span></span>
<span data-ttu-id="dcbc9-154">指定 A 記錄的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-154">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="dcbc9-155">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="dcbc9-155">-Ipv6Address</span></span>
<span data-ttu-id="dcbc9-156">指定 AAAA 記錄的 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-156">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="dcbc9-157">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="dcbc9-157">-Nsdname</span></span>
<span data-ttu-id="dcbc9-158">指定 name server (NS) 記錄的名稱伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-158">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="dcbc9-159">-埠</span><span class="sxs-lookup"><span data-stu-id="dcbc9-159">-Port</span></span>
<span data-ttu-id="dcbc9-160">指定服務 (SRV) 記錄的埠。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-160">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="dcbc9-161">-喜好設定</span><span class="sxs-lookup"><span data-stu-id="dcbc9-161">-Preference</span></span>
<span data-ttu-id="dcbc9-162">指定 MX 記錄的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-162">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="dcbc9-163">-優先順序</span><span class="sxs-lookup"><span data-stu-id="dcbc9-163">-Priority</span></span>
<span data-ttu-id="dcbc9-164">指定 SRV 記錄的優先順序。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-164">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="dcbc9-165">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="dcbc9-165">-Ptrdname</span></span>
<span data-ttu-id="dcbc9-166">指定指標資源的目標功能變數名稱 (PTR) 記錄。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-166">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="dcbc9-167">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="dcbc9-167">-RecordSet</span></span>
<span data-ttu-id="dcbc9-168">指定要編輯的 **記錄集** 物件。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-168">Specifies the **RecordSet** object to edit.</span></span>

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

### <span data-ttu-id="dcbc9-169">-目標</span><span class="sxs-lookup"><span data-stu-id="dcbc9-169">-Target</span></span>
<span data-ttu-id="dcbc9-170">指定 SRV 記錄的目標。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-170">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="dcbc9-171">-值</span><span class="sxs-lookup"><span data-stu-id="dcbc9-171">-Value</span></span>
<span data-ttu-id="dcbc9-172">指定 TXT 記錄的值。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-172">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="dcbc9-173">寬度</span><span class="sxs-lookup"><span data-stu-id="dcbc9-173">-Weight</span></span>
<span data-ttu-id="dcbc9-174">指定 SRV 記錄的權重。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-174">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="dcbc9-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcbc9-175">CommonParameters</span></span>
<span data-ttu-id="dcbc9-176">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcbc9-177">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcbc9-178">輸入</span><span class="sxs-lookup"><span data-stu-id="dcbc9-178">INPUTS</span></span>

### <span data-ttu-id="dcbc9-179">DnsRecordSet （）</span><span class="sxs-lookup"><span data-stu-id="dcbc9-179">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="dcbc9-180">您可以將 **RecordSet** 物件輸送到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-180">You can pipe a **RecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="dcbc9-181">這是 **記錄集** 的離線表示形式，在您執行 Set-AzureRmDnsRecordSet Cmdlet 之後，才能變更 DNS 回應。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-181">This is an offline representation of the **RecordSet** , and changes to it do not change DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet.</span></span>

## <span data-ttu-id="dcbc9-182">輸出</span><span class="sxs-lookup"><span data-stu-id="dcbc9-182">OUTPUTS</span></span>

### <span data-ttu-id="dcbc9-183">DnsRecordSet （）</span><span class="sxs-lookup"><span data-stu-id="dcbc9-183">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="dcbc9-184">這個 Cmdlet 會傳回修改過的 **RecordSet** 物件。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-184">This cmdlet returns the modified **RecordSet** object.</span></span>
<span data-ttu-id="dcbc9-185">此外，會直接修改傳入的物件。</span><span class="sxs-lookup"><span data-stu-id="dcbc9-185">In addition, the object passed in is modified directly.</span></span>

## <span data-ttu-id="dcbc9-186">筆記</span><span class="sxs-lookup"><span data-stu-id="dcbc9-186">NOTES</span></span>

## <span data-ttu-id="dcbc9-187">相關連結</span><span class="sxs-lookup"><span data-stu-id="dcbc9-187">RELATED LINKS</span></span>

[<span data-ttu-id="dcbc9-188">AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="dcbc9-188">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="dcbc9-189">移除-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="dcbc9-189">Remove-AzureRmDnsRecordConfig</span></span>](./Remove-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="dcbc9-190">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="dcbc9-190">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
