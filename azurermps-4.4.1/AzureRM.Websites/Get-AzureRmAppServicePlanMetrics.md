---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlanMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlanMetrics.md
ms.openlocfilehash: 65892738ac244a0af82e017efc015c0113a6ed72
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624523"
---
# <span data-ttu-id="b692c-101">Get-AzureRmAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="b692c-101">Get-AzureRmAppServicePlanMetrics</span></span>

## <span data-ttu-id="b692c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b692c-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b692c-103">句法</span><span class="sxs-lookup"><span data-stu-id="b692c-103">SYNTAX</span></span>

### <span data-ttu-id="b692c-104">S1</span><span class="sxs-lookup"><span data-stu-id="b692c-104">S1</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b692c-105">S2</span><span class="sxs-lookup"><span data-stu-id="b692c-105">S2</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <ServerFarmWithRichSku>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b692c-106">說明</span><span class="sxs-lookup"><span data-stu-id="b692c-106">DESCRIPTION</span></span>
<span data-ttu-id="b692c-107">**AzureRmAppServicePlanMetrics** 會取得 App 服務方案度量單位。</span><span class="sxs-lookup"><span data-stu-id="b692c-107">The **Get-AzureRmAppServicePlanMetrics** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="b692c-108">示例</span><span class="sxs-lookup"><span data-stu-id="b692c-108">EXAMPLES</span></span>

### <span data-ttu-id="b692c-109">sr-1</span><span class="sxs-lookup"><span data-stu-id="b692c-109">1:</span></span>
```
PS C:\>Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["CPU Percentage"]
```

<span data-ttu-id="b692c-110">這個命令會在每分鐘 (PT1M 輪詢時間1分鐘內，) StartTime 和 EndTime 之間取得 App 服務方案的 CPU 百分比</span><span class="sxs-lookup"><span data-stu-id="b692c-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="b692c-111">參數</span><span class="sxs-lookup"><span data-stu-id="b692c-111">PARAMETERS</span></span>

### <span data-ttu-id="b692c-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b692c-112">-AppServicePlan</span></span>
<span data-ttu-id="b692c-113">App Service 方案物件</span><span class="sxs-lookup"><span data-stu-id="b692c-113">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b692c-114">-EndTime</span><span class="sxs-lookup"><span data-stu-id="b692c-114">-EndTime</span></span>
<span data-ttu-id="b692c-115">UTC 的結束時間</span><span class="sxs-lookup"><span data-stu-id="b692c-115">End Time in UTC</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b692c-116">-細微性</span><span class="sxs-lookup"><span data-stu-id="b692c-116">-Granularity</span></span>
<span data-ttu-id="b692c-117">細微性</span><span class="sxs-lookup"><span data-stu-id="b692c-117">Granularity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b692c-118">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="b692c-118">-InstanceDetails</span></span>
<span data-ttu-id="b692c-119">實例詳細資料</span><span class="sxs-lookup"><span data-stu-id="b692c-119">Instance Details</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b692c-120">-度量單位</span><span class="sxs-lookup"><span data-stu-id="b692c-120">-Metrics</span></span>
<span data-ttu-id="b692c-121">指標</span><span class="sxs-lookup"><span data-stu-id="b692c-121">Metrics</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b692c-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="b692c-122">-Name</span></span>
<span data-ttu-id="b692c-123">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="b692c-123">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b692c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b692c-124">-ResourceGroupName</span></span>
<span data-ttu-id="b692c-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="b692c-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b692c-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b692c-126">-StartTime</span></span>
<span data-ttu-id="b692c-127">UTC 的開始時間</span><span class="sxs-lookup"><span data-stu-id="b692c-127">Start Time in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b692c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b692c-128">-DefaultProfile</span></span>
<span data-ttu-id="b692c-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b692c-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b692c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b692c-130">CommonParameters</span></span>
<span data-ttu-id="b692c-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b692c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b692c-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b692c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b692c-133">輸入</span><span class="sxs-lookup"><span data-stu-id="b692c-133">INPUTS</span></span>

### <span data-ttu-id="b692c-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="b692c-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="b692c-135">形參 "AppServicePlan" 接受管線中 "ServerFarmWithRichSku" 類型的值</span><span class="sxs-lookup"><span data-stu-id="b692c-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="b692c-136">輸出</span><span class="sxs-lookup"><span data-stu-id="b692c-136">OUTPUTS</span></span>

## <span data-ttu-id="b692c-137">筆記</span><span class="sxs-lookup"><span data-stu-id="b692c-137">NOTES</span></span>

## <span data-ttu-id="b692c-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="b692c-138">RELATED LINKS</span></span>

