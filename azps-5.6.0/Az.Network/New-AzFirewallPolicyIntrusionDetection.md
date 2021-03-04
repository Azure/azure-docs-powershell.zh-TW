---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicyintrusiondetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetection.md
ms.openlocfilehash: 3587917e1a4216445e59b182ce6307c7a94684bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913478"
---
# <span data-ttu-id="1dbe2-101">New-AzFirewallPolicyIntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="1dbe2-101">New-AzFirewallPolicyIntrusionDetection</span></span>

## <span data-ttu-id="1dbe2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1dbe2-102">SYNOPSIS</span></span>
<span data-ttu-id="1dbe2-103">建立新 Azure 防火牆策略入侵偵測，以與防火牆策略建立關聯</span><span class="sxs-lookup"><span data-stu-id="1dbe2-103">Creates a new Azure Firewall Policy Intrusion Detection to associate with Firewall Policy</span></span>

## <span data-ttu-id="1dbe2-104">語法</span><span class="sxs-lookup"><span data-stu-id="1dbe2-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetection -Mode <String>
 [-SignatureOverride <PSAzureFirewallPolicyIntrusionDetectionSignatureOverride[]>]
 [-BypassTraffic <PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dbe2-105">描述</span><span class="sxs-lookup"><span data-stu-id="1dbe2-105">DESCRIPTION</span></span>
<span data-ttu-id="1dbe2-106">**New-AzFirewallPolicyIntrusionDetection** Cmdlet 會建立 Azure 防火牆策略入侵偵測物件。</span><span class="sxs-lookup"><span data-stu-id="1dbe2-106">The **New-AzFirewallPolicyIntrusionDetection** cmdlet creates an Azure Firewall Policy Intrusion Detection Object.</span></span>

## <span data-ttu-id="1dbe2-107">例子</span><span class="sxs-lookup"><span data-stu-id="1dbe2-107">EXAMPLES</span></span>

### <span data-ttu-id="1dbe2-108">範例 1：1。</span><span class="sxs-lookup"><span data-stu-id="1dbe2-108">Example 1: 1.</span></span> <span data-ttu-id="1dbe2-109">使用模式建立入侵偵測</span><span class="sxs-lookup"><span data-stu-id="1dbe2-109">Create intrusion detection with mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert"
```

<span data-ttu-id="1dbe2-110">此範例使用警示和偵測模式 (入侵) 偵測</span><span class="sxs-lookup"><span data-stu-id="1dbe2-110">This example creates intrusion detection with Alert (detection) mode</span></span>

### <span data-ttu-id="1dbe2-111">範例 2：2。</span><span class="sxs-lookup"><span data-stu-id="1dbe2-111">Example 2: 2.</span></span> <span data-ttu-id="1dbe2-112">使用簽章覆蓋建立入侵偵測</span><span class="sxs-lookup"><span data-stu-id="1dbe2-112">Create intrusion detection with signature overrides</span></span>
```powershell
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride
```

<span data-ttu-id="1dbe2-113">此範例會建立具有特定簽章的入侵偵測</span><span class="sxs-lookup"><span data-stu-id="1dbe2-113">This example creates intrusion detection with specific signature override</span></span>

### <span data-ttu-id="1dbe2-114">範例 3：3。</span><span class="sxs-lookup"><span data-stu-id="1dbe2-114">Example 3: 3.</span></span> <span data-ttu-id="1dbe2-115">使用旁路流量設定設定入侵偵測來建立防火牆策略</span><span class="sxs-lookup"><span data-stu-id="1dbe2-115">Create firewall policy with intrusion detection configured with bypass traffic setting</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress "10.0.0.0"
PS C:\> $intrusionDetection = New-AzFirewallPolicyIntrusionDetection -Mode "Deny" -BypassTraffic $bypass
PS C:\> New-AzFirewallPolicy -Name fp1 -Location "westus2" -ResourceGroup TestRg -SkuTier "Premium" -IntrusionDetection $intrusionDetection
```

<span data-ttu-id="1dbe2-116">此範例使用旁路流量設定建立入侵偵測</span><span class="sxs-lookup"><span data-stu-id="1dbe2-116">This example creates intrusion detection with bypass traffic setting</span></span>

## <span data-ttu-id="1dbe2-117">參數</span><span class="sxs-lookup"><span data-stu-id="1dbe2-117">PARAMETERS</span></span>

### <span data-ttu-id="1dbe2-118">-BypassTraffic</span><span class="sxs-lookup"><span data-stu-id="1dbe2-118">-BypassTraffic</span></span>
<span data-ttu-id="1dbe2-119">要忽略的流量規則清單。</span><span class="sxs-lookup"><span data-stu-id="1dbe2-119">List of rules for traffic to bypass.</span></span>

```yaml
Type: PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dbe2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dbe2-120">-DefaultProfile</span></span>
<span data-ttu-id="1dbe2-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1dbe2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dbe2-122">-模式</span><span class="sxs-lookup"><span data-stu-id="1dbe2-122">-Mode</span></span>
<span data-ttu-id="1dbe2-123">入侵偵測一般狀態。</span><span class="sxs-lookup"><span data-stu-id="1dbe2-123">Intrusion Detection general state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Off, Alert, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dbe2-124">-SignatureOverride</span><span class="sxs-lookup"><span data-stu-id="1dbe2-124">-SignatureOverride</span></span>
<span data-ttu-id="1dbe2-125">特定簽章狀態清單。</span><span class="sxs-lookup"><span data-stu-id="1dbe2-125">List of specific signatures states.</span></span>

```yaml
Type: PSAzureFirewallPolicyIntrusionDetectionSignatureOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dbe2-126">-確認</span><span class="sxs-lookup"><span data-stu-id="1dbe2-126">-Confirm</span></span>
<span data-ttu-id="1dbe2-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1dbe2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dbe2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dbe2-128">-WhatIf</span></span>
<span data-ttu-id="1dbe2-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1dbe2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dbe2-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1dbe2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dbe2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dbe2-131">CommonParameters</span></span>
<span data-ttu-id="1dbe2-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1dbe2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dbe2-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1dbe2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dbe2-134">輸入</span><span class="sxs-lookup"><span data-stu-id="1dbe2-134">INPUTS</span></span>

### <span data-ttu-id="1dbe2-135">沒有</span><span class="sxs-lookup"><span data-stu-id="1dbe2-135">None</span></span>

## <span data-ttu-id="1dbe2-136">輸出</span><span class="sxs-lookup"><span data-stu-id="1dbe2-136">OUTPUTS</span></span>

### <span data-ttu-id="1dbe2-137">Microsoft.Azure.Commands.Network.models.PSAzureFirewallPolicyIntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="1dbe2-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetection</span></span>

## <span data-ttu-id="1dbe2-138">筆記</span><span class="sxs-lookup"><span data-stu-id="1dbe2-138">NOTES</span></span>

## <span data-ttu-id="1dbe2-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="1dbe2-139">RELATED LINKS</span></span>
