---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmFirewall.md
ms.openlocfilehash: 8f2c2560ac8ca0787a8a0eb8d37fb5242f4a915e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443799"
---
# <span data-ttu-id="26dab-101">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="26dab-101">Set-AzureRmFirewall</span></span>

## <span data-ttu-id="26dab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="26dab-102">SYNOPSIS</span></span>
<span data-ttu-id="26dab-103">儲存已修改的防火牆。</span><span class="sxs-lookup"><span data-stu-id="26dab-103">Saves a modified Firewall.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26dab-104">句法</span><span class="sxs-lookup"><span data-stu-id="26dab-104">SYNTAX</span></span>

```
Set-AzureRmFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26dab-105">說明</span><span class="sxs-lookup"><span data-stu-id="26dab-105">DESCRIPTION</span></span>
<span data-ttu-id="26dab-106">**AzureRmFirewall** Cmdlet 會更新 Azure 防火牆。</span><span class="sxs-lookup"><span data-stu-id="26dab-106">The **Set-AzureRmFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="26dab-107">示例</span><span class="sxs-lookup"><span data-stu-id="26dab-107">EXAMPLES</span></span>

### <span data-ttu-id="26dab-108">1：更新防火牆應用程式規則集合的優先順序</span><span class="sxs-lookup"><span data-stu-id="26dab-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzureRmFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzureRmFirewall -Firewall $azFw
```

<span data-ttu-id="26dab-109">此範例更新現有的 Azure 防火牆規則集合的優先順序。</span><span class="sxs-lookup"><span data-stu-id="26dab-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="26dab-110">假設資源群組 "rg" 中的 Azure 防火牆「AzureFirewall」包含名為「ruleCollectionName」的應用程式規則集合，則上述命令將會變更該規則集合的優先順序，之後就會更新 Azure 防火牆。</span><span class="sxs-lookup"><span data-stu-id="26dab-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="26dab-111">如果沒有 Set-AzureRmFirewall 命令，在本機 $azFw 物件上執行的所有操作都會不會反映在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="26dab-111">Without the Set-AzureRmFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="26dab-112">2：建立 Azure 防火牆並稍後設定應用程式規則集合</span><span class="sxs-lookup"><span data-stu-id="26dab-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzureRmFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzureRmFirewall
```

<span data-ttu-id="26dab-113">在這個範例中，首先會建立不含任何應用程式規則集合的防火牆。</span><span class="sxs-lookup"><span data-stu-id="26dab-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="26dab-114">接著會建立應用程式規則和應用程式規則集合，然後在記憶體中修改 Firewall 物件，而不會影響雲端的實際設定。</span><span class="sxs-lookup"><span data-stu-id="26dab-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="26dab-115">若要在雲端反射的變更，必須呼叫 Set-AzureRmFirewall。</span><span class="sxs-lookup"><span data-stu-id="26dab-115">For changes to be reflected in cloud, Set-AzureRmFirewall must be called.</span></span>

## <span data-ttu-id="26dab-116">參數</span><span class="sxs-lookup"><span data-stu-id="26dab-116">PARAMETERS</span></span>

### <span data-ttu-id="26dab-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26dab-117">-AsJob</span></span>
<span data-ttu-id="26dab-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26dab-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26dab-119">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="26dab-119">-AzureFirewall</span></span>
<span data-ttu-id="26dab-120">AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="26dab-120">The AzureFirewall</span></span>

```yaml
Type: PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26dab-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26dab-121">-DefaultProfile</span></span>
<span data-ttu-id="26dab-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="26dab-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26dab-123">-確認</span><span class="sxs-lookup"><span data-stu-id="26dab-123">-Confirm</span></span>
<span data-ttu-id="26dab-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="26dab-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26dab-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26dab-125">-WhatIf</span></span>
<span data-ttu-id="26dab-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="26dab-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26dab-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26dab-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26dab-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26dab-128">CommonParameters</span></span>
<span data-ttu-id="26dab-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="26dab-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26dab-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="26dab-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26dab-131">輸入</span><span class="sxs-lookup"><span data-stu-id="26dab-131">INPUTS</span></span>

### <span data-ttu-id="26dab-132">PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="26dab-132">PSAzureFirewall</span></span>
<span data-ttu-id="26dab-133">形參 "AzureFirewall" 接受管線中 "PSAzureFirewall" 類型的值</span><span class="sxs-lookup"><span data-stu-id="26dab-133">Parameter 'AzureFirewall' accepts value of type 'PSAzureFirewall' from the pipeline</span></span>

## <span data-ttu-id="26dab-134">輸出</span><span class="sxs-lookup"><span data-stu-id="26dab-134">OUTPUTS</span></span>

### <span data-ttu-id="26dab-135">PSAzureFirewall 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="26dab-135">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="26dab-136">筆記</span><span class="sxs-lookup"><span data-stu-id="26dab-136">NOTES</span></span>

## <span data-ttu-id="26dab-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="26dab-137">RELATED LINKS</span></span>

[<span data-ttu-id="26dab-138">AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="26dab-138">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="26dab-139">新-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="26dab-139">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="26dab-140">移除-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="26dab-140">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)
