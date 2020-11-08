---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableprivateendpointtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
ms.openlocfilehash: 1ca9e604a1371d83fdedd2986534fa8926b6286b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126538"
---
# <span data-ttu-id="148b6-101">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="148b6-101">Get-AzAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="148b6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="148b6-102">SYNOPSIS</span></span>
<span data-ttu-id="148b6-103">傳回位置中可用的私有端點類型。</span><span class="sxs-lookup"><span data-stu-id="148b6-103">Return available private end point types in the location.</span></span>

## <span data-ttu-id="148b6-104">句法</span><span class="sxs-lookup"><span data-stu-id="148b6-104">SYNTAX</span></span>

```
Get-AzAvailablePrivateEndpointType -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="148b6-105">說明</span><span class="sxs-lookup"><span data-stu-id="148b6-105">DESCRIPTION</span></span>
<span data-ttu-id="148b6-106">**AzAvailablePrivateEndpointType** Cmdlet 會傳回位置中所有可用的私有端點類型。</span><span class="sxs-lookup"><span data-stu-id="148b6-106">The **Get-AzAvailablePrivateEndpointType** cmdlet returns all available private end point types in the location.</span></span>

## <span data-ttu-id="148b6-107">示例</span><span class="sxs-lookup"><span data-stu-id="148b6-107">EXAMPLES</span></span>

### <span data-ttu-id="148b6-108">範例1</span><span class="sxs-lookup"><span data-stu-id="148b6-108">Example 1</span></span>
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

<span data-ttu-id="148b6-109">這個範例會傳回位置中所有可用的私有端點類型。</span><span class="sxs-lookup"><span data-stu-id="148b6-109">This example returns all available private end point types in the location.</span></span>

## <span data-ttu-id="148b6-110">參數</span><span class="sxs-lookup"><span data-stu-id="148b6-110">PARAMETERS</span></span>

### <span data-ttu-id="148b6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="148b6-111">-DefaultProfile</span></span>
<span data-ttu-id="148b6-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="148b6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="148b6-113">-位置</span><span class="sxs-lookup"><span data-stu-id="148b6-113">-Location</span></span>
<span data-ttu-id="148b6-114">位置。</span><span class="sxs-lookup"><span data-stu-id="148b6-114">The location.</span></span>

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

### <span data-ttu-id="148b6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="148b6-115">-ResourceGroupName</span></span>
<span data-ttu-id="148b6-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="148b6-116">The resource group name.</span></span>

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

### <span data-ttu-id="148b6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="148b6-117">CommonParameters</span></span>
<span data-ttu-id="148b6-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="148b6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="148b6-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="148b6-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="148b6-120">輸入</span><span class="sxs-lookup"><span data-stu-id="148b6-120">INPUTS</span></span>

### <span data-ttu-id="148b6-121">System.object</span><span class="sxs-lookup"><span data-stu-id="148b6-121">System.String</span></span>

## <span data-ttu-id="148b6-122">輸出</span><span class="sxs-lookup"><span data-stu-id="148b6-122">OUTPUTS</span></span>

### <span data-ttu-id="148b6-123">PSAvailablePrivateEndpointType 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="148b6-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="148b6-124">筆記</span><span class="sxs-lookup"><span data-stu-id="148b6-124">NOTES</span></span>

## <span data-ttu-id="148b6-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="148b6-125">RELATED LINKS</span></span>
