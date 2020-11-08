---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotMetric.md
ms.openlocfilehash: 27800007756f8de91f23feab2f3cc1bd5206aa76
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970760"
---
# <span data-ttu-id="0eb32-101">Get-AzWebAppSlotMetric</span><span class="sxs-lookup"><span data-stu-id="0eb32-101">Get-AzWebAppSlotMetric</span></span>

## <span data-ttu-id="0eb32-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0eb32-102">SYNOPSIS</span></span>
<span data-ttu-id="0eb32-103">取得 Azure Web App 槽的指標。</span><span class="sxs-lookup"><span data-stu-id="0eb32-103">Gets metrics for an Azure Web App slot.</span></span>

## <span data-ttu-id="0eb32-104">句法</span><span class="sxs-lookup"><span data-stu-id="0eb32-104">SYNTAX</span></span>

### <span data-ttu-id="0eb32-105">S1</span><span class="sxs-lookup"><span data-stu-id="0eb32-105">S1</span></span>
```
Get-AzWebAppSlotMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0eb32-106">S2</span><span class="sxs-lookup"><span data-stu-id="0eb32-106">S2</span></span>
```
Get-AzWebAppSlotMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0eb32-107">說明</span><span class="sxs-lookup"><span data-stu-id="0eb32-107">DESCRIPTION</span></span>
<span data-ttu-id="0eb32-108">**AzWebAppSlotMetric** 會取得指定槽的 Web App 度量單位。</span><span class="sxs-lookup"><span data-stu-id="0eb32-108">The **Get-AzWebAppSlotMetric** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="0eb32-109">示例</span><span class="sxs-lookup"><span data-stu-id="0eb32-109">EXAMPLES</span></span>

### <span data-ttu-id="0eb32-110">範例1</span><span class="sxs-lookup"><span data-stu-id="0eb32-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="0eb32-111">這個命令會每分鐘 (PT1M 的輪詢時間1分鐘內，以) StartTime 和 EndTime 之間的要求來取得指定的 Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="0eb32-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="0eb32-112">參數</span><span class="sxs-lookup"><span data-stu-id="0eb32-112">PARAMETERS</span></span>

### <span data-ttu-id="0eb32-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eb32-113">-DefaultProfile</span></span>
<span data-ttu-id="0eb32-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0eb32-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0eb32-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="0eb32-115">-EndTime</span></span>
<span data-ttu-id="0eb32-116">UTC 的結束時間</span><span class="sxs-lookup"><span data-stu-id="0eb32-116">End Time in UTC</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb32-117">-細微性</span><span class="sxs-lookup"><span data-stu-id="0eb32-117">-Granularity</span></span>
<span data-ttu-id="0eb32-118">細微性</span><span class="sxs-lookup"><span data-stu-id="0eb32-118">Granularity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb32-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="0eb32-119">-InstanceDetails</span></span>
<span data-ttu-id="0eb32-120">實例詳細資料</span><span class="sxs-lookup"><span data-stu-id="0eb32-120">Instance Details</span></span>

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

### <span data-ttu-id="0eb32-121">-度量單位</span><span class="sxs-lookup"><span data-stu-id="0eb32-121">-Metrics</span></span>
<span data-ttu-id="0eb32-122">指標</span><span class="sxs-lookup"><span data-stu-id="0eb32-122">Metrics</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb32-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="0eb32-123">-Name</span></span>
<span data-ttu-id="0eb32-124">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="0eb32-124">WebApp Name</span></span>

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

### <span data-ttu-id="0eb32-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eb32-125">-ResourceGroupName</span></span>
<span data-ttu-id="0eb32-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="0eb32-126">Resource Group Name</span></span>

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

### <span data-ttu-id="0eb32-127">-槽</span><span class="sxs-lookup"><span data-stu-id="0eb32-127">-Slot</span></span>
<span data-ttu-id="0eb32-128">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="0eb32-128">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb32-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0eb32-129">-StartTime</span></span>
<span data-ttu-id="0eb32-130">UTC 的開始時間</span><span class="sxs-lookup"><span data-stu-id="0eb32-130">Start Time in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb32-131">-WebApp</span><span class="sxs-lookup"><span data-stu-id="0eb32-131">-WebApp</span></span>
<span data-ttu-id="0eb32-132">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="0eb32-132">WebApp Object</span></span>

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

### <span data-ttu-id="0eb32-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eb32-133">CommonParameters</span></span>
<span data-ttu-id="0eb32-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0eb32-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eb32-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0eb32-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eb32-136">輸入</span><span class="sxs-lookup"><span data-stu-id="0eb32-136">INPUTS</span></span>

### <span data-ttu-id="0eb32-137">System.object</span><span class="sxs-lookup"><span data-stu-id="0eb32-137">System.String</span></span>

### <span data-ttu-id="0eb32-138">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="0eb32-138">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0eb32-139">輸出</span><span class="sxs-lookup"><span data-stu-id="0eb32-139">OUTPUTS</span></span>

### <span data-ttu-id="0eb32-140">ResourceMetric 中的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="0eb32-140">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="0eb32-141">筆記</span><span class="sxs-lookup"><span data-stu-id="0eb32-141">NOTES</span></span>

## <span data-ttu-id="0eb32-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="0eb32-142">RELATED LINKS</span></span>

[<span data-ttu-id="0eb32-143">AzAppServicePlanMetric</span><span class="sxs-lookup"><span data-stu-id="0eb32-143">Get-AzAppServicePlanMetric</span></span>](./Get-AzAppServicePlanMetric.md)

[<span data-ttu-id="0eb32-144">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0eb32-144">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="0eb32-145">AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0eb32-145">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)