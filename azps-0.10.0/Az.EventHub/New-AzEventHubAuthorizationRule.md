---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
ms.openlocfilehash: c59a58e458ceed2c183978a8839de1cd864ffaa7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794766"
---
# <span data-ttu-id="c2a0f-101">New-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c2a0f-101">New-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="c2a0f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2a0f-102">SYNOPSIS</span></span>
<span data-ttu-id="c2a0f-103">為 namespace 或 eventhub 建立新的事件中心授權規則。</span><span class="sxs-lookup"><span data-stu-id="c2a0f-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

## <span data-ttu-id="c2a0f-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2a0f-104">SYNTAX</span></span>

### <span data-ttu-id="c2a0f-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c2a0f-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2a0f-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c2a0f-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2a0f-107">說明</span><span class="sxs-lookup"><span data-stu-id="c2a0f-107">DESCRIPTION</span></span>
<span data-ttu-id="c2a0f-108">New-AzEventHubAuthorizationRule Cmdlet 會建立新的事件中樞授權規則。</span><span class="sxs-lookup"><span data-stu-id="c2a0f-108">The New-AzEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="c2a0f-109">示例</span><span class="sxs-lookup"><span data-stu-id="c2a0f-109">EXAMPLES</span></span>

### <span data-ttu-id="c2a0f-110">範例1</span><span class="sxs-lookup"><span data-stu-id="c2a0f-110">Example 1</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="c2a0f-111">\` \` \` \` 使用資源群組 MyResourceGroupName，建立授權規則 MyAuthRuleName，將偵聽和傳送許可權授予命名空間 \` MyNamespaceName \` 。</span><span class="sxs-lookup"><span data-stu-id="c2a0f-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c2a0f-112">範例2</span><span class="sxs-lookup"><span data-stu-id="c2a0f-112">Example 2</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="c2a0f-113">\` \` \` \` 在 \` \` 使用資源群組 MyResourceGroupName 的命名空間 MyNamespaceName 中，建立 \` MyAuthRuleName 的偵聽和傳送權利給事件中心 MyEventHubName 的 \` 授權規則。</span><span class="sxs-lookup"><span data-stu-id="c2a0f-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="c2a0f-114">參數</span><span class="sxs-lookup"><span data-stu-id="c2a0f-114">PARAMETERS</span></span>

### <span data-ttu-id="c2a0f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2a0f-115">-DefaultProfile</span></span>
<span data-ttu-id="c2a0f-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c2a0f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2a0f-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="c2a0f-117">-EventHub</span></span>
<span data-ttu-id="c2a0f-118">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="c2a0f-118">EventHub Name</span></span>

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

### <span data-ttu-id="c2a0f-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="c2a0f-119">-Name</span></span>
<span data-ttu-id="c2a0f-120">AuthorizationRule 名稱</span><span class="sxs-lookup"><span data-stu-id="c2a0f-120">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="c2a0f-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="c2a0f-121">-Namespace</span></span>
<span data-ttu-id="c2a0f-122">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="c2a0f-122">Namespace Name</span></span>

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

### <span data-ttu-id="c2a0f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2a0f-123">-ResourceGroupName</span></span>
<span data-ttu-id="c2a0f-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="c2a0f-124">Resource Group Name</span></span>

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

### <span data-ttu-id="c2a0f-125">-許可權</span><span class="sxs-lookup"><span data-stu-id="c2a0f-125">-Rights</span></span>
<span data-ttu-id="c2a0f-126">權力，例如「聆聽」、「傳送」、「管理」</span><span class="sxs-lookup"><span data-stu-id="c2a0f-126">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="c2a0f-127">-確認</span><span class="sxs-lookup"><span data-stu-id="c2a0f-127">-Confirm</span></span>
<span data-ttu-id="c2a0f-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c2a0f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2a0f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2a0f-129">-WhatIf</span></span>
<span data-ttu-id="c2a0f-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c2a0f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2a0f-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2a0f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2a0f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2a0f-132">CommonParameters</span></span>
<span data-ttu-id="c2a0f-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2a0f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2a0f-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c2a0f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2a0f-135">輸入</span><span class="sxs-lookup"><span data-stu-id="c2a0f-135">INPUTS</span></span>

### <span data-ttu-id="c2a0f-136">System.object</span><span class="sxs-lookup"><span data-stu-id="c2a0f-136">System.String</span></span>

### <span data-ttu-id="c2a0f-137">System.object []</span><span class="sxs-lookup"><span data-stu-id="c2a0f-137">System.String[]</span></span>

## <span data-ttu-id="c2a0f-138">輸出</span><span class="sxs-lookup"><span data-stu-id="c2a0f-138">OUTPUTS</span></span>

### <span data-ttu-id="c2a0f-139">PSSharedAccessAuthorizationRuleAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="c2a0f-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="c2a0f-140">筆記</span><span class="sxs-lookup"><span data-stu-id="c2a0f-140">NOTES</span></span>

## <span data-ttu-id="c2a0f-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2a0f-141">RELATED LINKS</span></span>
