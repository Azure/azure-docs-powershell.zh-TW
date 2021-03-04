---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
ms.openlocfilehash: 542a207e60e451d97ba5edcbdccc45b84b14f760
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903530"
---
# <span data-ttu-id="657cc-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="657cc-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="657cc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="657cc-102">SYNOPSIS</span></span>
<span data-ttu-id="657cc-103">建立連接監視器測試組。</span><span class="sxs-lookup"><span data-stu-id="657cc-103">Create a connection monitor test configuration.</span></span>

## <span data-ttu-id="657cc-104">語法</span><span class="sxs-lookup"><span data-stu-id="657cc-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name <String> -TestFrequencySec <Int32>
 -ProtocolConfiguration <PSNetworkWatcherConnectionMonitorProtocolConfiguration>
 [-SuccessThresholdChecksFailedPercent <Int32>] [-SuccessThresholdRoundTripTimeMs <Double>]
 [-PreferredIPVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="657cc-105">描述</span><span class="sxs-lookup"><span data-stu-id="657cc-105">DESCRIPTION</span></span>
<span data-ttu-id="657cc-106">Cmdlet New-AzNetworkWatcherConnectionMonitorTestConfigurationObject建立連接監視器測試組。</span><span class="sxs-lookup"><span data-stu-id="657cc-106">The New-AzNetworkWatcherConnectionMonitorTestConfigurationObject cmdlet creates a connection monitor test configuration.</span></span>

## <span data-ttu-id="657cc-107">例子</span><span class="sxs-lookup"><span data-stu-id="657cc-107">EXAMPLES</span></span>

### <span data-ttu-id="657cc-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="657cc-108">Example 1</span></span>
```powershell
PS C:\>$httpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -HttpProtocol -Port 443 -Method GET -RequestHeader @{"Allow" = "GET"} -ValidStatusCodeRange 2xx, 300-308 -PreferHTTPS
PS C:\>$httpTestConfiguration = New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name httpTC -TestFrequencySec 120 -ProtocolConfiguration $httpProtocolConfiguration -SuccessThresholdChecksFailedPercent 20 -SuccessThresholdRoundTripTimeMs 30
```

<span data-ttu-id="657cc-109">名稱 ： HTTPTC TestFrequencySec ： 120 PreferredIPVersion ： ProtocolConfiguration ： { "Port"： 443， "Method"： "GET"， "RequestHeaders"： [ { "Name"： "Allow"， "Value"： "GET" } ]， "ValidStatusCodeRanges"： [ "2xx"， "300-308" ]， "PreferHTTPS"： true } SuccessThreshold ： { "ChecksFailedPercent"： 20， "RoundTripTimeMs"： 30 }</span><span class="sxs-lookup"><span data-stu-id="657cc-109">Name                  : httpTC TestFrequencySec      : 120 PreferredIPVersion    : ProtocolConfiguration : { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true } SuccessThreshold      : { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 }</span></span> 

## <span data-ttu-id="657cc-110">參數</span><span class="sxs-lookup"><span data-stu-id="657cc-110">PARAMETERS</span></span>

### <span data-ttu-id="657cc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="657cc-111">-DefaultProfile</span></span>
<span data-ttu-id="657cc-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="657cc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="657cc-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="657cc-113">-Name</span></span>
<span data-ttu-id="657cc-114">連接監視器測試組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="657cc-114">The name of the connection monitor test configuration.</span></span>

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

### <span data-ttu-id="657cc-115">-PreferredIPVersion</span><span class="sxs-lookup"><span data-stu-id="657cc-115">-PreferredIPVersion</span></span>
<span data-ttu-id="657cc-116">用於測試評估的偏好 IP 版本。</span><span class="sxs-lookup"><span data-stu-id="657cc-116">The preferred IP version to use in test evaluation.</span></span> <span data-ttu-id="657cc-117">根據其他參數，連接監視器可能會選擇使用不同的版本。</span><span class="sxs-lookup"><span data-stu-id="657cc-117">The connection monitor may choose to use a different version depending on other parameters.</span></span>

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

### <span data-ttu-id="657cc-118">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="657cc-118">-ProtocolConfiguration</span></span>
<span data-ttu-id="657cc-119">用來在某些通訊協定上執行測試評估的參數。</span><span class="sxs-lookup"><span data-stu-id="657cc-119">The parameters used to perform test evaluation over some protocol.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorProtocolConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="657cc-120">-SuccessThresholdChecksFailedPercent</span><span class="sxs-lookup"><span data-stu-id="657cc-120">-SuccessThresholdChecksFailedPercent</span></span>
<span data-ttu-id="657cc-121">測試評估成功所允許的失敗檢查百分比上限。</span><span class="sxs-lookup"><span data-stu-id="657cc-121">The maximum percentage of failed checks permitted for a test to evaluate as successful.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="657cc-122">-SuccessThresholdRoundTripTimeMs</span><span class="sxs-lookup"><span data-stu-id="657cc-122">-SuccessThresholdRoundTripTimeMs</span></span>
<span data-ttu-id="657cc-123">測試評估成功所允許的最大往返時間 ，以毫秒為單位。</span><span class="sxs-lookup"><span data-stu-id="657cc-123">The maximum round-trip time in milliseconds permitted for a test to evaluate as successful.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="657cc-124">-TestFrequencySec</span><span class="sxs-lookup"><span data-stu-id="657cc-124">-TestFrequencySec</span></span>
<span data-ttu-id="657cc-125">測試評估的頻率 ，以碼錶示。</span><span class="sxs-lookup"><span data-stu-id="657cc-125">The frequency of test evaluation, in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: TestFrequency

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="657cc-126">-確認</span><span class="sxs-lookup"><span data-stu-id="657cc-126">-Confirm</span></span>
<span data-ttu-id="657cc-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="657cc-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="657cc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="657cc-128">-WhatIf</span></span>
<span data-ttu-id="657cc-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="657cc-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="657cc-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="657cc-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="657cc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="657cc-131">CommonParameters</span></span>
<span data-ttu-id="657cc-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="657cc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="657cc-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="657cc-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="657cc-134">輸入</span><span class="sxs-lookup"><span data-stu-id="657cc-134">INPUTS</span></span>

### <span data-ttu-id="657cc-135">沒有</span><span class="sxs-lookup"><span data-stu-id="657cc-135">None</span></span>

## <span data-ttu-id="657cc-136">輸出</span><span class="sxs-lookup"><span data-stu-id="657cc-136">OUTPUTS</span></span>

### <span data-ttu-id="657cc-137">Microsoft.Azure.Commands.Network.models.PSNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="657cc-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="657cc-138">筆記</span><span class="sxs-lookup"><span data-stu-id="657cc-138">NOTES</span></span>

## <span data-ttu-id="657cc-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="657cc-139">RELATED LINKS</span></span>
