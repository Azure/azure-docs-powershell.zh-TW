---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableprivateendpointtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
ms.openlocfilehash: a8f256f9a383b3cb7c7aed014474c1ea24706106
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789658"
---
# <span data-ttu-id="56895-101">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="56895-101">Get-AzAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="56895-102">摘要</span><span class="sxs-lookup"><span data-stu-id="56895-102">SYNOPSIS</span></span>
<span data-ttu-id="56895-103">傳回位置中可用的私有端點類型</span><span class="sxs-lookup"><span data-stu-id="56895-103">Return available private end point types in the location</span></span>

## <span data-ttu-id="56895-104">句法</span><span class="sxs-lookup"><span data-stu-id="56895-104">SYNTAX</span></span>

```
Get-AzAvailablePrivateEndpointType -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56895-105">說明</span><span class="sxs-lookup"><span data-stu-id="56895-105">DESCRIPTION</span></span>
<span data-ttu-id="56895-106">**AzAvailablePrivateEndpointType** Cmdlet 會傳回位置中所有可用的私有端點類型。</span><span class="sxs-lookup"><span data-stu-id="56895-106">The **Get-AzAvailablePrivateEndpointType** cmdlet returns all available private end point types in the location.</span></span>

## <span data-ttu-id="56895-107">示例</span><span class="sxs-lookup"><span data-stu-id="56895-107">EXAMPLES</span></span>

### <span data-ttu-id="56895-108">範例</span><span class="sxs-lookup"><span data-stu-id="56895-108">Example</span></span>
```
Get-AzAvailablePrivateEndpointType -Location eastus

[
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename1",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsot.Sql/servers"
  },
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename2",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsot.Storage/accounts"
  },
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename3",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsot.Cosmos/cosmosDbAccounts"
  }
]
```

<span data-ttu-id="56895-109">這個範例會傳回位置中所有可用的私有端點類型。</span><span class="sxs-lookup"><span data-stu-id="56895-109">This example returns all available private end point types in the location.</span></span>

## <span data-ttu-id="56895-110">參數</span><span class="sxs-lookup"><span data-stu-id="56895-110">PARAMETERS</span></span>

### <span data-ttu-id="56895-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56895-111">-DefaultProfile</span></span>
<span data-ttu-id="56895-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="56895-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56895-113">-位置</span><span class="sxs-lookup"><span data-stu-id="56895-113">-Location</span></span>
<span data-ttu-id="56895-114">位置。</span><span class="sxs-lookup"><span data-stu-id="56895-114">The location.</span></span>

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

### <span data-ttu-id="56895-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56895-115">-ResourceGroupName</span></span>
<span data-ttu-id="56895-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="56895-116">The resource group name.</span></span>

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

### <span data-ttu-id="56895-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56895-117">CommonParameters</span></span>
<span data-ttu-id="56895-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="56895-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56895-119">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="56895-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56895-120">輸入</span><span class="sxs-lookup"><span data-stu-id="56895-120">INPUTS</span></span>

### <span data-ttu-id="56895-121">System.object</span><span class="sxs-lookup"><span data-stu-id="56895-121">System.String</span></span>

## <span data-ttu-id="56895-122">輸出</span><span class="sxs-lookup"><span data-stu-id="56895-122">OUTPUTS</span></span>

### <span data-ttu-id="56895-123">PSAvailablePrivateEndpointType 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="56895-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="56895-124">筆記</span><span class="sxs-lookup"><span data-stu-id="56895-124">NOTES</span></span>

## <span data-ttu-id="56895-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="56895-125">RELATED LINKS</span></span>
