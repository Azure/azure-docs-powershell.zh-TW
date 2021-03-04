---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/powershell/module/az.dns/remove-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
ms.openlocfilehash: 8c1058345d78289a7601fa390e202e428554b50c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910122"
---
# <span data-ttu-id="61134-101">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="61134-101">Remove-AzDnsZone</span></span>

## <span data-ttu-id="61134-102">簡介</span><span class="sxs-lookup"><span data-stu-id="61134-102">SYNOPSIS</span></span>
<span data-ttu-id="61134-103">從資源群組移除 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="61134-103">Removes a DNS zone from a resource group.</span></span>

## <span data-ttu-id="61134-104">語法</span><span class="sxs-lookup"><span data-stu-id="61134-104">SYNTAX</span></span>

### <span data-ttu-id="61134-105">領域</span><span class="sxs-lookup"><span data-stu-id="61134-105">Fields</span></span>
```
Remove-AzDnsZone -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61134-106">物件</span><span class="sxs-lookup"><span data-stu-id="61134-106">Object</span></span>
```
Remove-AzDnsZone -Zone <DnsZone> [-Overwrite] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61134-107">描述</span><span class="sxs-lookup"><span data-stu-id="61134-107">DESCRIPTION</span></span>
<span data-ttu-id="61134-108">**Remove-AzDnsZone** Cmdlet 會永久刪除指定資源 (DNS) 區域中的網域名稱系統。</span><span class="sxs-lookup"><span data-stu-id="61134-108">The **Remove-AzDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="61134-109">區域中包含的所有記錄集也會一併刪除。</span><span class="sxs-lookup"><span data-stu-id="61134-109">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="61134-110">您可以使用 Name 參數或管道運算子傳遞 **DnsZone** 物件，或者您也可以指定 *ZoneName* 和 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="61134-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="61134-111">您可以使用確認參數$ConfirmPreference Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="61134-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="61134-112">使用透過管線或區域參數) 傳遞 **的 Dns Zone** 物件 (來指定區域時，如果區域在 Azure DNS 中已經變更，則區域不會刪除，因為已取回本地 **Dns Zone** 物件 (只有直接在 DNS 區域資源計數上執行作業做為變更，區域中的記錄集作業不會) 。</span><span class="sxs-lookup"><span data-stu-id="61134-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="61134-113">這可保護同時區域變更。</span><span class="sxs-lookup"><span data-stu-id="61134-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="61134-114">您可以使用覆寫參數隱藏此設定，無論同時變更，都會刪除該區域。</span><span class="sxs-lookup"><span data-stu-id="61134-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="61134-115">例子</span><span class="sxs-lookup"><span data-stu-id="61134-115">EXAMPLES</span></span>

### <span data-ttu-id="61134-116">範例 1：移除區域</span><span class="sxs-lookup"><span data-stu-id="61134-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="61134-117">此命令會從名為 MyResourceGroup myzone.com資源群組移除名為 myResourceGroup 的區域。</span><span class="sxs-lookup"><span data-stu-id="61134-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="61134-118">參數</span><span class="sxs-lookup"><span data-stu-id="61134-118">PARAMETERS</span></span>

### <span data-ttu-id="61134-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61134-119">-DefaultProfile</span></span>
<span data-ttu-id="61134-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="61134-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61134-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="61134-121">-Name</span></span>
<span data-ttu-id="61134-122">指定此 Cmdlet 移除的 DNS 區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="61134-122">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="61134-123">您也必須指定 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="61134-123">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="61134-124">或者，您可以使用 Zone 參數指定 DNS *區域。*</span><span class="sxs-lookup"><span data-stu-id="61134-124">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="61134-125">-覆寫</span><span class="sxs-lookup"><span data-stu-id="61134-125">-Overwrite</span></span>
<span data-ttu-id="61134-126">使用透過管線或區域參數) 傳遞 **的 Dns Zone** 物件 (來指定區域時，如果區域在 Azure DNS 中已經變更，則區域不會刪除，因為已取回本地 **Dns Zone** 物件 (只有直接在 DNS 區域資源計數上執行作業做為變更，區域中的記錄集作業不會) 。</span><span class="sxs-lookup"><span data-stu-id="61134-126">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="61134-127">這可保護同時區域變更。</span><span class="sxs-lookup"><span data-stu-id="61134-127">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="61134-128">您可以使用覆寫參數隱藏此設定，無論同時變更，都會刪除該區域。</span><span class="sxs-lookup"><span data-stu-id="61134-128">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="61134-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61134-129">-PassThru</span></span>
<span data-ttu-id="61134-130">Passthru</span><span class="sxs-lookup"><span data-stu-id="61134-130">passthru</span></span>

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

### <span data-ttu-id="61134-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61134-131">-ResourceGroupName</span></span>
<span data-ttu-id="61134-132">指定包含要移除之區域的資源組名。</span><span class="sxs-lookup"><span data-stu-id="61134-132">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="61134-133">您也必須指定 *ZoneName* 參數。</span><span class="sxs-lookup"><span data-stu-id="61134-133">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="61134-134">或者，您可以使用透過管線或區域參數傳遞的 **Dns Zone** 物件來指定 *DNS* 區域。</span><span class="sxs-lookup"><span data-stu-id="61134-134">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="61134-135">-區域</span><span class="sxs-lookup"><span data-stu-id="61134-135">-Zone</span></span>
<span data-ttu-id="61134-136">指定要刪除的 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="61134-136">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="61134-137">傳遞 **的 DnsZone** 物件也可以透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="61134-137">The **DnsZone** object passed can also be passed via the pipeline.</span></span>
<span data-ttu-id="61134-138">或者，您可以使用 *ZoneName* 和 *ResourceGroupName* 參數指定要刪除的 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="61134-138">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="61134-139">-確認</span><span class="sxs-lookup"><span data-stu-id="61134-139">-Confirm</span></span>
<span data-ttu-id="61134-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="61134-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61134-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61134-141">-WhatIf</span></span>
<span data-ttu-id="61134-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="61134-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61134-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="61134-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61134-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61134-144">CommonParameters</span></span>
<span data-ttu-id="61134-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="61134-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61134-146">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="61134-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61134-147">輸入</span><span class="sxs-lookup"><span data-stu-id="61134-147">INPUTS</span></span>

### <span data-ttu-id="61134-148">System.String</span><span class="sxs-lookup"><span data-stu-id="61134-148">System.String</span></span>

### <span data-ttu-id="61134-149">Microsoft.Azure.Commands.dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="61134-149">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="61134-150">輸出</span><span class="sxs-lookup"><span data-stu-id="61134-150">OUTPUTS</span></span>

### <span data-ttu-id="61134-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="61134-151">System.Boolean</span></span>

## <span data-ttu-id="61134-152">筆記</span><span class="sxs-lookup"><span data-stu-id="61134-152">NOTES</span></span>
<span data-ttu-id="61134-153">由於刪除 DNS 區域的潛在嚴重影響，此 Cmdlet 預設會提示確認 $ConfirmPreference Windows PowerShell 變數有 None 外的任何值。</span><span class="sxs-lookup"><span data-stu-id="61134-153">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>
<span data-ttu-id="61134-154">如果您 *指定確認或* 確認 *：$True，* 此 Cmdlet 會先提示您確認再執行。</span><span class="sxs-lookup"><span data-stu-id="61134-154">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="61134-155">如果您指定 *確認：$False，Cmdlet* 不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="61134-155">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="61134-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="61134-156">RELATED LINKS</span></span>

[<span data-ttu-id="61134-157">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="61134-157">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="61134-158">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="61134-158">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="61134-159">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="61134-159">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)
