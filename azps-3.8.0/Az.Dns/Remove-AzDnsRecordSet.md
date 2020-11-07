---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: f5d7075322bb2b5a4b61635400664f0e909f126d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956888"
---
# <span data-ttu-id="4ece3-101">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4ece3-101">Remove-AzDnsRecordSet</span></span>

## <span data-ttu-id="4ece3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4ece3-102">SYNOPSIS</span></span>
<span data-ttu-id="4ece3-103">刪除記錄集。</span><span class="sxs-lookup"><span data-stu-id="4ece3-103">Deletes a record set.</span></span>

## <span data-ttu-id="4ece3-104">句法</span><span class="sxs-lookup"><span data-stu-id="4ece3-104">SYNTAX</span></span>

### <span data-ttu-id="4ece3-105">區域</span><span class="sxs-lookup"><span data-stu-id="4ece3-105">Fields</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String> -ResourceGroupName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ece3-106">混淆</span><span class="sxs-lookup"><span data-stu-id="4ece3-106">Mixed</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ece3-107">面向</span><span class="sxs-lookup"><span data-stu-id="4ece3-107">Object</span></span>
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ece3-108">說明</span><span class="sxs-lookup"><span data-stu-id="4ece3-108">DESCRIPTION</span></span>
<span data-ttu-id="4ece3-109">**AzDnsRecordSet** Cmdlet 會從指定的區域刪除指定的記錄集。</span><span class="sxs-lookup"><span data-stu-id="4ece3-109">The **Remove-AzDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="4ece3-110">您無法刪除 SOA 或名稱伺服器 (在區域 apex 自動建立的 NS) 記錄。</span><span class="sxs-lookup"><span data-stu-id="4ece3-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>
<span data-ttu-id="4ece3-111">您可以使用管線運算子或參數，將 **RecordSet** 物件傳遞到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4ece3-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="4ece3-112">若要透過名稱和類型來找出不使用 **RecordSet** 物件的記錄，您必須使用管線運算子或參數，將該區域以 **DnsZone** 物件傳遞給這個 Cmdlet，或者也可以指定 *ZoneName* 和 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="4ece3-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="4ece3-113">您可以使用 Confirm 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4ece3-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="4ece3-114">使用 **RecordSet** 物件指定記錄集時，如果自檢索到本機 **記錄** 集物件之後，在 Azure DNS 中變更記錄集，就不會刪除。</span><span class="sxs-lookup"><span data-stu-id="4ece3-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="4ece3-115">這可為併發變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="4ece3-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="4ece3-116">您可以使用 *Overwrite* 參數來取消這項設定，不論併發變更為何，都會刪除記錄集。</span><span class="sxs-lookup"><span data-stu-id="4ece3-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="4ece3-117">示例</span><span class="sxs-lookup"><span data-stu-id="4ece3-117">EXAMPLES</span></span>

### <span data-ttu-id="4ece3-118">範例1：移除記錄集</span><span class="sxs-lookup"><span data-stu-id="4ece3-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="4ece3-119">第一個命令會取得指定的記錄集，然後將它儲存在 $RecordSet 變數中。第二個命令會移除 $RecordSet 中的記錄集。</span><span class="sxs-lookup"><span data-stu-id="4ece3-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="4ece3-120">範例2：移除記錄集並禁止所有確認</span><span class="sxs-lookup"><span data-stu-id="4ece3-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="4ece3-121">第一個命令會取得指定的記錄集。</span><span class="sxs-lookup"><span data-stu-id="4ece3-121">The first command gets the specified record set.</span></span>
<span data-ttu-id="4ece3-122">第二個命令會刪除記錄集，即使在其間已變更也一樣。</span><span class="sxs-lookup"><span data-stu-id="4ece3-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="4ece3-123">已取消確認提示。</span><span class="sxs-lookup"><span data-stu-id="4ece3-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="4ece3-124">參數</span><span class="sxs-lookup"><span data-stu-id="4ece3-124">PARAMETERS</span></span>

