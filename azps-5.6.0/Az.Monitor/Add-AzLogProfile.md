---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/powershell/module/az.monitor/add-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
ms.openlocfilehash: a5d60cbda668e963793dbb350950ea0e85812892
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909002"
---
# <span data-ttu-id="db9b3-101">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="db9b3-101">Add-AzLogProfile</span></span>

## <span data-ttu-id="db9b3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="db9b3-102">SYNOPSIS</span></span>
<span data-ttu-id="db9b3-103">建立新活動記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="db9b3-103">Creates a new activity log profile.</span></span> <span data-ttu-id="db9b3-104">此設定檔可用來將活動記錄存檔至 Azure 儲存空間帳戶，或串流至同一訂閱中的 Azure 事件中心。</span><span class="sxs-lookup"><span data-stu-id="db9b3-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

## <span data-ttu-id="db9b3-105">語法</span><span class="sxs-lookup"><span data-stu-id="db9b3-105">SYNTAX</span></span>

```
Add-AzLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db9b3-106">描述</span><span class="sxs-lookup"><span data-stu-id="db9b3-106">DESCRIPTION</span></span>
<span data-ttu-id="db9b3-107">**Add-AzLogProfile** Cmdlet 會建立記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="db9b3-107">The **Add-AzLogProfile** cmdlet creates a log profile.</span></span>
- <span data-ttu-id="db9b3-108">**儲存空間帳戶** - 僅支援 (儲存空間帳戶或進) 帳戶。</span><span class="sxs-lookup"><span data-stu-id="db9b3-108">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="db9b3-109">它可以是 ARM 類型或傳統型。</span><span class="sxs-lookup"><span data-stu-id="db9b3-109">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="db9b3-110">如果記錄到儲存空間帳戶，儲存活動記錄的成本會以標準儲存費率計費。</span><span class="sxs-lookup"><span data-stu-id="db9b3-110">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="db9b3-111">每個訂閱可能只有一個記錄設定檔，因此每個訂閱只能使用一個儲存空間帳戶來匯出活動記錄。</span><span class="sxs-lookup"><span data-stu-id="db9b3-111">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 
- <span data-ttu-id="db9b3-112">**事件中樞** - 每個訂閱可能只有一個記錄設定檔，因此每個訂閱只能使用一個事件中樞來匯出活動記錄。</span><span class="sxs-lookup"><span data-stu-id="db9b3-112">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="db9b3-113">如果活動記錄串流至事件中樞，將會適用標準事件中樞定價。</span><span class="sxs-lookup"><span data-stu-id="db9b3-113">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> <span data-ttu-id="db9b3-114">在活動記錄中，事件可以與區域相關，或可能是「全域」。</span><span class="sxs-lookup"><span data-stu-id="db9b3-114">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="db9b3-115">全域基本上表示這些事件是區域不可知的，而且與區域無關，事實上，大部分的事件屬於這個類別。</span><span class="sxs-lookup"><span data-stu-id="db9b3-115">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="db9b3-116">如果活動記錄設定檔是從入口網站設定，它會隱含地加上 "Global" 以及使用者介面中選取的其他任何區域。</span><span class="sxs-lookup"><span data-stu-id="db9b3-116">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="db9b3-117">使用 Cmdlet 時，必須明確提及「全域」位置與任何其他區域。</span><span class="sxs-lookup"><span data-stu-id="db9b3-117">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 
<span data-ttu-id="db9b3-118">**注意** ：在位置中未設定「全域」會導致大部分 **的活動記錄無法匯出。**</span><span class="sxs-lookup"><span data-stu-id="db9b3-118">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> <span data-ttu-id="db9b3-119">此 Cmdlet 實做 ShouldProcess 模式，即實際建立、修改或移除資源之前，可能會向使用者要求確認。</span><span class="sxs-lookup"><span data-stu-id="db9b3-119">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="db9b3-120">例子</span><span class="sxs-lookup"><span data-stu-id="db9b3-120">EXAMPLES</span></span>

### <span data-ttu-id="db9b3-121">範例 1：新增記錄設定檔，將符合位置條件的活動記錄匯出至儲存帳戶</span><span class="sxs-lookup"><span data-stu-id="db9b3-121">Example 1: Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```powershell
Add-AzLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

### <span data-ttu-id="db9b3-122">範例 2</span><span class="sxs-lookup"><span data-stu-id="db9b3-122">Example 2</span></span>

<span data-ttu-id="db9b3-123">建立新活動記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="db9b3-123">Creates a new activity log profile.</span></span> <span data-ttu-id="db9b3-124"> (自動) </span><span class="sxs-lookup"><span data-stu-id="db9b3-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Add-AzLogProfile -Location 'Global' -Name ExportLogProfile -RetentionInDays <Int32> -ServiceBusRuleId <String> -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="db9b3-125">參數</span><span class="sxs-lookup"><span data-stu-id="db9b3-125">PARAMETERS</span></span>

