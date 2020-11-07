---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azappserviceplanmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlanMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlanMetrics.md
ms.openlocfilehash: c08ae63999582fd220005dde84316a2f4421d7b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795005"
---
# <span data-ttu-id="35bb9-101">Get-AzAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="35bb9-101">Get-AzAppServicePlanMetrics</span></span>

## <span data-ttu-id="35bb9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="35bb9-102">SYNOPSIS</span></span>
<span data-ttu-id="35bb9-103">取得 Azure Web 服務方案度量單位。</span><span class="sxs-lookup"><span data-stu-id="35bb9-103">Gets Azure Web service plan metrics.</span></span>

## <span data-ttu-id="35bb9-104">句法</span><span class="sxs-lookup"><span data-stu-id="35bb9-104">SYNTAX</span></span>

### <span data-ttu-id="35bb9-105">S1</span><span class="sxs-lookup"><span data-stu-id="35bb9-105">S1</span></span>
```
Get-AzAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35bb9-106">S2</span><span class="sxs-lookup"><span data-stu-id="35bb9-106">S2</span></span>
```
Get-AzAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <AppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35bb9-107">說明</span><span class="sxs-lookup"><span data-stu-id="35bb9-107">DESCRIPTION</span></span>
<span data-ttu-id="35bb9-108">**AzAppServicePlanMetrics** 會取得 App 服務方案度量單位。</span><span class="sxs-lookup"><span data-stu-id="35bb9-108">The **Get-AzAppServicePlanMetrics** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="35bb9-109">示例</span><span class="sxs-lookup"><span data-stu-id="35bb9-109">EXAMPLES</span></span>

### <span data-ttu-id="35bb9-110">sr-1</span><span class="sxs-lookup"><span data-stu-id="35bb9-110">1:</span></span>
```
PS C:\>Get-AzAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["CPU Percentage"]
```

<span data-ttu-id="35bb9-111">這個命令會在每分鐘 (PT1M 輪詢時間1分鐘內，) StartTime 和 EndTime 之間取得 App 服務方案的 CPU 百分比</span><span class="sxs-lookup"><span data-stu-id="35bb9-111">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="35bb9-112">參數</span><span class="sxs-lookup"><span data-stu-id="35bb9-112">PARAMETERS</span></span>

### <span data-ttu-id="35bb9-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="35bb9-113">-AppServicePlan</span></span>
<span data-ttu-id="35bb9-114">App Service 方案物件</span><span class="sxs-lookup"><span data-stu-id="35bb9-114">App Service Plan Object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35bb9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35bb9-115">-DefaultProfile</span></span>
<span data-ttu-id="35bb9-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="35bb9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35bb9-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="35bb9-117">-EndTime</span></span>
<span data-ttu-id="35bb9-118">UTC 的結束時間</span><span class="sxs-lookup"><span data-stu-id="35bb9-118">End Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35bb9-119">-細微性</span><span class="sxs-lookup"><span data-stu-id="35bb9-119">-Granularity</span></span>
<span data-ttu-id="35bb9-120">細微性</span><span class="sxs-lookup"><span data-stu-id="35bb9-120">Granularity</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35bb9-121">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="35bb9-121">-InstanceDetails</span></span>
<span data-ttu-id="35bb9-122">實例詳細資料</span><span class="sxs-lookup"><span data-stu-id="35bb9-122">Instance Details</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35bb9-123">-度量單位</span><span class="sxs-lookup"><span data-stu-id="35bb9-123">-Metrics</span></span>
<span data-ttu-id="35bb9-124">指標</span><span class="sxs-lookup"><span data-stu-id="35bb9-124">Metrics</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35bb9-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="35bb9-125">-Name</span></span>
<span data-ttu-id="35bb9-126">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="35bb9-126">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35bb9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35bb9-127">-ResourceGroupName</span></span>
<span data-ttu-id="35bb9-128">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="35bb9-128">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35bb9-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="35bb9-129">-StartTime</span></span>
<span data-ttu-id="35bb9-130">UTC 的開始時間</span><span class="sxs-lookup"><span data-stu-id="35bb9-130">Start Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35bb9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35bb9-131">CommonParameters</span></span>
<span data-ttu-id="35bb9-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="35bb9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35bb9-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="35bb9-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35bb9-134">輸入</span><span class="sxs-lookup"><span data-stu-id="35bb9-134">INPUTS</span></span>

### <span data-ttu-id="35bb9-135">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="35bb9-135">ServerFarmWithRichSku</span></span>
<span data-ttu-id="35bb9-136">形參 "AppServicePlan" 接受管線中 "ServerFarmWithRichSku" 類型的值</span><span class="sxs-lookup"><span data-stu-id="35bb9-136">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="35bb9-137">輸出</span><span class="sxs-lookup"><span data-stu-id="35bb9-137">OUTPUTS</span></span>

## <span data-ttu-id="35bb9-138">筆記</span><span class="sxs-lookup"><span data-stu-id="35bb9-138">NOTES</span></span>

## <span data-ttu-id="35bb9-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="35bb9-139">RELATED LINKS</span></span>

