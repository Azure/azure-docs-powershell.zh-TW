---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermlocalnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 1a2a8aa8405be5dfc5275a07d253f06f1134e3e7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801265"
---
# <span data-ttu-id="3790e-101">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3790e-101">Get-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="3790e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3790e-102">SYNOPSIS</span></span>
<span data-ttu-id="3790e-103">取得局域網路閘道</span><span class="sxs-lookup"><span data-stu-id="3790e-103">Gets a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3790e-104">句法</span><span class="sxs-lookup"><span data-stu-id="3790e-104">SYNTAX</span></span>

```
Get-AzureRmLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3790e-105">說明</span><span class="sxs-lookup"><span data-stu-id="3790e-105">DESCRIPTION</span></span>
<span data-ttu-id="3790e-106">本機網路閘道是代表您的 VPN 裝置內部部署的物件。</span><span class="sxs-lookup"><span data-stu-id="3790e-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="3790e-107">**AzureRmLocalNetworkGateway** Cmdlet 會根據名稱和資源群組名稱，傳回代表您的內部部署閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="3790e-107">The **Get-AzureRmLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="3790e-108">示例</span><span class="sxs-lookup"><span data-stu-id="3790e-108">EXAMPLES</span></span>

### <span data-ttu-id="3790e-109">1：取得局域網路閘道</span><span class="sxs-lookup"><span data-stu-id="3790e-109">1: Get a Local Network Gateway</span></span>
```
Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="3790e-110">傳回資源群組 "myRG" 中名稱為 "myLocalGW" 的本機網路閘道物件</span><span class="sxs-lookup"><span data-stu-id="3790e-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="3790e-111">參數</span><span class="sxs-lookup"><span data-stu-id="3790e-111">PARAMETERS</span></span>

### <span data-ttu-id="3790e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3790e-112">-DefaultProfile</span></span>
<span data-ttu-id="3790e-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3790e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3790e-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="3790e-114">-Name</span></span>
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

### <span data-ttu-id="3790e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3790e-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="3790e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3790e-116">CommonParameters</span></span>
<span data-ttu-id="3790e-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3790e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3790e-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3790e-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3790e-119">輸入</span><span class="sxs-lookup"><span data-stu-id="3790e-119">INPUTS</span></span>

## <span data-ttu-id="3790e-120">輸出</span><span class="sxs-lookup"><span data-stu-id="3790e-120">OUTPUTS</span></span>

### <span data-ttu-id="3790e-121">PSLocalNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3790e-121">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="3790e-122">筆記</span><span class="sxs-lookup"><span data-stu-id="3790e-122">NOTES</span></span>

## <span data-ttu-id="3790e-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="3790e-123">RELATED LINKS</span></span>

