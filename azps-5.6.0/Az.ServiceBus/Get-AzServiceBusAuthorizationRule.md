---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: 39f43af6685f754cacfd1340560fd4c3429f792d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904342"
---
# <span data-ttu-id="fdb2e-101">Get-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fdb2e-101">Get-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="fdb2e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fdb2e-102">SYNOPSIS</span></span>
<span data-ttu-id="fdb2e-103">獲得指定命名空間或佇列或主題或 GeoDR 組 (別名的指定授權規則) 。</span><span class="sxs-lookup"><span data-stu-id="fdb2e-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

## <span data-ttu-id="fdb2e-104">語法</span><span class="sxs-lookup"><span data-stu-id="fdb2e-104">SYNTAX</span></span>

### <span data-ttu-id="fdb2e-105">命名空間驗證RuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fdb2e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdb2e-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="fdb2e-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdb2e-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="fdb2e-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdb2e-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="fdb2e-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdb2e-109">描述</span><span class="sxs-lookup"><span data-stu-id="fdb2e-109">DESCRIPTION</span></span>
<span data-ttu-id="fdb2e-110">**Get-AzServiceBusAuthorizationRule** Cmdlet 會取得指定命名空間或佇列或主題或別名 (GeoDR 組) 。</span><span class="sxs-lookup"><span data-stu-id="fdb2e-110">The **Get-AzServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="fdb2e-111">例子</span><span class="sxs-lookup"><span data-stu-id="fdb2e-111">EXAMPLES</span></span>

### <span data-ttu-id="fdb2e-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="fdb2e-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="fdb2e-113">會針對指定的命名空間，返回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="fdb2e-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="fdb2e-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="fdb2e-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="fdb2e-115">會針對指定的佇列，返回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="fdb2e-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="fdb2e-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="fdb2e-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="fdb2e-117">會針對指定的主題，返回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="fdb2e-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="fdb2e-118">範例 4</span><span class="sxs-lookup"><span data-stu-id="fdb2e-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="fdb2e-119">會針對指定的命名空間和別名，返回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="fdb2e-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="fdb2e-120">參數</span><span class="sxs-lookup"><span data-stu-id="fdb2e-120">PARAMETERS</span></span>

### <span data-ttu-id="fdb2e-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="fdb2e-121">-AliasName</span></span>
<span data-ttu-id="fdb2e-122">GeoDR 組組名稱</span><span class="sxs-lookup"><span data-stu-id="fdb2e-122">GeoDR Configuration Name</span></span>

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

### <span data-ttu-id="fdb2e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdb2e-123">-DefaultProfile</span></span>
<span data-ttu-id="fdb2e-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fdb2e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdb2e-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="fdb2e-125">-Name</span></span>
<span data-ttu-id="fdb2e-126">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="fdb2e-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="fdb2e-127">-命名空間</span><span class="sxs-lookup"><span data-stu-id="fdb2e-127">-Namespace</span></span>
<span data-ttu-id="fdb2e-128">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="fdb2e-128">Namespace Name</span></span>

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

### <span data-ttu-id="fdb2e-129">-佇列</span><span class="sxs-lookup"><span data-stu-id="fdb2e-129">-Queue</span></span>
<span data-ttu-id="fdb2e-130">佇列名稱</span><span class="sxs-lookup"><span data-stu-id="fdb2e-130">Queue Name</span></span>

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

### <span data-ttu-id="fdb2e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdb2e-131">-ResourceGroupName</span></span>
<span data-ttu-id="fdb2e-132">資源組名</span><span class="sxs-lookup"><span data-stu-id="fdb2e-132">Resource Group Name</span></span>

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

### <span data-ttu-id="fdb2e-133">-主題</span><span class="sxs-lookup"><span data-stu-id="fdb2e-133">-Topic</span></span>
<span data-ttu-id="fdb2e-134">主題名稱</span><span class="sxs-lookup"><span data-stu-id="fdb2e-134">Topic Name</span></span>

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

### <span data-ttu-id="fdb2e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdb2e-135">CommonParameters</span></span>
<span data-ttu-id="fdb2e-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fdb2e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdb2e-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="fdb2e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdb2e-138">輸入</span><span class="sxs-lookup"><span data-stu-id="fdb2e-138">INPUTS</span></span>

### <span data-ttu-id="fdb2e-139">System.String</span><span class="sxs-lookup"><span data-stu-id="fdb2e-139">System.String</span></span>

## <span data-ttu-id="fdb2e-140">輸出</span><span class="sxs-lookup"><span data-stu-id="fdb2e-140">OUTPUTS</span></span>

### <span data-ttu-id="fdb2e-141">Microsoft.Azure.Commands.ServiceBus.models.PSSharedAccesssAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="fdb2e-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="fdb2e-142">筆記</span><span class="sxs-lookup"><span data-stu-id="fdb2e-142">NOTES</span></span>

## <span data-ttu-id="fdb2e-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="fdb2e-143">RELATED LINKS</span></span>
