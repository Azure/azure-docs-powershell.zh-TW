---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/add-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Add-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Add-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: a6150f6f54db57abbcd643c99729d41254db7d27
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139507"
---
# <span data-ttu-id="53a39-101">Add-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="53a39-101">Add-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="53a39-102">摘要</span><span class="sxs-lookup"><span data-stu-id="53a39-102">SYNOPSIS</span></span>
<span data-ttu-id="53a39-103">將私人 DNS 記錄新增到本機記錄集物件。</span><span class="sxs-lookup"><span data-stu-id="53a39-103">Adds a Private DNS record to a local record set object.</span></span>

## <span data-ttu-id="53a39-104">句法</span><span class="sxs-lookup"><span data-stu-id="53a39-104">SYNTAX</span></span>

### <span data-ttu-id="53a39-105"> (預設) </span><span class="sxs-lookup"><span data-stu-id="53a39-105">A (Default)</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53a39-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="53a39-106">AAAA</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53a39-107">MX</span><span class="sxs-lookup"><span data-stu-id="53a39-107">MX</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53a39-108">PTR</span><span class="sxs-lookup"><span data-stu-id="53a39-108">PTR</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53a39-109">文字檔</span><span class="sxs-lookup"><span data-stu-id="53a39-109">TXT</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53a39-110">DNS-SRV</span><span class="sxs-lookup"><span data-stu-id="53a39-110">SRV</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Priority <UInt16> -Target <String>
 -Port <UInt16> -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53a39-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="53a39-111">CNAME</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53a39-112">說明</span><span class="sxs-lookup"><span data-stu-id="53a39-112">DESCRIPTION</span></span>
<span data-ttu-id="53a39-113">Add-AzPrivateDnsRecordConfig Cmdlet 會將私人網功能變數名稱稱系統 (DNS) 記錄新增至 RecordSet 物件。</span><span class="sxs-lookup"><span data-stu-id="53a39-113">The Add-AzPrivateDnsRecordConfig cmdlet adds a Private Domain Name System (DNS) record to a RecordSet object.</span></span> <span data-ttu-id="53a39-114">RecordSet 物件是離線物件，而對它所做的變更不會變更私人 DNS 回應，除非您執行 Set-AzPrivateDnsRecordSet Cmdlet，才能保留 Microsoft Azure 私人 DNS 服務的變更。</span><span class="sxs-lookup"><span data-stu-id="53a39-114">The RecordSet object is an offline object, and changes to it do not change the Private DNS responses until after you run the Set-AzPrivateDnsRecordSet cmdlet to persist the change to the Microsoft Azure Private DNS service.</span></span> <span data-ttu-id="53a39-115">SOA 記錄是在建立私人 DNS 區域時建立，而且會在刪除 [私人 DNS 區域] 時移除。</span><span class="sxs-lookup"><span data-stu-id="53a39-115">SOA records are created when a Private DNS zone is created, and are removed when the Private DNS zone is deleted.</span></span> <span data-ttu-id="53a39-116">您無法新增或移除 SOA 記錄，但您可以進行編輯。</span><span class="sxs-lookup"><span data-stu-id="53a39-116">You cannot add or remove SOA records, but you can edit them.</span></span> <span data-ttu-id="53a39-117">您可以將 RecordSet 物件作為參數傳遞給這個 Cmdlet，或使用管線運算子。</span><span class="sxs-lookup"><span data-stu-id="53a39-117">You can pass the RecordSet object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="53a39-118">示例</span><span class="sxs-lookup"><span data-stu-id="53a39-118">EXAMPLES</span></span>

### <span data-ttu-id="53a39-119">範例1：將 A 記錄新增至記錄集</span><span class="sxs-lookup"><span data-stu-id="53a39-119">Example 1: Add an A record to a record set</span></span>
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

<span data-ttu-id="53a39-120">這個範例會將 A 記錄新增至現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="53a39-120">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="53a39-121">範例2：新增 AAAA 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="53a39-121">Example 2: Add an AAAA record to a record set</span></span>
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

