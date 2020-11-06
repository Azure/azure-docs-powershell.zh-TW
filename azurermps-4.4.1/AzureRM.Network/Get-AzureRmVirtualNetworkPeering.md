---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 7ffe74795725e0751ed45dcc76864078ec372ac2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449619"
---
# <span data-ttu-id="b7acf-101">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b7acf-101">Get-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="b7acf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b7acf-102">SYNOPSIS</span></span>
<span data-ttu-id="b7acf-103">取得虛擬網路對等。</span><span class="sxs-lookup"><span data-stu-id="b7acf-103">Gets the virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7acf-104">句法</span><span class="sxs-lookup"><span data-stu-id="b7acf-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7acf-105">說明</span><span class="sxs-lookup"><span data-stu-id="b7acf-105">DESCRIPTION</span></span>
<span data-ttu-id="b7acf-106">**AzureRmVirtualNetworkPeering** Cmdlet 會取得虛擬網路對等。</span><span class="sxs-lookup"><span data-stu-id="b7acf-106">The **Get-AzureRmVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="b7acf-107">示例</span><span class="sxs-lookup"><span data-stu-id="b7acf-107">EXAMPLES</span></span>

### <span data-ttu-id="b7acf-108">範例1：在兩個虛擬網路之間取得對等</span><span class="sxs-lookup"><span data-stu-id="b7acf-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="b7acf-109">參數</span><span class="sxs-lookup"><span data-stu-id="b7acf-109">PARAMETERS</span></span>

### <span data-ttu-id="b7acf-110">-名稱</span><span class="sxs-lookup"><span data-stu-id="b7acf-110">-Name</span></span>
<span data-ttu-id="b7acf-111">指定虛擬網路對等名稱。</span><span class="sxs-lookup"><span data-stu-id="b7acf-111">Specifies the virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7acf-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7acf-112">-ResourceGroupName</span></span>
<span data-ttu-id="b7acf-113">指定虛擬網路對等所屬的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="b7acf-113">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="b7acf-114">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="b7acf-114">-VirtualNetworkName</span></span>
<span data-ttu-id="b7acf-115">指定此 Cmdlet 取得的虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="b7acf-115">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b7acf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7acf-116">-DefaultProfile</span></span>
<span data-ttu-id="b7acf-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b7acf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7acf-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7acf-118">CommonParameters</span></span>
<span data-ttu-id="b7acf-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b7acf-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7acf-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b7acf-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7acf-121">輸入</span><span class="sxs-lookup"><span data-stu-id="b7acf-121">INPUTS</span></span>

## <span data-ttu-id="b7acf-122">輸出</span><span class="sxs-lookup"><span data-stu-id="b7acf-122">OUTPUTS</span></span>

### <span data-ttu-id="b7acf-123">PSVirtualNetworkPeering 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b7acf-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="b7acf-124">筆記</span><span class="sxs-lookup"><span data-stu-id="b7acf-124">NOTES</span></span>

## <span data-ttu-id="b7acf-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="b7acf-125">RELATED LINKS</span></span>

[<span data-ttu-id="b7acf-126">附加 AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b7acf-126">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="b7acf-127">移除-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b7acf-127">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="b7acf-128">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b7acf-128">Set-AzureRmVirtualNetworkPeering</span></span>](./Set-AzureRmVirtualNetworkPeering.md)

