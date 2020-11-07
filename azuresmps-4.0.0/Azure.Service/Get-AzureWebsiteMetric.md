---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 717023DA-AA2D-4F1B-AE46-67ED75AA0D15
online version: ''
schema: 2.0.0
ms.openlocfilehash: b6d8dae704946680dd72ff8227d2a88d55f8b77a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967717"
---
# <span data-ttu-id="3b8b9-101">Get-AzureWebsiteMetric</span><span class="sxs-lookup"><span data-stu-id="3b8b9-101">Get-AzureWebsiteMetric</span></span>

## <span data-ttu-id="3b8b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3b8b9-102">SYNOPSIS</span></span>
<span data-ttu-id="3b8b9-103">取得目前訂閱中 Azure 網站的指標。</span><span class="sxs-lookup"><span data-stu-id="3b8b9-103">Gets metrics for the Azure website in the current subscription.</span></span>

## <span data-ttu-id="3b8b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="3b8b9-104">SYNTAX</span></span>

```
Get-AzureWebsiteMetric [-MetricNames <String[]>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-TimeGrain <String>] [-InstanceDetails] [-SlotView] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3b8b9-105">說明</span><span class="sxs-lookup"><span data-stu-id="3b8b9-105">DESCRIPTION</span></span>
<span data-ttu-id="3b8b9-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3b8b9-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3b8b9-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="3b8b9-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="3b8b9-108">**AzureWebsiteMetric** Cmdlet 會在目前的訂閱中取得 Azure 網站的指標。</span><span class="sxs-lookup"><span data-stu-id="3b8b9-108">The **Get-AzureWebsiteMetric** cmdlet gets metrics for the Azure website in the current subscription.</span></span>

## <span data-ttu-id="3b8b9-109">示例</span><span class="sxs-lookup"><span data-stu-id="3b8b9-109">EXAMPLES</span></span>

### <span data-ttu-id="3b8b9-110">範例1：針對網站的每個實例層級取得過去3小時的度量單位</span><span class="sxs-lookup"><span data-stu-id="3b8b9-110">Example 1: Get metrics for the last three hours on a per-instance level for a website</span></span>
```
PS C:\> Get-AzureWebsiteMetric -Name "ContosoWebSite" -StartDate (get-date).AddHours(-3) -MetricNames "Requests" -InstanceDetails -SlotView -TimeGrain "PT1M" 
PS C:\> $metrics[1].Data Name : Requests 

Unit : Count 

StartTime : 8/11/2014 7:05:00 AM 

EndTime : 8/11/2014 5:06:01 PM 

