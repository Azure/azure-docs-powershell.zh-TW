---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppMetric.md
ms.openlocfilehash: 91b5de48805e458b771227ca9c92e9891be170e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797397"
---
# <span data-ttu-id="04925-101">Get-AzWebAppMetric</span><span class="sxs-lookup"><span data-stu-id="04925-101">Get-AzWebAppMetric</span></span>

## <span data-ttu-id="04925-102">摘要</span><span class="sxs-lookup"><span data-stu-id="04925-102">SYNOPSIS</span></span>
<span data-ttu-id="04925-103">取得 Azure Web App 度量單位。</span><span class="sxs-lookup"><span data-stu-id="04925-103">Gets Azure Web App metrics.</span></span>

## <span data-ttu-id="04925-104">句法</span><span class="sxs-lookup"><span data-stu-id="04925-104">SYNTAX</span></span>

### <span data-ttu-id="04925-105">S1</span><span class="sxs-lookup"><span data-stu-id="04925-105">S1</span></span>
```
Get-AzWebAppMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04925-106">S2</span><span class="sxs-lookup"><span data-stu-id="04925-106">S2</span></span>
```
Get-AzWebAppMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="04925-107">說明</span><span class="sxs-lookup"><span data-stu-id="04925-107">DESCRIPTION</span></span>
<span data-ttu-id="04925-108">**AzWebAppMetric** 會取得 Web App 的度量單位。</span><span class="sxs-lookup"><span data-stu-id="04925-108">The **Get-AzWebAppMetric** gets Web App metrics.</span></span>

## <span data-ttu-id="04925-109">示例</span><span class="sxs-lookup"><span data-stu-id="04925-109">EXAMPLES</span></span>

### <span data-ttu-id="04925-110">範例1</span><span class="sxs-lookup"><span data-stu-id="04925-110">Example 1</span></span>
```
PS C:\> Get-AzAppServicePlanMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "Requests"
```

<span data-ttu-id="04925-111">這個命令會在 StartTime 和 EndTime 之間每分鐘 (PT1M 的輪詢時間1分鐘) 內，取得 Web App ContosoWebApp 的要求。</span><span class="sxs-lookup"><span data-stu-id="04925-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="04925-112">參數</span><span class="sxs-lookup"><span data-stu-id="04925-112">PARAMETERS</span></span>

### <span data-ttu-id="04925-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04925-113">-DefaultProfile</span></span>
<span data-ttu-id="04925-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="04925-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04925-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="04925-115">-EndTime</span></span>
<span data-ttu-id="04925-116">UTC 的結束時間</span><span class="sxs-lookup"><span data-stu-id="04925-116">End Time in UTC</span></span>

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

### <span data-ttu-id="04925-117">-細微性</span><span class="sxs-lookup"><span data-stu-id="04925-117">-Granularity</span></span>
<span data-ttu-id="04925-118">細微性</span><span class="sxs-lookup"><span data-stu-id="04925-118">Granularity</span></span>

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

### <span data-ttu-id="04925-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="04925-119">-InstanceDetails</span></span>
<span data-ttu-id="04925-120">實例詳細資料</span><span class="sxs-lookup"><span data-stu-id="04925-120">Instance Details</span></span>

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

### <span data-ttu-id="04925-121">-度量單位</span><span class="sxs-lookup"><span data-stu-id="04925-121">-Metrics</span></span>
<span data-ttu-id="04925-122">字串陣列形式的度量單位</span><span class="sxs-lookup"><span data-stu-id="04925-122">Metrics as a string array</span></span>

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

### <span data-ttu-id="04925-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="04925-123">-Name</span></span>
<span data-ttu-id="04925-124">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="04925-124">WebApp Name</span></span>

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

### <span data-ttu-id="04925-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04925-125">-ResourceGroupName</span></span>
<span data-ttu-id="04925-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="04925-126">Resource Group Name</span></span>

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

### <span data-ttu-id="04925-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="04925-127">-StartTime</span></span>
<span data-ttu-id="04925-128">UTC 的開始時間</span><span class="sxs-lookup"><span data-stu-id="04925-128">Start Time in UTC</span></span>

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

### <span data-ttu-id="04925-129">-WebApp</span><span class="sxs-lookup"><span data-stu-id="04925-129">-WebApp</span></span>
<span data-ttu-id="04925-130">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="04925-130">WebApp object</span></span>

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

### <span data-ttu-id="04925-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04925-131">CommonParameters</span></span>
<span data-ttu-id="04925-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="04925-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04925-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="04925-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04925-134">輸入</span><span class="sxs-lookup"><span data-stu-id="04925-134">INPUTS</span></span>

### <span data-ttu-id="04925-135">System.object</span><span class="sxs-lookup"><span data-stu-id="04925-135">System.String</span></span>

### <span data-ttu-id="04925-136">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="04925-136">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="04925-137">輸出</span><span class="sxs-lookup"><span data-stu-id="04925-137">OUTPUTS</span></span>

### <span data-ttu-id="04925-138">ResourceMetric 中的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="04925-138">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="04925-139">筆記</span><span class="sxs-lookup"><span data-stu-id="04925-139">NOTES</span></span>

## <span data-ttu-id="04925-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="04925-140">RELATED LINKS</span></span>

[<span data-ttu-id="04925-141">AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="04925-141">Get-AzWebAppCertificate</span></span>](./Get-AzWebAppCertificate.md)

