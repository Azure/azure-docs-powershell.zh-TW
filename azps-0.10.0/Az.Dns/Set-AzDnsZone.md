---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsZone.md
ms.openlocfilehash: 9b6d84f9007a872db0e41efa78d8e16d7269eb02
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794791"
---
# <span data-ttu-id="6985b-101">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="6985b-101">Set-AzDnsZone</span></span>

## <span data-ttu-id="6985b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6985b-102">SYNOPSIS</span></span>
<span data-ttu-id="6985b-103">更新 DNS 區域的屬性。</span><span class="sxs-lookup"><span data-stu-id="6985b-103">Updates the properties of a DNS zone.</span></span>

## <span data-ttu-id="6985b-104">句法</span><span class="sxs-lookup"><span data-stu-id="6985b-104">SYNTAX</span></span>

### <span data-ttu-id="6985b-105">區域</span><span class="sxs-lookup"><span data-stu-id="6985b-105">Fields</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6985b-106">面向</span><span class="sxs-lookup"><span data-stu-id="6985b-106">Object</span></span>
```
Set-AzDnsZone -Zone <DnsZone> [-Overwrite] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6985b-107">說明</span><span class="sxs-lookup"><span data-stu-id="6985b-107">DESCRIPTION</span></span>
<span data-ttu-id="6985b-108">**AzDnsZone** Cmdlet 會更新 Azure DNS 服務中指定的 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="6985b-108">The **Set-AzDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="6985b-109">這個 Cmdlet 不會更新區域中的記錄集。</span><span class="sxs-lookup"><span data-stu-id="6985b-109">This cmdlet does not update the record sets in the zone.</span></span>

<span data-ttu-id="6985b-110">您可以將 **DnsZone** 物件傳遞為參數或使用管線運算子，或者也可以指定 *ZoneName* 和 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="6985b-110">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="6985b-111">您可以使用 *Confirm* 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6985b-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="6985b-112">當您使用 Zone 物件或透過) 管線將 DNS 區域傳輸成物件 (，如果在已檢索到本機 DnsZone 物件之後，在 Azure DNS 中已變更，則不會更新它。</span><span class="sxs-lookup"><span data-stu-id="6985b-112">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="6985b-113">這可為併發變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="6985b-113">This provides protection for concurrent changes.</span></span> <span data-ttu-id="6985b-114">您可以使用 *Overwrite* 參數來抑制此行為，不論併發變更為何，都會更新區域。</span><span class="sxs-lookup"><span data-stu-id="6985b-114">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="6985b-115">示例</span><span class="sxs-lookup"><span data-stu-id="6985b-115">EXAMPLES</span></span>

### <span data-ttu-id="6985b-116">範例1：更新 DNS 區域</span><span class="sxs-lookup"><span data-stu-id="6985b-116">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzDnsZone -Zone $Zone
```

<span data-ttu-id="6985b-117">第一個命令會從指定的資源群組中取得名為 myzone.com 的區域，然後將它儲存在 $Zone 變數中。</span><span class="sxs-lookup"><span data-stu-id="6985b-117">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

<span data-ttu-id="6985b-118">第二個命令會更新 $Zone 的標記。</span><span class="sxs-lookup"><span data-stu-id="6985b-118">The second command updates the tags for $Zone.</span></span>

<span data-ttu-id="6985b-119">最後一個命令會提交變更。</span><span class="sxs-lookup"><span data-stu-id="6985b-119">The final command commits the change.</span></span>

### <span data-ttu-id="6985b-120">範例2：更新區域的標記</span><span class="sxs-lookup"><span data-stu-id="6985b-120">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="6985b-121">這個命令會更新名為 myzone.com 區域的標籤，而不需要先明確取得該區域。</span><span class="sxs-lookup"><span data-stu-id="6985b-121">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

## <span data-ttu-id="6985b-122">參數</span><span class="sxs-lookup"><span data-stu-id="6985b-122">PARAMETERS</span></span>

### <span data-ttu-id="6985b-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="6985b-123">-Name</span></span>
<span data-ttu-id="6985b-124">指定要更新之 DNS 區域的名稱。</span><span class="sxs-lookup"><span data-stu-id="6985b-124">Specifies the name of the DNS zone to update.</span></span>

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

