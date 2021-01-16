---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Disable-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: 3747109d13fd4224b0f86bc5ecf2992ed4229487
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278604"
---
# <span data-ttu-id="e0600-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="e0600-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="e0600-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e0600-102">SYNOPSIS</span></span>
<span data-ttu-id="e0600-103">關閉 Iot 匯總通知</span><span class="sxs-lookup"><span data-stu-id="e0600-103">Dismiss Iot aggregated alert</span></span>

## <span data-ttu-id="e0600-104">句法</span><span class="sxs-lookup"><span data-stu-id="e0600-104">SYNTAX</span></span>

### <span data-ttu-id="e0600-105">SolutionLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="e0600-105">SolutionLevelResource (Default)</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0600-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e0600-106">InputObject</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -InputObject <PSIoTSecurityAggregatedAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0600-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0600-107">ResourceId</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0600-108">說明</span><span class="sxs-lookup"><span data-stu-id="e0600-108">DESCRIPTION</span></span>
<span data-ttu-id="e0600-109">Disable-AzIotSecurityAnalyticsAggregatedAlert Cmdlet 會在 iot 中樞的裝置上關閉特定的 aggragated 通知。</span><span class="sxs-lookup"><span data-stu-id="e0600-109">The Disable-AzIotSecurityAnalyticsAggregatedAlert cmdlet dismisses a specific aggragated alert on devices of iot hub.</span></span> <span data-ttu-id="e0600-110">[匯總警示] 的名稱是 [警示類型] 與 [警示 aggragted 日期] 的組合，並以 "/" 分隔。</span><span class="sxs-lookup"><span data-stu-id="e0600-110">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="e0600-111">示例</span><span class="sxs-lookup"><span data-stu-id="e0600-111">EXAMPLES</span></span>

### <span data-ttu-id="e0600-112">範例1</span><span class="sxs-lookup"><span data-stu-id="e0600-112">Example 1</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolutionName" -Name "IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="e0600-113">關閉匯總警報「IoT_SucessfulLocalLogin/2020 年3月」 (名稱與警示類型及其匯總日期) 從資源群組 "MyResourceGroup" 中的 IoT 安全解決方案 "MySolutionName"</span><span class="sxs-lookup"><span data-stu-id="e0600-113">Dismiss aggregated alert "IoT_SucessfulLocalLogin/2020-03-15" (name combined from alert type and its aggregated date) from the IoT security solution "MySolutionName" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="e0600-114">範例2</span><span class="sxs-lookup"><span data-stu-id="e0600-114">Example 2</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="e0600-115">關閉資源識別碼為「/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15」的匯總警示</span><span class="sxs-lookup"><span data-stu-id="e0600-115">Dismiss aggregated alert with resource Id "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span></span>

## <span data-ttu-id="e0600-116">參數</span><span class="sxs-lookup"><span data-stu-id="e0600-116">PARAMETERS</span></span>

### <span data-ttu-id="e0600-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0600-117">-DefaultProfile</span></span>
<span data-ttu-id="e0600-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e0600-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0600-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0600-119">-InputObject</span></span>
<span data-ttu-id="e0600-120">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="e0600-120">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0600-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e0600-121">-Name</span></span>
<span data-ttu-id="e0600-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="e0600-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0600-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0600-123">-PassThru</span></span>
<span data-ttu-id="e0600-124">傳回操作是否成功。</span><span class="sxs-lookup"><span data-stu-id="e0600-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="e0600-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0600-125">-ResourceGroupName</span></span>
<span data-ttu-id="e0600-126">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e0600-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0600-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0600-127">-ResourceId</span></span>
<span data-ttu-id="e0600-128">您想要在其上喚醒命令的安全性資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e0600-128">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0600-129">-解決方案名稱</span><span class="sxs-lookup"><span data-stu-id="e0600-129">-SolutionName</span></span>
<span data-ttu-id="e0600-130">方案名稱</span><span class="sxs-lookup"><span data-stu-id="e0600-130">Solution name</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0600-131">-確認</span><span class="sxs-lookup"><span data-stu-id="e0600-131">-Confirm</span></span>
<span data-ttu-id="e0600-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e0600-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0600-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0600-133">-WhatIf</span></span>
<span data-ttu-id="e0600-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e0600-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0600-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e0600-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0600-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0600-136">CommonParameters</span></span>
<span data-ttu-id="e0600-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e0600-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0600-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e0600-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0600-139">輸入</span><span class="sxs-lookup"><span data-stu-id="e0600-139">INPUTS</span></span>

### <span data-ttu-id="e0600-140">PSIoTSecurityAggregatedAlert 中的 IotSecuritySolutionAnalytics （Security..。</span><span class="sxs-lookup"><span data-stu-id="e0600-140">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

### <span data-ttu-id="e0600-141">System.object</span><span class="sxs-lookup"><span data-stu-id="e0600-141">System.String</span></span>

## <span data-ttu-id="e0600-142">輸出</span><span class="sxs-lookup"><span data-stu-id="e0600-142">OUTPUTS</span></span>

### <span data-ttu-id="e0600-143">System.object</span><span class="sxs-lookup"><span data-stu-id="e0600-143">System.Boolean</span></span>

## <span data-ttu-id="e0600-144">筆記</span><span class="sxs-lookup"><span data-stu-id="e0600-144">NOTES</span></span>

## <span data-ttu-id="e0600-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0600-145">RELATED LINKS</span></span>
