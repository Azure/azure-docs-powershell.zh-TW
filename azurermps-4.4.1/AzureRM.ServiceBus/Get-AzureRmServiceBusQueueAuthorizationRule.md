---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 5d3f9212fcaf55d6506723b6c29ed1da0d676bb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447995"
---
# <span data-ttu-id="b5086-101">Get-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b5086-101">Get-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="b5086-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b5086-102">SYNOPSIS</span></span>
<span data-ttu-id="b5086-103">取得特定服務匯流排佇列的指定授權規則的描述。</span><span class="sxs-lookup"><span data-stu-id="b5086-103">Gets the description of a specified authorization rule for a given Service Bus queue.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5086-104">句法</span><span class="sxs-lookup"><span data-stu-id="b5086-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5086-105">說明</span><span class="sxs-lookup"><span data-stu-id="b5086-105">DESCRIPTION</span></span>
<span data-ttu-id="b5086-106">**AzureRmServiceBusQueueAuthorizationRule** Cmdlet 會在指定的服務匯流排佇列上取得指定授權規則的描述。</span><span class="sxs-lookup"><span data-stu-id="b5086-106">The **Get-AzureRmServiceBusQueueAuthorizationRule** cmdlet gets the description of a specified authorization rule on the given Service Bus queue.</span></span>

## <span data-ttu-id="b5086-107">示例</span><span class="sxs-lookup"><span data-stu-id="b5086-107">EXAMPLES</span></span>

### <span data-ttu-id="b5086-108">範例1</span><span class="sxs-lookup"><span data-stu-id="b5086-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

<span data-ttu-id="b5086-109">針對特定服務匯流排佇列傳回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="b5086-109">Returns the specified authorization rule description for a given Service Bus queue.</span></span>

## <span data-ttu-id="b5086-110">參數</span><span class="sxs-lookup"><span data-stu-id="b5086-110">PARAMETERS</span></span>

### <span data-ttu-id="b5086-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b5086-111">-ResourceGroup</span></span>
<span data-ttu-id="b5086-112">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5086-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="b5086-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5086-113">-DefaultProfile</span></span>
<span data-ttu-id="b5086-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b5086-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5086-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="b5086-115">-Name</span></span>
<span data-ttu-id="b5086-116">EventHub AuthorizationRule Name。</span><span class="sxs-lookup"><span data-stu-id="b5086-116">EventHub AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="b5086-117">-命名空間</span><span class="sxs-lookup"><span data-stu-id="b5086-117">-Namespace</span></span>
<span data-ttu-id="b5086-118">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="b5086-118">Namespace Name.</span></span>

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

### <span data-ttu-id="b5086-119">-佇列</span><span class="sxs-lookup"><span data-stu-id="b5086-119">-Queue</span></span>
<span data-ttu-id="b5086-120">佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="b5086-120">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5086-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5086-121">CommonParameters</span></span>
<span data-ttu-id="b5086-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b5086-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5086-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b5086-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5086-124">輸入</span><span class="sxs-lookup"><span data-stu-id="b5086-124">INPUTS</span></span>

### <span data-ttu-id="b5086-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b5086-125">-ResourceGroup</span></span>
 <span data-ttu-id="b5086-126">System.object</span><span class="sxs-lookup"><span data-stu-id="b5086-126">System.String</span></span>
 

### <span data-ttu-id="b5086-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="b5086-127">-NamespaceName</span></span>
 <span data-ttu-id="b5086-128">System.object</span><span class="sxs-lookup"><span data-stu-id="b5086-128">System.String</span></span>
 

### <span data-ttu-id="b5086-129">-QueueName</span><span class="sxs-lookup"><span data-stu-id="b5086-129">-QueueName</span></span>
 <span data-ttu-id="b5086-130">System.object</span><span class="sxs-lookup"><span data-stu-id="b5086-130">System.String</span></span>
 

### <span data-ttu-id="b5086-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="b5086-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="b5086-132">System.object</span><span class="sxs-lookup"><span data-stu-id="b5086-132">System.String</span></span>

## <span data-ttu-id="b5086-133">輸出</span><span class="sxs-lookup"><span data-stu-id="b5086-133">OUTPUTS</span></span>

### <span data-ttu-id="b5086-134">[System.object]。清單 ' 1 [0.0.1.0，SharedAccessAuthorizationRuleAttributes，，版本 =，Culture = 中性，PublicKeyToken = null]」））。）</span><span class="sxs-lookup"><span data-stu-id="b5086-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="b5086-135">識別碼：/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onRules/SBAuthoRule1 類型： AuthorizationRules Name： SBAuthoRule1 Location：西美式標籤：許可權： {偵聽、傳送}</span><span class="sxs-lookup"><span data-stu-id="b5086-135">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onRules/SBAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="b5086-136">筆記</span><span class="sxs-lookup"><span data-stu-id="b5086-136">NOTES</span></span>

## <span data-ttu-id="b5086-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5086-137">RELATED LINKS</span></span>

