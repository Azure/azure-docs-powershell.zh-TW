---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A70F4C03-E842-45D5-9323-DC5B14B569F1
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azautoscalehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAutoscaleHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAutoscaleHistory.md
ms.openlocfilehash: c88cd3bbf132ccb7b8913b15dcc66f58ea2d2db3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908949"
---
# <span data-ttu-id="30050-101">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="30050-101">Get-AzAutoscaleHistory</span></span>

## <span data-ttu-id="30050-102">簡介</span><span class="sxs-lookup"><span data-stu-id="30050-102">SYNOPSIS</span></span>
<span data-ttu-id="30050-103">獲得自動縮放歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="30050-103">Gets the Autoscale history.</span></span>

## <span data-ttu-id="30050-104">語法</span><span class="sxs-lookup"><span data-stu-id="30050-104">SYNTAX</span></span>

```
Get-AzAutoscaleHistory [-ResourceId <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>]
 [-Caller <String>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30050-105">描述</span><span class="sxs-lookup"><span data-stu-id="30050-105">DESCRIPTION</span></span>
<span data-ttu-id="30050-106">**Get-AzAutoscaleHistory Cmdlet** 會取得與自動縮放設定相關的事件歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="30050-106">The **Get-AzAutoscaleHistory** cmdlet gets the history of events related to an Autoscale setting.</span></span>

## <span data-ttu-id="30050-107">例子</span><span class="sxs-lookup"><span data-stu-id="30050-107">EXAMPLES</span></span>

### <span data-ttu-id="30050-108">範例 1：取得與訂閱關聯的所有事件</span><span class="sxs-lookup"><span data-stu-id="30050-108">Example 1: Get all events associated with a subscription</span></span>
```
PS C:\>Get-AzAutoscaleHistory -StartTime 2015-02-09T18:35:00 -EndTime 2015-02-09T18:40:00 -DetailedOutput
```

<span data-ttu-id="30050-109">此命令會獲得與目前訂閱相關聯的所有自動縮放相關事件。</span><span class="sxs-lookup"><span data-stu-id="30050-109">This command gets all of the Autoscale-related events associated with the current subscription.</span></span>

### <span data-ttu-id="30050-110">範例 2：特定資源的 GetAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="30050-110">Example 2: GetAutoscaleHistory for a particular resource</span></span>
```
PS C:\>Get-AzAutoscaleHistory -StartTime 2015-02-09T18:35:00 -EndTime 2015-02-09T18:40:00 -ResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS" -DetailedOutput
Authorization        : 
Caller               : Microsoft.Insights/autoscaleSettings
Claims               :  http://schemas.xmlsoap.org/ws/2005/05/identity/claims/spn: Microsoft.Insights/autoscaleSettings
CorrelationId        : ac5b03ca-05d4-4811-9c27-0314a145f785
Description          : The autoscale engine attempting to scale resource '/subscriptions/a93fb07c-6c93-40be-bf3b-4f0deb
                       a10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm'
                       from 1 instances count to 2 instances count. 
EventDataId          : c554f7ed-514c-449c-9338-13e15b4b56a3
EventName            : AutoscaleAction
EventSource          : microsoft.insights/autoscalesettings
EventTimestamp       : 2/10/2015 2:38:19 AM
HttpRequest          : 
Id                   : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS/events/c554f7ed-514c-4
                       49c-9338-13e15b4b56a3/ticks/635591326997519815
Level                : Informational
OperationId          : ac5b03ca-05d4-4811-9c27-0314a145f785
OperationName        : ScaleUp
Properties           : 
Description    : The autoscale engine attempting to scale resource '/subscriptions/a93fb07c-6c93
                       -40be-bf3b-4f0deba10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/De
                       faultServerFarm' from 1 instances count to 2 instances count. 
ResourceName   : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-
                       EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
OldInstancesCount: 1
NewInstancesCount: 2
ActiveAutoscaleProfile: {
                         "Name": "No scheduled times",
                         "Capacity": {
                           "Minimum": "1",
                           "Maximum": "3",
                           "Default": "1"
                         },
                         "Rules": [
                           {
                             "MetricTrigger": {
                               "Name": "CpuPercentage",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT45M",
                               "TimeAggregation": "Average",
                               "Operator": "GreaterThanOrEqual",
                               "Threshold": 14.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Increase",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT5M"
                             }
                           },
                           {
                             "MetricTrigger": {
                               "Name": "CpuPercentage",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT45M",
                               "TimeAggregation": "Average",
                               "Operator": "LessThanOrEqual",
                               "Threshold": 4.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Decrease",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT2H"
                             }
                           },
                           {
                             "MetricTrigger": {
                               "Name": "BytesReceived",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT10M",
                               "TimeAggregation": "Average",
                               "Operator": "LessThanOrEqual",
                               "Threshold": 50.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Decrease",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT10M"
                             }
                           },
                           {
                             "MetricTrigger": {
                               "Name": "BytesReceived",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT5M",
                               "TimeAggregation": "Average",
                               "Operator": "GreaterThanOrEqual",
                               "Threshold": 100.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Increase",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT10M"
                             }
                           }
                         ] 
                       }
