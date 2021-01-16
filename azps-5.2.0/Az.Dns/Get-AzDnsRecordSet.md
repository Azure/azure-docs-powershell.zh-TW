---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: b64432364b9c86a1153ba9a535d70645cf15d4d1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279675"
---
# <span data-ttu-id="8c035-101">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8c035-101">Get-AzDnsRecordSet</span></span>

## <span data-ttu-id="8c035-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c035-102">SYNOPSIS</span></span>
<span data-ttu-id="8c035-103">取得 DNS 記錄集。</span><span class="sxs-lookup"><span data-stu-id="8c035-103">Gets a DNS record set.</span></span>

## <span data-ttu-id="8c035-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c035-104">SYNTAX</span></span>

### <span data-ttu-id="8c035-105">區域</span><span class="sxs-lookup"><span data-stu-id="8c035-105">Fields</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c035-106">面向</span><span class="sxs-lookup"><span data-stu-id="8c035-106">Object</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c035-107">說明</span><span class="sxs-lookup"><span data-stu-id="8c035-107">DESCRIPTION</span></span>
<span data-ttu-id="8c035-108">**AzDnsRecordSet** Cmdlet 會在指定的區域中，以指定的名稱與類型來取得網功能變數名稱稱系統 (DNS) 記錄集。</span><span class="sxs-lookup"><span data-stu-id="8c035-108">The **Get-AzDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>
<span data-ttu-id="8c035-109">如果您沒有指定 *Name* 或 *RecordType* 參數，這個 Cmdlet 會傳回區域中指定類型的所有記錄集。</span><span class="sxs-lookup"><span data-stu-id="8c035-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="8c035-110">如果您指定 *RecordType* 參數而不是 *Name* 參數，這個 Cmdlet 會傳回指定記錄類型的所有記錄集。</span><span class="sxs-lookup"><span data-stu-id="8c035-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>
<span data-ttu-id="8c035-111">您可以使用管線運算子，將 **DnsZone** 物件傳遞到這個 Cmdlet，或者您可以將 **DnsZone** 物件傳遞為 *zone* 參數，或者也可以依名稱指定區域和資源群組。</span><span class="sxs-lookup"><span data-stu-id="8c035-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="8c035-112">示例</span><span class="sxs-lookup"><span data-stu-id="8c035-112">EXAMPLES</span></span>

### <span data-ttu-id="8c035-113">範例1：取得具有指定名稱和類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="8c035-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="8c035-114">這個命令會在指定的資源群組和區域中取得一組記錄類型的記錄，並將它儲存在 $RecordSet 變數中。</span><span class="sxs-lookup"><span data-stu-id="8c035-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="8c035-115">因為已指定 *Name* 和 *RecordType* 參數，所以只會傳回一個 **記錄集** 物件。</span><span class="sxs-lookup"><span data-stu-id="8c035-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="8c035-116">範例2：取得指定類型的記錄集</span><span class="sxs-lookup"><span data-stu-id="8c035-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="8c035-117">這個命令會在名為 [MyResourceGroup] 的資源群組中，從名為「myzone.com」的區域中取得記錄類型 A 之所有記錄集的陣列，然後將它們儲存在 $RecordSets 變數中。</span><span class="sxs-lookup"><span data-stu-id="8c035-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="8c035-118">範例3：取得區域中的所有記錄集</span><span class="sxs-lookup"><span data-stu-id="8c035-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="8c035-119">這個命令會在名為 MyResourceGroup 的資源群組中，從名為 myzone.com 的區域中取得所有記錄集的陣列，然後將它們儲存在 $RecordSets 變數中。</span><span class="sxs-lookup"><span data-stu-id="8c035-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="8c035-120">範例4：使用 DnsZone 物件在區域中取得所有記錄集</span><span class="sxs-lookup"><span data-stu-id="8c035-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

<span data-ttu-id="8c035-121">這個範例與上述範例3相當。</span><span class="sxs-lookup"><span data-stu-id="8c035-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="8c035-122">這次，該區域是使用 zone 物件來指定的。</span><span class="sxs-lookup"><span data-stu-id="8c035-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="8c035-123">參數</span><span class="sxs-lookup"><span data-stu-id="8c035-123">PARAMETERS</span></span>

### <span data-ttu-id="8c035-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c035-124">-DefaultProfile</span></span>
<span data-ttu-id="8c035-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8c035-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c035-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="8c035-126">-Name</span></span>
<span data-ttu-id="8c035-127">指定要取得的 **記錄集** 名稱。</span><span class="sxs-lookup"><span data-stu-id="8c035-127">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="8c035-128">如果您沒有指定 *Name* 參數，則會傳回指定類型的所有記錄集。</span><span class="sxs-lookup"><span data-stu-id="8c035-128">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

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

