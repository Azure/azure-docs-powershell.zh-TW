---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
ms.openlocfilehash: 86559299a4711d95e1b5c94c455bdbb841e141e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789857"
---
# <span data-ttu-id="49911-101">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="49911-101">Get-AzScheduledQueryRule</span></span>

## <span data-ttu-id="49911-102">摘要</span><span class="sxs-lookup"><span data-stu-id="49911-102">SYNOPSIS</span></span>
<span data-ttu-id="49911-103">取得排程的查詢資源</span><span class="sxs-lookup"><span data-stu-id="49911-103">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="49911-104">句法</span><span class="sxs-lookup"><span data-stu-id="49911-104">SYNTAX</span></span>

### <span data-ttu-id="49911-105">BySubscriptionOrResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="49911-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzScheduledQueryRule [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49911-106">ByRuleName</span><span class="sxs-lookup"><span data-stu-id="49911-106">ByRuleName</span></span>
```
Get-AzScheduledQueryRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49911-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="49911-107">ByResourceId</span></span>
```
Get-AzScheduledQueryRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49911-108">說明</span><span class="sxs-lookup"><span data-stu-id="49911-108">DESCRIPTION</span></span>
<span data-ttu-id="49911-109">取得排程的查詢資源</span><span class="sxs-lookup"><span data-stu-id="49911-109">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="49911-110">示例</span><span class="sxs-lookup"><span data-stu-id="49911-110">EXAMPLES</span></span>

### <span data-ttu-id="49911-111">範例 1-依訂閱或資源群組列出清單</span><span class="sxs-lookup"><span data-stu-id="49911-111">Example 1 - List by subscription or resource group</span></span>
```powershell
PS C:\> Get-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup"

Description       : description 1
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:29:39 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}

Description       : description 2
Enabled           : true
LastUpdatedTime   : 15-Apr-19 6:57:00 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.Action
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule2
Name              : LogAlertRule2
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="49911-112">範例 2-依規則名稱取得</span><span class="sxs-lookup"><span data-stu-id="49911-112">Example 2 - Get by rule name</span></span>
```powershell
PS C:\> Get-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"

Description       : desc 1
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:29:39 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="49911-113">範例 3-依資源識別碼取得</span><span class="sxs-lookup"><span data-stu-id="49911-113">Example 3 - Get by resource Id</span></span>
```powershell
PS C:\> Get-AzScheduledQueryRule -ResourceId "/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1"

Description       : desc 1
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:29:39 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

## <span data-ttu-id="49911-114">參數</span><span class="sxs-lookup"><span data-stu-id="49911-114">PARAMETERS</span></span>

### <span data-ttu-id="49911-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49911-115">-DefaultProfile</span></span>
<span data-ttu-id="49911-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="49911-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49911-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="49911-117">-Name</span></span>
<span data-ttu-id="49911-118">警示規則名稱</span><span class="sxs-lookup"><span data-stu-id="49911-118">The alert rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49911-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49911-119">-ResourceGroupName</span></span>
<span data-ttu-id="49911-120">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="49911-120">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionOrResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49911-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49911-121">-ResourceId</span></span>
<span data-ttu-id="49911-122">資源識別碼</span><span class="sxs-lookup"><span data-stu-id="49911-122">The resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49911-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49911-123">CommonParameters</span></span>
<span data-ttu-id="49911-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="49911-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49911-125">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="49911-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49911-126">輸入</span><span class="sxs-lookup"><span data-stu-id="49911-126">INPUTS</span></span>

### <span data-ttu-id="49911-127">所有</span><span class="sxs-lookup"><span data-stu-id="49911-127">None</span></span>

## <span data-ttu-id="49911-128">輸出</span><span class="sxs-lookup"><span data-stu-id="49911-128">OUTPUTS</span></span>

### <span data-ttu-id="49911-129">PSScheduledQueryRuleResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="49911-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="49911-130">筆記</span><span class="sxs-lookup"><span data-stu-id="49911-130">NOTES</span></span>

## <span data-ttu-id="49911-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="49911-131">RELATED LINKS</span></span>