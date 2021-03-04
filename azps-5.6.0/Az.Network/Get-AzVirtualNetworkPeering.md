---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: 5648fe6049a7686d5f3930de6ea780598e2c0b06
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906438"
---
# <span data-ttu-id="98b7e-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="98b7e-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="98b7e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="98b7e-102">SYNOPSIS</span></span>
<span data-ttu-id="98b7e-103">進行虛擬網路對等。</span><span class="sxs-lookup"><span data-stu-id="98b7e-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="98b7e-104">語法</span><span class="sxs-lookup"><span data-stu-id="98b7e-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98b7e-105">描述</span><span class="sxs-lookup"><span data-stu-id="98b7e-105">DESCRIPTION</span></span>
<span data-ttu-id="98b7e-106">**Get-AzVirtualNetworkPeering** Cmdlet 會取得虛擬網路對等。</span><span class="sxs-lookup"><span data-stu-id="98b7e-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="98b7e-107">例子</span><span class="sxs-lookup"><span data-stu-id="98b7e-107">EXAMPLES</span></span>

### <span data-ttu-id="98b7e-108">範例 1：在兩個虛擬網路之間取得對等</span><span class="sxs-lookup"><span data-stu-id="98b7e-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

### <span data-ttu-id="98b7e-109">範例 2：在虛擬網路中取得所有對等互連</span><span class="sxs-lookup"><span data-stu-id="98b7e-109">Example 2: Get all peerings in virtual network</span></span>
```
# Get all virtual network peerings located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1To*" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="98b7e-110">參數</span><span class="sxs-lookup"><span data-stu-id="98b7e-110">PARAMETERS</span></span>

### <span data-ttu-id="98b7e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98b7e-111">-DefaultProfile</span></span>
<span data-ttu-id="98b7e-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="98b7e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98b7e-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="98b7e-113">-Name</span></span>
<span data-ttu-id="98b7e-114">指定虛擬網路對等名稱。</span><span class="sxs-lookup"><span data-stu-id="98b7e-114">Specifies the virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="98b7e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98b7e-115">-ResourceGroupName</span></span>
<span data-ttu-id="98b7e-116">指定虛擬網路對等所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="98b7e-116">Specifies the resource group name that the virtual network peering belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98b7e-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="98b7e-117">-VirtualNetworkName</span></span>
<span data-ttu-id="98b7e-118">指定此 Cmdlet 所獲取的虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="98b7e-118">Specifies the virtual network name that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98b7e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98b7e-119">CommonParameters</span></span>
<span data-ttu-id="98b7e-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="98b7e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98b7e-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98b7e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98b7e-122">輸入</span><span class="sxs-lookup"><span data-stu-id="98b7e-122">INPUTS</span></span>

### <span data-ttu-id="98b7e-123">System.String</span><span class="sxs-lookup"><span data-stu-id="98b7e-123">System.String</span></span>

## <span data-ttu-id="98b7e-124">輸出</span><span class="sxs-lookup"><span data-stu-id="98b7e-124">OUTPUTS</span></span>

### <span data-ttu-id="98b7e-125">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="98b7e-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="98b7e-126">筆記</span><span class="sxs-lookup"><span data-stu-id="98b7e-126">NOTES</span></span>

## <span data-ttu-id="98b7e-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="98b7e-127">RELATED LINKS</span></span>

[<span data-ttu-id="98b7e-128">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="98b7e-128">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="98b7e-129">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="98b7e-129">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="98b7e-130">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="98b7e-130">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
