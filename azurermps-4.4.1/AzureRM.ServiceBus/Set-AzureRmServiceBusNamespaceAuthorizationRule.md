---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: a56f9b27e19868d22eed94fbcf7717fbe1c68b39
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625962"
---
# <span data-ttu-id="54807-101">Set-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="54807-101">Set-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="54807-102">摘要</span><span class="sxs-lookup"><span data-stu-id="54807-102">SYNOPSIS</span></span>
<span data-ttu-id="54807-103">針對指定的服務匯流排命名空間更新指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="54807-103">Updates the specified authorization rule description for the given Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54807-104">句法</span><span class="sxs-lookup"><span data-stu-id="54807-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusNamespaceAuthorizationRule [-ResourceGroup] <String> -Namespace <String>
 -InputObj <SharedAccessAuthorizationRuleAttributes> [-Name <String>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54807-105">說明</span><span class="sxs-lookup"><span data-stu-id="54807-105">DESCRIPTION</span></span>
<span data-ttu-id="54807-106">**AzureRmServiceBusNamespaceAuthorizationRule** Cmdlet 會在指定的服務匯流排命名空間中更新指定授權規則的描述。</span><span class="sxs-lookup"><span data-stu-id="54807-106">The **Set-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace.</span></span>

## <span data-ttu-id="54807-107">示例</span><span class="sxs-lookup"><span data-stu-id="54807-107">EXAMPLES</span></span>

### <span data-ttu-id="54807-108">範例1</span><span class="sxs-lookup"><span data-stu-id="54807-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="54807-109">從命名空間中授權規則的存取許可權中移除 [ **管理** ] `AuthoRule1` `SB-Example1` 。</span><span class="sxs-lookup"><span data-stu-id="54807-109">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

## <span data-ttu-id="54807-110">參數</span><span class="sxs-lookup"><span data-stu-id="54807-110">PARAMETERS</span></span>

### <span data-ttu-id="54807-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="54807-111">-ResourceGroup</span></span>
<span data-ttu-id="54807-112">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="54807-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="54807-113">-許可權</span><span class="sxs-lookup"><span data-stu-id="54807-113">-Rights</span></span>
<span data-ttu-id="54807-114">版權例如 @ ( 「聆聽」、「傳送」、「管理」 ) 。</span><span class="sxs-lookup"><span data-stu-id="54807-114">Rights; for example @("Listen","Send","Manage").</span></span> <span data-ttu-id="54807-115">如果未指定 **AuthruleObj** ，則為必要。</span><span class="sxs-lookup"><span data-stu-id="54807-115">Required if **AuthruleObj** is not specified.</span></span>

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

### <span data-ttu-id="54807-116">-確認</span><span class="sxs-lookup"><span data-stu-id="54807-116">-Confirm</span></span>
<span data-ttu-id="54807-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="54807-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54807-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54807-118">-WhatIf</span></span>
<span data-ttu-id="54807-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="54807-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54807-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="54807-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54807-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54807-121">-DefaultProfile</span></span>
<span data-ttu-id="54807-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="54807-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54807-123">-InputObj</span><span class="sxs-lookup"><span data-stu-id="54807-123">-InputObj</span></span>
<span data-ttu-id="54807-124">已將 NameSpace AuthorizationRule 物件。</span><span class="sxs-lookup"><span data-stu-id="54807-124">ServiceBus NameSpace AuthorizationRule Object.</span></span>

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

### <span data-ttu-id="54807-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="54807-125">-Name</span></span>
<span data-ttu-id="54807-126">AuthorizationRule Name-如果未指定 ' AuthruleObj」則是必要的。</span><span class="sxs-lookup"><span data-stu-id="54807-126">AuthorizationRule Name - Required if 'AuthruleObj' not specified.</span></span>

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

### <span data-ttu-id="54807-127">-命名空間</span><span class="sxs-lookup"><span data-stu-id="54807-127">-Namespace</span></span>
<span data-ttu-id="54807-128">已將命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="54807-128">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="54807-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54807-129">CommonParameters</span></span>
<span data-ttu-id="54807-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="54807-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54807-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="54807-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54807-132">輸入</span><span class="sxs-lookup"><span data-stu-id="54807-132">INPUTS</span></span>

### <span data-ttu-id="54807-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="54807-133">-ResourceGroup</span></span>
 <span data-ttu-id="54807-134">System.object</span><span class="sxs-lookup"><span data-stu-id="54807-134">System.String</span></span>

### <span data-ttu-id="54807-135">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="54807-135">-NamespaceName</span></span>
 <span data-ttu-id="54807-136">System.object</span><span class="sxs-lookup"><span data-stu-id="54807-136">System.String</span></span>

### <span data-ttu-id="54807-137">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="54807-137">-AuthRuleObj</span></span>
 <span data-ttu-id="54807-138">SharedAccessAuthorizationRuleAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="54807-138">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="54807-139">輸出</span><span class="sxs-lookup"><span data-stu-id="54807-139">OUTPUTS</span></span>

### <span data-ttu-id="54807-140">SharedAccessAuthorizationRuleAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="54807-140">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="54807-141">識別碼：/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 類型： AuthorizationRules Name： AuthoRule1 Location：標記：許可權： {偵聽、傳送}</span><span class="sxs-lookup"><span data-stu-id="54807-141">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : AuthoRule1 Location : Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="54807-142">筆記</span><span class="sxs-lookup"><span data-stu-id="54807-142">NOTES</span></span>

## <span data-ttu-id="54807-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="54807-143">RELATED LINKS</span></span>

