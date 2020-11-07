---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueKey.md
ms.openlocfilehash: 0a2bfe70e986b3ed92cef215cc23245216c0e961
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626218"
---
# <span data-ttu-id="e7878-101">New-AzureRmServiceBusQueueKey</span><span class="sxs-lookup"><span data-stu-id="e7878-101">New-AzureRmServiceBusQueueKey</span></span>

## <span data-ttu-id="e7878-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e7878-102">SYNOPSIS</span></span>
<span data-ttu-id="e7878-103">重新產生服務匯流排佇列的主要或次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="e7878-103">Regenerates the primary or secondary connection strings for the Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7878-104">句法</span><span class="sxs-lookup"><span data-stu-id="e7878-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueueKey [-ResourceGroup] <String> [-NamespaceName] <String> [-QueueName] <String>
 [-AuthorizationRuleName] <String> [-RegenerateKeys] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7878-105">說明</span><span class="sxs-lookup"><span data-stu-id="e7878-105">DESCRIPTION</span></span>
<span data-ttu-id="e7878-106">**新的-AzureRmServiceBusQueueKey** Cmdlet 會為指定的服務匯流排佇列和授權規則重新產生主要或次要的連線字串。</span><span class="sxs-lookup"><span data-stu-id="e7878-106">The **New-AzureRmServiceBusQueueKey** cmdlet regenerates the primary or secondary connection strings for the specified Service Bus queue and authorization rule.</span></span>

## <span data-ttu-id="e7878-107">示例</span><span class="sxs-lookup"><span data-stu-id="e7878-107">EXAMPLES</span></span>

### <span data-ttu-id="e7878-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e7878-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="e7878-109">重新生成命名空間的主要連接字串。</span><span class="sxs-lookup"><span data-stu-id="e7878-109">Regenerates the primary connection string for the namespace.</span></span>

### <span data-ttu-id="e7878-110">範例2</span><span class="sxs-lookup"><span data-stu-id="e7878-110">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -RegenerateKeys SecondaryKey
```

<span data-ttu-id="e7878-111">重新生成命名空間的次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="e7878-111">Regenerates the secondary connection string for the namespace.</span></span>

## <span data-ttu-id="e7878-112">參數</span><span class="sxs-lookup"><span data-stu-id="e7878-112">PARAMETERS</span></span>

### <span data-ttu-id="e7878-113">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="e7878-113">-AuthorizationRuleName</span></span>
<span data-ttu-id="e7878-114">授權規則名稱。</span><span class="sxs-lookup"><span data-stu-id="e7878-114">The authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7878-115">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="e7878-115">-NamespaceName</span></span>
<span data-ttu-id="e7878-116">服務匯流排命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="e7878-116">The Service Bus namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7878-117">-QueueName</span><span class="sxs-lookup"><span data-stu-id="e7878-117">-QueueName</span></span>
<span data-ttu-id="e7878-118">服務匯流排佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="e7878-118">The Service Bus queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7878-119">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="e7878-119">-RegenerateKeys</span></span>
<span data-ttu-id="e7878-120">指定是否要重新產生主要或次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="e7878-120">Specifies whether to regenerate the primary or secondary keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7878-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e7878-121">-ResourceGroup</span></span>
<span data-ttu-id="e7878-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7878-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="e7878-123">-確認</span><span class="sxs-lookup"><span data-stu-id="e7878-123">-Confirm</span></span>
<span data-ttu-id="e7878-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e7878-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7878-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7878-125">-WhatIf</span></span>
<span data-ttu-id="e7878-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e7878-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7878-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e7878-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7878-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7878-128">CommonParameters</span></span>
<span data-ttu-id="e7878-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e7878-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7878-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e7878-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7878-131">輸入</span><span class="sxs-lookup"><span data-stu-id="e7878-131">INPUTS</span></span>

### <span data-ttu-id="e7878-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e7878-132">-ResourceGroup</span></span>
 <span data-ttu-id="e7878-133">System.object</span><span class="sxs-lookup"><span data-stu-id="e7878-133">System.String</span></span>
 

### <span data-ttu-id="e7878-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="e7878-134">-NamespaceName</span></span>
 <span data-ttu-id="e7878-135">System.object</span><span class="sxs-lookup"><span data-stu-id="e7878-135">System.String</span></span>
 

### <span data-ttu-id="e7878-136">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="e7878-136">-AuthorizationRuleName</span></span>
 <span data-ttu-id="e7878-137">System.object</span><span class="sxs-lookup"><span data-stu-id="e7878-137">System.String</span></span>
 

### <span data-ttu-id="e7878-138">-QueueName</span><span class="sxs-lookup"><span data-stu-id="e7878-138">-QueueName</span></span>
 <span data-ttu-id="e7878-139">System.object</span><span class="sxs-lookup"><span data-stu-id="e7878-139">System.String</span></span>
 

### <span data-ttu-id="e7878-140">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="e7878-140">-RegenerateKeys</span></span>
 <span data-ttu-id="e7878-141">System.object</span><span class="sxs-lookup"><span data-stu-id="e7878-141">System.String</span></span>

## <span data-ttu-id="e7878-142">輸出</span><span class="sxs-lookup"><span data-stu-id="e7878-142">OUTPUTS</span></span>

### <span data-ttu-id="e7878-143">ResourceListKeys （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="e7878-143">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="e7878-144">PrimaryConnectionString： Endpoint = sb：//sb-example1.servicebus.windows.net/;SharedAccessKeyName = SBAuthoRule1;SharedAccessKey = {SharedAccessKey 值};EntityPath = SB-Queue_exa mpl1 SecondaryConnectionString： Endpoint = SB：//sb-example1.servicebus.windows.net/;SharedAccessKeyName = SBAuthoRule1;SharedAccessKey = {SharedAccessKey 值};EntityPath = SB-Queue_exa mpl1 PrimaryKey： {PrimaryKey 值} SecondaryKey： {SecondaryKey 值} KeyName： SBAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="e7878-144">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_exa mpl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_exa mpl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBAuthoRule1</span></span>

## <span data-ttu-id="e7878-145">筆記</span><span class="sxs-lookup"><span data-stu-id="e7878-145">NOTES</span></span>

## <span data-ttu-id="e7878-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="e7878-146">RELATED LINKS</span></span>

