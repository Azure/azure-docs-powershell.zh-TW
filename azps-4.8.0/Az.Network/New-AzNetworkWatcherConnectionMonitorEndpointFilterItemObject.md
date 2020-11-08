---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointfilteritemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject.md
ms.openlocfilehash: c06052ee28d849c5d07a941366efd15cbfeefe25
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970347"
---
# <span data-ttu-id="707f2-101">New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject</span><span class="sxs-lookup"><span data-stu-id="707f2-101">New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject</span></span>

## <span data-ttu-id="707f2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="707f2-102">SYNOPSIS</span></span>
<span data-ttu-id="707f2-103">建立連線監視器端點篩選項目。</span><span class="sxs-lookup"><span data-stu-id="707f2-103">Creates a connection monitor endpoint filter item.</span></span>

## <span data-ttu-id="707f2-104">句法</span><span class="sxs-lookup"><span data-stu-id="707f2-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="707f2-105">說明</span><span class="sxs-lookup"><span data-stu-id="707f2-105">DESCRIPTION</span></span>
<span data-ttu-id="707f2-106">New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject Cmdlet 會建立端點篩選項目。</span><span class="sxs-lookup"><span data-stu-id="707f2-106">The New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject cmdlet creates endpoint filter item.</span></span>

## <span data-ttu-id="707f2-107">示例</span><span class="sxs-lookup"><span data-stu-id="707f2-107">EXAMPLES</span></span>

### <span data-ttu-id="707f2-108">範例1</span><span class="sxs-lookup"><span data-stu-id="707f2-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type "AgentAddress" -Address "10.0.0.1"
```

<span data-ttu-id="707f2-109">類型： AgentAddress 位址：10.0.0。1</span><span class="sxs-lookup"><span data-stu-id="707f2-109">Type    : AgentAddress Address : 10.0.0.1</span></span>

## <span data-ttu-id="707f2-110">參數</span><span class="sxs-lookup"><span data-stu-id="707f2-110">PARAMETERS</span></span>

### <span data-ttu-id="707f2-111">-位址</span><span class="sxs-lookup"><span data-stu-id="707f2-111">-Address</span></span>
<span data-ttu-id="707f2-112">篩選項目的位址。</span><span class="sxs-lookup"><span data-stu-id="707f2-112">The address of the filter item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="707f2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="707f2-113">-DefaultProfile</span></span>
<span data-ttu-id="707f2-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="707f2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="707f2-115">-類型</span><span class="sxs-lookup"><span data-stu-id="707f2-115">-Type</span></span>
<span data-ttu-id="707f2-116">篩選中所包含的專案類型。</span><span class="sxs-lookup"><span data-stu-id="707f2-116">The type of item included in the filter.</span></span> <span data-ttu-id="707f2-117">目前僅支援 ' AgentAddress」。</span><span class="sxs-lookup"><span data-stu-id="707f2-117">Currently only 'AgentAddress' is supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="707f2-118">-確認</span><span class="sxs-lookup"><span data-stu-id="707f2-118">-Confirm</span></span>
<span data-ttu-id="707f2-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="707f2-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="707f2-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="707f2-120">-WhatIf</span></span>
<span data-ttu-id="707f2-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="707f2-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="707f2-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="707f2-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="707f2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="707f2-123">CommonParameters</span></span>
<span data-ttu-id="707f2-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="707f2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="707f2-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="707f2-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="707f2-126">輸入</span><span class="sxs-lookup"><span data-stu-id="707f2-126">INPUTS</span></span>

### <span data-ttu-id="707f2-127">所有</span><span class="sxs-lookup"><span data-stu-id="707f2-127">None</span></span>

## <span data-ttu-id="707f2-128">輸出</span><span class="sxs-lookup"><span data-stu-id="707f2-128">OUTPUTS</span></span>

### <span data-ttu-id="707f2-129">PSConnectionMonitorEndpointFilterItem 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="707f2-129">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorEndpointFilterItem</span></span>

## <span data-ttu-id="707f2-130">筆記</span><span class="sxs-lookup"><span data-stu-id="707f2-130">NOTES</span></span>

## <span data-ttu-id="707f2-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="707f2-131">RELATED LINKS</span></span>
