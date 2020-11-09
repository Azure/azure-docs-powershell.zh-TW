---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
ms.openlocfilehash: d381af8de23b5eb781882f10670e6ba69afbc571
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94288096"
---
# <span data-ttu-id="100b6-101">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="100b6-101">Remove-AzPrivateDnsZone</span></span>

## <span data-ttu-id="100b6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="100b6-102">SYNOPSIS</span></span>
<span data-ttu-id="100b6-103">從資源群組中移除私人 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="100b6-103">Removes a private DNS zone from a resource group.</span></span>

## <span data-ttu-id="100b6-104">句法</span><span class="sxs-lookup"><span data-stu-id="100b6-104">SYNTAX</span></span>

### <span data-ttu-id="100b6-105">預設)  (的欄位</span><span class="sxs-lookup"><span data-stu-id="100b6-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="100b6-106">面向</span><span class="sxs-lookup"><span data-stu-id="100b6-106">Object</span></span>
```
Remove-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="100b6-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="100b6-107">ResourceId</span></span>
```
Remove-AzPrivateDnsZone -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="100b6-108">說明</span><span class="sxs-lookup"><span data-stu-id="100b6-108">DESCRIPTION</span></span>
<span data-ttu-id="100b6-109">AzPrivateDnsZone Cmdlet 會從指定 **的** 資源群組中永久刪除私人網功能變數名稱稱系統 (DNS) 區域。</span><span class="sxs-lookup"><span data-stu-id="100b6-109">The **Remove-AzPrivateDnsZone** cmdlet permanently deletes a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="100b6-110">該區域中包含的所有記錄集也都會刪除。</span><span class="sxs-lookup"><span data-stu-id="100b6-110">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="100b6-111">您可以使用 *PrivateZone* 參數或使用管線運算子來傳遞 **PrivateDnsZone** 物件，或者也可以指定 *Name* 和 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="100b6-111">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="100b6-112">您可以使用 Confirm 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="100b6-112">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="100b6-113">使用 **PrivateDnsZone** 物件來指定區域時 (透過管線或 *zone* 參數) ，如果您自本機 **PrivateDnsZone** 物件檢索之後，在 Azure DNS 中已變更，該區域就不會被刪除 (在該區域內，記錄集的操作不) 。</span><span class="sxs-lookup"><span data-stu-id="100b6-113">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="100b6-114">這可為併發區域變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="100b6-114">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="100b6-115">這個值可以使用 *Overwrite* 參數加以取消，不論併發變更為何，都會刪除該區域。</span><span class="sxs-lookup"><span data-stu-id="100b6-115">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="100b6-116">示例</span><span class="sxs-lookup"><span data-stu-id="100b6-116">EXAMPLES</span></span>

### <span data-ttu-id="100b6-117">範例1：移除私人區域</span><span class="sxs-lookup"><span data-stu-id="100b6-117">Example 1: Remove a private zone</span></span>
```
PS C:\>Remove-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="100b6-118">這個命令會從名為 MyResourceGroup 的資源群組中移除名為 myzone.com 的區域。</span><span class="sxs-lookup"><span data-stu-id="100b6-118">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="100b6-119">參數</span><span class="sxs-lookup"><span data-stu-id="100b6-119">PARAMETERS</span></span>

### <span data-ttu-id="100b6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="100b6-120">-DefaultProfile</span></span>
<span data-ttu-id="100b6-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="100b6-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="100b6-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="100b6-122">-Name</span></span>
<span data-ttu-id="100b6-123">指定此 Cmdlet 移除之專用 DNS 區域的名稱。</span><span class="sxs-lookup"><span data-stu-id="100b6-123">Specifies the name of the private DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="100b6-124">您也必須指定 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="100b6-124">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="100b6-125">或者，您也可以使用 *zone* 參數指定 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="100b6-125">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="100b6-126">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="100b6-126">-Overwrite</span></span>
<span data-ttu-id="100b6-127">使用 **PrivateDnsZone** 物件來指定區域時 (透過管線或 *zone* 參數) ，如果您自本機 **PrivateDnsZone** 物件檢索之後，在 Azure DNS 中已變更，該區域就不會被刪除 (在該區域內，記錄集的操作不) 。</span><span class="sxs-lookup"><span data-stu-id="100b6-127">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="100b6-128">這可為併發區域變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="100b6-128">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="100b6-129">這個值可以使用 *Overwrite* 參數加以取消，不論併發變更為何，都會刪除該區域。</span><span class="sxs-lookup"><span data-stu-id="100b6-129">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="100b6-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="100b6-130">-PassThru</span></span>
<span data-ttu-id="100b6-131">用來傳送操作的結果 (布林) ，以從管線中移除私有區域。</span><span class="sxs-lookup"><span data-stu-id="100b6-131">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="100b6-132">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="100b6-132">-PrivateZone</span></span>
<span data-ttu-id="100b6-133">要刪除的私人區域物件。</span><span class="sxs-lookup"><span data-stu-id="100b6-133">The private zone object to delete.</span></span>

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

### <span data-ttu-id="100b6-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="100b6-134">-ResourceGroupName</span></span>
<span data-ttu-id="100b6-135">指定包含要移除之區域的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="100b6-135">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="100b6-136">您也必須指定 *ZoneName* 參數。</span><span class="sxs-lookup"><span data-stu-id="100b6-136">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="100b6-137">或者，您也可以使用 **PrivateDnsZone** 物件來指定 DNS 區域，方法是透過管線或 *zone* 參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="100b6-137">Alternatively, you can specify the DNS zone using a **PrivateDnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="100b6-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="100b6-138">-ResourceId</span></span>
<span data-ttu-id="100b6-139">私人 DNS 區域 ResourceID。</span><span class="sxs-lookup"><span data-stu-id="100b6-139">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="100b6-140">-確認</span><span class="sxs-lookup"><span data-stu-id="100b6-140">-Confirm</span></span>
<span data-ttu-id="100b6-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="100b6-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="100b6-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="100b6-142">-WhatIf</span></span>
<span data-ttu-id="100b6-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="100b6-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="100b6-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="100b6-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="100b6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="100b6-145">CommonParameters</span></span>
<span data-ttu-id="100b6-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="100b6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="100b6-147">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="100b6-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="100b6-148">輸入</span><span class="sxs-lookup"><span data-stu-id="100b6-148">INPUTS</span></span>

### <span data-ttu-id="100b6-149">PSPrivateDnsZone 中的 PrivateDns。</span><span class="sxs-lookup"><span data-stu-id="100b6-149">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="100b6-150">System.object</span><span class="sxs-lookup"><span data-stu-id="100b6-150">System.String</span></span>

## <span data-ttu-id="100b6-151">輸出</span><span class="sxs-lookup"><span data-stu-id="100b6-151">OUTPUTS</span></span>

### <span data-ttu-id="100b6-152">System.object</span><span class="sxs-lookup"><span data-stu-id="100b6-152">System.Boolean</span></span>

## <span data-ttu-id="100b6-153">筆記</span><span class="sxs-lookup"><span data-stu-id="100b6-153">NOTES</span></span>

## <span data-ttu-id="100b6-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="100b6-154">RELATED LINKS</span></span>

[<span data-ttu-id="100b6-155">AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="100b6-155">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="100b6-156">新-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="100b6-156">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="100b6-157">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="100b6-157">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
