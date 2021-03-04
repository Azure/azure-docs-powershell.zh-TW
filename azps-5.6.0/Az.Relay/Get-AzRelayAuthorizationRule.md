---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/get-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
ms.openlocfilehash: bed3165eee350f55470c0cbca575226e77ec9d71
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914614"
---
# <span data-ttu-id="11fd2-101">Get-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="11fd2-101">Get-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="11fd2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="11fd2-102">SYNOPSIS</span></span>
<span data-ttu-id="11fd2-103">在命名空間/WcfRelay/HybridConnection (中，獲得指定轉場實體之指定授權規則) 。</span><span class="sxs-lookup"><span data-stu-id="11fd2-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="11fd2-104">語法</span><span class="sxs-lookup"><span data-stu-id="11fd2-104">SYNTAX</span></span>

### <span data-ttu-id="11fd2-105">命名空間驗證RuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="11fd2-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11fd2-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="11fd2-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11fd2-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="11fd2-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11fd2-108">描述</span><span class="sxs-lookup"><span data-stu-id="11fd2-108">DESCRIPTION</span></span>
<span data-ttu-id="11fd2-109">**Get-AzRelayAuthorizationRule** Cmdlet 會取得指定轉寄實體中指定授權規則的描述 (命名空間/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="11fd2-109">The **Get-AzRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="11fd2-110">例子</span><span class="sxs-lookup"><span data-stu-id="11fd2-110">EXAMPLES</span></span>

### <span data-ttu-id="11fd2-111">範例 1：命名空間</span><span class="sxs-lookup"><span data-stu-id="11fd2-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut
         hoRule1
```

<span data-ttu-id="11fd2-112">會針對指定的命名空間，返回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="11fd2-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="11fd2-113">範例 2：WcfRelay</span><span class="sxs-lookup"><span data-stu-id="11fd2-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>Get-AzWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
         1/authorizationRules/AuthoRule1
```

<span data-ttu-id="11fd2-114">會針對指定的 WcfRelay，返回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="11fd2-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="11fd2-115">範例 3：HybridConnection</span><span class="sxs-lookup"><span data-stu-id="11fd2-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\> Get-AzRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test
         HybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="11fd2-116">會針對指定的 HybridConnection，返回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="11fd2-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="11fd2-117">參數</span><span class="sxs-lookup"><span data-stu-id="11fd2-117">PARAMETERS</span></span>

### <span data-ttu-id="11fd2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11fd2-118">-DefaultProfile</span></span>
<span data-ttu-id="11fd2-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="11fd2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11fd2-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="11fd2-120">-HybridConnection</span></span>
<span data-ttu-id="11fd2-121">HybridConnection 名稱。</span><span class="sxs-lookup"><span data-stu-id="11fd2-121">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11fd2-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="11fd2-122">-Name</span></span>
<span data-ttu-id="11fd2-123">AuthorizationRule Name.</span><span class="sxs-lookup"><span data-stu-id="11fd2-123">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11fd2-124">-命名空間</span><span class="sxs-lookup"><span data-stu-id="11fd2-124">-Namespace</span></span>
<span data-ttu-id="11fd2-125">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="11fd2-125">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11fd2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11fd2-126">-ResourceGroupName</span></span>
<span data-ttu-id="11fd2-127">資源組名。</span><span class="sxs-lookup"><span data-stu-id="11fd2-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="11fd2-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="11fd2-128">-WcfRelay</span></span>
<span data-ttu-id="11fd2-129">WcfRelay 名稱。</span><span class="sxs-lookup"><span data-stu-id="11fd2-129">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11fd2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11fd2-130">CommonParameters</span></span>
<span data-ttu-id="11fd2-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="11fd2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11fd2-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="11fd2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11fd2-133">輸入</span><span class="sxs-lookup"><span data-stu-id="11fd2-133">INPUTS</span></span>

### <span data-ttu-id="11fd2-134">System.String</span><span class="sxs-lookup"><span data-stu-id="11fd2-134">System.String</span></span>

## <span data-ttu-id="11fd2-135">輸出</span><span class="sxs-lookup"><span data-stu-id="11fd2-135">OUTPUTS</span></span>

### <span data-ttu-id="11fd2-136">Microsoft.Azure.Commands.Relay.models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="11fd2-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="11fd2-137">筆記</span><span class="sxs-lookup"><span data-stu-id="11fd2-137">NOTES</span></span>

## <span data-ttu-id="11fd2-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="11fd2-138">RELATED LINKS</span></span>
