---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: ab4f7bf6693eda413587b572832706d617b3e683
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910130"
---
# <span data-ttu-id="1f08c-101">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1f08c-101">Remove-AzDnsRecordSet</span></span>

## <span data-ttu-id="1f08c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1f08c-102">SYNOPSIS</span></span>
<span data-ttu-id="1f08c-103">刪除記錄集。</span><span class="sxs-lookup"><span data-stu-id="1f08c-103">Deletes a record set.</span></span>

## <span data-ttu-id="1f08c-104">語法</span><span class="sxs-lookup"><span data-stu-id="1f08c-104">SYNTAX</span></span>

### <span data-ttu-id="1f08c-105">領域</span><span class="sxs-lookup"><span data-stu-id="1f08c-105">Fields</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String> -ResourceGroupName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f08c-106">混合</span><span class="sxs-lookup"><span data-stu-id="1f08c-106">Mixed</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f08c-107">物件</span><span class="sxs-lookup"><span data-stu-id="1f08c-107">Object</span></span>
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f08c-108">描述</span><span class="sxs-lookup"><span data-stu-id="1f08c-108">DESCRIPTION</span></span>
<span data-ttu-id="1f08c-109">**Remove-AzDnsRecordSet** Cmdlet 會從指定的區域刪除指定的記錄集。</span><span class="sxs-lookup"><span data-stu-id="1f08c-109">The **Remove-AzDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="1f08c-110">您無法刪除在區域 (自動) NS 記錄或名稱伺服器。</span><span class="sxs-lookup"><span data-stu-id="1f08c-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>
<span data-ttu-id="1f08c-111">您可以使用管線運算子或參數，將 **RecordSet** 物件傳遞到此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1f08c-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="1f08c-112">若要在不使用 **RecordSet** 物件的情況下，根據名稱與類型識別記錄，您必須使用管線運算子或參數，將區域以 **DnsZone** 物件傳遞至此 Cmdlet，或者您也可以指定 *ZoneName* 和 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="1f08c-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="1f08c-113">您可以使用確認參數$ConfirmPreference Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1f08c-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="1f08c-114">使用 RecordSet 物件指定記錄集時，如果自已取回本地 **RecordSet** 物件之後，已在 Azure DNS 中變更記錄集， **則記錄** 集不會刪除。</span><span class="sxs-lookup"><span data-stu-id="1f08c-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="1f08c-115">這可保護同時進行變更。</span><span class="sxs-lookup"><span data-stu-id="1f08c-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="1f08c-116">您可以使用覆寫參數隱藏此設定，無論同時變更，都會刪除記錄集。</span><span class="sxs-lookup"><span data-stu-id="1f08c-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="1f08c-117">例子</span><span class="sxs-lookup"><span data-stu-id="1f08c-117">EXAMPLES</span></span>

### <span data-ttu-id="1f08c-118">範例 1：移除記錄集</span><span class="sxs-lookup"><span data-stu-id="1f08c-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="1f08c-119">第一個命令會獲得指定的記錄集，然後將它儲存在$RecordSet變數中。第二個命令會移除 $RecordSet。</span><span class="sxs-lookup"><span data-stu-id="1f08c-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="1f08c-120">範例 2：移除記錄集並隱藏所有確認</span><span class="sxs-lookup"><span data-stu-id="1f08c-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="1f08c-121">第一個命令會獲得指定的記錄集。</span><span class="sxs-lookup"><span data-stu-id="1f08c-121">The first command gets the specified record set.</span></span>
<span data-ttu-id="1f08c-122">第二個命令會刪除記錄集，即使同時已變更。</span><span class="sxs-lookup"><span data-stu-id="1f08c-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="1f08c-123">確認提示會隱藏。</span><span class="sxs-lookup"><span data-stu-id="1f08c-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="1f08c-124">參數</span><span class="sxs-lookup"><span data-stu-id="1f08c-124">PARAMETERS</span></span>

