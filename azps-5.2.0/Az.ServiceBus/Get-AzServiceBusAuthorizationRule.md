---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e0f6c8c2b07c0d9ab788504bb8eae3eb4615a7e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279144"
---
# <span data-ttu-id="bca21-101">Get-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bca21-101">Get-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="bca21-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bca21-102">SYNOPSIS</span></span>
<span data-ttu-id="bca21-103">針對指定的命名空間或佇列或主題或 (GeoDR 設定的別名，取得指定授權規則的描述) 。</span><span class="sxs-lookup"><span data-stu-id="bca21-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

## <span data-ttu-id="bca21-104">句法</span><span class="sxs-lookup"><span data-stu-id="bca21-104">SYNTAX</span></span>

### <span data-ttu-id="bca21-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bca21-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bca21-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="bca21-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bca21-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="bca21-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bca21-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="bca21-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bca21-109">說明</span><span class="sxs-lookup"><span data-stu-id="bca21-109">DESCRIPTION</span></span>
<span data-ttu-id="bca21-110">**AzServiceBusAuthorizationRule** Cmdlet 會在指定的命名空間或佇列或主題或主題或主題或主題或別名中取得指定授權規則的描述，) 的 [ (GeoDR 設定]。</span><span class="sxs-lookup"><span data-stu-id="bca21-110">The **Get-AzServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="bca21-111">示例</span><span class="sxs-lookup"><span data-stu-id="bca21-111">EXAMPLES</span></span>

### <span data-ttu-id="bca21-112">範例1</span><span class="sxs-lookup"><span data-stu-id="bca21-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="bca21-113">針對指定的命名空間傳回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="bca21-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="bca21-114">範例2</span><span class="sxs-lookup"><span data-stu-id="bca21-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="bca21-115">針對指定的佇列傳回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="bca21-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="bca21-116">範例3</span><span class="sxs-lookup"><span data-stu-id="bca21-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="bca21-117">針對指定的主題，傳回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="bca21-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="bca21-118">範例4</span><span class="sxs-lookup"><span data-stu-id="bca21-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="bca21-119">針對指定的命名空間和別名傳回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="bca21-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="bca21-120">參數</span><span class="sxs-lookup"><span data-stu-id="bca21-120">PARAMETERS</span></span>

### <span data-ttu-id="bca21-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="bca21-121">-AliasName</span></span>
<span data-ttu-id="bca21-122">GeoDR 配置名稱</span><span class="sxs-lookup"><span data-stu-id="bca21-122">GeoDR Configuration Name</span></span>

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

### <span data-ttu-id="bca21-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bca21-123">-DefaultProfile</span></span>
<span data-ttu-id="bca21-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bca21-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bca21-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="bca21-125">-Name</span></span>
<span data-ttu-id="bca21-126">AuthorizationRule 名稱</span><span class="sxs-lookup"><span data-stu-id="bca21-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="bca21-127">-命名空間</span><span class="sxs-lookup"><span data-stu-id="bca21-127">-Namespace</span></span>
<span data-ttu-id="bca21-128">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="bca21-128">Namespace Name</span></span>

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

### <span data-ttu-id="bca21-129">-佇列</span><span class="sxs-lookup"><span data-stu-id="bca21-129">-Queue</span></span>
<span data-ttu-id="bca21-130">佇列名稱</span><span class="sxs-lookup"><span data-stu-id="bca21-130">Queue Name</span></span>

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

### <span data-ttu-id="bca21-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bca21-131">-ResourceGroupName</span></span>
<span data-ttu-id="bca21-132">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="bca21-132">Resource Group Name</span></span>

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

### <span data-ttu-id="bca21-133">-主題</span><span class="sxs-lookup"><span data-stu-id="bca21-133">-Topic</span></span>
<span data-ttu-id="bca21-134">主題名稱</span><span class="sxs-lookup"><span data-stu-id="bca21-134">Topic Name</span></span>

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

### <span data-ttu-id="bca21-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bca21-135">CommonParameters</span></span>
<span data-ttu-id="bca21-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bca21-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bca21-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bca21-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bca21-138">輸入</span><span class="sxs-lookup"><span data-stu-id="bca21-138">INPUTS</span></span>

### <span data-ttu-id="bca21-139">System.object</span><span class="sxs-lookup"><span data-stu-id="bca21-139">System.String</span></span>

## <span data-ttu-id="bca21-140">輸出</span><span class="sxs-lookup"><span data-stu-id="bca21-140">OUTPUTS</span></span>

### <span data-ttu-id="bca21-141">PSSharedAccessAuthorizationRuleAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bca21-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="bca21-142">筆記</span><span class="sxs-lookup"><span data-stu-id="bca21-142">NOTES</span></span>

## <span data-ttu-id="bca21-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="bca21-143">RELATED LINKS</span></span>
