---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/powershell/module/az.privatedns/Set-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 1e1fa3709e597d220ba8269856f562a8ad8c3bd1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910402"
---
# <span data-ttu-id="4328f-101">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="4328f-101">Set-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="4328f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4328f-102">SYNOPSIS</span></span>
<span data-ttu-id="4328f-103">更新/設定與私人區域和資源群組相關聯的虛擬網路連結。</span><span class="sxs-lookup"><span data-stu-id="4328f-103">Updates/Sets a virtual network link associated with a private zone and a resource group.</span></span>

## <span data-ttu-id="4328f-104">語法</span><span class="sxs-lookup"><span data-stu-id="4328f-104">SYNTAX</span></span>

### <span data-ttu-id="4328f-105">欄位 (預設) </span><span class="sxs-lookup"><span data-stu-id="4328f-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4328f-106">物件</span><span class="sxs-lookup"><span data-stu-id="4328f-106">Object</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4328f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4328f-107">ResourceId</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4328f-108">描述</span><span class="sxs-lookup"><span data-stu-id="4328f-108">DESCRIPTION</span></span>
<span data-ttu-id="4328f-109">**Set-AzPrivateDnsVirtualNetworkLink** Cmdlet 會更新來自指定資源群組之區域的連結。</span><span class="sxs-lookup"><span data-stu-id="4328f-109">The **Set-AzPrivateDnsVirtualNetworkLink** cmdlet updates a link associated with a zone from a specified resource group.</span></span>
<span data-ttu-id="4328f-110">您可以使用 *Link* 參數或管道運算子傳遞 **PSPrivateDnsVirtualNetworkLink** 物件，或者您也可以指定 *Name* *ZoneName* 和 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="4328f-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="4328f-111">您可以使用確認參數$ConfirmPreference Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4328f-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="4328f-112">使用 **PSPrivateDnsVirtualNetworkLink** 物件 (透過管線或 *Link* 參數) 指定區域時，如果連結在 Azure DNS 中已經變更，則自已取回本地 **PSPrivateDnsVirtualNetworkLink** 物件之後，連結不會更新。</span><span class="sxs-lookup"><span data-stu-id="4328f-112">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not updated if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="4328f-113">這可保護同時進行的連結變更。</span><span class="sxs-lookup"><span data-stu-id="4328f-113">This provides protection for concurrent link changes.</span></span> <span data-ttu-id="4328f-114">您可以使用覆寫參數隱藏此設定，無論同時變更，都會更新連結。</span><span class="sxs-lookup"><span data-stu-id="4328f-114">This can be suppressed using the *Overwrite* parameter, which updates the link regardless of concurrent changes.</span></span>

## <span data-ttu-id="4328f-115">例子</span><span class="sxs-lookup"><span data-stu-id="4328f-115">EXAMPLES</span></span>

