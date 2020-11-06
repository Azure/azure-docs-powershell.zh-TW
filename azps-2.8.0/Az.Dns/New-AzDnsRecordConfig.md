---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
ms.openlocfilehash: d31bc3b2d250010bd359a3fda03cbd7788c49c86
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612501"
---
# <span data-ttu-id="1fdc3-101">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="1fdc3-101">New-AzDnsRecordConfig</span></span>

## <span data-ttu-id="1fdc3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1fdc3-102">SYNOPSIS</span></span>
<span data-ttu-id="1fdc3-103">建立新的 DNS 記錄本機物件。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-103">Creates a new DNS record local object.</span></span>

## <span data-ttu-id="1fdc3-104">句法</span><span class="sxs-lookup"><span data-stu-id="1fdc3-104">SYNTAX</span></span>

### <span data-ttu-id="1fdc3-105">是</span><span class="sxs-lookup"><span data-stu-id="1fdc3-105">A</span></span>
```
New-AzDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fdc3-106">Aaaa</span><span class="sxs-lookup"><span data-stu-id="1fdc3-106">Aaaa</span></span>
```
New-AzDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fdc3-107">Ns</span><span class="sxs-lookup"><span data-stu-id="1fdc3-107">Ns</span></span>
```
New-AzDnsRecordConfig -Nsdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fdc3-108">Mx</span><span class="sxs-lookup"><span data-stu-id="1fdc3-108">Mx</span></span>
```
New-AzDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1fdc3-109">Ptr</span><span class="sxs-lookup"><span data-stu-id="1fdc3-109">Ptr</span></span>
```
New-AzDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fdc3-110">文字檔</span><span class="sxs-lookup"><span data-stu-id="1fdc3-110">Txt</span></span>
```
New-AzDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fdc3-111">Dns-srv</span><span class="sxs-lookup"><span data-stu-id="1fdc3-111">Srv</span></span>
```
New-AzDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fdc3-112">CName</span><span class="sxs-lookup"><span data-stu-id="1fdc3-112">CName</span></span>
```
New-AzDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fdc3-113">Caa</span><span class="sxs-lookup"><span data-stu-id="1fdc3-113">Caa</span></span>
```
New-AzDnsRecordConfig -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fdc3-114">說明</span><span class="sxs-lookup"><span data-stu-id="1fdc3-114">DESCRIPTION</span></span>
<span data-ttu-id="1fdc3-115">**新的-AzDnsRecordConfig** Cmdlet 會建立本機 **DnsRecord** 物件。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-115">The **New-AzDnsRecordConfig** cmdlet creates a local **DnsRecord** object.</span></span>
<span data-ttu-id="1fdc3-116">這些物件的陣列會使用 *DnsRecords* 參數傳遞到 New-AzDnsRecordSet Cmdlet，以指定要在記錄集中建立的記錄。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-116">An array of these objects is passed to the New-AzDnsRecordSet cmdlet using the *DnsRecords* parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="1fdc3-117">示例</span><span class="sxs-lookup"><span data-stu-id="1fdc3-117">EXAMPLES</span></span>

### <span data-ttu-id="1fdc3-118">範例1：建立 A 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="1fdc3-118">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="1fdc3-119">這個範例會在區域 myzone.com 中建立名為 www 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-119">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="1fdc3-120">記錄集的類型是 A，且每個小時的 TTL (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="1fdc3-121">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-121">It contains a single DNS record.</span></span>

### <span data-ttu-id="1fdc3-122">範例2：建立 AAAA 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="1fdc3-122">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="1fdc3-123">這個範例會在區域 myzone.com 中建立名為 www 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-123">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="1fdc3-124">記錄集的類型是 AAAA，且每個小時的 TTL (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="1fdc3-125">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-125">It contains a single DNS record.</span></span>
<span data-ttu-id="1fdc3-126">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-126">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="1fdc3-127">範例3：建立 CNAME 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="1fdc3-127">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="1fdc3-128">這個範例會在區域 myzone.com 中建立名為 www 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-128">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="1fdc3-129">此記錄集的類型為 CNAME，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="1fdc3-130">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-130">It contains a single DNS record.</span></span>
<span data-ttu-id="1fdc3-131">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-131">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="1fdc3-132">範例4：建立 MX 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="1fdc3-132">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="1fdc3-133">這個命令會在區域 myzone.com 中建立名為 www 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-133">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="1fdc3-134">記錄集的類型是 MX，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="1fdc3-135">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-135">It contains a single DNS record.</span></span>
<span data-ttu-id="1fdc3-136">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-136">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="1fdc3-137">範例5：建立 NS 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="1fdc3-137">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="1fdc3-138">這個命令會在區域 myzone.com 中建立一個名為 ns1 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-138">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="1fdc3-139">記錄集的類型是 NS，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-139">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="1fdc3-140">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-140">It contains a single DNS record.</span></span>
<span data-ttu-id="1fdc3-141">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-141">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="1fdc3-142">範例6：建立類型指標的記錄集</span><span class="sxs-lookup"><span data-stu-id="1fdc3-142">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="1fdc3-143">這個命令會在 zone 3.2.1.in-arpa 中建立名為4的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-143">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="1fdc3-144">記錄集的類型是 PTR，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-144">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="1fdc3-145">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-145">It contains a single DNS record.</span></span>
<span data-ttu-id="1fdc3-146">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-146">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="1fdc3-147">範例7：建立 SRV 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="1fdc3-147">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="1fdc3-148">這個命令會在區域 myzone.com 中建立名為 _sip 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-148">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="1fdc3-149">記錄集的類型為 SRV，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-149">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="1fdc3-150">它包含單一 DNS 記錄，並指向 IP 位址2001.2.3.4。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-150">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="1fdc3-151">服務 (sip) ，而 (tcp) 的通訊協定，則會指定為記錄集名稱的一部分，而不是記錄資料的一部分。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-151">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="1fdc3-152">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-152">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="1fdc3-153">範例8：建立 TXT 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="1fdc3-153">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="1fdc3-154">這個命令會在區域 myzone.com 中建立名為 text 的 **記錄集** 。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-154">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="1fdc3-155">記錄集的類型為 TXT，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-155">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="1fdc3-156">它包含單一的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-156">It contains a single DNS record.</span></span>
<span data-ttu-id="1fdc3-157">若要建立只使用一行 pn_PowerShell_short 的 **記錄集** ，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-157">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="1fdc3-158">參數</span><span class="sxs-lookup"><span data-stu-id="1fdc3-158">PARAMETERS</span></span>

### <span data-ttu-id="1fdc3-159">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="1fdc3-159">-CaaFlags</span></span>
<span data-ttu-id="1fdc3-160">要新增之 CAA 記錄的旗標。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-160">The flags for the CAA record to add.</span></span> <span data-ttu-id="1fdc3-161">必須是介於0與255之間的數位。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-161">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="1fdc3-162">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="1fdc3-162">-CaaTag</span></span>
<span data-ttu-id="1fdc3-163">要新增之 CAA 記錄的 tag 欄位。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-163">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="1fdc3-164">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="1fdc3-164">-CaaValue</span></span>
<span data-ttu-id="1fdc3-165">要新增之 CAA 記錄的 [值] 欄位。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-165">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="1fdc3-166">-Cname</span><span class="sxs-lookup"><span data-stu-id="1fdc3-166">-Cname</span></span>
<span data-ttu-id="1fdc3-167">指定正常化) 記錄 (CNAME 名稱的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-167">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: System.String
Parameter Sets: CName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fdc3-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fdc3-168">-DefaultProfile</span></span>
<span data-ttu-id="1fdc3-169">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1fdc3-169">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1fdc3-170">-Exchange</span><span class="sxs-lookup"><span data-stu-id="1fdc3-170">-Exchange</span></span>
<span data-ttu-id="1fdc3-171">指定郵件交換 (MX) 記錄的郵件交換伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-171">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: System.String
Parameter Sets: Mx
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fdc3-172">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="1fdc3-172">-Ipv4Address</span></span>
<span data-ttu-id="1fdc3-173">指定 A 記錄的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-173">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="1fdc3-174">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="1fdc3-174">-Ipv6Address</span></span>
<span data-ttu-id="1fdc3-175">指定 AAAA 記錄的 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-175">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: System.String
Parameter Sets: Aaaa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fdc3-176">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="1fdc3-176">-Nsdname</span></span>
<span data-ttu-id="1fdc3-177">指定 name server (NS) 記錄的名稱伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-177">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: System.String
Parameter Sets: Ns
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fdc3-178">-埠</span><span class="sxs-lookup"><span data-stu-id="1fdc3-178">-Port</span></span>
<span data-ttu-id="1fdc3-179">指定服務 (SRV) 記錄的埠。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-179">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fdc3-180">-喜好設定</span><span class="sxs-lookup"><span data-stu-id="1fdc3-180">-Preference</span></span>
<span data-ttu-id="1fdc3-181">指定 MX 記錄的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-181">Specifies the preference for an MX record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Mx
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fdc3-182">-優先順序</span><span class="sxs-lookup"><span data-stu-id="1fdc3-182">-Priority</span></span>
<span data-ttu-id="1fdc3-183">指定 SRV 記錄的優先順序。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-183">Specifies the priority for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fdc3-184">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="1fdc3-184">-Ptrdname</span></span>
<span data-ttu-id="1fdc3-185">指定指標資源的目標功能變數名稱 (PTR) 記錄。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-185">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: System.String
Parameter Sets: Ptr
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fdc3-186">-目標</span><span class="sxs-lookup"><span data-stu-id="1fdc3-186">-Target</span></span>
<span data-ttu-id="1fdc3-187">指定 SRV 記錄的目標。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-187">Specifies the target for an SRV record.</span></span>

```yaml
Type: System.String
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fdc3-188">-值</span><span class="sxs-lookup"><span data-stu-id="1fdc3-188">-Value</span></span>
<span data-ttu-id="1fdc3-189">指定 TXT 記錄的值。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-189">Specifies the value for a TXT record.</span></span>

