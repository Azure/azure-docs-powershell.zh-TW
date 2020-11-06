---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: e5a4886eef132f0e48c146fa70889dfa283489b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447649"
---
# <span data-ttu-id="b0f07-101">Get-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b0f07-101">Get-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="b0f07-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b0f07-102">SYNOPSIS</span></span>
<span data-ttu-id="b0f07-103">針對指定的命名空間或佇列或主題或 (GeoDR 設定的別名，取得指定授權規則的描述) 。</span><span class="sxs-lookup"><span data-stu-id="b0f07-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 


[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0f07-104">句法</span><span class="sxs-lookup"><span data-stu-id="b0f07-104">SYNTAX</span></span>

### <span data-ttu-id="b0f07-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b0f07-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0f07-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b0f07-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0f07-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b0f07-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0f07-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="b0f07-108">AliasAuthoRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String>
 [-AliasName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0f07-109">說明</span><span class="sxs-lookup"><span data-stu-id="b0f07-109">DESCRIPTION</span></span>
<span data-ttu-id="b0f07-110">**AzureRmServiceBusAuthorizationRule** Cmdlet 會在指定的命名空間或佇列或主題或主題或主題或主題或別名中取得指定授權規則的描述，) 的 [ (GeoDR 設定]。</span><span class="sxs-lookup"><span data-stu-id="b0f07-110">The **Get-AzureRmServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="b0f07-111">示例</span><span class="sxs-lookup"><span data-stu-id="b0f07-111">EXAMPLES</span></span>

### <span data-ttu-id="b0f07-112">範例1</span><span class="sxs-lookup"><span data-stu-id="b0f07-112">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="b0f07-113">針對指定的命名空間傳回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="b0f07-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="b0f07-114">範例2</span><span class="sxs-lookup"><span data-stu-id="b0f07-114">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="b0f07-115">針對指定的佇列傳回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="b0f07-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="b0f07-116">範例3</span><span class="sxs-lookup"><span data-stu-id="b0f07-116">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="b0f07-117">針對指定的主題，傳回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="b0f07-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="b0f07-118">範例4</span><span class="sxs-lookup"><span data-stu-id="b0f07-118">Example 4</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="b0f07-119">針對指定的命名空間和別名傳回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="b0f07-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="b0f07-120">參數</span><span class="sxs-lookup"><span data-stu-id="b0f07-120">PARAMETERS</span></span>

### <span data-ttu-id="b0f07-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="b0f07-121">-AliasName</span></span>
<span data-ttu-id="b0f07-122">GeoDR 配置名稱</span><span class="sxs-lookup"><span data-stu-id="b0f07-122">GeoDR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0f07-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0f07-123">-DefaultProfile</span></span>
<span data-ttu-id="b0f07-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b0f07-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0f07-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="b0f07-125">-Name</span></span>
<span data-ttu-id="b0f07-126">AuthorizationRule 名稱</span><span class="sxs-lookup"><span data-stu-id="b0f07-126">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0f07-127">-命名空間</span><span class="sxs-lookup"><span data-stu-id="b0f07-127">-Namespace</span></span>
<span data-ttu-id="b0f07-128">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="b0f07-128">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0f07-129">-佇列</span><span class="sxs-lookup"><span data-stu-id="b0f07-129">-Queue</span></span>
<span data-ttu-id="b0f07-130">佇列名稱</span><span class="sxs-lookup"><span data-stu-id="b0f07-130">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0f07-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0f07-131">-ResourceGroupName</span></span>
<span data-ttu-id="b0f07-132">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="b0f07-132">Resource Group Name</span></span>

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

### <span data-ttu-id="b0f07-133">-主題</span><span class="sxs-lookup"><span data-stu-id="b0f07-133">-Topic</span></span>
<span data-ttu-id="b0f07-134">主題名稱</span><span class="sxs-lookup"><span data-stu-id="b0f07-134">Topic Name</span></span>

```yaml
Type: String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0f07-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0f07-135">CommonParameters</span></span>
<span data-ttu-id="b0f07-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b0f07-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b0f07-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b0f07-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0f07-138">輸入</span><span class="sxs-lookup"><span data-stu-id="b0f07-138">INPUTS</span></span>

### <span data-ttu-id="b0f07-139">System.object</span><span class="sxs-lookup"><span data-stu-id="b0f07-139">System.String</span></span>


## <span data-ttu-id="b0f07-140">輸出</span><span class="sxs-lookup"><span data-stu-id="b0f07-140">OUTPUTS</span></span>

### <span data-ttu-id="b0f07-141">[System.object]。清單 ' 1 [0.5.0.0，PSSharedAccessAuthorizationRuleAttributes，，版本 =，Culture = 中性，PublicKeyToken = null]」））。）</span><span class="sxs-lookup"><span data-stu-id="b0f07-141">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="b0f07-142">筆記</span><span class="sxs-lookup"><span data-stu-id="b0f07-142">NOTES</span></span>

## <span data-ttu-id="b0f07-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="b0f07-143">RELATED LINKS</span></span>
