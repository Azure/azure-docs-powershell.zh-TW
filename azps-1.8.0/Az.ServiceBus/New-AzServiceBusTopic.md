---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusTopic.md
ms.openlocfilehash: 8fe78fff4d297233ee322b58c426099f160b2990
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620620"
---
# <span data-ttu-id="ffd96-101">New-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="ffd96-101">New-AzServiceBusTopic</span></span>

## <span data-ttu-id="ffd96-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ffd96-102">SYNOPSIS</span></span>
<span data-ttu-id="ffd96-103">在指定的服務匯流排命名空間中建立新的服務匯流排主題。</span><span class="sxs-lookup"><span data-stu-id="ffd96-103">Creates a new Service Bus topic in  the specified Service Bus namespace.</span></span>

## <span data-ttu-id="ffd96-104">句法</span><span class="sxs-lookup"><span data-stu-id="ffd96-104">SYNTAX</span></span>

```
New-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -EnablePartitioning <Boolean> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DuplicateDetectionHistoryTimeWindow <String>] [-EnableBatchedOperations <Boolean>]
 [-EnableExpress <Boolean>] [-MaxSizeInMegabytes <Int64>] [-RequiresDuplicateDetection <Boolean>]
 [-SupportOrdering <Boolean>] [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffd96-105">說明</span><span class="sxs-lookup"><span data-stu-id="ffd96-105">DESCRIPTION</span></span>
<span data-ttu-id="ffd96-106">**新的-AzServiceBusTopic** Cmdlet 會在指定的服務匯流排命名空間中建立新的服務匯流排主題。</span><span class="sxs-lookup"><span data-stu-id="ffd96-106">The **New-AzServiceBusTopic** cmdlet creates a new Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="ffd96-107">示例</span><span class="sxs-lookup"><span data-stu-id="ffd96-107">EXAMPLES</span></span>

### <span data-ttu-id="ffd96-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ffd96-108">Example 1</span></span>
```
PS C:\> New-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -EnablePartitioning $True

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 11:51:24 PM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : False
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : True
UpdatedAt                           : 10/11/2018 11:51:24 PM
```

<span data-ttu-id="ffd96-109">`SB-Topic_exampl1`在指定的服務匯流排命名空間中建立新的服務匯流排主題 `SB-Example1` 。</span><span class="sxs-lookup"><span data-stu-id="ffd96-109">Creates a new Service Bus topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="ffd96-110">參數</span><span class="sxs-lookup"><span data-stu-id="ffd96-110">PARAMETERS</span></span>

### <span data-ttu-id="ffd96-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="ffd96-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="ffd96-112">指定將自動刪除主題之後的 [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) 空閒間隔時間。</span><span class="sxs-lookup"><span data-stu-id="ffd96-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval after which the topic is automatically deleted.</span></span> <span data-ttu-id="ffd96-113">最短持續時間為5分鐘。</span><span class="sxs-lookup"><span data-stu-id="ffd96-113">The minimum duration is 5 minutes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd96-114">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="ffd96-114">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="ffd96-115">指定郵件到期後的持續時間，從郵件傳送到服務匯流排時開始。</span><span class="sxs-lookup"><span data-stu-id="ffd96-115">Specifies the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd96-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffd96-116">-DefaultProfile</span></span>
<span data-ttu-id="ffd96-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ffd96-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffd96-118">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="ffd96-118">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="ffd96-119">指定 [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) 結構，該結構定義重複偵測歷程記錄的持續時間。</span><span class="sxs-lookup"><span data-stu-id="ffd96-119">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) structure that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="ffd96-120">預設值為10分鐘。</span><span class="sxs-lookup"><span data-stu-id="ffd96-120">The default value is 10 minutes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd96-121">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="ffd96-121">-EnableBatchedOperations</span></span>
<span data-ttu-id="ffd96-122">指出是否已啟用伺服器端批次作業。</span><span class="sxs-lookup"><span data-stu-id="ffd96-122">Indicates whether server-side batched operations are enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd96-123">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="ffd96-123">-EnableExpress</span></span>
<span data-ttu-id="ffd96-124">指出是否已啟用快速實體。</span><span class="sxs-lookup"><span data-stu-id="ffd96-124">Indicates whether Express Entities are enabled.</span></span> <span data-ttu-id="ffd96-125">快速佇列會將郵件暫時儲存在記憶體中，然後再將它寫入持久性儲存。</span><span class="sxs-lookup"><span data-stu-id="ffd96-125">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd96-126">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="ffd96-126">-EnablePartitioning</span></span>
<span data-ttu-id="ffd96-127">指定是否要讓主題能在多個郵件經紀人間劃分分區。</span><span class="sxs-lookup"><span data-stu-id="ffd96-127">Specifies whether to enable the topic to be partitioned across multiple message brokers.</span></span> 

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd96-128">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="ffd96-128">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="ffd96-129">主題的大小上限，以百萬位元組為單位，即為該主題所指派的記憶體大小。</span><span class="sxs-lookup"><span data-stu-id="ffd96-129">The maximum size of the topic in megabytes, which is the size of memory allocated for the topic.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd96-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="ffd96-130">-Name</span></span>
<span data-ttu-id="ffd96-131">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="ffd96-131">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd96-132">-命名空間</span><span class="sxs-lookup"><span data-stu-id="ffd96-132">-Namespace</span></span>
<span data-ttu-id="ffd96-133">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="ffd96-133">Namespace Name.</span></span>

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

### <span data-ttu-id="ffd96-134">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="ffd96-134">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="ffd96-135">指出主題是否需要重複偵測。</span><span class="sxs-lookup"><span data-stu-id="ffd96-135">Indicates whether the topic requires duplication detection.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd96-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffd96-136">-ResourceGroupName</span></span>
<span data-ttu-id="ffd96-137">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="ffd96-137">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd96-138">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="ffd96-138">-SizeInBytes</span></span>
<span data-ttu-id="ffd96-139">指定主題的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ffd96-139">Specifies the size of the topic in bytes.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd96-140">-SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="ffd96-140">-SupportOrdering</span></span>
<span data-ttu-id="ffd96-141">指出主題是否支援排序。</span><span class="sxs-lookup"><span data-stu-id="ffd96-141">Indicates whether the topic supports ordering.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd96-142">-確認</span><span class="sxs-lookup"><span data-stu-id="ffd96-142">-Confirm</span></span>
<span data-ttu-id="ffd96-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ffd96-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffd96-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffd96-144">-WhatIf</span></span>
<span data-ttu-id="ffd96-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ffd96-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffd96-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ffd96-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffd96-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffd96-147">CommonParameters</span></span>
<span data-ttu-id="ffd96-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ffd96-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffd96-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ffd96-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffd96-150">輸入</span><span class="sxs-lookup"><span data-stu-id="ffd96-150">INPUTS</span></span>

### <span data-ttu-id="ffd96-151">System.object</span><span class="sxs-lookup"><span data-stu-id="ffd96-151">System.String</span></span>

### <span data-ttu-id="ffd96-152">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ffd96-152">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ffd96-153">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ffd96-153">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ffd96-154">輸出</span><span class="sxs-lookup"><span data-stu-id="ffd96-154">OUTPUTS</span></span>

### <span data-ttu-id="ffd96-155">PSTopicAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ffd96-155">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="ffd96-156">筆記</span><span class="sxs-lookup"><span data-stu-id="ffd96-156">NOTES</span></span>

## <span data-ttu-id="ffd96-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="ffd96-157">RELATED LINKS</span></span>