```yaml
Type: System.String
Parameter Sets: Txt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fdc3-190">寬度</span><span class="sxs-lookup"><span data-stu-id="1fdc3-190">-Weight</span></span>
<span data-ttu-id="1fdc3-191">指定 SRV 記錄的權重。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-191">Specifies the weight for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fdc3-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fdc3-192">CommonParameters</span></span>
<span data-ttu-id="1fdc3-193">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fdc3-194">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1fdc3-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fdc3-195">輸入</span><span class="sxs-lookup"><span data-stu-id="1fdc3-195">INPUTS</span></span>

### <span data-ttu-id="1fdc3-196">System.object</span><span class="sxs-lookup"><span data-stu-id="1fdc3-196">System.String</span></span>

### <span data-ttu-id="1fdc3-197">System.object</span><span class="sxs-lookup"><span data-stu-id="1fdc3-197">System.UInt16</span></span>

### <span data-ttu-id="1fdc3-198">System.object</span><span class="sxs-lookup"><span data-stu-id="1fdc3-198">System.Byte</span></span>

## <span data-ttu-id="1fdc3-199">輸出</span><span class="sxs-lookup"><span data-stu-id="1fdc3-199">OUTPUTS</span></span>

### <span data-ttu-id="1fdc3-200">DnsRecordBase （）</span><span class="sxs-lookup"><span data-stu-id="1fdc3-200">Microsoft.Azure.Commands.Dns.DnsRecordBase</span></span>

## <span data-ttu-id="1fdc3-201">筆記</span><span class="sxs-lookup"><span data-stu-id="1fdc3-201">NOTES</span></span>

## <span data-ttu-id="1fdc3-202">相關連結</span><span class="sxs-lookup"><span data-stu-id="1fdc3-202">RELATED LINKS</span></span>

[<span data-ttu-id="1fdc3-203">附加 AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="1fdc3-203">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="1fdc3-204">新-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1fdc3-204">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="1fdc3-205">移除-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="1fdc3-205">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)