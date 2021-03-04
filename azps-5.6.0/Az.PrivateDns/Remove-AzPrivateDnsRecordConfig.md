---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/remove-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: cd0e2f2913a950e677b1f7294076351556b81c80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915921"
---
# <span data-ttu-id="32a05-101">Remove-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="32a05-101">Remove-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="32a05-102">簡介</span><span class="sxs-lookup"><span data-stu-id="32a05-102">SYNOPSIS</span></span>
<span data-ttu-id="32a05-103">從本地記錄集物件移除私人 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="32a05-103">Removes a Private DNS record from a local record set object.</span></span>

## <span data-ttu-id="32a05-104">語法</span><span class="sxs-lookup"><span data-stu-id="32a05-104">SYNTAX</span></span>

### <span data-ttu-id="32a05-105">預設 () </span><span class="sxs-lookup"><span data-stu-id="32a05-105">A (Default)</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32a05-106">Aaaa</span><span class="sxs-lookup"><span data-stu-id="32a05-106">AAAA</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32a05-107">Mx</span><span class="sxs-lookup"><span data-stu-id="32a05-107">MX</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32a05-108">Ptr</span><span class="sxs-lookup"><span data-stu-id="32a05-108">PTR</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32a05-109">Txt</span><span class="sxs-lookup"><span data-stu-id="32a05-109">TXT</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32a05-110">SRV</span><span class="sxs-lookup"><span data-stu-id="32a05-110">SRV</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Priority <UInt16> -Target <String>
 -Port <UInt16> -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32a05-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="32a05-111">CNAME</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32a05-112">描述</span><span class="sxs-lookup"><span data-stu-id="32a05-112">DESCRIPTION</span></span>
<span data-ttu-id="32a05-113">此Remove-AzPrivateDnsRecordConfig Cmdlet 會從記錄集 (DNS) 私人網域名稱系統。</span><span class="sxs-lookup"><span data-stu-id="32a05-113">The Remove-AzPrivateDnsRecordConfig cmdlet removes a Private Domain Name System (DNS) record from a record set.</span></span> <span data-ttu-id="32a05-114">RecordSet 物件是離線物件，而變更不會變更私人 DNS 回應，直到您執行 Set-AzPrivateDnsRecordSet Cmdlet 以將變更持續變更至 Microsoft Azure Private DNS 服務之後。</span><span class="sxs-lookup"><span data-stu-id="32a05-114">The RecordSet object is an offline object, and changes to it do not change the Private DNS responses until after you run the Set-AzPrivateDnsRecordSet cmdlet to persist the change to the Microsoft Azure Private DNS service.</span></span> <span data-ttu-id="32a05-115">若要移除記錄，該記錄類型的所有欄位必須完全相符。</span><span class="sxs-lookup"><span data-stu-id="32a05-115">To remove a record, all the fields for that record type must match exactly.</span></span> <span data-ttu-id="32a05-116">您無法新增或移除 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="32a05-116">You cannot add or remove SOA records.</span></span> <span data-ttu-id="32a05-117">建立私人 DNS 區域時，會自動建立 DNS 記錄，並會在刪除私人 DNS 區域時自動刪除。</span><span class="sxs-lookup"><span data-stu-id="32a05-117">SOA records are automatically created when a Private DNS zone is created and automatically deleted when the Private DNS zone is deleted.</span></span> <span data-ttu-id="32a05-118">您可以將 RecordSet 物件以參數或管道運算子傳遞至此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="32a05-118">You can pass the RecordSet object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="32a05-119">例子</span><span class="sxs-lookup"><span data-stu-id="32a05-119">EXAMPLES</span></span>

