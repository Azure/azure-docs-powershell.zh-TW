---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicyintrusiondetectionbypasstraffic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionBypassTraffic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionBypassTraffic.md
ms.openlocfilehash: dd15a93fc2df022a0b016f9dae4845da13240534
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909346"
---
# <span data-ttu-id="0dbbd-101">New-AzFirewallPolicyIntrusionDetectionBypassTraffic</span><span class="sxs-lookup"><span data-stu-id="0dbbd-101">New-AzFirewallPolicyIntrusionDetectionBypassTraffic</span></span>

## <span data-ttu-id="0dbbd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0dbbd-102">SYNOPSIS</span></span>
<span data-ttu-id="0dbbd-103">建立新的 Azure 防火牆策略入侵偵測忽略流量設定</span><span class="sxs-lookup"><span data-stu-id="0dbbd-103">Creates a new Azure Firewall Policy Intrusion Detection Bypass Traffic Setting</span></span>

## <span data-ttu-id="0dbbd-104">語法</span><span class="sxs-lookup"><span data-stu-id="0dbbd-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name <String> [-Description <String>] -Protocol <String>
 [-SourceAddress <String[]>] [-DestinationAddress <String[]>] [-SourceIpGroup <String[]>]
 [-DestinationIpGroup <String[]>] -DestinationPort <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dbbd-105">描述</span><span class="sxs-lookup"><span data-stu-id="0dbbd-105">DESCRIPTION</span></span>
<span data-ttu-id="0dbbd-106">**New-AzFirewallPolicyIntrusionDetectionBypassTraffic** Cmdlet 會建立 Azure 防火牆策略入侵偵測忽略流量物件。</span><span class="sxs-lookup"><span data-stu-id="0dbbd-106">The **New-AzFirewallPolicyIntrusionDetectionBypassTraffic** cmdlet creates an Azure Firewall Policy Intrusion Detection Bypass Traffic Object.</span></span>

## <span data-ttu-id="0dbbd-107">例子</span><span class="sxs-lookup"><span data-stu-id="0dbbd-107">EXAMPLES</span></span>

### <span data-ttu-id="0dbbd-108">範例 1：1。</span><span class="sxs-lookup"><span data-stu-id="0dbbd-108">Example 1: 1.</span></span> <span data-ttu-id="0dbbd-109">使用特定埠和來源位址建立旁路流量</span><span class="sxs-lookup"><span data-stu-id="0dbbd-109">Create bypass traffic with specific port and source address</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress "*"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Deny" -BypassTraffic $bypass
```

<span data-ttu-id="0dbbd-110">此範例使用旁路流量設定建立入侵偵測</span><span class="sxs-lookup"><span data-stu-id="0dbbd-110">This example creates intrusion detection with bypass traffic setting</span></span>

## <span data-ttu-id="0dbbd-111">參數</span><span class="sxs-lookup"><span data-stu-id="0dbbd-111">PARAMETERS</span></span>

### <span data-ttu-id="0dbbd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dbbd-112">-DefaultProfile</span></span>
<span data-ttu-id="0dbbd-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0dbbd-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dbbd-114">-描述</span><span class="sxs-lookup"><span data-stu-id="0dbbd-114">-Description</span></span>
<span data-ttu-id="0dbbd-115">忽略設定描述。</span><span class="sxs-lookup"><span data-stu-id="0dbbd-115">Bypass setting description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dbbd-116">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="0dbbd-116">-DestinationAddress</span></span>
<span data-ttu-id="0dbbd-117">目的地 IP 位址或範圍的清單。</span><span class="sxs-lookup"><span data-stu-id="0dbbd-117">List of destination IP addresses or ranges.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dbbd-118">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="0dbbd-118">-DestinationIpGroup</span></span>
<span data-ttu-id="0dbbd-119">目的地 IpGroups 清單。</span><span class="sxs-lookup"><span data-stu-id="0dbbd-119">List of destination IpGroups.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dbbd-120">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="0dbbd-120">-DestinationPort</span></span>
<span data-ttu-id="0dbbd-121">目的地埠或範圍的清單。</span><span class="sxs-lookup"><span data-stu-id="0dbbd-121">List of destination ports or ranges.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dbbd-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="0dbbd-122">-Name</span></span>
<span data-ttu-id="0dbbd-123">忽略設定名稱。</span><span class="sxs-lookup"><span data-stu-id="0dbbd-123">Bypass setting name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dbbd-124">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="0dbbd-124">-Protocol</span></span>
<span data-ttu-id="0dbbd-125">忽略設定通訊協定。</span><span class="sxs-lookup"><span data-stu-id="0dbbd-125">Bypass setting protocol.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: TCP, UDP, ICMP, ANY

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dbbd-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="0dbbd-126">-SourceAddress</span></span>
<span data-ttu-id="0dbbd-127">來源 IP 位址或範圍清單。</span><span class="sxs-lookup"><span data-stu-id="0dbbd-127">List of source IP addresses or ranges.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dbbd-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="0dbbd-128">-SourceIpGroup</span></span>
<span data-ttu-id="0dbbd-129">來源 IpGroups 清單。</span><span class="sxs-lookup"><span data-stu-id="0dbbd-129">List of source IpGroups.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dbbd-130">-確認</span><span class="sxs-lookup"><span data-stu-id="0dbbd-130">-Confirm</span></span>
<span data-ttu-id="0dbbd-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0dbbd-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dbbd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dbbd-132">-WhatIf</span></span>
<span data-ttu-id="0dbbd-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0dbbd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0dbbd-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0dbbd-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dbbd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dbbd-135">CommonParameters</span></span>
<span data-ttu-id="0dbbd-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0dbbd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dbbd-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0dbbd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dbbd-138">輸入</span><span class="sxs-lookup"><span data-stu-id="0dbbd-138">INPUTS</span></span>

### <span data-ttu-id="0dbbd-139">沒有</span><span class="sxs-lookup"><span data-stu-id="0dbbd-139">None</span></span>

## <span data-ttu-id="0dbbd-140">輸出</span><span class="sxs-lookup"><span data-stu-id="0dbbd-140">OUTPUTS</span></span>

### <span data-ttu-id="0dbbd-141">Microsoft.Azure.Commands.Network.models.PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting</span><span class="sxs-lookup"><span data-stu-id="0dbbd-141">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting</span></span>

## <span data-ttu-id="0dbbd-142">筆記</span><span class="sxs-lookup"><span data-stu-id="0dbbd-142">NOTES</span></span>

## <span data-ttu-id="0dbbd-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="0dbbd-143">RELATED LINKS</span></span>
