---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
ms.openlocfilehash: 9c336c1bb2c2485c5bef691a5d5560a1b8795360
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443628"
---
# <span data-ttu-id="f1672-101">Get-AzureRmWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="f1672-101">Get-AzureRmWebAppSlotMetrics</span></span>

## <span data-ttu-id="f1672-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f1672-102">SYNOPSIS</span></span>
<span data-ttu-id="f1672-103">取得 Azure Web App 槽的指標。</span><span class="sxs-lookup"><span data-stu-id="f1672-103">Gets metrics for an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1672-104">句法</span><span class="sxs-lookup"><span data-stu-id="f1672-104">SYNTAX</span></span>

### <span data-ttu-id="f1672-105">S1</span><span class="sxs-lookup"><span data-stu-id="f1672-105">S1</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1672-106">S2</span><span class="sxs-lookup"><span data-stu-id="f1672-106">S2</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1672-107">說明</span><span class="sxs-lookup"><span data-stu-id="f1672-107">DESCRIPTION</span></span>
<span data-ttu-id="f1672-108">**AzureRmWebAppSlotMetrics** 會取得指定槽的 Web App 度量單位。</span><span class="sxs-lookup"><span data-stu-id="f1672-108">The **Get-AzureRmWebAppSlotMetrics** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="f1672-109">示例</span><span class="sxs-lookup"><span data-stu-id="f1672-109">EXAMPLES</span></span>

### <span data-ttu-id="f1672-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f1672-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="f1672-111">這個命令會每分鐘 (PT1M 的輪詢時間1分鐘內，以) StartTime 和 EndTime 之間的要求來取得指定的 Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="f1672-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="f1672-112">參數</span><span class="sxs-lookup"><span data-stu-id="f1672-112">PARAMETERS</span></span>

### <span data-ttu-id="f1672-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1672-113">-DefaultProfile</span></span>
<span data-ttu-id="f1672-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f1672-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1672-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="f1672-115">-EndTime</span></span>
<span data-ttu-id="f1672-116">UTC 的結束時間</span><span class="sxs-lookup"><span data-stu-id="f1672-116">End Time in UTC</span></span>

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

### <span data-ttu-id="f1672-117">-細微性</span><span class="sxs-lookup"><span data-stu-id="f1672-117">-Granularity</span></span>
<span data-ttu-id="f1672-118">細微性</span><span class="sxs-lookup"><span data-stu-id="f1672-118">Granularity</span></span>

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

### <span data-ttu-id="f1672-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="f1672-119">-InstanceDetails</span></span>
<span data-ttu-id="f1672-120">實例詳細資料</span><span class="sxs-lookup"><span data-stu-id="f1672-120">Instance Details</span></span>

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

### <span data-ttu-id="f1672-121">-度量單位</span><span class="sxs-lookup"><span data-stu-id="f1672-121">-Metrics</span></span>
<span data-ttu-id="f1672-122">指標</span><span class="sxs-lookup"><span data-stu-id="f1672-122">Metrics</span></span>

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

### <span data-ttu-id="f1672-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="f1672-123">-Name</span></span>
<span data-ttu-id="f1672-124">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="f1672-124">WebApp Name</span></span>

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

### <span data-ttu-id="f1672-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1672-125">-ResourceGroupName</span></span>
<span data-ttu-id="f1672-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="f1672-126">Resource Group Name</span></span>

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

### <span data-ttu-id="f1672-127">-槽</span><span class="sxs-lookup"><span data-stu-id="f1672-127">-Slot</span></span>
<span data-ttu-id="f1672-128">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="f1672-128">WebApp Slot Name</span></span>

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

### <span data-ttu-id="f1672-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f1672-129">-StartTime</span></span>
<span data-ttu-id="f1672-130">UTC 的開始時間</span><span class="sxs-lookup"><span data-stu-id="f1672-130">Start Time in UTC</span></span>

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

### <span data-ttu-id="f1672-131">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f1672-131">-WebApp</span></span>
<span data-ttu-id="f1672-132">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="f1672-132">WebApp Object</span></span>

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

### <span data-ttu-id="f1672-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1672-133">CommonParameters</span></span>
<span data-ttu-id="f1672-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f1672-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1672-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f1672-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1672-136">輸入</span><span class="sxs-lookup"><span data-stu-id="f1672-136">INPUTS</span></span>

### <span data-ttu-id="f1672-137">System.object</span><span class="sxs-lookup"><span data-stu-id="f1672-137">System.String</span></span>

### <span data-ttu-id="f1672-138">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="f1672-138">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="f1672-139">參數： WebApp (ByValue) </span><span class="sxs-lookup"><span data-stu-id="f1672-139">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="f1672-140">輸出</span><span class="sxs-lookup"><span data-stu-id="f1672-140">OUTPUTS</span></span>

### <span data-ttu-id="f1672-141">ResourceMetric 中的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="f1672-141">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="f1672-142">筆記</span><span class="sxs-lookup"><span data-stu-id="f1672-142">NOTES</span></span>

## <span data-ttu-id="f1672-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1672-143">RELATED LINKS</span></span>

[<span data-ttu-id="f1672-144">AzureRMAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="f1672-144">Get-AzureRMAppServicePlanMetrics</span></span>](./Get-AzureRmAppServicePlanMetrics.md)

[<span data-ttu-id="f1672-145">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f1672-145">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="f1672-146">AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f1672-146">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)
