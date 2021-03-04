---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 385301bf9cab32474aea59937de09003356a5798
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903554"
---
# <span data-ttu-id="94e3b-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="94e3b-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="94e3b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="94e3b-102">SYNOPSIS</span></span>
<span data-ttu-id="94e3b-103">建立連接監視器端點。</span><span class="sxs-lookup"><span data-stu-id="94e3b-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="94e3b-104">語法</span><span class="sxs-lookup"><span data-stu-id="94e3b-104">SYNTAX</span></span>

### <span data-ttu-id="94e3b-105">AzureAZM</span><span class="sxs-lookup"><span data-stu-id="94e3b-105">AzureVM</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVM] -ResourceId <String>
 [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94e3b-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="94e3b-106">AzureVNet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVNet] -ResourceId <String>
 [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94e3b-107">AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="94e3b-107">AzureSubnet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureSubnet] -ResourceId <String>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94e3b-108">ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="94e3b-108">ExternalAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-ExternalAddress] -Address <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94e3b-109">MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="94e3b-109">MMAWorkspaceMachine</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceMachine] -ResourceId <String>
 -Address <String> [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94e3b-110">MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="94e3b-110">MMAWorkspaceNetwork</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceNetwork] -ResourceId <String>
 -IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94e3b-111">描述</span><span class="sxs-lookup"><span data-stu-id="94e3b-111">DESCRIPTION</span></span>
<span data-ttu-id="94e3b-112">New-AzNetworkWatcherConnectionMonitorEndpointObject Cmdlet 會建立連接監視器端點。</span><span class="sxs-lookup"><span data-stu-id="94e3b-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="94e3b-113">例子</span><span class="sxs-lookup"><span data-stu-id="94e3b-113">EXAMPLES</span></span>

### <span data-ttu-id="94e3b-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="94e3b-114">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointScopeItem1 = New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndpointObject -Name "workspaceEndpoint" -MMAWorkspaceMachine -ResourceId $MySrcResourceId1 -IncludeItem $SrcEndpointScopeItem1
```

<span data-ttu-id="94e3b-115">名稱 ： workspaceEndpoint 類型 ： MMAWorkspaceMachine ResourceId ： /subscriptions/00000000-0000-0000-0000-0000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address： Scope ： { "Include"： [ { "Address"： "WIN-P0HGNDO2S1B" } ] }</span><span class="sxs-lookup"><span data-stu-id="94e3b-115">Name       : workspaceEndpoint Type       : MMAWorkspaceMachine ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Scope     : { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="94e3b-116">參數</span><span class="sxs-lookup"><span data-stu-id="94e3b-116">PARAMETERS</span></span>

### <span data-ttu-id="94e3b-117">-Address</span><span class="sxs-lookup"><span data-stu-id="94e3b-117">-Address</span></span>
<span data-ttu-id="94e3b-118">IP 或功能變數名稱 (之連接監視器端點) 。</span><span class="sxs-lookup"><span data-stu-id="94e3b-118">Address of the connection monitor endpoint (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVM
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExternalAddress, MMAWorkspaceMachine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e3b-119">-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="94e3b-119">-AzureSubnet</span></span>
<span data-ttu-id="94e3b-120">Azure 子網端點切換。</span><span class="sxs-lookup"><span data-stu-id="94e3b-120">Azure Subnet endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e3b-121">-AzureAZM</span><span class="sxs-lookup"><span data-stu-id="94e3b-121">-AzureVM</span></span>
<span data-ttu-id="94e3b-122">Azure VM 端點切換。</span><span class="sxs-lookup"><span data-stu-id="94e3b-122">Azure VM endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVM
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e3b-123">-AzureVNet</span><span class="sxs-lookup"><span data-stu-id="94e3b-123">-AzureVNet</span></span>
<span data-ttu-id="94e3b-124">Azure Vnet 端點切換。</span><span class="sxs-lookup"><span data-stu-id="94e3b-124">Azure Vnet endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVNet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e3b-125">-CoverageLevel</span><span class="sxs-lookup"><span data-stu-id="94e3b-125">-CoverageLevel</span></span>
<span data-ttu-id="94e3b-126">測試端點的涵蓋範圍。</span><span class="sxs-lookup"><span data-stu-id="94e3b-126">Test coverage for the endpoint.</span></span>
<span data-ttu-id="94e3b-127">支援的值為預設值、最低、低於Average、Average、AboveAvergae、Full。</span><span class="sxs-lookup"><span data-stu-id="94e3b-127">Supported values are Default, Low, BelowAverage, Average, AboveAvergae, Full.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVNet, AzureSubnet, MMAWorkspaceNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e3b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94e3b-128">-DefaultProfile</span></span>
<span data-ttu-id="94e3b-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="94e3b-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94e3b-130">-ExcludeItem</span><span class="sxs-lookup"><span data-stu-id="94e3b-130">-ExcludeItem</span></span>
<span data-ttu-id="94e3b-131">需要從端點範圍排除的專案清單。</span><span class="sxs-lookup"><span data-stu-id="94e3b-131">List of items which need to be excluded from endpoint scope.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: AzureVNet, AzureSubnet, MMAWorkspaceNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e3b-132">-ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="94e3b-132">-ExternalAddress</span></span>
<span data-ttu-id="94e3b-133">外部地址端點切換。</span><span class="sxs-lookup"><span data-stu-id="94e3b-133">External Address endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExternalAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e3b-134">-IncludeItem</span><span class="sxs-lookup"><span data-stu-id="94e3b-134">-IncludeItem</span></span>
<span data-ttu-id="94e3b-135">需要包含在 endpont 範圍中的專案清單。</span><span class="sxs-lookup"><span data-stu-id="94e3b-135">List of items which need to be included into endpont scope.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: AzureVNet, MMAWorkspaceMachine
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e3b-136">-MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="94e3b-136">-MMAWorkspaceMachine</span></span>
<span data-ttu-id="94e3b-137">MMA Workspace Machine 端點開關。</span><span class="sxs-lookup"><span data-stu-id="94e3b-137">MMA Workspace Machine endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MMAWorkspaceMachine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e3b-138">-MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="94e3b-138">-MMAWorkspaceNetwork</span></span>
<span data-ttu-id="94e3b-139">MMA Workspace Network 端點切換。</span><span class="sxs-lookup"><span data-stu-id="94e3b-139">MMA Workspace Network endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e3b-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="94e3b-140">-Name</span></span>
<span data-ttu-id="94e3b-141">連接監視器端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="94e3b-141">The name of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="94e3b-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94e3b-142">-ResourceId</span></span>
<span data-ttu-id="94e3b-143">連接監視器端點的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="94e3b-143">Resource ID of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVM, AzureVNet, AzureSubnet, MMAWorkspaceMachine, MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e3b-144">-確認</span><span class="sxs-lookup"><span data-stu-id="94e3b-144">-Confirm</span></span>
<span data-ttu-id="94e3b-145">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="94e3b-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94e3b-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94e3b-146">-WhatIf</span></span>
<span data-ttu-id="94e3b-147">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="94e3b-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94e3b-148">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94e3b-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94e3b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94e3b-149">CommonParameters</span></span>
<span data-ttu-id="94e3b-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="94e3b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94e3b-151">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94e3b-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94e3b-152">輸入</span><span class="sxs-lookup"><span data-stu-id="94e3b-152">INPUTS</span></span>

### <span data-ttu-id="94e3b-153">沒有</span><span class="sxs-lookup"><span data-stu-id="94e3b-153">None</span></span>

## <span data-ttu-id="94e3b-154">輸出</span><span class="sxs-lookup"><span data-stu-id="94e3b-154">OUTPUTS</span></span>

### <span data-ttu-id="94e3b-155">Microsoft.Azure.Commands.Network.models.PSNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="94e3b-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="94e3b-156">筆記</span><span class="sxs-lookup"><span data-stu-id="94e3b-156">NOTES</span></span>

## <span data-ttu-id="94e3b-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="94e3b-157">RELATED LINKS</span></span>
