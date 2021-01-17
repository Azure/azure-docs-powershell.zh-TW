---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 91c38686d8621f3bba521d738cc125e4b8473188
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438480"
---
# <span data-ttu-id="43c2b-101">Remove-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="43c2b-101">Remove-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="43c2b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43c2b-102">SYNOPSIS</span></span>
<span data-ttu-id="43c2b-103">移除指定的事件中心授權規則。</span><span class="sxs-lookup"><span data-stu-id="43c2b-103">Removes the specified Event Hub authorization rule.</span></span>

## <span data-ttu-id="43c2b-104">句法</span><span class="sxs-lookup"><span data-stu-id="43c2b-104">SYNTAX</span></span>

### <span data-ttu-id="43c2b-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="43c2b-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43c2b-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="43c2b-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43c2b-107">說明</span><span class="sxs-lookup"><span data-stu-id="43c2b-107">DESCRIPTION</span></span>
<span data-ttu-id="43c2b-108">Remove-AzEventHubAuthorizationRule Cmdlet 會從指定的事件中樞中移除並刪除指定的授權規則。</span><span class="sxs-lookup"><span data-stu-id="43c2b-108">The Remove-AzEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="43c2b-109">示例</span><span class="sxs-lookup"><span data-stu-id="43c2b-109">EXAMPLES</span></span>

### <span data-ttu-id="43c2b-110">範例1</span><span class="sxs-lookup"><span data-stu-id="43c2b-110">Example 1</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="43c2b-111">\` \` 從命名空間 MyNamespaceName 移除授權規則 MyAuthRuleName \` \` 。</span><span class="sxs-lookup"><span data-stu-id="43c2b-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="43c2b-112">範例2</span><span class="sxs-lookup"><span data-stu-id="43c2b-112">Example 2</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="43c2b-113">\` \` 從事件中心 MyEventHubName 移除授權規則 MyAuthRuleName \` \` 。</span><span class="sxs-lookup"><span data-stu-id="43c2b-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="43c2b-114">參數</span><span class="sxs-lookup"><span data-stu-id="43c2b-114">PARAMETERS</span></span>

### <span data-ttu-id="43c2b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43c2b-115">-DefaultProfile</span></span>
<span data-ttu-id="43c2b-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="43c2b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43c2b-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="43c2b-117">-EventHub</span></span>
<span data-ttu-id="43c2b-118">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="43c2b-118">EventHub Name</span></span>

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

### <span data-ttu-id="43c2b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="43c2b-119">-Force</span></span>
<span data-ttu-id="43c2b-120">不要求確認</span><span class="sxs-lookup"><span data-stu-id="43c2b-120">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="43c2b-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="43c2b-121">-Name</span></span>
<span data-ttu-id="43c2b-122">AuthorizationRule 名稱</span><span class="sxs-lookup"><span data-stu-id="43c2b-122">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="43c2b-123">-命名空間</span><span class="sxs-lookup"><span data-stu-id="43c2b-123">-Namespace</span></span>
<span data-ttu-id="43c2b-124">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="43c2b-124">Namespace Name</span></span>

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

### <span data-ttu-id="43c2b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43c2b-125">-PassThru</span></span>
<span data-ttu-id="43c2b-126">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="43c2b-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="43c2b-127">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="43c2b-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="43c2b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43c2b-128">-ResourceGroupName</span></span>
<span data-ttu-id="43c2b-129">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="43c2b-129">Resource Group Name</span></span>

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

### <span data-ttu-id="43c2b-130">-確認</span><span class="sxs-lookup"><span data-stu-id="43c2b-130">-Confirm</span></span>
<span data-ttu-id="43c2b-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="43c2b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43c2b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43c2b-132">-WhatIf</span></span>
<span data-ttu-id="43c2b-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="43c2b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43c2b-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="43c2b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43c2b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43c2b-135">CommonParameters</span></span>
<span data-ttu-id="43c2b-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43c2b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43c2b-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="43c2b-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43c2b-138">輸入</span><span class="sxs-lookup"><span data-stu-id="43c2b-138">INPUTS</span></span>

### <span data-ttu-id="43c2b-139">System.object</span><span class="sxs-lookup"><span data-stu-id="43c2b-139">System.String</span></span>

## <span data-ttu-id="43c2b-140">輸出</span><span class="sxs-lookup"><span data-stu-id="43c2b-140">OUTPUTS</span></span>

### <span data-ttu-id="43c2b-141">System.object</span><span class="sxs-lookup"><span data-stu-id="43c2b-141">System.Boolean</span></span>

## <span data-ttu-id="43c2b-142">筆記</span><span class="sxs-lookup"><span data-stu-id="43c2b-142">NOTES</span></span>

## <span data-ttu-id="43c2b-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="43c2b-143">RELATED LINKS</span></span>
