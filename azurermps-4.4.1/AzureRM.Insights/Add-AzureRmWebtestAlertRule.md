---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
ms.openlocfilehash: 52b3d39aef4c117fe8b26bb35f1bf50143e5fec5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456603"
---
# <span data-ttu-id="cc597-101">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="cc597-101">Add-AzureRmWebtestAlertRule</span></span>

## <span data-ttu-id="cc597-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cc597-102">SYNOPSIS</span></span>
<span data-ttu-id="cc597-103">新增或更新 webtest 提醒規則。</span><span class="sxs-lookup"><span data-stu-id="cc597-103">Adds or updates a webtest alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc597-104">句法</span><span class="sxs-lookup"><span data-stu-id="cc597-104">SYNTAX</span></span>

```
Add-AzureRmWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc597-105">說明</span><span class="sxs-lookup"><span data-stu-id="cc597-105">DESCRIPTION</span></span>
<span data-ttu-id="cc597-106">**AzureRmWebtestAlertRule** Cmdlet 會新增或更新公制、event 或 webtest 類型的警示規則。</span><span class="sxs-lookup"><span data-stu-id="cc597-106">The **Add-AzureRmWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="cc597-107">新增的規則會與資源群組相關聯，且具有名稱。</span><span class="sxs-lookup"><span data-stu-id="cc597-107">The added rule is associated to a resource group and has a name.</span></span>

## <span data-ttu-id="cc597-108">示例</span><span class="sxs-lookup"><span data-stu-id="cc597-108">EXAMPLES</span></span>

### <span data-ttu-id="cc597-109">範例1：新增 webtest 警示規則</span><span class="sxs-lookup"><span data-stu-id="cc597-109">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzureRmWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri ":/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="cc597-110">這個命令會新增或更新 webtest 警示規則。</span><span class="sxs-lookup"><span data-stu-id="cc597-110">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="cc597-111">參數</span><span class="sxs-lookup"><span data-stu-id="cc597-111">PARAMETERS</span></span>

### <span data-ttu-id="cc597-112">-動作</span><span class="sxs-lookup"><span data-stu-id="cc597-112">-Actions</span></span>
<span data-ttu-id="cc597-113">指定以逗號分隔的動作清單。</span><span class="sxs-lookup"><span data-stu-id="cc597-113">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc597-114">-描述</span><span class="sxs-lookup"><span data-stu-id="cc597-114">-Description</span></span>
<span data-ttu-id="cc597-115">指定規則的描述。</span><span class="sxs-lookup"><span data-stu-id="cc597-115">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="cc597-116">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="cc597-116">-DisableRule</span></span>
<span data-ttu-id="cc597-117">停用規則。</span><span class="sxs-lookup"><span data-stu-id="cc597-117">Disables the rule.</span></span>
<span data-ttu-id="cc597-118">如果您沒有指定此參數，則會啟用規則。</span><span class="sxs-lookup"><span data-stu-id="cc597-118">If you do not specify this parameter, the rule is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc597-119">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="cc597-119">-FailedLocationCount</span></span>
<span data-ttu-id="cc597-120">指定 webtest 規則的失敗位置計數。</span><span class="sxs-lookup"><span data-stu-id="cc597-120">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="cc597-121">這與其他規則類型中的閾值類似。</span><span class="sxs-lookup"><span data-stu-id="cc597-121">This is similar to the threshold in the other types of rules.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc597-122">-位置</span><span class="sxs-lookup"><span data-stu-id="cc597-122">-Location</span></span>
<span data-ttu-id="cc597-123">指定定義規則的位置。</span><span class="sxs-lookup"><span data-stu-id="cc597-123">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="cc597-124">-MetricName</span><span class="sxs-lookup"><span data-stu-id="cc597-124">-MetricName</span></span>
<span data-ttu-id="cc597-125">指定度量值的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc597-125">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="cc597-126">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="cc597-126">-MetricNamespace</span></span>
<span data-ttu-id="cc597-127">指定規則的度量命名空間。</span><span class="sxs-lookup"><span data-stu-id="cc597-127">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="cc597-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="cc597-128">-Name</span></span>
<span data-ttu-id="cc597-129">指定規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc597-129">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="cc597-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cc597-130">-ResourceGroup</span></span>
<span data-ttu-id="cc597-131">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc597-131">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="cc597-132">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="cc597-132">-TargetResourceUri</span></span>
<span data-ttu-id="cc597-133">指定 webtest 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="cc597-133">Specifies the resource ID of the webtest.</span></span>

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

### <span data-ttu-id="cc597-134">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="cc597-134">-WindowSize</span></span>
<span data-ttu-id="cc597-135">指定規則計算其資料的時間視窗大小。</span><span class="sxs-lookup"><span data-stu-id="cc597-135">Specifies the time window size for the rule to compute its data.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc597-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc597-136">-DefaultProfile</span></span>
<span data-ttu-id="cc597-137">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc597-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc597-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc597-138">CommonParameters</span></span>
<span data-ttu-id="cc597-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cc597-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc597-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cc597-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc597-141">輸入</span><span class="sxs-lookup"><span data-stu-id="cc597-141">INPUTS</span></span>

## <span data-ttu-id="cc597-142">輸出</span><span class="sxs-lookup"><span data-stu-id="cc597-142">OUTPUTS</span></span>

### <span data-ttu-id="cc597-143">PSAddAlertRuleOperationResponse 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="cc597-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="cc597-144">筆記</span><span class="sxs-lookup"><span data-stu-id="cc597-144">NOTES</span></span>

## <span data-ttu-id="cc597-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc597-145">RELATED LINKS</span></span>

[<span data-ttu-id="cc597-146">附加 AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="cc597-146">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="cc597-147">附加 AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="cc597-147">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="cc597-148">AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="cc597-148">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="cc597-149">新-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="cc597-149">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


