---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 21e02077e7c2644c622a3f290a82fa26d7d6fc64
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791962"
---
# <span data-ttu-id="9394a-101">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="9394a-101">Remove-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="9394a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9394a-102">SYNOPSIS</span></span>
<span data-ttu-id="9394a-103">從資源群組中移除虛擬網路連結。</span><span class="sxs-lookup"><span data-stu-id="9394a-103">Removes a virtual network link from a resource group.</span></span>

## <span data-ttu-id="9394a-104">句法</span><span class="sxs-lookup"><span data-stu-id="9394a-104">SYNTAX</span></span>

### <span data-ttu-id="9394a-105">預設)  (的欄位</span><span class="sxs-lookup"><span data-stu-id="9394a-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9394a-106">面向</span><span class="sxs-lookup"><span data-stu-id="9394a-106">Object</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9394a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9394a-107">ResourceId</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9394a-108">說明</span><span class="sxs-lookup"><span data-stu-id="9394a-108">DESCRIPTION</span></span>
<span data-ttu-id="9394a-109">**AzPrivateDnsVirtualNetworkLink** Cmdlet 會從指定的資源群組中永久刪除私人網域名稱系統 (DNS) 連結。</span><span class="sxs-lookup"><span data-stu-id="9394a-109">The **Remove-AzPrivateDnsVirtualNetworkLink** cmdlet permanently deletes a private Domain Name System (DNS) link from a specified resource group.</span></span>
<span data-ttu-id="9394a-110">您可以使用 *Link* 參數或使用管線運算子來傳遞 **PSPrivateDnsVirtualNetworkLink** 物件，或者也可以指定 *名稱* *ZoneName* 和 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="9394a-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="9394a-111">您可以使用 Confirm 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9394a-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="9394a-112">使用 **PSPrivateDnsVirtualNetworkLink** 物件來指定連結時 (透過管線或 *link* ) 參數傳送時，如果在已檢索到本機 **PSPrivateDnsVirtualNetworkLink** 物件之後，該連結就不會被刪除。</span><span class="sxs-lookup"><span data-stu-id="9394a-112">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure Private DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="9394a-113">這可為併發區域變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="9394a-113">This provides protection for concurrent zone changes.</span></span> <span data-ttu-id="9394a-114">這個值可以使用 *Overwrite* 參數加以取消，不論併發變更為何，都會刪除該區域。</span><span class="sxs-lookup"><span data-stu-id="9394a-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="9394a-115">示例</span><span class="sxs-lookup"><span data-stu-id="9394a-115">EXAMPLES</span></span>

### <span data-ttu-id="9394a-116">範例1：移除連結</span><span class="sxs-lookup"><span data-stu-id="9394a-116">Example 1: Remove a link</span></span>
```
PS C:\>Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"
```

<span data-ttu-id="9394a-117">這個命令會從名為 MyResourceGroup 的資源群組中移除名為 mylink 的連結至區域 myzone.com 的連結。</span><span class="sxs-lookup"><span data-stu-id="9394a-117">This command removes the link named mylink linked to zone myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="9394a-118">參數</span><span class="sxs-lookup"><span data-stu-id="9394a-118">PARAMETERS</span></span>

### <span data-ttu-id="9394a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9394a-119">-DefaultProfile</span></span>
<span data-ttu-id="9394a-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9394a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9394a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9394a-121">-InputObject</span></span>
<span data-ttu-id="9394a-122">要移除的虛擬網路連結化物件。</span><span class="sxs-lookup"><span data-stu-id="9394a-122">The virtual network link object to remove.</span></span>

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

