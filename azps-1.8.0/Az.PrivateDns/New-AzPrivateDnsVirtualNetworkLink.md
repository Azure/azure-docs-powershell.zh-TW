---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/New-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 7d2a9a399e6582e2ff3815447570548ac62f6676
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621227"
---
# <span data-ttu-id="16dc6-101">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="16dc6-101">New-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="16dc6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="16dc6-102">SYNOPSIS</span></span>
<span data-ttu-id="16dc6-103">建立新的私人 DNS 虛擬網路連結。</span><span class="sxs-lookup"><span data-stu-id="16dc6-103">Creates a new private DNS virtual network link.</span></span>

## <span data-ttu-id="16dc6-104">句法</span><span class="sxs-lookup"><span data-stu-id="16dc6-104">SYNTAX</span></span>

### <span data-ttu-id="16dc6-105">VirtualNetworkId (預設) </span><span class="sxs-lookup"><span data-stu-id="16dc6-105">VirtualNetworkId (Default)</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetworkId <String> [-EnableRegistration] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16dc6-106">VirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="16dc6-106">VirtualNetworkObject</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetwork <VirtualNetwork> [-EnableRegistration] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16dc6-107">說明</span><span class="sxs-lookup"><span data-stu-id="16dc6-107">DESCRIPTION</span></span>
<span data-ttu-id="16dc6-108">**新的-AzPrivateDnsVirtualNetworkLink** Cmdlet 會在指定的資源群組和私人區域中， (DNS) 虛擬網路連結中，建立新的私人網域名稱系統。</span><span class="sxs-lookup"><span data-stu-id="16dc6-108">The **New-AzPrivateDnsVirtualNetworkLink** cmdlet creates a new private Domain Name System (DNS) virtual network link in the specified resource group and private zone.</span></span> <span data-ttu-id="16dc6-109">您必須為 *name* 參數指定唯一的連結名稱，否則 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="16dc6-109">You must specify a unique link name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="16dc6-110">您可以使用 *Confirm* 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="16dc6-110">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="16dc6-111">示例</span><span class="sxs-lookup"><span data-stu-id="16dc6-111">EXAMPLES</span></span>

### <span data-ttu-id="16dc6-112">範例1：建立私人 DNS 虛擬網路連結</span><span class="sxs-lookup"><span data-stu-id="16dc6-112">Example 1: Create a Private DNS virtual network link</span></span>
```
PS C:\>$Link = New-AzPrivateDnsVirtualNetworkLink -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Name "mylink" -VirtualNetworkId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork" -EnableRegistration

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

<span data-ttu-id="16dc6-113">這個命令會建立一個新的虛擬網路連結，其與名為 myzone.com 和虛擬網路 "myvirtualnetwork" 的私人 DNS 區域相關聯， (已在 [資源]) 群組中建立，並將其儲存在 $Link 變數中。</span><span class="sxs-lookup"><span data-stu-id="16dc6-113">This command creates a new virtual network link associated with the private DNS zone named myzone.com and virtual network "myvirtualnetwork" (which has already been created in the resource group) in the specified resource group, and then stores it in the $Link variable.</span></span>

## <span data-ttu-id="16dc6-114">參數</span><span class="sxs-lookup"><span data-stu-id="16dc6-114">PARAMETERS</span></span>

### <span data-ttu-id="16dc6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16dc6-115">-DefaultProfile</span></span>
<span data-ttu-id="16dc6-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="16dc6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16dc6-117">-EnableRegistration</span><span class="sxs-lookup"><span data-stu-id="16dc6-117">-EnableRegistration</span></span>
<span data-ttu-id="16dc6-118">代表是否已啟用註冊連結的 Switch 參數。</span><span class="sxs-lookup"><span data-stu-id="16dc6-118">Switch parameter that represents if the link is registration enabled or not.</span></span>

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

### <span data-ttu-id="16dc6-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="16dc6-119">-Name</span></span>
<span data-ttu-id="16dc6-120">指定要建立的虛擬網路連結的名稱。</span><span class="sxs-lookup"><span data-stu-id="16dc6-120">Specifies the name of the virtual network link to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16dc6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16dc6-121">-ResourceGroupName</span></span>
<span data-ttu-id="16dc6-122">指定要在其中建立連結的資源群組。</span><span class="sxs-lookup"><span data-stu-id="16dc6-122">Specifies the resource group in which to create the link.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16dc6-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="16dc6-123">-Tag</span></span>
<span data-ttu-id="16dc6-124">代表資源標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="16dc6-124">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="16dc6-125">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="16dc6-125">-VirtualNetwork</span></span>
<span data-ttu-id="16dc6-126">與連結相關聯的虛擬網路物件。</span><span class="sxs-lookup"><span data-stu-id="16dc6-126">The virtual network object associated with the link.</span></span>

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IVirtualNetwork
Parameter Sets: VirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16dc6-127">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="16dc6-127">-VirtualNetworkId</span></span>
<span data-ttu-id="16dc6-128">與連結相關聯之虛擬網路的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="16dc6-128">The resource id of the virtual network associated with the link.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16dc6-129">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="16dc6-129">-ZoneName</span></span>
<span data-ttu-id="16dc6-130">指定將連結至 [虛擬網路] 連結的區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="16dc6-130">Specifies the name of the zone which will be linked to the virtual network link.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16dc6-131">-確認</span><span class="sxs-lookup"><span data-stu-id="16dc6-131">-Confirm</span></span>
<span data-ttu-id="16dc6-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="16dc6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16dc6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16dc6-133">-WhatIf</span></span>
<span data-ttu-id="16dc6-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="16dc6-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16dc6-135">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="16dc6-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16dc6-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="16dc6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16dc6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16dc6-137">CommonParameters</span></span>
<span data-ttu-id="16dc6-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="16dc6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16dc6-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="16dc6-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16dc6-140">輸入</span><span class="sxs-lookup"><span data-stu-id="16dc6-140">INPUTS</span></span>

### <span data-ttu-id="16dc6-141">所有</span><span class="sxs-lookup"><span data-stu-id="16dc6-141">None</span></span>

## <span data-ttu-id="16dc6-142">輸出</span><span class="sxs-lookup"><span data-stu-id="16dc6-142">OUTPUTS</span></span>

### <span data-ttu-id="16dc6-143">PSPrivateDnsVirtualNetworkLink 中的 PrivateDns。</span><span class="sxs-lookup"><span data-stu-id="16dc6-143">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="16dc6-144">筆記</span><span class="sxs-lookup"><span data-stu-id="16dc6-144">NOTES</span></span>

## <span data-ttu-id="16dc6-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="16dc6-145">RELATED LINKS</span></span>

[<span data-ttu-id="16dc6-146">AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="16dc6-146">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="16dc6-147">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="16dc6-147">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="16dc6-148">移除-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="16dc6-148">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)
