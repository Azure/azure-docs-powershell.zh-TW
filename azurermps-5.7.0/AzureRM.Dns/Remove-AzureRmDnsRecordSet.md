---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/remove-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordSet.md
ms.openlocfilehash: fce5cbe993861d2a0d97bffd4bf4c7dbe19cc535
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624184"
---
# <span data-ttu-id="235fd-101">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="235fd-101">Remove-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="235fd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="235fd-102">SYNOPSIS</span></span>
<span data-ttu-id="235fd-103">刪除記錄集。</span><span class="sxs-lookup"><span data-stu-id="235fd-103">Deletes a record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="235fd-104">句法</span><span class="sxs-lookup"><span data-stu-id="235fd-104">SYNTAX</span></span>

### <span data-ttu-id="235fd-105">區域</span><span class="sxs-lookup"><span data-stu-id="235fd-105">Fields</span></span>
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String>
 -ResourceGroupName <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="235fd-106">混淆</span><span class="sxs-lookup"><span data-stu-id="235fd-106">Mixed</span></span>
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="235fd-107">面向</span><span class="sxs-lookup"><span data-stu-id="235fd-107">Object</span></span>
```
Remove-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="235fd-108">說明</span><span class="sxs-lookup"><span data-stu-id="235fd-108">DESCRIPTION</span></span>
<span data-ttu-id="235fd-109">**AzureRmDnsRecordSet** Cmdlet 會從指定的區域刪除指定的記錄集。</span><span class="sxs-lookup"><span data-stu-id="235fd-109">The **Remove-AzureRmDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="235fd-110">您無法刪除 SOA 或名稱伺服器 (在區域 apex 自動建立的 NS) 記錄。</span><span class="sxs-lookup"><span data-stu-id="235fd-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>

<span data-ttu-id="235fd-111">您可以使用管線運算子或參數，將 **RecordSet** 物件傳遞到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="235fd-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="235fd-112">若要透過名稱和類型來找出不使用 **RecordSet** 物件的記錄，您必須使用管線運算子或參數，將該區域以 **DnsZone** 物件傳遞給這個 Cmdlet，或者也可以指定 *ZoneName* 和 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="235fd-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="235fd-113">您可以使用 Confirm 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="235fd-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="235fd-114">使用 **RecordSet** 物件指定記錄集時，如果自檢索到本機 **記錄** 集物件之後，在 Azure DNS 中變更記錄集，就不會刪除。</span><span class="sxs-lookup"><span data-stu-id="235fd-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="235fd-115">這可為併發變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="235fd-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="235fd-116">您可以使用 *Overwrite* 參數來取消這項設定，不論併發變更為何，都會刪除記錄集。</span><span class="sxs-lookup"><span data-stu-id="235fd-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="235fd-117">示例</span><span class="sxs-lookup"><span data-stu-id="235fd-117">EXAMPLES</span></span>

### <span data-ttu-id="235fd-118">範例1：移除記錄集</span><span class="sxs-lookup"><span data-stu-id="235fd-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="235fd-119">第一個命令會取得指定的記錄集，然後將它儲存在 $RecordSet 變數中。第二個命令會移除 $RecordSet 中的記錄集。</span><span class="sxs-lookup"><span data-stu-id="235fd-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="235fd-120">範例2：移除記錄集並禁止所有確認</span><span class="sxs-lookup"><span data-stu-id="235fd-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="235fd-121">第一個命令會取得指定的記錄集。</span><span class="sxs-lookup"><span data-stu-id="235fd-121">The first command gets the specified record set.</span></span>

<span data-ttu-id="235fd-122">第二個命令會刪除記錄集，即使在其間已變更也一樣。</span><span class="sxs-lookup"><span data-stu-id="235fd-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="235fd-123">已取消確認提示。</span><span class="sxs-lookup"><span data-stu-id="235fd-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="235fd-124">參數</span><span class="sxs-lookup"><span data-stu-id="235fd-124">PARAMETERS</span></span>

### <span data-ttu-id="235fd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="235fd-125">-DefaultProfile</span></span>
<span data-ttu-id="235fd-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="235fd-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="235fd-127">-Force</span><span class="sxs-lookup"><span data-stu-id="235fd-127">-Force</span></span>
<span data-ttu-id="235fd-128">此 Cmdlet 已棄用此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="235fd-128">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="235fd-129">在未來版本中將會移除它。</span><span class="sxs-lookup"><span data-stu-id="235fd-129">It will be removed in a future release.</span></span>

<span data-ttu-id="235fd-130">若要控制此 Cmdlet 是否提示您進行確認，請使用 *Confirm* 參數。</span><span class="sxs-lookup"><span data-stu-id="235fd-130">To control whether this cmdlet prompts you for confirmation, use the *Confirm* parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="235fd-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="235fd-131">-Name</span></span>
<span data-ttu-id="235fd-132">指定要移除的 **記錄集** 名稱。</span><span class="sxs-lookup"><span data-stu-id="235fd-132">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="235fd-133">依名稱指定記錄時，必須使用 *zone* 參數或 *ZoneName* 與 *ResourceGroupName* 參數來指定 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="235fd-133">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="235fd-134">或者，您可以使用 **recordset 物件來指定記錄集** ，並使用 *記錄集* 參數來傳遞。</span><span class="sxs-lookup"><span data-stu-id="235fd-134">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields, Mixed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="235fd-135">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="235fd-135">-Overwrite</span></span>
<span data-ttu-id="235fd-136">使用 **RecordSet** 物件指定記錄集時，如果自檢索到本機 **記錄** 集物件之後，在 Azure DNS 中變更記錄集，就不會刪除。</span><span class="sxs-lookup"><span data-stu-id="235fd-136">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="235fd-137">這可為併發變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="235fd-137">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="235fd-138">這個值可以使用 *Overwrite* 參數加以取消，不論併發變更為何，都會刪除記錄集。</span><span class="sxs-lookup"><span data-stu-id="235fd-138">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Object
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="235fd-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="235fd-139">-PassThru</span></span>
<span data-ttu-id="235fd-140">passthru</span><span class="sxs-lookup"><span data-stu-id="235fd-140">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="235fd-141">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="235fd-141">-RecordSet</span></span>
<span data-ttu-id="235fd-142">指定要移除的 **RecordSet** 物件。</span><span class="sxs-lookup"><span data-stu-id="235fd-142">Specifies the **RecordSet** object to remove.</span></span>

<span data-ttu-id="235fd-143">或者，您可以使用 *name* 和 *Zone* 參數指定記錄集，或使用 *name* 、 *ZoneName* 及 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="235fd-143">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsRecordSet
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="235fd-144">-RecordType</span><span class="sxs-lookup"><span data-stu-id="235fd-144">-RecordType</span></span>
<span data-ttu-id="235fd-145">指定 DNS 記錄的類型。</span><span class="sxs-lookup"><span data-stu-id="235fd-145">Specifies the type of DNS record.</span></span>

<span data-ttu-id="235fd-146">有效值為：</span><span class="sxs-lookup"><span data-stu-id="235fd-146">Valid values are:</span></span>

- <span data-ttu-id="235fd-147">是</span><span class="sxs-lookup"><span data-stu-id="235fd-147">A</span></span>
- <span data-ttu-id="235fd-148">AAAA</span><span class="sxs-lookup"><span data-stu-id="235fd-148">AAAA</span></span>
- <span data-ttu-id="235fd-149">CNAME</span><span class="sxs-lookup"><span data-stu-id="235fd-149">CNAME</span></span>
- <span data-ttu-id="235fd-150">MX</span><span class="sxs-lookup"><span data-stu-id="235fd-150">MX</span></span>
- <span data-ttu-id="235fd-151">NS</span><span class="sxs-lookup"><span data-stu-id="235fd-151">NS</span></span>
- <span data-ttu-id="235fd-152">PTR</span><span class="sxs-lookup"><span data-stu-id="235fd-152">PTR</span></span>
- <span data-ttu-id="235fd-153">DNS-SRV</span><span class="sxs-lookup"><span data-stu-id="235fd-153">SRV</span></span>
- <span data-ttu-id="235fd-154">文字檔</span><span class="sxs-lookup"><span data-stu-id="235fd-154">TXT</span></span>

<span data-ttu-id="235fd-155">刪除區域時，系統會自動刪除 SOA 記錄。</span><span class="sxs-lookup"><span data-stu-id="235fd-155">SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="235fd-156">您無法手動刪除 SOA 記錄。</span><span class="sxs-lookup"><span data-stu-id="235fd-156">You cannot manually delete SOA records.</span></span>

```yaml
Type: RecordType
Parameter Sets: Fields, Mixed
Aliases: 
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="235fd-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="235fd-157">-ResourceGroupName</span></span>
<span data-ttu-id="235fd-158">指定包含要刪除之 **記錄集** 之 DNS 區域的資源群組。</span><span class="sxs-lookup"><span data-stu-id="235fd-158">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="235fd-159">這個參數只有在使用 *Name* 和 *ZoneName* 參數指定記錄集和 DNS 區域時才適用。</span><span class="sxs-lookup"><span data-stu-id="235fd-159">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>

