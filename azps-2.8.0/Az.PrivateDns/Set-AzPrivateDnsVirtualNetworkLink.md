---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: d2d00df48cbaf4bff1d6e9dac648004d73e65f2c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791951"
---
# <span data-ttu-id="6883c-101">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="6883c-101">Set-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="6883c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6883c-102">SYNOPSIS</span></span>
<span data-ttu-id="6883c-103">更新/設定與私人區域及資源群組相關聯的虛擬網路連結。</span><span class="sxs-lookup"><span data-stu-id="6883c-103">Updates/Sets a virtual network link associated with a private zone and a resource group.</span></span>

## <span data-ttu-id="6883c-104">句法</span><span class="sxs-lookup"><span data-stu-id="6883c-104">SYNTAX</span></span>

### <span data-ttu-id="6883c-105">預設)  (的欄位</span><span class="sxs-lookup"><span data-stu-id="6883c-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6883c-106">面向</span><span class="sxs-lookup"><span data-stu-id="6883c-106">Object</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6883c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6883c-107">ResourceId</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6883c-108">說明</span><span class="sxs-lookup"><span data-stu-id="6883c-108">DESCRIPTION</span></span>
<span data-ttu-id="6883c-109">**AzPrivateDnsVirtualNetworkLink** Cmdlet 會更新與特定資源群組中的區域相關聯的連結。</span><span class="sxs-lookup"><span data-stu-id="6883c-109">The **Set-AzPrivateDnsVirtualNetworkLink** cmdlet updates a link associated with a zone from a specified resource group.</span></span>
<span data-ttu-id="6883c-110">您可以使用 *Link* 參數或使用管線運算子來傳遞 **PSPrivateDnsVirtualNetworkLink** 物件，或者也可以指定 *名稱* *ZoneName* 和 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="6883c-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="6883c-111">您可以使用 Confirm 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6883c-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="6883c-112">使用 **PSPrivateDnsVirtualNetworkLink** 物件指定區域 (透過管線或 *Link* ) 參數傳遞時，如果在已檢索到本機 **PSPrivateDnsVirtualNetworkLink** 物件之後，就不會更新連結。</span><span class="sxs-lookup"><span data-stu-id="6883c-112">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not updated if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="6883c-113">這可為併發連結變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="6883c-113">This provides protection for concurrent link changes.</span></span> <span data-ttu-id="6883c-114">這可以使用 *Overwrite* 參數加以取消，不論併發變更為何都會更新連結。</span><span class="sxs-lookup"><span data-stu-id="6883c-114">This can be suppressed using the *Overwrite* parameter, which updates the link regardless of concurrent changes.</span></span>

## <span data-ttu-id="6883c-115">示例</span><span class="sxs-lookup"><span data-stu-id="6883c-115">EXAMPLES</span></span>

### <span data-ttu-id="6883c-116">範例1：設定連結</span><span class="sxs-lookup"><span data-stu-id="6883c-116">Example 1: Set a link</span></span>
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

<span data-ttu-id="6883c-117">這個命令會將名為 mylink 的連結的 IsRegistrationEnabled 設定為 True，並連結至名為 MyResourceGroup 之資源群組的區域（名為 myzone.com）。</span><span class="sxs-lookup"><span data-stu-id="6883c-117">This command sets IsRegistrationEnabled to True for the link named mylink, linked to zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="6883c-118">參數</span><span class="sxs-lookup"><span data-stu-id="6883c-118">PARAMETERS</span></span>

### <span data-ttu-id="6883c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6883c-119">-DefaultProfile</span></span>
<span data-ttu-id="6883c-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6883c-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6883c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6883c-121">-InputObject</span></span>
<span data-ttu-id="6883c-122">要設定的虛擬網路連結化物件。</span><span class="sxs-lookup"><span data-stu-id="6883c-122">The virtual network link object to set.</span></span>

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

### <span data-ttu-id="6883c-123">-IsRegistrationEnabled</span><span class="sxs-lookup"><span data-stu-id="6883c-123">-IsRegistrationEnabled</span></span>
<span data-ttu-id="6883c-124">表示是否已在虛擬網路連結上啟用註冊的布林值。</span><span class="sxs-lookup"><span data-stu-id="6883c-124">Boolean that represents if registration is enabled on the virtual network link.</span></span>

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