### <span data-ttu-id="32a05-120">範例 1：從記錄集移除記錄</span><span class="sxs-lookup"><span data-stu-id="32a05-120">Example 1: Remove an A record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="32a05-121">此範例會從現有的記錄集移除 A 記錄。</span><span class="sxs-lookup"><span data-stu-id="32a05-121">This example removes an A record from an existing record set.</span></span> <span data-ttu-id="32a05-122">如果這是記錄集的唯一記錄，結果就會是空白的記錄集。</span><span class="sxs-lookup"><span data-stu-id="32a05-122">If this is the only record in the record set, the result will be an empty record set.</span></span> <span data-ttu-id="32a05-123">若要完全移除記錄集，請參閱 Remove-AzPrivateDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="32a05-123">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="32a05-124">範例 2：從記錄集移除 AAAA 記錄</span><span class="sxs-lookup"><span data-stu-id="32a05-124">Example 2: Remove an AAAA record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="32a05-125">此範例會從現有的記錄集移除 AAAA 記錄。</span><span class="sxs-lookup"><span data-stu-id="32a05-125">This example removes an AAAA record from an existing record set.</span></span> <span data-ttu-id="32a05-126">如果這是記錄集的唯一記錄，結果就會是空白的記錄集。</span><span class="sxs-lookup"><span data-stu-id="32a05-126">If this is the only record in the record set, the result will be an empty record set.</span></span> <span data-ttu-id="32a05-127">若要完全移除記錄集，請參閱 Remove-AzPrivateDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="32a05-127">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="32a05-128">範例 3：從記錄集移除 CNAME 記錄</span><span class="sxs-lookup"><span data-stu-id="32a05-128">Example 3: Remove a CNAME record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Cname contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/CNAME/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : CNAME
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="32a05-129">此範例會從現有的記錄集移除 CNAME 記錄。</span><span class="sxs-lookup"><span data-stu-id="32a05-129">This example removes a CNAME record from an existing record set.</span></span> <span data-ttu-id="32a05-130">由於 CNAME 記錄集最多隻能包含一筆記錄，因此結果為空白的記錄集。</span><span class="sxs-lookup"><span data-stu-id="32a05-130">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="32a05-131">範例 4：從記錄集移除 MX 記錄</span><span class="sxs-lookup"><span data-stu-id="32a05-131">Example 4: Remove a MX record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/MX/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : MX
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="32a05-132">此範例會從現有的記錄集移除 MX 記錄。</span><span class="sxs-lookup"><span data-stu-id="32a05-132">This example removes an MX record from an existing record set.</span></span> <span data-ttu-id="32a05-133">記錄名稱 "@" 表示區域頂點的記錄集。</span><span class="sxs-lookup"><span data-stu-id="32a05-133">The record name "@" indicates a record set at the zone apex.</span></span> <span data-ttu-id="32a05-134">如果這是記錄集的唯一記錄，則結果為空白的記錄集。</span><span class="sxs-lookup"><span data-stu-id="32a05-134">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="32a05-135">若要完全移除記錄集，請參閱 Remove-AzPrivateDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="32a05-135">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="32a05-136">範例 5：從記錄集移除 PTR 記錄</span><span class="sxs-lookup"><span data-stu-id="32a05-136">Example 5: Remove a PTR record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/3.2.1.in-addr.arpa/PTR/4
Name              : 4
ZoneName          : 3.2.1.in-addr.arpa
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : PTR
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="32a05-137">此範例會從現有的記錄集移除 PTR 記錄。</span><span class="sxs-lookup"><span data-stu-id="32a05-137">This example removes a PTR record from an existing record set.</span></span> <span data-ttu-id="32a05-138">如果這是記錄集的唯一記錄，則結果為空白的記錄集。</span><span class="sxs-lookup"><span data-stu-id="32a05-138">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="32a05-139">若要完全移除記錄集，請參閱 Remove-AzPrivateDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="32a05-139">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="32a05-140">範例 6：從記錄集移除 SRV 記錄</span><span class="sxs-lookup"><span data-stu-id="32a05-140">Example 6: Remove a SRV record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SRV/_sip._tcp
Name              : _sip._tcp
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SRV
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="32a05-141">此範例會從現有的記錄集移除 SRV 記錄。</span><span class="sxs-lookup"><span data-stu-id="32a05-141">This example removes an SRV record from an existing record set.</span></span> <span data-ttu-id="32a05-142">如果這是記錄集的唯一記錄，則結果為空白的記錄集。</span><span class="sxs-lookup"><span data-stu-id="32a05-142">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="32a05-143">若要完全移除記錄集，請參閱 Remove-AzPrivateDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="32a05-143">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="32a05-144">範例 7：從記錄集移除 TXT 記錄</span><span class="sxs-lookup"><span data-stu-id="32a05-144">Example 7: Remove a TXT record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Value "This is a TXT Record"  | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/TXT/text
Name              : text
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : TXT
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="32a05-145">此範例會從現有的記錄集移除 TXT 記錄。</span><span class="sxs-lookup"><span data-stu-id="32a05-145">This example removes a TXT record from an existing record set.</span></span> <span data-ttu-id="32a05-146">如果這是記錄集的唯一記錄，則結果為空白的記錄集。</span><span class="sxs-lookup"><span data-stu-id="32a05-146">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="32a05-147">若要完全移除記錄集，請參閱 Remove-AzPrivateDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="32a05-147">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

## <span data-ttu-id="32a05-148">參數</span><span class="sxs-lookup"><span data-stu-id="32a05-148">PARAMETERS</span></span>

