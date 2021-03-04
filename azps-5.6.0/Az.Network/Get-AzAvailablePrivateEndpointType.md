---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azavailableprivateendpointtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
ms.openlocfilehash: ae7c7bdd41f21c3f9263a8ea65aab722512543f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912738"
---
# <span data-ttu-id="42f58-101">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="42f58-101">Get-AzAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="42f58-102">簡介</span><span class="sxs-lookup"><span data-stu-id="42f58-102">SYNOPSIS</span></span>
<span data-ttu-id="42f58-103">在位置中返回可用的私人結束點類型。</span><span class="sxs-lookup"><span data-stu-id="42f58-103">Return available private end point types in the location.</span></span>

## <span data-ttu-id="42f58-104">語法</span><span class="sxs-lookup"><span data-stu-id="42f58-104">SYNTAX</span></span>

```
Get-AzAvailablePrivateEndpointType -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42f58-105">描述</span><span class="sxs-lookup"><span data-stu-id="42f58-105">DESCRIPTION</span></span>
<span data-ttu-id="42f58-106">**Get-AzAvailablePrivateEndpointType** Cmdlet 會傳回該位置中所有可用的私人結束點類型。</span><span class="sxs-lookup"><span data-stu-id="42f58-106">The **Get-AzAvailablePrivateEndpointType** cmdlet returns all available private end point types in the location.</span></span>

## <span data-ttu-id="42f58-107">例子</span><span class="sxs-lookup"><span data-stu-id="42f58-107">EXAMPLES</span></span>

### <span data-ttu-id="42f58-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="42f58-108">Example 1</span></span>
```powershell
Get-AzAvailablePrivateEndpointType -Location eastus

[
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename1",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Sql/servers"
  },
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename2",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Storage/accounts"
  },
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename3",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Cosmos/cosmosDbAccounts"
  }
]
```

<span data-ttu-id="42f58-109">此範例會返回該位置中所有可用的私人結束點類型。</span><span class="sxs-lookup"><span data-stu-id="42f58-109">This example returns all available private end point types in the location.</span></span>

## <span data-ttu-id="42f58-110">參數</span><span class="sxs-lookup"><span data-stu-id="42f58-110">PARAMETERS</span></span>

### <span data-ttu-id="42f58-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42f58-111">-DefaultProfile</span></span>
<span data-ttu-id="42f58-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="42f58-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42f58-113">-位置</span><span class="sxs-lookup"><span data-stu-id="42f58-113">-Location</span></span>
<span data-ttu-id="42f58-114">位置。</span><span class="sxs-lookup"><span data-stu-id="42f58-114">The location.</span></span>

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

### <span data-ttu-id="42f58-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42f58-115">-ResourceGroupName</span></span>
<span data-ttu-id="42f58-116">資源組名。</span><span class="sxs-lookup"><span data-stu-id="42f58-116">The resource group name.</span></span>

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

### <span data-ttu-id="42f58-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42f58-117">CommonParameters</span></span>
<span data-ttu-id="42f58-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="42f58-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42f58-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="42f58-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42f58-120">輸入</span><span class="sxs-lookup"><span data-stu-id="42f58-120">INPUTS</span></span>

### <span data-ttu-id="42f58-121">System.String</span><span class="sxs-lookup"><span data-stu-id="42f58-121">System.String</span></span>

## <span data-ttu-id="42f58-122">輸出</span><span class="sxs-lookup"><span data-stu-id="42f58-122">OUTPUTS</span></span>

### <span data-ttu-id="42f58-123">Microsoft.Azure.Commands.Network.models.PSAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="42f58-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="42f58-124">筆記</span><span class="sxs-lookup"><span data-stu-id="42f58-124">NOTES</span></span>

## <span data-ttu-id="42f58-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="42f58-125">RELATED LINKS</span></span>
