---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
ms.openlocfilehash: da0dde546d5875c1a29bd02805f40c7f12a68188
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790033"
---
# <span data-ttu-id="c7f6a-101">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c7f6a-101">Get-AzVirtualNetwork</span></span>

## <span data-ttu-id="c7f6a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c7f6a-102">SYNOPSIS</span></span>
<span data-ttu-id="c7f6a-103">取得資源群組中的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="c7f6a-103">Gets a virtual network in a resource group.</span></span>

## <span data-ttu-id="c7f6a-104">句法</span><span class="sxs-lookup"><span data-stu-id="c7f6a-104">SYNTAX</span></span>

### <span data-ttu-id="c7f6a-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="c7f6a-105">NoExpand</span></span>
```
Get-AzVirtualNetwork [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c7f6a-106">擴充</span><span class="sxs-lookup"><span data-stu-id="c7f6a-106">Expand</span></span>
```
Get-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7f6a-107">說明</span><span class="sxs-lookup"><span data-stu-id="c7f6a-107">DESCRIPTION</span></span>
<span data-ttu-id="c7f6a-108">**AzVirtualNetwork** Cmdlet 會取得一或多個虛擬網路 n a 資源群組。</span><span class="sxs-lookup"><span data-stu-id="c7f6a-108">The **Get-AzVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="c7f6a-109">示例</span><span class="sxs-lookup"><span data-stu-id="c7f6a-109">EXAMPLES</span></span>

### <span data-ttu-id="c7f6a-110">1：檢索虛擬網路</span><span class="sxs-lookup"><span data-stu-id="c7f6a-110">1: Retrieve a virtual network</span></span>
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

<span data-ttu-id="c7f6a-111">這個命令會在 [資源] 群組 TestResourceGroup 中取得名為 MyVirtualNetwork 的虛擬網路</span><span class="sxs-lookup"><span data-stu-id="c7f6a-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="c7f6a-112">2：使用篩選器列出虛擬網路</span><span class="sxs-lookup"><span data-stu-id="c7f6a-112">2: List virtual networks using filter</span></span>
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

<span data-ttu-id="c7f6a-113">這個命令會取得以 "MyVirtualNetwork" 為開頭的所有虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="c7f6a-113">This command gets all virtual networks that start with "MyVirtualNetwork".</span></span>

## <span data-ttu-id="c7f6a-114">參數</span><span class="sxs-lookup"><span data-stu-id="c7f6a-114">PARAMETERS</span></span>

### <span data-ttu-id="c7f6a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7f6a-115">-DefaultProfile</span></span>
<span data-ttu-id="c7f6a-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c7f6a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7f6a-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="c7f6a-117">-ExpandResource</span></span>
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

### <span data-ttu-id="c7f6a-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="c7f6a-118">-Name</span></span>
<span data-ttu-id="c7f6a-119">指定此 Cmdlet 所取得之虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="c7f6a-119">Specifies the name of the virtual network that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c7f6a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7f6a-120">-ResourceGroupName</span></span>
<span data-ttu-id="c7f6a-121">指定虛擬網路所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c7f6a-121">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="c7f6a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7f6a-122">CommonParameters</span></span>
<span data-ttu-id="c7f6a-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c7f6a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7f6a-124">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c7f6a-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7f6a-125">輸入</span><span class="sxs-lookup"><span data-stu-id="c7f6a-125">INPUTS</span></span>

### <span data-ttu-id="c7f6a-126">System.object</span><span class="sxs-lookup"><span data-stu-id="c7f6a-126">System.String</span></span>

## <span data-ttu-id="c7f6a-127">輸出</span><span class="sxs-lookup"><span data-stu-id="c7f6a-127">OUTPUTS</span></span>

### <span data-ttu-id="c7f6a-128">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c7f6a-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="c7f6a-129">筆記</span><span class="sxs-lookup"><span data-stu-id="c7f6a-129">NOTES</span></span>

## <span data-ttu-id="c7f6a-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="c7f6a-130">RELATED LINKS</span></span>

[<span data-ttu-id="c7f6a-131">新-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c7f6a-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="c7f6a-132">移除-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c7f6a-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="c7f6a-133">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c7f6a-133">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


