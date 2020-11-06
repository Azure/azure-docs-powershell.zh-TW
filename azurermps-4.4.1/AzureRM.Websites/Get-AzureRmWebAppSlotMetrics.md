---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
ms.openlocfilehash: 93af61d0554435fae4b9d87170b9202026644e49
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455572"
---
# <span data-ttu-id="f7344-101">Get-AzureRmWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="f7344-101">Get-AzureRmWebAppSlotMetrics</span></span>

## <span data-ttu-id="f7344-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f7344-102">SYNOPSIS</span></span>
<span data-ttu-id="f7344-103">取得 Azure Web App 槽的指標。</span><span class="sxs-lookup"><span data-stu-id="f7344-103">Gets metrics for an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7344-104">句法</span><span class="sxs-lookup"><span data-stu-id="f7344-104">SYNTAX</span></span>

### <span data-ttu-id="f7344-105">S1</span><span class="sxs-lookup"><span data-stu-id="f7344-105">S1</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7344-106">S2</span><span class="sxs-lookup"><span data-stu-id="f7344-106">S2</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7344-107">說明</span><span class="sxs-lookup"><span data-stu-id="f7344-107">DESCRIPTION</span></span>
<span data-ttu-id="f7344-108">**AzureRmWebAppSlotMetrics** 會取得指定槽的 Web App 度量單位。</span><span class="sxs-lookup"><span data-stu-id="f7344-108">The **Get-AzureRmWebAppSlotMetrics** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="f7344-109">示例</span><span class="sxs-lookup"><span data-stu-id="f7344-109">EXAMPLES</span></span>

### <span data-ttu-id="f7344-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f7344-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="f7344-111">這個命令會每分鐘 (PT1M 的輪詢時間1分鐘內，以) StartTime 和 EndTime 之間的要求來取得指定的 Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="f7344-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="f7344-112">參數</span><span class="sxs-lookup"><span data-stu-id="f7344-112">PARAMETERS</span></span>

### <span data-ttu-id="f7344-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="f7344-113">-EndTime</span></span>
<span data-ttu-id="f7344-114">UTC 的結束時間</span><span class="sxs-lookup"><span data-stu-id="f7344-114">End Time in UTC</span></span>

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

### <span data-ttu-id="f7344-115">-細微性</span><span class="sxs-lookup"><span data-stu-id="f7344-115">-Granularity</span></span>
<span data-ttu-id="f7344-116">細微性</span><span class="sxs-lookup"><span data-stu-id="f7344-116">Granularity</span></span>

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

### <span data-ttu-id="f7344-117">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="f7344-117">-InstanceDetails</span></span>
<span data-ttu-id="f7344-118">實例詳細資料</span><span class="sxs-lookup"><span data-stu-id="f7344-118">Instance Details</span></span>

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

### <span data-ttu-id="f7344-119">-度量單位</span><span class="sxs-lookup"><span data-stu-id="f7344-119">-Metrics</span></span>
<span data-ttu-id="f7344-120">指標</span><span class="sxs-lookup"><span data-stu-id="f7344-120">Metrics</span></span>

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

### <span data-ttu-id="f7344-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="f7344-121">-Name</span></span>
<span data-ttu-id="f7344-122">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="f7344-122">WebApp Name</span></span>

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

### <span data-ttu-id="f7344-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7344-123">-ResourceGroupName</span></span>
<span data-ttu-id="f7344-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="f7344-124">Resource Group Name</span></span>

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

### <span data-ttu-id="f7344-125">-槽</span><span class="sxs-lookup"><span data-stu-id="f7344-125">-Slot</span></span>
<span data-ttu-id="f7344-126">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="f7344-126">WebApp Slot Name</span></span>

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

### <span data-ttu-id="f7344-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f7344-127">-StartTime</span></span>
<span data-ttu-id="f7344-128">UTC 的開始時間</span><span class="sxs-lookup"><span data-stu-id="f7344-128">Start Time in UTC</span></span>

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

### <span data-ttu-id="f7344-129">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f7344-129">-WebApp</span></span>
<span data-ttu-id="f7344-130">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="f7344-130">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7344-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7344-131">-DefaultProfile</span></span>
<span data-ttu-id="f7344-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7344-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7344-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7344-133">CommonParameters</span></span>
<span data-ttu-id="f7344-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f7344-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7344-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f7344-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7344-136">輸入</span><span class="sxs-lookup"><span data-stu-id="f7344-136">INPUTS</span></span>

### <span data-ttu-id="f7344-137">網站地圖</span><span class="sxs-lookup"><span data-stu-id="f7344-137">Site</span></span>
<span data-ttu-id="f7344-138">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="f7344-138">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f7344-139">輸出</span><span class="sxs-lookup"><span data-stu-id="f7344-139">OUTPUTS</span></span>

## <span data-ttu-id="f7344-140">筆記</span><span class="sxs-lookup"><span data-stu-id="f7344-140">NOTES</span></span>

## <span data-ttu-id="f7344-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7344-141">RELATED LINKS</span></span>

[<span data-ttu-id="f7344-142">AzureRMAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="f7344-142">Get-AzureRMAppServicePlanMetrics</span></span>](./Get-AzureRmAppServicePlanMetrics.md)

[<span data-ttu-id="f7344-143">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f7344-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="f7344-144">AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f7344-144">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)