### <span data-ttu-id="6985b-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="6985b-125">-Overwrite</span></span>
<span data-ttu-id="6985b-126">當您使用 Zone 物件或透過) 管線將 DNS 區域傳輸成物件 (，如果在已檢索到本機 DnsZone 物件之後，在 Azure DNS 中已變更，則不會更新它。</span><span class="sxs-lookup"><span data-stu-id="6985b-126">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="6985b-127">這可為併發變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="6985b-127">This provides protection for concurrent changes.</span></span> <span data-ttu-id="6985b-128">您可以使用 *Overwrite* 參數來抑制此行為，不論併發變更為何，都會更新區域。</span><span class="sxs-lookup"><span data-stu-id="6985b-128">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="6985b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6985b-129">-ResourceGroupName</span></span>
<span data-ttu-id="6985b-130">指定包含要更新之區域之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6985b-130">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="6985b-131">您也必須指定 ZoneName 參數。</span><span class="sxs-lookup"><span data-stu-id="6985b-131">You must also specify the ZoneName parameter.</span></span>

<span data-ttu-id="6985b-132">或者，您也可以使用 DnsZone 物件與 *zone* 參數或管線來指定區域。</span><span class="sxs-lookup"><span data-stu-id="6985b-132">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

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

### <span data-ttu-id="6985b-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="6985b-133">-Tag</span></span>
<span data-ttu-id="6985b-134">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="6985b-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6985b-135">例如：</span><span class="sxs-lookup"><span data-stu-id="6985b-135">For example:</span></span>

<span data-ttu-id="6985b-136">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="6985b-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: Fields
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6985b-137">-Zone</span><span class="sxs-lookup"><span data-stu-id="6985b-137">-Zone</span></span>
<span data-ttu-id="6985b-138">指定要更新的 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="6985b-138">Specifies the DNS zone to update.</span></span>

<span data-ttu-id="6985b-139">或者，您也可以使用 *ZoneName* 和 *ResourceGroupName* 參數指定區域。</span><span class="sxs-lookup"><span data-stu-id="6985b-139">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="6985b-140">-確認</span><span class="sxs-lookup"><span data-stu-id="6985b-140">-Confirm</span></span>
<span data-ttu-id="6985b-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6985b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6985b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6985b-142">-WhatIf</span></span>
<span data-ttu-id="6985b-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6985b-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6985b-144">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6985b-144">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6985b-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6985b-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6985b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6985b-146">CommonParameters</span></span>
<span data-ttu-id="6985b-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6985b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6985b-148">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6985b-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6985b-149">輸入</span><span class="sxs-lookup"><span data-stu-id="6985b-149">INPUTS</span></span>

### <span data-ttu-id="6985b-150">DnsZone （）</span><span class="sxs-lookup"><span data-stu-id="6985b-150">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="6985b-151">您可以將 DnsZone 物件輸送到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6985b-151">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="6985b-152">輸出</span><span class="sxs-lookup"><span data-stu-id="6985b-152">OUTPUTS</span></span>

### <span data-ttu-id="6985b-153">DnsZone （）</span><span class="sxs-lookup"><span data-stu-id="6985b-153">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="6985b-154">這個 Cmdlet 會傳回 DnsZone 物件，該物件會以新的 Etag 表示已更新的 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="6985b-154">This cmdlet returns a DnsZone object that represents the updated DNS zone with a new Etag.</span></span>

## <span data-ttu-id="6985b-155">筆記</span><span class="sxs-lookup"><span data-stu-id="6985b-155">NOTES</span></span>
<span data-ttu-id="6985b-156">您可以使用 *Confirm* 參數來控制此 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6985b-156">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="6985b-157">根據預設，如果 $ConfirmPreference 的 Windows PowerShell 變數的值為 [中] 或 [低]，則該 Cmdlet 會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6985b-157">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="6985b-158">如果您指定 [ *確認* ] 或 [ *確認]： $True* ，此 Cmdlet 會在您執行之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6985b-158">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="6985b-159">如果您指定 [ *確認： $False* ]，則 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6985b-159">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6985b-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="6985b-160">RELATED LINKS</span></span>

[<span data-ttu-id="6985b-161">AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="6985b-161">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="6985b-162">新-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="6985b-162">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="6985b-163">移除-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="6985b-163">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)