### <span data-ttu-id="8c035-129">-RecordType</span><span class="sxs-lookup"><span data-stu-id="8c035-129">-RecordType</span></span>
<span data-ttu-id="8c035-130">指定此 Cmdlet 取得的 DNS 記錄類型。</span><span class="sxs-lookup"><span data-stu-id="8c035-130">Specifies the type of DNS record that this cmdlet gets.</span></span>
<span data-ttu-id="8c035-131">有效值為：</span><span class="sxs-lookup"><span data-stu-id="8c035-131">Valid values are:</span></span> 
- <span data-ttu-id="8c035-132">是</span><span class="sxs-lookup"><span data-stu-id="8c035-132">A</span></span>
- <span data-ttu-id="8c035-133">AAAA</span><span class="sxs-lookup"><span data-stu-id="8c035-133">AAAA</span></span>
- <span data-ttu-id="8c035-134">CNAME</span><span class="sxs-lookup"><span data-stu-id="8c035-134">CNAME</span></span>
- <span data-ttu-id="8c035-135">MX</span><span class="sxs-lookup"><span data-stu-id="8c035-135">MX</span></span>
- <span data-ttu-id="8c035-136">NS</span><span class="sxs-lookup"><span data-stu-id="8c035-136">NS</span></span>
- <span data-ttu-id="8c035-137">PTR</span><span class="sxs-lookup"><span data-stu-id="8c035-137">PTR</span></span>
- <span data-ttu-id="8c035-138">SOA</span><span class="sxs-lookup"><span data-stu-id="8c035-138">SOA</span></span>
- <span data-ttu-id="8c035-139">DNS-SRV</span><span class="sxs-lookup"><span data-stu-id="8c035-139">SRV</span></span>
- <span data-ttu-id="8c035-140">TXT 如果您沒有指定 *RecordType* 參數，也必須省略 *Name* 參數。</span><span class="sxs-lookup"><span data-stu-id="8c035-140">TXT If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="8c035-141">這個 Cmdlet 會傳回所有名稱和類型的區域 (中的所有記錄集) 。</span><span class="sxs-lookup"><span data-stu-id="8c035-141">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

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

### <span data-ttu-id="8c035-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c035-142">-ResourceGroupName</span></span>
<span data-ttu-id="8c035-143">指定包含 DNS 區域的資源群組。</span><span class="sxs-lookup"><span data-stu-id="8c035-143">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="8c035-144">您也必須使用 *ZoneName* 參數指定區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="8c035-144">The zone name must also be specified, using the *ZoneName* parameter.</span></span>
<span data-ttu-id="8c035-145">或者，您也可以使用 *zone* 參數傳入 **DnsZone** 物件來指定區域和資源群組。</span><span class="sxs-lookup"><span data-stu-id="8c035-145">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="8c035-146">-Zone</span><span class="sxs-lookup"><span data-stu-id="8c035-146">-Zone</span></span>
<span data-ttu-id="8c035-147">指定包含此 Cmdlet 所取得之記錄集的 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="8c035-147">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="8c035-148">或者，您也可以使用 *ZoneName* 和 *ResourceGroupName* 參數指定區域。</span><span class="sxs-lookup"><span data-stu-id="8c035-148">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="8c035-149">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="8c035-149">-ZoneName</span></span>
<span data-ttu-id="8c035-150">指定包含要取得之記錄集之 DNS 區域的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c035-150">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="8c035-151">您也必須使用 *ResourceGroupName* 參數指定包含該區域的資源群組。</span><span class="sxs-lookup"><span data-stu-id="8c035-151">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="8c035-152">或者，您也可以使用 *zone* 參數傳入 DNS 區域物件來指定區域和資源群組。</span><span class="sxs-lookup"><span data-stu-id="8c035-152">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="8c035-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c035-153">CommonParameters</span></span>
<span data-ttu-id="8c035-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c035-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c035-155">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8c035-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c035-156">輸入</span><span class="sxs-lookup"><span data-stu-id="8c035-156">INPUTS</span></span>

### <span data-ttu-id="8c035-157">System.object</span><span class="sxs-lookup"><span data-stu-id="8c035-157">System.String</span></span>

### <span data-ttu-id="8c035-158">DnsZone （）</span><span class="sxs-lookup"><span data-stu-id="8c035-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="8c035-159">"RecordType" 1 [[3.0.0.0 版]。 Dns，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]] （"）]</span><span class="sxs-lookup"><span data-stu-id="8c035-159">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="8c035-160">輸出</span><span class="sxs-lookup"><span data-stu-id="8c035-160">OUTPUTS</span></span>

### <span data-ttu-id="8c035-161">DnsRecordSet （）</span><span class="sxs-lookup"><span data-stu-id="8c035-161">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="8c035-162">筆記</span><span class="sxs-lookup"><span data-stu-id="8c035-162">NOTES</span></span>

## <span data-ttu-id="8c035-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c035-163">RELATED LINKS</span></span>

[<span data-ttu-id="8c035-164">新-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8c035-164">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="8c035-165">移除-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8c035-165">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="8c035-166">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8c035-166">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)


