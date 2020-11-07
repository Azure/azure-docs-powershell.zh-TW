---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 35e3889603dc7e86a7d10679864adfd34a880b66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624061"
---
# <span data-ttu-id="cf202-101">Remove-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cf202-101">Remove-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="cf202-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cf202-102">SYNOPSIS</span></span>
<span data-ttu-id="cf202-103">移除指定的事件中心授權規則。</span><span class="sxs-lookup"><span data-stu-id="cf202-103">Removes the specified Event Hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf202-104">句法</span><span class="sxs-lookup"><span data-stu-id="cf202-104">SYNTAX</span></span>

### <span data-ttu-id="cf202-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="cf202-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf202-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="cf202-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String>
 [-EventHub] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf202-107">說明</span><span class="sxs-lookup"><span data-stu-id="cf202-107">DESCRIPTION</span></span>
<span data-ttu-id="cf202-108">Remove-AzureRmEventHubAuthorizationRule Cmdlet 會從指定的事件中樞中移除並刪除指定的授權規則。</span><span class="sxs-lookup"><span data-stu-id="cf202-108">The Remove-AzureRmEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="cf202-109">示例</span><span class="sxs-lookup"><span data-stu-id="cf202-109">EXAMPLES</span></span>

### <span data-ttu-id="cf202-110">範例1</span><span class="sxs-lookup"><span data-stu-id="cf202-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="cf202-111">\` \` 從命名空間 MyNamespaceName 移除授權規則 MyAuthRuleName \` \` 。</span><span class="sxs-lookup"><span data-stu-id="cf202-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="cf202-112">範例2</span><span class="sxs-lookup"><span data-stu-id="cf202-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="cf202-113">\` \` 從事件中心 MyEventHubName 移除授權規則 MyAuthRuleName \` \` 。</span><span class="sxs-lookup"><span data-stu-id="cf202-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="cf202-114">參數</span><span class="sxs-lookup"><span data-stu-id="cf202-114">PARAMETERS</span></span>

### <span data-ttu-id="cf202-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf202-115">-DefaultProfile</span></span>
<span data-ttu-id="cf202-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf202-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf202-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="cf202-117">-EventHub</span></span>
<span data-ttu-id="cf202-118">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="cf202-118">EventHub Name</span></span>

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

### <span data-ttu-id="cf202-119">-Force</span><span class="sxs-lookup"><span data-stu-id="cf202-119">-Force</span></span>
<span data-ttu-id="cf202-120">不要求確認</span><span class="sxs-lookup"><span data-stu-id="cf202-120">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="cf202-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="cf202-121">-Name</span></span>
<span data-ttu-id="cf202-122">AuthorizationRule 名稱</span><span class="sxs-lookup"><span data-stu-id="cf202-122">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="cf202-123">-命名空間</span><span class="sxs-lookup"><span data-stu-id="cf202-123">-Namespace</span></span>
<span data-ttu-id="cf202-124">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="cf202-124">Namespace Name</span></span>

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

### <span data-ttu-id="cf202-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf202-125">-PassThru</span></span>
<span data-ttu-id="cf202-126">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="cf202-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cf202-127">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="cf202-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cf202-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf202-128">-ResourceGroupName</span></span>
<span data-ttu-id="cf202-129">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="cf202-129">Resource Group Name</span></span>

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

### <span data-ttu-id="cf202-130">-確認</span><span class="sxs-lookup"><span data-stu-id="cf202-130">-Confirm</span></span>
<span data-ttu-id="cf202-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cf202-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf202-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf202-132">-WhatIf</span></span>
<span data-ttu-id="cf202-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cf202-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf202-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cf202-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf202-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf202-135">CommonParameters</span></span>
<span data-ttu-id="cf202-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cf202-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf202-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cf202-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf202-138">輸入</span><span class="sxs-lookup"><span data-stu-id="cf202-138">INPUTS</span></span>

### <span data-ttu-id="cf202-139">System.object</span><span class="sxs-lookup"><span data-stu-id="cf202-139">System.String</span></span>

## <span data-ttu-id="cf202-140">輸出</span><span class="sxs-lookup"><span data-stu-id="cf202-140">OUTPUTS</span></span>

### <span data-ttu-id="cf202-141">System.object</span><span class="sxs-lookup"><span data-stu-id="cf202-141">System.Boolean</span></span>

## <span data-ttu-id="cf202-142">筆記</span><span class="sxs-lookup"><span data-stu-id="cf202-142">NOTES</span></span>

## <span data-ttu-id="cf202-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf202-143">RELATED LINKS</span></span>
