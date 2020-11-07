---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 8658dcf73d6cf1549ac6471e79269883abdf7616
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794349"
---
# <span data-ttu-id="39e51-101">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="39e51-101">Get-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="39e51-102">摘要</span><span class="sxs-lookup"><span data-stu-id="39e51-102">SYNOPSIS</span></span>
<span data-ttu-id="39e51-103">取得虛擬網路閘道連線</span><span class="sxs-lookup"><span data-stu-id="39e51-103">Gets a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="39e51-104">句法</span><span class="sxs-lookup"><span data-stu-id="39e51-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39e51-105">說明</span><span class="sxs-lookup"><span data-stu-id="39e51-105">DESCRIPTION</span></span>
<span data-ttu-id="39e51-106">虛擬網路閘道連線是代表連接至 Azure 中虛擬網路閘道的 IPsec 隧道 (點對點或 Vnet 到 Vnet) 的物件。</span><span class="sxs-lookup"><span data-stu-id="39e51-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="39e51-107">**AzVirtualNetworkGatewayConnection** Cmdlet 會根據名稱和資源群組名稱，傳回連線物件。</span><span class="sxs-lookup"><span data-stu-id="39e51-107">The **Get-AzVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="39e51-108">示例</span><span class="sxs-lookup"><span data-stu-id="39e51-108">EXAMPLES</span></span>

### <span data-ttu-id="39e51-109">1：取得虛擬網路閘道連線</span><span class="sxs-lookup"><span data-stu-id="39e51-109">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="39e51-110">傳回資源群組 "myRG" 中名稱為 "myTunnel" 的虛擬網路閘道連線物件</span><span class="sxs-lookup"><span data-stu-id="39e51-110">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="39e51-111">參數</span><span class="sxs-lookup"><span data-stu-id="39e51-111">PARAMETERS</span></span>

### <span data-ttu-id="39e51-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39e51-112">-DefaultProfile</span></span>
<span data-ttu-id="39e51-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="39e51-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39e51-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="39e51-114">-Name</span></span>
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

### <span data-ttu-id="39e51-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39e51-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="39e51-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39e51-116">CommonParameters</span></span>
<span data-ttu-id="39e51-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="39e51-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39e51-118">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="39e51-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39e51-119">輸入</span><span class="sxs-lookup"><span data-stu-id="39e51-119">INPUTS</span></span>

## <span data-ttu-id="39e51-120">輸出</span><span class="sxs-lookup"><span data-stu-id="39e51-120">OUTPUTS</span></span>

### <span data-ttu-id="39e51-121">PSVirtualNetworkGatewayConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="39e51-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="39e51-122">筆記</span><span class="sxs-lookup"><span data-stu-id="39e51-122">NOTES</span></span>

## <span data-ttu-id="39e51-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="39e51-123">RELATED LINKS</span></span>

