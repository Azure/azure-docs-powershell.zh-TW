---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: 7e1ea1213759e9c4edf9524a36637aff1ef1c12b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795685"
---
# <span data-ttu-id="0645a-101">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0645a-101">Get-AzDnsRecordSet</span></span>

## <span data-ttu-id="0645a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0645a-102">SYNOPSIS</span></span>
<span data-ttu-id="0645a-103">取得 DNS 記錄集。</span><span class="sxs-lookup"><span data-stu-id="0645a-103">Gets a DNS record set.</span></span>

## <span data-ttu-id="0645a-104">句法</span><span class="sxs-lookup"><span data-stu-id="0645a-104">SYNTAX</span></span>

### <span data-ttu-id="0645a-105">區域</span><span class="sxs-lookup"><span data-stu-id="0645a-105">Fields</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String>
 [-RecordType <RecordType>] [<CommonParameters>]
```

### <span data-ttu-id="0645a-106">面向</span><span class="sxs-lookup"><span data-stu-id="0645a-106">Object</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>] [<CommonParameters>]
```

## <span data-ttu-id="0645a-107">說明</span><span class="sxs-lookup"><span data-stu-id="0645a-107">DESCRIPTION</span></span>
<span data-ttu-id="0645a-108">**AzDnsRecordSet** Cmdlet 會在指定的區域中，以指定的名稱與類型來取得網功能變數名稱稱系統 (DNS) 記錄集。</span><span class="sxs-lookup"><span data-stu-id="0645a-108">The **Get-AzDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>

<span data-ttu-id="0645a-109">如果您沒有指定 *Name* 或 *RecordType* 參數，這個 Cmdlet 會傳回區域中指定類型的所有記錄集。</span><span class="sxs-lookup"><span data-stu-id="0645a-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="0645a-110">如果您指定 *RecordType* 參數而不是 *Name* 參數，這個 Cmdlet 會傳回指定記錄類型的所有記錄集。</span><span class="sxs-lookup"><span data-stu-id="0645a-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>

<span data-ttu-id="0645a-111">您可以使用管線運算子，將 **DnsZone** 物件傳遞到這個 Cmdlet，或者您可以將 **DnsZone** 物件傳遞為 *zone* 參數，或者也可以依名稱指定區域和資源群組。</span><span class="sxs-lookup"><span data-stu-id="0645a-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="0645a-112">示例</span><span class="sxs-lookup"><span data-stu-id="0645a-112">EXAMPLES</span></span>

### <span data-ttu-id="0645a-113">範例1：取得具有指定名稱和類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="0645a-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="0645a-114">這個命令會在指定的資源群組和區域中取得一組記錄類型的記錄，並將它儲存在 $RecordSet 變數中。</span><span class="sxs-lookup"><span data-stu-id="0645a-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="0645a-115">因為已指定 *Name* 和 *RecordType* 參數，所以只會傳回一個 **記錄集** 物件。</span><span class="sxs-lookup"><span data-stu-id="0645a-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="0645a-116">範例2：取得指定類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="0645a-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="0645a-117">這個命令會在名為 [MyResourceGroup] 的資源群組中，從名為「myzone.com」的區域中取得記錄類型 A 之所有記錄集的陣列，然後將它們儲存在 $RecordSets 變數中。</span><span class="sxs-lookup"><span data-stu-id="0645a-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="0645a-118">範例3：取得區域中的所有記錄集</span><span class="sxs-lookup"><span data-stu-id="0645a-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="0645a-119">這個命令會在名為 MyResourceGroup 的資源群組中，從名為 myzone.com 的區域中取得所有記錄集的陣列，然後將它們儲存在 $RecordSets 變數中。</span><span class="sxs-lookup"><span data-stu-id="0645a-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="0645a-120">範例4：使用 DnsZone 物件在區域中取得所有記錄集</span><span class="sxs-lookup"><span data-stu-id="0645a-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

<span data-ttu-id="0645a-121">這個範例與上述範例3相當。</span><span class="sxs-lookup"><span data-stu-id="0645a-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="0645a-122">這次，該區域是使用 zone 物件來指定的。</span><span class="sxs-lookup"><span data-stu-id="0645a-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="0645a-123">參數</span><span class="sxs-lookup"><span data-stu-id="0645a-123">PARAMETERS</span></span>

### <span data-ttu-id="0645a-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="0645a-124">-Name</span></span>
<span data-ttu-id="0645a-125">指定要取得的 **記錄集** 名稱。</span><span class="sxs-lookup"><span data-stu-id="0645a-125">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="0645a-126">如果您沒有指定 *Name* 參數，則會傳回指定類型的所有記錄集。</span><span class="sxs-lookup"><span data-stu-id="0645a-126">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Object
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0645a-127">-RecordType</span><span class="sxs-lookup"><span data-stu-id="0645a-127">-RecordType</span></span>
<span data-ttu-id="0645a-128">指定此 Cmdlet 取得的 DNS 記錄類型。</span><span class="sxs-lookup"><span data-stu-id="0645a-128">Specifies the type of DNS record that this cmdlet gets.</span></span>

<span data-ttu-id="0645a-129">有效值為：</span><span class="sxs-lookup"><span data-stu-id="0645a-129">Valid values are:</span></span> 

