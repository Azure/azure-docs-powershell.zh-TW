---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
ms.openlocfilehash: beef1ab92a931f4f4041d9e9083712fe0b14f86b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93786789"
---
# <span data-ttu-id="e4e9c-101">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="e4e9c-101">Add-AzLogProfile</span></span>

## <span data-ttu-id="e4e9c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e4e9c-102">SYNOPSIS</span></span>
<span data-ttu-id="e4e9c-103">建立新的活動記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-103">Creates a new activity log profile.</span></span> <span data-ttu-id="e4e9c-104">此設定檔是用來將活動記錄封存至 Azure 儲存空間帳戶，或在相同訂閱中將它資料流程至 Azure 事件中樞。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

## <span data-ttu-id="e4e9c-105">句法</span><span class="sxs-lookup"><span data-stu-id="e4e9c-105">SYNTAX</span></span>

```
Add-AzLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4e9c-106">說明</span><span class="sxs-lookup"><span data-stu-id="e4e9c-106">DESCRIPTION</span></span>
<span data-ttu-id="e4e9c-107">**AzLogProfile** Cmdlet 會建立記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-107">The **Add-AzLogProfile** cmdlet creates a log profile.</span></span>
- <span data-ttu-id="e4e9c-108">僅支援 **儲存空間** 帳戶標準儲存空間帳戶 (premium 儲存空間帳戶不支援) 。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-108">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="e4e9c-109">它可能是 ARM 類型或傳統模式。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-109">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="e4e9c-110">如果它是記錄在儲存空間帳戶中，則儲存活動記錄的成本會以標準的標準儲存費率計費。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-110">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="e4e9c-111">每個訂閱只能有一個記錄 consequentially 每個訂閱只能使用一個儲存空間帳戶來匯出活動記錄。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-111">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 
- <span data-ttu-id="e4e9c-112">**事件中心** -每個訂閱只能有一個記錄設定檔 consequentially 每個訂閱只能使用一個事件中樞來匯出活動記錄。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-112">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="e4e9c-113">如果活動記錄是流入事件中樞，則會套用標準事件中樞定價。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-113">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> <span data-ttu-id="e4e9c-114">在活動記錄檔中，事件可與區域或「全域」相關。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-114">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="e4e9c-115">[全域] 是指這些事件是地區 agnostics，且與區域無關，事實上大部分事件都屬於這種類別。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-115">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="e4e9c-116">如果活動記錄設定檔是從入口網站進行設定，則會將 [全域] 與您在使用者介面中選取的任何其他區域一起隱出。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-116">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="e4e9c-117">使用 Cmdlet 時，"Global" 是「全域」的位置，必須從任何其他區域明確提及。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-117">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 
<span data-ttu-id="e4e9c-118">**注意** ：- **在位置中設定「全域」失敗，會導致大部分的活動記錄不會匯出。**</span><span class="sxs-lookup"><span data-stu-id="e4e9c-118">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> <span data-ttu-id="e4e9c-119">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際建立、修改或移除資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-119">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="e4e9c-120">示例</span><span class="sxs-lookup"><span data-stu-id="e4e9c-120">EXAMPLES</span></span>

### <span data-ttu-id="e4e9c-121">範例1：新增記錄設定檔，將符合位置條件的活動記錄匯出至儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="e4e9c-121">Example 1 : Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```
Add-AzLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="e4e9c-122">參數</span><span class="sxs-lookup"><span data-stu-id="e4e9c-122">PARAMETERS</span></span>

### <span data-ttu-id="e4e9c-123">-類別</span><span class="sxs-lookup"><span data-stu-id="e4e9c-123">-Category</span></span>
<span data-ttu-id="e4e9c-124">指定類別清單。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-124">Specifies the list of categories.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e9c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4e9c-125">-DefaultProfile</span></span>
<span data-ttu-id="e4e9c-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e4e9c-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4e9c-127">-位置</span><span class="sxs-lookup"><span data-stu-id="e4e9c-127">-Location</span></span>
<span data-ttu-id="e4e9c-128">指定記錄設定檔的位置。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-128">Specifies the location of the log profile.</span></span>
<span data-ttu-id="e4e9c-129">有效值：請在下方執行 Cmdlet，以取得最新的位置清單。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-129">Valid values: Run below cmdlet to get the latest list of locations.</span></span> <span data-ttu-id="e4e9c-130">Get-AzLocation |選取 DisplayName</span><span class="sxs-lookup"><span data-stu-id="e4e9c-130">Get-AzLocation | Select DisplayName</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e9c-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="e4e9c-131">-Name</span></span>
<span data-ttu-id="e4e9c-132">指定設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-132">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e9c-133">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e4e9c-133">-RetentionInDays</span></span>
<span data-ttu-id="e4e9c-134">指定保留原則（以天為單位）。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-134">Specifies the retention policy, in days.</span></span> <span data-ttu-id="e4e9c-135">這是記錄在指定的儲存空間帳戶中保留的天數。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-135">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="e4e9c-136">若要永久保留資料，請將此設定為 **0** 。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-136">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="e4e9c-137">如果沒有指定，則預設為 **0** 。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-137">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="e4e9c-138">一般標準儲存或活動中心帳單費用會套用到資料保留。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-138">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e9c-139">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="e4e9c-139">-ServiceBusRuleId</span></span>
<span data-ttu-id="e4e9c-140">指定服務匯流排規則的 ID。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-140">Specifies the ID of the Service Bus rule.</span></span>

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

### <span data-ttu-id="e4e9c-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e4e9c-141">-StorageAccountId</span></span>
<span data-ttu-id="e4e9c-142">指定儲存空間帳戶的 ID。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-142">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="e4e9c-143">[識別碼] 是儲存帳戶的完全合格的資源識別碼（例如</span><span class="sxs-lookup"><span data-stu-id="e4e9c-143">ID is the fully qualified Resource ID of the storage account for example</span></span>  
<span data-ttu-id="e4e9c-144">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="e4e9c-144">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

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

### <span data-ttu-id="e4e9c-145">-確認</span><span class="sxs-lookup"><span data-stu-id="e4e9c-145">-Confirm</span></span>
<span data-ttu-id="e4e9c-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4e9c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4e9c-147">-WhatIf</span></span>
<span data-ttu-id="e4e9c-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4e9c-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4e9c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4e9c-150">CommonParameters</span></span>
<span data-ttu-id="e4e9c-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4e9c-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4e9c-153">輸入</span><span class="sxs-lookup"><span data-stu-id="e4e9c-153">INPUTS</span></span>

### <span data-ttu-id="e4e9c-154">System.object</span><span class="sxs-lookup"><span data-stu-id="e4e9c-154">System.String</span></span>

### <span data-ttu-id="e4e9c-155">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e4e9c-155">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e4e9c-156">[System.object]。清單 ' 1 [CoreLib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e4e9c-156">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e4e9c-157">輸出</span><span class="sxs-lookup"><span data-stu-id="e4e9c-157">OUTPUTS</span></span>

### <span data-ttu-id="e4e9c-158">PSLogProfile 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="e4e9c-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="e4e9c-159">筆記</span><span class="sxs-lookup"><span data-stu-id="e4e9c-159">NOTES</span></span>

## <span data-ttu-id="e4e9c-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="e4e9c-160">RELATED LINKS</span></span>

[<span data-ttu-id="e4e9c-161">AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="e4e9c-161">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)

[<span data-ttu-id="e4e9c-162">移除-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="e4e9c-162">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


