---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e6e3fb3c1998a009b10599c3ea059a147ab7f9ce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126806"
---
# <span data-ttu-id="2e901-101">Remove-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2e901-101">Remove-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="2e901-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2e901-102">SYNOPSIS</span></span>
<span data-ttu-id="2e901-103">從指定的資源群組中移除服務匯流排命名空間或佇列或主題的授權規則。</span><span class="sxs-lookup"><span data-stu-id="2e901-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

## <span data-ttu-id="2e901-104">句法</span><span class="sxs-lookup"><span data-stu-id="2e901-104">SYNTAX</span></span>

### <span data-ttu-id="2e901-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2e901-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e901-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2e901-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e901-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2e901-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e901-108">說明</span><span class="sxs-lookup"><span data-stu-id="2e901-108">DESCRIPTION</span></span>
<span data-ttu-id="2e901-109">**AzServiceBusAuthorizationRule** Cmdlet 會移除指定資源群組的服務匯流排命名空間或佇列或主題的授權規則。</span><span class="sxs-lookup"><span data-stu-id="2e901-109">The **Remove-AzServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="2e901-110">示例</span><span class="sxs-lookup"><span data-stu-id="2e901-110">EXAMPLES</span></span>

### <span data-ttu-id="2e901-111">範例1</span><span class="sxs-lookup"><span data-stu-id="2e901-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="2e901-112">`SBAuthoRule1` `SB-Example1` 從指定的資源群組中移除命名空間的授權規則。</span><span class="sxs-lookup"><span data-stu-id="2e901-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="2e901-113">範例2</span><span class="sxs-lookup"><span data-stu-id="2e901-113">Example 2</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="2e901-114">`SBAuthoRule1` `SBQueue` 從指定的資源群組移除佇列的授權規則。</span><span class="sxs-lookup"><span data-stu-id="2e901-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="2e901-115">範例3</span><span class="sxs-lookup"><span data-stu-id="2e901-115">Example 3</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="2e901-116">`SBAuthoRule1` `SBTopic` 從指定的資源群組中移除主題的授權規則。</span><span class="sxs-lookup"><span data-stu-id="2e901-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="2e901-117">參數</span><span class="sxs-lookup"><span data-stu-id="2e901-117">PARAMETERS</span></span>

### <span data-ttu-id="2e901-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e901-118">-DefaultProfile</span></span>
<span data-ttu-id="2e901-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2e901-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e901-120">-Force</span><span class="sxs-lookup"><span data-stu-id="2e901-120">-Force</span></span>
<span data-ttu-id="2e901-121">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="2e901-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2e901-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e901-122">-InputObject</span></span>
<span data-ttu-id="2e901-123">AuthorizationRule 物件</span><span class="sxs-lookup"><span data-stu-id="2e901-123">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e901-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="2e901-124">-Name</span></span>
<span data-ttu-id="2e901-125">AuthorizationRule 名稱</span><span class="sxs-lookup"><span data-stu-id="2e901-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="2e901-126">-命名空間</span><span class="sxs-lookup"><span data-stu-id="2e901-126">-Namespace</span></span>
<span data-ttu-id="2e901-127">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="2e901-127">Namespace Name</span></span>

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

### <span data-ttu-id="2e901-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e901-128">-PassThru</span></span>
<span data-ttu-id="2e901-129">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="2e901-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2e901-130">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="2e901-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2e901-131">-佇列</span><span class="sxs-lookup"><span data-stu-id="2e901-131">-Queue</span></span>
<span data-ttu-id="2e901-132">佇列名稱</span><span class="sxs-lookup"><span data-stu-id="2e901-132">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e901-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e901-133">-ResourceGroupName</span></span>
<span data-ttu-id="2e901-134">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="2e901-134">Resource Group Name</span></span>

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

### <span data-ttu-id="2e901-135">-主題</span><span class="sxs-lookup"><span data-stu-id="2e901-135">-Topic</span></span>
<span data-ttu-id="2e901-136">主題名稱</span><span class="sxs-lookup"><span data-stu-id="2e901-136">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e901-137">-確認</span><span class="sxs-lookup"><span data-stu-id="2e901-137">-Confirm</span></span>
<span data-ttu-id="2e901-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2e901-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e901-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e901-139">-WhatIf</span></span>
<span data-ttu-id="2e901-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2e901-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e901-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2e901-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e901-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e901-142">CommonParameters</span></span>
<span data-ttu-id="2e901-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2e901-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e901-144">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2e901-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e901-145">輸入</span><span class="sxs-lookup"><span data-stu-id="2e901-145">INPUTS</span></span>

### <span data-ttu-id="2e901-146">System.object</span><span class="sxs-lookup"><span data-stu-id="2e901-146">System.String</span></span>

### <span data-ttu-id="2e901-147">PSSharedAccessAuthorizationRuleAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2e901-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="2e901-148">輸出</span><span class="sxs-lookup"><span data-stu-id="2e901-148">OUTPUTS</span></span>

### <span data-ttu-id="2e901-149">System.object</span><span class="sxs-lookup"><span data-stu-id="2e901-149">System.Boolean</span></span>

## <span data-ttu-id="2e901-150">筆記</span><span class="sxs-lookup"><span data-stu-id="2e901-150">NOTES</span></span>

## <span data-ttu-id="2e901-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="2e901-151">RELATED LINKS</span></span>
