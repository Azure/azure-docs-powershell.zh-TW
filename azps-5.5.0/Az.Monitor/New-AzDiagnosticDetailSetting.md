---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdiagnosticdetailsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticDetailSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticDetailSetting.md
ms.openlocfilehash: b990a386feebe8e04ba612c45550ecbd07524c7a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140614"
---
# <span data-ttu-id="8bb68-101">New-AzDiagnosticDetailSetting</span><span class="sxs-lookup"><span data-stu-id="8bb68-101">New-AzDiagnosticDetailSetting</span></span>

## <span data-ttu-id="8bb68-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8bb68-102">SYNOPSIS</span></span>
<span data-ttu-id="8bb68-103">建立 PSDiagnosticDetailSetting 物件，類型可以是公制或 log</span><span class="sxs-lookup"><span data-stu-id="8bb68-103">Create PSDiagnosticDetailSetting Object, type could be metric or log</span></span>

## <span data-ttu-id="8bb68-104">句法</span><span class="sxs-lookup"><span data-stu-id="8bb68-104">SYNTAX</span></span>

### <span data-ttu-id="8bb68-105">LogSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="8bb68-105">LogSettingParameterSet</span></span>
```
New-AzDiagnosticDetailSetting -Log [-RetentionInDays <Int32>] [-RetentionEnabled] -Category <String>
 [-Enabled] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8bb68-106">MetricSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="8bb68-106">MetricSettingParameterSet</span></span>
```
New-AzDiagnosticDetailSetting -Metric [-RetentionInDays <Int32>] [-RetentionEnabled] -Category <String>
 [-Enabled] [-TimeGrain <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8bb68-107">說明</span><span class="sxs-lookup"><span data-stu-id="8bb68-107">DESCRIPTION</span></span>
<span data-ttu-id="8bb68-108">建立 PSMetricSettings 或 PSLogSettings 物件。</span><span class="sxs-lookup"><span data-stu-id="8bb68-108">Create PSMetricSettings or PSLogSettings object.</span></span> <span data-ttu-id="8bb68-109">您可以使用來取得類別 `Get-AzDiagnosticSettingCategory` 。</span><span class="sxs-lookup"><span data-stu-id="8bb68-109">You can get categories by using `Get-AzDiagnosticSettingCategory`.</span></span>

## <span data-ttu-id="8bb68-110">示例</span><span class="sxs-lookup"><span data-stu-id="8bb68-110">EXAMPLES</span></span>

### <span data-ttu-id="8bb68-111">範例1</span><span class="sxs-lookup"><span data-stu-id="8bb68-111">Example 1</span></span>
```powershell
PS C:\> $TimeGrain=New-TimeSpan -Days 90
PS C:\> New-AzDiagnosticDetailSetting -Metric -RetentionInDays 1 -RetentionEnabled -Category AllMetrics -Enabled -TimeGrain $TimeGrain
TimeGrain       : 90.00:00:00
Category        : AllMetrics
Enabled         : True
RetentionPolicy :
                  Enabled : True
                  Days    : 1
CategoryType    : Metrics
```

<span data-ttu-id="8bb68-112">建立 PSMetricSettings 物件。</span><span class="sxs-lookup"><span data-stu-id="8bb68-112">Create PSMetricSettings object.</span></span>

### <span data-ttu-id="8bb68-113">範例2</span><span class="sxs-lookup"><span data-stu-id="8bb68-113">Example 2</span></span>
```powershell
PS C:\> New-AzDiagnosticDetailSetting -Log -RetentionInDays 1 -RetentionEnabled -Category Audit -Enabled
Category Enabled RetentionPolicy               CategoryType
-------- ------- ---------------               ------------
Audit       True …                                     Logs
```

<span data-ttu-id="8bb68-114">建立 PSLogSettings 物件。</span><span class="sxs-lookup"><span data-stu-id="8bb68-114">Create PSLogSettings object.</span></span>

## <span data-ttu-id="8bb68-115">參數</span><span class="sxs-lookup"><span data-stu-id="8bb68-115">PARAMETERS</span></span>

### <span data-ttu-id="8bb68-116">-類別</span><span class="sxs-lookup"><span data-stu-id="8bb68-116">-Category</span></span>
<span data-ttu-id="8bb68-117">設定類別</span><span class="sxs-lookup"><span data-stu-id="8bb68-117">Category of setting</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bb68-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bb68-118">-DefaultProfile</span></span>
<span data-ttu-id="8bb68-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8bb68-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bb68-120">-啟用</span><span class="sxs-lookup"><span data-stu-id="8bb68-120">-Enabled</span></span>
<span data-ttu-id="8bb68-121">啟用設定</span><span class="sxs-lookup"><span data-stu-id="8bb68-121">Enable the setting</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bb68-122">-記錄</span><span class="sxs-lookup"><span data-stu-id="8bb68-122">-Log</span></span>
<span data-ttu-id="8bb68-123">建立記錄設定</span><span class="sxs-lookup"><span data-stu-id="8bb68-123">To create log setting</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LogSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bb68-124">-公制</span><span class="sxs-lookup"><span data-stu-id="8bb68-124">-Metric</span></span>
<span data-ttu-id="8bb68-125">建立公制設定</span><span class="sxs-lookup"><span data-stu-id="8bb68-125">To create metric setting</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MetricSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bb68-126">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="8bb68-126">-RetentionEnabled</span></span>
<span data-ttu-id="8bb68-127">啟用保留原則</span><span class="sxs-lookup"><span data-stu-id="8bb68-127">Enable Retention policy</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bb68-128">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="8bb68-128">-RetentionInDays</span></span>
<span data-ttu-id="8bb68-129">保留原則的保留天數</span><span class="sxs-lookup"><span data-stu-id="8bb68-129">Retention days for retention policy</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bb68-130">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="8bb68-130">-TimeGrain</span></span>
<span data-ttu-id="8bb68-131">TimeGrain （公制）設定</span><span class="sxs-lookup"><span data-stu-id="8bb68-131">TimeGrain for metric setting</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: MetricSettingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bb68-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bb68-132">CommonParameters</span></span>
<span data-ttu-id="8bb68-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8bb68-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bb68-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8bb68-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bb68-135">輸入</span><span class="sxs-lookup"><span data-stu-id="8bb68-135">INPUTS</span></span>

### <span data-ttu-id="8bb68-136">System.object</span><span class="sxs-lookup"><span data-stu-id="8bb68-136">System.String</span></span>

## <span data-ttu-id="8bb68-137">輸出</span><span class="sxs-lookup"><span data-stu-id="8bb68-137">OUTPUTS</span></span>

### <span data-ttu-id="8bb68-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings</span><span class="sxs-lookup"><span data-stu-id="8bb68-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings</span></span>

## <span data-ttu-id="8bb68-139">筆記</span><span class="sxs-lookup"><span data-stu-id="8bb68-139">NOTES</span></span>

## <span data-ttu-id="8bb68-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="8bb68-140">RELATED LINKS</span></span>
