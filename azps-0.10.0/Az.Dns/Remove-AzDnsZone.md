---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsZone.md
ms.openlocfilehash: bc77e2c69f285f0acab0bed8e6a40592374ebd18
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794796"
---
# <span data-ttu-id="13d46-101">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="13d46-101">Remove-AzDnsZone</span></span>

## <span data-ttu-id="13d46-102">摘要</span><span class="sxs-lookup"><span data-stu-id="13d46-102">SYNOPSIS</span></span>
<span data-ttu-id="13d46-103">從資源群組中移除 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="13d46-103">Removes a DNS zone from a resource group.</span></span>

## <span data-ttu-id="13d46-104">句法</span><span class="sxs-lookup"><span data-stu-id="13d46-104">SYNTAX</span></span>

### <span data-ttu-id="13d46-105">區域</span><span class="sxs-lookup"><span data-stu-id="13d46-105">Fields</span></span>
```
Remove-AzDnsZone -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13d46-106">面向</span><span class="sxs-lookup"><span data-stu-id="13d46-106">Object</span></span>
```
Remove-AzDnsZone -Zone <DnsZone> [-Overwrite] [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13d46-107">說明</span><span class="sxs-lookup"><span data-stu-id="13d46-107">DESCRIPTION</span></span>
<span data-ttu-id="13d46-108">AzDnsZone Cmdlet 會從指定 **的** 資源群組中永久刪除網域名稱系統 (DNS) 區域。</span><span class="sxs-lookup"><span data-stu-id="13d46-108">The **Remove-AzDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="13d46-109">該區域中包含的所有記錄集也都會刪除。</span><span class="sxs-lookup"><span data-stu-id="13d46-109">All record sets contained in the zone are also deleted.</span></span>

<span data-ttu-id="13d46-110">您可以使用 *Name* 參數或使用管線運算子來傳遞 **DnsZone** 物件，或者也可以指定 *ZoneName* 和 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="13d46-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="13d46-111">您可以使用 Confirm 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="13d46-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="13d46-112">使用 **DnsZone** 物件來指定區域時 (透過管線或 *zone* 參數) ，如果您自本機 **DnsZone** 物件檢索之後，在 Azure DNS 中已變更，該區域就不會被刪除 (在該區域內，記錄集的操作不) 。</span><span class="sxs-lookup"><span data-stu-id="13d46-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="13d46-113">這可為併發區域變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="13d46-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="13d46-114">這個值可以使用 *Overwrite* 參數加以取消，不論併發變更為何，都會刪除該區域。</span><span class="sxs-lookup"><span data-stu-id="13d46-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="13d46-115">示例</span><span class="sxs-lookup"><span data-stu-id="13d46-115">EXAMPLES</span></span>

### <span data-ttu-id="13d46-116">範例1：移除區域</span><span class="sxs-lookup"><span data-stu-id="13d46-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="13d46-117">這個命令會從名為 MyResourceGroup 的資源群組中移除名為 myzone.com 的區域。</span><span class="sxs-lookup"><span data-stu-id="13d46-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="13d46-118">參數</span><span class="sxs-lookup"><span data-stu-id="13d46-118">PARAMETERS</span></span>

### <span data-ttu-id="13d46-119">-Force</span><span class="sxs-lookup"><span data-stu-id="13d46-119">-Force</span></span>
<span data-ttu-id="13d46-120">此 Cmdlet 已棄用此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="13d46-120">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="13d46-121">在未來版本中將會移除它。</span><span class="sxs-lookup"><span data-stu-id="13d46-121">It will be removed in a future release.</span></span>

<span data-ttu-id="13d46-122">若要控制此 Cmdlet 是否提示您進行確認，請使用 *Confirm* 參數。</span><span class="sxs-lookup"><span data-stu-id="13d46-122">To control whether this cmdlet prompts you for confirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="13d46-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="13d46-123">-Name</span></span>
<span data-ttu-id="13d46-124">指定此 Cmdlet 移除之 DNS 區域的名稱。</span><span class="sxs-lookup"><span data-stu-id="13d46-124">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="13d46-125">您也必須指定 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="13d46-125">You must also specify the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="13d46-126">或者，您也可以使用 *zone* 參數指定 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="13d46-126">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="13d46-127">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="13d46-127">-Overwrite</span></span>
<span data-ttu-id="13d46-128">使用 **DnsZone** 物件來指定區域時 (透過管線或 *zone* 參數) ，如果您自本機 **DnsZone** 物件檢索之後，在 Azure DNS 中已變更，該區域就不會被刪除 (在該區域內，記錄集的操作不) 。</span><span class="sxs-lookup"><span data-stu-id="13d46-128">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="13d46-129">這可為併發區域變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="13d46-129">This provides protection for concurrent zone changes.</span></span>

<span data-ttu-id="13d46-130">這個值可以使用 *Overwrite* 參數加以取消，不論併發變更為何，都會刪除該區域。</span><span class="sxs-lookup"><span data-stu-id="13d46-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="13d46-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13d46-131">-PassThru</span></span>
<span data-ttu-id="13d46-132">passthru</span><span class="sxs-lookup"><span data-stu-id="13d46-132">passthru</span></span>

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

### <span data-ttu-id="13d46-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13d46-133">-ResourceGroupName</span></span>
<span data-ttu-id="13d46-134">指定包含要移除之區域的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="13d46-134">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="13d46-135">您也必須指定 *ZoneName* 參數。</span><span class="sxs-lookup"><span data-stu-id="13d46-135">You must also specify the *ZoneName* parameter.</span></span>

<span data-ttu-id="13d46-136">或者，您也可以使用 **DnsZone** 物件來指定 DNS 區域，方法是透過管線或 *zone* 參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="13d46-136">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="13d46-137">-Zone</span><span class="sxs-lookup"><span data-stu-id="13d46-137">-Zone</span></span>
<span data-ttu-id="13d46-138">指定要刪除的 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="13d46-138">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="13d46-139">傳遞的 **DnsZone** 物件也可以透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="13d46-139">The **DnsZone** object passed can also be passed via the pipeline.</span></span>

<span data-ttu-id="13d46-140">或者，您也可以使用 *ZoneName* 和 *ResourceGroupName* 參數指定要刪除的 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="13d46-140">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="13d46-141">-確認</span><span class="sxs-lookup"><span data-stu-id="13d46-141">-Confirm</span></span>
<span data-ttu-id="13d46-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="13d46-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13d46-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13d46-143">-WhatIf</span></span>
<span data-ttu-id="13d46-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="13d46-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13d46-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="13d46-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13d46-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13d46-146">CommonParameters</span></span>
<span data-ttu-id="13d46-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="13d46-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13d46-148">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="13d46-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13d46-149">輸入</span><span class="sxs-lookup"><span data-stu-id="13d46-149">INPUTS</span></span>

### <span data-ttu-id="13d46-150">DnsZone （）</span><span class="sxs-lookup"><span data-stu-id="13d46-150">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="13d46-151">您可以將 **DnsZone** 物件輸送到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="13d46-151">You can pipe a **DnsZone** object to this cmdlet.</span></span>

## <span data-ttu-id="13d46-152">輸出</span><span class="sxs-lookup"><span data-stu-id="13d46-152">OUTPUTS</span></span>

### <span data-ttu-id="13d46-153">所有</span><span class="sxs-lookup"><span data-stu-id="13d46-153">None</span></span>
<span data-ttu-id="13d46-154">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="13d46-154">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="13d46-155">筆記</span><span class="sxs-lookup"><span data-stu-id="13d46-155">NOTES</span></span>
<span data-ttu-id="13d46-156">由於刪除 DNS 區域可能會產生很大的影響，因此如果 $ConfirmPreference 的 Windows PowerShell 變數具有 None 以外的任何值，這個 Cmdlet 會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="13d46-156">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>

<span data-ttu-id="13d46-157">如果您指定 [ *確認* ] 或 [ *確認]： $True* ，此 Cmdlet 會在您執行之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="13d46-157">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="13d46-158">如果您指定 [ *確認： $False* ]，則 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="13d46-158">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="13d46-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="13d46-159">RELATED LINKS</span></span>

[<span data-ttu-id="13d46-160">AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="13d46-160">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="13d46-161">新-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="13d46-161">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="13d46-162">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="13d46-162">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)
