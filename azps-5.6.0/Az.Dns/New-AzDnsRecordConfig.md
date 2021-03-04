---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/powershell/module/az.dns/new-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
ms.openlocfilehash: c85cc0b4ad60529cc57becb9ca864751d90a37c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910138"
---
# <span data-ttu-id="11e2d-101">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="11e2d-101">New-AzDnsRecordConfig</span></span>

## <span data-ttu-id="11e2d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="11e2d-102">SYNOPSIS</span></span>
<span data-ttu-id="11e2d-103">建立新的 DNS 記錄本機物件。</span><span class="sxs-lookup"><span data-stu-id="11e2d-103">Creates a new DNS record local object.</span></span>

## <span data-ttu-id="11e2d-104">語法</span><span class="sxs-lookup"><span data-stu-id="11e2d-104">SYNTAX</span></span>

### <span data-ttu-id="11e2d-105">A</span><span class="sxs-lookup"><span data-stu-id="11e2d-105">A</span></span>
```
New-AzDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11e2d-106">Aaaa</span><span class="sxs-lookup"><span data-stu-id="11e2d-106">Aaaa</span></span>
```
New-AzDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11e2d-107">Ns</span><span class="sxs-lookup"><span data-stu-id="11e2d-107">Ns</span></span>
```
New-AzDnsRecordConfig -Nsdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11e2d-108">Mx</span><span class="sxs-lookup"><span data-stu-id="11e2d-108">Mx</span></span>
```
New-AzDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="11e2d-109">Ptr</span><span class="sxs-lookup"><span data-stu-id="11e2d-109">Ptr</span></span>
```
New-AzDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11e2d-110">Txt</span><span class="sxs-lookup"><span data-stu-id="11e2d-110">Txt</span></span>
```
New-AzDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11e2d-111">Srv</span><span class="sxs-lookup"><span data-stu-id="11e2d-111">Srv</span></span>
```
New-AzDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11e2d-112">CName</span><span class="sxs-lookup"><span data-stu-id="11e2d-112">CName</span></span>
```
New-AzDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11e2d-113">Caa</span><span class="sxs-lookup"><span data-stu-id="11e2d-113">Caa</span></span>
```
New-AzDnsRecordConfig -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11e2d-114">描述</span><span class="sxs-lookup"><span data-stu-id="11e2d-114">DESCRIPTION</span></span>
<span data-ttu-id="11e2d-115">**New-AzDnsRecordConfig** Cmdlet 會建立一個本地 **DnsRecord** 物件。</span><span class="sxs-lookup"><span data-stu-id="11e2d-115">The **New-AzDnsRecordConfig** cmdlet creates a local **DnsRecord** object.</span></span>
<span data-ttu-id="11e2d-116">這些物件的陣列會傳遞至 New-AzDnsRecordSet Cmdlet，使用 *DnsRecords* 參數指定要于記錄集建立的記錄。</span><span class="sxs-lookup"><span data-stu-id="11e2d-116">An array of these objects is passed to the New-AzDnsRecordSet cmdlet using the *DnsRecords* parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="11e2d-117">例子</span><span class="sxs-lookup"><span data-stu-id="11e2d-117">EXAMPLES</span></span>

### <span data-ttu-id="11e2d-118">範例 1：建立類型 A 的 RecordSet</span><span class="sxs-lookup"><span data-stu-id="11e2d-118">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="11e2d-119">此範例在 myzone.com 區域中建立名為 www 的 **RecordSet。**</span><span class="sxs-lookup"><span data-stu-id="11e2d-119">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="11e2d-120">記錄集的類型為 A，TTL 為 1 小時， (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="11e2d-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="11e2d-121">它包含單一 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="11e2d-121">It contains a single DNS record.</span></span>

### <span data-ttu-id="11e2d-122">範例 2：建立類型 AAAA 的 RecordSet</span><span class="sxs-lookup"><span data-stu-id="11e2d-122">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="11e2d-123">此範例在 myzone.com 區域中建立名為 www 的 **RecordSet。**</span><span class="sxs-lookup"><span data-stu-id="11e2d-123">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="11e2d-124">記錄集的類型為 AAAA，TTL 為 1 小時， (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="11e2d-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="11e2d-125">它包含單一 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="11e2d-125">It contains a single DNS record.</span></span>
<span data-ttu-id="11e2d-126">若要使用一行記錄來建立 **記錄** 集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。</span><span class="sxs-lookup"><span data-stu-id="11e2d-126">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="11e2d-127">範例 3：建立類型 CNAME 的 RecordSet</span><span class="sxs-lookup"><span data-stu-id="11e2d-127">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="11e2d-128">此範例在 myzone.com 區域中建立名為 www 的 **RecordSet。**</span><span class="sxs-lookup"><span data-stu-id="11e2d-128">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="11e2d-129">記錄集的類型為 CNAME，TTL 為 1 小時， (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="11e2d-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="11e2d-130">它包含單一 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="11e2d-130">It contains a single DNS record.</span></span>
<span data-ttu-id="11e2d-131">若要使用一行記錄來建立 **記錄** 集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。</span><span class="sxs-lookup"><span data-stu-id="11e2d-131">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="11e2d-132">範例 4：建立類型 MX 的 RecordSet</span><span class="sxs-lookup"><span data-stu-id="11e2d-132">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="11e2d-133">此命令在 myzone.com 區域中建立名為 www 的 **RecordSet。**</span><span class="sxs-lookup"><span data-stu-id="11e2d-133">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="11e2d-134">記錄集的類型為 MX，TTL 為 1 小時， (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="11e2d-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="11e2d-135">它包含單一 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="11e2d-135">It contains a single DNS record.</span></span>
<span data-ttu-id="11e2d-136">若要使用一行記錄來建立 **記錄** 集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。</span><span class="sxs-lookup"><span data-stu-id="11e2d-136">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="11e2d-137">範例 5：建立類型 NS 的 RecordSet</span><span class="sxs-lookup"><span data-stu-id="11e2d-137">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="11e2d-138">此命令在活動區域建立名為 ns1 的 **RecordSet** myzone.com。</span><span class="sxs-lookup"><span data-stu-id="11e2d-138">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="11e2d-139">記錄集的類型為 NS，TTL 為 1 小時， (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="11e2d-139">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="11e2d-140">它包含單一 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="11e2d-140">It contains a single DNS record.</span></span>
<span data-ttu-id="11e2d-141">若要使用一行記錄來建立 **記錄** 集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。</span><span class="sxs-lookup"><span data-stu-id="11e2d-141">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="11e2d-142">範例 6：建立類型 PTR 的 RecordSet</span><span class="sxs-lookup"><span data-stu-id="11e2d-142">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="11e2d-143">此命令在 3.2.1.in-addr.arpa 區域中建立名為 4 的 RecordSet。</span><span class="sxs-lookup"><span data-stu-id="11e2d-143">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="11e2d-144">記錄集的類型為 PTR，且 TTL 為 1 小時， (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="11e2d-144">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="11e2d-145">它包含單一 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="11e2d-145">It contains a single DNS record.</span></span>
<span data-ttu-id="11e2d-146">若要使用一行記錄來建立 **記錄** 集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。</span><span class="sxs-lookup"><span data-stu-id="11e2d-146">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="11e2d-147">範例 7：建立類型 SRV 的 RecordSet</span><span class="sxs-lookup"><span data-stu-id="11e2d-147">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="11e2d-148">此命令會建立一個名為 _sip._tcp 的 **RecordSet，myzone.com。**</span><span class="sxs-lookup"><span data-stu-id="11e2d-148">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="11e2d-149">記錄集的類型為 SRV，TTL 為 1 小時， (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="11e2d-149">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="11e2d-150">它包含指向 IP 位址 2001.2.3.4 的單一 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="11e2d-150">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="11e2d-151">服務 (sip) 和 (tcp) 會指定為記錄集名稱的一部分，而不是記錄資料的一部分。</span><span class="sxs-lookup"><span data-stu-id="11e2d-151">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="11e2d-152">若要使用一行記錄來建立 **記錄** 集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。</span><span class="sxs-lookup"><span data-stu-id="11e2d-152">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="11e2d-153">範例 8：建立類型 TXT 的 RecordSet</span><span class="sxs-lookup"><span data-stu-id="11e2d-153">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="11e2d-154">此命令會在這個區域中建立名為文字的 **RecordSet** myzone.com。</span><span class="sxs-lookup"><span data-stu-id="11e2d-154">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="11e2d-155">記錄集的類型為 TXT，TTL 為 1 小時， (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="11e2d-155">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="11e2d-156">它包含單一 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="11e2d-156">It contains a single DNS record.</span></span>
<span data-ttu-id="11e2d-157">若要使用一行記錄來建立 **記錄** 集pn_PowerShell_short或建立包含多個記錄的記錄集，請參閱範例 1。</span><span class="sxs-lookup"><span data-stu-id="11e2d-157">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="11e2d-158">參數</span><span class="sxs-lookup"><span data-stu-id="11e2d-158">PARAMETERS</span></span>

### <span data-ttu-id="11e2d-159">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="11e2d-159">-CaaFlags</span></span>
<span data-ttu-id="11e2d-160">要新增之 CAA 記錄的標標。</span><span class="sxs-lookup"><span data-stu-id="11e2d-160">The flags for the CAA record to add.</span></span> <span data-ttu-id="11e2d-161">必須是介於 0 到 255 之間的數位。</span><span class="sxs-lookup"><span data-stu-id="11e2d-161">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="11e2d-162">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="11e2d-162">-CaaTag</span></span>
<span data-ttu-id="11e2d-163">要新增之 CAA 記錄的標記欄位。</span><span class="sxs-lookup"><span data-stu-id="11e2d-163">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="11e2d-164">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="11e2d-164">-CaaValue</span></span>
<span data-ttu-id="11e2d-165">要新增之 CAA 記錄的值欄位。</span><span class="sxs-lookup"><span data-stu-id="11e2d-165">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="11e2d-166">-Cname</span><span class="sxs-lookup"><span data-stu-id="11e2d-166">-Cname</span></span>
<span data-ttu-id="11e2d-167">指定 CNAME 記錄中標準名稱 (功能變數名稱) 名稱。</span><span class="sxs-lookup"><span data-stu-id="11e2d-167">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="11e2d-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11e2d-168">-DefaultProfile</span></span>
<span data-ttu-id="11e2d-169">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="11e2d-169">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11e2d-170">-Exchange</span><span class="sxs-lookup"><span data-stu-id="11e2d-170">-Exchange</span></span>
<span data-ttu-id="11e2d-171">指定 MX 記錄中郵件交換 (伺服器) 名稱。</span><span class="sxs-lookup"><span data-stu-id="11e2d-171">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="11e2d-172">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="11e2d-172">-Ipv4Address</span></span>
<span data-ttu-id="11e2d-173">指定 A 記錄的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="11e2d-173">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="11e2d-174">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="11e2d-174">-Ipv6Address</span></span>
<span data-ttu-id="11e2d-175">指定 AAAA 記錄的 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="11e2d-175">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="11e2d-176">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="11e2d-176">-Nsdname</span></span>
<span data-ttu-id="11e2d-177">指定名稱伺服器的名稱伺服器名稱 (NS) 記錄。</span><span class="sxs-lookup"><span data-stu-id="11e2d-177">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="11e2d-178">-埠</span><span class="sxs-lookup"><span data-stu-id="11e2d-178">-Port</span></span>
<span data-ttu-id="11e2d-179">指定 SRV 記錄中 (的) 埠。</span><span class="sxs-lookup"><span data-stu-id="11e2d-179">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="11e2d-180">-喜好設定</span><span class="sxs-lookup"><span data-stu-id="11e2d-180">-Preference</span></span>
<span data-ttu-id="11e2d-181">指定 MX 記錄的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="11e2d-181">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="11e2d-182">-優先順序</span><span class="sxs-lookup"><span data-stu-id="11e2d-182">-Priority</span></span>
<span data-ttu-id="11e2d-183">指定 SRV 記錄的優先順序。</span><span class="sxs-lookup"><span data-stu-id="11e2d-183">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="11e2d-184">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="11e2d-184">-Ptrdname</span></span>
<span data-ttu-id="11e2d-185">指定 PTR 記錄中指標資源 (功能變數名稱) 名稱。</span><span class="sxs-lookup"><span data-stu-id="11e2d-185">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="11e2d-186">-目標</span><span class="sxs-lookup"><span data-stu-id="11e2d-186">-Target</span></span>
<span data-ttu-id="11e2d-187">指定 SRV 記錄的目標。</span><span class="sxs-lookup"><span data-stu-id="11e2d-187">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="11e2d-188">-值</span><span class="sxs-lookup"><span data-stu-id="11e2d-188">-Value</span></span>
<span data-ttu-id="11e2d-189">指定 TXT 記錄的值。</span><span class="sxs-lookup"><span data-stu-id="11e2d-189">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="11e2d-190">-重量</span><span class="sxs-lookup"><span data-stu-id="11e2d-190">-Weight</span></span>
<span data-ttu-id="11e2d-191">指定 SRV 記錄的粗細。</span><span class="sxs-lookup"><span data-stu-id="11e2d-191">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="11e2d-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11e2d-192">CommonParameters</span></span>
<span data-ttu-id="11e2d-193">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="11e2d-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11e2d-194">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="11e2d-194">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11e2d-195">輸入</span><span class="sxs-lookup"><span data-stu-id="11e2d-195">INPUTS</span></span>

### <span data-ttu-id="11e2d-196">System.String</span><span class="sxs-lookup"><span data-stu-id="11e2d-196">System.String</span></span>

### <span data-ttu-id="11e2d-197">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="11e2d-197">System.UInt16</span></span>

### <span data-ttu-id="11e2d-198">System.Byte</span><span class="sxs-lookup"><span data-stu-id="11e2d-198">System.Byte</span></span>

## <span data-ttu-id="11e2d-199">輸出</span><span class="sxs-lookup"><span data-stu-id="11e2d-199">OUTPUTS</span></span>

### <span data-ttu-id="11e2d-200">Microsoft.Azure.Commands.dns.DnsRecordBase</span><span class="sxs-lookup"><span data-stu-id="11e2d-200">Microsoft.Azure.Commands.Dns.DnsRecordBase</span></span>

## <span data-ttu-id="11e2d-201">筆記</span><span class="sxs-lookup"><span data-stu-id="11e2d-201">NOTES</span></span>

## <span data-ttu-id="11e2d-202">相關連結</span><span class="sxs-lookup"><span data-stu-id="11e2d-202">RELATED LINKS</span></span>

[<span data-ttu-id="11e2d-203">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="11e2d-203">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="11e2d-204">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="11e2d-204">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="11e2d-205">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="11e2d-205">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)
