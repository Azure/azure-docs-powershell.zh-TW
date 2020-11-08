---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 60da913ea7743be288e58eee9e4840c15e4818b4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797833"
---
# <span data-ttu-id="2030c-101">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="2030c-101">Get-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="2030c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2030c-102">SYNOPSIS</span></span>
<span data-ttu-id="2030c-103">取得與指定的專用 DNS 區域相關聯的虛擬網路連結。</span><span class="sxs-lookup"><span data-stu-id="2030c-103">Gets a virtual network link associated with the specified Private DNS zone.</span></span>

## <span data-ttu-id="2030c-104">句法</span><span class="sxs-lookup"><span data-stu-id="2030c-104">SYNTAX</span></span>

```
Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2030c-105">說明</span><span class="sxs-lookup"><span data-stu-id="2030c-105">DESCRIPTION</span></span>
<span data-ttu-id="2030c-106">**AzPrivateDnsVirtualNetworkLink** Cmdlet 會從指定的資源群組取得與特定專用 DNS 區域相關聯的虛擬網路連結。</span><span class="sxs-lookup"><span data-stu-id="2030c-106">The **Get-AzPrivateDnsVirtualNetworkLink** cmdlet gets virtual network links associated with a particular Private DNS zone from the specified resource group.</span></span>
<span data-ttu-id="2030c-107">如果您指定 *Name* 參數，則會傳回單一 **PSPrivateDnsVirtualNetworkLink** 物件。</span><span class="sxs-lookup"><span data-stu-id="2030c-107">If you specify the *Name* parameter, a single **PSPrivateDnsVirtualNetworkLink** object is returned.</span></span>
<span data-ttu-id="2030c-108">如果您沒有指定 *Name* 參數，則會傳回包含與指定資源群組中之區域相關聯之所有連結的陣列。</span><span class="sxs-lookup"><span data-stu-id="2030c-108">If you do not specify the *Name* parameter, an array containing all of the links associated with the zone in the specified resource group is returned.</span></span>
<span data-ttu-id="2030c-109">您可以使用 **PSPrivateDnsVirtualNetworkLink** 物件來更新連結。</span><span class="sxs-lookup"><span data-stu-id="2030c-109">You can use the **PSPrivateDnsVirtualNetworkLink** object to update the link.</span></span>

## <span data-ttu-id="2030c-110">示例</span><span class="sxs-lookup"><span data-stu-id="2030c-110">EXAMPLES</span></span>

### <span data-ttu-id="2030c-111">範例1：取得虛擬網路連結。</span><span class="sxs-lookup"><span data-stu-id="2030c-111">Example 1: Get a virtual network link.</span></span>
```
PS C:\> $Link = Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"

The link object returned looks like the following:

Name                    : mylink
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="2030c-112">這個範例會取得與指定資源群組中名為 myzone.com 的專用 DNS 區域相關聯的虛擬網路連結 mylink，然後將其儲存在 $Link 變數中。</span><span class="sxs-lookup"><span data-stu-id="2030c-112">This example gets the virtual network link mylink associated with the Private DNS zone named myzone.com from the specified resource group, and then stores it in the $Link variable.</span></span>

### <span data-ttu-id="2030c-113">範例2：取得與資源群組中的某個區域相關的所有連結。</span><span class="sxs-lookup"><span data-stu-id="2030c-113">Example 2: Get all of the links associated with a zone in a resource group.</span></span>
```
PS C:\> $Links = Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"

Name                    : mylink1
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink1
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded

Name                    : mylink2
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink2
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="2030c-114">這個範例會取得與指定資源群組中的專用 DNS 區域「myzone.com」相關聯的所有虛擬網路連結，然後將其儲存在 $Links 變數中。</span><span class="sxs-lookup"><span data-stu-id="2030c-114">This example gets all of the virtual network links associated with the Private DNS zone "myzone.com" in the specified resource group, and then stores it in the $Links variable.</span></span>

## <span data-ttu-id="2030c-115">參數</span><span class="sxs-lookup"><span data-stu-id="2030c-115">PARAMETERS</span></span>

### <span data-ttu-id="2030c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2030c-116">-DefaultProfile</span></span>
<span data-ttu-id="2030c-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2030c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2030c-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="2030c-118">-Name</span></span>
<span data-ttu-id="2030c-119">指定要取得的虛擬網路連結的名稱。</span><span class="sxs-lookup"><span data-stu-id="2030c-119">Specifies the name of the virtual network link to get.</span></span>
<span data-ttu-id="2030c-120">如果您沒有指定 *Name* 參數的值，這個 Cmdlet 會取得與指定資源群組中指定的專用 DNS 區域相關聯的所有連結。</span><span class="sxs-lookup"><span data-stu-id="2030c-120">If you do not specify a value for the *Name* parameter, this cmdlet gets all links associated with the specified Private DNS zone in the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2030c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2030c-121">-ResourceGroupName</span></span>
<span data-ttu-id="2030c-122">指定包含要取得之虛擬網路連結之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2030c-122">Specifies the name of the resource group that contains the virtual network link to get.</span></span>

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

### <span data-ttu-id="2030c-123">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="2030c-123">-ZoneName</span></span>
<span data-ttu-id="2030c-124">指定虛擬網路連結連結的專用 DNS 區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="2030c-124">Specifies the name of the Private DNS zone that the virtual network link is linked to.</span></span>


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

### <span data-ttu-id="2030c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2030c-125">CommonParameters</span></span>
<span data-ttu-id="2030c-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2030c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2030c-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2030c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2030c-128">輸入</span><span class="sxs-lookup"><span data-stu-id="2030c-128">INPUTS</span></span>

### <span data-ttu-id="2030c-129">所有</span><span class="sxs-lookup"><span data-stu-id="2030c-129">None</span></span>

## <span data-ttu-id="2030c-130">輸出</span><span class="sxs-lookup"><span data-stu-id="2030c-130">OUTPUTS</span></span>

### <span data-ttu-id="2030c-131">PSPrivateDnsVirtualNetworkLink 中的 PrivateDns。</span><span class="sxs-lookup"><span data-stu-id="2030c-131">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="2030c-132">筆記</span><span class="sxs-lookup"><span data-stu-id="2030c-132">NOTES</span></span>

## <span data-ttu-id="2030c-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="2030c-133">RELATED LINKS</span></span>

[<span data-ttu-id="2030c-134">新-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="2030c-134">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="2030c-135">移除-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="2030c-135">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="2030c-136">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="2030c-136">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)