<span data-ttu-id="235fd-160">或者，您也可以使用 *記錄* 集參數指定記錄集，或是 *名稱* 和 *區域* 參數。</span><span class="sxs-lookup"><span data-stu-id="235fd-160">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="235fd-161">-Zone</span><span class="sxs-lookup"><span data-stu-id="235fd-161">-Zone</span></span>
<span data-ttu-id="235fd-162">指定包含要刪除之 **記錄集** 的 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="235fd-162">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="235fd-163">這個參數只適用于使用 *Name* 參數指定記錄集時。</span><span class="sxs-lookup"><span data-stu-id="235fd-163">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>

<span data-ttu-id="235fd-164">或者，您也可以使用 *記錄* 集參數或 *名稱* 、 *ZoneName* 及 *ResourceGroupName* 參數來指定記錄集。</span><span class="sxs-lookup"><span data-stu-id="235fd-164">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsZone
Parameter Sets: Mixed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="235fd-165">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="235fd-165">-ZoneName</span></span>
<span data-ttu-id="235fd-166">指定包含要刪除之 **記錄集** 的區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="235fd-166">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="235fd-167">您也必須指定 *Name* 及 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="235fd-167">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="235fd-168">或者，您可以使用 *RecordSet* 參數或 *名稱* 和 *區域* 參數來指定記錄集。</span><span class="sxs-lookup"><span data-stu-id="235fd-168">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="235fd-169">-確認</span><span class="sxs-lookup"><span data-stu-id="235fd-169">-Confirm</span></span>
<span data-ttu-id="235fd-170">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="235fd-170">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="235fd-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="235fd-171">-WhatIf</span></span>
<span data-ttu-id="235fd-172">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="235fd-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="235fd-173">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="235fd-173">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="235fd-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="235fd-174">CommonParameters</span></span>
<span data-ttu-id="235fd-175">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="235fd-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="235fd-176">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="235fd-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="235fd-177">輸入</span><span class="sxs-lookup"><span data-stu-id="235fd-177">INPUTS</span></span>

