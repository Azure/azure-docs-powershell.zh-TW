---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: 75725505e7c5239f1b5dc8f05d4cdfe3cf2b4903
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794343"
---
# <span data-ttu-id="e8aba-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e8aba-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="e8aba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8aba-102">SYNOPSIS</span></span>
<span data-ttu-id="e8aba-103">取得虛擬網路對等。</span><span class="sxs-lookup"><span data-stu-id="e8aba-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="e8aba-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8aba-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8aba-105">說明</span><span class="sxs-lookup"><span data-stu-id="e8aba-105">DESCRIPTION</span></span>
<span data-ttu-id="e8aba-106">**AzVirtualNetworkPeering** Cmdlet 會取得虛擬網路對等。</span><span class="sxs-lookup"><span data-stu-id="e8aba-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="e8aba-107">示例</span><span class="sxs-lookup"><span data-stu-id="e8aba-107">EXAMPLES</span></span>

### <span data-ttu-id="e8aba-108">範例1：在兩個虛擬網路之間取得對等</span><span class="sxs-lookup"><span data-stu-id="e8aba-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="e8aba-109">參數</span><span class="sxs-lookup"><span data-stu-id="e8aba-109">PARAMETERS</span></span>

### <span data-ttu-id="e8aba-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8aba-110">-DefaultProfile</span></span>
<span data-ttu-id="e8aba-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8aba-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8aba-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8aba-112">-Name</span></span>
<span data-ttu-id="e8aba-113">指定虛擬網路對等名稱。</span><span class="sxs-lookup"><span data-stu-id="e8aba-113">Specifies the virtual network peering name.</span></span>

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

### <span data-ttu-id="e8aba-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8aba-114">-ResourceGroupName</span></span>
<span data-ttu-id="e8aba-115">指定虛擬網路對等所屬的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e8aba-115">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="e8aba-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e8aba-116">-VirtualNetworkName</span></span>
<span data-ttu-id="e8aba-117">指定此 Cmdlet 取得的虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="e8aba-117">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e8aba-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8aba-118">CommonParameters</span></span>
<span data-ttu-id="e8aba-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8aba-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8aba-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e8aba-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8aba-121">輸入</span><span class="sxs-lookup"><span data-stu-id="e8aba-121">INPUTS</span></span>

## <span data-ttu-id="e8aba-122">輸出</span><span class="sxs-lookup"><span data-stu-id="e8aba-122">OUTPUTS</span></span>

### <span data-ttu-id="e8aba-123">PSVirtualNetworkPeering 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e8aba-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="e8aba-124">筆記</span><span class="sxs-lookup"><span data-stu-id="e8aba-124">NOTES</span></span>

## <span data-ttu-id="e8aba-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8aba-125">RELATED LINKS</span></span>

[<span data-ttu-id="e8aba-126">附加 AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e8aba-126">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="e8aba-127">移除-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e8aba-127">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="e8aba-128">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e8aba-128">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)


