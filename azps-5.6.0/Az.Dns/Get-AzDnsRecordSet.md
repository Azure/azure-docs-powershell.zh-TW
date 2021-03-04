---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: 447b1e32473d00504446478a9efaa5634e3b1c65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910146"
---
# <span data-ttu-id="b2b38-101">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b2b38-101">Get-AzDnsRecordSet</span></span>

## <span data-ttu-id="b2b38-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b2b38-102">SYNOPSIS</span></span>
<span data-ttu-id="b2b38-103">獲得 DNS 記錄集。</span><span class="sxs-lookup"><span data-stu-id="b2b38-103">Gets a DNS record set.</span></span>

## <span data-ttu-id="b2b38-104">語法</span><span class="sxs-lookup"><span data-stu-id="b2b38-104">SYNTAX</span></span>

### <span data-ttu-id="b2b38-105">領域</span><span class="sxs-lookup"><span data-stu-id="b2b38-105">Fields</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2b38-106">物件</span><span class="sxs-lookup"><span data-stu-id="b2b38-106">Object</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2b38-107">描述</span><span class="sxs-lookup"><span data-stu-id="b2b38-107">DESCRIPTION</span></span>
<span data-ttu-id="b2b38-108">**Get-AzDnsRecordSet** Cmdlet 會取得指定區域中具有指定名稱和類型的網域名稱系統 (DNS) 記錄集。</span><span class="sxs-lookup"><span data-stu-id="b2b38-108">The **Get-AzDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>
<span data-ttu-id="b2b38-109">如果您未指定 *Name* 或 *RecordType* 參數，此 Cmdlet 會傳回區域中指定類型的所有記錄集。</span><span class="sxs-lookup"><span data-stu-id="b2b38-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="b2b38-110">如果您指定 *RecordType* 參數，但未指定 *Name* 參數，此 Cmdlet 會傳回指定記錄類型的所有記錄集。</span><span class="sxs-lookup"><span data-stu-id="b2b38-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>
<span data-ttu-id="b2b38-111">您可以使用管線運算子將 **DnsZone** 物件傳遞到此 Cmdlet，或將 **DnsZone** 物件傳遞為 *Zone* 參數，或者您也可以根據名稱指定區域和資源群組。</span><span class="sxs-lookup"><span data-stu-id="b2b38-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="b2b38-112">例子</span><span class="sxs-lookup"><span data-stu-id="b2b38-112">EXAMPLES</span></span>

### <span data-ttu-id="b2b38-113">範例 1：取得具有指定名稱和類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="b2b38-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="b2b38-114">此命令會獲得指定資源群組和區域中名為 www 的記錄類型 A 記錄集，然後將它儲存在$RecordSet變數。</span><span class="sxs-lookup"><span data-stu-id="b2b38-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="b2b38-115">由於會 *指定 Name* 和 *RecordType* 參數，因此只會 **傳回一個 RecordSet** 物件。</span><span class="sxs-lookup"><span data-stu-id="b2b38-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="b2b38-116">範例 2：取得指定類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="b2b38-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="b2b38-117">此命令會從名為 MyResourceGroup 的資源群組中，將 A 記錄類型的所有記錄集陣列放在名為 myzone.com 的區域，然後將它們儲存在 $RecordSets 變數中。</span><span class="sxs-lookup"><span data-stu-id="b2b38-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="b2b38-118">範例 3：取得區域中的所有記錄集</span><span class="sxs-lookup"><span data-stu-id="b2b38-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="b2b38-119">此命令會獲得名為 MyResourceGroup 之資源群組中名為 myzone.com 之區域中所有記錄集的陣列，然後將它們儲存在 $RecordSets 變數中。</span><span class="sxs-lookup"><span data-stu-id="b2b38-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="b2b38-120">範例 4：使用 DnsZone 物件取得區域中的所有記錄集</span><span class="sxs-lookup"><span data-stu-id="b2b38-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

<span data-ttu-id="b2b38-121">此範例相當於上述範例 3。</span><span class="sxs-lookup"><span data-stu-id="b2b38-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="b2b38-122">這一次，區域是使用區域物件指定。</span><span class="sxs-lookup"><span data-stu-id="b2b38-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="b2b38-123">參數</span><span class="sxs-lookup"><span data-stu-id="b2b38-123">PARAMETERS</span></span>

