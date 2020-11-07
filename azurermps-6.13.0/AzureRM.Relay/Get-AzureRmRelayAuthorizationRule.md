---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 13de3f05879234a0db1af34517d37172c2a5a6bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625759"
---
# <span data-ttu-id="b06d4-101">Get-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b06d4-101">Get-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="b06d4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b06d4-102">SYNOPSIS</span></span>
<span data-ttu-id="b06d4-103">針對特定的中繼實體 (Namespace/WcfRelay/HybridConnection) ，取得指定授權規則的描述。</span><span class="sxs-lookup"><span data-stu-id="b06d4-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b06d4-104">句法</span><span class="sxs-lookup"><span data-stu-id="b06d4-104">SYNTAX</span></span>

### <span data-ttu-id="b06d4-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b06d4-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b06d4-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b06d4-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b06d4-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b06d4-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b06d4-108">說明</span><span class="sxs-lookup"><span data-stu-id="b06d4-108">DESCRIPTION</span></span>
<span data-ttu-id="b06d4-109">**AzureRmRelayAuthorizationRule** Cmdlet 會在指定的中繼實體中取得指定授權規則的描述， (命名空間/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="b06d4-109">The **Get-AzureRmRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="b06d4-110">示例</span><span class="sxs-lookup"><span data-stu-id="b06d4-110">EXAMPLES</span></span>

### <span data-ttu-id="b06d4-111">範例 1-命名空間</span><span class="sxs-lookup"><span data-stu-id="b06d4-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut
         hoRule1
```

<span data-ttu-id="b06d4-112">針對指定的命名空間傳回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="b06d4-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="b06d4-113">範例 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="b06d4-113">Example 2 - WcfRelay</span></span>
```
PS C:\>Get-AzureRmWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
         1/authorizationRules/AuthoRule1
```

<span data-ttu-id="b06d4-114">針對指定的 WcfRelay 傳回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="b06d4-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="b06d4-115">範例 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="b06d4-115">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test
         HybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="b06d4-116">針對指定的 HybridConnection 傳回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="b06d4-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="b06d4-117">參數</span><span class="sxs-lookup"><span data-stu-id="b06d4-117">PARAMETERS</span></span>

### <span data-ttu-id="b06d4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b06d4-118">-DefaultProfile</span></span>
<span data-ttu-id="b06d4-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b06d4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b06d4-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="b06d4-120">-HybridConnection</span></span>
<span data-ttu-id="b06d4-121">HybridConnection [名稱]。</span><span class="sxs-lookup"><span data-stu-id="b06d4-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="b06d4-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="b06d4-122">-Name</span></span>
<span data-ttu-id="b06d4-123">AuthorizationRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="b06d4-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="b06d4-124">-命名空間</span><span class="sxs-lookup"><span data-stu-id="b06d4-124">-Namespace</span></span>
<span data-ttu-id="b06d4-125">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="b06d4-125">Namespace Name.</span></span>

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

### <span data-ttu-id="b06d4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b06d4-126">-ResourceGroupName</span></span>
<span data-ttu-id="b06d4-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="b06d4-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="b06d4-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="b06d4-128">-WcfRelay</span></span>
<span data-ttu-id="b06d4-129">WcfRelay [名稱]。</span><span class="sxs-lookup"><span data-stu-id="b06d4-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="b06d4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b06d4-130">CommonParameters</span></span>
<span data-ttu-id="b06d4-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b06d4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b06d4-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b06d4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b06d4-133">輸入</span><span class="sxs-lookup"><span data-stu-id="b06d4-133">INPUTS</span></span>

### <span data-ttu-id="b06d4-134">System.object</span><span class="sxs-lookup"><span data-stu-id="b06d4-134">System.String</span></span>


## <span data-ttu-id="b06d4-135">輸出</span><span class="sxs-lookup"><span data-stu-id="b06d4-135">OUTPUTS</span></span>

### <span data-ttu-id="b06d4-136">PSAuthorizationRuleAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b06d4-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="b06d4-137">筆記</span><span class="sxs-lookup"><span data-stu-id="b06d4-137">NOTES</span></span>

## <span data-ttu-id="b06d4-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="b06d4-138">RELATED LINKS</span></span>
