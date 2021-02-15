---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyintrusiondetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetection.md
ms.openlocfilehash: bc3c71c8900be049dce7b00b698068e96ccc8519
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131258"
---
# <span data-ttu-id="2455f-101">New-AzFirewallPolicyIntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="2455f-101">New-AzFirewallPolicyIntrusionDetection</span></span>

## <span data-ttu-id="2455f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2455f-102">SYNOPSIS</span></span>
<span data-ttu-id="2455f-103">建立新的 Azure 防火牆原則入侵偵測以與防火牆原則建立關聯</span><span class="sxs-lookup"><span data-stu-id="2455f-103">Creates a new Azure Firewall Policy Intrusion Detection to associate with Firewall Policy</span></span>

## <span data-ttu-id="2455f-104">句法</span><span class="sxs-lookup"><span data-stu-id="2455f-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetection -Mode <String>
 [-SignatureOverride <PSAzureFirewallPolicyIntrusionDetectionSignatureOverride[]>]
 [-BypassTraffic <PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2455f-105">說明</span><span class="sxs-lookup"><span data-stu-id="2455f-105">DESCRIPTION</span></span>
<span data-ttu-id="2455f-106">**新的-AzFirewallPolicyIntrusionDetection** Cmdlet 會建立 Azure 防火牆原則入侵偵測物件。</span><span class="sxs-lookup"><span data-stu-id="2455f-106">The **New-AzFirewallPolicyIntrusionDetection** cmdlet creates an Azure Firewall Policy Intrusion Detection Object.</span></span>

## <span data-ttu-id="2455f-107">示例</span><span class="sxs-lookup"><span data-stu-id="2455f-107">EXAMPLES</span></span>

### <span data-ttu-id="2455f-108">範例 1: 1。</span><span class="sxs-lookup"><span data-stu-id="2455f-108">Example 1: 1.</span></span> <span data-ttu-id="2455f-109">使用模式建立入侵偵測</span><span class="sxs-lookup"><span data-stu-id="2455f-109">Create intrusion detection with mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert"
```

<span data-ttu-id="2455f-110">這個範例會使用警示 (偵測) 模式來建立入侵偵測</span><span class="sxs-lookup"><span data-stu-id="2455f-110">This example creates intrusion detection with Alert (detection) mode</span></span>

### <span data-ttu-id="2455f-111">範例 2: 2。</span><span class="sxs-lookup"><span data-stu-id="2455f-111">Example 2: 2.</span></span> <span data-ttu-id="2455f-112">使用簽名覆蓋來建立入侵偵測</span><span class="sxs-lookup"><span data-stu-id="2455f-112">Create intrusion detection with signature overrides</span></span>
```powershell
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride
```

<span data-ttu-id="2455f-113">這個範例會使用特定的簽名覆蓋來建立入侵偵測</span><span class="sxs-lookup"><span data-stu-id="2455f-113">This example creates intrusion detection with specific signature override</span></span>

### <span data-ttu-id="2455f-114">範例 3: 3。</span><span class="sxs-lookup"><span data-stu-id="2455f-114">Example 3: 3.</span></span> <span data-ttu-id="2455f-115">使用設定了 [略過流量] 設定的入侵偵測建立防火牆原則</span><span class="sxs-lookup"><span data-stu-id="2455f-115">Create firewall policy with intrusion detection configured with bypass traffic setting</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress "10.0.0.0"
PS C:\> $intrusionDetection = New-AzFirewallPolicyIntrusionDetection -Mode "Deny" -BypassTraffic $bypass
PS C:\> New-AzFirewallPolicy -Name fp1 -Location "westus2" -ResourceGroup TestRg -SkuTier "Premium" -IntrusionDetection $intrusionDetection
```

<span data-ttu-id="2455f-116">這個範例會使用 [旁路流量] 設定來建立入侵偵測</span><span class="sxs-lookup"><span data-stu-id="2455f-116">This example creates intrusion detection with bypass traffic setting</span></span>

## <span data-ttu-id="2455f-117">參數</span><span class="sxs-lookup"><span data-stu-id="2455f-117">PARAMETERS</span></span>

### <span data-ttu-id="2455f-118">-BypassTraffic</span><span class="sxs-lookup"><span data-stu-id="2455f-118">-BypassTraffic</span></span>
<span data-ttu-id="2455f-119">要繞過之通信量的規則清單。</span><span class="sxs-lookup"><span data-stu-id="2455f-119">List of rules for traffic to bypass.</span></span>

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

### <span data-ttu-id="2455f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2455f-120">-DefaultProfile</span></span>
<span data-ttu-id="2455f-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2455f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2455f-122">模式</span><span class="sxs-lookup"><span data-stu-id="2455f-122">-Mode</span></span>
<span data-ttu-id="2455f-123">入侵偵測一般狀態。</span><span class="sxs-lookup"><span data-stu-id="2455f-123">Intrusion Detection general state.</span></span>

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

### <span data-ttu-id="2455f-124">-SignatureOverride</span><span class="sxs-lookup"><span data-stu-id="2455f-124">-SignatureOverride</span></span>
<span data-ttu-id="2455f-125">特定簽章狀態的清單。</span><span class="sxs-lookup"><span data-stu-id="2455f-125">List of specific signatures states.</span></span>

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

### <span data-ttu-id="2455f-126">-確認</span><span class="sxs-lookup"><span data-stu-id="2455f-126">-Confirm</span></span>
<span data-ttu-id="2455f-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2455f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2455f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2455f-128">-WhatIf</span></span>
<span data-ttu-id="2455f-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2455f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2455f-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2455f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2455f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2455f-131">CommonParameters</span></span>
<span data-ttu-id="2455f-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2455f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2455f-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2455f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2455f-134">輸入</span><span class="sxs-lookup"><span data-stu-id="2455f-134">INPUTS</span></span>

### <span data-ttu-id="2455f-135">所有</span><span class="sxs-lookup"><span data-stu-id="2455f-135">None</span></span>

## <span data-ttu-id="2455f-136">輸出</span><span class="sxs-lookup"><span data-stu-id="2455f-136">OUTPUTS</span></span>

### <span data-ttu-id="2455f-137">PSAzureFirewallPolicyIntrusionDetection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2455f-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetection</span></span>

## <span data-ttu-id="2455f-138">筆記</span><span class="sxs-lookup"><span data-stu-id="2455f-138">NOTES</span></span>

## <span data-ttu-id="2455f-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="2455f-139">RELATED LINKS</span></span>
