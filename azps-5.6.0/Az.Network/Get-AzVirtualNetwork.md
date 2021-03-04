---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
ms.openlocfilehash: 80a1c21b118bf8bcc5a613fef2cdfbe382b117a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906906"
---
# <span data-ttu-id="a774e-101">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a774e-101">Get-AzVirtualNetwork</span></span>

## <span data-ttu-id="a774e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a774e-102">SYNOPSIS</span></span>
<span data-ttu-id="a774e-103">在資源群組中建立虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="a774e-103">Gets a virtual network in a resource group.</span></span>

## <span data-ttu-id="a774e-104">語法</span><span class="sxs-lookup"><span data-stu-id="a774e-104">SYNTAX</span></span>

### <span data-ttu-id="a774e-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="a774e-105">NoExpand</span></span>
```
Get-AzVirtualNetwork [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a774e-106">擴大</span><span class="sxs-lookup"><span data-stu-id="a774e-106">Expand</span></span>
```
Get-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a774e-107">描述</span><span class="sxs-lookup"><span data-stu-id="a774e-107">DESCRIPTION</span></span>
<span data-ttu-id="a774e-108">**Get-AzVirtualNetwork** Cmdlet 會取得資源群組中的一或多個虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="a774e-108">The **Get-AzVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="a774e-109">例子</span><span class="sxs-lookup"><span data-stu-id="a774e-109">EXAMPLES</span></span>

### <span data-ttu-id="a774e-110">1：取回虛擬網路</span><span class="sxs-lookup"><span data-stu-id="a774e-110">1: Retrieve a virtual network</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup

Name                   : MyVirtualNetwork1
ResourceGroupName      : TestResourceGroup
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup
                         /providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "xx.x.x.x/x"
                           ]
                         }
DhcpOptions            : {}
Subnets                : []
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
```

<span data-ttu-id="a774e-111">此命令會獲得資源群組 TestResourceGroup 中名為 MyVirtualNetwork 的虛擬網路</span><span class="sxs-lookup"><span data-stu-id="a774e-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="a774e-112">2：使用篩選列出虛擬網路</span><span class="sxs-lookup"><span data-stu-id="a774e-112">2: List virtual networks using filter</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork*

Name                   : MyVirtualNetwork1
ResourceGroupName      : TestResourceGroup
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup
                         /providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "xx.x.x.x/x"
                           ]
                         }
DhcpOptions            : {}
Subnets                : []
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
```

<span data-ttu-id="a774e-113">此命令會獲得以「MyVirtualNetwork」為起點的所有虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="a774e-113">This command gets all virtual networks that start with "MyVirtualNetwork".</span></span>

## <span data-ttu-id="a774e-114">參數</span><span class="sxs-lookup"><span data-stu-id="a774e-114">PARAMETERS</span></span>

### <span data-ttu-id="a774e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a774e-115">-DefaultProfile</span></span>
<span data-ttu-id="a774e-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a774e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a774e-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="a774e-117">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a774e-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="a774e-118">-Name</span></span>
<span data-ttu-id="a774e-119">指定此 Cmdlet 所獲取的虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="a774e-119">Specifies the name of the virtual network that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="a774e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a774e-120">-ResourceGroupName</span></span>
<span data-ttu-id="a774e-121">指定虛擬網路所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a774e-121">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="a774e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a774e-122">CommonParameters</span></span>
<span data-ttu-id="a774e-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a774e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a774e-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a774e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a774e-125">輸入</span><span class="sxs-lookup"><span data-stu-id="a774e-125">INPUTS</span></span>

### <span data-ttu-id="a774e-126">System.String</span><span class="sxs-lookup"><span data-stu-id="a774e-126">System.String</span></span>

## <span data-ttu-id="a774e-127">輸出</span><span class="sxs-lookup"><span data-stu-id="a774e-127">OUTPUTS</span></span>

### <span data-ttu-id="a774e-128">Microsoft.Azure.Commands.Network.models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a774e-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="a774e-129">筆記</span><span class="sxs-lookup"><span data-stu-id="a774e-129">NOTES</span></span>

## <span data-ttu-id="a774e-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="a774e-130">RELATED LINKS</span></span>

[<span data-ttu-id="a774e-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a774e-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="a774e-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a774e-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="a774e-133">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a774e-133">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