### <span data-ttu-id="9394a-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="9394a-123">-Name</span></span>
<span data-ttu-id="9394a-124">指定要刪除之連結的名稱。</span><span class="sxs-lookup"><span data-stu-id="9394a-124">Specifies the name of the link to be deleted.</span></span>
<span data-ttu-id="9394a-125">您也必須指定 *ResourceGroupName* 和 *ZoneName* 參數。</span><span class="sxs-lookup"><span data-stu-id="9394a-125">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="9394a-126">或者，您也可以使用 *link* 參數指定連結。</span><span class="sxs-lookup"><span data-stu-id="9394a-126">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="9394a-127">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="9394a-127">-Overwrite</span></span>
<span data-ttu-id="9394a-128">使用 **PSPrivateDnsVirtualNetworkLink** 物件指定區域 (透過管線或 *Link* ) 參數傳送時，如果在已檢索到本機 **PSPrivateDnsVirtualNetworkLink** 物件之後，該區域就不會被刪除。</span><span class="sxs-lookup"><span data-stu-id="9394a-128">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="9394a-129">這可為併發區域變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="9394a-129">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="9394a-130">這個值可以使用 *Overwrite* 參數加以取消，不論併發變更為何，都會刪除該區域。</span><span class="sxs-lookup"><span data-stu-id="9394a-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="9394a-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9394a-131">-PassThru</span></span>
<span data-ttu-id="9394a-132">用來傳送作業的結果 (布林) ，將 [刪除虛擬網路] 連結，在管線的下方。</span><span class="sxs-lookup"><span data-stu-id="9394a-132">Used for passing the result (boolean) of the operation delete virtual network link further down the pipeline.</span></span>

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

### <span data-ttu-id="9394a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9394a-133">-ResourceGroupName</span></span>
<span data-ttu-id="9394a-134">指定包含要移除之連結之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9394a-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="9394a-135">您也必須指定 *ZoneName* 和 *Name* 參數。</span><span class="sxs-lookup"><span data-stu-id="9394a-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="9394a-136">或者，您也可以使用 **PSPrivateDnsVirtualNetworkLink** 物件來指定 DNS 區域，方法是透過管線或 *Link* 參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="9394a-136">Alternatively, you can specify the DNS zone using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="9394a-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9394a-137">-ResourceId</span></span>
<span data-ttu-id="9394a-138">指定連結的 ARM 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9394a-138">Specifies the ARM resource ID of the link.</span></span>

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

### <span data-ttu-id="9394a-139">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="9394a-139">-ZoneName</span></span>
<span data-ttu-id="9394a-140">指定連結所關聯的專用 DNS 區域的名稱。</span><span class="sxs-lookup"><span data-stu-id="9394a-140">Specifies the name of the private DNS zone that the link is associated with.</span></span>
<span data-ttu-id="9394a-141">您也必須指定 *ResourceGroupName* 和 *Name* 參數。</span><span class="sxs-lookup"><span data-stu-id="9394a-141">You must also specify the *ResourceGroupName* and *Name* parameter.</span></span>
<span data-ttu-id="9394a-142">或者，您也可以使用 *link* 參數指定連結。</span><span class="sxs-lookup"><span data-stu-id="9394a-142">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="9394a-143">-確認</span><span class="sxs-lookup"><span data-stu-id="9394a-143">-Confirm</span></span>
<span data-ttu-id="9394a-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9394a-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9394a-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9394a-145">-WhatIf</span></span>
<span data-ttu-id="9394a-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9394a-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9394a-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9394a-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9394a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9394a-148">CommonParameters</span></span>
<span data-ttu-id="9394a-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9394a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9394a-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9394a-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9394a-151">輸入</span><span class="sxs-lookup"><span data-stu-id="9394a-151">INPUTS</span></span>

### <span data-ttu-id="9394a-152">PSPrivateDnsVirtualNetworkLink 中的 PrivateDns。</span><span class="sxs-lookup"><span data-stu-id="9394a-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="9394a-153">System.object</span><span class="sxs-lookup"><span data-stu-id="9394a-153">System.String</span></span>

## <span data-ttu-id="9394a-154">輸出</span><span class="sxs-lookup"><span data-stu-id="9394a-154">OUTPUTS</span></span>

### <span data-ttu-id="9394a-155">System.object</span><span class="sxs-lookup"><span data-stu-id="9394a-155">System.Boolean</span></span>

## <span data-ttu-id="9394a-156">筆記</span><span class="sxs-lookup"><span data-stu-id="9394a-156">NOTES</span></span>

## <span data-ttu-id="9394a-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="9394a-157">RELATED LINKS</span></span>

[<span data-ttu-id="9394a-158">AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="9394a-158">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="9394a-159">新-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="9394a-159">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="9394a-160">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="9394a-160">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
