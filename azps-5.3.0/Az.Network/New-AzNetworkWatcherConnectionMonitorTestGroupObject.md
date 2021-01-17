---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestgroupobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
ms.openlocfilehash: af924210c8f1fb465881f054815f874ff5d99429
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286887"
---
# <span data-ttu-id="89f90-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="89f90-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="89f90-102">摘要</span><span class="sxs-lookup"><span data-stu-id="89f90-102">SYNOPSIS</span></span>
<span data-ttu-id="89f90-103">建立連線監視測試組。</span><span class="sxs-lookup"><span data-stu-id="89f90-103">Create a connection monitor test group.</span></span>

## <span data-ttu-id="89f90-104">句法</span><span class="sxs-lookup"><span data-stu-id="89f90-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name <String>
 -TestConfiguration <PSNetworkWatcherConnectionMonitorTestConfigurationObject[]>
 -Source <PSNetworkWatcherConnectionMonitorEndpointObject[]>
 -Destination <PSNetworkWatcherConnectionMonitorEndpointObject[]> [-Disable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89f90-105">說明</span><span class="sxs-lookup"><span data-stu-id="89f90-105">DESCRIPTION</span></span>
<span data-ttu-id="89f90-106">New-AzNetworkWatcherConnectionMonitorTestGroupObject Cmdlet 會建立連接監視器測試群組。</span><span class="sxs-lookup"><span data-stu-id="89f90-106">The New-AzNetworkWatcherConnectionMonitorTestGroupObject cmdlet creates a connection monitor test group.</span></span>

## <span data-ttu-id="89f90-107">示例</span><span class="sxs-lookup"><span data-stu-id="89f90-107">EXAMPLES</span></span>

### <span data-ttu-id="89f90-108">範例1：建立含 2 testConfigurations、w 來源和2目的地端點的測試群組</span><span class="sxs-lookup"><span data-stu-id="89f90-108">Example 1: Create a test group with 2 testConfigurations, w source and 2 destination endpoints</span></span>

```
$testGroup1 = New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name testGroup1 -TestConfiguration $tcpTestConfiguration, $icmpTestConfiguration -Source $vmEndpoint, $workspaceEndpoint -Destination $bingEndpoint, $googleEndpoint
```

## <span data-ttu-id="89f90-109">參數</span><span class="sxs-lookup"><span data-stu-id="89f90-109">PARAMETERS</span></span>

### <span data-ttu-id="89f90-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89f90-110">-DefaultProfile</span></span>
<span data-ttu-id="89f90-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="89f90-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89f90-112">-目的地</span><span class="sxs-lookup"><span data-stu-id="89f90-112">-Destination</span></span>
<span data-ttu-id="89f90-113">目的地端點清單。</span><span class="sxs-lookup"><span data-stu-id="89f90-113">List of destination endpoints.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89f90-114">-停用</span><span class="sxs-lookup"><span data-stu-id="89f90-114">-Disable</span></span>
<span data-ttu-id="89f90-115">指示是否已停用 [測試] 群組的標記。</span><span class="sxs-lookup"><span data-stu-id="89f90-115">Flag indicating whether test group is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89f90-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="89f90-116">-Name</span></span>
<span data-ttu-id="89f90-117">測試組的名稱。</span><span class="sxs-lookup"><span data-stu-id="89f90-117">The test group name.</span></span>

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

### <span data-ttu-id="89f90-118">-來源</span><span class="sxs-lookup"><span data-stu-id="89f90-118">-Source</span></span>
<span data-ttu-id="89f90-119">來源端點清單。</span><span class="sxs-lookup"><span data-stu-id="89f90-119">List of source endpoints.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89f90-120">-TestConfiguration</span><span class="sxs-lookup"><span data-stu-id="89f90-120">-TestConfiguration</span></span>
<span data-ttu-id="89f90-121">測試組態清單。</span><span class="sxs-lookup"><span data-stu-id="89f90-121">List of test configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89f90-122">-確認</span><span class="sxs-lookup"><span data-stu-id="89f90-122">-Confirm</span></span>
<span data-ttu-id="89f90-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="89f90-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89f90-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89f90-124">-WhatIf</span></span>
<span data-ttu-id="89f90-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="89f90-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89f90-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="89f90-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89f90-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89f90-127">CommonParameters</span></span>
<span data-ttu-id="89f90-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="89f90-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89f90-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="89f90-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89f90-130">輸入</span><span class="sxs-lookup"><span data-stu-id="89f90-130">INPUTS</span></span>

### <span data-ttu-id="89f90-131">所有</span><span class="sxs-lookup"><span data-stu-id="89f90-131">None</span></span>

## <span data-ttu-id="89f90-132">輸出</span><span class="sxs-lookup"><span data-stu-id="89f90-132">OUTPUTS</span></span>

### <span data-ttu-id="89f90-133">PSNetworkWatcherConnectionMonitorTestGroupObject 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="89f90-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="89f90-134">筆記</span><span class="sxs-lookup"><span data-stu-id="89f90-134">NOTES</span></span>

## <span data-ttu-id="89f90-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="89f90-135">RELATED LINKS</span></span>
