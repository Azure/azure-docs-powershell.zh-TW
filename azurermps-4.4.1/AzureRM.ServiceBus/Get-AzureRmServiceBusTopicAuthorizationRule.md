---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: e8bcb3688aec6d718c192e4dac4b6b4632eba059
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454856"
---
# <span data-ttu-id="78ca3-101">Get-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="78ca3-101">Get-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="78ca3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="78ca3-102">SYNOPSIS</span></span>
<span data-ttu-id="78ca3-103">傳回指定主題之授權規則描述的描述。</span><span class="sxs-lookup"><span data-stu-id="78ca3-103">Returns the description of the specified authorization rule description for the given topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78ca3-104">句法</span><span class="sxs-lookup"><span data-stu-id="78ca3-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78ca3-105">說明</span><span class="sxs-lookup"><span data-stu-id="78ca3-105">DESCRIPTION</span></span>
<span data-ttu-id="78ca3-106">**AzureRmServiceBusTopicAuthorizationRule** Cmdlet 會針對給定服務匯流排主題取得指定授權規則的描述。</span><span class="sxs-lookup"><span data-stu-id="78ca3-106">The **Get-AzureRmServiceBusTopicAuthorizationRule** cmdlet gets the description of the specified authorization rule on the given Service Bus topic.</span></span>

## <span data-ttu-id="78ca3-107">示例</span><span class="sxs-lookup"><span data-stu-id="78ca3-107">EXAMPLES</span></span>

### <span data-ttu-id="78ca3-108">範例1</span><span class="sxs-lookup"><span data-stu-id="78ca3-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_example1 -AuthorizationRuleName SBTopicAuthoRule1
```

<span data-ttu-id="78ca3-109">傳回指定主題之授權規則的描述。</span><span class="sxs-lookup"><span data-stu-id="78ca3-109">Returns the description of the specified authorization rule for the given topic.</span></span>

## <span data-ttu-id="78ca3-110">參數</span><span class="sxs-lookup"><span data-stu-id="78ca3-110">PARAMETERS</span></span>

### <span data-ttu-id="78ca3-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="78ca3-111">-ResourceGroup</span></span>
<span data-ttu-id="78ca3-112">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="78ca3-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="78ca3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78ca3-113">-DefaultProfile</span></span>
<span data-ttu-id="78ca3-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="78ca3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78ca3-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="78ca3-115">-Name</span></span>
<span data-ttu-id="78ca3-116">主題 AuthorizationRule 名稱。</span><span class="sxs-lookup"><span data-stu-id="78ca3-116">Topic AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="78ca3-117">-命名空間</span><span class="sxs-lookup"><span data-stu-id="78ca3-117">-Namespace</span></span>
<span data-ttu-id="78ca3-118">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="78ca3-118">Namespace Name.</span></span>

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

### <span data-ttu-id="78ca3-119">-主題</span><span class="sxs-lookup"><span data-stu-id="78ca3-119">-Topic</span></span>
<span data-ttu-id="78ca3-120">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="78ca3-120">Topic Name.</span></span>

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

### <span data-ttu-id="78ca3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78ca3-121">CommonParameters</span></span>
<span data-ttu-id="78ca3-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="78ca3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78ca3-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="78ca3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78ca3-124">輸入</span><span class="sxs-lookup"><span data-stu-id="78ca3-124">INPUTS</span></span>

### <span data-ttu-id="78ca3-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="78ca3-125">-ResourceGroup</span></span>
 <span data-ttu-id="78ca3-126">System.object</span><span class="sxs-lookup"><span data-stu-id="78ca3-126">System.String</span></span>
 

### <span data-ttu-id="78ca3-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="78ca3-127">-NamespaceName</span></span>
 <span data-ttu-id="78ca3-128">System.object</span><span class="sxs-lookup"><span data-stu-id="78ca3-128">System.String</span></span>
 

### <span data-ttu-id="78ca3-129">-TopicName</span><span class="sxs-lookup"><span data-stu-id="78ca3-129">-TopicName</span></span>
 <span data-ttu-id="78ca3-130">System.object</span><span class="sxs-lookup"><span data-stu-id="78ca3-130">System.String</span></span>
 

### <span data-ttu-id="78ca3-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="78ca3-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="78ca3-132">System.object</span><span class="sxs-lookup"><span data-stu-id="78ca3-132">System.String</span></span>

## <span data-ttu-id="78ca3-133">輸出</span><span class="sxs-lookup"><span data-stu-id="78ca3-133">OUTPUTS</span></span>

### <span data-ttu-id="78ca3-134">[System.object]。清單 ' 1 [0.0.1.0，SharedAccessAuthorizationRuleAttributes，，版本 =，Culture = 中性，PublicKeyToken = null]」））。）</span><span class="sxs-lookup"><span data-stu-id="78ca3-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="78ca3-135">識別碼：/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1/authorizati onRules/SBTopicAuthoRule1 類型： AuthorizationRules Name： SBTopicAuthoRule1 Location：西美式標籤：許可權： {偵聽、傳送}</span><span class="sxs-lookup"><span data-stu-id="78ca3-135">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1/authorizati onRules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="78ca3-136">筆記</span><span class="sxs-lookup"><span data-stu-id="78ca3-136">NOTES</span></span>

## <span data-ttu-id="78ca3-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="78ca3-137">RELATED LINKS</span></span>