### <span data-ttu-id="4ece3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ece3-125">-DefaultProfile</span></span>
<span data-ttu-id="4ece3-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4ece3-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ece3-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="4ece3-127">-Name</span></span>
<span data-ttu-id="4ece3-128">指定要移除的 **記錄集** 名稱。</span><span class="sxs-lookup"><span data-stu-id="4ece3-128">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="4ece3-129">依名稱指定記錄時，必須使用 *zone* 參數或 *ZoneName* 與 *ResourceGroupName* 參數來指定 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="4ece3-129">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="4ece3-130">或者，您可以使用 **recordset 物件來指定記錄集** ，並使用 *記錄集* 參數來傳遞。</span><span class="sxs-lookup"><span data-stu-id="4ece3-130">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ece3-131">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="4ece3-131">-Overwrite</span></span>
<span data-ttu-id="4ece3-132">使用 **RecordSet** 物件指定記錄集時，如果自檢索到本機 **記錄** 集物件之後，在 Azure DNS 中變更記錄集，就不會刪除。</span><span class="sxs-lookup"><span data-stu-id="4ece3-132">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="4ece3-133">這可為併發變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="4ece3-133">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="4ece3-134">這個值可以使用 *Overwrite* 參數加以取消，不論併發變更為何，都會刪除記錄集。</span><span class="sxs-lookup"><span data-stu-id="4ece3-134">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ece3-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ece3-135">-PassThru</span></span>
<span data-ttu-id="4ece3-136">passthru</span><span class="sxs-lookup"><span data-stu-id="4ece3-136">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ece3-137">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="4ece3-137">-RecordSet</span></span>
<span data-ttu-id="4ece3-138">指定要移除的 **RecordSet** 物件。</span><span class="sxs-lookup"><span data-stu-id="4ece3-138">Specifies the **RecordSet** object to remove.</span></span>
<span data-ttu-id="4ece3-139">或者，您可以使用 *name* 和 *Zone* 參數指定記錄集，或使用 *name* 、 *ZoneName* 及 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="4ece3-139">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ece3-140">-RecordType</span><span class="sxs-lookup"><span data-stu-id="4ece3-140">-RecordType</span></span>
<span data-ttu-id="4ece3-141">指定 DNS 記錄的類型。</span><span class="sxs-lookup"><span data-stu-id="4ece3-141">Specifies the type of DNS record.</span></span>
<span data-ttu-id="4ece3-142">有效值為：</span><span class="sxs-lookup"><span data-stu-id="4ece3-142">Valid values are:</span></span>
- <span data-ttu-id="4ece3-143">是</span><span class="sxs-lookup"><span data-stu-id="4ece3-143">A</span></span>
- <span data-ttu-id="4ece3-144">AAAA</span><span class="sxs-lookup"><span data-stu-id="4ece3-144">AAAA</span></span>
- <span data-ttu-id="4ece3-145">CNAME</span><span class="sxs-lookup"><span data-stu-id="4ece3-145">CNAME</span></span>
- <span data-ttu-id="4ece3-146">MX</span><span class="sxs-lookup"><span data-stu-id="4ece3-146">MX</span></span>
- <span data-ttu-id="4ece3-147">NS</span><span class="sxs-lookup"><span data-stu-id="4ece3-147">NS</span></span>
- <span data-ttu-id="4ece3-148">PTR</span><span class="sxs-lookup"><span data-stu-id="4ece3-148">PTR</span></span>
- <span data-ttu-id="4ece3-149">DNS-SRV</span><span class="sxs-lookup"><span data-stu-id="4ece3-149">SRV</span></span>
- <span data-ttu-id="4ece3-150">當區域刪除時，會自動刪除 TXT SOA 記錄。</span><span class="sxs-lookup"><span data-stu-id="4ece3-150">TXT SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="4ece3-151">您無法手動刪除 SOA 記錄。</span><span class="sxs-lookup"><span data-stu-id="4ece3-151">You cannot manually delete SOA records.</span></span>

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ece3-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ece3-152">-ResourceGroupName</span></span>
<span data-ttu-id="4ece3-153">指定包含要刪除之 **記錄集** 之 DNS 區域的資源群組。</span><span class="sxs-lookup"><span data-stu-id="4ece3-153">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="4ece3-154">這個參數只有在使用 *Name* 和 *ZoneName* 參數指定記錄集和 DNS 區域時才適用。</span><span class="sxs-lookup"><span data-stu-id="4ece3-154">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>
<span data-ttu-id="4ece3-155">或者，您也可以使用 *記錄* 集參數指定記錄集，或是 *名稱* 和 *區域* 參數。</span><span class="sxs-lookup"><span data-stu-id="4ece3-155">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="4ece3-156">-Zone</span><span class="sxs-lookup"><span data-stu-id="4ece3-156">-Zone</span></span>
<span data-ttu-id="4ece3-157">指定包含要刪除之 **記錄集** 的 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="4ece3-157">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="4ece3-158">這個參數只適用于使用 *Name* 參數指定記錄集時。</span><span class="sxs-lookup"><span data-stu-id="4ece3-158">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>
<span data-ttu-id="4ece3-159">或者，您也可以使用 *記錄* 集參數或 *名稱* 、 *ZoneName* 及 *ResourceGroupName* 參數來指定記錄集。</span><span class="sxs-lookup"><span data-stu-id="4ece3-159">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ece3-160">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="4ece3-160">-ZoneName</span></span>
<span data-ttu-id="4ece3-161">指定包含要刪除之 **記錄集** 的區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="4ece3-161">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="4ece3-162">您也必須指定 *Name* 及 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="4ece3-162">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="4ece3-163">或者，您可以使用 *RecordSet* 參數或 *名稱* 和 *區域* 參數來指定記錄集。</span><span class="sxs-lookup"><span data-stu-id="4ece3-163">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="4ece3-164">-確認</span><span class="sxs-lookup"><span data-stu-id="4ece3-164">-Confirm</span></span>
<span data-ttu-id="4ece3-165">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4ece3-165">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ece3-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ece3-166">-WhatIf</span></span>
<span data-ttu-id="4ece3-167">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4ece3-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ece3-168">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4ece3-168">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ece3-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ece3-169">CommonParameters</span></span>
<span data-ttu-id="4ece3-170">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4ece3-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ece3-171">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4ece3-171">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ece3-172">輸入</span><span class="sxs-lookup"><span data-stu-id="4ece3-172">INPUTS</span></span>

