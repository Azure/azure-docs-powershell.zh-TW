---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2DEF8B3A-4E91-4D39-AD39-1871F9FECE10
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5a59c93c9de0d2445f2839d9a66f4750751c987f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967956"
---
# <span data-ttu-id="7e925-101">Get-AzureWebHostingPlanMetric</span><span class="sxs-lookup"><span data-stu-id="7e925-101">Get-AzureWebHostingPlanMetric</span></span>

## <span data-ttu-id="7e925-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7e925-102">SYNOPSIS</span></span>
<span data-ttu-id="7e925-103">取得 Azure 網站託管方案的指標。</span><span class="sxs-lookup"><span data-stu-id="7e925-103">Gets metrics for Azure website hosting plans.</span></span>

## <span data-ttu-id="7e925-104">句法</span><span class="sxs-lookup"><span data-stu-id="7e925-104">SYNTAX</span></span>

```
Get-AzureWebHostingPlanMetric [-MetricNames <String[]>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-TimeGrain <String>] [-InstanceDetails] [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e925-105">說明</span><span class="sxs-lookup"><span data-stu-id="7e925-105">DESCRIPTION</span></span>
<span data-ttu-id="7e925-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7e925-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7e925-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="7e925-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7e925-108">**AzureWebHostingPlanMetric** Cmdlet 會在訂閱中取得 Azure web 託管方案的指標。</span><span class="sxs-lookup"><span data-stu-id="7e925-108">The **Get-AzureWebHostingPlanMetric** cmdlet gets metrics for Azure web hosting plans in a subscription.</span></span>

## <span data-ttu-id="7e925-109">示例</span><span class="sxs-lookup"><span data-stu-id="7e925-109">EXAMPLES</span></span>

### <span data-ttu-id="7e925-110">範例1：針對每個實例層級取得過去3小時的度量單位</span><span class="sxs-lookup"><span data-stu-id="7e925-110">Example 1: Get metrics for the last three hours at a per-instance level</span></span>
```
PS C:\> Get-AzureWebHostingPlanMetric -WebSpaceName "eastuswebspace" -StartDate (get-date).AddHours(-3) -InstanceDetails $Metrics[1].Data 

Name : CpuPercentage 
Unit : Percent 
StartTime : 8/11/2014 7:00:00 AM 
EndTime : 8/11/2014 5:00:23 PM 
TimeGrain : PT1H 
PrimaryAggregationType : Instance 
Values : {Time:8/11/2014 7:00:00 AM, Total:2, Min:9, Max:0, Time:8/11/2014 8:00:00 AM, Total:2, Min:9, Max:0, 
Time:8/11/2014 9:00:00 AM, Total:2, Min:9, Max:0, Time:8/11/2014 10:00:00 AM, Total:2, Min:8, Max:0...} $metrics[1].Data.Values | ft 
TimeCreated Total Minimum Maximum Count InstanceName
 ----------- ----- ------- ------- ----- ------------ 