- <span data-ttu-id="0645a-130">是</span><span class="sxs-lookup"><span data-stu-id="0645a-130">A</span></span>
- <span data-ttu-id="0645a-131">AAAA</span><span class="sxs-lookup"><span data-stu-id="0645a-131">AAAA</span></span>
- <span data-ttu-id="0645a-132">CNAME</span><span class="sxs-lookup"><span data-stu-id="0645a-132">CNAME</span></span>
- <span data-ttu-id="0645a-133">MX</span><span class="sxs-lookup"><span data-stu-id="0645a-133">MX</span></span>
- <span data-ttu-id="0645a-134">NS</span><span class="sxs-lookup"><span data-stu-id="0645a-134">NS</span></span>
- <span data-ttu-id="0645a-135">PTR</span><span class="sxs-lookup"><span data-stu-id="0645a-135">PTR</span></span>
- <span data-ttu-id="0645a-136">SOA</span><span class="sxs-lookup"><span data-stu-id="0645a-136">SOA</span></span>
- <span data-ttu-id="0645a-137">DNS-SRV</span><span class="sxs-lookup"><span data-stu-id="0645a-137">SRV</span></span>
- <span data-ttu-id="0645a-138">文字檔</span><span class="sxs-lookup"><span data-stu-id="0645a-138">TXT</span></span>

<span data-ttu-id="0645a-139">如果您沒有指定 *RecordType* 參數，也必須省略 *Name* 參數。</span><span class="sxs-lookup"><span data-stu-id="0645a-139">If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="0645a-140">這個 Cmdlet 會傳回所有名稱和類型的區域 (中的所有記錄集) 。</span><span class="sxs-lookup"><span data-stu-id="0645a-140">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

```yaml
Type: RecordType
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0645a-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0645a-141">-ResourceGroupName</span></span>
<span data-ttu-id="0645a-142">指定包含 DNS 區域的資源群組。</span><span class="sxs-lookup"><span data-stu-id="0645a-142">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="0645a-143">您也必須使用 *ZoneName* 參數指定區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="0645a-143">The zone name must also be specified, using the *ZoneName* parameter.</span></span>

<span data-ttu-id="0645a-144">或者，您也可以使用 *zone* 參數傳入 **DnsZone** 物件來指定區域和資源群組。</span><span class="sxs-lookup"><span data-stu-id="0645a-144">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0645a-145">-Zone</span><span class="sxs-lookup"><span data-stu-id="0645a-145">-Zone</span></span>
<span data-ttu-id="0645a-146">指定包含此 Cmdlet 所取得之記錄集的 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="0645a-146">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="0645a-147">或者，您也可以使用 *ZoneName* 和 *ResourceGroupName* 參數指定區域。</span><span class="sxs-lookup"><span data-stu-id="0645a-147">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsZone
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0645a-148">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="0645a-148">-ZoneName</span></span>
<span data-ttu-id="0645a-149">指定包含要取得之記錄集之 DNS 區域的名稱。</span><span class="sxs-lookup"><span data-stu-id="0645a-149">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="0645a-150">您也必須使用 *ResourceGroupName* 參數指定包含該區域的資源群組。</span><span class="sxs-lookup"><span data-stu-id="0645a-150">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="0645a-151">或者，您也可以使用 *zone* 參數傳入 DNS 區域物件來指定區域和資源群組。</span><span class="sxs-lookup"><span data-stu-id="0645a-151">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0645a-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0645a-152">CommonParameters</span></span>
<span data-ttu-id="0645a-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0645a-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0645a-154">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0645a-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0645a-155">輸入</span><span class="sxs-lookup"><span data-stu-id="0645a-155">INPUTS</span></span>

### <span data-ttu-id="0645a-156">DnsZone （）</span><span class="sxs-lookup"><span data-stu-id="0645a-156">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="0645a-157">您可以將 **DnsZone** 物件輸送到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0645a-157">You can pipe a **DnsZone** object to this cmdlet.</span></span>
<span data-ttu-id="0645a-158">**DnsZone** 物件代表要在其中尋找 **RecordSet** 物件的區域。</span><span class="sxs-lookup"><span data-stu-id="0645a-158">The **DnsZone** object represents the zone in which to look for the **RecordSet** object.</span></span>

## <span data-ttu-id="0645a-159">輸出</span><span class="sxs-lookup"><span data-stu-id="0645a-159">OUTPUTS</span></span>

### <span data-ttu-id="0645a-160">DnsRecordSet （）</span><span class="sxs-lookup"><span data-stu-id="0645a-160">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="0645a-161">這個 Cmdlet 會傳回一個或多個代表找到之記錄集的物件。</span><span class="sxs-lookup"><span data-stu-id="0645a-161">This cmdlet returns one or more objects that represents the record sets that are found.</span></span>
<span data-ttu-id="0645a-162">如果指定 *Name* 與 *RecordType* 參數，則最多會傳回一個 **記錄集** ，否則會以陣列形式傳回多個 **記錄集** 物件。</span><span class="sxs-lookup"><span data-stu-id="0645a-162">There will be at most one **RecordSet** returned if the *Name* and *RecordType* parameters are specified, otherwise multiple **RecordSet** objects are returned as an array.</span></span>

## <span data-ttu-id="0645a-163">筆記</span><span class="sxs-lookup"><span data-stu-id="0645a-163">NOTES</span></span>

## <span data-ttu-id="0645a-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="0645a-164">RELATED LINKS</span></span>

[<span data-ttu-id="0645a-165">新-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0645a-165">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="0645a-166">移除-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0645a-166">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="0645a-167">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0645a-167">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)


