---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
ms.openlocfilehash: 0483c60a1624374dc3e5b750439d905f19ceb2fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625676"
---
# <span data-ttu-id="375f0-101">New-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="375f0-101">New-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="375f0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="375f0-102">SYNOPSIS</span></span>
<span data-ttu-id="375f0-103">重新生成服務匯流排命名空間或佇列或主題的主要或次要連線字串。</span><span class="sxs-lookup"><span data-stu-id="375f0-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="375f0-104">句法</span><span class="sxs-lookup"><span data-stu-id="375f0-104">SYNTAX</span></span>

### <span data-ttu-id="375f0-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="375f0-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="375f0-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="375f0-106">QueueAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="375f0-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="375f0-107">TopicAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="375f0-108">說明</span><span class="sxs-lookup"><span data-stu-id="375f0-108">DESCRIPTION</span></span>
<span data-ttu-id="375f0-109">**新的-AzureRmServiceBusKey** Cmdlet 會針對指定的命名空間或佇列或主題和授權規則產生新的主要或次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="375f0-109">The **New-AzureRmServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="375f0-110">示例</span><span class="sxs-lookup"><span data-stu-id="375f0-110">EXAMPLES</span></span>

### <span data-ttu-id="375f0-111">範例1</span><span class="sxs-lookup"><span data-stu-id="375f0-111">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="375f0-112">重新生成命名空間的主要或次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="375f0-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="375f0-113">範例2</span><span class="sxs-lookup"><span data-stu-id="375f0-113">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="375f0-114">重新產生佇列的主要或次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="375f0-114">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="375f0-115">範例3</span><span class="sxs-lookup"><span data-stu-id="375f0-115">Example 3</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="375f0-116">重新產生主題的主要或次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="375f0-116">Regenerates the primary or secondary connection strings for the topic.</span></span>

## <span data-ttu-id="375f0-117">參數</span><span class="sxs-lookup"><span data-stu-id="375f0-117">PARAMETERS</span></span>

### <span data-ttu-id="375f0-118">-確認</span><span class="sxs-lookup"><span data-stu-id="375f0-118">-Confirm</span></span>
<span data-ttu-id="375f0-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="375f0-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="375f0-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="375f0-120">-Name</span></span>
<span data-ttu-id="375f0-121">AuthorizationRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="375f0-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="375f0-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="375f0-122">-Namespace</span></span>
<span data-ttu-id="375f0-123">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="375f0-123">Namespace Name.</span></span>

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

### <span data-ttu-id="375f0-124">-佇列</span><span class="sxs-lookup"><span data-stu-id="375f0-124">-Queue</span></span>
<span data-ttu-id="375f0-125">佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="375f0-125">Queue Name.</span></span>

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

### <span data-ttu-id="375f0-126">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="375f0-126">-RegenerateKey</span></span>
<span data-ttu-id="375f0-127">重新產生按鍵-"PrimaryKey"/"SecondaryKey"。</span><span class="sxs-lookup"><span data-stu-id="375f0-127">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="375f0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="375f0-128">-ResourceGroupName</span></span>
<span data-ttu-id="375f0-129">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="375f0-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="375f0-130">-主題</span><span class="sxs-lookup"><span data-stu-id="375f0-130">-Topic</span></span>
<span data-ttu-id="375f0-131">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="375f0-131">Topic Name.</span></span>

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

### <span data-ttu-id="375f0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="375f0-132">-WhatIf</span></span>
<span data-ttu-id="375f0-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="375f0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="375f0-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="375f0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="375f0-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="375f0-135">-DefaultProfile</span></span>
<span data-ttu-id="375f0-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="375f0-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="375f0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="375f0-137">CommonParameters</span></span>
<span data-ttu-id="375f0-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="375f0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="375f0-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="375f0-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="375f0-140">輸入</span><span class="sxs-lookup"><span data-stu-id="375f0-140">INPUTS</span></span>

### <span data-ttu-id="375f0-141">System.object</span><span class="sxs-lookup"><span data-stu-id="375f0-141">System.String</span></span>

## <span data-ttu-id="375f0-142">輸出</span><span class="sxs-lookup"><span data-stu-id="375f0-142">OUTPUTS</span></span>

### <span data-ttu-id="375f0-143">ListKeysAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="375f0-143">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="375f0-144">筆記</span><span class="sxs-lookup"><span data-stu-id="375f0-144">NOTES</span></span>

## <span data-ttu-id="375f0-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="375f0-145">RELATED LINKS</span></span>

