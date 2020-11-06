---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppMetrics.md
ms.openlocfilehash: 47fa876ff021dd920627ce4f08089c5fd04fb885
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448154"
---
# <span data-ttu-id="43b02-101">Get-AzureRmWebAppMetrics</span><span class="sxs-lookup"><span data-stu-id="43b02-101">Get-AzureRmWebAppMetrics</span></span>

## <span data-ttu-id="43b02-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43b02-102">SYNOPSIS</span></span>
<span data-ttu-id="43b02-103">取得 Azure Web App 度量單位。</span><span class="sxs-lookup"><span data-stu-id="43b02-103">Gets Azure Web App metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43b02-104">句法</span><span class="sxs-lookup"><span data-stu-id="43b02-104">SYNTAX</span></span>

### <span data-ttu-id="43b02-105">S1</span><span class="sxs-lookup"><span data-stu-id="43b02-105">S1</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43b02-106">S2</span><span class="sxs-lookup"><span data-stu-id="43b02-106">S2</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="43b02-107">說明</span><span class="sxs-lookup"><span data-stu-id="43b02-107">DESCRIPTION</span></span>
<span data-ttu-id="43b02-108">**AzureRmWebAppMetrics** 會取得 Web App 的度量單位。</span><span class="sxs-lookup"><span data-stu-id="43b02-108">The **Get-AzureRmWebAppMetrics** gets Web App metrics.</span></span>

## <span data-ttu-id="43b02-109">示例</span><span class="sxs-lookup"><span data-stu-id="43b02-109">EXAMPLES</span></span>

### <span data-ttu-id="43b02-110">範例1</span><span class="sxs-lookup"><span data-stu-id="43b02-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "Requests"
```

<span data-ttu-id="43b02-111">這個命令會在 StartTime 和 EndTime 之間每分鐘 (PT1M 的輪詢時間1分鐘) 內，取得 Web App ContosoWebApp 的要求。</span><span class="sxs-lookup"><span data-stu-id="43b02-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="43b02-112">參數</span><span class="sxs-lookup"><span data-stu-id="43b02-112">PARAMETERS</span></span>

### <span data-ttu-id="43b02-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43b02-113">-DefaultProfile</span></span>
<span data-ttu-id="43b02-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="43b02-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43b02-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="43b02-115">-EndTime</span></span>
<span data-ttu-id="43b02-116">UTC 的結束時間</span><span class="sxs-lookup"><span data-stu-id="43b02-116">End Time in UTC</span></span>

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

### <span data-ttu-id="43b02-117">-細微性</span><span class="sxs-lookup"><span data-stu-id="43b02-117">-Granularity</span></span>
<span data-ttu-id="43b02-118">細微性</span><span class="sxs-lookup"><span data-stu-id="43b02-118">Granularity</span></span>

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

### <span data-ttu-id="43b02-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="43b02-119">-InstanceDetails</span></span>
<span data-ttu-id="43b02-120">實例詳細資料</span><span class="sxs-lookup"><span data-stu-id="43b02-120">Instance Details</span></span>

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

### <span data-ttu-id="43b02-121">-度量單位</span><span class="sxs-lookup"><span data-stu-id="43b02-121">-Metrics</span></span>
<span data-ttu-id="43b02-122">字串陣列形式的度量單位</span><span class="sxs-lookup"><span data-stu-id="43b02-122">Metrics as a string array</span></span>

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

### <span data-ttu-id="43b02-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="43b02-123">-Name</span></span>
<span data-ttu-id="43b02-124">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="43b02-124">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43b02-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43b02-125">-ResourceGroupName</span></span>
<span data-ttu-id="43b02-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="43b02-126">Resource Group Name</span></span>

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

### <span data-ttu-id="43b02-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="43b02-127">-StartTime</span></span>
<span data-ttu-id="43b02-128">UTC 的開始時間</span><span class="sxs-lookup"><span data-stu-id="43b02-128">Start Time in UTC</span></span>

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

### <span data-ttu-id="43b02-129">-WebApp</span><span class="sxs-lookup"><span data-stu-id="43b02-129">-WebApp</span></span>
<span data-ttu-id="43b02-130">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="43b02-130">WebApp object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43b02-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43b02-131">CommonParameters</span></span>
<span data-ttu-id="43b02-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43b02-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43b02-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="43b02-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43b02-134">輸入</span><span class="sxs-lookup"><span data-stu-id="43b02-134">INPUTS</span></span>

### <span data-ttu-id="43b02-135">System.object</span><span class="sxs-lookup"><span data-stu-id="43b02-135">System.String</span></span>

### <span data-ttu-id="43b02-136">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="43b02-136">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="43b02-137">參數： WebApp (ByValue) </span><span class="sxs-lookup"><span data-stu-id="43b02-137">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="43b02-138">輸出</span><span class="sxs-lookup"><span data-stu-id="43b02-138">OUTPUTS</span></span>

### <span data-ttu-id="43b02-139">ResourceMetric 中的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="43b02-139">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="43b02-140">筆記</span><span class="sxs-lookup"><span data-stu-id="43b02-140">NOTES</span></span>

## <span data-ttu-id="43b02-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="43b02-141">RELATED LINKS</span></span>

[<span data-ttu-id="43b02-142">AzureRmWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="43b02-142">Get-AzureRmWebAppCertificate</span></span>](./Get-AzureRmWebAppCertificate.md)