### <span data-ttu-id="6883c-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="6883c-125">-Name</span></span>
<span data-ttu-id="6883c-126">指定此 Cmdlet 移除之連結的名稱。</span><span class="sxs-lookup"><span data-stu-id="6883c-126">Specifies the name of the link that this cmdlet removes.</span></span>
<span data-ttu-id="6883c-127">您也必須指定 *ResourceGroupName* 和 *ZoneName* 參數。</span><span class="sxs-lookup"><span data-stu-id="6883c-127">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="6883c-128">或者，您也可以使用 *link* 參數指定私人 DNS 連結。</span><span class="sxs-lookup"><span data-stu-id="6883c-128">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

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

### <span data-ttu-id="6883c-129">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="6883c-129">-Overwrite</span></span>
<span data-ttu-id="6883c-130">使用 **PSPrivateDnsVirtualNetworkLink** 物件來指定連結時 (透過管線或 *link* ) 參數傳送時，如果在已檢索到本機 **PSPrivateDnsVirtualNetworkLink** 物件之後，該連結就不會被刪除。</span><span class="sxs-lookup"><span data-stu-id="6883c-130">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="6883c-131">這可為併發連結變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="6883c-131">This provides protection for concurrent link changes.</span></span>
<span data-ttu-id="6883c-132">這可以使用 *Overwrite* 參數加以取消，不論併發變更為何都會刪除連結。</span><span class="sxs-lookup"><span data-stu-id="6883c-132">This can be suppressed using the *Overwrite* parameter, which deletes the link regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="6883c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6883c-133">-ResourceGroupName</span></span>
<span data-ttu-id="6883c-134">指定包含要移除之連結之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6883c-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="6883c-135">您也必須指定 *ZoneName* 和 *Name* 參數。</span><span class="sxs-lookup"><span data-stu-id="6883c-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="6883c-136">或者，您也可以使用 **PSPrivateDnsVirtualNetworkLink** 物件來指定虛擬網路連結，方法是透過管線或 *link* 參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="6883c-136">Alternatively, you can specify the virtual network link using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="6883c-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6883c-137">-ResourceId</span></span>
<span data-ttu-id="6883c-138">私人 DNS 區域 ResourceID。</span><span class="sxs-lookup"><span data-stu-id="6883c-138">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="6883c-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="6883c-139">-Tag</span></span>
<span data-ttu-id="6883c-140">代表資源標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="6883c-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="6883c-141">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="6883c-141">-ZoneName</span></span>
<span data-ttu-id="6883c-142">指定此 Cmdlet 移除之 DNS 區域的名稱。</span><span class="sxs-lookup"><span data-stu-id="6883c-142">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="6883c-143">您也必須指定 *Name* 與 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="6883c-143">You must also specify the *Name* and *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="6883c-144">或者，您也可以使用 *link* 參數指定私人 DNS 連結。</span><span class="sxs-lookup"><span data-stu-id="6883c-144">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

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

### <span data-ttu-id="6883c-145">-確認</span><span class="sxs-lookup"><span data-stu-id="6883c-145">-Confirm</span></span>
<span data-ttu-id="6883c-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6883c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6883c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6883c-147">-WhatIf</span></span>
<span data-ttu-id="6883c-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6883c-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6883c-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6883c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6883c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6883c-150">CommonParameters</span></span>
<span data-ttu-id="6883c-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6883c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6883c-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6883c-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6883c-153">輸入</span><span class="sxs-lookup"><span data-stu-id="6883c-153">INPUTS</span></span>

### <span data-ttu-id="6883c-154">PSPrivateDnsVirtualNetworkLink 中的 PrivateDns。</span><span class="sxs-lookup"><span data-stu-id="6883c-154">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="6883c-155">System.object</span><span class="sxs-lookup"><span data-stu-id="6883c-155">System.String</span></span>

## <span data-ttu-id="6883c-156">輸出</span><span class="sxs-lookup"><span data-stu-id="6883c-156">OUTPUTS</span></span>

### <span data-ttu-id="6883c-157">PSPrivateDnsVirtualNetworkLink 中的 PrivateDns。</span><span class="sxs-lookup"><span data-stu-id="6883c-157">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="6883c-158">筆記</span><span class="sxs-lookup"><span data-stu-id="6883c-158">NOTES</span></span>

## <span data-ttu-id="6883c-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="6883c-159">RELATED LINKS</span></span>

[<span data-ttu-id="6883c-160">AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="6883c-160">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="6883c-161">新-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="6883c-161">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="6883c-162">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="6883c-162">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
