---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
ms.openlocfilehash: 28abf3ff725f5a1b124f99c96b46d03458b42f8e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446672"
---
# <span data-ttu-id="e5074-101">Get-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="e5074-101">Get-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="e5074-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5074-102">SYNOPSIS</span></span>
<span data-ttu-id="e5074-103">針對指定的命名空間或佇列或主題取得主要和次要的連線字串。</span><span class="sxs-lookup"><span data-stu-id="e5074-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5074-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5074-104">SYNTAX</span></span>

### <span data-ttu-id="e5074-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e5074-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5074-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e5074-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5074-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e5074-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5074-108">說明</span><span class="sxs-lookup"><span data-stu-id="e5074-108">DESCRIPTION</span></span>
<span data-ttu-id="e5074-109">**AzureRmServiceBusKey** Cmdlet 會針對指定的命名空間或佇列或主題傳回主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="e5074-109">The **Get-AzureRmServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic.</span></span> 

## <span data-ttu-id="e5074-110">示例</span><span class="sxs-lookup"><span data-stu-id="e5074-110">EXAMPLES</span></span>

### <span data-ttu-id="e5074-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e5074-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="e5074-112">在指定命名空間中的主要和次要連線字串。</span><span class="sxs-lookup"><span data-stu-id="e5074-112">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="e5074-113">範例2</span><span class="sxs-lookup"><span data-stu-id="e5074-113">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="e5074-114">主要和次要連接字串到指定的佇列。</span><span class="sxs-lookup"><span data-stu-id="e5074-114">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="e5074-115">範例3</span><span class="sxs-lookup"><span data-stu-id="e5074-115">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="e5074-116">指定主題的主要和次要連線字串。</span><span class="sxs-lookup"><span data-stu-id="e5074-116">Primary and secondary connection string to the specified topic.</span></span>

## <span data-ttu-id="e5074-117">參數</span><span class="sxs-lookup"><span data-stu-id="e5074-117">PARAMETERS</span></span>

### <span data-ttu-id="e5074-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="e5074-118">-Name</span></span>
<span data-ttu-id="e5074-119">AuthorizationRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="e5074-119">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="e5074-120">-命名空間</span><span class="sxs-lookup"><span data-stu-id="e5074-120">-Namespace</span></span>
<span data-ttu-id="e5074-121">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="e5074-121">Namespace Name.</span></span>

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

### <span data-ttu-id="e5074-122">-佇列</span><span class="sxs-lookup"><span data-stu-id="e5074-122">-Queue</span></span>
<span data-ttu-id="e5074-123">佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="e5074-123">Queue Name.</span></span>

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

### <span data-ttu-id="e5074-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5074-124">-ResourceGroupName</span></span>
<span data-ttu-id="e5074-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e5074-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="e5074-126">-主題</span><span class="sxs-lookup"><span data-stu-id="e5074-126">-Topic</span></span>
<span data-ttu-id="e5074-127">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="e5074-127">Topic Name.</span></span>

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

### <span data-ttu-id="e5074-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5074-128">-DefaultProfile</span></span>
<span data-ttu-id="e5074-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5074-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5074-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5074-130">CommonParameters</span></span>
<span data-ttu-id="e5074-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5074-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5074-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e5074-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5074-133">輸入</span><span class="sxs-lookup"><span data-stu-id="e5074-133">INPUTS</span></span>

### <span data-ttu-id="e5074-134">System.object</span><span class="sxs-lookup"><span data-stu-id="e5074-134">System.String</span></span>

## <span data-ttu-id="e5074-135">輸出</span><span class="sxs-lookup"><span data-stu-id="e5074-135">OUTPUTS</span></span>

### <span data-ttu-id="e5074-136">ListKeysAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e5074-136">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="e5074-137">筆記</span><span class="sxs-lookup"><span data-stu-id="e5074-137">NOTES</span></span>

## <span data-ttu-id="e5074-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5074-138">RELATED LINKS</span></span>

