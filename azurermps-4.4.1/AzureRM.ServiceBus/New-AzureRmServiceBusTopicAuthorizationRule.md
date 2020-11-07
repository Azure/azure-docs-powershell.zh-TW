---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: 603eb1363e15b58a324f7131dd986a7c84371a89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623855"
---
# <span data-ttu-id="5e26c-101">New-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5e26c-101">New-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="5e26c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5e26c-102">SYNOPSIS</span></span>
<span data-ttu-id="5e26c-103">針對指定的服務匯流排主題建立新的授權規則。</span><span class="sxs-lookup"><span data-stu-id="5e26c-103">Creates a new authorization rule for the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e26c-104">句法</span><span class="sxs-lookup"><span data-stu-id="5e26c-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 -Name <String> [-Rights] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e26c-105">說明</span><span class="sxs-lookup"><span data-stu-id="5e26c-105">DESCRIPTION</span></span>
<span data-ttu-id="5e26c-106">**新的-AzureRmServiceBusTopicAuthorizationRule** Cmdlet 會針對指定的服務匯流排主題建立新的授權規則。</span><span class="sxs-lookup"><span data-stu-id="5e26c-106">The **New-AzureRmServiceBusTopicAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus topic.</span></span>

## <span data-ttu-id="5e26c-107">示例</span><span class="sxs-lookup"><span data-stu-id="5e26c-107">EXAMPLES</span></span>

### <span data-ttu-id="5e26c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="5e26c-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="5e26c-109">`SBTopicAuthoRule1`使用主題的 [ **聆聽** ] 和 [ **傳送** ] 權利建立授權規則 `SB-Topic_exampl1` 。</span><span class="sxs-lookup"><span data-stu-id="5e26c-109">Creates authorization rule `SBTopicAuthoRule1` with **Listen** and **Send** rights for the topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="5e26c-110">參數</span><span class="sxs-lookup"><span data-stu-id="5e26c-110">PARAMETERS</span></span>

### <span data-ttu-id="5e26c-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5e26c-111">-ResourceGroup</span></span>
<span data-ttu-id="5e26c-112">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5e26c-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="5e26c-113">-許可權</span><span class="sxs-lookup"><span data-stu-id="5e26c-113">-Rights</span></span>
<span data-ttu-id="5e26c-114">權力;例如，@ ( 「聆聽」、「傳送」、「管理」 ) </span><span class="sxs-lookup"><span data-stu-id="5e26c-114">The rights; for example, @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e26c-115">-確認</span><span class="sxs-lookup"><span data-stu-id="5e26c-115">-Confirm</span></span>
<span data-ttu-id="5e26c-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5e26c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e26c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e26c-117">-WhatIf</span></span>
<span data-ttu-id="5e26c-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5e26c-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e26c-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5e26c-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e26c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e26c-120">-DefaultProfile</span></span>
<span data-ttu-id="5e26c-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5e26c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e26c-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="5e26c-122">-Name</span></span>
<span data-ttu-id="5e26c-123">AuthorizationRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="5e26c-123">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e26c-124">-命名空間</span><span class="sxs-lookup"><span data-stu-id="5e26c-124">-Namespace</span></span>
<span data-ttu-id="5e26c-125">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="5e26c-125">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e26c-126">-主題</span><span class="sxs-lookup"><span data-stu-id="5e26c-126">-Topic</span></span>
<span data-ttu-id="5e26c-127">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="5e26c-127">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e26c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e26c-128">CommonParameters</span></span>
<span data-ttu-id="5e26c-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5e26c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e26c-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5e26c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e26c-131">輸入</span><span class="sxs-lookup"><span data-stu-id="5e26c-131">INPUTS</span></span>

### <span data-ttu-id="5e26c-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5e26c-132">-ResourceGroup</span></span>
 <span data-ttu-id="5e26c-133">System.object</span><span class="sxs-lookup"><span data-stu-id="5e26c-133">System.String</span></span>
 

### <span data-ttu-id="5e26c-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="5e26c-134">-NamespaceName</span></span>
 <span data-ttu-id="5e26c-135">System.object</span><span class="sxs-lookup"><span data-stu-id="5e26c-135">System.String</span></span>
 

### <span data-ttu-id="5e26c-136">-TopicName</span><span class="sxs-lookup"><span data-stu-id="5e26c-136">-TopicName</span></span>
 <span data-ttu-id="5e26c-137">System.object</span><span class="sxs-lookup"><span data-stu-id="5e26c-137">System.String</span></span>
 

### <span data-ttu-id="5e26c-138">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="5e26c-138">-AuthorizationRuleName</span></span>
 <span data-ttu-id="5e26c-139">System.object</span><span class="sxs-lookup"><span data-stu-id="5e26c-139">System.String</span></span>

## <span data-ttu-id="5e26c-140">輸出</span><span class="sxs-lookup"><span data-stu-id="5e26c-140">OUTPUTS</span></span>

### <span data-ttu-id="5e26c-141">SharedAccessAuthorizationRuleAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5e26c-141">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="5e26c-142">識別碼：/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorizati onRules/SBTopicAuthoRule1 類型： AuthorizationRules Name： SBTopicAuthoRule1 Location：西美式標籤：許可權： {偵聽、傳送}</span><span class="sxs-lookup"><span data-stu-id="5e26c-142">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorizati onRules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="5e26c-143">筆記</span><span class="sxs-lookup"><span data-stu-id="5e26c-143">NOTES</span></span>

## <span data-ttu-id="5e26c-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e26c-144">RELATED LINKS</span></span>

