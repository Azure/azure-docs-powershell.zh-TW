---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
ms.openlocfilehash: a79afdbba1293c3340e499387b5df745d8b76228
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624284"
---
# <span data-ttu-id="9881e-101">New-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="9881e-101">New-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="9881e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9881e-102">SYNOPSIS</span></span>
<span data-ttu-id="9881e-103">在指定的服務匯流排命名空間中建立新的服務匯流排主題。</span><span class="sxs-lookup"><span data-stu-id="9881e-103">Creates a new Service Bus topic in  the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9881e-104">句法</span><span class="sxs-lookup"><span data-stu-id="9881e-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -EnablePartitioning <Boolean> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DuplicateDetectionHistoryTimeWindow <String>] [-EnableBatchedOperations <Boolean>]
 [-EnableExpress <Boolean>] [-MaxSizeInMegabytes <Int64>] [-RequiresDuplicateDetection <Boolean>]
 [-SupportOrdering <Boolean>] [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9881e-105">說明</span><span class="sxs-lookup"><span data-stu-id="9881e-105">DESCRIPTION</span></span>
<span data-ttu-id="9881e-106">**新的-AzureRmServiceBusTopic** Cmdlet 會在指定的服務匯流排命名空間中建立新的服務匯流排主題。</span><span class="sxs-lookup"><span data-stu-id="9881e-106">The **New-AzureRmServiceBusTopic** cmdlet creates a new Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="9881e-107">示例</span><span class="sxs-lookup"><span data-stu-id="9881e-107">EXAMPLES</span></span>

### <span data-ttu-id="9881e-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9881e-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -EnablePartitioning $True

Name                                : SB-Topic_exampl1
Id                                  : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S
                                      B-Topic_exampl1
Type                                : Microsoft.ServiceBus/Topic
AccessedAt                          : 
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 3:16:42 AM
CountDetails                        : 
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 16384
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 
SupportOrdering                     : False
UpdatedAt                           : 1/20/2017 3:16:43 AM

```
<span data-ttu-id="9881e-109">`SB-Topic_exampl1`在指定的服務匯流排命名空間中建立新的服務匯流排主題 `SB-Example1` 。</span><span class="sxs-lookup"><span data-stu-id="9881e-109">Creates a new Service Bus topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="9881e-110">參數</span><span class="sxs-lookup"><span data-stu-id="9881e-110">PARAMETERS</span></span>

### <span data-ttu-id="9881e-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="9881e-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="9881e-112">指定將自動刪除主題之後的 [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) 空閒間隔時間。</span><span class="sxs-lookup"><span data-stu-id="9881e-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval after which the topic is automatically deleted.</span></span> <span data-ttu-id="9881e-113">最短持續時間為5分鐘。</span><span class="sxs-lookup"><span data-stu-id="9881e-113">The minimum duration is 5 minutes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9881e-114">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="9881e-114">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="9881e-115">指定郵件到期後的持續時間，從郵件傳送到服務匯流排時開始。</span><span class="sxs-lookup"><span data-stu-id="9881e-115">Specifies the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9881e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9881e-116">-DefaultProfile</span></span>
<span data-ttu-id="9881e-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9881e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9881e-118">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="9881e-118">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="9881e-119">指定 [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) 結構，該結構定義重複偵測歷程記錄的持續時間。</span><span class="sxs-lookup"><span data-stu-id="9881e-119">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) structure that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="9881e-120">預設值為10分鐘。</span><span class="sxs-lookup"><span data-stu-id="9881e-120">The default value is 10 minutes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9881e-121">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="9881e-121">-EnableBatchedOperations</span></span>
<span data-ttu-id="9881e-122">指出是否已啟用伺服器端批次作業。</span><span class="sxs-lookup"><span data-stu-id="9881e-122">Indicates whether server-side batched operations are enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9881e-123">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="9881e-123">-EnableExpress</span></span>
<span data-ttu-id="9881e-124">指出是否已啟用快速實體。</span><span class="sxs-lookup"><span data-stu-id="9881e-124">Indicates whether Express Entities are enabled.</span></span> <span data-ttu-id="9881e-125">快速佇列會將郵件暫時儲存在記憶體中，然後再將它寫入持久性儲存。</span><span class="sxs-lookup"><span data-stu-id="9881e-125">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9881e-126">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="9881e-126">-EnablePartitioning</span></span>
<span data-ttu-id="9881e-127">指定是否要讓主題能在多個郵件經紀人間劃分分區。</span><span class="sxs-lookup"><span data-stu-id="9881e-127">Specifies whether to enable the topic to be partitioned across multiple message brokers.</span></span> 

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9881e-128">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="9881e-128">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="9881e-129">主題的大小上限，以百萬位元組為單位，即為該主題所指派的記憶體大小。</span><span class="sxs-lookup"><span data-stu-id="9881e-129">The maximum size of the topic in megabytes, which is the size of memory allocated for the topic.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9881e-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="9881e-130">-Name</span></span>
<span data-ttu-id="9881e-131">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="9881e-131">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9881e-132">-命名空間</span><span class="sxs-lookup"><span data-stu-id="9881e-132">-Namespace</span></span>
<span data-ttu-id="9881e-133">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="9881e-133">Namespace Name.</span></span>

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

### <span data-ttu-id="9881e-134">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="9881e-134">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="9881e-135">指出主題是否需要重複偵測。</span><span class="sxs-lookup"><span data-stu-id="9881e-135">Indicates whether the topic requires duplication detection.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9881e-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9881e-136">-ResourceGroupName</span></span>
<span data-ttu-id="9881e-137">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="9881e-137">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9881e-138">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="9881e-138">-SizeInBytes</span></span>
<span data-ttu-id="9881e-139">指定主題的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="9881e-139">Specifies the size of the topic in bytes.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9881e-140">-SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="9881e-140">-SupportOrdering</span></span>
<span data-ttu-id="9881e-141">指出主題是否支援排序。</span><span class="sxs-lookup"><span data-stu-id="9881e-141">Indicates whether the topic supports ordering.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9881e-142">-確認</span><span class="sxs-lookup"><span data-stu-id="9881e-142">-Confirm</span></span>
<span data-ttu-id="9881e-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9881e-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9881e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9881e-144">-WhatIf</span></span>
<span data-ttu-id="9881e-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9881e-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9881e-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9881e-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9881e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9881e-147">CommonParameters</span></span>
<span data-ttu-id="9881e-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9881e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9881e-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9881e-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9881e-150">輸入</span><span class="sxs-lookup"><span data-stu-id="9881e-150">INPUTS</span></span>

### <span data-ttu-id="9881e-151">System.object</span><span class="sxs-lookup"><span data-stu-id="9881e-151">System.String</span></span>
<span data-ttu-id="9881e-152">可為 Null \` \[ \[ 的1系統. Boolean、mscorlib、Version = 4.0.0.0、culture = 中性、PublicKeyToken = B77a5c561934e089 \] \] System。 Nullable \` 1 system.object、 \[ \[ mscorlib、Version = 4.0.0.0、culture = 中立、publickeytoken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="9881e-152">System.Nullable\`1\[\[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Nullable\`1\[\[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

### <span data-ttu-id="9881e-153">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9881e-153">-ResourceGroup</span></span>
 <span data-ttu-id="9881e-154">System.object</span><span class="sxs-lookup"><span data-stu-id="9881e-154">System.String</span></span>

### <span data-ttu-id="9881e-155">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="9881e-155">-NamespaceName</span></span>
 <span data-ttu-id="9881e-156">System.object</span><span class="sxs-lookup"><span data-stu-id="9881e-156">System.String</span></span>

### <span data-ttu-id="9881e-157">-TopicName</span><span class="sxs-lookup"><span data-stu-id="9881e-157">-TopicName</span></span>
 <span data-ttu-id="9881e-158">System.object</span><span class="sxs-lookup"><span data-stu-id="9881e-158">System.String</span></span>

### <span data-ttu-id="9881e-159">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="9881e-159">-EnablePartitioning</span></span>
 <span data-ttu-id="9881e-160">System.object？</span><span class="sxs-lookup"><span data-stu-id="9881e-160">System.Boolean?</span></span>

## <span data-ttu-id="9881e-161">輸出</span><span class="sxs-lookup"><span data-stu-id="9881e-161">OUTPUTS</span></span>

### <span data-ttu-id="9881e-162">PSTopicAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9881e-162">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="9881e-163">筆記</span><span class="sxs-lookup"><span data-stu-id="9881e-163">NOTES</span></span>

## <span data-ttu-id="9881e-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="9881e-164">RELATED LINKS</span></span>

