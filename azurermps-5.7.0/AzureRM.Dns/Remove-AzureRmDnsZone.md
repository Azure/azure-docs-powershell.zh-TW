---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/remove-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsZone.md
ms.openlocfilehash: ac3f65ed82f9b04eb49e26a8cb03a3dcd8c9bc34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454252"
---
# <span data-ttu-id="f1720-101">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="f1720-101">Remove-AzureRmDnsZone</span></span>

## <span data-ttu-id="f1720-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f1720-102">SYNOPSIS</span></span>
<span data-ttu-id="f1720-103">從資源群組中移除 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="f1720-103">Removes a DNS zone from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1720-104">句法</span><span class="sxs-lookup"><span data-stu-id="f1720-104">SYNTAX</span></span>

### <span data-ttu-id="f1720-105">區域</span><span class="sxs-lookup"><span data-stu-id="f1720-105">Fields</span></span>
```
Remove-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1720-106">面向</span><span class="sxs-lookup"><span data-stu-id="f1720-106">Object</span></span>
```
Remove-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1720-107">說明</span><span class="sxs-lookup"><span data-stu-id="f1720-107">DESCRIPTION</span></span>
<span data-ttu-id="f1720-108">AzureRmDnsZone Cmdlet 會從指定 **的** 資源群組中永久刪除網域名稱系統 (DNS) 區域。</span><span class="sxs-lookup"><span data-stu-id="f1720-108">The **Remove-AzureRmDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="f1720-109">該區域中包含的所有記錄集也都會刪除。</span><span class="sxs-lookup"><span data-stu-id="f1720-109">All record sets contained in the zone are also deleted.</span></span>

<span data-ttu-id="f1720-110">您可以使用 *Name* 參數或使用管線運算子來傳遞 **DnsZone** 物件，或者也可以指定 *ZoneName* 和 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="f1720-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="f1720-111">您可以使用 Confirm 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f1720-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="f1720-112">使用 **DnsZone** 物件來指定區域時 (透過管線或 *zone* 參數) ，如果您自本機 **DnsZone** 物件檢索之後，在 Azure DNS 中已變更，該區域就不會被刪除 (在該區域內，記錄集的操作不) 。</span><span class="sxs-lookup"><span data-stu-id="f1720-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="f1720-113">這可為併發區域變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="f1720-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="f1720-114">這個值可以使用 *Overwrite* 參數加以取消，不論併發變更為何，都會刪除該區域。</span><span class="sxs-lookup"><span data-stu-id="f1720-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="f1720-115">示例</span><span class="sxs-lookup"><span data-stu-id="f1720-115">EXAMPLES</span></span>

### <span data-ttu-id="f1720-116">範例1：移除區域</span><span class="sxs-lookup"><span data-stu-id="f1720-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="f1720-117">這個命令會從名為 MyResourceGroup 的資源群組中移除名為 myzone.com 的區域。</span><span class="sxs-lookup"><span data-stu-id="f1720-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="f1720-118">參數</span><span class="sxs-lookup"><span data-stu-id="f1720-118">PARAMETERS</span></span>

### <span data-ttu-id="f1720-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1720-119">-DefaultProfile</span></span>
<span data-ttu-id="f1720-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f1720-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1720-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f1720-121">-Force</span></span>
<span data-ttu-id="f1720-122">此 Cmdlet 已棄用此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1720-122">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="f1720-123">在未來版本中將會移除它。</span><span class="sxs-lookup"><span data-stu-id="f1720-123">It will be removed in a future release.</span></span>

