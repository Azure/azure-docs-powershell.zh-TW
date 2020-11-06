---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: c15528befc90a0249101602fef9b178e7a63c0ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449378"
---
# <span data-ttu-id="fa0a8-101">Remove-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fa0a8-101">Remove-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="fa0a8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fa0a8-102">SYNOPSIS</span></span>
<span data-ttu-id="fa0a8-103">移除指定的事件中心授權規則。</span><span class="sxs-lookup"><span data-stu-id="fa0a8-103">Removes the specified Event Hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa0a8-104">句法</span><span class="sxs-lookup"><span data-stu-id="fa0a8-104">SYNTAX</span></span>

### <span data-ttu-id="fa0a8-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fa0a8-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa0a8-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="fa0a8-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String>
 [-EventHub] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa0a8-107">說明</span><span class="sxs-lookup"><span data-stu-id="fa0a8-107">DESCRIPTION</span></span>
<span data-ttu-id="fa0a8-108">Remove-AzureRmEventHubAuthorizationRule Cmdlet 會從指定的事件中樞中移除並刪除指定的授權規則。</span><span class="sxs-lookup"><span data-stu-id="fa0a8-108">The Remove-AzureRmEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="fa0a8-109">示例</span><span class="sxs-lookup"><span data-stu-id="fa0a8-109">EXAMPLES</span></span>

### <span data-ttu-id="fa0a8-110">範例1</span><span class="sxs-lookup"><span data-stu-id="fa0a8-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

### <span data-ttu-id="fa0a8-111">範例2</span><span class="sxs-lookup"><span data-stu-id="fa0a8-111">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="fa0a8-112">\` \` 從事件中心 MyEventHubName 移除授權規則 MyAuthRuleName \` \` 。</span><span class="sxs-lookup"><span data-stu-id="fa0a8-112">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="fa0a8-113">參數</span><span class="sxs-lookup"><span data-stu-id="fa0a8-113">PARAMETERS</span></span>

### <span data-ttu-id="fa0a8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa0a8-114">-DefaultProfile</span></span>
<span data-ttu-id="fa0a8-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fa0a8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa0a8-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="fa0a8-116">-EventHub</span></span>
<span data-ttu-id="fa0a8-117">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="fa0a8-117">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa0a8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fa0a8-118">-Force</span></span>
<span data-ttu-id="fa0a8-119">不要求確認</span><span class="sxs-lookup"><span data-stu-id="fa0a8-119">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="fa0a8-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="fa0a8-120">-Name</span></span>
<span data-ttu-id="fa0a8-121">AuthorizationRule 名稱</span><span class="sxs-lookup"><span data-stu-id="fa0a8-121">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa0a8-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="fa0a8-122">-Namespace</span></span>
<span data-ttu-id="fa0a8-123">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="fa0a8-123">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa0a8-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa0a8-124">-PassThru</span></span>
<span data-ttu-id="fa0a8-125">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="fa0a8-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fa0a8-126">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="fa0a8-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fa0a8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa0a8-127">-ResourceGroupName</span></span>
<span data-ttu-id="fa0a8-128">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="fa0a8-128">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa0a8-129">-確認</span><span class="sxs-lookup"><span data-stu-id="fa0a8-129">-Confirm</span></span>
<span data-ttu-id="fa0a8-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fa0a8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa0a8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa0a8-131">-WhatIf</span></span>
<span data-ttu-id="fa0a8-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fa0a8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa0a8-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fa0a8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa0a8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa0a8-134">CommonParameters</span></span>
<span data-ttu-id="fa0a8-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fa0a8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fa0a8-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fa0a8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa0a8-137">輸入</span><span class="sxs-lookup"><span data-stu-id="fa0a8-137">INPUTS</span></span>

### <span data-ttu-id="fa0a8-138">System.object</span><span class="sxs-lookup"><span data-stu-id="fa0a8-138">System.String</span></span>


## <span data-ttu-id="fa0a8-139">輸出</span><span class="sxs-lookup"><span data-stu-id="fa0a8-139">OUTPUTS</span></span>

### <span data-ttu-id="fa0a8-140">System.object</span><span class="sxs-lookup"><span data-stu-id="fa0a8-140">System.Boolean</span></span>


## <span data-ttu-id="fa0a8-141">筆記</span><span class="sxs-lookup"><span data-stu-id="fa0a8-141">NOTES</span></span>

## <span data-ttu-id="fa0a8-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="fa0a8-142">RELATED LINKS</span></span>
