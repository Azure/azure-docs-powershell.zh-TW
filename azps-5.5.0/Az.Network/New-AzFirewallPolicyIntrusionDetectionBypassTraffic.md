---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyintrusiondetectionbypasstraffic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionBypassTraffic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionBypassTraffic.md
ms.openlocfilehash: c296c44c96d756dc0ca3a107d8eee265a9226b15
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131255"
---
# <span data-ttu-id="80a9e-101">New-AzFirewallPolicyIntrusionDetectionBypassTraffic</span><span class="sxs-lookup"><span data-stu-id="80a9e-101">New-AzFirewallPolicyIntrusionDetectionBypassTraffic</span></span>

## <span data-ttu-id="80a9e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="80a9e-102">SYNOPSIS</span></span>
<span data-ttu-id="80a9e-103">建立新的 Azure 防火牆原則入侵偵測旁路流量設定</span><span class="sxs-lookup"><span data-stu-id="80a9e-103">Creates a new Azure Firewall Policy Intrusion Detection Bypass Traffic Setting</span></span>

## <span data-ttu-id="80a9e-104">句法</span><span class="sxs-lookup"><span data-stu-id="80a9e-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name <String> [-Description <String>] -Protocol <String>
 [-SourceAddress <String[]>] [-DestinationAddress <String[]>] [-SourceIpGroup <String[]>]
 [-DestinationIpGroup <String[]>] -DestinationPort <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80a9e-105">說明</span><span class="sxs-lookup"><span data-stu-id="80a9e-105">DESCRIPTION</span></span>
<span data-ttu-id="80a9e-106">**新的-AzFirewallPolicyIntrusionDetectionBypassTraffic** Cmdlet 會建立 Azure 防火牆原則入侵偵測旁路流量物件。</span><span class="sxs-lookup"><span data-stu-id="80a9e-106">The **New-AzFirewallPolicyIntrusionDetectionBypassTraffic** cmdlet creates an Azure Firewall Policy Intrusion Detection Bypass Traffic Object.</span></span>

## <span data-ttu-id="80a9e-107">示例</span><span class="sxs-lookup"><span data-stu-id="80a9e-107">EXAMPLES</span></span>

### <span data-ttu-id="80a9e-108">範例 1: 1。</span><span class="sxs-lookup"><span data-stu-id="80a9e-108">Example 1: 1.</span></span> <span data-ttu-id="80a9e-109">建立具有特定埠和來源位址的旁路流量</span><span class="sxs-lookup"><span data-stu-id="80a9e-109">Create bypass traffic with specific port and source address</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress "*"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Deny" -BypassTraffic $bypass
```

<span data-ttu-id="80a9e-110">這個範例會使用 [旁路流量] 設定來建立入侵偵測</span><span class="sxs-lookup"><span data-stu-id="80a9e-110">This example creates intrusion detection with bypass traffic setting</span></span>

## <span data-ttu-id="80a9e-111">參數</span><span class="sxs-lookup"><span data-stu-id="80a9e-111">PARAMETERS</span></span>

### <span data-ttu-id="80a9e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80a9e-112">-DefaultProfile</span></span>
<span data-ttu-id="80a9e-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="80a9e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80a9e-114">-描述</span><span class="sxs-lookup"><span data-stu-id="80a9e-114">-Description</span></span>
<span data-ttu-id="80a9e-115">繞過設定描述。</span><span class="sxs-lookup"><span data-stu-id="80a9e-115">Bypass setting description.</span></span>

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

### <span data-ttu-id="80a9e-116">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="80a9e-116">-DestinationAddress</span></span>
<span data-ttu-id="80a9e-117">目的地 IP 位址或範圍的清單。</span><span class="sxs-lookup"><span data-stu-id="80a9e-117">List of destination IP addresses or ranges.</span></span>

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

### <span data-ttu-id="80a9e-118">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="80a9e-118">-DestinationIpGroup</span></span>
<span data-ttu-id="80a9e-119">目的地 IpGroups 清單。</span><span class="sxs-lookup"><span data-stu-id="80a9e-119">List of destination IpGroups.</span></span>

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

### <span data-ttu-id="80a9e-120">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="80a9e-120">-DestinationPort</span></span>
<span data-ttu-id="80a9e-121">[目的地埠] 或 [範圍] 清單。</span><span class="sxs-lookup"><span data-stu-id="80a9e-121">List of destination ports or ranges.</span></span>

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

### <span data-ttu-id="80a9e-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="80a9e-122">-Name</span></span>
<span data-ttu-id="80a9e-123">略過設定名稱。</span><span class="sxs-lookup"><span data-stu-id="80a9e-123">Bypass setting name.</span></span>

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

### <span data-ttu-id="80a9e-124">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="80a9e-124">-Protocol</span></span>
<span data-ttu-id="80a9e-125">略過設定通訊協定。</span><span class="sxs-lookup"><span data-stu-id="80a9e-125">Bypass setting protocol.</span></span>

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

### <span data-ttu-id="80a9e-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="80a9e-126">-SourceAddress</span></span>
<span data-ttu-id="80a9e-127">來源 IP 位址或範圍的清單。</span><span class="sxs-lookup"><span data-stu-id="80a9e-127">List of source IP addresses or ranges.</span></span>

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

### <span data-ttu-id="80a9e-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="80a9e-128">-SourceIpGroup</span></span>
<span data-ttu-id="80a9e-129">來源 IpGroups 清單。</span><span class="sxs-lookup"><span data-stu-id="80a9e-129">List of source IpGroups.</span></span>

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

### <span data-ttu-id="80a9e-130">-確認</span><span class="sxs-lookup"><span data-stu-id="80a9e-130">-Confirm</span></span>
<span data-ttu-id="80a9e-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="80a9e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80a9e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80a9e-132">-WhatIf</span></span>
<span data-ttu-id="80a9e-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="80a9e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80a9e-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80a9e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80a9e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80a9e-135">CommonParameters</span></span>
<span data-ttu-id="80a9e-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="80a9e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80a9e-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="80a9e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80a9e-138">輸入</span><span class="sxs-lookup"><span data-stu-id="80a9e-138">INPUTS</span></span>

### <span data-ttu-id="80a9e-139">所有</span><span class="sxs-lookup"><span data-stu-id="80a9e-139">None</span></span>

## <span data-ttu-id="80a9e-140">輸出</span><span class="sxs-lookup"><span data-stu-id="80a9e-140">OUTPUTS</span></span>

### <span data-ttu-id="80a9e-141">PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="80a9e-141">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting</span></span>

## <span data-ttu-id="80a9e-142">筆記</span><span class="sxs-lookup"><span data-stu-id="80a9e-142">NOTES</span></span>

## <span data-ttu-id="80a9e-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="80a9e-143">RELATED LINKS</span></span>