### <span data-ttu-id="4328f-116">範例 1：設定連結</span><span class="sxs-lookup"><span data-stu-id="4328f-116">Example 1: Set a link</span></span>
```
PS C:\>Set-AzPrivateDnsVirtualNetworkLink -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Name "mylink" -Tag @{} -IsRegistrationEnabled $true

Name                    : mylink
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="4328f-117">此命令會針對名稱為 mylink 的連結將 IsRegistrationEnabled 設定為 True，連結至名稱為 MyResourceGroup myzone.com名為 MyResourceGroup 的區域。</span><span class="sxs-lookup"><span data-stu-id="4328f-117">This command sets IsRegistrationEnabled to True for the link named mylink, linked to zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="4328f-118">參數</span><span class="sxs-lookup"><span data-stu-id="4328f-118">PARAMETERS</span></span>

### <span data-ttu-id="4328f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4328f-119">-DefaultProfile</span></span>
<span data-ttu-id="4328f-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="4328f-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4328f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4328f-121">-InputObject</span></span>
<span data-ttu-id="4328f-122">要設定之虛擬網路連結化物件。</span><span class="sxs-lookup"><span data-stu-id="4328f-122">The virtual network link object to set.</span></span>

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

### <span data-ttu-id="4328f-123">-IsRegistrationEnabled</span><span class="sxs-lookup"><span data-stu-id="4328f-123">-IsRegistrationEnabled</span></span>
<span data-ttu-id="4328f-124">代表在虛擬網路連結上啟用註冊的布林值。</span><span class="sxs-lookup"><span data-stu-id="4328f-124">Boolean that represents if registration is enabled on the virtual network link.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4328f-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="4328f-125">-Name</span></span>
<span data-ttu-id="4328f-126">指定此 Cmdlet 移除的連結名稱。</span><span class="sxs-lookup"><span data-stu-id="4328f-126">Specifies the name of the link that this cmdlet removes.</span></span>
<span data-ttu-id="4328f-127">您也必須指定 *ResourceGroupName 和* *ZoneName* 參數。</span><span class="sxs-lookup"><span data-stu-id="4328f-127">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="4328f-128">或者，您可以使用連結參數指定私人 DNS *連結* 。</span><span class="sxs-lookup"><span data-stu-id="4328f-128">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

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

### <span data-ttu-id="4328f-129">-覆寫</span><span class="sxs-lookup"><span data-stu-id="4328f-129">-Overwrite</span></span>
<span data-ttu-id="4328f-130">使用 **PSPrivateDnsVirtualNetworkLink** 物件 (透過管線或 *Link* 參數) 指定連結時，如果連結在 Azure DNS 中已經變更，則自已取回本地 **PSPrivateDnsVirtualNetworkLink** 物件之後，不會刪除該連結。</span><span class="sxs-lookup"><span data-stu-id="4328f-130">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="4328f-131">這可保護同時進行的連結變更。</span><span class="sxs-lookup"><span data-stu-id="4328f-131">This provides protection for concurrent link changes.</span></span>
<span data-ttu-id="4328f-132">您可以使用覆寫參數隱藏此設定，無論同時變更，都會刪除連結。</span><span class="sxs-lookup"><span data-stu-id="4328f-132">This can be suppressed using the *Overwrite* parameter, which deletes the link regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="4328f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4328f-133">-ResourceGroupName</span></span>
<span data-ttu-id="4328f-134">指定包含要移除之連結的資源組名。</span><span class="sxs-lookup"><span data-stu-id="4328f-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="4328f-135">您也必須指定 *ZoneName 和* *Name* 參數。</span><span class="sxs-lookup"><span data-stu-id="4328f-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="4328f-136">或者，您可以使用 **PSPrivateDnsVirtualNetworkLink** 物件指定透過管線或 Link 參數傳遞的 *虛擬網路連結* 。</span><span class="sxs-lookup"><span data-stu-id="4328f-136">Alternatively, you can specify the virtual network link using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="4328f-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4328f-137">-ResourceId</span></span>
<span data-ttu-id="4328f-138">私人 DNS 區域資源ID。</span><span class="sxs-lookup"><span data-stu-id="4328f-138">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="4328f-139">-標記</span><span class="sxs-lookup"><span data-stu-id="4328f-139">-Tag</span></span>
<span data-ttu-id="4328f-140">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4328f-140">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4328f-141">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="4328f-141">-ZoneName</span></span>
<span data-ttu-id="4328f-142">指定此 Cmdlet 移除的 DNS 區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="4328f-142">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="4328f-143">您也必須指定 *Name* 和 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="4328f-143">You must also specify the *Name* and *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="4328f-144">或者，您可以使用連結參數指定私人 DNS *連結* 。</span><span class="sxs-lookup"><span data-stu-id="4328f-144">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

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

### <span data-ttu-id="4328f-145">-確認</span><span class="sxs-lookup"><span data-stu-id="4328f-145">-Confirm</span></span>
<span data-ttu-id="4328f-146">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4328f-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4328f-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4328f-147">-WhatIf</span></span>
<span data-ttu-id="4328f-148">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4328f-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4328f-149">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4328f-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4328f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4328f-150">CommonParameters</span></span>
<span data-ttu-id="4328f-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4328f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4328f-152">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4328f-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4328f-153">輸入</span><span class="sxs-lookup"><span data-stu-id="4328f-153">INPUTS</span></span>

### <span data-ttu-id="4328f-154">Microsoft.Azure.Commands.PrivateDns.models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="4328f-154">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="4328f-155">System.String</span><span class="sxs-lookup"><span data-stu-id="4328f-155">System.String</span></span>

## <span data-ttu-id="4328f-156">輸出</span><span class="sxs-lookup"><span data-stu-id="4328f-156">OUTPUTS</span></span>

### <span data-ttu-id="4328f-157">Microsoft.Azure.Commands.PrivateDns.models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="4328f-157">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="4328f-158">筆記</span><span class="sxs-lookup"><span data-stu-id="4328f-158">NOTES</span></span>

## <span data-ttu-id="4328f-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="4328f-159">RELATED LINKS</span></span>

[<span data-ttu-id="4328f-160">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="4328f-160">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="4328f-161">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="4328f-161">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="4328f-162">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="4328f-162">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