### <span data-ttu-id="1f08c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f08c-125">-DefaultProfile</span></span>
<span data-ttu-id="1f08c-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="1f08c-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f08c-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="1f08c-127">-Name</span></span>
<span data-ttu-id="1f08c-128">指定要移除 **的 RecordSet** 名稱。</span><span class="sxs-lookup"><span data-stu-id="1f08c-128">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="1f08c-129">在根據名稱指定記錄集時，必須使用 *Zone* 參數或 *ZoneName* 和 *ResourceGroupName* 參數來指定 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="1f08c-129">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="1f08c-130">或者，您可以使用 **RecordSet** 物件來指定記錄集，使用 *RecordSet* 參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="1f08c-130">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

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

### <span data-ttu-id="1f08c-131">-覆寫</span><span class="sxs-lookup"><span data-stu-id="1f08c-131">-Overwrite</span></span>
<span data-ttu-id="1f08c-132">使用 RecordSet 物件指定記錄集時，如果自已取回本地 **RecordSet** 物件之後，已在 Azure DNS 中變更記錄集， **則記錄** 集不會刪除。</span><span class="sxs-lookup"><span data-stu-id="1f08c-132">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="1f08c-133">這可保護同時進行變更。</span><span class="sxs-lookup"><span data-stu-id="1f08c-133">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="1f08c-134">您可以使用覆寫參數隱藏此設定，無論同時變更，都會刪除記錄集。</span><span class="sxs-lookup"><span data-stu-id="1f08c-134">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="1f08c-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f08c-135">-PassThru</span></span>
<span data-ttu-id="1f08c-136">Passthru</span><span class="sxs-lookup"><span data-stu-id="1f08c-136">passthru</span></span>

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

### <span data-ttu-id="1f08c-137">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="1f08c-137">-RecordSet</span></span>
<span data-ttu-id="1f08c-138">指定 **要移除的 RecordSet** 物件。</span><span class="sxs-lookup"><span data-stu-id="1f08c-138">Specifies the **RecordSet** object to remove.</span></span>
<span data-ttu-id="1f08c-139">或者，您可以使用名稱和區域參數，或是使用 *名稱\*\*、ZoneName* 和 *ResourceGroupName* 參數來指定記錄集。 </span><span class="sxs-lookup"><span data-stu-id="1f08c-139">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name*, *ZoneName*, and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="1f08c-140">-RecordType</span><span class="sxs-lookup"><span data-stu-id="1f08c-140">-RecordType</span></span>
<span data-ttu-id="1f08c-141">指定 DNS 記錄的類型。</span><span class="sxs-lookup"><span data-stu-id="1f08c-141">Specifies the type of DNS record.</span></span>
<span data-ttu-id="1f08c-142">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="1f08c-142">Valid values are:</span></span>
- <span data-ttu-id="1f08c-143">A</span><span class="sxs-lookup"><span data-stu-id="1f08c-143">A</span></span>
- <span data-ttu-id="1f08c-144">Aaaa</span><span class="sxs-lookup"><span data-stu-id="1f08c-144">AAAA</span></span>
- <span data-ttu-id="1f08c-145">CNAME</span><span class="sxs-lookup"><span data-stu-id="1f08c-145">CNAME</span></span>
- <span data-ttu-id="1f08c-146">Mx</span><span class="sxs-lookup"><span data-stu-id="1f08c-146">MX</span></span>
- <span data-ttu-id="1f08c-147">Ns</span><span class="sxs-lookup"><span data-stu-id="1f08c-147">NS</span></span>
- <span data-ttu-id="1f08c-148">Ptr</span><span class="sxs-lookup"><span data-stu-id="1f08c-148">PTR</span></span>
- <span data-ttu-id="1f08c-149">SRV</span><span class="sxs-lookup"><span data-stu-id="1f08c-149">SRV</span></span>
- <span data-ttu-id="1f08c-150">刪除區域時，會自動刪除 TXT 的 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="1f08c-150">TXT SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="1f08c-151">您無法手動刪除 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="1f08c-151">You cannot manually delete SOA records.</span></span>

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

