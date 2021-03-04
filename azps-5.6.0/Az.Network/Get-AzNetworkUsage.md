---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkUsage.md
ms.openlocfilehash: 7072d7a2c61f11433fbf75e99366769e4e86b277
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902558"
---
# <span data-ttu-id="73260-101">Get-AzNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="73260-101">Get-AzNetworkUsage</span></span>

## <span data-ttu-id="73260-102">簡介</span><span class="sxs-lookup"><span data-stu-id="73260-102">SYNOPSIS</span></span>
<span data-ttu-id="73260-103">列出訂閱的網路使用狀況</span><span class="sxs-lookup"><span data-stu-id="73260-103">Lists network usages for a subscription</span></span>

## <span data-ttu-id="73260-104">語法</span><span class="sxs-lookup"><span data-stu-id="73260-104">SYNTAX</span></span>

```
Get-AzNetworkUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73260-105">描述</span><span class="sxs-lookup"><span data-stu-id="73260-105">DESCRIPTION</span></span>
<span data-ttu-id="73260-106">Cmdlet Get-AzNetworkUsage會限制和目前網路資源的使用量。</span><span class="sxs-lookup"><span data-stu-id="73260-106">The Get-AzNetworkUsage cmdlet gets limits and current usage for Network resources.</span></span>

## <span data-ttu-id="73260-107">例子</span><span class="sxs-lookup"><span data-stu-id="73260-107">EXAMPLES</span></span>

### <span data-ttu-id="73260-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="73260-108">Example 1</span></span>
```
PS C:\> Get-AzNetworkUsage -Location westcentralus

ResourceType : Virtual Networks
CurrentValue : 6
Limit        : 50

ResourceType : Static Public IP Addresses
CurrentValue : 1
Limit        : 20

ResourceType : Network Security Groups
CurrentValue : 2
Limit        : 100

ResourceType : Public IP Addresses
CurrentValue : 6
Limit        : 60

ResourceType : Network Interfaces
CurrentValue : 1
Limit        : 300

ResourceType : Load Balancers
CurrentValue : 1
Limit        : 100

ResourceType : Application Gateways
CurrentValue : 1
Limit        : 50

ResourceType : Route Tables
CurrentValue : 0
Limit        : 100

ResourceType : Route Filters
CurrentValue : 0
Limit        : 1000

ResourceType : Network Watchers
CurrentValue : 1
Limit        : 1

ResourceType : Packet Captures
CurrentValue : 0
Limit        : 10
```

<span data-ttu-id="73260-109">在西半部地區獲得資源使用量資料</span><span class="sxs-lookup"><span data-stu-id="73260-109">Gets resources usage data in westcentralus region</span></span>

## <span data-ttu-id="73260-110">參數</span><span class="sxs-lookup"><span data-stu-id="73260-110">PARAMETERS</span></span>

### <span data-ttu-id="73260-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73260-111">-DefaultProfile</span></span>
<span data-ttu-id="73260-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="73260-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73260-113">-位置</span><span class="sxs-lookup"><span data-stu-id="73260-113">-Location</span></span>
<span data-ttu-id="73260-114">查詢資源使用量的位置。</span><span class="sxs-lookup"><span data-stu-id="73260-114">The location where resource usage is queried.</span></span>

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

### <span data-ttu-id="73260-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73260-115">CommonParameters</span></span>
<span data-ttu-id="73260-116">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="73260-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73260-117">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73260-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73260-118">輸入</span><span class="sxs-lookup"><span data-stu-id="73260-118">INPUTS</span></span>

### <span data-ttu-id="73260-119">System.String</span><span class="sxs-lookup"><span data-stu-id="73260-119">System.String</span></span>

## <span data-ttu-id="73260-120">輸出</span><span class="sxs-lookup"><span data-stu-id="73260-120">OUTPUTS</span></span>

### <span data-ttu-id="73260-121">Microsoft.Azure.Commands.Network.models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="73260-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span></span>

## <span data-ttu-id="73260-122">筆記</span><span class="sxs-lookup"><span data-stu-id="73260-122">NOTES</span></span>

## <span data-ttu-id="73260-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="73260-123">RELATED LINKS</span></span>