<span data-ttu-id="53a39-122">這個範例會將 AAAAA 記錄新增至現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="53a39-122">This example adds an AAAAA record to an existing record set.</span></span>

### <span data-ttu-id="53a39-123">範例3：新增 CNAME 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="53a39-123">Example 3: Add a CNAME record to a record set</span></span>
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

<span data-ttu-id="53a39-124">這個範例會在現有的記錄集中加入 CNAME 記錄。</span><span class="sxs-lookup"><span data-stu-id="53a39-124">This example adds a CNAME record to an existing record set.</span></span>

### <span data-ttu-id="53a39-125">範例4：新增 MX 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="53a39-125">Example 4: Add a MX record to a record set</span></span>
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

<span data-ttu-id="53a39-126">這個範例會將 MX 記錄新增至現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="53a39-126">This example adds a MX record to an existing record set.</span></span>

### <span data-ttu-id="53a39-127">範例5：將 PTR 記錄新增至記錄集</span><span class="sxs-lookup"><span data-stu-id="53a39-127">Example 5: Add a PTR record to a record set</span></span>
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

<span data-ttu-id="53a39-128">這個範例會將 PTR 記錄新增至現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="53a39-128">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="53a39-129">範例6：將 SRV 記錄新增至記錄集</span><span class="sxs-lookup"><span data-stu-id="53a39-129">Example 6: Add a SRV record to a record set</span></span>
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

<span data-ttu-id="53a39-130">這個範例會將 SRV 記錄新增至現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="53a39-130">This example adds a SRV record to an existing record set.</span></span>

### <span data-ttu-id="53a39-131">範例7：新增 TXT 記錄至記錄集</span><span class="sxs-lookup"><span data-stu-id="53a39-131">Example 7: Add a TXT record to a record set</span></span>
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

<span data-ttu-id="53a39-132">這個範例會將 TXT 記錄新增至現有的記錄集。</span><span class="sxs-lookup"><span data-stu-id="53a39-132">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="53a39-133">參數</span><span class="sxs-lookup"><span data-stu-id="53a39-133">PARAMETERS</span></span>

### <span data-ttu-id="53a39-134">-Cname</span><span class="sxs-lookup"><span data-stu-id="53a39-134">-Cname</span></span>
<span data-ttu-id="53a39-135">要新增之 CNAME 記錄的正式名稱。</span><span class="sxs-lookup"><span data-stu-id="53a39-135">The canonical name for the CNAME record to add.</span></span>
<span data-ttu-id="53a39-136">不得與區功能變數名稱稱相關。</span><span class="sxs-lookup"><span data-stu-id="53a39-136">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="53a39-137">不能有終止點</span><span class="sxs-lookup"><span data-stu-id="53a39-137">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="53a39-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53a39-138">-DefaultProfile</span></span>
<span data-ttu-id="53a39-139">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="53a39-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53a39-140">-Exchange</span><span class="sxs-lookup"><span data-stu-id="53a39-140">-Exchange</span></span>
<span data-ttu-id="53a39-141">要新增之 MX 記錄的郵件交換主機。</span><span class="sxs-lookup"><span data-stu-id="53a39-141">The mail exchange host for the MX record to add.</span></span>
<span data-ttu-id="53a39-142">不得與區功能變數名稱稱相關。</span><span class="sxs-lookup"><span data-stu-id="53a39-142">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="53a39-143">不能有終止點</span><span class="sxs-lookup"><span data-stu-id="53a39-143">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="53a39-144">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="53a39-144">-Ipv4Address</span></span>
<span data-ttu-id="53a39-145">要新增之 A 記錄的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="53a39-145">The IPv4 address for the A record to add.</span></span>

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

### <span data-ttu-id="53a39-146">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="53a39-146">-Ipv6Address</span></span>
<span data-ttu-id="53a39-147">要新增之 AAAA 記錄的 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="53a39-147">The IPv6 address for the AAAA record to add.</span></span>

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