<span data-ttu-id="f1720-124">若要控制此 Cmdlet 是否提示您進行確認，請使用 *Confirm* 參數。</span><span class="sxs-lookup"><span data-stu-id="f1720-124">To control whether this cmdlet prompts you for confirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="f1720-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="f1720-125">-Name</span></span>
<span data-ttu-id="f1720-126">指定此 Cmdlet 移除之 DNS 區域的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1720-126">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="f1720-127">您也必須指定 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="f1720-127">You must also specify the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="f1720-128">或者，您也可以使用 *zone* 參數指定 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="f1720-128">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="f1720-129">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="f1720-129">-Overwrite</span></span>
<span data-ttu-id="f1720-130">使用 **DnsZone** 物件來指定區域時 (透過管線或 *zone* 參數) ，如果您自本機 **DnsZone** 物件檢索之後，在 Azure DNS 中已變更，該區域就不會被刪除 (在該區域內，記錄集的操作不) 。</span><span class="sxs-lookup"><span data-stu-id="f1720-130">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="f1720-131">這可為併發區域變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="f1720-131">This provides protection for concurrent zone changes.</span></span>

<span data-ttu-id="f1720-132">這個值可以使用 *Overwrite* 參數加以取消，不論併發變更為何，都會刪除該區域。</span><span class="sxs-lookup"><span data-stu-id="f1720-132">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="f1720-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1720-133">-PassThru</span></span>
<span data-ttu-id="f1720-134">passthru</span><span class="sxs-lookup"><span data-stu-id="f1720-134">passthru</span></span>

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

### <span data-ttu-id="f1720-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1720-135">-ResourceGroupName</span></span>
<span data-ttu-id="f1720-136">指定包含要移除之區域的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1720-136">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="f1720-137">您也必須指定 *ZoneName* 參數。</span><span class="sxs-lookup"><span data-stu-id="f1720-137">You must also specify the *ZoneName* parameter.</span></span>

<span data-ttu-id="f1720-138">或者，您也可以使用 **DnsZone** 物件來指定 DNS 區域，方法是透過管線或 *zone* 參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="f1720-138">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="f1720-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="f1720-139">-Zone</span></span>
<span data-ttu-id="f1720-140">指定要刪除的 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="f1720-140">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="f1720-141">傳遞的 **DnsZone** 物件也可以透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="f1720-141">The **DnsZone** object passed can also be passed via the pipeline.</span></span>

<span data-ttu-id="f1720-142">或者，您也可以使用 *ZoneName* 和 *ResourceGroupName* 參數指定要刪除的 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="f1720-142">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="f1720-143">-確認</span><span class="sxs-lookup"><span data-stu-id="f1720-143">-Confirm</span></span>
<span data-ttu-id="f1720-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f1720-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1720-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1720-145">-WhatIf</span></span>
<span data-ttu-id="f1720-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f1720-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1720-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1720-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1720-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1720-148">CommonParameters</span></span>
<span data-ttu-id="f1720-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f1720-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1720-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f1720-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1720-151">輸入</span><span class="sxs-lookup"><span data-stu-id="f1720-151">INPUTS</span></span>

### <span data-ttu-id="f1720-152">DnsZone （）</span><span class="sxs-lookup"><span data-stu-id="f1720-152">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="f1720-153">您可以將 **DnsZone** 物件輸送到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1720-153">You can pipe a **DnsZone** object to this cmdlet.</span></span>

## <span data-ttu-id="f1720-154">輸出</span><span class="sxs-lookup"><span data-stu-id="f1720-154">OUTPUTS</span></span>

### <span data-ttu-id="f1720-155">所有</span><span class="sxs-lookup"><span data-stu-id="f1720-155">None</span></span>
<span data-ttu-id="f1720-156">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="f1720-156">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="f1720-157">筆記</span><span class="sxs-lookup"><span data-stu-id="f1720-157">NOTES</span></span>
<span data-ttu-id="f1720-158">由於刪除 DNS 區域可能會產生很大的影響，因此如果 $ConfirmPreference 的 Windows PowerShell 變數具有 None 以外的任何值，這個 Cmdlet 會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f1720-158">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>

<span data-ttu-id="f1720-159">如果您指定 [ *確認* ] 或 [ *確認]： $True* ，此 Cmdlet 會在您執行之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f1720-159">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="f1720-160">如果您指定 [ *確認： $False* ]，則 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f1720-160">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="f1720-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1720-161">RELATED LINKS</span></span>

[<span data-ttu-id="f1720-162">AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="f1720-162">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="f1720-163">新-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="f1720-163">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="f1720-164">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="f1720-164">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