### <span data-ttu-id="32a05-149">-Cname</span><span class="sxs-lookup"><span data-stu-id="32a05-149">-Cname</span></span>
<span data-ttu-id="32a05-150">要移除之 CNAME 記錄的正式名稱。</span><span class="sxs-lookup"><span data-stu-id="32a05-150">The canonical name of the CNAME record to remove.</span></span>
<span data-ttu-id="32a05-151">不得相對於區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="32a05-151">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="32a05-152">不得有終止點</span><span class="sxs-lookup"><span data-stu-id="32a05-152">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="32a05-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32a05-153">-DefaultProfile</span></span>
<span data-ttu-id="32a05-154">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="32a05-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32a05-155">-Exchange</span><span class="sxs-lookup"><span data-stu-id="32a05-155">-Exchange</span></span>
<span data-ttu-id="32a05-156">要移除的 MX 記錄的郵件交換主機。</span><span class="sxs-lookup"><span data-stu-id="32a05-156">The mail exchange host of the MX record to remove.</span></span>
<span data-ttu-id="32a05-157">不得相對於區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="32a05-157">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="32a05-158">不得有終止點</span><span class="sxs-lookup"><span data-stu-id="32a05-158">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="32a05-159">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="32a05-159">-Ipv4Address</span></span>
<span data-ttu-id="32a05-160">要移除之 A 記錄的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="32a05-160">The IPv4 address of the A record to remove.</span></span>

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

### <span data-ttu-id="32a05-161">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="32a05-161">-Ipv6Address</span></span>
<span data-ttu-id="32a05-162">要移除之 AAAA 記錄的 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="32a05-162">The IPv6 address of the AAAA record to remove.</span></span>

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

### <span data-ttu-id="32a05-163">-埠</span><span class="sxs-lookup"><span data-stu-id="32a05-163">-Port</span></span>
<span data-ttu-id="32a05-164">要移除的 SRV 記錄的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="32a05-164">The port number of the SRV record to remove.</span></span>

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

### <span data-ttu-id="32a05-165">-喜好設定</span><span class="sxs-lookup"><span data-stu-id="32a05-165">-Preference</span></span>
<span data-ttu-id="32a05-166">要移除的 MX 記錄的喜好設定值。</span><span class="sxs-lookup"><span data-stu-id="32a05-166">The preference value of the MX record to remove.</span></span>

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

### <span data-ttu-id="32a05-167">-優先順序</span><span class="sxs-lookup"><span data-stu-id="32a05-167">-Priority</span></span>
<span data-ttu-id="32a05-168">要移除之 SRV 記錄的優先順序值。</span><span class="sxs-lookup"><span data-stu-id="32a05-168">The priority value of the SRV record to remove.</span></span>

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

### <span data-ttu-id="32a05-169">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="32a05-169">-Ptrdname</span></span>
<span data-ttu-id="32a05-170">要移除之 PTR 記錄的目標主機。</span><span class="sxs-lookup"><span data-stu-id="32a05-170">The target host of the PTR record to remove.</span></span>
<span data-ttu-id="32a05-171">不得相對於區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="32a05-171">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="32a05-172">不得有終止點</span><span class="sxs-lookup"><span data-stu-id="32a05-172">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="32a05-173">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="32a05-173">-RecordSet</span></span>
<span data-ttu-id="32a05-174">移除記錄的記錄集。</span><span class="sxs-lookup"><span data-stu-id="32a05-174">The record set from which to remove the record.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32a05-175">-目標</span><span class="sxs-lookup"><span data-stu-id="32a05-175">-Target</span></span>
<span data-ttu-id="32a05-176">要移除之 SRV 記錄的目標主機。</span><span class="sxs-lookup"><span data-stu-id="32a05-176">The target host of the SRV record to remove.</span></span>
<span data-ttu-id="32a05-177">不得相對於區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="32a05-177">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="32a05-178">不得有終止點</span><span class="sxs-lookup"><span data-stu-id="32a05-178">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="32a05-179">-值</span><span class="sxs-lookup"><span data-stu-id="32a05-179">-Value</span></span>
<span data-ttu-id="32a05-180">要移除之 TXT 記錄的文字值。</span><span class="sxs-lookup"><span data-stu-id="32a05-180">The text value of the TXT record to remove.</span></span>

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

### <span data-ttu-id="32a05-181">-重量</span><span class="sxs-lookup"><span data-stu-id="32a05-181">-Weight</span></span>
<span data-ttu-id="32a05-182">要移除之 SRV 記錄的粗細值。</span><span class="sxs-lookup"><span data-stu-id="32a05-182">The weight value of the SRV record to remove.</span></span>

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

### <span data-ttu-id="32a05-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32a05-183">CommonParameters</span></span>
<span data-ttu-id="32a05-184">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="32a05-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32a05-185">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="32a05-185">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32a05-186">輸入</span><span class="sxs-lookup"><span data-stu-id="32a05-186">INPUTS</span></span>

### <span data-ttu-id="32a05-187">Microsoft.Azure.Commands.PrivateDns.models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="32a05-187">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="32a05-188">輸出</span><span class="sxs-lookup"><span data-stu-id="32a05-188">OUTPUTS</span></span>

### <span data-ttu-id="32a05-189">Microsoft.Azure.Commands.PrivateDns.models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="32a05-189">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="32a05-190">筆記</span><span class="sxs-lookup"><span data-stu-id="32a05-190">NOTES</span></span>

## <span data-ttu-id="32a05-191">相關連結</span><span class="sxs-lookup"><span data-stu-id="32a05-191">RELATED LINKS</span></span>
