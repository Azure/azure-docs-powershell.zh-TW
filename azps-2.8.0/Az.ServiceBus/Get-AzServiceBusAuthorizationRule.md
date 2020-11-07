---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: 4717775f840d816b8f99cc64c4036d5563e8d849
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792129"
---
# <span data-ttu-id="e538a-101">Get-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e538a-101">Get-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="e538a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e538a-102">SYNOPSIS</span></span>
<span data-ttu-id="e538a-103">針對指定的命名空間或佇列或主題或 (GeoDR 設定的別名，取得指定授權規則的描述) 。</span><span class="sxs-lookup"><span data-stu-id="e538a-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

## <span data-ttu-id="e538a-104">句法</span><span class="sxs-lookup"><span data-stu-id="e538a-104">SYNTAX</span></span>

### <span data-ttu-id="e538a-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e538a-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e538a-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e538a-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e538a-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e538a-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e538a-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="e538a-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e538a-109">說明</span><span class="sxs-lookup"><span data-stu-id="e538a-109">DESCRIPTION</span></span>
<span data-ttu-id="e538a-110">**AzServiceBusAuthorizationRule** Cmdlet 會在指定的命名空間或佇列或主題或主題或主題或主題或別名中取得指定授權規則的描述，) 的 [ (GeoDR 設定]。</span><span class="sxs-lookup"><span data-stu-id="e538a-110">The **Get-AzServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="e538a-111">示例</span><span class="sxs-lookup"><span data-stu-id="e538a-111">EXAMPLES</span></span>

### <span data-ttu-id="e538a-112">範例1</span><span class="sxs-lookup"><span data-stu-id="e538a-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="e538a-113">針對指定的命名空間傳回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="e538a-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="e538a-114">範例2</span><span class="sxs-lookup"><span data-stu-id="e538a-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="e538a-115">針對指定的佇列傳回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="e538a-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="e538a-116">範例3</span><span class="sxs-lookup"><span data-stu-id="e538a-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="e538a-117">針對指定的主題，傳回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="e538a-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="e538a-118">範例4</span><span class="sxs-lookup"><span data-stu-id="e538a-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="e538a-119">針對指定的命名空間和別名傳回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="e538a-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="e538a-120">參數</span><span class="sxs-lookup"><span data-stu-id="e538a-120">PARAMETERS</span></span>

### <span data-ttu-id="e538a-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="e538a-121">-AliasName</span></span>
<span data-ttu-id="e538a-122">GeoDR 配置名稱</span><span class="sxs-lookup"><span data-stu-id="e538a-122">GeoDR Configuration Name</span></span>

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

### <span data-ttu-id="e538a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e538a-123">-DefaultProfile</span></span>
<span data-ttu-id="e538a-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e538a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e538a-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="e538a-125">-Name</span></span>
<span data-ttu-id="e538a-126">AuthorizationRule 名稱</span><span class="sxs-lookup"><span data-stu-id="e538a-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="e538a-127">-命名空間</span><span class="sxs-lookup"><span data-stu-id="e538a-127">-Namespace</span></span>
<span data-ttu-id="e538a-128">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="e538a-128">Namespace Name</span></span>

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

### <span data-ttu-id="e538a-129">-佇列</span><span class="sxs-lookup"><span data-stu-id="e538a-129">-Queue</span></span>
<span data-ttu-id="e538a-130">佇列名稱</span><span class="sxs-lookup"><span data-stu-id="e538a-130">Queue Name</span></span>

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

### <span data-ttu-id="e538a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e538a-131">-ResourceGroupName</span></span>
<span data-ttu-id="e538a-132">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="e538a-132">Resource Group Name</span></span>

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

### <span data-ttu-id="e538a-133">-主題</span><span class="sxs-lookup"><span data-stu-id="e538a-133">-Topic</span></span>
<span data-ttu-id="e538a-134">主題名稱</span><span class="sxs-lookup"><span data-stu-id="e538a-134">Topic Name</span></span>

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

### <span data-ttu-id="e538a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e538a-135">CommonParameters</span></span>
<span data-ttu-id="e538a-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e538a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e538a-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e538a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e538a-138">輸入</span><span class="sxs-lookup"><span data-stu-id="e538a-138">INPUTS</span></span>

### <span data-ttu-id="e538a-139">System.object</span><span class="sxs-lookup"><span data-stu-id="e538a-139">System.String</span></span>

## <span data-ttu-id="e538a-140">輸出</span><span class="sxs-lookup"><span data-stu-id="e538a-140">OUTPUTS</span></span>

### <span data-ttu-id="e538a-141">PSSharedAccessAuthorizationRuleAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e538a-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="e538a-142">筆記</span><span class="sxs-lookup"><span data-stu-id="e538a-142">NOTES</span></span>

## <span data-ttu-id="e538a-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="e538a-143">RELATED LINKS</span></span>
