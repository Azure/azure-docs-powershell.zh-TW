---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicKey.md
ms.openlocfilehash: ed31934a75d9d6826a7e0464dccd43fd2d853daa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447989"
---
# <span data-ttu-id="8e90f-101">New-AzureRmServiceBusTopicKey</span><span class="sxs-lookup"><span data-stu-id="8e90f-101">New-AzureRmServiceBusTopicKey</span></span>

## <span data-ttu-id="8e90f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8e90f-102">SYNOPSIS</span></span>
<span data-ttu-id="8e90f-103">重新產生服務匯流排主題的主要或次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="8e90f-103">Regenerates the primary or secondary connection strings for the Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e90f-104">句法</span><span class="sxs-lookup"><span data-stu-id="8e90f-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopicKey [-ResourceGroup] <String> -Namespace <String> -Topic <String> -Name <String>
 [-RegenerateKeys] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e90f-105">說明</span><span class="sxs-lookup"><span data-stu-id="8e90f-105">DESCRIPTION</span></span>
<span data-ttu-id="8e90f-106">**新的-AzureRmServiceBusTopicKey** Cmdlet 會針對指定的服務匯流排主題和授權規則產生新的主要或次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="8e90f-106">The **New-AzureRmServiceBusTopicKey** cmdlet generates a new primary or secondary connection string for the specified Service Bus topic and authorization rule.</span></span>

## <span data-ttu-id="8e90f-107">示例</span><span class="sxs-lookup"><span data-stu-id="8e90f-107">EXAMPLES</span></span>

### <span data-ttu-id="8e90f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="8e90f-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="8e90f-109">重新生成命名空間的主要連接字串。</span><span class="sxs-lookup"><span data-stu-id="8e90f-109">Regenerates the primary connection string for the namespace.</span></span>

### <span data-ttu-id="8e90f-110">範例2</span><span class="sxs-lookup"><span data-stu-id="8e90f-110">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -RegenerateKeys SecondaryKey
```

<span data-ttu-id="8e90f-111">重新生成命名空間的次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="8e90f-111">Regenerates the secondary connection string for the namespace.</span></span>

## <span data-ttu-id="8e90f-112">參數</span><span class="sxs-lookup"><span data-stu-id="8e90f-112">PARAMETERS</span></span>

### <span data-ttu-id="8e90f-113">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="8e90f-113">-RegenerateKeys</span></span>
<span data-ttu-id="8e90f-114">指定是否要重新產生主要或次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="8e90f-114">Specifies whether to regenerate the primary or secondary keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e90f-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8e90f-115">-ResourceGroup</span></span>
<span data-ttu-id="8e90f-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e90f-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="8e90f-117">-確認</span><span class="sxs-lookup"><span data-stu-id="8e90f-117">-Confirm</span></span>
<span data-ttu-id="8e90f-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8e90f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e90f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e90f-119">-WhatIf</span></span>
<span data-ttu-id="8e90f-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8e90f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e90f-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e90f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e90f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e90f-122">-DefaultProfile</span></span>
<span data-ttu-id="8e90f-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8e90f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e90f-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="8e90f-124">-Name</span></span>
<span data-ttu-id="8e90f-125">授權規則名稱。</span><span class="sxs-lookup"><span data-stu-id="8e90f-125">Authorization Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e90f-126">-命名空間</span><span class="sxs-lookup"><span data-stu-id="8e90f-126">-Namespace</span></span>
<span data-ttu-id="8e90f-127">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="8e90f-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e90f-128">-主題</span><span class="sxs-lookup"><span data-stu-id="8e90f-128">-Topic</span></span>
<span data-ttu-id="8e90f-129">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="8e90f-129">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e90f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e90f-130">CommonParameters</span></span>
<span data-ttu-id="8e90f-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8e90f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e90f-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8e90f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e90f-133">輸入</span><span class="sxs-lookup"><span data-stu-id="8e90f-133">INPUTS</span></span>

### <span data-ttu-id="8e90f-134">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8e90f-134">-ResourceGroup</span></span>
 <span data-ttu-id="8e90f-135">System.object</span><span class="sxs-lookup"><span data-stu-id="8e90f-135">System.String</span></span>
 

### <span data-ttu-id="8e90f-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="8e90f-136">-NamespaceName</span></span>
 <span data-ttu-id="8e90f-137">System.object</span><span class="sxs-lookup"><span data-stu-id="8e90f-137">System.String</span></span>
 

### <span data-ttu-id="8e90f-138">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="8e90f-138">-AuthorizationRuleName</span></span>
 <span data-ttu-id="8e90f-139">System.object</span><span class="sxs-lookup"><span data-stu-id="8e90f-139">System.String</span></span>
 

### <span data-ttu-id="8e90f-140">-TopicName</span><span class="sxs-lookup"><span data-stu-id="8e90f-140">-TopicName</span></span>
 <span data-ttu-id="8e90f-141">System.object</span><span class="sxs-lookup"><span data-stu-id="8e90f-141">System.String</span></span>
 

### <span data-ttu-id="8e90f-142">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="8e90f-142">-RegenerateKeys</span></span>
 <span data-ttu-id="8e90f-143">System.object</span><span class="sxs-lookup"><span data-stu-id="8e90f-143">System.String</span></span>

## <span data-ttu-id="8e90f-144">輸出</span><span class="sxs-lookup"><span data-stu-id="8e90f-144">OUTPUTS</span></span>

### <span data-ttu-id="8e90f-145">ListKeysAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8e90f-145">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>
<span data-ttu-id="8e90f-146">PrimaryConnectionString： Endpoint = sb：//sb-example1.servicebus.windows.net/;SharedAccessKeyName = SBTopicAuthoRule1;SharedAccessKey = {SharedAccessKey 值};EntityPath = SB-Topi c_exampl1 SecondaryConnectionString： Endpoint = SB：//sb-example1.servicebus.windows.net/;SharedAccessKeyName = SBTopicAuthoRule1;SharedAccessKey = {SharedAccessKey 值};EntityPath = SB-Topi c_exampl1 PrimaryKey： {PrimaryKey 值} SecondaryKey： {SecondaryKey 值} KeyName： SBTopicAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="8e90f-146">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Topi c_exampl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Topi c_exampl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBTopicAuthoRule1</span></span>

## <span data-ttu-id="8e90f-147">筆記</span><span class="sxs-lookup"><span data-stu-id="8e90f-147">NOTES</span></span>

## <span data-ttu-id="8e90f-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e90f-148">RELATED LINKS</span></span>

