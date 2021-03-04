---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
ms.openlocfilehash: ac3b98089a3bbb710680269692685a32ef7adc03
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901661"
---
# <span data-ttu-id="c048c-101">New-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="c048c-101">New-AzServiceBusKey</span></span>

## <span data-ttu-id="c048c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c048c-102">SYNOPSIS</span></span>
<span data-ttu-id="c048c-103">重新產生 Service Bus 命名空間或佇列或主題的主要或次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="c048c-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="c048c-104">語法</span><span class="sxs-lookup"><span data-stu-id="c048c-104">SYNTAX</span></span>

### <span data-ttu-id="c048c-105">命名空間驗證RuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c048c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c048c-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c048c-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c048c-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c048c-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c048c-108">描述</span><span class="sxs-lookup"><span data-stu-id="c048c-108">DESCRIPTION</span></span>
<span data-ttu-id="c048c-109">**New-AzServiceBusKey** Cmdlet 會為指定的命名空間或佇列或主題及授權規則產生新的主要或次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="c048c-109">The **New-AzServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="c048c-110">例子</span><span class="sxs-lookup"><span data-stu-id="c048c-110">EXAMPLES</span></span>

### <span data-ttu-id="c048c-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="c048c-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="c048c-112">重新產生命名空間的主要或次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="c048c-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="c048c-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="c048c-113">Example 2</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="c048c-114">使用命名空間提供的 Key 值重新產生主要或次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="c048c-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="c048c-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="c048c-115">Example 3</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="c048c-116">重新產生佇列的主要或次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="c048c-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="c048c-117">範例 4</span><span class="sxs-lookup"><span data-stu-id="c048c-117">Example 4</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="c048c-118">使用佇列提供的 Key 值重新產生主要或次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="c048c-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="c048c-119">範例 5</span><span class="sxs-lookup"><span data-stu-id="c048c-119">Example 5</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="c048c-120">重新產生主題的主要或次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="c048c-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="c048c-121">範例 6</span><span class="sxs-lookup"><span data-stu-id="c048c-121">Example 6</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="c048c-122">使用主題提供的 Key 值重新產生主要或次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="c048c-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="c048c-123">參數</span><span class="sxs-lookup"><span data-stu-id="c048c-123">PARAMETERS</span></span>

### <span data-ttu-id="c048c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c048c-124">-DefaultProfile</span></span>
<span data-ttu-id="c048c-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c048c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c048c-126">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="c048c-126">-KeyValue</span></span>
<span data-ttu-id="c048c-127">用於簽署及驗證 SAS 權杖的 256 位基本編碼金鑰。</span><span class="sxs-lookup"><span data-stu-id="c048c-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c048c-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="c048c-128">-Name</span></span>
<span data-ttu-id="c048c-129">AuthorizationRule Name.</span><span class="sxs-lookup"><span data-stu-id="c048c-129">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="c048c-130">-命名空間</span><span class="sxs-lookup"><span data-stu-id="c048c-130">-Namespace</span></span>
<span data-ttu-id="c048c-131">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="c048c-131">Namespace Name</span></span>

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

### <span data-ttu-id="c048c-132">-佇列</span><span class="sxs-lookup"><span data-stu-id="c048c-132">-Queue</span></span>
<span data-ttu-id="c048c-133">佇列名稱</span><span class="sxs-lookup"><span data-stu-id="c048c-133">Queue Name</span></span>

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

### <span data-ttu-id="c048c-134">-重新產生金鑰</span><span class="sxs-lookup"><span data-stu-id="c048c-134">-RegenerateKey</span></span>
<span data-ttu-id="c048c-135">重新產生金鑰 - 'PrimaryKey'/'SecondaryKey'。</span><span class="sxs-lookup"><span data-stu-id="c048c-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c048c-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c048c-136">-ResourceGroupName</span></span>
<span data-ttu-id="c048c-137">資源組名</span><span class="sxs-lookup"><span data-stu-id="c048c-137">Resource Group Name</span></span>

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

### <span data-ttu-id="c048c-138">-主題</span><span class="sxs-lookup"><span data-stu-id="c048c-138">-Topic</span></span>
<span data-ttu-id="c048c-139">主題名稱</span><span class="sxs-lookup"><span data-stu-id="c048c-139">Topic Name</span></span>

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

### <span data-ttu-id="c048c-140">-確認</span><span class="sxs-lookup"><span data-stu-id="c048c-140">-Confirm</span></span>
<span data-ttu-id="c048c-141">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c048c-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c048c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c048c-142">-WhatIf</span></span>
<span data-ttu-id="c048c-143">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c048c-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c048c-144">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c048c-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c048c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c048c-145">CommonParameters</span></span>
<span data-ttu-id="c048c-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c048c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c048c-147">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c048c-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c048c-148">輸入</span><span class="sxs-lookup"><span data-stu-id="c048c-148">INPUTS</span></span>

### <span data-ttu-id="c048c-149">System.String</span><span class="sxs-lookup"><span data-stu-id="c048c-149">System.String</span></span>

## <span data-ttu-id="c048c-150">輸出</span><span class="sxs-lookup"><span data-stu-id="c048c-150">OUTPUTS</span></span>

### <span data-ttu-id="c048c-151">Microsoft.Azure.Commands.ServiceBus.models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="c048c-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="c048c-152">筆記</span><span class="sxs-lookup"><span data-stu-id="c048c-152">NOTES</span></span>

## <span data-ttu-id="c048c-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="c048c-153">RELATED LINKS</span></span>
