---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
ms.openlocfilehash: 28ecd68167a7db2f41ee64a38a4616548707096c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908738"
---
# <span data-ttu-id="5d4ad-101">Get-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="5d4ad-101">Get-AzServiceBusKey</span></span>

## <span data-ttu-id="5d4ad-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5d4ad-102">SYNOPSIS</span></span>
<span data-ttu-id="5d4ad-103">在 GeoDR 組配置中，為指定命名空間或佇列或主題或別名 (主要和次要) 。</span><span class="sxs-lookup"><span data-stu-id="5d4ad-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="5d4ad-104">語法</span><span class="sxs-lookup"><span data-stu-id="5d4ad-104">SYNTAX</span></span>

### <span data-ttu-id="5d4ad-105">命名空間驗證RuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5d4ad-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d4ad-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5d4ad-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d4ad-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5d4ad-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d4ad-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="5d4ad-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d4ad-109">描述</span><span class="sxs-lookup"><span data-stu-id="5d4ad-109">DESCRIPTION</span></span>
<span data-ttu-id="5d4ad-110">**Get-AzServiceBusKey** Cmdlet 會針對指定命名空間或佇列或主題或別名 (GeoDR 組) 。</span><span class="sxs-lookup"><span data-stu-id="5d4ad-110">The **Get-AzServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="5d4ad-111">例子</span><span class="sxs-lookup"><span data-stu-id="5d4ad-111">EXAMPLES</span></span>

### <span data-ttu-id="5d4ad-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="5d4ad-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="5d4ad-113">到指定命名空間的主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="5d4ad-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="5d4ad-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="5d4ad-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="5d4ad-115">指定佇列的主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="5d4ad-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="5d4ad-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="5d4ad-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="5d4ad-117">指定主題的主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="5d4ad-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="5d4ad-118">範例 4</span><span class="sxs-lookup"><span data-stu-id="5d4ad-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="5d4ad-119">指定命名空間和別名的主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="5d4ad-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="5d4ad-120">參數</span><span class="sxs-lookup"><span data-stu-id="5d4ad-120">PARAMETERS</span></span>

### <span data-ttu-id="5d4ad-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="5d4ad-121">-AliasName</span></span>
<span data-ttu-id="5d4ad-122">別名名稱</span><span class="sxs-lookup"><span data-stu-id="5d4ad-122">Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d4ad-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d4ad-123">-DefaultProfile</span></span>
<span data-ttu-id="5d4ad-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5d4ad-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d4ad-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="5d4ad-125">-Name</span></span>
<span data-ttu-id="5d4ad-126">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="5d4ad-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="5d4ad-127">-命名空間</span><span class="sxs-lookup"><span data-stu-id="5d4ad-127">-Namespace</span></span>
<span data-ttu-id="5d4ad-128">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="5d4ad-128">Namespace Name</span></span>

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

### <span data-ttu-id="5d4ad-129">-佇列</span><span class="sxs-lookup"><span data-stu-id="5d4ad-129">-Queue</span></span>
<span data-ttu-id="5d4ad-130">佇列名稱</span><span class="sxs-lookup"><span data-stu-id="5d4ad-130">Queue Name</span></span>

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

### <span data-ttu-id="5d4ad-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d4ad-131">-ResourceGroupName</span></span>
<span data-ttu-id="5d4ad-132">資源組名</span><span class="sxs-lookup"><span data-stu-id="5d4ad-132">Resource Group Name</span></span>

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

### <span data-ttu-id="5d4ad-133">-主題</span><span class="sxs-lookup"><span data-stu-id="5d4ad-133">-Topic</span></span>
<span data-ttu-id="5d4ad-134">主題名稱</span><span class="sxs-lookup"><span data-stu-id="5d4ad-134">Topic Name</span></span>

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

### <span data-ttu-id="5d4ad-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d4ad-135">CommonParameters</span></span>
<span data-ttu-id="5d4ad-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5d4ad-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d4ad-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5d4ad-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d4ad-138">輸入</span><span class="sxs-lookup"><span data-stu-id="5d4ad-138">INPUTS</span></span>

### <span data-ttu-id="5d4ad-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5d4ad-139">System.String</span></span>

## <span data-ttu-id="5d4ad-140">輸出</span><span class="sxs-lookup"><span data-stu-id="5d4ad-140">OUTPUTS</span></span>

### <span data-ttu-id="5d4ad-141">Microsoft.Azure.Commands.ServiceBus.models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="5d4ad-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="5d4ad-142">筆記</span><span class="sxs-lookup"><span data-stu-id="5d4ad-142">NOTES</span></span>

## <span data-ttu-id="5d4ad-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="5d4ad-143">RELATED LINKS</span></span>