TimeGrain : PT1M 
PrimaryAggregationType : Instance 
Values : {Time:8/11/2014 7:05:00 AM, Total:4, Min:, Max:, Time:8/11/2014 7:06:00 AM, Total:3, Min:, Max:, 
Time:8/11/2014 7:07:00 AM, Total:3, Min:, Max:, Time:8/11/2014 7:08:00 AM, Total:12, Min:, Max:...} 
$metrics[1].Data.Values | ft 
TimeCreated Total Minimum Maximum Count InstanceName 
----------- ----- ------- ------- ----- ------------ 
8/11/2014 7:05:00 AM 4 1 RD00155DC24599 
8/11/2014 7:06:00 AM 3 1 RD00155DC24599 
8/11/2014 7:07:00 AM 3 1 RD00155DC24589 
8/11/2014 7:08:00 AM 12 1 RD00155DC24599
8/11/2014 7:09:00 AM 37 1 RD00155DC24599 
8/11/2014 7:10:00 AM 9 1 RD00155DC24599
```

<span data-ttu-id="3b8b9-111">這個命令會針對網站的每個實例層級，取得過去3小時的度量單位。</span><span class="sxs-lookup"><span data-stu-id="3b8b9-111">This command gets metrics for the last three hours on a per-instance level for a website.</span></span>

## <span data-ttu-id="3b8b9-112">參數</span><span class="sxs-lookup"><span data-stu-id="3b8b9-112">PARAMETERS</span></span>

### <span data-ttu-id="3b8b9-113">-結束日期</span><span class="sxs-lookup"><span data-stu-id="3b8b9-113">-EndDate</span></span>
<span data-ttu-id="3b8b9-114">指定時間（以 **DateTime** 物件表示），以停止取得度量單位。</span><span class="sxs-lookup"><span data-stu-id="3b8b9-114">Specifies the time, as a **DateTime** object, to stop getting metrics.</span></span>
<span data-ttu-id="3b8b9-115">若要取得 **DateTime** 物件，請使用 [ **取得日期** ] Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3b8b9-115">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="3b8b9-116">如需詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="3b8b9-116">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8b9-117">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="3b8b9-117">-InstanceDetails</span></span>
<span data-ttu-id="3b8b9-118">表示此 Cmdlet 包含針對每個實例層級的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3b8b9-118">Indicates that this cmdlet includes details on a per-instance level.</span></span>
<span data-ttu-id="3b8b9-119">如果網頁主機託管方案是在兩個以上的電腦上執行，此 Cmdlet 會針對每個電腦傳回度量單位。</span><span class="sxs-lookup"><span data-stu-id="3b8b9-119">If the web hosting plan runs on two or more computers, this cmdlet returns metrics for each computer.</span></span>

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

### <span data-ttu-id="3b8b9-120">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="3b8b9-120">-MetricNames</span></span>
<span data-ttu-id="3b8b9-121">指定要取得的度量陣列。</span><span class="sxs-lookup"><span data-stu-id="3b8b9-121">Specifies an array of metrics to get.</span></span>
<span data-ttu-id="3b8b9-122">如果您沒有指定此參數，則 Cmdlet 會取得所有度量單位。</span><span class="sxs-lookup"><span data-stu-id="3b8b9-122">If you do not specify this parameter, the cmdlet gets all metrics.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8b9-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="3b8b9-123">-Name</span></span>
<span data-ttu-id="3b8b9-124">指定訂閱中的網站名稱。</span><span class="sxs-lookup"><span data-stu-id="3b8b9-124">Specifies the name of a website in the subscription.</span></span>
<span data-ttu-id="3b8b9-125">這個參數不支援萬用字元字元。</span><span class="sxs-lookup"><span data-stu-id="3b8b9-125">This parameter does not support wildcard characters.</span></span>

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

### <span data-ttu-id="3b8b9-126">-設定檔</span><span class="sxs-lookup"><span data-stu-id="3b8b9-126">-Profile</span></span>
<span data-ttu-id="3b8b9-127">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="3b8b9-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3b8b9-128">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="3b8b9-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b8b9-129">-槽</span><span class="sxs-lookup"><span data-stu-id="3b8b9-129">-Slot</span></span>
<span data-ttu-id="3b8b9-130">指定雲端服務部署的環境。</span><span class="sxs-lookup"><span data-stu-id="3b8b9-130">Specifies the environment of a cloud service deployment.</span></span>
<span data-ttu-id="3b8b9-131">有效值為： [生產] 和 [轉移]。</span><span class="sxs-lookup"><span data-stu-id="3b8b9-131">Valid values are: Production and Staging.</span></span>

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

### <span data-ttu-id="3b8b9-132">-SlotView</span><span class="sxs-lookup"><span data-stu-id="3b8b9-132">-SlotView</span></span>
<span data-ttu-id="3b8b9-133">表示此 Cmdlet 會取得在目前槽接收流量之主機名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="3b8b9-133">Indicates that this cmdlet gets metrics for the host names that receive traffic at the current slot.</span></span>
<span data-ttu-id="3b8b9-134">如果在時段內發生交換，則會合並度量單位。</span><span class="sxs-lookup"><span data-stu-id="3b8b9-134">If a swap occurs during the time period, the metrics are merged.</span></span>

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

### <span data-ttu-id="3b8b9-135">-開始日期</span><span class="sxs-lookup"><span data-stu-id="3b8b9-135">-StartDate</span></span>
<span data-ttu-id="3b8b9-136">指定時間（作為 **DateTime** 物件）以開始取得度量單位。</span><span class="sxs-lookup"><span data-stu-id="3b8b9-136">Specifies the time, as a **DateTime** object, to start getting metrics.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8b9-137">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="3b8b9-137">-TimeGrain</span></span>
<span data-ttu-id="3b8b9-138">指定度量單位的時間單位。</span><span class="sxs-lookup"><span data-stu-id="3b8b9-138">Specifies the time unit for metrics.</span></span>
<span data-ttu-id="3b8b9-139">有效值為：</span><span class="sxs-lookup"><span data-stu-id="3b8b9-139">Valid values are:</span></span> 

- <span data-ttu-id="3b8b9-140">PT1M (分鐘) </span><span class="sxs-lookup"><span data-stu-id="3b8b9-140">PT1M (Minute)</span></span> 
- <span data-ttu-id="3b8b9-141">PT1H (小時) </span><span class="sxs-lookup"><span data-stu-id="3b8b9-141">PT1H (Hour)</span></span> 
- <span data-ttu-id="3b8b9-142">P1D (日) </span><span class="sxs-lookup"><span data-stu-id="3b8b9-142">P1D (Day)</span></span>

<span data-ttu-id="3b8b9-143">預設值為 PT1H。</span><span class="sxs-lookup"><span data-stu-id="3b8b9-143">The default value is PT1H.</span></span>

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

### <span data-ttu-id="3b8b9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b8b9-144">CommonParameters</span></span>
<span data-ttu-id="3b8b9-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3b8b9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b8b9-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3b8b9-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b8b9-147">輸入</span><span class="sxs-lookup"><span data-stu-id="3b8b9-147">INPUTS</span></span>

###  
<span data-ttu-id="3b8b9-148">您可以透過屬性名稱（而不是依值），將輸入傳遞到此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3b8b9-148">You can pass input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="3b8b9-149">輸出</span><span class="sxs-lookup"><span data-stu-id="3b8b9-149">OUTPUTS</span></span>

### <span data-ttu-id="3b8b9-150">WindowsAzure. WebEntities. MetricResponse （）</span><span class="sxs-lookup"><span data-stu-id="3b8b9-150">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.MetricResponse</span></span>
<span data-ttu-id="3b8b9-151">根據預設， **AzureWebsiteMetric** 會傳回 **MetricResponse** 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="3b8b9-151">By default, **Get-AzureWebsiteMetric** returns an array of **MetricResponse** objects.</span></span>

## <span data-ttu-id="3b8b9-152">筆記</span><span class="sxs-lookup"><span data-stu-id="3b8b9-152">NOTES</span></span>

## <span data-ttu-id="3b8b9-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b8b9-153">RELATED LINKS</span></span>

[<span data-ttu-id="3b8b9-154">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="3b8b9-154">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)