### <span data-ttu-id="db9b3-126">-類別</span><span class="sxs-lookup"><span data-stu-id="db9b3-126">-Category</span></span>
<span data-ttu-id="db9b3-127">指定類別清單。</span><span class="sxs-lookup"><span data-stu-id="db9b3-127">Specifies the list of categories.</span></span>

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

### <span data-ttu-id="db9b3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db9b3-128">-DefaultProfile</span></span>
<span data-ttu-id="db9b3-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="db9b3-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db9b3-130">-位置</span><span class="sxs-lookup"><span data-stu-id="db9b3-130">-Location</span></span>
<span data-ttu-id="db9b3-131">指定記錄檔的位置。</span><span class="sxs-lookup"><span data-stu-id="db9b3-131">Specifies the location of the log profile.</span></span>
<span data-ttu-id="db9b3-132">有效值：在 Cmdlet 下方執行以取得最新的位置清單。</span><span class="sxs-lookup"><span data-stu-id="db9b3-132">Valid values: Run below cmdlet to get the latest list of locations.</span></span> <span data-ttu-id="db9b3-133">Get-AzLocation |選取 DisplayName</span><span class="sxs-lookup"><span data-stu-id="db9b3-133">Get-AzLocation | Select DisplayName</span></span>

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

### <span data-ttu-id="db9b3-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="db9b3-134">-Name</span></span>
<span data-ttu-id="db9b3-135">指定設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="db9b3-135">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="db9b3-136">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="db9b3-136">-RetentionInDays</span></span>
<span data-ttu-id="db9b3-137">指定保留政策 ，以天數表示。</span><span class="sxs-lookup"><span data-stu-id="db9b3-137">Specifies the retention policy, in days.</span></span> <span data-ttu-id="db9b3-138">這是記錄在指定的儲存帳戶中保留的天數。</span><span class="sxs-lookup"><span data-stu-id="db9b3-138">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="db9b3-139">若要永遠保留資料，請設為 **0。**</span><span class="sxs-lookup"><span data-stu-id="db9b3-139">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="db9b3-140">如果未指定，則預設值為 **0。**</span><span class="sxs-lookup"><span data-stu-id="db9b3-140">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="db9b3-141">一般標準儲存空間或活動中心帳單費率將適用于資料保留。</span><span class="sxs-lookup"><span data-stu-id="db9b3-141">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

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

### <span data-ttu-id="db9b3-142">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="db9b3-142">-ServiceBusRuleId</span></span>
<span data-ttu-id="db9b3-143">指定服務母線規則的識別碼。</span><span class="sxs-lookup"><span data-stu-id="db9b3-143">Specifies the ID of the Service Bus rule.</span></span>

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

### <span data-ttu-id="db9b3-144">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="db9b3-144">-StorageAccountId</span></span>
<span data-ttu-id="db9b3-145">指定儲存空間帳戶的識別碼。</span><span class="sxs-lookup"><span data-stu-id="db9b3-145">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="db9b3-146">識別碼是儲存帳戶的完全合格的資源識別碼，例如</span><span class="sxs-lookup"><span data-stu-id="db9b3-146">ID is the fully qualified Resource ID of the storage account for example</span></span>  
<span data-ttu-id="db9b3-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="db9b3-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

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

### <span data-ttu-id="db9b3-148">-確認</span><span class="sxs-lookup"><span data-stu-id="db9b3-148">-Confirm</span></span>
<span data-ttu-id="db9b3-149">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="db9b3-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db9b3-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db9b3-150">-WhatIf</span></span>
<span data-ttu-id="db9b3-151">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="db9b3-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db9b3-152">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db9b3-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db9b3-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db9b3-153">CommonParameters</span></span>
<span data-ttu-id="db9b3-154">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="db9b3-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db9b3-155">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db9b3-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db9b3-156">輸入</span><span class="sxs-lookup"><span data-stu-id="db9b3-156">INPUTS</span></span>

### <span data-ttu-id="db9b3-157">System.String</span><span class="sxs-lookup"><span data-stu-id="db9b3-157">System.String</span></span>

### <span data-ttu-id="db9b3-158">System.Nullable'1[[System.Int32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="db9b3-158">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="db9b3-159">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="db9b3-159">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="db9b3-160">輸出</span><span class="sxs-lookup"><span data-stu-id="db9b3-160">OUTPUTS</span></span>

### <span data-ttu-id="db9b3-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="db9b3-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="db9b3-162">筆記</span><span class="sxs-lookup"><span data-stu-id="db9b3-162">NOTES</span></span>

## <span data-ttu-id="db9b3-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="db9b3-163">RELATED LINKS</span></span>

[<span data-ttu-id="db9b3-164">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="db9b3-164">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)

[<span data-ttu-id="db9b3-165">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="db9b3-165">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


