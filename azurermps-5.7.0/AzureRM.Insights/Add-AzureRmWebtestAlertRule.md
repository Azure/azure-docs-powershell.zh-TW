---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermwebtestalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
ms.openlocfilehash: da395b66cb4d63593c097f214701365370e06b75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448653"
---
# <span data-ttu-id="db91f-101">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="db91f-101">Add-AzureRmWebtestAlertRule</span></span>

## <span data-ttu-id="db91f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="db91f-102">SYNOPSIS</span></span>
<span data-ttu-id="db91f-103">新增或更新 webtest 提醒規則。</span><span class="sxs-lookup"><span data-stu-id="db91f-103">Adds or updates a webtest alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db91f-104">句法</span><span class="sxs-lookup"><span data-stu-id="db91f-104">SYNTAX</span></span>

```
Add-AzureRmWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db91f-105">說明</span><span class="sxs-lookup"><span data-stu-id="db91f-105">DESCRIPTION</span></span>
<span data-ttu-id="db91f-106">**AzureRmWebtestAlertRule** Cmdlet 會新增或更新公制、event 或 webtest 類型的警示規則。</span><span class="sxs-lookup"><span data-stu-id="db91f-106">The **Add-AzureRmWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="db91f-107">新增的規則會與資源群組相關聯，且具有名稱。</span><span class="sxs-lookup"><span data-stu-id="db91f-107">The added rule is associated to a resource group and has a name.</span></span>
<span data-ttu-id="db91f-108">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際建立、修改或移除資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="db91f-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="db91f-109">示例</span><span class="sxs-lookup"><span data-stu-id="db91f-109">EXAMPLES</span></span>

### <span data-ttu-id="db91f-110">範例1：新增 webtest 警示規則</span><span class="sxs-lookup"><span data-stu-id="db91f-110">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzureRmWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri ":/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="db91f-111">這個命令會新增或更新 webtest 警示規則。</span><span class="sxs-lookup"><span data-stu-id="db91f-111">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="db91f-112">參數</span><span class="sxs-lookup"><span data-stu-id="db91f-112">PARAMETERS</span></span>

### <span data-ttu-id="db91f-113">-動作</span><span class="sxs-lookup"><span data-stu-id="db91f-113">-Action</span></span>
<span data-ttu-id="db91f-114">指定以逗號分隔的動作清單。</span><span class="sxs-lookup"><span data-stu-id="db91f-114">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases: Actions

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db91f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db91f-115">-DefaultProfile</span></span>
<span data-ttu-id="db91f-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="db91f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db91f-117">-描述</span><span class="sxs-lookup"><span data-stu-id="db91f-117">-Description</span></span>
<span data-ttu-id="db91f-118">指定規則的描述。</span><span class="sxs-lookup"><span data-stu-id="db91f-118">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="db91f-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="db91f-119">-DisableRule</span></span>
<span data-ttu-id="db91f-120">停用規則。</span><span class="sxs-lookup"><span data-stu-id="db91f-120">Disables the rule.</span></span>
<span data-ttu-id="db91f-121">如果您沒有指定此參數，則會啟用規則。</span><span class="sxs-lookup"><span data-stu-id="db91f-121">If you do not specify this parameter, the rule is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db91f-122">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="db91f-122">-FailedLocationCount</span></span>
<span data-ttu-id="db91f-123">指定 webtest 規則的失敗位置計數。</span><span class="sxs-lookup"><span data-stu-id="db91f-123">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="db91f-124">這與其他規則類型中的閾值類似。</span><span class="sxs-lookup"><span data-stu-id="db91f-124">This is similar to the threshold in the other types of rules.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db91f-125">-位置</span><span class="sxs-lookup"><span data-stu-id="db91f-125">-Location</span></span>
<span data-ttu-id="db91f-126">指定定義規則的位置。</span><span class="sxs-lookup"><span data-stu-id="db91f-126">Specifies the location where the rule is defined.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db91f-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="db91f-127">-MetricName</span></span>
<span data-ttu-id="db91f-128">指定度量值的名稱。</span><span class="sxs-lookup"><span data-stu-id="db91f-128">Specifies the name of the metric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db91f-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="db91f-129">-MetricNamespace</span></span>
<span data-ttu-id="db91f-130">指定規則的度量命名空間。</span><span class="sxs-lookup"><span data-stu-id="db91f-130">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="db91f-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="db91f-131">-Name</span></span>
<span data-ttu-id="db91f-132">指定規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="db91f-132">Specifies the name of the rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db91f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db91f-133">-ResourceGroupName</span></span>
<span data-ttu-id="db91f-134">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="db91f-134">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db91f-135">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="db91f-135">-TargetResourceUri</span></span>
<span data-ttu-id="db91f-136">指定 webtest 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="db91f-136">Specifies the resource ID of the webtest.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db91f-137">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="db91f-137">-WindowSize</span></span>
<span data-ttu-id="db91f-138">指定規則計算其資料的時間視窗大小。</span><span class="sxs-lookup"><span data-stu-id="db91f-138">Specifies the time window size for the rule to compute its data.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db91f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db91f-139">CommonParameters</span></span>
<span data-ttu-id="db91f-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="db91f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db91f-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="db91f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db91f-142">輸入</span><span class="sxs-lookup"><span data-stu-id="db91f-142">INPUTS</span></span>

### <span data-ttu-id="db91f-143">所有</span><span class="sxs-lookup"><span data-stu-id="db91f-143">None</span></span>
<span data-ttu-id="db91f-144">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="db91f-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="db91f-145">輸出</span><span class="sxs-lookup"><span data-stu-id="db91f-145">OUTPUTS</span></span>

### <span data-ttu-id="db91f-146">PSAddAlertRuleOperationResponse 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="db91f-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="db91f-147">筆記</span><span class="sxs-lookup"><span data-stu-id="db91f-147">NOTES</span></span>

## <span data-ttu-id="db91f-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="db91f-148">RELATED LINKS</span></span>

[<span data-ttu-id="db91f-149">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="db91f-149">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="db91f-150">附加 AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="db91f-150">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="db91f-151">AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="db91f-151">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="db91f-152">新-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="db91f-152">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


