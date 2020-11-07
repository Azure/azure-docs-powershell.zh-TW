---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A70F4C03-E842-45D5-9323-DC5B14B569F1
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azautoscalehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzAutoscaleHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzAutoscaleHistory.md
ms.openlocfilehash: 1b0751656920434e85087ea07241f4f6a01e2fce
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794627"
---
# <span data-ttu-id="68375-101">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="68375-101">Get-AzAutoscaleHistory</span></span>

## <span data-ttu-id="68375-102">摘要</span><span class="sxs-lookup"><span data-stu-id="68375-102">SYNOPSIS</span></span>
<span data-ttu-id="68375-103">取得自動縮放歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="68375-103">Gets the Autoscale history.</span></span>

## <span data-ttu-id="68375-104">句法</span><span class="sxs-lookup"><span data-stu-id="68375-104">SYNTAX</span></span>

```
Get-AzAutoscaleHistory [-ResourceId <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>]
 [-Caller <String>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68375-105">說明</span><span class="sxs-lookup"><span data-stu-id="68375-105">DESCRIPTION</span></span>
<span data-ttu-id="68375-106">**AzAutoscaleHistory** Cmdlet 會取得與自動縮放設定相關的事件歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="68375-106">The **Get-AzAutoscaleHistory** cmdlet gets the history of events related to an Autoscale setting.</span></span>

## <span data-ttu-id="68375-107">示例</span><span class="sxs-lookup"><span data-stu-id="68375-107">EXAMPLES</span></span>

### <span data-ttu-id="68375-108">範例1：取得與訂閱相關聯的所有事件</span><span class="sxs-lookup"><span data-stu-id="68375-108">Example 1: Get all events associated with a subscription</span></span>
```
PS C:\>Get-AzAutoscaleHistory -StartTime 2015-02-09T18:35:00 -EndTime 2015-02-09T18:40:00 -DetailedOutput
```

<span data-ttu-id="68375-109">這個命令會取得與目前訂閱相關聯的所有自動縮放相關事件。</span><span class="sxs-lookup"><span data-stu-id="68375-109">This command gets all of the Autoscale-related events associated with the current subscription.</span></span>

### <span data-ttu-id="68375-110">範例2：針對特定資源的 GetAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="68375-110">Example 2: GetAutoscaleHistory for a particular resource</span></span>
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

<span data-ttu-id="68375-111">這個命令會取得與資源識別碼所識別之特定資源相關聯的所有自動縮放相關事件， (實質上是 ResourceUri) 。</span><span class="sxs-lookup"><span data-stu-id="68375-111">This command gets all Autoscale-related events associated with a particular resource identified by the resource's ID (essentially, the ResourceUri).</span></span>

## <span data-ttu-id="68375-112">參數</span><span class="sxs-lookup"><span data-stu-id="68375-112">PARAMETERS</span></span>

### <span data-ttu-id="68375-113">-來電者</span><span class="sxs-lookup"><span data-stu-id="68375-113">-Caller</span></span>
<span data-ttu-id="68375-114">指定來電者。</span><span class="sxs-lookup"><span data-stu-id="68375-114">Specifies a caller.</span></span>

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

### <span data-ttu-id="68375-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68375-115">-DefaultProfile</span></span>
<span data-ttu-id="68375-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="68375-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68375-117">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="68375-117">-DetailedOutput</span></span>
<span data-ttu-id="68375-118">表示此操作包含詳細的輸出。</span><span class="sxs-lookup"><span data-stu-id="68375-118">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="68375-119">如果您沒有指定此參數，則會匯總輸出。</span><span class="sxs-lookup"><span data-stu-id="68375-119">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="68375-120">-EndTime</span><span class="sxs-lookup"><span data-stu-id="68375-120">-EndTime</span></span>
<span data-ttu-id="68375-121">指定當地時間的查詢結束時間。</span><span class="sxs-lookup"><span data-stu-id="68375-121">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="68375-122">預設為目前時間。</span><span class="sxs-lookup"><span data-stu-id="68375-122">The default is the current time.</span></span>

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

### <span data-ttu-id="68375-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68375-123">-ResourceId</span></span>
<span data-ttu-id="68375-124">指定自動縮放設定所關聯的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="68375-124">Specifies the resource ID to which the autoscale setting is associated.</span></span>

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

### <span data-ttu-id="68375-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="68375-125">-StartTime</span></span>
<span data-ttu-id="68375-126">指定當地時間查詢的開始時間。</span><span class="sxs-lookup"><span data-stu-id="68375-126">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="68375-127">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="68375-127">This parameter is optional.</span></span>
<span data-ttu-id="68375-128">預設為目前的當地時間減去1小時。</span><span class="sxs-lookup"><span data-stu-id="68375-128">The default is the current local time minus one hour.</span></span>

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

### <span data-ttu-id="68375-129">-狀態</span><span class="sxs-lookup"><span data-stu-id="68375-129">-Status</span></span>
<span data-ttu-id="68375-130">依狀態指定篩選。</span><span class="sxs-lookup"><span data-stu-id="68375-130">Specifies a filter by status.</span></span>
<span data-ttu-id="68375-131">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="68375-131">This parameter is optional.</span></span>
<span data-ttu-id="68375-132">錯誤是空字串 (亦即沒有篩選) </span><span class="sxs-lookup"><span data-stu-id="68375-132">The fault is an empty string (i.e. no filter)</span></span>

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

### <span data-ttu-id="68375-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68375-133">CommonParameters</span></span>
<span data-ttu-id="68375-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="68375-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68375-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="68375-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68375-136">輸入</span><span class="sxs-lookup"><span data-stu-id="68375-136">INPUTS</span></span>

### <span data-ttu-id="68375-137">System.object</span><span class="sxs-lookup"><span data-stu-id="68375-137">System.String</span></span>

### <span data-ttu-id="68375-138">System.object Null ' 1 [CoreLib，System.object = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="68375-138">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="68375-139">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="68375-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="68375-140">輸出</span><span class="sxs-lookup"><span data-stu-id="68375-140">OUTPUTS</span></span>

### <span data-ttu-id="68375-141">PSEventData 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="68375-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="68375-142">筆記</span><span class="sxs-lookup"><span data-stu-id="68375-142">NOTES</span></span>

## <span data-ttu-id="68375-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="68375-143">RELATED LINKS</span></span>

[<span data-ttu-id="68375-144">附加 AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="68375-144">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="68375-145">AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="68375-145">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="68375-146">移除-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="68375-146">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


