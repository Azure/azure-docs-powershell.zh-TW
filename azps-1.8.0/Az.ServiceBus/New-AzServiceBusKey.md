---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
ms.openlocfilehash: 46a3551e309504d9938359a0fed4d37860fcb524
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620631"
---
# <span data-ttu-id="f6955-101">New-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="f6955-101">New-AzServiceBusKey</span></span>

## <span data-ttu-id="f6955-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6955-102">SYNOPSIS</span></span>
<span data-ttu-id="f6955-103">重新生成服務匯流排命名空間或佇列或主題的主要或次要連線字串。</span><span class="sxs-lookup"><span data-stu-id="f6955-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="f6955-104">句法</span><span class="sxs-lookup"><span data-stu-id="f6955-104">SYNTAX</span></span>

### <span data-ttu-id="f6955-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f6955-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f6955-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f6955-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f6955-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f6955-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f6955-108">說明</span><span class="sxs-lookup"><span data-stu-id="f6955-108">DESCRIPTION</span></span>
<span data-ttu-id="f6955-109">**新的-AzServiceBusKey** Cmdlet 會針對指定的命名空間或佇列或主題和授權規則產生新的主要或次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="f6955-109">The **New-AzServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="f6955-110">示例</span><span class="sxs-lookup"><span data-stu-id="f6955-110">EXAMPLES</span></span>

### <span data-ttu-id="f6955-111">範例1</span><span class="sxs-lookup"><span data-stu-id="f6955-111">Example 1</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="f6955-112">重新生成命名空間的主要或次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="f6955-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="f6955-113">範例1。1</span><span class="sxs-lookup"><span data-stu-id="f6955-113">Example 1.1</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="f6955-114">重新產生主要或次要連接字串，並提供命名空間的提供鍵值。</span><span class="sxs-lookup"><span data-stu-id="f6955-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="f6955-115">範例2</span><span class="sxs-lookup"><span data-stu-id="f6955-115">Example 2</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="f6955-116">重新產生佇列的主要或次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="f6955-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="f6955-117">範例2。2</span><span class="sxs-lookup"><span data-stu-id="f6955-117">Example 2.2</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="f6955-118">使用為佇列提供的鍵值重新產生主要或次要的連線字串。</span><span class="sxs-lookup"><span data-stu-id="f6955-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="f6955-119">範例3</span><span class="sxs-lookup"><span data-stu-id="f6955-119">Example 3</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="f6955-120">重新產生主題的主要或次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="f6955-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="f6955-121">範例3。1</span><span class="sxs-lookup"><span data-stu-id="f6955-121">Example 3.1</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="f6955-122">重新產生主要或次要連線字串，並提供主題的鍵值。</span><span class="sxs-lookup"><span data-stu-id="f6955-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="f6955-123">參數</span><span class="sxs-lookup"><span data-stu-id="f6955-123">PARAMETERS</span></span>

### <span data-ttu-id="f6955-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6955-124">-DefaultProfile</span></span>
<span data-ttu-id="f6955-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6955-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6955-126">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="f6955-126">-KeyValue</span></span>
<span data-ttu-id="f6955-127">用於簽署及驗證 SAS 權杖的 base64 編碼256位金鑰。</span><span class="sxs-lookup"><span data-stu-id="f6955-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="f6955-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="f6955-128">-Name</span></span>
<span data-ttu-id="f6955-129">AuthorizationRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="f6955-129">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="f6955-130">-命名空間</span><span class="sxs-lookup"><span data-stu-id="f6955-130">-Namespace</span></span>
<span data-ttu-id="f6955-131">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="f6955-131">Namespace Name</span></span>

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

### <span data-ttu-id="f6955-132">-佇列</span><span class="sxs-lookup"><span data-stu-id="f6955-132">-Queue</span></span>
<span data-ttu-id="f6955-133">佇列名稱</span><span class="sxs-lookup"><span data-stu-id="f6955-133">Queue Name</span></span>

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

### <span data-ttu-id="f6955-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="f6955-134">-RegenerateKey</span></span>
<span data-ttu-id="f6955-135">重新產生按鍵-"PrimaryKey"/"SecondaryKey"。</span><span class="sxs-lookup"><span data-stu-id="f6955-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="f6955-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6955-136">-ResourceGroupName</span></span>
<span data-ttu-id="f6955-137">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="f6955-137">Resource Group Name</span></span>

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

### <span data-ttu-id="f6955-138">-主題</span><span class="sxs-lookup"><span data-stu-id="f6955-138">-Topic</span></span>
<span data-ttu-id="f6955-139">主題名稱</span><span class="sxs-lookup"><span data-stu-id="f6955-139">Topic Name</span></span>

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

### <span data-ttu-id="f6955-140">-確認</span><span class="sxs-lookup"><span data-stu-id="f6955-140">-Confirm</span></span>
<span data-ttu-id="f6955-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f6955-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6955-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6955-142">-WhatIf</span></span>
<span data-ttu-id="f6955-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f6955-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6955-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6955-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6955-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6955-145">CommonParameters</span></span>
<span data-ttu-id="f6955-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6955-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6955-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f6955-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6955-148">輸入</span><span class="sxs-lookup"><span data-stu-id="f6955-148">INPUTS</span></span>

### <span data-ttu-id="f6955-149">System.object</span><span class="sxs-lookup"><span data-stu-id="f6955-149">System.String</span></span>

## <span data-ttu-id="f6955-150">輸出</span><span class="sxs-lookup"><span data-stu-id="f6955-150">OUTPUTS</span></span>

### <span data-ttu-id="f6955-151">PSListKeysAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f6955-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="f6955-152">筆記</span><span class="sxs-lookup"><span data-stu-id="f6955-152">NOTES</span></span>

## <span data-ttu-id="f6955-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6955-153">RELATED LINKS</span></span>