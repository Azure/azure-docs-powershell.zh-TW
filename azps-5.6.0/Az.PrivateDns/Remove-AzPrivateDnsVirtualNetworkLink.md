---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/powershell/module/az.privatedns/remove-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 8de4922b5d71902fe22a17a6c02f21a40e35ddc7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905310"
---
# <span data-ttu-id="b96c8-101">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="b96c8-101">Remove-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="b96c8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b96c8-102">SYNOPSIS</span></span>
<span data-ttu-id="b96c8-103">從資源群組移除虛擬網路連結。</span><span class="sxs-lookup"><span data-stu-id="b96c8-103">Removes a virtual network link from a resource group.</span></span>

## <span data-ttu-id="b96c8-104">語法</span><span class="sxs-lookup"><span data-stu-id="b96c8-104">SYNTAX</span></span>

### <span data-ttu-id="b96c8-105">欄位 (預設) </span><span class="sxs-lookup"><span data-stu-id="b96c8-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b96c8-106">物件</span><span class="sxs-lookup"><span data-stu-id="b96c8-106">Object</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b96c8-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b96c8-107">ResourceId</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b96c8-108">描述</span><span class="sxs-lookup"><span data-stu-id="b96c8-108">DESCRIPTION</span></span>
<span data-ttu-id="b96c8-109">**Remove-AzPrivateDnsVirtualNetworkLink** Cmdlet 會永久刪除指定資源群組中的私人網域名稱系統 (DNS) 連結。</span><span class="sxs-lookup"><span data-stu-id="b96c8-109">The **Remove-AzPrivateDnsVirtualNetworkLink** cmdlet permanently deletes a private Domain Name System (DNS) link from a specified resource group.</span></span>
<span data-ttu-id="b96c8-110">您可以使用 *Link* 參數或管道運算子傳遞 **PSPrivateDnsVirtualNetworkLink** 物件，或者您也可以指定 *Name* *ZoneName* 和 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="b96c8-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="b96c8-111">您可以使用確認參數$ConfirmPreference Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b96c8-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="b96c8-112">使用透過管線或連結參數) 傳遞 **的 PSPrivateDnsVirtualNetworkLink** 物件 (指定連結時，如果連結在 Azure Private DNS 中已經變更，則自已取回本地 **PSPrivateDnsVirtualNetworkLink** 物件之後，不會刪除該連結。</span><span class="sxs-lookup"><span data-stu-id="b96c8-112">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure Private DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="b96c8-113">這可保護同時區域變更。</span><span class="sxs-lookup"><span data-stu-id="b96c8-113">This provides protection for concurrent zone changes.</span></span> <span data-ttu-id="b96c8-114">您可以使用覆寫參數隱藏此設定，無論同時變更，都會刪除該區域。</span><span class="sxs-lookup"><span data-stu-id="b96c8-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="b96c8-115">例子</span><span class="sxs-lookup"><span data-stu-id="b96c8-115">EXAMPLES</span></span>

### <span data-ttu-id="b96c8-116">範例 1：移除連結</span><span class="sxs-lookup"><span data-stu-id="b96c8-116">Example 1: Remove a link</span></span>
```
PS C:\>Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"
```

<span data-ttu-id="b96c8-117">此命令會從名為 MyResourceGroup 的資源群組移除連結至區域myzone.com名為 mylink 的連結。</span><span class="sxs-lookup"><span data-stu-id="b96c8-117">This command removes the link named mylink linked to zone myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="b96c8-118">參數</span><span class="sxs-lookup"><span data-stu-id="b96c8-118">PARAMETERS</span></span>

