---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
ms.openlocfilehash: af83820d33b9f36d93cc7623001d22a6cb5e0212
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141898"
---
# <span data-ttu-id="4e799-101">Get-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4e799-101">Get-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="4e799-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e799-102">SYNOPSIS</span></span>
<span data-ttu-id="4e799-103">針對特定的中繼實體 (Namespace/WcfRelay/HybridConnection) ，取得指定授權規則的描述。</span><span class="sxs-lookup"><span data-stu-id="4e799-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="4e799-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e799-104">SYNTAX</span></span>

### <span data-ttu-id="4e799-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4e799-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e799-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="4e799-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e799-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="4e799-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e799-108">說明</span><span class="sxs-lookup"><span data-stu-id="4e799-108">DESCRIPTION</span></span>
<span data-ttu-id="4e799-109">**AzRelayAuthorizationRule** Cmdlet 會在指定的中繼實體中取得指定授權規則的描述， (命名空間/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="4e799-109">The **Get-AzRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="4e799-110">示例</span><span class="sxs-lookup"><span data-stu-id="4e799-110">EXAMPLES</span></span>

### <span data-ttu-id="4e799-111">範例1：命名空間</span><span class="sxs-lookup"><span data-stu-id="4e799-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut
         hoRule1
```

<span data-ttu-id="4e799-112">針對指定的命名空間傳回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="4e799-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="4e799-113">範例2： WcfRelay</span><span class="sxs-lookup"><span data-stu-id="4e799-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>Get-AzWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
         1/authorizationRules/AuthoRule1
```

<span data-ttu-id="4e799-114">針對指定的 WcfRelay 傳回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="4e799-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="4e799-115">範例3： HybridConnection</span><span class="sxs-lookup"><span data-stu-id="4e799-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\> Get-AzRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test
         HybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="4e799-116">針對指定的 HybridConnection 傳回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="4e799-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="4e799-117">參數</span><span class="sxs-lookup"><span data-stu-id="4e799-117">PARAMETERS</span></span>

### <span data-ttu-id="4e799-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e799-118">-DefaultProfile</span></span>
<span data-ttu-id="4e799-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e799-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e799-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="4e799-120">-HybridConnection</span></span>
<span data-ttu-id="4e799-121">HybridConnection [名稱]。</span><span class="sxs-lookup"><span data-stu-id="4e799-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="4e799-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="4e799-122">-Name</span></span>
<span data-ttu-id="4e799-123">AuthorizationRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="4e799-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="4e799-124">-命名空間</span><span class="sxs-lookup"><span data-stu-id="4e799-124">-Namespace</span></span>
<span data-ttu-id="4e799-125">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="4e799-125">Namespace Name.</span></span>

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

### <span data-ttu-id="4e799-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e799-126">-ResourceGroupName</span></span>
<span data-ttu-id="4e799-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="4e799-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="4e799-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="4e799-128">-WcfRelay</span></span>
<span data-ttu-id="4e799-129">WcfRelay [名稱]。</span><span class="sxs-lookup"><span data-stu-id="4e799-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="4e799-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e799-130">CommonParameters</span></span>
<span data-ttu-id="4e799-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e799-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e799-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4e799-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e799-133">輸入</span><span class="sxs-lookup"><span data-stu-id="4e799-133">INPUTS</span></span>

### <span data-ttu-id="4e799-134">System.object</span><span class="sxs-lookup"><span data-stu-id="4e799-134">System.String</span></span>

## <span data-ttu-id="4e799-135">輸出</span><span class="sxs-lookup"><span data-stu-id="4e799-135">OUTPUTS</span></span>

### <span data-ttu-id="4e799-136">PSAuthorizationRuleAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4e799-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="4e799-137">筆記</span><span class="sxs-lookup"><span data-stu-id="4e799-137">NOTES</span></span>

## <span data-ttu-id="4e799-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e799-138">RELATED LINKS</span></span>
