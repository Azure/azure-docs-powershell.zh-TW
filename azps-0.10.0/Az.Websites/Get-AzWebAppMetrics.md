---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppMetrics.md
ms.openlocfilehash: 9a3aeabc3eb38127b37ca4ab6a12975c51daea5b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794995"
---
# <span data-ttu-id="01b68-101">Get-AzWebAppMetrics</span><span class="sxs-lookup"><span data-stu-id="01b68-101">Get-AzWebAppMetrics</span></span>

## <span data-ttu-id="01b68-102">摘要</span><span class="sxs-lookup"><span data-stu-id="01b68-102">SYNOPSIS</span></span>
<span data-ttu-id="01b68-103">取得 Azure Web App 度量單位。</span><span class="sxs-lookup"><span data-stu-id="01b68-103">Gets Azure Web App metrics.</span></span>

## <span data-ttu-id="01b68-104">句法</span><span class="sxs-lookup"><span data-stu-id="01b68-104">SYNTAX</span></span>

### <span data-ttu-id="01b68-105">S1</span><span class="sxs-lookup"><span data-stu-id="01b68-105">S1</span></span>
```
Get-AzWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01b68-106">S2</span><span class="sxs-lookup"><span data-stu-id="01b68-106">S2</span></span>
```
Get-AzWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01b68-107">說明</span><span class="sxs-lookup"><span data-stu-id="01b68-107">DESCRIPTION</span></span>
<span data-ttu-id="01b68-108">**AzWebAppMetrics** 會取得 Web App 的度量單位。</span><span class="sxs-lookup"><span data-stu-id="01b68-108">The **Get-AzWebAppMetrics** gets Web App metrics.</span></span>

## <span data-ttu-id="01b68-109">示例</span><span class="sxs-lookup"><span data-stu-id="01b68-109">EXAMPLES</span></span>

### <span data-ttu-id="01b68-110">範例1</span><span class="sxs-lookup"><span data-stu-id="01b68-110">Example 1</span></span>
```
PS C:\> Get-AzAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="01b68-111">這個命令會在 StartTime 和 EndTime 之間每分鐘 (PT1M 的輪詢時間1分鐘) 內，取得 Web App ContosoWebApp 的要求。</span><span class="sxs-lookup"><span data-stu-id="01b68-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="01b68-112">參數</span><span class="sxs-lookup"><span data-stu-id="01b68-112">PARAMETERS</span></span>

### <span data-ttu-id="01b68-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01b68-113">-DefaultProfile</span></span>
<span data-ttu-id="01b68-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="01b68-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01b68-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="01b68-115">-EndTime</span></span>
<span data-ttu-id="01b68-116">UTC 的結束時間</span><span class="sxs-lookup"><span data-stu-id="01b68-116">End Time in UTC</span></span>

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

### <span data-ttu-id="01b68-117">-細微性</span><span class="sxs-lookup"><span data-stu-id="01b68-117">-Granularity</span></span>
<span data-ttu-id="01b68-118">細微性</span><span class="sxs-lookup"><span data-stu-id="01b68-118">Granularity</span></span>

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

### <span data-ttu-id="01b68-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="01b68-119">-InstanceDetails</span></span>
<span data-ttu-id="01b68-120">實例詳細資料</span><span class="sxs-lookup"><span data-stu-id="01b68-120">Instance Details</span></span>

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

### <span data-ttu-id="01b68-121">-度量單位</span><span class="sxs-lookup"><span data-stu-id="01b68-121">-Metrics</span></span>
<span data-ttu-id="01b68-122">字串陣列形式的度量單位</span><span class="sxs-lookup"><span data-stu-id="01b68-122">Metrics as a string array</span></span>

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

### <span data-ttu-id="01b68-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="01b68-123">-Name</span></span>
<span data-ttu-id="01b68-124">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="01b68-124">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01b68-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01b68-125">-ResourceGroupName</span></span>
<span data-ttu-id="01b68-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="01b68-126">Resource Group Name</span></span>

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

### <span data-ttu-id="01b68-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="01b68-127">-StartTime</span></span>
<span data-ttu-id="01b68-128">UTC 的開始時間</span><span class="sxs-lookup"><span data-stu-id="01b68-128">Start Time in UTC</span></span>

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

### <span data-ttu-id="01b68-129">-WebApp</span><span class="sxs-lookup"><span data-stu-id="01b68-129">-WebApp</span></span>
<span data-ttu-id="01b68-130">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="01b68-130">WebApp object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01b68-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01b68-131">CommonParameters</span></span>
<span data-ttu-id="01b68-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="01b68-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01b68-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="01b68-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01b68-134">輸入</span><span class="sxs-lookup"><span data-stu-id="01b68-134">INPUTS</span></span>

### <span data-ttu-id="01b68-135">網站地圖</span><span class="sxs-lookup"><span data-stu-id="01b68-135">Site</span></span>
<span data-ttu-id="01b68-136">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="01b68-136">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="01b68-137">輸出</span><span class="sxs-lookup"><span data-stu-id="01b68-137">OUTPUTS</span></span>

## <span data-ttu-id="01b68-138">筆記</span><span class="sxs-lookup"><span data-stu-id="01b68-138">NOTES</span></span>

## <span data-ttu-id="01b68-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="01b68-139">RELATED LINKS</span></span>

[<span data-ttu-id="01b68-140">AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="01b68-140">Get-AzWebAppCertificate</span></span>](./Get-AzWebAppCertificate.md)

