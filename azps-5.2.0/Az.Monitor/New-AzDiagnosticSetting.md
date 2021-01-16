---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticSetting.md
ms.openlocfilehash: 8fa796b9b8940662c091e160cea55235816a29d6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280336"
---
# <span data-ttu-id="44081-101">New-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="44081-101">New-AzDiagnosticSetting</span></span>

## <span data-ttu-id="44081-102">摘要</span><span class="sxs-lookup"><span data-stu-id="44081-102">SYNOPSIS</span></span>
<span data-ttu-id="44081-103">建立 PSServiceDiagnosticSettings 物件。</span><span class="sxs-lookup"><span data-stu-id="44081-103">Create PSServiceDiagnosticSettings object.</span></span>

## <span data-ttu-id="44081-104">句法</span><span class="sxs-lookup"><span data-stu-id="44081-104">SYNTAX</span></span>

```
New-AzDiagnosticSetting -TargetResourceId <String> -Name <String> [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-WorkspaceId <String>] [-DedicatedLogAnalyticsDestinationType] [-Setting <PSDiagnosticDetailSettings[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44081-105">說明</span><span class="sxs-lookup"><span data-stu-id="44081-105">DESCRIPTION</span></span>
<span data-ttu-id="44081-106">建立 PSServiceDiagnosticSettings 物件。</span><span class="sxs-lookup"><span data-stu-id="44081-106">Create PSServiceDiagnosticSettings object.</span></span>
<span data-ttu-id="44081-107">這可以用來做為 `-InputObject` 參數 `Set-AzDiagnosticSetting`</span><span class="sxs-lookup"><span data-stu-id="44081-107">This can be used as parameter `-InputObject` for `Set-AzDiagnosticSetting`</span></span>

## <span data-ttu-id="44081-108">示例</span><span class="sxs-lookup"><span data-stu-id="44081-108">EXAMPLES</span></span>

### <span data-ttu-id="44081-109">範例1</span><span class="sxs-lookup"><span data-stu-id="44081-109">Example 1</span></span>
```powershell
$TimeGrain=New-TimeSpan -Days 90
$metric = New-AzDiagnosticDetailSetting -Metric -RetentionInDays 1 -RetentionEnabled -Category AllMetrics
$log = New-AzDiagnosticDetailSetting -Log -RetentionInDays 1 -RetentionEnabled -Category Audit -Enabled
$setting = New-AzDiagnosticSetting -TargetResourceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX -Name diagnostic-test -WorkspaceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.OperationalInsights/workspaces/XXXXXXXXX -DedicatedLogAnalyticsDestinationType -Setting $log,$metric
Location                    :
Tags                        :
Id                          : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/diagnosticSettings/diagnostic-test
Name                        : diagnostic-test
StorageAccountId            :
ServiceBusRuleId            :
EventHubAuthorizationRuleId :
EventHubName                :
Metrics
    TimeGrain       :
    Category        : AllMetrics
    Enabled         : False
    RetentionPolicy
    Enabled : True
    Days    : 1


Logs
    Category        : Audit
    Enabled         : True
    RetentionPolicy
    Enabled : True
    Days    : 1


WorkspaceId                 : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.OperationalInsights/workspaces/XXXXXXXXX
LogAnalyticsDestinationType : Dedicated
Type                        :

Set-AzDiagnosticSetting -InputObject $setting
```

<span data-ttu-id="44081-110">建立 PSServiceDiagnosticSettings 物件。</span><span class="sxs-lookup"><span data-stu-id="44081-110">Create PSServiceDiagnosticSettings object.</span></span> <span data-ttu-id="44081-111">並建立目標資源的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="44081-111">And create diagnostic setting for target resource.</span></span>

## <span data-ttu-id="44081-112">參數</span><span class="sxs-lookup"><span data-stu-id="44081-112">PARAMETERS</span></span>

### <span data-ttu-id="44081-113">-DedicatedLogAnalyticsDestinationType</span><span class="sxs-lookup"><span data-stu-id="44081-113">-DedicatedLogAnalyticsDestinationType</span></span>
<span data-ttu-id="44081-114">指示是否要將 (匯出到 ODS) 至資源特定 (（如果有的話）) 或 AzureDiagnostics (預設值，則不會顯示) </span><span class="sxs-lookup"><span data-stu-id="44081-114">The value indicating whether to export (to ODS) to resource-specific (if present) or to AzureDiagnostics (default, not present)</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44081-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44081-115">-DefaultProfile</span></span>
<span data-ttu-id="44081-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="44081-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44081-117">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="44081-117">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="44081-118">事件中心規則識別碼</span><span class="sxs-lookup"><span data-stu-id="44081-118">The event hub rule id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44081-119">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="44081-119">-EventHubName</span></span>
<span data-ttu-id="44081-120">服務匯流排規則識別碼</span><span class="sxs-lookup"><span data-stu-id="44081-120">The service bus rule id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44081-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="44081-121">-Name</span></span>
<span data-ttu-id="44081-122">診斷設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="44081-122">The name of the diagnostic setting.</span></span>
<span data-ttu-id="44081-123">預設為 [服務]</span><span class="sxs-lookup"><span data-stu-id="44081-123">Defaults to 'service'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44081-124">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="44081-124">-ServiceBusRuleId</span></span>
<span data-ttu-id="44081-125">服務匯流排規則識別碼</span><span class="sxs-lookup"><span data-stu-id="44081-125">The service bus rule id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44081-126">-設定</span><span class="sxs-lookup"><span data-stu-id="44081-126">-Setting</span></span>
<span data-ttu-id="44081-127">公制設定或記錄設定</span><span class="sxs-lookup"><span data-stu-id="44081-127">Metric settings or Log settings</span></span>

```yaml
Type: PSDiagnosticDetailSettings[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44081-128">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="44081-128">-StorageAccountId</span></span>
<span data-ttu-id="44081-129">儲存空間帳戶識別碼</span><span class="sxs-lookup"><span data-stu-id="44081-129">The storage account id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44081-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="44081-130">-TargetResourceId</span></span>
<span data-ttu-id="44081-131">資源識別碼</span><span class="sxs-lookup"><span data-stu-id="44081-131">The resource id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44081-132">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="44081-132">-WorkspaceId</span></span>
<span data-ttu-id="44081-133">要傳送記錄/度量單位之 Log Analytics 工作區的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="44081-133">The resource Id of the Log Analytics workspace to send logs/metrics to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44081-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44081-134">CommonParameters</span></span>
<span data-ttu-id="44081-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="44081-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44081-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="44081-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44081-137">輸入</span><span class="sxs-lookup"><span data-stu-id="44081-137">INPUTS</span></span>

### <span data-ttu-id="44081-138">System.object</span><span class="sxs-lookup"><span data-stu-id="44081-138">System.String</span></span>

### <span data-ttu-id="44081-139">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="44081-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="44081-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings []</span><span class="sxs-lookup"><span data-stu-id="44081-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings[]</span></span>

## <span data-ttu-id="44081-141">輸出</span><span class="sxs-lookup"><span data-stu-id="44081-141">OUTPUTS</span></span>

### <span data-ttu-id="44081-142">PSServiceDiagnosticSettings 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="44081-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="44081-143">筆記</span><span class="sxs-lookup"><span data-stu-id="44081-143">NOTES</span></span>

## <span data-ttu-id="44081-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="44081-144">RELATED LINKS</span></span>