### <span data-ttu-id="1f08c-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f08c-152">-ResourceGroupName</span></span>
<span data-ttu-id="1f08c-153">指定包含要刪除 **RecordSet** 之 DNS 區域的資源群組。</span><span class="sxs-lookup"><span data-stu-id="1f08c-153">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="1f08c-154">只有在使用 Name 和 *ZoneName* 參數指定記錄集和DNS 區域時，此參數才適用。</span><span class="sxs-lookup"><span data-stu-id="1f08c-154">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>
<span data-ttu-id="1f08c-155">或者，您可以使用 *RecordSet* 參數或名稱和區域參數來指定 *記錄* 集。 </span><span class="sxs-lookup"><span data-stu-id="1f08c-155">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="1f08c-156">-區域</span><span class="sxs-lookup"><span data-stu-id="1f08c-156">-Zone</span></span>
<span data-ttu-id="1f08c-157">指定包含要刪除 **之 RecordSet 的 DNS** 區域。</span><span class="sxs-lookup"><span data-stu-id="1f08c-157">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="1f08c-158">此參數僅適用于使用 Name 參數指定記錄 *集* 時。</span><span class="sxs-lookup"><span data-stu-id="1f08c-158">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>
<span data-ttu-id="1f08c-159">或者，您可以使用 *RecordSet* 參數或 Name、ZoneName 及 *ResourceGroupName* 參數來指定記錄集。  </span><span class="sxs-lookup"><span data-stu-id="1f08c-159">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name*, *ZoneName*, and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="1f08c-160">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="1f08c-160">-ZoneName</span></span>
<span data-ttu-id="1f08c-161">指定要刪除包含 **RecordSet 的區域** 名稱。</span><span class="sxs-lookup"><span data-stu-id="1f08c-161">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="1f08c-162">您也必須指定 *Name* 和 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="1f08c-162">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="1f08c-163">或者，您可以使用 *RecordSet* 參數或 Name 和 Zone 參數來 *指定\*\*記錄* 集。</span><span class="sxs-lookup"><span data-stu-id="1f08c-163">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="1f08c-164">-確認</span><span class="sxs-lookup"><span data-stu-id="1f08c-164">-Confirm</span></span>
<span data-ttu-id="1f08c-165">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1f08c-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f08c-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f08c-166">-WhatIf</span></span>
<span data-ttu-id="1f08c-167">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1f08c-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f08c-168">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1f08c-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f08c-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f08c-169">CommonParameters</span></span>
<span data-ttu-id="1f08c-170">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1f08c-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f08c-171">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1f08c-171">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f08c-172">輸入</span><span class="sxs-lookup"><span data-stu-id="1f08c-172">INPUTS</span></span>

### <span data-ttu-id="1f08c-173">Microsoft.Azure.management.dns.models.RecordType</span><span class="sxs-lookup"><span data-stu-id="1f08c-173">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="1f08c-174">System.String</span><span class="sxs-lookup"><span data-stu-id="1f08c-174">System.String</span></span>

### <span data-ttu-id="1f08c-175">Microsoft.Azure.Commands.dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="1f08c-175">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="1f08c-176">Microsoft.Azure.Commands.dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1f08c-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="1f08c-177">輸出</span><span class="sxs-lookup"><span data-stu-id="1f08c-177">OUTPUTS</span></span>

### <span data-ttu-id="1f08c-178">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1f08c-178">System.Boolean</span></span>

## <span data-ttu-id="1f08c-179">筆記</span><span class="sxs-lookup"><span data-stu-id="1f08c-179">NOTES</span></span>
<span data-ttu-id="1f08c-180">您可以使用 *確認參數來控制* 此 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1f08c-180">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="1f08c-181">根據預設，如果 Windows PowerShell 變數的 $ConfirmPreference中或較低值，Cmdlet 會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1f08c-181">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="1f08c-182">如果您 *指定確認或* 確認 *：$True，* 此 Cmdlet 會先提示您確認再執行。</span><span class="sxs-lookup"><span data-stu-id="1f08c-182">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="1f08c-183">如果您指定 *確認：$False，Cmdlet* 不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1f08c-183">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="1f08c-184">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f08c-184">RELATED LINKS</span></span>

[<span data-ttu-id="1f08c-185">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1f08c-185">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="1f08c-186">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1f08c-186">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="1f08c-187">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1f08c-187">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
