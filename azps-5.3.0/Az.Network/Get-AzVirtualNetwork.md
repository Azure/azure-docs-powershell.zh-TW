---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
ms.openlocfilehash: ff2e1a820a2a1cc664969c1872aebe6b88fc415b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449322"
---
# <span data-ttu-id="36070-101">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="36070-101">Get-AzVirtualNetwork</span></span>

## <span data-ttu-id="36070-102">摘要</span><span class="sxs-lookup"><span data-stu-id="36070-102">SYNOPSIS</span></span>
<span data-ttu-id="36070-103">取得資源群組中的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="36070-103">Gets a virtual network in a resource group.</span></span>

## <span data-ttu-id="36070-104">句法</span><span class="sxs-lookup"><span data-stu-id="36070-104">SYNTAX</span></span>

### <span data-ttu-id="36070-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="36070-105">NoExpand</span></span>
```
Get-AzVirtualNetwork [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="36070-106">擴充</span><span class="sxs-lookup"><span data-stu-id="36070-106">Expand</span></span>
```
Get-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36070-107">說明</span><span class="sxs-lookup"><span data-stu-id="36070-107">DESCRIPTION</span></span>
<span data-ttu-id="36070-108">**AzVirtualNetwork** Cmdlet 會取得一或多個虛擬網路 n a 資源群組。</span><span class="sxs-lookup"><span data-stu-id="36070-108">The **Get-AzVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="36070-109">示例</span><span class="sxs-lookup"><span data-stu-id="36070-109">EXAMPLES</span></span>

### <span data-ttu-id="36070-110">1：檢索虛擬網路</span><span class="sxs-lookup"><span data-stu-id="36070-110">1: Retrieve a virtual network</span></span>
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

<span data-ttu-id="36070-111">這個命令會在 [資源] 群組 TestResourceGroup 中取得名為 MyVirtualNetwork 的虛擬網路</span><span class="sxs-lookup"><span data-stu-id="36070-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="36070-112">2：使用篩選器列出虛擬網路</span><span class="sxs-lookup"><span data-stu-id="36070-112">2: List virtual networks using filter</span></span>
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

<span data-ttu-id="36070-113">這個命令會取得以 "MyVirtualNetwork" 為開頭的所有虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="36070-113">This command gets all virtual networks that start with "MyVirtualNetwork".</span></span>

## <span data-ttu-id="36070-114">參數</span><span class="sxs-lookup"><span data-stu-id="36070-114">PARAMETERS</span></span>

### <span data-ttu-id="36070-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36070-115">-DefaultProfile</span></span>
<span data-ttu-id="36070-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="36070-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36070-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="36070-117">-ExpandResource</span></span>
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

### <span data-ttu-id="36070-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="36070-118">-Name</span></span>
<span data-ttu-id="36070-119">指定此 Cmdlet 所取得之虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="36070-119">Specifies the name of the virtual network that this cmdlet gets.</span></span>

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

### <span data-ttu-id="36070-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36070-120">-ResourceGroupName</span></span>
<span data-ttu-id="36070-121">指定虛擬網路所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="36070-121">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="36070-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36070-122">CommonParameters</span></span>
<span data-ttu-id="36070-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="36070-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36070-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="36070-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36070-125">輸入</span><span class="sxs-lookup"><span data-stu-id="36070-125">INPUTS</span></span>

### <span data-ttu-id="36070-126">System.object</span><span class="sxs-lookup"><span data-stu-id="36070-126">System.String</span></span>

## <span data-ttu-id="36070-127">輸出</span><span class="sxs-lookup"><span data-stu-id="36070-127">OUTPUTS</span></span>

### <span data-ttu-id="36070-128">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="36070-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="36070-129">筆記</span><span class="sxs-lookup"><span data-stu-id="36070-129">NOTES</span></span>

## <span data-ttu-id="36070-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="36070-130">RELATED LINKS</span></span>

[<span data-ttu-id="36070-131">新-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="36070-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="36070-132">移除-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="36070-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="36070-133">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="36070-133">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


