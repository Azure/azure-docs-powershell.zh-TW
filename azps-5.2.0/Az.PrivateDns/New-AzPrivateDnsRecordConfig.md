---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: f828c422447768ff59aea413eeca036a60877b09
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278556"
---
# <span data-ttu-id="d976b-101">New-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="d976b-101">New-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="d976b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d976b-102">SYNOPSIS</span></span>
<span data-ttu-id="d976b-103">建立新的私人 DNS 記錄本機物件。</span><span class="sxs-lookup"><span data-stu-id="d976b-103">Creates a new Private DNS record local object.</span></span>

## <span data-ttu-id="d976b-104">句法</span><span class="sxs-lookup"><span data-stu-id="d976b-104">SYNTAX</span></span>

### <span data-ttu-id="d976b-105"> (預設) </span><span class="sxs-lookup"><span data-stu-id="d976b-105">A (Default)</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d976b-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="d976b-106">AAAA</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d976b-107">MX</span><span class="sxs-lookup"><span data-stu-id="d976b-107">MX</span></span>
```
New-AzPrivateDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d976b-108">PTR</span><span class="sxs-lookup"><span data-stu-id="d976b-108">PTR</span></span>
```
New-AzPrivateDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d976b-109">文字檔</span><span class="sxs-lookup"><span data-stu-id="d976b-109">TXT</span></span>
```
New-AzPrivateDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d976b-110">DNS-SRV</span><span class="sxs-lookup"><span data-stu-id="d976b-110">SRV</span></span>
```
New-AzPrivateDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d976b-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="d976b-111">CNAME</span></span>
```
New-AzPrivateDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d976b-112">說明</span><span class="sxs-lookup"><span data-stu-id="d976b-112">DESCRIPTION</span></span>
<span data-ttu-id="d976b-113">New-AzPrivateDnsRecordConfig Cmdlet 會建立本機 PSPrivateDnsRecord 物件。</span><span class="sxs-lookup"><span data-stu-id="d976b-113">The New-AzPrivateDnsRecordConfig cmdlet creates a local PSPrivateDnsRecord object.</span></span> <span data-ttu-id="d976b-114">這些物件的陣列會使用 PrivateDnsRecord 參數傳遞到 New-AzPrivateDnsRecordSet Cmdlet，以指定要在記錄集中建立的記錄。</span><span class="sxs-lookup"><span data-stu-id="d976b-114">An array of these objects is passed to the New-AzPrivateDnsRecordSet cmdlet using the PrivateDnsRecord parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="d976b-115">示例</span><span class="sxs-lookup"><span data-stu-id="d976b-115">EXAMPLES</span></span>

### <span data-ttu-id="d976b-116">範例1：建立 A 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="d976b-116">Example 1: Create a RecordSet of type A</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4)

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :


# To create a record set containing multiple records, use New-AzPrivateDnsRecordConfig to add each record to the $Records array,
# then call New-AzPrivateDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4, 5.6.7.8}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="d976b-117">這個範例會在 [私人區域 myzone.com] 中建立名為「www」的記錄集。</span><span class="sxs-lookup"><span data-stu-id="d976b-117">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="d976b-118">記錄集的類型是 A，且每個小時的 TTL (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="d976b-118">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="d976b-119">它包含單一的私人 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="d976b-119">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="d976b-120">範例2：建立 AAAA 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="d976b-120">Example 2: Create a RecordSet of type AAAA</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:db8::1}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="d976b-121">這個範例會在 [私人區域 myzone.com] 中建立名為「www」的記錄集。</span><span class="sxs-lookup"><span data-stu-id="d976b-121">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="d976b-122">記錄集的類型是 AAAA，且每個小時的 TTL (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="d976b-122">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="d976b-123">它包含單一的私人 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="d976b-123">It contains a single Private DNS record.</span></span> <span data-ttu-id="d976b-124">若要建立只使用一行 pn_PowerShell_short 的記錄集，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="d976b-124">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d976b-125">範例3：建立 CNAME 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="d976b-125">Example 3: Create a RecordSet of type CNAME</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/CNAME/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : CNAME
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="d976b-126">這個範例會在 [私人區域 myzone.com] 中建立名為「www」的記錄集。</span><span class="sxs-lookup"><span data-stu-id="d976b-126">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="d976b-127">此記錄集的類型為 CNAME，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="d976b-127">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="d976b-128">它包含單一的私人 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="d976b-128">It contains a single Private DNS record.</span></span> <span data-ttu-id="d976b-129">若要建立只使用一行 pn_PowerShell_short 的記錄集，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="d976b-129">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d976b-130">範例4：建立 MX 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="d976b-130">Example 4: Create a RecordSet of type MX</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/MX/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : MX
Records           : {[5,mail.microsoft.com]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="d976b-131">這個命令會在 [私人區域 myzone.com] 中建立一個名為「www」的記錄集。</span><span class="sxs-lookup"><span data-stu-id="d976b-131">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="d976b-132">記錄集的類型是 MX，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="d976b-132">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="d976b-133">它包含單一的私人 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="d976b-133">It contains a single Private DNS record.</span></span> <span data-ttu-id="d976b-134">若要建立只使用一行 pn_PowerShell_short 的記錄集，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="d976b-134">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d976b-135">範例5：建立類型指標的記錄集</span><span class="sxs-lookup"><span data-stu-id="d976b-135">Example 5: Create a RecordSet of type PTR</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/3.2.1.in-addr.arpa/PTR/4
Name              : 4
ZoneName          : 3.2.1.in-addr.arpa
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : PTR
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="d976b-136">這個命令會在私人區域3.2.1.in （arpa）中建立名為4的記錄集。</span><span class="sxs-lookup"><span data-stu-id="d976b-136">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="d976b-137">記錄集的類型是 PTR，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="d976b-137">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="d976b-138">它包含單一的私人 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="d976b-138">It contains a single Private DNS record.</span></span> <span data-ttu-id="d976b-139">若要建立只使用一行 pn_PowerShell_short 的記錄集，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="d976b-139">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d976b-140">範例6：建立 SRV 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="d976b-140">Example 6: Create a RecordSet of type SRV</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SRV/_sip._tcp
Name              : _sip._tcp
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SRV
Records           : {[0,5,8080,sipservice.contoso.com]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="d976b-141">這個命令會在 [私人區域 myzone.com] 中建立名為 _sip 的記錄集。</span><span class="sxs-lookup"><span data-stu-id="d976b-141">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="d976b-142">記錄集的類型為 SRV，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="d976b-142">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="d976b-143">它包含一個私有 DNS 記錄，並指向 IP 位址2001.2.3.4。</span><span class="sxs-lookup"><span data-stu-id="d976b-143">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="d976b-144">服務 (sip) ，而 (tcp) 的通訊協定，則會指定為記錄集名稱的一部分，而不是記錄資料的一部分。</span><span class="sxs-lookup"><span data-stu-id="d976b-144">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="d976b-145">若要建立只使用一行 pn_PowerShell_short 的記錄集，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="d976b-145">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d976b-146">範例7：建立 TXT 類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="d976b-146">Example 7: Create a RecordSet of type TXT</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/TXT/text
Name              : text
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : TXT
Records           : {This is a TXT Record}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="d976b-147">這個命令會在 [私人區域 myzone.com] 中建立名為「文字」的記錄集。</span><span class="sxs-lookup"><span data-stu-id="d976b-147">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="d976b-148">記錄集的類型為 TXT，且每個小時 (3600 秒) 。</span><span class="sxs-lookup"><span data-stu-id="d976b-148">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="d976b-149">它包含單一的私人 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="d976b-149">It contains a single Private DNS record.</span></span> <span data-ttu-id="d976b-150">若要建立只使用一行 pn_PowerShell_short 的記錄集，或建立包含多筆記錄的記錄集，請參閱範例1。</span><span class="sxs-lookup"><span data-stu-id="d976b-150">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="d976b-151">參數</span><span class="sxs-lookup"><span data-stu-id="d976b-151">PARAMETERS</span></span>

### <span data-ttu-id="d976b-152">-Cname</span><span class="sxs-lookup"><span data-stu-id="d976b-152">-Cname</span></span>
<span data-ttu-id="d976b-153">要新增之 CNAME 記錄的正式名稱。</span><span class="sxs-lookup"><span data-stu-id="d976b-153">The canonical name for the CNAME record to add.</span></span>
<span data-ttu-id="d976b-154">不得與區功能變數名稱稱相關。</span><span class="sxs-lookup"><span data-stu-id="d976b-154">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="d976b-155">不能有終止點</span><span class="sxs-lookup"><span data-stu-id="d976b-155">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: CNAME
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d976b-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d976b-156">-DefaultProfile</span></span>
<span data-ttu-id="d976b-157">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d976b-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d976b-158">-Exchange</span><span class="sxs-lookup"><span data-stu-id="d976b-158">-Exchange</span></span>
<span data-ttu-id="d976b-159">要新增之 MX 記錄的郵件交換主機。</span><span class="sxs-lookup"><span data-stu-id="d976b-159">The mail exchange host for the MX record to add.</span></span>
<span data-ttu-id="d976b-160">不得與區功能變數名稱稱相關。</span><span class="sxs-lookup"><span data-stu-id="d976b-160">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="d976b-161">不能有終止點</span><span class="sxs-lookup"><span data-stu-id="d976b-161">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d976b-162">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="d976b-162">-Ipv4Address</span></span>
<span data-ttu-id="d976b-163">要新增之 A 記錄的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="d976b-163">The IPv4 address for the A record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: A
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d976b-164">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="d976b-164">-Ipv6Address</span></span>
<span data-ttu-id="d976b-165">要新增之 AAAA 記錄的 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="d976b-165">The IPv6 address for the AAAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AAAA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d976b-166">-埠</span><span class="sxs-lookup"><span data-stu-id="d976b-166">-Port</span></span>
<span data-ttu-id="d976b-167">要新增之 SRV 記錄的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="d976b-167">The port number for the SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d976b-168">-喜好設定</span><span class="sxs-lookup"><span data-stu-id="d976b-168">-Preference</span></span>
<span data-ttu-id="d976b-169">要新增之 MX 記錄的喜好設定值。</span><span class="sxs-lookup"><span data-stu-id="d976b-169">The preference value for the MX record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d976b-170">-優先順序</span><span class="sxs-lookup"><span data-stu-id="d976b-170">-Priority</span></span>
<span data-ttu-id="d976b-171">要新增的優先順序值 SRV 記錄。</span><span class="sxs-lookup"><span data-stu-id="d976b-171">The priority value SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d976b-172">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="d976b-172">-Ptrdname</span></span>
<span data-ttu-id="d976b-173">要新增之 PTR 記錄的目標主機。</span><span class="sxs-lookup"><span data-stu-id="d976b-173">The target host for the PTR record to add.</span></span>
<span data-ttu-id="d976b-174">不得與區功能變數名稱稱相關。</span><span class="sxs-lookup"><span data-stu-id="d976b-174">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="d976b-175">不能有終止點</span><span class="sxs-lookup"><span data-stu-id="d976b-175">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: PTR
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d976b-176">-目標</span><span class="sxs-lookup"><span data-stu-id="d976b-176">-Target</span></span>
<span data-ttu-id="d976b-177">要新增之 SRV 記錄的目標主機。</span><span class="sxs-lookup"><span data-stu-id="d976b-177">The target host for the SRV record to add.</span></span>
<span data-ttu-id="d976b-178">不得與區功能變數名稱稱相關。</span><span class="sxs-lookup"><span data-stu-id="d976b-178">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="d976b-179">不能有終止點</span><span class="sxs-lookup"><span data-stu-id="d976b-179">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d976b-180">-值</span><span class="sxs-lookup"><span data-stu-id="d976b-180">-Value</span></span>
<span data-ttu-id="d976b-181">要新增之 TXT 記錄的文字值。</span><span class="sxs-lookup"><span data-stu-id="d976b-181">The text value for the TXT record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: TXT
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d976b-182">寬度</span><span class="sxs-lookup"><span data-stu-id="d976b-182">-Weight</span></span>
<span data-ttu-id="d976b-183">要新增之 SRV 記錄的 [體重] 值。</span><span class="sxs-lookup"><span data-stu-id="d976b-183">The weight value for the SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d976b-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d976b-184">CommonParameters</span></span>
<span data-ttu-id="d976b-185">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d976b-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d976b-186">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d976b-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d976b-187">輸入</span><span class="sxs-lookup"><span data-stu-id="d976b-187">INPUTS</span></span>

### <span data-ttu-id="d976b-188">所有</span><span class="sxs-lookup"><span data-stu-id="d976b-188">None</span></span>

## <span data-ttu-id="d976b-189">輸出</span><span class="sxs-lookup"><span data-stu-id="d976b-189">OUTPUTS</span></span>

### <span data-ttu-id="d976b-190">PSPrivateDnsRecordSet 中的 PrivateDns。</span><span class="sxs-lookup"><span data-stu-id="d976b-190">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="d976b-191">筆記</span><span class="sxs-lookup"><span data-stu-id="d976b-191">NOTES</span></span>

## <span data-ttu-id="d976b-192">相關連結</span><span class="sxs-lookup"><span data-stu-id="d976b-192">RELATED LINKS</span></span>