### <span data-ttu-id="235fd-178">DnsRecordSet （）</span><span class="sxs-lookup"><span data-stu-id="235fd-178">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="235fd-179">您可以將 **RecordSet** 物件輸送到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="235fd-179">You can pipe a **RecordSet** object to this cmdlet.</span></span>

## <span data-ttu-id="235fd-180">輸出</span><span class="sxs-lookup"><span data-stu-id="235fd-180">OUTPUTS</span></span>

### <span data-ttu-id="235fd-181">所有</span><span class="sxs-lookup"><span data-stu-id="235fd-181">None</span></span>
<span data-ttu-id="235fd-182">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="235fd-182">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="235fd-183">筆記</span><span class="sxs-lookup"><span data-stu-id="235fd-183">NOTES</span></span>
<span data-ttu-id="235fd-184">您可以使用 *Confirm* 參數來控制此 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="235fd-184">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="235fd-185">根據預設，如果 $ConfirmPreference 的 Windows PowerShell 變數的值為 [中] 或 [低]，則該 Cmdlet 會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="235fd-185">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="235fd-186">如果您指定 [ *確認* ] 或 [ *確認]： $True* ，此 Cmdlet 會在您執行之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="235fd-186">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="235fd-187">如果您指定 [ *確認： $False* ]，則 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="235fd-187">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="235fd-188">相關連結</span><span class="sxs-lookup"><span data-stu-id="235fd-188">RELATED LINKS</span></span>

[<span data-ttu-id="235fd-189">AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="235fd-189">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="235fd-190">新-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="235fd-190">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="235fd-191">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="235fd-191">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
