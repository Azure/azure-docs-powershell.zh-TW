---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A70F4C03-E842-45D5-9323-DC5B14B569F1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAutoscaleHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAutoscaleHistory.md
ms.openlocfilehash: 12907bc7dbe7507dd12dbda13f0eb2ca722eaec3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456583"
---
# <span data-ttu-id="b5efe-101">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="b5efe-101">Get-AzureRmAutoscaleHistory</span></span>

## <span data-ttu-id="b5efe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b5efe-102">SYNOPSIS</span></span>
<span data-ttu-id="b5efe-103">取得自動縮放歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="b5efe-103">Gets the Autoscale history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5efe-104">句法</span><span class="sxs-lookup"><span data-stu-id="b5efe-104">SYNTAX</span></span>

```
Get-AzureRmAutoscaleHistory [-ResourceId <String>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Status <String>] [-Caller <String>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5efe-105">說明</span><span class="sxs-lookup"><span data-stu-id="b5efe-105">DESCRIPTION</span></span>
<span data-ttu-id="b5efe-106">**AzureRmAutoscaleHistory** Cmdlet 會取得與自動縮放設定相關的事件歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="b5efe-106">The **Get-AzureRmAutoscaleHistory** cmdlet gets the history of events related to an Autoscale setting.</span></span>

## <span data-ttu-id="b5efe-107">示例</span><span class="sxs-lookup"><span data-stu-id="b5efe-107">EXAMPLES</span></span>

### <span data-ttu-id="b5efe-108">範例1：取得與訂閱相關聯的所有事件</span><span class="sxs-lookup"><span data-stu-id="b5efe-108">Example 1: Get all events associated with a subscription</span></span>
```
PS C:\>Get-AzureRmAutoscaleHistory -StartTime 2015-02-09T18:35:00 -EndTime 2015-02-09T18:40:00 -DetailedOutput
```

<span data-ttu-id="b5efe-109">這個命令會取得與目前訂閱相關聯的所有自動縮放相關事件。</span><span class="sxs-lookup"><span data-stu-id="b5efe-109">This command gets all of the Autoscale-related events associated with the current subscription.</span></span>

### <span data-ttu-id="b5efe-110">範例2：針對特定資源的 GetAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="b5efe-110">Example 2: GetAutoscaleHistory for a particular resource</span></span>
```
PS C:\>Get-AzureRmAutoscaleHistory -StartTime 2015-02-09T18:35:00 -EndTime 2015-02-09T18:40:00 -ResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS" -DetailedOutput
Authorization        : 
Caller               : Microsoft.Insights/autoscaleSettings
Claims               :  http://schemas.xmlsoap.org/ws/2005/05/identity/claims/spn: Microsoft.Insights/autoscaleSettings
CorrelationId        : ac5b03ca-05d4-4811-9c27-0314a145f785
Description          : The autoscale engine attempting to scale resource '/subscriptions/a93fb07c-6c93-40be-bf3b-4f0deb
                       a10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm'
                       from 1 instances count to 2 instances count. 
EventChannels        : Admin, Operation
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

<span data-ttu-id="b5efe-111">這個命令會取得與資源識別碼所識別之特定資源相關聯的所有自動縮放相關事件， (實質上是 ResourceUri) 。</span><span class="sxs-lookup"><span data-stu-id="b5efe-111">This command gets all Autoscale-related events associated with a particular resource identified by the resource's ID (essentially, the ResourceUri).</span></span>

## <span data-ttu-id="b5efe-112">參數</span><span class="sxs-lookup"><span data-stu-id="b5efe-112">PARAMETERS</span></span>

### <span data-ttu-id="b5efe-113">-來電者</span><span class="sxs-lookup"><span data-stu-id="b5efe-113">-Caller</span></span>
<span data-ttu-id="b5efe-114">指定來電者。</span><span class="sxs-lookup"><span data-stu-id="b5efe-114">Specifies a caller.</span></span>

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

### <span data-ttu-id="b5efe-115">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="b5efe-115">-DetailedOutput</span></span>
<span data-ttu-id="b5efe-116">表示此操作包含詳細的輸出。</span><span class="sxs-lookup"><span data-stu-id="b5efe-116">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="b5efe-117">如果您沒有指定此參數，則會匯總輸出。</span><span class="sxs-lookup"><span data-stu-id="b5efe-117">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="b5efe-118">-EndTime</span><span class="sxs-lookup"><span data-stu-id="b5efe-118">-EndTime</span></span>
<span data-ttu-id="b5efe-119">指定當地時間的查詢結束時間。</span><span class="sxs-lookup"><span data-stu-id="b5efe-119">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="b5efe-120">預設為目前時間。</span><span class="sxs-lookup"><span data-stu-id="b5efe-120">The default is the current time.</span></span>

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

### <span data-ttu-id="b5efe-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5efe-121">-ResourceId</span></span>
<span data-ttu-id="b5efe-122">指定自動縮放設定所關聯的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b5efe-122">Specifies the resource ID to which the autoscale setting is associated.</span></span>

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

### <span data-ttu-id="b5efe-123">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b5efe-123">-StartTime</span></span>
<span data-ttu-id="b5efe-124">指定當地時間查詢的開始時間。</span><span class="sxs-lookup"><span data-stu-id="b5efe-124">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="b5efe-125">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="b5efe-125">This parameter is optional.</span></span>
<span data-ttu-id="b5efe-126">預設為目前的當地時間減去1小時。</span><span class="sxs-lookup"><span data-stu-id="b5efe-126">The default is the current local time minus one hour.</span></span>

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

### <span data-ttu-id="b5efe-127">-狀態</span><span class="sxs-lookup"><span data-stu-id="b5efe-127">-Status</span></span>
<span data-ttu-id="b5efe-128">依狀態指定篩選。</span><span class="sxs-lookup"><span data-stu-id="b5efe-128">Specifies a filter by status.</span></span>
<span data-ttu-id="b5efe-129">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="b5efe-129">This parameter is optional.</span></span>
<span data-ttu-id="b5efe-130">錯誤是空字串 (亦即沒有篩選) </span><span class="sxs-lookup"><span data-stu-id="b5efe-130">The fault is an empty string (i.e. no filter)</span></span>

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

### <span data-ttu-id="b5efe-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5efe-131">-DefaultProfile</span></span>
<span data-ttu-id="b5efe-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b5efe-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5efe-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5efe-133">CommonParameters</span></span>
<span data-ttu-id="b5efe-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b5efe-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5efe-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b5efe-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5efe-136">輸入</span><span class="sxs-lookup"><span data-stu-id="b5efe-136">INPUTS</span></span>

## <span data-ttu-id="b5efe-137">輸出</span><span class="sxs-lookup"><span data-stu-id="b5efe-137">OUTPUTS</span></span>

### <span data-ttu-id="b5efe-138">[System.object]。清單 ' 1 [IPSEventData] OutputClasses.]</span><span class="sxs-lookup"><span data-stu-id="b5efe-138">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSEventData]</span></span>

## <span data-ttu-id="b5efe-139">筆記</span><span class="sxs-lookup"><span data-stu-id="b5efe-139">NOTES</span></span>

## <span data-ttu-id="b5efe-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5efe-140">RELATED LINKS</span></span>

[<span data-ttu-id="b5efe-141">附加 AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b5efe-141">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="b5efe-142">AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b5efe-142">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="b5efe-143">移除-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b5efe-143">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)

