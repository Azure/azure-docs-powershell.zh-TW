---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/add-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Add-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Add-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: 63e42c7784fe34d726d6f9cb8db987db877c9248
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913353"
---
# <span data-ttu-id="01ca6-101">Add-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="01ca6-101">Add-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="01ca6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="01ca6-102">SYNOPSIS</span></span>
<span data-ttu-id="01ca6-103">新增私人 DNS 記錄至本地記錄集物件。</span><span class="sxs-lookup"><span data-stu-id="01ca6-103">Adds a Private DNS record to a local record set object.</span></span>

## <span data-ttu-id="01ca6-104">語法</span><span class="sxs-lookup"><span data-stu-id="01ca6-104">SYNTAX</span></span>

### <span data-ttu-id="01ca6-105">預設 () </span><span class="sxs-lookup"><span data-stu-id="01ca6-105">A (Default)</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01ca6-106">Aaaa</span><span class="sxs-lookup"><span data-stu-id="01ca6-106">AAAA</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01ca6-107">Mx</span><span class="sxs-lookup"><span data-stu-id="01ca6-107">MX</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01ca6-108">Ptr</span><span class="sxs-lookup"><span data-stu-id="01ca6-108">PTR</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01ca6-109">Txt</span><span class="sxs-lookup"><span data-stu-id="01ca6-109">TXT</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01ca6-110">SRV</span><span class="sxs-lookup"><span data-stu-id="01ca6-110">SRV</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Priority <UInt16> -Target <String>
 -Port <UInt16> -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01ca6-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="01ca6-111">CNAME</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01ca6-112">描述</span><span class="sxs-lookup"><span data-stu-id="01ca6-112">DESCRIPTION</span></span>
<span data-ttu-id="01ca6-113">此Add-AzPrivateDnsRecordConfig Cmdlet 會新增私人網域名稱系統 (DNS) 記錄至 RecordSet 物件。</span><span class="sxs-lookup"><span data-stu-id="01ca6-113">The Add-AzPrivateDnsRecordConfig cmdlet adds a Private Domain Name System (DNS) record to a RecordSet object.</span></span> <span data-ttu-id="01ca6-114">RecordSet 物件是離線物件，而變更不會變更私人 DNS 回應，直到您執行 Set-AzPrivateDnsRecordSet Cmdlet 以將變更持續變更至 Microsoft Azure Private DNS 服務之後。</span><span class="sxs-lookup"><span data-stu-id="01ca6-114">The RecordSet object is an offline object, and changes to it do not change the Private DNS responses until after you run the Set-AzPrivateDnsRecordSet cmdlet to persist the change to the Microsoft Azure Private DNS service.</span></span> <span data-ttu-id="01ca6-115">建立私人 DNS 區域時，會建立 DNS 記錄，而刪除私人 DNS 區域時，會移除這些記錄。</span><span class="sxs-lookup"><span data-stu-id="01ca6-115">SOA records are created when a Private DNS zone is created, and are removed when the Private DNS zone is deleted.</span></span> <span data-ttu-id="01ca6-116">您無法新增或移除 DNS 記錄，但可以編輯記錄。</span><span class="sxs-lookup"><span data-stu-id="01ca6-116">You cannot add or remove SOA records, but you can edit them.</span></span> <span data-ttu-id="01ca6-117">您可以將 RecordSet 物件以參數或管道運算子傳遞至此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="01ca6-117">You can pass the RecordSet object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="01ca6-118">例子</span><span class="sxs-lookup"><span data-stu-id="01ca6-118">EXAMPLES</span></span>

### <span data-ttu-id="01ca6-119">範例 1：新增 A 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="01ca6-119">Example 1: Add an A record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType A -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType A -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="01ca6-120">此範例會將 A 記錄新增到現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="01ca6-120">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="01ca6-121">範例 2：新增 AAAA 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="01ca6-121">Example 2: Add an AAAA record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType AAAAA -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType AAAAA -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="01ca6-122">此範例會將 AAAAA 記錄新增到現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="01ca6-122">This example adds an AAAAA record to an existing record set.</span></span>

