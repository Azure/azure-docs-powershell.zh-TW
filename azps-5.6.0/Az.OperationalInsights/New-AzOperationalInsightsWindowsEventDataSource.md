---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: 29f109e0e4f063a72e188a908da8bc65723f5065
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911593"
---
# <span data-ttu-id="27008-101">New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="27008-101">New-AzOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="27008-102">簡介</span><span class="sxs-lookup"><span data-stu-id="27008-102">SYNOPSIS</span></span>
<span data-ttu-id="27008-103">從執行 Windows 作業系統的電腦收集事件記錄。</span><span class="sxs-lookup"><span data-stu-id="27008-103">Collects event logs from computers that run the Windows operating system.</span></span>

## <span data-ttu-id="27008-104">語法</span><span class="sxs-lookup"><span data-stu-id="27008-104">SYNTAX</span></span>

### <span data-ttu-id="27008-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="27008-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27008-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="27008-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27008-107">描述</span><span class="sxs-lookup"><span data-stu-id="27008-107">DESCRIPTION</span></span>
<span data-ttu-id="27008-108">**New-AzOperationalInsightsWindowsEventDataSource** Cmdlet 會新增資料來源，從在 Azure 營運深入資訊中執行 Windows 作業系統的已連接電腦收集 Windows 事件記錄。</span><span class="sxs-lookup"><span data-stu-id="27008-108">The **New-AzOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="27008-109">例子</span><span class="sxs-lookup"><span data-stu-id="27008-109">EXAMPLES</span></span>

### <span data-ttu-id="27008-110">範例 1：建立系統 Windows 事件資料來源</span><span class="sxs-lookup"><span data-stu-id="27008-110">Example 1: Create system Windows event data source</span></span>
```
$EventLogNames       = @()
$EventLogNames      += 'Directory Service'
$EventLogNames      += 'Microsoft-Windows-EventCollector/Operational'
$EventLogNames      += 'System'
$ResourceGroupName   = 'MyResourceGroup'
$WorkspaceName       = 'MyWorkspaceName'

$Count = 0
foreach ($EventLogName in $EventLogNames) {
    $Count++
    $null = New-AzOperationalInsightsWindowsEventDataSource `
    -ResourceGroupName $ResourceGroupName `
    -WorkspaceName $WorkspaceName `
    -Name "Windows-event-$($Count)" `
    -EventLogName $EventLogName `
    -CollectErrors `
    -CollectWarnings `
    -CollectInformation
}

Get-AzOperationalInsightsDataSource `
   -ResourceGroupName $ResourceGroupName `
   -WorkspaceName $WorkspaceName `
   -Kind 'WindowsEvent'
```

## <span data-ttu-id="27008-111">參數</span><span class="sxs-lookup"><span data-stu-id="27008-111">PARAMETERS</span></span>

### <span data-ttu-id="27008-112">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="27008-112">-CollectErrors</span></span>
<span data-ttu-id="27008-113">表示營運深入資訊會收集錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="27008-113">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="27008-114">-CollectInformation</span><span class="sxs-lookup"><span data-stu-id="27008-114">-CollectInformation</span></span>
<span data-ttu-id="27008-115">表示營運深入資訊會收集資訊訊息。</span><span class="sxs-lookup"><span data-stu-id="27008-115">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="27008-116">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="27008-116">-CollectWarnings</span></span>
<span data-ttu-id="27008-117">表示營運深入資訊會收集警告訊息。</span><span class="sxs-lookup"><span data-stu-id="27008-117">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="27008-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27008-118">-DefaultProfile</span></span>
<span data-ttu-id="27008-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="27008-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27008-120">-EventLogName</span><span class="sxs-lookup"><span data-stu-id="27008-120">-EventLogName</span></span>
<span data-ttu-id="27008-121">指定事件記錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="27008-121">Specifies the name of the event log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27008-122">-強制</span><span class="sxs-lookup"><span data-stu-id="27008-122">-Force</span></span>
<span data-ttu-id="27008-123">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="27008-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="27008-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="27008-124">-Name</span></span>
<span data-ttu-id="27008-125">指定資料來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="27008-125">Specifies a name for the data source.</span></span> <span data-ttu-id="27008-126">名稱不會在 Azure 入口網站中公開，而且任何字串都可以使用，只要它是唯一的。</span><span class="sxs-lookup"><span data-stu-id="27008-126">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27008-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27008-127">-ResourceGroupName</span></span>
<span data-ttu-id="27008-128">指定包含電腦的資源組名。</span><span class="sxs-lookup"><span data-stu-id="27008-128">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27008-129">-工作區</span><span class="sxs-lookup"><span data-stu-id="27008-129">-Workspace</span></span>
<span data-ttu-id="27008-130">指定此 Cmdlet 在哪個工作區中操作。</span><span class="sxs-lookup"><span data-stu-id="27008-130">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27008-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="27008-131">-WorkspaceName</span></span>
<span data-ttu-id="27008-132">指定此 Cmdlet 操作之工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="27008-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27008-133">-確認</span><span class="sxs-lookup"><span data-stu-id="27008-133">-Confirm</span></span>
<span data-ttu-id="27008-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="27008-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27008-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27008-135">-WhatIf</span></span>
<span data-ttu-id="27008-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="27008-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27008-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="27008-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27008-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27008-138">CommonParameters</span></span>
<span data-ttu-id="27008-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="27008-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27008-140">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="27008-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27008-141">輸入</span><span class="sxs-lookup"><span data-stu-id="27008-141">INPUTS</span></span>

### <span data-ttu-id="27008-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="27008-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="27008-143">System.String</span><span class="sxs-lookup"><span data-stu-id="27008-143">System.String</span></span>

## <span data-ttu-id="27008-144">輸出</span><span class="sxs-lookup"><span data-stu-id="27008-144">OUTPUTS</span></span>

### <span data-ttu-id="27008-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="27008-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="27008-146">筆記</span><span class="sxs-lookup"><span data-stu-id="27008-146">NOTES</span></span>

## <span data-ttu-id="27008-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="27008-147">RELATED LINKS</span></span>
