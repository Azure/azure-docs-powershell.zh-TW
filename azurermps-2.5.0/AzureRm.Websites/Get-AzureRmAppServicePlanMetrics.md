---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplanmetrics
schema: 2.0.0
ms.openlocfilehash: 097b4c5ff6a4a9be32889f104c8e2c8fe0058b13
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93799706"
---
# <span data-ttu-id="2118f-101">Get-AzureRmAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="2118f-101">Get-AzureRmAppServicePlanMetrics</span></span>

## <span data-ttu-id="2118f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2118f-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2118f-103">句法</span><span class="sxs-lookup"><span data-stu-id="2118f-103">SYNTAX</span></span>

### <span data-ttu-id="2118f-104">S1</span><span class="sxs-lookup"><span data-stu-id="2118f-104">S1</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2118f-105">S2</span><span class="sxs-lookup"><span data-stu-id="2118f-105">S2</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <AppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2118f-106">說明</span><span class="sxs-lookup"><span data-stu-id="2118f-106">DESCRIPTION</span></span>
<span data-ttu-id="2118f-107">**AzureRmAppServicePlanMetrics** 會取得 App 服務方案度量單位。</span><span class="sxs-lookup"><span data-stu-id="2118f-107">The **Get-AzureRmAppServicePlanMetrics** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="2118f-108">示例</span><span class="sxs-lookup"><span data-stu-id="2118f-108">EXAMPLES</span></span>

### <span data-ttu-id="2118f-109">sr-1</span><span class="sxs-lookup"><span data-stu-id="2118f-109">1:</span></span>
```
PS C:\>Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["CPU Percentage"]
```

<span data-ttu-id="2118f-110">這個命令會在每分鐘 (PT1M 輪詢時間1分鐘內，) StartTime 和 EndTime 之間取得 App 服務方案的 CPU 百分比</span><span class="sxs-lookup"><span data-stu-id="2118f-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="2118f-111">參數</span><span class="sxs-lookup"><span data-stu-id="2118f-111">PARAMETERS</span></span>

### <span data-ttu-id="2118f-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2118f-112">-AppServicePlan</span></span>
<span data-ttu-id="2118f-113">App Service 方案物件</span><span class="sxs-lookup"><span data-stu-id="2118f-113">App Service Plan Object</span></span>

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

### <span data-ttu-id="2118f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2118f-114">-DefaultProfile</span></span>
<span data-ttu-id="2118f-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2118f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2118f-116">-EndTime</span><span class="sxs-lookup"><span data-stu-id="2118f-116">-EndTime</span></span>
<span data-ttu-id="2118f-117">UTC 的結束時間</span><span class="sxs-lookup"><span data-stu-id="2118f-117">End Time in UTC</span></span>

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

### <span data-ttu-id="2118f-118">-細微性</span><span class="sxs-lookup"><span data-stu-id="2118f-118">-Granularity</span></span>
<span data-ttu-id="2118f-119">細微性</span><span class="sxs-lookup"><span data-stu-id="2118f-119">Granularity</span></span>

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

### <span data-ttu-id="2118f-120">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="2118f-120">-InstanceDetails</span></span>
<span data-ttu-id="2118f-121">實例詳細資料</span><span class="sxs-lookup"><span data-stu-id="2118f-121">Instance Details</span></span>

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

### <span data-ttu-id="2118f-122">-度量單位</span><span class="sxs-lookup"><span data-stu-id="2118f-122">-Metrics</span></span>
<span data-ttu-id="2118f-123">指標</span><span class="sxs-lookup"><span data-stu-id="2118f-123">Metrics</span></span>

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

### <span data-ttu-id="2118f-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="2118f-124">-Name</span></span>
<span data-ttu-id="2118f-125">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="2118f-125">App Service Plan Name</span></span>

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

### <span data-ttu-id="2118f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2118f-126">-ResourceGroupName</span></span>
<span data-ttu-id="2118f-127">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="2118f-127">Resource Group Name</span></span>

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

### <span data-ttu-id="2118f-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2118f-128">-StartTime</span></span>
<span data-ttu-id="2118f-129">UTC 的開始時間</span><span class="sxs-lookup"><span data-stu-id="2118f-129">Start Time in UTC</span></span>

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

### <span data-ttu-id="2118f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2118f-130">CommonParameters</span></span>
<span data-ttu-id="2118f-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2118f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2118f-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2118f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2118f-133">輸入</span><span class="sxs-lookup"><span data-stu-id="2118f-133">INPUTS</span></span>

### <span data-ttu-id="2118f-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="2118f-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="2118f-135">形參 "AppServicePlan" 接受管線中 "ServerFarmWithRichSku" 類型的值</span><span class="sxs-lookup"><span data-stu-id="2118f-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="2118f-136">輸出</span><span class="sxs-lookup"><span data-stu-id="2118f-136">OUTPUTS</span></span>

## <span data-ttu-id="2118f-137">筆記</span><span class="sxs-lookup"><span data-stu-id="2118f-137">NOTES</span></span>

## <span data-ttu-id="2118f-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="2118f-138">RELATED LINKS</span></span>