ResourceGroupName    : Default-Web-EastUS
ResourceProviderName : microsoft.insights
ResourceId           : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS
Status               : Succeeded
SubmissionTimestamp  : 2/10/2015 2:38:19 AM
SubscriptionId       : b93fb07a-6f93-30be-bf3e-4f0deca15f4f
SubStatus            :
```

<span data-ttu-id="30050-111">此命令會獲得與資源識別碼識別的特定資源相關聯的所有自動縮放相關事件，其 (，即 ResourceUri) 。</span><span class="sxs-lookup"><span data-stu-id="30050-111">This command gets all Autoscale-related events associated with a particular resource identified by the resource's ID (essentially, the ResourceUri).</span></span>

## <span data-ttu-id="30050-112">參數</span><span class="sxs-lookup"><span data-stu-id="30050-112">PARAMETERS</span></span>

### <span data-ttu-id="30050-113">-本機號碼</span><span class="sxs-lookup"><span data-stu-id="30050-113">-Caller</span></span>
<span data-ttu-id="30050-114">指定來電者。</span><span class="sxs-lookup"><span data-stu-id="30050-114">Specifies a caller.</span></span>

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

### <span data-ttu-id="30050-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30050-115">-DefaultProfile</span></span>
<span data-ttu-id="30050-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="30050-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30050-117">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="30050-117">-DetailedOutput</span></span>
<span data-ttu-id="30050-118">表示此作業包含詳細輸出。</span><span class="sxs-lookup"><span data-stu-id="30050-118">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="30050-119">如果您未指定此參數，輸出會摘要顯示。</span><span class="sxs-lookup"><span data-stu-id="30050-119">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="30050-120">-EndTime</span><span class="sxs-lookup"><span data-stu-id="30050-120">-EndTime</span></span>
<span data-ttu-id="30050-121">指定查詢在本地時間中的結束時間。</span><span class="sxs-lookup"><span data-stu-id="30050-121">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="30050-122">預設值為目前時間。</span><span class="sxs-lookup"><span data-stu-id="30050-122">The default is the current time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30050-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30050-123">-ResourceId</span></span>
<span data-ttu-id="30050-124">指定與自動縮放設定相關聯的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="30050-124">Specifies the resource ID to which the autoscale setting is associated.</span></span>

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

### <span data-ttu-id="30050-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="30050-125">-StartTime</span></span>
<span data-ttu-id="30050-126">指定查詢在本地時間中的開始時間。</span><span class="sxs-lookup"><span data-stu-id="30050-126">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="30050-127">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="30050-127">This parameter is optional.</span></span>
<span data-ttu-id="30050-128">預設值為目前的當地時間減 1 小時。</span><span class="sxs-lookup"><span data-stu-id="30050-128">The default is the current local time minus one hour.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30050-129">-狀態</span><span class="sxs-lookup"><span data-stu-id="30050-129">-Status</span></span>
<span data-ttu-id="30050-130">根據狀態指定篩選。</span><span class="sxs-lookup"><span data-stu-id="30050-130">Specifies a filter by status.</span></span>
<span data-ttu-id="30050-131">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="30050-131">This parameter is optional.</span></span>
<span data-ttu-id="30050-132">錯誤是空字串 (例如沒有篩選) </span><span class="sxs-lookup"><span data-stu-id="30050-132">The fault is an empty string (i.e. no filter)</span></span>

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

### <span data-ttu-id="30050-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30050-133">CommonParameters</span></span>
<span data-ttu-id="30050-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="30050-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30050-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30050-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30050-136">輸入</span><span class="sxs-lookup"><span data-stu-id="30050-136">INPUTS</span></span>

### <span data-ttu-id="30050-137">System.String</span><span class="sxs-lookup"><span data-stu-id="30050-137">System.String</span></span>

### <span data-ttu-id="30050-138">System.Nullable'1[[System.DateTime， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="30050-138">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="30050-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="30050-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="30050-140">輸出</span><span class="sxs-lookup"><span data-stu-id="30050-140">OUTPUTS</span></span>

### <span data-ttu-id="30050-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span><span class="sxs-lookup"><span data-stu-id="30050-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="30050-142">筆記</span><span class="sxs-lookup"><span data-stu-id="30050-142">NOTES</span></span>

## <span data-ttu-id="30050-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="30050-143">RELATED LINKS</span></span>

[<span data-ttu-id="30050-144">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="30050-144">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="30050-145">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="30050-145">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="30050-146">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="30050-146">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


