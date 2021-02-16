---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: b17f6e7245cb79a5b1098463e3c6dc0ca2b01c68
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128939"
---
# <span data-ttu-id="a4a90-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a4a90-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="a4a90-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a4a90-102">SYNOPSIS</span></span>
<span data-ttu-id="a4a90-103">取得虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="a4a90-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="a4a90-104">句法</span><span class="sxs-lookup"><span data-stu-id="a4a90-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4a90-105">說明</span><span class="sxs-lookup"><span data-stu-id="a4a90-105">DESCRIPTION</span></span>
<span data-ttu-id="a4a90-106">虛擬網路閘道是代表您在 Azure 中閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="a4a90-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="a4a90-107">**AzVirtualNetworkGateway** Cmdlet 會根據名稱和資源群組名稱，傳回 Azure 中閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="a4a90-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="a4a90-108">示例</span><span class="sxs-lookup"><span data-stu-id="a4a90-108">EXAMPLES</span></span>

### <span data-ttu-id="a4a90-109">範例1：取得虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="a4a90-109">Example 1: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway1 -ResourceGroupName myRG
```

<span data-ttu-id="a4a90-110">傳回資源群組 "myRG" 中名稱為 "myGateway1" 的虛擬網路閘道物件</span><span class="sxs-lookup"><span data-stu-id="a4a90-110">Returns the object of the Virtual Network Gateway with the name "myGateway1" within the resource group "myRG"</span></span>

### <span data-ttu-id="a4a90-111">範例2：取得虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="a4a90-111">Example 2: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway* -ResourceGroupName myRG
```

<span data-ttu-id="a4a90-112">傳回資源群組 "myRG" 中以 "myGateway" 為開頭的所有虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="a4a90-112">Returns all Virtual Network Gateways that start with "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="a4a90-113">參數</span><span class="sxs-lookup"><span data-stu-id="a4a90-113">PARAMETERS</span></span>

### <span data-ttu-id="a4a90-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4a90-114">-DefaultProfile</span></span>
<span data-ttu-id="a4a90-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a4a90-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4a90-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="a4a90-116">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="a4a90-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4a90-117">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="a4a90-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4a90-118">CommonParameters</span></span>
<span data-ttu-id="a4a90-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a4a90-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4a90-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a4a90-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4a90-121">輸入</span><span class="sxs-lookup"><span data-stu-id="a4a90-121">INPUTS</span></span>

### <span data-ttu-id="a4a90-122">System.object</span><span class="sxs-lookup"><span data-stu-id="a4a90-122">System.String</span></span>

## <span data-ttu-id="a4a90-123">輸出</span><span class="sxs-lookup"><span data-stu-id="a4a90-123">OUTPUTS</span></span>

### <span data-ttu-id="a4a90-124">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a4a90-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="a4a90-125">筆記</span><span class="sxs-lookup"><span data-stu-id="a4a90-125">NOTES</span></span>

## <span data-ttu-id="a4a90-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4a90-126">RELATED LINKS</span></span>

[<span data-ttu-id="a4a90-127">新-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a4a90-127">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="a4a90-128">移除-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a4a90-128">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="a4a90-129">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a4a90-129">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="a4a90-130">調整大小-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a4a90-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="a4a90-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a4a90-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
