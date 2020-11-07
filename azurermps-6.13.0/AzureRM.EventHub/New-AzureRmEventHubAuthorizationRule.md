---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 63da2be82f8af6339a68eab580c6871b05f2d884
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625577"
---
# <span data-ttu-id="59647-101">New-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="59647-101">New-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="59647-102">摘要</span><span class="sxs-lookup"><span data-stu-id="59647-102">SYNOPSIS</span></span>
<span data-ttu-id="59647-103">為 namespace 或 eventhub 建立新的事件中心授權規則。</span><span class="sxs-lookup"><span data-stu-id="59647-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59647-104">句法</span><span class="sxs-lookup"><span data-stu-id="59647-104">SYNTAX</span></span>

### <span data-ttu-id="59647-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="59647-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59647-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="59647-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59647-107">說明</span><span class="sxs-lookup"><span data-stu-id="59647-107">DESCRIPTION</span></span>
<span data-ttu-id="59647-108">New-AzureRmEventHubAuthorizationRule Cmdlet 會建立新的事件中樞授權規則。</span><span class="sxs-lookup"><span data-stu-id="59647-108">The New-AzureRmEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="59647-109">示例</span><span class="sxs-lookup"><span data-stu-id="59647-109">EXAMPLES</span></span>

### <span data-ttu-id="59647-110">範例1</span><span class="sxs-lookup"><span data-stu-id="59647-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="59647-111">\` \` \` \` 使用資源群組 MyResourceGroupName，建立授權規則 MyAuthRuleName，將偵聽和傳送許可權授予命名空間 \` MyNamespaceName \` 。</span><span class="sxs-lookup"><span data-stu-id="59647-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="59647-112">範例2</span><span class="sxs-lookup"><span data-stu-id="59647-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="59647-113">\` \` \` \` 在 \` \` 使用資源群組 MyResourceGroupName 的命名空間 MyNamespaceName 中，建立 \` MyAuthRuleName 的偵聽和傳送權利給事件中心 MyEventHubName 的 \` 授權規則。</span><span class="sxs-lookup"><span data-stu-id="59647-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="59647-114">參數</span><span class="sxs-lookup"><span data-stu-id="59647-114">PARAMETERS</span></span>

### <span data-ttu-id="59647-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59647-115">-DefaultProfile</span></span>
<span data-ttu-id="59647-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="59647-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59647-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="59647-117">-EventHub</span></span>
<span data-ttu-id="59647-118">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="59647-118">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59647-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="59647-119">-Name</span></span>
<span data-ttu-id="59647-120">AuthorizationRule 名稱</span><span class="sxs-lookup"><span data-stu-id="59647-120">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59647-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="59647-121">-Namespace</span></span>
<span data-ttu-id="59647-122">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="59647-122">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59647-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59647-123">-ResourceGroupName</span></span>
<span data-ttu-id="59647-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="59647-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59647-125">-許可權</span><span class="sxs-lookup"><span data-stu-id="59647-125">-Rights</span></span>
<span data-ttu-id="59647-126">權力，例如「聆聽」、「傳送」、「管理」</span><span class="sxs-lookup"><span data-stu-id="59647-126">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59647-127">-確認</span><span class="sxs-lookup"><span data-stu-id="59647-127">-Confirm</span></span>
<span data-ttu-id="59647-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="59647-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59647-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59647-129">-WhatIf</span></span>
<span data-ttu-id="59647-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="59647-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59647-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="59647-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59647-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59647-132">CommonParameters</span></span>
<span data-ttu-id="59647-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="59647-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59647-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="59647-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59647-135">輸入</span><span class="sxs-lookup"><span data-stu-id="59647-135">INPUTS</span></span>

### <span data-ttu-id="59647-136">System.object</span><span class="sxs-lookup"><span data-stu-id="59647-136">System.String</span></span>

### <span data-ttu-id="59647-137">System.object []</span><span class="sxs-lookup"><span data-stu-id="59647-137">System.String[]</span></span>

## <span data-ttu-id="59647-138">輸出</span><span class="sxs-lookup"><span data-stu-id="59647-138">OUTPUTS</span></span>

### <span data-ttu-id="59647-139">PSSharedAccessAuthorizationRuleAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="59647-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="59647-140">筆記</span><span class="sxs-lookup"><span data-stu-id="59647-140">NOTES</span></span>

## <span data-ttu-id="59647-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="59647-141">RELATED LINKS</span></span>
