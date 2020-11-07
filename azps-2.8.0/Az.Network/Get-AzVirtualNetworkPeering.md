---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: e2b4625536124cdb5352c97564cd4c2792dadb96
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789490"
---
# <span data-ttu-id="8b8aa-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="8b8aa-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="8b8aa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8b8aa-102">SYNOPSIS</span></span>
<span data-ttu-id="8b8aa-103">取得虛擬網路對等。</span><span class="sxs-lookup"><span data-stu-id="8b8aa-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="8b8aa-104">句法</span><span class="sxs-lookup"><span data-stu-id="8b8aa-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b8aa-105">說明</span><span class="sxs-lookup"><span data-stu-id="8b8aa-105">DESCRIPTION</span></span>
<span data-ttu-id="8b8aa-106">**AzVirtualNetworkPeering** Cmdlet 會取得虛擬網路對等。</span><span class="sxs-lookup"><span data-stu-id="8b8aa-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="8b8aa-107">示例</span><span class="sxs-lookup"><span data-stu-id="8b8aa-107">EXAMPLES</span></span>

### <span data-ttu-id="8b8aa-108">範例1：在兩個虛擬網路之間取得對等</span><span class="sxs-lookup"><span data-stu-id="8b8aa-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

### <span data-ttu-id="8b8aa-109">範例2：取得虛擬網路中的所有 peerings</span><span class="sxs-lookup"><span data-stu-id="8b8aa-109">Example 2: Get all peerings in virtual network</span></span>
```
# Get all virtual network peerings located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1To*" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="8b8aa-110">參數</span><span class="sxs-lookup"><span data-stu-id="8b8aa-110">PARAMETERS</span></span>

### <span data-ttu-id="8b8aa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b8aa-111">-DefaultProfile</span></span>
<span data-ttu-id="8b8aa-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8b8aa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b8aa-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="8b8aa-113">-Name</span></span>
<span data-ttu-id="8b8aa-114">指定虛擬網路對等名稱。</span><span class="sxs-lookup"><span data-stu-id="8b8aa-114">Specifies the virtual network peering name.</span></span>

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

### <span data-ttu-id="8b8aa-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b8aa-115">-ResourceGroupName</span></span>
<span data-ttu-id="8b8aa-116">指定虛擬網路對等所屬的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8b8aa-116">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="8b8aa-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="8b8aa-117">-VirtualNetworkName</span></span>
<span data-ttu-id="8b8aa-118">指定此 Cmdlet 取得的虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="8b8aa-118">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8b8aa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b8aa-119">CommonParameters</span></span>
<span data-ttu-id="8b8aa-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8b8aa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b8aa-121">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8b8aa-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b8aa-122">輸入</span><span class="sxs-lookup"><span data-stu-id="8b8aa-122">INPUTS</span></span>

### <span data-ttu-id="8b8aa-123">System.object</span><span class="sxs-lookup"><span data-stu-id="8b8aa-123">System.String</span></span>

## <span data-ttu-id="8b8aa-124">輸出</span><span class="sxs-lookup"><span data-stu-id="8b8aa-124">OUTPUTS</span></span>

### <span data-ttu-id="8b8aa-125">PSVirtualNetworkPeering 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8b8aa-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="8b8aa-126">筆記</span><span class="sxs-lookup"><span data-stu-id="8b8aa-126">NOTES</span></span>

## <span data-ttu-id="8b8aa-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="8b8aa-127">RELATED LINKS</span></span>

[<span data-ttu-id="8b8aa-128">附加 AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="8b8aa-128">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="8b8aa-129">移除-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="8b8aa-129">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="8b8aa-130">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="8b8aa-130">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
