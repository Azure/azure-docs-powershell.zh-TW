---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 1700ec112767397653201ff16608afbfb4af8f3e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800857"
---
# <span data-ttu-id="5b798-101">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5b798-101">Get-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="5b798-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5b798-102">SYNOPSIS</span></span>
<span data-ttu-id="5b798-103">取得虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="5b798-103">Gets a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b798-104">句法</span><span class="sxs-lookup"><span data-stu-id="5b798-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b798-105">說明</span><span class="sxs-lookup"><span data-stu-id="5b798-105">DESCRIPTION</span></span>
<span data-ttu-id="5b798-106">虛擬網路閘道是代表您在 Azure 中閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="5b798-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="5b798-107">**AzureRmVirtualNetworkGateway** Cmdlet 會根據名稱和資源群組名稱，傳回 Azure 中閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="5b798-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="5b798-108">示例</span><span class="sxs-lookup"><span data-stu-id="5b798-108">EXAMPLES</span></span>

### <span data-ttu-id="5b798-109">1：取得虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="5b798-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="5b798-110">傳回資源群組 "myRG" 中名稱為 "myGateway" 的虛擬網路閘道物件</span><span class="sxs-lookup"><span data-stu-id="5b798-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="5b798-111">參數</span><span class="sxs-lookup"><span data-stu-id="5b798-111">PARAMETERS</span></span>

### <span data-ttu-id="5b798-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b798-112">-DefaultProfile</span></span>
<span data-ttu-id="5b798-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5b798-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b798-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="5b798-114">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b798-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b798-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="5b798-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b798-116">CommonParameters</span></span>
<span data-ttu-id="5b798-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5b798-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b798-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5b798-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b798-119">輸入</span><span class="sxs-lookup"><span data-stu-id="5b798-119">INPUTS</span></span>

## <span data-ttu-id="5b798-120">輸出</span><span class="sxs-lookup"><span data-stu-id="5b798-120">OUTPUTS</span></span>

### <span data-ttu-id="5b798-121">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5b798-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="5b798-122">筆記</span><span class="sxs-lookup"><span data-stu-id="5b798-122">NOTES</span></span>

## <span data-ttu-id="5b798-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b798-123">RELATED LINKS</span></span>

