---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 36e523fbb224b77df205b8c7e7d736af0faa2962
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624813"
---
# <span data-ttu-id="73870-101">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="73870-101">Set-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="73870-102">摘要</span><span class="sxs-lookup"><span data-stu-id="73870-102">SYNOPSIS</span></span>
<span data-ttu-id="73870-103">設定資源的記錄和標準設定。</span><span class="sxs-lookup"><span data-stu-id="73870-103">Sets the logs and metrics settings for the resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73870-104">句法</span><span class="sxs-lookup"><span data-stu-id="73870-104">SYNTAX</span></span>

```
Set-AzureRmDiagnosticSetting -ResourceId <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-EventHubAuthorizationRuleId <String>] [-Enabled <Boolean>]
 [-Categories <System.Collections.Generic.List`1[System.String]>]
 [-Timegrains <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73870-105">說明</span><span class="sxs-lookup"><span data-stu-id="73870-105">DESCRIPTION</span></span>
<span data-ttu-id="73870-106">**AzureRmDiagnosticSetting** Cmdlet 可針對特定資源啟用或停用每個時間細微性與記錄類別。</span><span class="sxs-lookup"><span data-stu-id="73870-106">The **Set-AzureRmDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>

<span data-ttu-id="73870-107">記錄和度量單位儲存在指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="73870-107">The logs and metrics are stored in the specified storage account.</span></span>

## <span data-ttu-id="73870-108">示例</span><span class="sxs-lookup"><span data-stu-id="73870-108">EXAMPLES</span></span>

### <span data-ttu-id="73870-109">範例1：啟用資源的所有度量及記錄</span><span class="sxs-lookup"><span data-stu-id="73870-109">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="73870-110">這個命令會啟用 Resource01 的所有可用度量值和記錄。</span><span class="sxs-lookup"><span data-stu-id="73870-110">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="73870-111">範例2：停用所有的度量及記錄</span><span class="sxs-lookup"><span data-stu-id="73870-111">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="73870-112">這個命令會針對資源 Resource01 停用所有可用的度量和記錄。</span><span class="sxs-lookup"><span data-stu-id="73870-112">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="73870-113">範例3：啟用多個類別</span><span class="sxs-lookup"><span data-stu-id="73870-113">Example 3: Enable multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
Enabled   : True
Timegrain : PT1M
Enabled   : True
Timegrain : PT1H
Logs
Enabled  : True
Category : Category1
Enabled  : True
Category : Category2
Enabled  : True
Category : Category3
Enabled  : False
Category : Category4
```

<span data-ttu-id="73870-114">這個命令會啟用 Category1 和 Category2。</span><span class="sxs-lookup"><span data-stu-id="73870-114">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="73870-115">所有 timegrains 及其他類別會保持不變。</span><span class="sxs-lookup"><span data-stu-id="73870-115">All timegrains and other categories remain the same.</span></span>

### <span data-ttu-id="73870-116">範例4：啟用時間細微性和多個類別</span><span class="sxs-lookup"><span data-stu-id="73870-116">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2 -Timegrains PT1M
```

<span data-ttu-id="73870-117">這個命令只啟用 Category1、Category2 和時間細微性 PT1M。</span><span class="sxs-lookup"><span data-stu-id="73870-117">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="73870-118">所有其他時間 grains 和類別都不會改變。</span><span class="sxs-lookup"><span data-stu-id="73870-118">All other time grains and categories are unchanged.</span></span>

## <span data-ttu-id="73870-119">參數</span><span class="sxs-lookup"><span data-stu-id="73870-119">PARAMETERS</span></span>

### <span data-ttu-id="73870-120">-類別</span><span class="sxs-lookup"><span data-stu-id="73870-120">-Categories</span></span>
<span data-ttu-id="73870-121">根據 *Enabled* 的值，指定要啟用或停用的記錄類別清單。</span><span class="sxs-lookup"><span data-stu-id="73870-121">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="73870-122">如果您沒有指定類別，此命令會作用於所有類別。</span><span class="sxs-lookup"><span data-stu-id="73870-122">If you do not specify a category, this command operates on all categories.</span></span>

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

### <span data-ttu-id="73870-123">-啟用</span><span class="sxs-lookup"><span data-stu-id="73870-123">-Enabled</span></span>
<span data-ttu-id="73870-124">指出是否要啟用診斷。</span><span class="sxs-lookup"><span data-stu-id="73870-124">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="73870-125">指定 $True 以啟用診斷，或 $False 以停用診斷程式。</span><span class="sxs-lookup"><span data-stu-id="73870-125">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73870-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73870-126">-ResourceId</span></span>
<span data-ttu-id="73870-127">指定資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="73870-127">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="73870-128">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="73870-128">-RetentionEnabled</span></span>
<span data-ttu-id="73870-129">指出是否已啟用診斷資訊的保留。</span><span class="sxs-lookup"><span data-stu-id="73870-129">Indicates whether retention of diagnostic information is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73870-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="73870-130">-RetentionInDays</span></span>
<span data-ttu-id="73870-131">指定保留原則（以天為單位）。</span><span class="sxs-lookup"><span data-stu-id="73870-131">Specifies the retention policy, in days.</span></span>

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

### <span data-ttu-id="73870-132">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="73870-132">-ServiceBusRuleId</span></span>
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

### <span data-ttu-id="73870-133">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="73870-133">-StorageAccountId</span></span>
<span data-ttu-id="73870-134">指定要儲存資料的儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="73870-134">Specifies the ID of the Storage account in which to save the data.</span></span>

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

### <span data-ttu-id="73870-135">-Timegrains</span><span class="sxs-lookup"><span data-stu-id="73870-135">-Timegrains</span></span>
<span data-ttu-id="73870-136">根據 [ *Enabled* ] 的值，指定要啟用或停用度量單位的時間 grains。</span><span class="sxs-lookup"><span data-stu-id="73870-136">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="73870-137">如果您沒有指定時間細微性，這個命令會在所有可用的時間 grains 上執行。</span><span class="sxs-lookup"><span data-stu-id="73870-137">If you do not specify a time grain, this command operates on all available time grains.</span></span>

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

### <span data-ttu-id="73870-138">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="73870-138">-WorkspaceId</span></span>
<span data-ttu-id="73870-139">工作區的識別碼</span><span class="sxs-lookup"><span data-stu-id="73870-139">The Id of the workspace</span></span>

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

### <span data-ttu-id="73870-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73870-140">-DefaultProfile</span></span>
<span data-ttu-id="73870-141">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="73870-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73870-142">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="73870-142">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="73870-143">事件中心規則識別碼</span><span class="sxs-lookup"><span data-stu-id="73870-143">The event hub rule id</span></span>

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

### <span data-ttu-id="73870-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73870-144">CommonParameters</span></span>
<span data-ttu-id="73870-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="73870-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73870-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="73870-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73870-147">輸入</span><span class="sxs-lookup"><span data-stu-id="73870-147">INPUTS</span></span>

## <span data-ttu-id="73870-148">輸出</span><span class="sxs-lookup"><span data-stu-id="73870-148">OUTPUTS</span></span>

### <span data-ttu-id="73870-149">PSServiceDiagnosticSettings 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="73870-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="73870-150">筆記</span><span class="sxs-lookup"><span data-stu-id="73870-150">NOTES</span></span>

## <span data-ttu-id="73870-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="73870-151">RELATED LINKS</span></span>

[<span data-ttu-id="73870-152">AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="73870-152">Get-AzureRmDiagnosticSetting</span></span>](./Get-AzureRmDiagnosticSetting.md)


