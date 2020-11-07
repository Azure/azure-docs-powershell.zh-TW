---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: bbc6c0119f0f8f424b508adc38b5de80cd097734
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625672"
---
# <span data-ttu-id="edccf-101">Set-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="edccf-101">Set-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="edccf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="edccf-102">SYNOPSIS</span></span>
<span data-ttu-id="edccf-103">針對指定的服務匯流排主題更新指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="edccf-103">Updates the specified authorization rule description for the given Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edccf-104">句法</span><span class="sxs-lookup"><span data-stu-id="edccf-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 -InputObj <SharedAccessAuthorizationRuleAttributes> [-Name <String>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edccf-105">說明</span><span class="sxs-lookup"><span data-stu-id="edccf-105">DESCRIPTION</span></span>
<span data-ttu-id="edccf-106">**AzureRmServiceBusTopicAuthorizationRule** Cmdlet 會更新特定服務匯流排主題之指定授權規則的描述。</span><span class="sxs-lookup"><span data-stu-id="edccf-106">The **Set-AzureRmServiceBusTopicAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Service Bus topic.</span></span>

## <span data-ttu-id="edccf-107">示例</span><span class="sxs-lookup"><span data-stu-id="edccf-107">EXAMPLES</span></span>

### <span data-ttu-id="edccf-108">範例1</span><span class="sxs-lookup"><span data-stu-id="edccf-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1

PS C:\> $authRuleObj.Rights.Add("Manage")

PS C:\> Set-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="edccf-109">針對主題的授權規則，將 [ **管理** ] 新增至 [存取權] `SBTopicAuthoRule1` `SB-Topic_exampl1` 。</span><span class="sxs-lookup"><span data-stu-id="edccf-109">Adds **Manage** to the access rights of the authorization rule `SBTopicAuthoRule1` on topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="edccf-110">參數</span><span class="sxs-lookup"><span data-stu-id="edccf-110">PARAMETERS</span></span>

### <span data-ttu-id="edccf-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="edccf-111">-ResourceGroup</span></span>
<span data-ttu-id="edccf-112">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="edccf-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="edccf-113">-許可權</span><span class="sxs-lookup"><span data-stu-id="edccf-113">-Rights</span></span>
<span data-ttu-id="edccf-114">版權例如，@ ( 「聆聽」、「傳送」、「管理」 ) 。</span><span class="sxs-lookup"><span data-stu-id="edccf-114">Rights; for example, @("Listen","Send","Manage").</span></span> <span data-ttu-id="edccf-115">如果未指定 **-AuthruleObj** ，則為必要。</span><span class="sxs-lookup"><span data-stu-id="edccf-115">Required if **-AuthruleObj** is not specified.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edccf-116">-確認</span><span class="sxs-lookup"><span data-stu-id="edccf-116">-Confirm</span></span>
<span data-ttu-id="edccf-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="edccf-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edccf-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edccf-118">-WhatIf</span></span>
<span data-ttu-id="edccf-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="edccf-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edccf-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="edccf-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edccf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edccf-121">-DefaultProfile</span></span>
<span data-ttu-id="edccf-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="edccf-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edccf-123">-InputObj</span><span class="sxs-lookup"><span data-stu-id="edccf-123">-InputObj</span></span>
<span data-ttu-id="edccf-124">AuthorizationRule 物件。</span><span class="sxs-lookup"><span data-stu-id="edccf-124">ServiceBus Topic AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edccf-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="edccf-125">-Name</span></span>
<span data-ttu-id="edccf-126">AuthorizationRule Name-如果未指定 ' AuthruleObj」則是必要的。</span><span class="sxs-lookup"><span data-stu-id="edccf-126">AuthorizationRule Name - Required if 'AuthruleObj' not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edccf-127">-命名空間</span><span class="sxs-lookup"><span data-stu-id="edccf-127">-Namespace</span></span>
<span data-ttu-id="edccf-128">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="edccf-128">Namespace Name.</span></span>

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

### <span data-ttu-id="edccf-129">-主題</span><span class="sxs-lookup"><span data-stu-id="edccf-129">-Topic</span></span>
<span data-ttu-id="edccf-130">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="edccf-130">Topic Name.</span></span>

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

### <span data-ttu-id="edccf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edccf-131">CommonParameters</span></span>
<span data-ttu-id="edccf-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="edccf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edccf-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="edccf-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edccf-134">輸入</span><span class="sxs-lookup"><span data-stu-id="edccf-134">INPUTS</span></span>

### <span data-ttu-id="edccf-135">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="edccf-135">-ResourceGroup</span></span>
 <span data-ttu-id="edccf-136">System.object</span><span class="sxs-lookup"><span data-stu-id="edccf-136">System.String</span></span>

### <span data-ttu-id="edccf-137">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="edccf-137">-NamespaceName</span></span>
 <span data-ttu-id="edccf-138">System.object</span><span class="sxs-lookup"><span data-stu-id="edccf-138">System.String</span></span>

### <span data-ttu-id="edccf-139">-TopicName</span><span class="sxs-lookup"><span data-stu-id="edccf-139">-TopicName</span></span>
 <span data-ttu-id="edccf-140">System.object</span><span class="sxs-lookup"><span data-stu-id="edccf-140">System.String</span></span>

### <span data-ttu-id="edccf-141">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="edccf-141">-AuthRuleObj</span></span>
 <span data-ttu-id="edccf-142">SharedAccessAuthorizationRuleAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="edccf-142">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="edccf-143">輸出</span><span class="sxs-lookup"><span data-stu-id="edccf-143">OUTPUTS</span></span>

### <span data-ttu-id="edccf-144">SharedAccessAuthorizationRuleAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="edccf-144">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="edccf-145">識別碼：/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorization 規則/SBTopicAuthoRule1 類型： SBTopicAuthoRule1/AuthorizationRules Name： Location：西美標記：許可權： {偵聽、傳送、管理}</span><span class="sxs-lookup"><span data-stu-id="edccf-145">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorization Rules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send, Manage}</span></span>

## <span data-ttu-id="edccf-146">筆記</span><span class="sxs-lookup"><span data-stu-id="edccf-146">NOTES</span></span>

## <span data-ttu-id="edccf-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="edccf-147">RELATED LINKS</span></span>