8/11/2014 7:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 8:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 9:00:00 AM 2 9 0 1 RD00155DC24579 
8/11/2014 10:00:00 AM 2 8 0 1 RD00155DC24599 
8/11/2014 11:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 12:00:00 PM 2 6 0 1 RD00155DC24599 
8/11/2014 1:00:00 PM 2 15 0 1 RD00155DC24599 
8/11/2014 2:00:00 PM 3 21 0 1 RD00155DC24599 
8/11/2014 3:00:00 PM 2 13 0 1 RD00155DC24599 
8/11/2014 4:00:00 PM 2 14 0 1 RD00155DC24599
```

<span data-ttu-id="7e925-111">這個命令會針對每個實例層級，取得過去3小時的 web 主機名稱規劃度量單位。</span><span class="sxs-lookup"><span data-stu-id="7e925-111">This command gets web hosting plan metrics for last three hours on per-instance level.</span></span>

## <span data-ttu-id="7e925-112">參數</span><span class="sxs-lookup"><span data-stu-id="7e925-112">PARAMETERS</span></span>

### <span data-ttu-id="7e925-113">-結束日期</span><span class="sxs-lookup"><span data-stu-id="7e925-113">-EndDate</span></span>
<span data-ttu-id="7e925-114">指定要傳回指標之 [結束時間] （ **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="7e925-114">Specifies the end time, as a **DateTime** object, from which to return metrics.</span></span>
<span data-ttu-id="7e925-115">若要取得 **DateTime** 物件，請使用 [ **取得日期** ] Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7e925-115">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="7e925-116">如需詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="7e925-116">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="7e925-117">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="7e925-117">-InstanceDetails</span></span>
<span data-ttu-id="7e925-118">表示此 Cmdlet 包含針對每個實例層級的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7e925-118">Indicates that this cmdlet includes details on a per-instance level.</span></span>
<span data-ttu-id="7e925-119">如果網站託管方案是在兩台以上的電腦上執行，這個 Cmdlet 會針對每個電腦傳回詳細資料指標。</span><span class="sxs-lookup"><span data-stu-id="7e925-119">If the website hosting plan runs on two or more machines, this cmdlet returns details metrics for each machine.</span></span>

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

### <span data-ttu-id="7e925-120">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="7e925-120">-MetricNames</span></span>
<span data-ttu-id="7e925-121">Species 要取得的度量陣列。</span><span class="sxs-lookup"><span data-stu-id="7e925-121">Species an array of metrics to get.</span></span>
<span data-ttu-id="7e925-122">如果您沒有指定此參數的值，這個 Cmdlet 會取得所有的度量單位。</span><span class="sxs-lookup"><span data-stu-id="7e925-122">If you do not specify a value for this parameter, this cmdlet gets all metrics.</span></span>

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

### <span data-ttu-id="7e925-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="7e925-123">-Name</span></span>
<span data-ttu-id="7e925-124">指定訂閱中的方案名稱。</span><span class="sxs-lookup"><span data-stu-id="7e925-124">Specifies the name of a plan in the subscription.</span></span>
<span data-ttu-id="7e925-125">根據預設， **AzureWebHostingPlanMetric 會取得** 目前訂閱中的所有網站。</span><span class="sxs-lookup"><span data-stu-id="7e925-125">By default, **Get-AzureWebHostingPlanMetric** gets all websites in the current subscription.</span></span>
<span data-ttu-id="7e925-126">這個參數不支援萬用字元字元。</span><span class="sxs-lookup"><span data-stu-id="7e925-126">This parameter does not support wildcard characters.</span></span>

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

### <span data-ttu-id="7e925-127">-設定檔</span><span class="sxs-lookup"><span data-stu-id="7e925-127">-Profile</span></span>
<span data-ttu-id="7e925-128">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="7e925-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7e925-129">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="7e925-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7e925-130">-開始日期</span><span class="sxs-lookup"><span data-stu-id="7e925-130">-StartDate</span></span>
<span data-ttu-id="7e925-131">指定要取得度量單位的開始時間，做為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="7e925-131">Specifies the start time, as a **DateTime** object, for which to get metrics.</span></span>

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

### <span data-ttu-id="7e925-132">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="7e925-132">-TimeGrain</span></span>
<span data-ttu-id="7e925-133">指定要取得度量單位的時間單位。</span><span class="sxs-lookup"><span data-stu-id="7e925-133">Specifies the time unit for which to get metrics.</span></span>
<span data-ttu-id="7e925-134">有效值為：</span><span class="sxs-lookup"><span data-stu-id="7e925-134">Valid values are:</span></span> 

- <span data-ttu-id="7e925-135">PT1M (分鐘) </span><span class="sxs-lookup"><span data-stu-id="7e925-135">PT1M (Minute)</span></span> 
- <span data-ttu-id="7e925-136">PT1H (小時) </span><span class="sxs-lookup"><span data-stu-id="7e925-136">PT1H (Hour)</span></span> 
- <span data-ttu-id="7e925-137">P1D (日) </span><span class="sxs-lookup"><span data-stu-id="7e925-137">P1D (Day)</span></span>

<span data-ttu-id="7e925-138">預設值為 PT1H。</span><span class="sxs-lookup"><span data-stu-id="7e925-138">The default value is PT1H.</span></span>

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

### <span data-ttu-id="7e925-139">-WebSpaceName</span><span class="sxs-lookup"><span data-stu-id="7e925-139">-WebSpaceName</span></span>
<span data-ttu-id="7e925-140">指定訂閱中的 web 空間名稱。</span><span class="sxs-lookup"><span data-stu-id="7e925-140">Specifies the name of a webspace in the subscription.</span></span>
<span data-ttu-id="7e925-141">根據預設， **AzureWebHostingPlanMetric** 會取得目前訂閱中的所有方案。</span><span class="sxs-lookup"><span data-stu-id="7e925-141">By default, **Get-AzureWebHostingPlanMetric** gets all plans in the current subscription.</span></span>
<span data-ttu-id="7e925-142">這個參數不支援萬用字元字元。</span><span class="sxs-lookup"><span data-stu-id="7e925-142">This parameter does not support wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e925-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e925-143">CommonParameters</span></span>
<span data-ttu-id="7e925-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7e925-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e925-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7e925-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e925-146">輸入</span><span class="sxs-lookup"><span data-stu-id="7e925-146">INPUTS</span></span>

###  
<span data-ttu-id="7e925-147">您可以透過屬性名稱（而不是依值），將輸入傳遞到此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7e925-147">You can pass input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="7e925-148">輸出</span><span class="sxs-lookup"><span data-stu-id="7e925-148">OUTPUTS</span></span>

###  
<span data-ttu-id="7e925-149">WindowsAzure. WebEntities. MetricResponse （）</span><span class="sxs-lookup"><span data-stu-id="7e925-149">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.MetricResponse</span></span>

<span data-ttu-id="7e925-150">根據預設， **AzureWebHostingPlanMetric** 會傳回 **MetricResponse** 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="7e925-150">By default, **Get-AzureWebHostingPlanMetric** returns an array of **MetricResponse** objects.</span></span>

## <span data-ttu-id="7e925-151">筆記</span><span class="sxs-lookup"><span data-stu-id="7e925-151">NOTES</span></span>

## <span data-ttu-id="7e925-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="7e925-152">RELATED LINKS</span></span>

[<span data-ttu-id="7e925-153">AzureWebHostingPlan</span><span class="sxs-lookup"><span data-stu-id="7e925-153">Get-AzureWebHostingPlan</span></span>](./Get-AzureWebHostingPlan.md)