### <span data-ttu-id="b96c8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b96c8-119">-DefaultProfile</span></span>
<span data-ttu-id="b96c8-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="b96c8-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b96c8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b96c8-121">-InputObject</span></span>
<span data-ttu-id="b96c8-122">要移除的虛擬網路連結化物件。</span><span class="sxs-lookup"><span data-stu-id="b96c8-122">The virtual network link object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b96c8-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="b96c8-123">-Name</span></span>
<span data-ttu-id="b96c8-124">指定要刪除的連結名稱。</span><span class="sxs-lookup"><span data-stu-id="b96c8-124">Specifies the name of the link to be deleted.</span></span>
<span data-ttu-id="b96c8-125">您也必須指定 *ResourceGroupName 和* *ZoneName* 參數。</span><span class="sxs-lookup"><span data-stu-id="b96c8-125">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="b96c8-126">或者，您可以使用 Link 參數指定 *連結* 。</span><span class="sxs-lookup"><span data-stu-id="b96c8-126">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="b96c8-127">-覆寫</span><span class="sxs-lookup"><span data-stu-id="b96c8-127">-Overwrite</span></span>
<span data-ttu-id="b96c8-128">使用 **PSPrivateDnsVirtualNetworkLink** 物件 (透過管線或 *Link* 參數) 指定區域時，如果區域在 Azure DNS 中已經變更，則自已取回本地 **PSPrivateDnsVirtualNetworkLink** 物件之後，不會刪除該區域。</span><span class="sxs-lookup"><span data-stu-id="b96c8-128">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="b96c8-129">這可保護同時區域變更。</span><span class="sxs-lookup"><span data-stu-id="b96c8-129">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="b96c8-130">您可以使用覆寫參數隱藏此設定，無論同時變更，都會刪除該區域。</span><span class="sxs-lookup"><span data-stu-id="b96c8-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="b96c8-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b96c8-131">-PassThru</span></span>
<span data-ttu-id="b96c8-132">用來傳遞作業結果 (布林值) 刪除管線下一個虛擬網路連結。</span><span class="sxs-lookup"><span data-stu-id="b96c8-132">Used for passing the result (boolean) of the operation delete virtual network link further down the pipeline.</span></span>

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

### <span data-ttu-id="b96c8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b96c8-133">-ResourceGroupName</span></span>
<span data-ttu-id="b96c8-134">指定包含要移除之連結的資源組名。</span><span class="sxs-lookup"><span data-stu-id="b96c8-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="b96c8-135">您也必須指定 *ZoneName 和* *Name* 參數。</span><span class="sxs-lookup"><span data-stu-id="b96c8-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="b96c8-136">或者，您可以使用透過管線或 Link 參數傳遞 **的 PSPrivateDnsVirtualNetworkLink** 物件來 *指定 DNS* 區域。</span><span class="sxs-lookup"><span data-stu-id="b96c8-136">Alternatively, you can specify the DNS zone using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="b96c8-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b96c8-137">-ResourceId</span></span>
<span data-ttu-id="b96c8-138">指定連結的 ARM 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b96c8-138">Specifies the ARM resource ID of the link.</span></span>

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

### <span data-ttu-id="b96c8-139">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="b96c8-139">-ZoneName</span></span>
<span data-ttu-id="b96c8-140">指定連結相關聯的私人 DNS 區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="b96c8-140">Specifies the name of the private DNS zone that the link is associated with.</span></span>
<span data-ttu-id="b96c8-141">您也必須指定 *ResourceGroupName 和* *Name* 參數。</span><span class="sxs-lookup"><span data-stu-id="b96c8-141">You must also specify the *ResourceGroupName* and *Name* parameter.</span></span>
<span data-ttu-id="b96c8-142">或者，您可以使用 Link 參數指定 *連結* 。</span><span class="sxs-lookup"><span data-stu-id="b96c8-142">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="b96c8-143">-確認</span><span class="sxs-lookup"><span data-stu-id="b96c8-143">-Confirm</span></span>
<span data-ttu-id="b96c8-144">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b96c8-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b96c8-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b96c8-145">-WhatIf</span></span>
<span data-ttu-id="b96c8-146">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b96c8-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b96c8-147">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b96c8-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b96c8-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b96c8-148">CommonParameters</span></span>
<span data-ttu-id="b96c8-149">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b96c8-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b96c8-150">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b96c8-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b96c8-151">輸入</span><span class="sxs-lookup"><span data-stu-id="b96c8-151">INPUTS</span></span>

### <span data-ttu-id="b96c8-152">Microsoft.Azure.Commands.PrivateDns.models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="b96c8-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="b96c8-153">System.String</span><span class="sxs-lookup"><span data-stu-id="b96c8-153">System.String</span></span>

## <span data-ttu-id="b96c8-154">輸出</span><span class="sxs-lookup"><span data-stu-id="b96c8-154">OUTPUTS</span></span>

### <span data-ttu-id="b96c8-155">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b96c8-155">System.Boolean</span></span>

## <span data-ttu-id="b96c8-156">筆記</span><span class="sxs-lookup"><span data-stu-id="b96c8-156">NOTES</span></span>

## <span data-ttu-id="b96c8-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="b96c8-157">RELATED LINKS</span></span>

[<span data-ttu-id="b96c8-158">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="b96c8-158">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="b96c8-159">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="b96c8-159">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="b96c8-160">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="b96c8-160">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
