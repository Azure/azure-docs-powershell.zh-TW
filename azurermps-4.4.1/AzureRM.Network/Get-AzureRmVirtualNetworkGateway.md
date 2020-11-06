---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: ed57a1832e3581d4d49b285fa9e61c93b17be02c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449978"
---
# <span data-ttu-id="868c0-101">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="868c0-101">Get-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="868c0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="868c0-102">SYNOPSIS</span></span>
<span data-ttu-id="868c0-103">取得虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="868c0-103">Gets a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="868c0-104">句法</span><span class="sxs-lookup"><span data-stu-id="868c0-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="868c0-105">說明</span><span class="sxs-lookup"><span data-stu-id="868c0-105">DESCRIPTION</span></span>
<span data-ttu-id="868c0-106">虛擬網路閘道是代表您在 Azure 中閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="868c0-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="868c0-107">**AzureRmVirtualNetworkGateway** Cmdlet 會根據名稱和資源群組名稱，傳回 Azure 中閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="868c0-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="868c0-108">示例</span><span class="sxs-lookup"><span data-stu-id="868c0-108">EXAMPLES</span></span>

### <span data-ttu-id="868c0-109">1：取得虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="868c0-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="868c0-110">傳回資源群組 "myRG" 中名稱為 "myGateway" 的虛擬網路閘道物件</span><span class="sxs-lookup"><span data-stu-id="868c0-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="868c0-111">參數</span><span class="sxs-lookup"><span data-stu-id="868c0-111">PARAMETERS</span></span>

### <span data-ttu-id="868c0-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="868c0-112">-Name</span></span>
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

### <span data-ttu-id="868c0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="868c0-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="868c0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="868c0-114">-DefaultProfile</span></span>
<span data-ttu-id="868c0-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="868c0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="868c0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="868c0-116">CommonParameters</span></span>
<span data-ttu-id="868c0-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="868c0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="868c0-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="868c0-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="868c0-119">輸入</span><span class="sxs-lookup"><span data-stu-id="868c0-119">INPUTS</span></span>

## <span data-ttu-id="868c0-120">輸出</span><span class="sxs-lookup"><span data-stu-id="868c0-120">OUTPUTS</span></span>

### <span data-ttu-id="868c0-121">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="868c0-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="868c0-122">筆記</span><span class="sxs-lookup"><span data-stu-id="868c0-122">NOTES</span></span>

## <span data-ttu-id="868c0-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="868c0-123">RELATED LINKS</span></span>

