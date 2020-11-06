---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 333e3eeaaf7655c78d557eb104fa4a349a0c05e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446043"
---
# <span data-ttu-id="7e4ba-101">Get-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7e4ba-101">Get-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="7e4ba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7e4ba-102">SYNOPSIS</span></span>
<span data-ttu-id="7e4ba-103">針對特定的中繼實體 (Namespace/WcfRelay/HybridConnection) ，取得指定授權規則的描述。</span><span class="sxs-lookup"><span data-stu-id="7e4ba-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e4ba-104">句法</span><span class="sxs-lookup"><span data-stu-id="7e4ba-104">SYNTAX</span></span>

### <span data-ttu-id="7e4ba-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7e4ba-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e4ba-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7e4ba-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e4ba-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7e4ba-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e4ba-108">說明</span><span class="sxs-lookup"><span data-stu-id="7e4ba-108">DESCRIPTION</span></span>
<span data-ttu-id="7e4ba-109">**AzureRmRelayAuthorizationRule** Cmdlet 會在指定的中繼實體中取得指定授權規則的描述， (命名空間/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="7e4ba-109">The **Get-AzureRmRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="7e4ba-110">示例</span><span class="sxs-lookup"><span data-stu-id="7e4ba-110">EXAMPLES</span></span>

### <span data-ttu-id="7e4ba-111">範例 1-命名空間</span><span class="sxs-lookup"><span data-stu-id="7e4ba-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="7e4ba-112">針對指定的命名空間傳回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="7e4ba-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="7e4ba-113">範例 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="7e4ba-113">Example 2 - WcfRelay</span></span>
```
PS C:\>Get-AzureRmWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
```

<span data-ttu-id="7e4ba-114">針對指定的 WcfRelay 傳回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="7e4ba-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="7e4ba-115">範例 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="7e4ba-115">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="7e4ba-116">針對指定的 HybridConnection 傳回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="7e4ba-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="7e4ba-117">參數</span><span class="sxs-lookup"><span data-stu-id="7e4ba-117">PARAMETERS</span></span>

### <span data-ttu-id="7e4ba-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e4ba-118">-DefaultProfile</span></span>
<span data-ttu-id="7e4ba-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7e4ba-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e4ba-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="7e4ba-120">-HybridConnection</span></span>
<span data-ttu-id="7e4ba-121">HybridConnection [名稱]。</span><span class="sxs-lookup"><span data-stu-id="7e4ba-121">HybridConnection Name.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e4ba-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="7e4ba-122">-Name</span></span>
<span data-ttu-id="7e4ba-123">AuthorizationRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="7e4ba-123">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e4ba-124">-命名空間</span><span class="sxs-lookup"><span data-stu-id="7e4ba-124">-Namespace</span></span>
<span data-ttu-id="7e4ba-125">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="7e4ba-125">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e4ba-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e4ba-126">-ResourceGroupName</span></span>
<span data-ttu-id="7e4ba-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="7e4ba-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e4ba-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="7e4ba-128">-WcfRelay</span></span>
<span data-ttu-id="7e4ba-129">WcfRelay [名稱]。</span><span class="sxs-lookup"><span data-stu-id="7e4ba-129">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e4ba-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e4ba-130">CommonParameters</span></span>
<span data-ttu-id="7e4ba-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7e4ba-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e4ba-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7e4ba-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e4ba-133">輸入</span><span class="sxs-lookup"><span data-stu-id="7e4ba-133">INPUTS</span></span>

### <span data-ttu-id="7e4ba-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e4ba-134">-ResourceGroupName</span></span>
 <span data-ttu-id="7e4ba-135">System.object</span><span class="sxs-lookup"><span data-stu-id="7e4ba-135">System.String</span></span> 

### <span data-ttu-id="7e4ba-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="7e4ba-136">-NamespaceName</span></span>
 <span data-ttu-id="7e4ba-137">System.object</span><span class="sxs-lookup"><span data-stu-id="7e4ba-137">System.String</span></span> 
 

### <span data-ttu-id="7e4ba-138">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="7e4ba-138">-HybridConnectionsName</span></span>
 <span data-ttu-id="7e4ba-139">System.object</span><span class="sxs-lookup"><span data-stu-id="7e4ba-139">System.String</span></span> 

### <span data-ttu-id="7e4ba-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="7e4ba-140">-WcfRelayName</span></span>
 <span data-ttu-id="7e4ba-141">System.object</span><span class="sxs-lookup"><span data-stu-id="7e4ba-141">System.String</span></span> 

### <span data-ttu-id="7e4ba-142">-名稱</span><span class="sxs-lookup"><span data-stu-id="7e4ba-142">-Name</span></span>
 <span data-ttu-id="7e4ba-143">System.object</span><span class="sxs-lookup"><span data-stu-id="7e4ba-143">System.String</span></span>

## <span data-ttu-id="7e4ba-144">輸出</span><span class="sxs-lookup"><span data-stu-id="7e4ba-144">OUTPUTS</span></span>

### <span data-ttu-id="7e4ba-145">[System.object]. 清單 ' 1 [AuthorizationRuleAttributes，0.1.0.0，#.. 繼電器，版本 =，Culture = 中性，PublicKeyToken = null]]。</span><span class="sxs-lookup"><span data-stu-id="7e4ba-145">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="7e4ba-146">範例 1-命名空間</span><span class="sxs-lookup"><span data-stu-id="7e4ba-146">Example 1 - Namespace</span></span>
<span data-ttu-id="7e4ba-147">權利： {聆聽，Send} Name： AuthoRule1 類型： Microsoft. 繼電器/AuthorizationRules Id：/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut hoRule1</span><span class="sxs-lookup"><span data-stu-id="7e4ba-147">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut hoRule1</span></span>

### <span data-ttu-id="7e4ba-148">範例 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="7e4ba-148">Example 2 - WcfRelay</span></span>
<span data-ttu-id="7e4ba-149">權利： {聆聽，傳送} 名稱： AuthoRule1 類型： Microsoft. 繼電器/AuthorizationRules Id：/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay 1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="7e4ba-149">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay 1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="7e4ba-150">範例 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="7e4ba-150">Example 3 - HybridConnection</span></span>
<span data-ttu-id="7e4ba-151">許可權： {偵聽，傳送} 名稱： AuthoRule1 類型： Microsoft. 中繼/AuthorizationRules Id：/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test HybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="7e4ba-151">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test HybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="7e4ba-152">筆記</span><span class="sxs-lookup"><span data-stu-id="7e4ba-152">NOTES</span></span>

## <span data-ttu-id="7e4ba-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="7e4ba-153">RELATED LINKS</span></span>

