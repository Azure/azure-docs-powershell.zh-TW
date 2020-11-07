---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 58e26de74abb46234f6985c3973b5bbe494bd0ad
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956971"
---
# <span data-ttu-id="9d21b-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="9d21b-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="9d21b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9d21b-102">SYNOPSIS</span></span>
<span data-ttu-id="9d21b-103">建立連接監視器端點。</span><span class="sxs-lookup"><span data-stu-id="9d21b-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="9d21b-104">句法</span><span class="sxs-lookup"><span data-stu-id="9d21b-104">SYNTAX</span></span>

### <span data-ttu-id="9d21b-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9d21b-105">SetByResourceId</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject [-Name <String>] -ResourceId <String>
 [-FilterType <String>]
 [-FilterItem <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d21b-106">SetByAddress</span><span class="sxs-lookup"><span data-stu-id="9d21b-106">SetByAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject [-Name <String>] [-Address <String>] [-FilterType <String>]
 [-FilterItem <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d21b-107">說明</span><span class="sxs-lookup"><span data-stu-id="9d21b-107">DESCRIPTION</span></span>
<span data-ttu-id="9d21b-108">New-AzNetworkWatcherConnectionMonitorEndpointObject Cmdlet 會建立連接監視器端點。</span><span class="sxs-lookup"><span data-stu-id="9d21b-108">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="9d21b-109">示例</span><span class="sxs-lookup"><span data-stu-id="9d21b-109">EXAMPLES</span></span>

### <span data-ttu-id="9d21b-110">範例1</span><span class="sxs-lookup"><span data-stu-id="9d21b-110">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type "AgentAddress" -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name "workspaceEndpoint" -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

<span data-ttu-id="9d21b-111">名稱： workspaceEndpoint ResourceId：/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace 位址：篩選： {"類型"： "Include"，"專案"： [{"類型"： "AgentAddress"，"Address"： "WIN-P0HGNDO2S1B"}]}</span><span class="sxs-lookup"><span data-stu-id="9d21b-111">Name       : workspaceEndpoint ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Filter     : { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="9d21b-112">參數</span><span class="sxs-lookup"><span data-stu-id="9d21b-112">PARAMETERS</span></span>

### <span data-ttu-id="9d21b-113">-位址</span><span class="sxs-lookup"><span data-stu-id="9d21b-113">-Address</span></span>
<span data-ttu-id="9d21b-114">連線監視端點的位址 (IP 或功能變數名稱) 。</span><span class="sxs-lookup"><span data-stu-id="9d21b-114">Address of the connection monitor endpoint (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: SetByAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d21b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d21b-115">-DefaultProfile</span></span>
<span data-ttu-id="9d21b-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d21b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d21b-117">-FilterItem</span><span class="sxs-lookup"><span data-stu-id="9d21b-117">-FilterItem</span></span>
<span data-ttu-id="9d21b-118">篩選中的專案清單。</span><span class="sxs-lookup"><span data-stu-id="9d21b-118">List of items in the filter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d21b-119">-FilterType</span><span class="sxs-lookup"><span data-stu-id="9d21b-119">-FilterType</span></span>
<span data-ttu-id="9d21b-120">端點篩選的行為。</span><span class="sxs-lookup"><span data-stu-id="9d21b-120">The behavior of the endpoint filter.</span></span> <span data-ttu-id="9d21b-121">目前僅支援 "Include"。</span><span class="sxs-lookup"><span data-stu-id="9d21b-121">Currently only 'Include' is supported.</span></span>

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

### <span data-ttu-id="9d21b-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="9d21b-122">-Name</span></span>
<span data-ttu-id="9d21b-123">[連線監視者] 端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="9d21b-123">The name of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="9d21b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d21b-124">-ResourceId</span></span>
<span data-ttu-id="9d21b-125">[連線監視者] 端點的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9d21b-125">Resource ID of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d21b-126">-確認</span><span class="sxs-lookup"><span data-stu-id="9d21b-126">-Confirm</span></span>
<span data-ttu-id="9d21b-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9d21b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d21b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d21b-128">-WhatIf</span></span>
<span data-ttu-id="9d21b-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9d21b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d21b-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9d21b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d21b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d21b-131">CommonParameters</span></span>
<span data-ttu-id="9d21b-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9d21b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d21b-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9d21b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d21b-134">輸入</span><span class="sxs-lookup"><span data-stu-id="9d21b-134">INPUTS</span></span>

### <span data-ttu-id="9d21b-135">所有</span><span class="sxs-lookup"><span data-stu-id="9d21b-135">None</span></span>

## <span data-ttu-id="9d21b-136">輸出</span><span class="sxs-lookup"><span data-stu-id="9d21b-136">OUTPUTS</span></span>

### <span data-ttu-id="9d21b-137">PSNetworkWatcherConnectionMonitorEndpointObject 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9d21b-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="9d21b-138">筆記</span><span class="sxs-lookup"><span data-stu-id="9d21b-138">NOTES</span></span>

## <span data-ttu-id="9d21b-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="9d21b-139">RELATED LINKS</span></span>
