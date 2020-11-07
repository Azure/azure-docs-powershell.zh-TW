---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkpeering
schema: 2.0.0
ms.openlocfilehash: b5e3cf083f003a643639635c61ca8e3f13e16eaf
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800830"
---
# <span data-ttu-id="1f032-101">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="1f032-101">Get-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="1f032-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1f032-102">SYNOPSIS</span></span>
<span data-ttu-id="1f032-103">取得虛擬網路對等。</span><span class="sxs-lookup"><span data-stu-id="1f032-103">Gets the virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f032-104">句法</span><span class="sxs-lookup"><span data-stu-id="1f032-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f032-105">說明</span><span class="sxs-lookup"><span data-stu-id="1f032-105">DESCRIPTION</span></span>
<span data-ttu-id="1f032-106">**AzureRmVirtualNetworkPeering** Cmdlet 會取得虛擬網路對等。</span><span class="sxs-lookup"><span data-stu-id="1f032-106">The **Get-AzureRmVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="1f032-107">示例</span><span class="sxs-lookup"><span data-stu-id="1f032-107">EXAMPLES</span></span>

### <span data-ttu-id="1f032-108">範例1：在兩個虛擬網路之間取得對等</span><span class="sxs-lookup"><span data-stu-id="1f032-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="1f032-109">參數</span><span class="sxs-lookup"><span data-stu-id="1f032-109">PARAMETERS</span></span>

### <span data-ttu-id="1f032-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f032-110">-DefaultProfile</span></span>
<span data-ttu-id="1f032-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1f032-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f032-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="1f032-112">-Name</span></span>
<span data-ttu-id="1f032-113">指定虛擬網路對等名稱。</span><span class="sxs-lookup"><span data-stu-id="1f032-113">Specifies the virtual network peering name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f032-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f032-114">-ResourceGroupName</span></span>
<span data-ttu-id="1f032-115">指定虛擬網路對等所屬的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="1f032-115">Specifies the resource group name that the virtual network peering belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f032-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="1f032-116">-VirtualNetworkName</span></span>
<span data-ttu-id="1f032-117">指定此 Cmdlet 取得的虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="1f032-117">Specifies the virtual network name that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f032-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f032-118">CommonParameters</span></span>
<span data-ttu-id="1f032-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1f032-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f032-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1f032-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f032-121">輸入</span><span class="sxs-lookup"><span data-stu-id="1f032-121">INPUTS</span></span>

## <span data-ttu-id="1f032-122">輸出</span><span class="sxs-lookup"><span data-stu-id="1f032-122">OUTPUTS</span></span>

### <span data-ttu-id="1f032-123">PSVirtualNetworkPeering 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1f032-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="1f032-124">筆記</span><span class="sxs-lookup"><span data-stu-id="1f032-124">NOTES</span></span>

## <span data-ttu-id="1f032-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f032-125">RELATED LINKS</span></span>

[<span data-ttu-id="1f032-126">附加 AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="1f032-126">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="1f032-127">移除-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="1f032-127">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="1f032-128">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="1f032-128">Set-AzureRmVirtualNetworkPeering</span></span>](./Set-AzureRmVirtualNetworkPeering.md)