### <span data-ttu-id="01ca6-123">範例 3：新增 CNAME 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="01ca6-123">Example 3: Add a CNAME record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType CNAME -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType CNAME -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Cname contoso.com | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="01ca6-124">此範例會將 CNAME 記錄新增到現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="01ca6-124">This example adds a CNAME record to an existing record set.</span></span>

### <span data-ttu-id="01ca6-125">範例 4：新增 MX 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="01ca6-125">Example 4: Add a MX record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name @ -RecordType MX -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="01ca6-126">此範例會將 MX 記錄新增到現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="01ca6-126">This example adds a MX record to an existing record set.</span></span>

### <span data-ttu-id="01ca6-127">範例 5：新增 PTR 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="01ca6-127">Example 5: Add a PTR record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name 4 -RecordType PTR -ResourceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name 4 -RecordType PTR -ResourceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="01ca6-128">此範例會將 PTR 記錄新增到現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="01ca6-128">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="01ca6-129">範例 6：新增 SRV 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="01ca6-129">Example 6: Add a SRV record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name _sip._tcp -RecordType SRV -ResourceGroupName MyResourceGroup-ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name _sip._tcp -RecordType SRV -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="01ca6-130">此範例會將 SRV 記錄新增到現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="01ca6-130">This example adds a SRV record to an existing record set.</span></span>

### <span data-ttu-id="01ca6-131">範例 7：新增 TXT 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="01ca6-131">Example 7: Add a TXT record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name text -RecordType TXT -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name text -RecordType TXT -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Value "This is a TXT Record" | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="01ca6-132">此範例會將 TXT 記錄新增到現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="01ca6-132">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="01ca6-133">參數</span><span class="sxs-lookup"><span data-stu-id="01ca6-133">PARAMETERS</span></span>

### <span data-ttu-id="01ca6-134">-Cname</span><span class="sxs-lookup"><span data-stu-id="01ca6-134">-Cname</span></span>
<span data-ttu-id="01ca6-135">要新增之 CNAME 記錄的正式名稱。</span><span class="sxs-lookup"><span data-stu-id="01ca6-135">The canonical name for the CNAME record to add.</span></span>
<span data-ttu-id="01ca6-136">不得相對於區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="01ca6-136">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="01ca6-137">不得有終止點</span><span class="sxs-lookup"><span data-stu-id="01ca6-137">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="01ca6-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01ca6-138">-DefaultProfile</span></span>
<span data-ttu-id="01ca6-139">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="01ca6-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01ca6-140">-Exchange</span><span class="sxs-lookup"><span data-stu-id="01ca6-140">-Exchange</span></span>
<span data-ttu-id="01ca6-141">要新增 MX 記錄的郵件交換主機。</span><span class="sxs-lookup"><span data-stu-id="01ca6-141">The mail exchange host for the MX record to add.</span></span>
<span data-ttu-id="01ca6-142">不得相對於區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="01ca6-142">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="01ca6-143">不得有終止點</span><span class="sxs-lookup"><span data-stu-id="01ca6-143">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="01ca6-144">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="01ca6-144">-Ipv4Address</span></span>
<span data-ttu-id="01ca6-145">要新增之 A 記錄的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="01ca6-145">The IPv4 address for the A record to add.</span></span>

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

### <span data-ttu-id="01ca6-146">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="01ca6-146">-Ipv6Address</span></span>
<span data-ttu-id="01ca6-147">要新增之 AAAA 記錄的 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="01ca6-147">The IPv6 address for the AAAA record to add.</span></span>

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