### <span data-ttu-id="53a39-148">-埠</span><span class="sxs-lookup"><span data-stu-id="53a39-148">-Port</span></span>
<span data-ttu-id="53a39-149">要新增之 SRV 記錄的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="53a39-149">The port number for the SRV record to add.</span></span>

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

### <span data-ttu-id="53a39-150">-喜好設定</span><span class="sxs-lookup"><span data-stu-id="53a39-150">-Preference</span></span>
<span data-ttu-id="53a39-151">要新增之 MX 記錄的喜好設定值。</span><span class="sxs-lookup"><span data-stu-id="53a39-151">The preference value for the MX record to add.</span></span>

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

### <span data-ttu-id="53a39-152">-優先順序</span><span class="sxs-lookup"><span data-stu-id="53a39-152">-Priority</span></span>
<span data-ttu-id="53a39-153">要新增的優先順序值 SRV 記錄。</span><span class="sxs-lookup"><span data-stu-id="53a39-153">The priority value SRV record to add.</span></span>

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

### <span data-ttu-id="53a39-154">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="53a39-154">-Ptrdname</span></span>
<span data-ttu-id="53a39-155">要新增之 PTR 記錄的目標主機。</span><span class="sxs-lookup"><span data-stu-id="53a39-155">The target host for the PTR record to add.</span></span>
<span data-ttu-id="53a39-156">不得與區功能變數名稱稱相關。</span><span class="sxs-lookup"><span data-stu-id="53a39-156">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="53a39-157">不能有終止點</span><span class="sxs-lookup"><span data-stu-id="53a39-157">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="53a39-158">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="53a39-158">-RecordSet</span></span>
<span data-ttu-id="53a39-159">要在其中新增記錄的記錄集。</span><span class="sxs-lookup"><span data-stu-id="53a39-159">The record set in which to add the record.</span></span>

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

### <span data-ttu-id="53a39-160">-目標</span><span class="sxs-lookup"><span data-stu-id="53a39-160">-Target</span></span>
<span data-ttu-id="53a39-161">要新增之 SRV 記錄的目標主機。</span><span class="sxs-lookup"><span data-stu-id="53a39-161">The target host for the SRV record to add.</span></span>
<span data-ttu-id="53a39-162">不得與區功能變數名稱稱相關。</span><span class="sxs-lookup"><span data-stu-id="53a39-162">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="53a39-163">不能有終止點</span><span class="sxs-lookup"><span data-stu-id="53a39-163">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="53a39-164">-值</span><span class="sxs-lookup"><span data-stu-id="53a39-164">-Value</span></span>
<span data-ttu-id="53a39-165">要新增之 TXT 記錄的文字值。</span><span class="sxs-lookup"><span data-stu-id="53a39-165">The text value for the TXT record to add.</span></span>

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

### <span data-ttu-id="53a39-166">寬度</span><span class="sxs-lookup"><span data-stu-id="53a39-166">-Weight</span></span>
<span data-ttu-id="53a39-167">要新增之 SRV 記錄的 [體重] 值。</span><span class="sxs-lookup"><span data-stu-id="53a39-167">The weight value for the SRV record to add.</span></span>

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

### <span data-ttu-id="53a39-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53a39-168">CommonParameters</span></span>
<span data-ttu-id="53a39-169">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="53a39-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53a39-170">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="53a39-170">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53a39-171">輸入</span><span class="sxs-lookup"><span data-stu-id="53a39-171">INPUTS</span></span>

### <span data-ttu-id="53a39-172">PSPrivateDnsRecordSet 中的 PrivateDns。</span><span class="sxs-lookup"><span data-stu-id="53a39-172">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="53a39-173">輸出</span><span class="sxs-lookup"><span data-stu-id="53a39-173">OUTPUTS</span></span>

### <span data-ttu-id="53a39-174">PSPrivateDnsRecordSet 中的 PrivateDns。</span><span class="sxs-lookup"><span data-stu-id="53a39-174">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="53a39-175">筆記</span><span class="sxs-lookup"><span data-stu-id="53a39-175">NOTES</span></span>

## <span data-ttu-id="53a39-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="53a39-176">RELATED LINKS</span></span>
