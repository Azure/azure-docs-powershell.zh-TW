---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: 89aed8cb651fc5e11f6314df0ec74f3b4f9aa29e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791758"
---
# <span data-ttu-id="ffcff-101">New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="ffcff-101">New-AzOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="ffcff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ffcff-102">SYNOPSIS</span></span>
<span data-ttu-id="ffcff-103">從執行 Windows 作業系統的電腦收集事件記錄。</span><span class="sxs-lookup"><span data-stu-id="ffcff-103">Collects event logs from computers that run the Windows operating system.</span></span>

## <span data-ttu-id="ffcff-104">句法</span><span class="sxs-lookup"><span data-stu-id="ffcff-104">SYNTAX</span></span>

### <span data-ttu-id="ffcff-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="ffcff-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffcff-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ffcff-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffcff-107">說明</span><span class="sxs-lookup"><span data-stu-id="ffcff-107">DESCRIPTION</span></span>
<span data-ttu-id="ffcff-108">**新的-AzOperationalInsightsWindowsEventDataSource** Cmdlet 會新增一個資料來源，從已連接的電腦，收集在 Azure Operational Insights 中執行 Windows 作業系統的 windows 事件記錄。</span><span class="sxs-lookup"><span data-stu-id="ffcff-108">The **New-AzOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="ffcff-109">示例</span><span class="sxs-lookup"><span data-stu-id="ffcff-109">EXAMPLES</span></span>

### <span data-ttu-id="ffcff-110">範例1：建立系統 Windows 事件資料來源</span><span class="sxs-lookup"><span data-stu-id="ffcff-110">Example 1: Create system Windows event data source</span></span>
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

## <span data-ttu-id="ffcff-111">參數</span><span class="sxs-lookup"><span data-stu-id="ffcff-111">PARAMETERS</span></span>

### <span data-ttu-id="ffcff-112">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="ffcff-112">-CollectErrors</span></span>
<span data-ttu-id="ffcff-113">表示 Operational Insights 會收集錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="ffcff-113">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="ffcff-114">-CollectInformation</span><span class="sxs-lookup"><span data-stu-id="ffcff-114">-CollectInformation</span></span>
<span data-ttu-id="ffcff-115">指示 Operational Insights 會收集資訊訊息。</span><span class="sxs-lookup"><span data-stu-id="ffcff-115">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="ffcff-116">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="ffcff-116">-CollectWarnings</span></span>
<span data-ttu-id="ffcff-117">指示 Operational Insights 會收集警告訊息。</span><span class="sxs-lookup"><span data-stu-id="ffcff-117">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="ffcff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffcff-118">-DefaultProfile</span></span>
<span data-ttu-id="ffcff-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ffcff-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ffcff-120">-EventLogName</span><span class="sxs-lookup"><span data-stu-id="ffcff-120">-EventLogName</span></span>
<span data-ttu-id="ffcff-121">指定事件記錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="ffcff-121">Specifies the name of the event log.</span></span>

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

### <span data-ttu-id="ffcff-122">-Force</span><span class="sxs-lookup"><span data-stu-id="ffcff-122">-Force</span></span>
<span data-ttu-id="ffcff-123">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ffcff-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ffcff-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="ffcff-124">-Name</span></span>
<span data-ttu-id="ffcff-125">指定資料來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="ffcff-125">Specifies a name for the data source.</span></span> <span data-ttu-id="ffcff-126">此名稱不會在 Azure 入口網站中公開，而且任何字串只要是唯一的，就可以使用。</span><span class="sxs-lookup"><span data-stu-id="ffcff-126">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

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

### <span data-ttu-id="ffcff-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffcff-127">-ResourceGroupName</span></span>
<span data-ttu-id="ffcff-128">指定包含電腦之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ffcff-128">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="ffcff-129">-工作區</span><span class="sxs-lookup"><span data-stu-id="ffcff-129">-Workspace</span></span>
<span data-ttu-id="ffcff-130">指定這個 Cmdlet 在其中運作的工作區。</span><span class="sxs-lookup"><span data-stu-id="ffcff-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ffcff-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ffcff-131">-WorkspaceName</span></span>
<span data-ttu-id="ffcff-132">指定此 Cmdlet 作用中的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="ffcff-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ffcff-133">-確認</span><span class="sxs-lookup"><span data-stu-id="ffcff-133">-Confirm</span></span>
<span data-ttu-id="ffcff-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ffcff-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffcff-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffcff-135">-WhatIf</span></span>
<span data-ttu-id="ffcff-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ffcff-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffcff-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ffcff-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffcff-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffcff-138">CommonParameters</span></span>
<span data-ttu-id="ffcff-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ffcff-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffcff-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ffcff-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffcff-141">輸入</span><span class="sxs-lookup"><span data-stu-id="ffcff-141">INPUTS</span></span>

### <span data-ttu-id="ffcff-142">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="ffcff-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="ffcff-143">System.object</span><span class="sxs-lookup"><span data-stu-id="ffcff-143">System.String</span></span>

## <span data-ttu-id="ffcff-144">輸出</span><span class="sxs-lookup"><span data-stu-id="ffcff-144">OUTPUTS</span></span>

### <span data-ttu-id="ffcff-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="ffcff-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="ffcff-146">筆記</span><span class="sxs-lookup"><span data-stu-id="ffcff-146">NOTES</span></span>

## <span data-ttu-id="ffcff-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="ffcff-147">RELATED LINKS</span></span>