### <span data-ttu-id="01ca6-148">-埠</span><span class="sxs-lookup"><span data-stu-id="01ca6-148">-Port</span></span>
<span data-ttu-id="01ca6-149">要新增之 SRV 記錄的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="01ca6-149">The port number for the SRV record to add.</span></span>

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

### <span data-ttu-id="01ca6-150">-喜好設定</span><span class="sxs-lookup"><span data-stu-id="01ca6-150">-Preference</span></span>
<span data-ttu-id="01ca6-151">要新增的 MX 記錄的喜好設定值。</span><span class="sxs-lookup"><span data-stu-id="01ca6-151">The preference value for the MX record to add.</span></span>

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

### <span data-ttu-id="01ca6-152">-優先順序</span><span class="sxs-lookup"><span data-stu-id="01ca6-152">-Priority</span></span>
<span data-ttu-id="01ca6-153">要新增的優先順序值 SRV 記錄。</span><span class="sxs-lookup"><span data-stu-id="01ca6-153">The priority value SRV record to add.</span></span>

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

### <span data-ttu-id="01ca6-154">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="01ca6-154">-Ptrdname</span></span>
<span data-ttu-id="01ca6-155">要新增之 PTR 記錄的目標主機。</span><span class="sxs-lookup"><span data-stu-id="01ca6-155">The target host for the PTR record to add.</span></span>
<span data-ttu-id="01ca6-156">不得相對於區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="01ca6-156">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="01ca6-157">不得有終止點</span><span class="sxs-lookup"><span data-stu-id="01ca6-157">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="01ca6-158">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="01ca6-158">-RecordSet</span></span>
<span data-ttu-id="01ca6-159">要新增記錄的記錄集。</span><span class="sxs-lookup"><span data-stu-id="01ca6-159">The record set in which to add the record.</span></span>

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

### <span data-ttu-id="01ca6-160">-目標</span><span class="sxs-lookup"><span data-stu-id="01ca6-160">-Target</span></span>
<span data-ttu-id="01ca6-161">要新增 SRV 記錄的目標主機。</span><span class="sxs-lookup"><span data-stu-id="01ca6-161">The target host for the SRV record to add.</span></span>
<span data-ttu-id="01ca6-162">不得相對於區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="01ca6-162">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="01ca6-163">不得有終止點</span><span class="sxs-lookup"><span data-stu-id="01ca6-163">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="01ca6-164">-值</span><span class="sxs-lookup"><span data-stu-id="01ca6-164">-Value</span></span>
<span data-ttu-id="01ca6-165">要新增之 TXT 記錄的文字值。</span><span class="sxs-lookup"><span data-stu-id="01ca6-165">The text value for the TXT record to add.</span></span>

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

### <span data-ttu-id="01ca6-166">-重量</span><span class="sxs-lookup"><span data-stu-id="01ca6-166">-Weight</span></span>
<span data-ttu-id="01ca6-167">要新增之 SRV 記錄的粗細值。</span><span class="sxs-lookup"><span data-stu-id="01ca6-167">The weight value for the SRV record to add.</span></span>

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

### <span data-ttu-id="01ca6-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01ca6-168">CommonParameters</span></span>
<span data-ttu-id="01ca6-169">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="01ca6-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01ca6-170">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="01ca6-170">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01ca6-171">輸入</span><span class="sxs-lookup"><span data-stu-id="01ca6-171">INPUTS</span></span>

### <span data-ttu-id="01ca6-172">Microsoft.Azure.Commands.PrivateDns.models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="01ca6-172">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="01ca6-173">輸出</span><span class="sxs-lookup"><span data-stu-id="01ca6-173">OUTPUTS</span></span>

### <span data-ttu-id="01ca6-174">Microsoft.Azure.Commands.PrivateDns.models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="01ca6-174">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="01ca6-175">筆記</span><span class="sxs-lookup"><span data-stu-id="01ca6-175">NOTES</span></span>

## <span data-ttu-id="01ca6-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="01ca6-176">RELATED LINKS</span></span>