### <span data-ttu-id="4ece3-173">RecordType 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="4ece3-173">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="4ece3-174">System.object</span><span class="sxs-lookup"><span data-stu-id="4ece3-174">System.String</span></span>

### <span data-ttu-id="4ece3-175">DnsZone （）</span><span class="sxs-lookup"><span data-stu-id="4ece3-175">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="4ece3-176">DnsRecordSet （）</span><span class="sxs-lookup"><span data-stu-id="4ece3-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="4ece3-177">輸出</span><span class="sxs-lookup"><span data-stu-id="4ece3-177">OUTPUTS</span></span>

### <span data-ttu-id="4ece3-178">System.object</span><span class="sxs-lookup"><span data-stu-id="4ece3-178">System.Boolean</span></span>

## <span data-ttu-id="4ece3-179">筆記</span><span class="sxs-lookup"><span data-stu-id="4ece3-179">NOTES</span></span>
<span data-ttu-id="4ece3-180">您可以使用 *Confirm* 參數來控制此 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4ece3-180">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="4ece3-181">根據預設，如果 $ConfirmPreference 的 Windows PowerShell 變數的值為 [中] 或 [低]，則該 Cmdlet 會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4ece3-181">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="4ece3-182">如果您指定 [ *確認* ] 或 [ *確認]： $True* ，此 Cmdlet 會在您執行之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4ece3-182">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="4ece3-183">如果您指定 [ *確認： $False* ]，則 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4ece3-183">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="4ece3-184">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ece3-184">RELATED LINKS</span></span>

[<span data-ttu-id="4ece3-185">AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4ece3-185">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="4ece3-186">新-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4ece3-186">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="4ece3-187">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4ece3-187">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
