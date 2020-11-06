---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: c881232c065f8494b962a0e010865cbefe8bc0eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451620"
---
# <span data-ttu-id="f4fe9-101">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f4fe9-101">Get-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="f4fe9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f4fe9-102">SYNOPSIS</span></span>
<span data-ttu-id="f4fe9-103">取得局域網路閘道</span><span class="sxs-lookup"><span data-stu-id="f4fe9-103">Gets a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4fe9-104">句法</span><span class="sxs-lookup"><span data-stu-id="f4fe9-104">SYNTAX</span></span>

```
Get-AzureRmLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4fe9-105">說明</span><span class="sxs-lookup"><span data-stu-id="f4fe9-105">DESCRIPTION</span></span>
<span data-ttu-id="f4fe9-106">本機網路閘道是代表您的 VPN 裝置內部部署的物件。</span><span class="sxs-lookup"><span data-stu-id="f4fe9-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="f4fe9-107">**AzureRmLocalNetworkGateway** Cmdlet 會根據名稱和資源群組名稱，傳回代表您的內部部署閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="f4fe9-107">The **Get-AzureRmLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="f4fe9-108">示例</span><span class="sxs-lookup"><span data-stu-id="f4fe9-108">EXAMPLES</span></span>

### <span data-ttu-id="f4fe9-109">1：取得局域網路閘道</span><span class="sxs-lookup"><span data-stu-id="f4fe9-109">1: Get a Local Network Gateway</span></span>
```
Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="f4fe9-110">傳回資源群組 "myRG" 中名稱為 "myLocalGW" 的本機網路閘道物件</span><span class="sxs-lookup"><span data-stu-id="f4fe9-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="f4fe9-111">參數</span><span class="sxs-lookup"><span data-stu-id="f4fe9-111">PARAMETERS</span></span>

### <span data-ttu-id="f4fe9-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="f4fe9-112">-Name</span></span>
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

### <span data-ttu-id="f4fe9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4fe9-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="f4fe9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4fe9-114">-DefaultProfile</span></span>
<span data-ttu-id="f4fe9-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4fe9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4fe9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4fe9-116">CommonParameters</span></span>
<span data-ttu-id="f4fe9-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f4fe9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4fe9-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f4fe9-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4fe9-119">輸入</span><span class="sxs-lookup"><span data-stu-id="f4fe9-119">INPUTS</span></span>

## <span data-ttu-id="f4fe9-120">輸出</span><span class="sxs-lookup"><span data-stu-id="f4fe9-120">OUTPUTS</span></span>

### <span data-ttu-id="f4fe9-121">PSLocalNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f4fe9-121">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="f4fe9-122">筆記</span><span class="sxs-lookup"><span data-stu-id="f4fe9-122">NOTES</span></span>

## <span data-ttu-id="f4fe9-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4fe9-123">RELATED LINKS</span></span>

