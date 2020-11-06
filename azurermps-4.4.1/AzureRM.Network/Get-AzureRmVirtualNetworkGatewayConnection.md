---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 3d58e2f9fbd62826084df329cd7047a293ef0291
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449976"
---
# <span data-ttu-id="00319-101">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="00319-101">Get-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="00319-102">摘要</span><span class="sxs-lookup"><span data-stu-id="00319-102">SYNOPSIS</span></span>
<span data-ttu-id="00319-103">取得虛擬網路閘道連線</span><span class="sxs-lookup"><span data-stu-id="00319-103">Gets a Virtual Network Gateway Connection</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00319-104">句法</span><span class="sxs-lookup"><span data-stu-id="00319-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00319-105">說明</span><span class="sxs-lookup"><span data-stu-id="00319-105">DESCRIPTION</span></span>
<span data-ttu-id="00319-106">虛擬網路閘道連線是代表連接至 Azure 中虛擬網路閘道的 IPsec 隧道 (點對點或 Vnet 到 Vnet) 的物件。</span><span class="sxs-lookup"><span data-stu-id="00319-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="00319-107">**AzureRmVirtualNetworkGatewayConnection** Cmdlet 會根據名稱和資源群組名稱，傳回連線物件。</span><span class="sxs-lookup"><span data-stu-id="00319-107">The **Get-AzureRmVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="00319-108">示例</span><span class="sxs-lookup"><span data-stu-id="00319-108">EXAMPLES</span></span>

### <span data-ttu-id="00319-109">1：取得虛擬網路閘道連線</span><span class="sxs-lookup"><span data-stu-id="00319-109">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzureRmVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="00319-110">傳回資源群組 "myRG" 中名稱為 "myTunnel" 的虛擬網路閘道連線物件</span><span class="sxs-lookup"><span data-stu-id="00319-110">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="00319-111">參數</span><span class="sxs-lookup"><span data-stu-id="00319-111">PARAMETERS</span></span>

### <span data-ttu-id="00319-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="00319-112">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00319-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00319-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="00319-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00319-114">-DefaultProfile</span></span>
<span data-ttu-id="00319-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="00319-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00319-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00319-116">CommonParameters</span></span>
<span data-ttu-id="00319-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="00319-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00319-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="00319-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00319-119">輸入</span><span class="sxs-lookup"><span data-stu-id="00319-119">INPUTS</span></span>

## <span data-ttu-id="00319-120">輸出</span><span class="sxs-lookup"><span data-stu-id="00319-120">OUTPUTS</span></span>

### <span data-ttu-id="00319-121">PSVirtualNetworkGatewayConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="00319-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="00319-122">筆記</span><span class="sxs-lookup"><span data-stu-id="00319-122">NOTES</span></span>

## <span data-ttu-id="00319-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="00319-123">RELATED LINKS</span></span>

