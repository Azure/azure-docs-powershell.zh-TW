---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 7937af38c7dd0becd57604a0a7c00e5d1f584e6c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621460"
---
# <span data-ttu-id="baf87-101">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="baf87-101">Set-AzFirewall</span></span>

## <span data-ttu-id="baf87-102">摘要</span><span class="sxs-lookup"><span data-stu-id="baf87-102">SYNOPSIS</span></span>
<span data-ttu-id="baf87-103">儲存已修改的防火牆。</span><span class="sxs-lookup"><span data-stu-id="baf87-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="baf87-104">句法</span><span class="sxs-lookup"><span data-stu-id="baf87-104">SYNTAX</span></span>

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="baf87-105">說明</span><span class="sxs-lookup"><span data-stu-id="baf87-105">DESCRIPTION</span></span>
<span data-ttu-id="baf87-106">**AzFirewall** Cmdlet 會更新 Azure 防火牆。</span><span class="sxs-lookup"><span data-stu-id="baf87-106">The **Set-AzFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="baf87-107">示例</span><span class="sxs-lookup"><span data-stu-id="baf87-107">EXAMPLES</span></span>

### <span data-ttu-id="baf87-108">1：更新防火牆應用程式規則集合的優先順序</span><span class="sxs-lookup"><span data-stu-id="baf87-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="baf87-109">此範例更新現有的 Azure 防火牆規則集合的優先順序。</span><span class="sxs-lookup"><span data-stu-id="baf87-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="baf87-110">假設資源群組 "rg" 中的 Azure 防火牆「AzureFirewall」包含名為「ruleCollectionName」的應用程式規則集合，則上述命令將會變更該規則集合的優先順序，之後就會更新 Azure 防火牆。</span><span class="sxs-lookup"><span data-stu-id="baf87-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="baf87-111">如果沒有 Set-AzFirewall 命令，在本機 $azFw 物件上執行的所有操作都會不會反映在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="baf87-111">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="baf87-112">2：建立 Azure 防火牆並稍後設定應用程式規則集合</span><span class="sxs-lookup"><span data-stu-id="baf87-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

<span data-ttu-id="baf87-113">在這個範例中，首先會建立不含任何應用程式規則集合的防火牆。</span><span class="sxs-lookup"><span data-stu-id="baf87-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="baf87-114">接著會建立應用程式規則和應用程式規則集合，然後在記憶體中修改 Firewall 物件，而不會影響雲端的實際設定。</span><span class="sxs-lookup"><span data-stu-id="baf87-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="baf87-115">若要在雲端反射的變更，必須呼叫 Set-AzFirewall。</span><span class="sxs-lookup"><span data-stu-id="baf87-115">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="baf87-116">3：更新 Microsoft Azure 防火牆的 [Intel 作業] 模式</span><span class="sxs-lookup"><span data-stu-id="baf87-116">3:  Update Threat Intel operation mode of Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

<span data-ttu-id="baf87-117">這個範例會更新資源群組 "rg" 中的 Azure 防火牆 "AzureFirewall" 的威脅 Intel 作業模式。</span><span class="sxs-lookup"><span data-stu-id="baf87-117">This example updates the Threat Intel operation mode of Azure Firewall "AzureFirewall" in resource group "rg".</span></span>
<span data-ttu-id="baf87-118">如果沒有 Set-AzFirewall 命令，在本機 $azFw 物件上執行的所有操作都會不會反映在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="baf87-118">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

## <span data-ttu-id="baf87-119">參數</span><span class="sxs-lookup"><span data-stu-id="baf87-119">PARAMETERS</span></span>

### <span data-ttu-id="baf87-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="baf87-120">-AsJob</span></span>
<span data-ttu-id="baf87-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="baf87-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="baf87-122">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="baf87-122">-AzureFirewall</span></span>
<span data-ttu-id="baf87-123">AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="baf87-123">The AzureFirewall</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="baf87-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baf87-124">-DefaultProfile</span></span>
<span data-ttu-id="baf87-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="baf87-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="baf87-126">-確認</span><span class="sxs-lookup"><span data-stu-id="baf87-126">-Confirm</span></span>
<span data-ttu-id="baf87-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="baf87-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="baf87-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baf87-128">-WhatIf</span></span>
<span data-ttu-id="baf87-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="baf87-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="baf87-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="baf87-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="baf87-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baf87-131">CommonParameters</span></span>
<span data-ttu-id="baf87-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="baf87-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baf87-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="baf87-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baf87-134">輸入</span><span class="sxs-lookup"><span data-stu-id="baf87-134">INPUTS</span></span>

### <span data-ttu-id="baf87-135">PSAzureFirewall 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="baf87-135">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="baf87-136">輸出</span><span class="sxs-lookup"><span data-stu-id="baf87-136">OUTPUTS</span></span>

### <span data-ttu-id="baf87-137">PSAzureFirewall 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="baf87-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="baf87-138">筆記</span><span class="sxs-lookup"><span data-stu-id="baf87-138">NOTES</span></span>

## <span data-ttu-id="baf87-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="baf87-139">RELATED LINKS</span></span>

[<span data-ttu-id="baf87-140">AzFirewall</span><span class="sxs-lookup"><span data-stu-id="baf87-140">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="baf87-141">新-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="baf87-141">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="baf87-142">移除-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="baf87-142">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)
