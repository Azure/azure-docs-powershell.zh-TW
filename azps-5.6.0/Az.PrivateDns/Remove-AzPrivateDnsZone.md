---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/remove-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
ms.openlocfilehash: 8c8e7059a6c23c928180b8d6fab3cfdbbfd9ed5d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906525"
---
# <span data-ttu-id="4faa4-101">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="4faa4-101">Remove-AzPrivateDnsZone</span></span>

## <span data-ttu-id="4faa4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4faa4-102">SYNOPSIS</span></span>
<span data-ttu-id="4faa4-103">從資源群組移除私人 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="4faa4-103">Removes a private DNS zone from a resource group.</span></span>

## <span data-ttu-id="4faa4-104">語法</span><span class="sxs-lookup"><span data-stu-id="4faa4-104">SYNTAX</span></span>

### <span data-ttu-id="4faa4-105">欄位 (預設) </span><span class="sxs-lookup"><span data-stu-id="4faa4-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4faa4-106">物件</span><span class="sxs-lookup"><span data-stu-id="4faa4-106">Object</span></span>
```
Remove-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4faa4-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4faa4-107">ResourceId</span></span>
```
Remove-AzPrivateDnsZone -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4faa4-108">描述</span><span class="sxs-lookup"><span data-stu-id="4faa4-108">DESCRIPTION</span></span>
<span data-ttu-id="4faa4-109">**Remove-AzPrivateDnsZone Cmdlet** 會永久刪除指定資源群組 (DNS) 區域的私人網域名稱系統。</span><span class="sxs-lookup"><span data-stu-id="4faa4-109">The **Remove-AzPrivateDnsZone** cmdlet permanently deletes a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="4faa4-110">區域中包含的所有記錄集也會一併刪除。</span><span class="sxs-lookup"><span data-stu-id="4faa4-110">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="4faa4-111">您可以使用 PrivateZone 參數或管道運算子傳遞 **PrivateDnsZone** 物件，或者您也可以指定 *Name* 和 *ResourceGroupName* 參數。 </span><span class="sxs-lookup"><span data-stu-id="4faa4-111">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="4faa4-112">您可以使用確認參數$ConfirmPreference Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4faa4-112">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="4faa4-113">使用透過管線或區域參數) 傳遞 **的 PrivateDnsZone** 物件 (來指定區域時，如果區域在 Azure DNS 中已經變更，則自已取回本地 **PrivateDnsZone** 物件之後 (只有在 DNS 區域資源計數為變更的作業時，區域的記錄集作業不會) 。</span><span class="sxs-lookup"><span data-stu-id="4faa4-113">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="4faa4-114">這可保護同時區域變更。</span><span class="sxs-lookup"><span data-stu-id="4faa4-114">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="4faa4-115">您可以使用覆寫參數隱藏此設定，無論同時變更，都會刪除該區域。</span><span class="sxs-lookup"><span data-stu-id="4faa4-115">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="4faa4-116">例子</span><span class="sxs-lookup"><span data-stu-id="4faa4-116">EXAMPLES</span></span>

