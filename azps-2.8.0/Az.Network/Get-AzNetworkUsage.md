---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkUsage.md
ms.openlocfilehash: 74da4bba721f415b48ee8ff626a1bfcf1d313b64
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789562"
---
# <span data-ttu-id="55f5a-101">Get-AzNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="55f5a-101">Get-AzNetworkUsage</span></span>

## <span data-ttu-id="55f5a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="55f5a-102">SYNOPSIS</span></span>
<span data-ttu-id="55f5a-103">列出訂閱的網路使用方式</span><span class="sxs-lookup"><span data-stu-id="55f5a-103">Lists network usages for a subscription</span></span>

## <span data-ttu-id="55f5a-104">句法</span><span class="sxs-lookup"><span data-stu-id="55f5a-104">SYNTAX</span></span>

```
Get-AzNetworkUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55f5a-105">說明</span><span class="sxs-lookup"><span data-stu-id="55f5a-105">DESCRIPTION</span></span>
<span data-ttu-id="55f5a-106">Get-AzNetworkUsage Cmdlet 會取得網路資源的限制和目前使用量。</span><span class="sxs-lookup"><span data-stu-id="55f5a-106">The Get-AzNetworkUsage cmdlet gets limits and current usage for Network resources.</span></span>

## <span data-ttu-id="55f5a-107">示例</span><span class="sxs-lookup"><span data-stu-id="55f5a-107">EXAMPLES</span></span>

### <span data-ttu-id="55f5a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="55f5a-108">Example 1</span></span>
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

<span data-ttu-id="55f5a-109">取得 westcentralus 區域中的資源使用資料</span><span class="sxs-lookup"><span data-stu-id="55f5a-109">Gets resources usage data in westcentralus region</span></span>

## <span data-ttu-id="55f5a-110">參數</span><span class="sxs-lookup"><span data-stu-id="55f5a-110">PARAMETERS</span></span>

### <span data-ttu-id="55f5a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55f5a-111">-DefaultProfile</span></span>
<span data-ttu-id="55f5a-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="55f5a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55f5a-113">-位置</span><span class="sxs-lookup"><span data-stu-id="55f5a-113">-Location</span></span>
<span data-ttu-id="55f5a-114">查詢資源使用狀況的位置。</span><span class="sxs-lookup"><span data-stu-id="55f5a-114">The location where resource usage is queried.</span></span>

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

### <span data-ttu-id="55f5a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55f5a-115">CommonParameters</span></span>
<span data-ttu-id="55f5a-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="55f5a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55f5a-117">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="55f5a-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55f5a-118">輸入</span><span class="sxs-lookup"><span data-stu-id="55f5a-118">INPUTS</span></span>

### <span data-ttu-id="55f5a-119">System.object</span><span class="sxs-lookup"><span data-stu-id="55f5a-119">System.String</span></span>

## <span data-ttu-id="55f5a-120">輸出</span><span class="sxs-lookup"><span data-stu-id="55f5a-120">OUTPUTS</span></span>

### <span data-ttu-id="55f5a-121">PSUsage 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="55f5a-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span></span>

## <span data-ttu-id="55f5a-122">筆記</span><span class="sxs-lookup"><span data-stu-id="55f5a-122">NOTES</span></span>

## <span data-ttu-id="55f5a-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="55f5a-123">RELATED LINKS</span></span>