### <span data-ttu-id="b2b38-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2b38-124">-DefaultProfile</span></span>
<span data-ttu-id="b2b38-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="b2b38-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2b38-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="b2b38-126">-Name</span></span>
<span data-ttu-id="b2b38-127">指定要取得 **之 RecordSet** 的名稱。</span><span class="sxs-lookup"><span data-stu-id="b2b38-127">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="b2b38-128">如果您沒有指定 *Name* 參數，則會返回指定類型的所有記錄集。</span><span class="sxs-lookup"><span data-stu-id="b2b38-128">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2b38-129">-RecordType</span><span class="sxs-lookup"><span data-stu-id="b2b38-129">-RecordType</span></span>
<span data-ttu-id="b2b38-130">指定此 Cmdlet 所獲取的 DNS 記錄類型。</span><span class="sxs-lookup"><span data-stu-id="b2b38-130">Specifies the type of DNS record that this cmdlet gets.</span></span>
<span data-ttu-id="b2b38-131">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="b2b38-131">Valid values are:</span></span> 
- <span data-ttu-id="b2b38-132">A</span><span class="sxs-lookup"><span data-stu-id="b2b38-132">A</span></span>
- <span data-ttu-id="b2b38-133">Aaaa</span><span class="sxs-lookup"><span data-stu-id="b2b38-133">AAAA</span></span>
- <span data-ttu-id="b2b38-134">CNAME</span><span class="sxs-lookup"><span data-stu-id="b2b38-134">CNAME</span></span>
- <span data-ttu-id="b2b38-135">Mx</span><span class="sxs-lookup"><span data-stu-id="b2b38-135">MX</span></span>
- <span data-ttu-id="b2b38-136">Ns</span><span class="sxs-lookup"><span data-stu-id="b2b38-136">NS</span></span>
- <span data-ttu-id="b2b38-137">Ptr</span><span class="sxs-lookup"><span data-stu-id="b2b38-137">PTR</span></span>
- <span data-ttu-id="b2b38-138">Soa</span><span class="sxs-lookup"><span data-stu-id="b2b38-138">SOA</span></span>
- <span data-ttu-id="b2b38-139">SRV</span><span class="sxs-lookup"><span data-stu-id="b2b38-139">SRV</span></span>
- <span data-ttu-id="b2b38-140">TXT 如果您未指定 *RecordType* 參數，您也必須省略 *Name* 參數。</span><span class="sxs-lookup"><span data-stu-id="b2b38-140">TXT If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="b2b38-141">此 Cmdlet 接著會以所有名稱及類型 (區域的所有記錄集) 。</span><span class="sxs-lookup"><span data-stu-id="b2b38-141">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.RecordType]
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2b38-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2b38-142">-ResourceGroupName</span></span>
<span data-ttu-id="b2b38-143">指定包含 DNS 區域的資源群組。</span><span class="sxs-lookup"><span data-stu-id="b2b38-143">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="b2b38-144">區功能變數名稱稱也必須使用 *ZoneName* 參數指定。</span><span class="sxs-lookup"><span data-stu-id="b2b38-144">The zone name must also be specified, using the *ZoneName* parameter.</span></span>
<span data-ttu-id="b2b38-145">或者，您也可以使用 Zone 參數傳遞 **DnsZone** 物件來指定 *區域* 和資源群組。</span><span class="sxs-lookup"><span data-stu-id="b2b38-145">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2b38-146">-區域</span><span class="sxs-lookup"><span data-stu-id="b2b38-146">-Zone</span></span>
<span data-ttu-id="b2b38-147">指定包含此 Cmdlet 所獲得記錄集的 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="b2b38-147">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="b2b38-148">或者，您可以使用 *ZoneName* 和 *ResourceGroupName* 參數指定區域。</span><span class="sxs-lookup"><span data-stu-id="b2b38-148">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2b38-149">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="b2b38-149">-ZoneName</span></span>
<span data-ttu-id="b2b38-150">指定包含要取得之記錄集的 DNS 區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="b2b38-150">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="b2b38-151">包含區域的資源群組也必須使用 *ResourceGroupName* 參數指定。</span><span class="sxs-lookup"><span data-stu-id="b2b38-151">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="b2b38-152">或者，您也可以使用 Zone 參數傳遞 DNS 區域物件來指定 *區域* 和資源群組。</span><span class="sxs-lookup"><span data-stu-id="b2b38-152">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2b38-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2b38-153">CommonParameters</span></span>
<span data-ttu-id="b2b38-154">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b2b38-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2b38-155">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b2b38-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2b38-156">輸入</span><span class="sxs-lookup"><span data-stu-id="b2b38-156">INPUTS</span></span>

### <span data-ttu-id="b2b38-157">System.String</span><span class="sxs-lookup"><span data-stu-id="b2b38-157">System.String</span></span>

### <span data-ttu-id="b2b38-158">Microsoft.Azure.Commands.dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="b2b38-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="b2b38-159">System.Nullable'1[[Microsoft.Azure.management.dns.models.RecordType，Microsoft.Azure.management.dns， Version=3.0.0.0， Culture=neutral， PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b2b38-159">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="b2b38-160">輸出</span><span class="sxs-lookup"><span data-stu-id="b2b38-160">OUTPUTS</span></span>

### <span data-ttu-id="b2b38-161">Microsoft.Azure.Commands.dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b2b38-161">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="b2b38-162">筆記</span><span class="sxs-lookup"><span data-stu-id="b2b38-162">NOTES</span></span>

## <span data-ttu-id="b2b38-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="b2b38-163">RELATED LINKS</span></span>

[<span data-ttu-id="b2b38-164">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b2b38-164">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="b2b38-165">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b2b38-165">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="b2b38-166">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b2b38-166">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)