### <span data-ttu-id="4faa4-117">範例 1：移除私人區域</span><span class="sxs-lookup"><span data-stu-id="4faa4-117">Example 1: Remove a private zone</span></span>
```
PS C:\>Remove-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="4faa4-118">此命令會從名為 MyResourceGroup myzone.com資源群組移除名為 myResourceGroup 的區域。</span><span class="sxs-lookup"><span data-stu-id="4faa4-118">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="4faa4-119">參數</span><span class="sxs-lookup"><span data-stu-id="4faa4-119">PARAMETERS</span></span>

### <span data-ttu-id="4faa4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4faa4-120">-DefaultProfile</span></span>
<span data-ttu-id="4faa4-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="4faa4-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4faa4-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="4faa4-122">-Name</span></span>
<span data-ttu-id="4faa4-123">指定此 Cmdlet 移除的專用 DNS 區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="4faa4-123">Specifies the name of the private DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="4faa4-124">您也必須指定 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="4faa4-124">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="4faa4-125">或者，您可以使用 Zone 參數指定 DNS *區域。*</span><span class="sxs-lookup"><span data-stu-id="4faa4-125">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4faa4-126">-覆寫</span><span class="sxs-lookup"><span data-stu-id="4faa4-126">-Overwrite</span></span>
<span data-ttu-id="4faa4-127">使用透過管線或區域參數) 傳遞 **的 PrivateDnsZone** 物件 (來指定區域時，如果區域在 Azure DNS 中已經變更，則自已取回本地 **PrivateDnsZone** 物件之後 (只有在 DNS 區域資源計數為變更的作業時，區域的記錄集作業不會) 。</span><span class="sxs-lookup"><span data-stu-id="4faa4-127">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="4faa4-128">這可保護同時區域變更。</span><span class="sxs-lookup"><span data-stu-id="4faa4-128">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="4faa4-129">您可以使用覆寫參數隱藏此設定，無論同時變更，都會刪除該區域。</span><span class="sxs-lookup"><span data-stu-id="4faa4-129">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="4faa4-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4faa4-130">-PassThru</span></span>
<span data-ttu-id="4faa4-131">用來傳遞作業中 (布林值) 刪除管線下一個私人區域。</span><span class="sxs-lookup"><span data-stu-id="4faa4-131">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="4faa4-132">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="4faa4-132">-PrivateZone</span></span>
<span data-ttu-id="4faa4-133">要刪除的私人區域物件。</span><span class="sxs-lookup"><span data-stu-id="4faa4-133">The private zone object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4faa4-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4faa4-134">-ResourceGroupName</span></span>
<span data-ttu-id="4faa4-135">指定包含要移除之區域的資源組名。</span><span class="sxs-lookup"><span data-stu-id="4faa4-135">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="4faa4-136">您也必須指定 *ZoneName* 參數。</span><span class="sxs-lookup"><span data-stu-id="4faa4-136">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="4faa4-137">或者，您可以使用透過管線或 Zone 參數傳遞 **的 PrivateDnsZone** 物件來指定 *DNS* 區域。</span><span class="sxs-lookup"><span data-stu-id="4faa4-137">Alternatively, you can specify the DNS zone using a **PrivateDnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4faa4-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4faa4-138">-ResourceId</span></span>
<span data-ttu-id="4faa4-139">私人 DNS 區域資源ID。</span><span class="sxs-lookup"><span data-stu-id="4faa4-139">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4faa4-140">-確認</span><span class="sxs-lookup"><span data-stu-id="4faa4-140">-Confirm</span></span>
<span data-ttu-id="4faa4-141">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4faa4-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4faa4-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4faa4-142">-WhatIf</span></span>
<span data-ttu-id="4faa4-143">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4faa4-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4faa4-144">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4faa4-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4faa4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4faa4-145">CommonParameters</span></span>
<span data-ttu-id="4faa4-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4faa4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4faa4-147">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4faa4-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4faa4-148">輸入</span><span class="sxs-lookup"><span data-stu-id="4faa4-148">INPUTS</span></span>

### <span data-ttu-id="4faa4-149">Microsoft.Azure.Commands.PrivateDns.models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="4faa4-149">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="4faa4-150">System.String</span><span class="sxs-lookup"><span data-stu-id="4faa4-150">System.String</span></span>

## <span data-ttu-id="4faa4-151">輸出</span><span class="sxs-lookup"><span data-stu-id="4faa4-151">OUTPUTS</span></span>

### <span data-ttu-id="4faa4-152">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4faa4-152">System.Boolean</span></span>

## <span data-ttu-id="4faa4-153">筆記</span><span class="sxs-lookup"><span data-stu-id="4faa4-153">NOTES</span></span>

## <span data-ttu-id="4faa4-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="4faa4-154">RELATED LINKS</span></span>

[<span data-ttu-id="4faa4-155">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="4faa4-155">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="4faa4-156">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="4faa4-156">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="4faa4-157">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="4faa4-157">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
