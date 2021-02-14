---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 91c38686d8621f3bba521d738cc125e4b8473188
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140899"
---
# <span data-ttu-id="f9f68-101">Remove-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f9f68-101">Remove-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="f9f68-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f9f68-102">SYNOPSIS</span></span>
<span data-ttu-id="f9f68-103">移除指定的事件中心授權規則。</span><span class="sxs-lookup"><span data-stu-id="f9f68-103">Removes the specified Event Hub authorization rule.</span></span>

## <span data-ttu-id="f9f68-104">句法</span><span class="sxs-lookup"><span data-stu-id="f9f68-104">SYNTAX</span></span>

### <span data-ttu-id="f9f68-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f9f68-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9f68-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9f68-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f9f68-107">說明</span><span class="sxs-lookup"><span data-stu-id="f9f68-107">DESCRIPTION</span></span>
<span data-ttu-id="f9f68-108">Remove-AzEventHubAuthorizationRule Cmdlet 會從指定的事件中樞中移除並刪除指定的授權規則。</span><span class="sxs-lookup"><span data-stu-id="f9f68-108">The Remove-AzEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="f9f68-109">示例</span><span class="sxs-lookup"><span data-stu-id="f9f68-109">EXAMPLES</span></span>

### <span data-ttu-id="f9f68-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f9f68-110">Example 1</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="f9f68-111">\` \` 從命名空間 MyNamespaceName 移除授權規則 MyAuthRuleName \` \` 。</span><span class="sxs-lookup"><span data-stu-id="f9f68-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="f9f68-112">範例2</span><span class="sxs-lookup"><span data-stu-id="f9f68-112">Example 2</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="f9f68-113">\` \` 從事件中心 MyEventHubName 移除授權規則 MyAuthRuleName \` \` 。</span><span class="sxs-lookup"><span data-stu-id="f9f68-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="f9f68-114">參數</span><span class="sxs-lookup"><span data-stu-id="f9f68-114">PARAMETERS</span></span>

### <span data-ttu-id="f9f68-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9f68-115">-DefaultProfile</span></span>
<span data-ttu-id="f9f68-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f9f68-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9f68-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="f9f68-117">-EventHub</span></span>
<span data-ttu-id="f9f68-118">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="f9f68-118">EventHub Name</span></span>

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

### <span data-ttu-id="f9f68-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f9f68-119">-Force</span></span>
<span data-ttu-id="f9f68-120">不要求確認</span><span class="sxs-lookup"><span data-stu-id="f9f68-120">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="f9f68-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="f9f68-121">-Name</span></span>
<span data-ttu-id="f9f68-122">AuthorizationRule 名稱</span><span class="sxs-lookup"><span data-stu-id="f9f68-122">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="f9f68-123">-命名空間</span><span class="sxs-lookup"><span data-stu-id="f9f68-123">-Namespace</span></span>
<span data-ttu-id="f9f68-124">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="f9f68-124">Namespace Name</span></span>

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

### <span data-ttu-id="f9f68-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9f68-125">-PassThru</span></span>
<span data-ttu-id="f9f68-126">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="f9f68-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f9f68-127">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="f9f68-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f9f68-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9f68-128">-ResourceGroupName</span></span>
<span data-ttu-id="f9f68-129">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="f9f68-129">Resource Group Name</span></span>

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

### <span data-ttu-id="f9f68-130">-確認</span><span class="sxs-lookup"><span data-stu-id="f9f68-130">-Confirm</span></span>
<span data-ttu-id="f9f68-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f9f68-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9f68-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9f68-132">-WhatIf</span></span>
<span data-ttu-id="f9f68-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f9f68-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9f68-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f9f68-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9f68-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9f68-135">CommonParameters</span></span>
<span data-ttu-id="f9f68-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f9f68-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9f68-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f9f68-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9f68-138">輸入</span><span class="sxs-lookup"><span data-stu-id="f9f68-138">INPUTS</span></span>

### <span data-ttu-id="f9f68-139">System.object</span><span class="sxs-lookup"><span data-stu-id="f9f68-139">System.String</span></span>

## <span data-ttu-id="f9f68-140">輸出</span><span class="sxs-lookup"><span data-stu-id="f9f68-140">OUTPUTS</span></span>

### <span data-ttu-id="f9f68-141">System.object</span><span class="sxs-lookup"><span data-stu-id="f9f68-141">System.Boolean</span></span>

## <span data-ttu-id="f9f68-142">筆記</span><span class="sxs-lookup"><span data-stu-id="f9f68-142">NOTES</span></span>

## <span data-ttu-id="f9f68-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9f68-143">RELATED LINKS</span></span>
