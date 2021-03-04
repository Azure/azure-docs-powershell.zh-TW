---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestgroupobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
ms.openlocfilehash: 4ab9feb0d99bc808cfabb481baf81bb12e050f28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903525"
---
# <span data-ttu-id="327e7-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="327e7-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="327e7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="327e7-102">SYNOPSIS</span></span>
<span data-ttu-id="327e7-103">建立連接監視器測試群組。</span><span class="sxs-lookup"><span data-stu-id="327e7-103">Create a connection monitor test group.</span></span>

## <span data-ttu-id="327e7-104">語法</span><span class="sxs-lookup"><span data-stu-id="327e7-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name <String>
 -TestConfiguration <PSNetworkWatcherConnectionMonitorTestConfigurationObject[]>
 -Source <PSNetworkWatcherConnectionMonitorEndpointObject[]>
 -Destination <PSNetworkWatcherConnectionMonitorEndpointObject[]> [-Disable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="327e7-105">描述</span><span class="sxs-lookup"><span data-stu-id="327e7-105">DESCRIPTION</span></span>
<span data-ttu-id="327e7-106">Cmdlet New-AzNetworkWatcherConnectionMonitorTestGroupObject建立一個連接監視器測試群組。</span><span class="sxs-lookup"><span data-stu-id="327e7-106">The New-AzNetworkWatcherConnectionMonitorTestGroupObject cmdlet creates a connection monitor test group.</span></span>

## <span data-ttu-id="327e7-107">例子</span><span class="sxs-lookup"><span data-stu-id="327e7-107">EXAMPLES</span></span>

### <span data-ttu-id="327e7-108">範例 1：使用 2 個 testConfigurations、w source 和 2 個目的地端點建立測試群組</span><span class="sxs-lookup"><span data-stu-id="327e7-108">Example 1: Create a test group with 2 testConfigurations, w source and 2 destination endpoints</span></span>

```
$testGroup1 = New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name testGroup1 -TestConfiguration $tcpTestConfiguration, $icmpTestConfiguration -Source $vmEndpoint, $workspaceEndpoint -Destination $bingEndpoint, $googleEndpoint
```

## <span data-ttu-id="327e7-109">參數</span><span class="sxs-lookup"><span data-stu-id="327e7-109">PARAMETERS</span></span>

### <span data-ttu-id="327e7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="327e7-110">-DefaultProfile</span></span>
<span data-ttu-id="327e7-111">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="327e7-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="327e7-112">-目的地</span><span class="sxs-lookup"><span data-stu-id="327e7-112">-Destination</span></span>
<span data-ttu-id="327e7-113">目的地端點清單。</span><span class="sxs-lookup"><span data-stu-id="327e7-113">List of destination endpoints.</span></span>

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

### <span data-ttu-id="327e7-114">-停用</span><span class="sxs-lookup"><span data-stu-id="327e7-114">-Disable</span></span>
<span data-ttu-id="327e7-115">指出測試群組是否已停用的標標。</span><span class="sxs-lookup"><span data-stu-id="327e7-115">Flag indicating whether test group is disabled.</span></span>

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

### <span data-ttu-id="327e7-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="327e7-116">-Name</span></span>
<span data-ttu-id="327e7-117">測試組名。</span><span class="sxs-lookup"><span data-stu-id="327e7-117">The test group name.</span></span>

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

### <span data-ttu-id="327e7-118">-來源</span><span class="sxs-lookup"><span data-stu-id="327e7-118">-Source</span></span>
<span data-ttu-id="327e7-119">來源端點清單。</span><span class="sxs-lookup"><span data-stu-id="327e7-119">List of source endpoints.</span></span>

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

### <span data-ttu-id="327e7-120">-TestConfiguration</span><span class="sxs-lookup"><span data-stu-id="327e7-120">-TestConfiguration</span></span>
<span data-ttu-id="327e7-121">測試組配置清單。</span><span class="sxs-lookup"><span data-stu-id="327e7-121">List of test configuration.</span></span>

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

### <span data-ttu-id="327e7-122">-確認</span><span class="sxs-lookup"><span data-stu-id="327e7-122">-Confirm</span></span>
<span data-ttu-id="327e7-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="327e7-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="327e7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="327e7-124">-WhatIf</span></span>
<span data-ttu-id="327e7-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="327e7-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="327e7-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="327e7-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="327e7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="327e7-127">CommonParameters</span></span>
<span data-ttu-id="327e7-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="327e7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="327e7-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="327e7-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="327e7-130">輸入</span><span class="sxs-lookup"><span data-stu-id="327e7-130">INPUTS</span></span>

### <span data-ttu-id="327e7-131">沒有</span><span class="sxs-lookup"><span data-stu-id="327e7-131">None</span></span>

## <span data-ttu-id="327e7-132">輸出</span><span class="sxs-lookup"><span data-stu-id="327e7-132">OUTPUTS</span></span>

### <span data-ttu-id="327e7-133">Microsoft.Azure.Commands.Network.models.PSNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="327e7-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="327e7-134">筆記</span><span class="sxs-lookup"><span data-stu-id="327e7-134">NOTES</span></span>

## <span data-ttu-id="327e7-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="327e7-135">RELATED LINKS</span></span>
