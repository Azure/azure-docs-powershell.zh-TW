---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: fa7224654581a5c71cb4daafa5dbb96100d63705
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456383"
---
# <span data-ttu-id="cd45c-101">Get-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cd45c-101">Get-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="cd45c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cd45c-102">SYNOPSIS</span></span>
<span data-ttu-id="cd45c-103">針對特定命名空間或佇列或主題取得指定授權規則的描述。</span><span class="sxs-lookup"><span data-stu-id="cd45c-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd45c-104">句法</span><span class="sxs-lookup"><span data-stu-id="cd45c-104">SYNTAX</span></span>

### <span data-ttu-id="cd45c-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="cd45c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd45c-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="cd45c-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd45c-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="cd45c-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd45c-108">說明</span><span class="sxs-lookup"><span data-stu-id="cd45c-108">DESCRIPTION</span></span>
<span data-ttu-id="cd45c-109">**AzureRmServiceBusAuthorizationRule** Cmdlet 會在指定的命名空間或主題中取得指定授權規則的描述。</span><span class="sxs-lookup"><span data-stu-id="cd45c-109">The **Get-AzureRmServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="cd45c-110">示例</span><span class="sxs-lookup"><span data-stu-id="cd45c-110">EXAMPLES</span></span>

### <span data-ttu-id="cd45c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="cd45c-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="cd45c-112">針對指定的命名空間傳回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="cd45c-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="cd45c-113">範例2</span><span class="sxs-lookup"><span data-stu-id="cd45c-113">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="cd45c-114">針對指定的佇列傳回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="cd45c-114">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="cd45c-115">範例3</span><span class="sxs-lookup"><span data-stu-id="cd45c-115">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="cd45c-116">針對指定的主題，傳回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="cd45c-116">Returns the specified authorization rule description for a specified topic.</span></span>

## <span data-ttu-id="cd45c-117">參數</span><span class="sxs-lookup"><span data-stu-id="cd45c-117">PARAMETERS</span></span>

### <span data-ttu-id="cd45c-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="cd45c-118">-Name</span></span>
<span data-ttu-id="cd45c-119">AuthorizationRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="cd45c-119">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd45c-120">-命名空間</span><span class="sxs-lookup"><span data-stu-id="cd45c-120">-Namespace</span></span>
<span data-ttu-id="cd45c-121">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="cd45c-121">Namespace Name.</span></span>

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

### <span data-ttu-id="cd45c-122">-佇列</span><span class="sxs-lookup"><span data-stu-id="cd45c-122">-Queue</span></span>
<span data-ttu-id="cd45c-123">佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="cd45c-123">Queue Name.</span></span>

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

### <span data-ttu-id="cd45c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd45c-124">-ResourceGroupName</span></span>
<span data-ttu-id="cd45c-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="cd45c-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="cd45c-126">-主題</span><span class="sxs-lookup"><span data-stu-id="cd45c-126">-Topic</span></span>
<span data-ttu-id="cd45c-127">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="cd45c-127">Topic Name.</span></span>

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

### <span data-ttu-id="cd45c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd45c-128">-DefaultProfile</span></span>
<span data-ttu-id="cd45c-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cd45c-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd45c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd45c-130">CommonParameters</span></span>
<span data-ttu-id="cd45c-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cd45c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd45c-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cd45c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd45c-133">輸入</span><span class="sxs-lookup"><span data-stu-id="cd45c-133">INPUTS</span></span>

### <span data-ttu-id="cd45c-134">System.object</span><span class="sxs-lookup"><span data-stu-id="cd45c-134">System.String</span></span>

## <span data-ttu-id="cd45c-135">輸出</span><span class="sxs-lookup"><span data-stu-id="cd45c-135">OUTPUTS</span></span>

### <span data-ttu-id="cd45c-136">[System.object]。清單 ' 1 [0.4.2.0，SharedAccessAuthorizationRuleAttributes，，版本 =，Culture = 中性，PublicKeyToken = null]」））。）</span><span class="sxs-lookup"><span data-stu-id="cd45c-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.4.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="cd45c-137">筆記</span><span class="sxs-lookup"><span data-stu-id="cd45c-137">NOTES</span></span>
## <span data-ttu-id="cd45c-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="cd45c-138">RELATED LINKS</span></span>

## <span data-ttu-id="cd45c-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="cd45c-139">RELATED LINKS</span></span>

