---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 09CC097E-0210-4443-BCDB-5CF6C8300288
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightswindowsperformancecounterdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsPerformanceCounterDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsPerformanceCounterDataSource.md
ms.openlocfilehash: e775f07249b9ec8a8987986d4e614e9fc66a25f8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621287"
---
# <span data-ttu-id="3c715-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span><span class="sxs-lookup"><span data-stu-id="3c715-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span></span>

## <span data-ttu-id="3c715-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3c715-102">SYNOPSIS</span></span>
<span data-ttu-id="3c715-103">新增執行 Windows 作業系統之已連接的電腦的 Windows 效能計數器資料來源。</span><span class="sxs-lookup"><span data-stu-id="3c715-103">Adds Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="3c715-104">句法</span><span class="sxs-lookup"><span data-stu-id="3c715-104">SYNTAX</span></span>

### <span data-ttu-id="3c715-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="3c715-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterName] <String>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-UseLegacyCollector] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c715-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3c715-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterName] <String> [-InstanceName <String>] [-IntervalSeconds <Int32>]
 [-UseLegacyCollector] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3c715-107">說明</span><span class="sxs-lookup"><span data-stu-id="3c715-107">DESCRIPTION</span></span>
<span data-ttu-id="3c715-108">**新的-AzOperationalInsightsWindowsPerformanceCounterDataSource** Cmdlet 會針對執行 windows 作業系統的已連接電腦新增 Windows 效能計數器資料來源。</span><span class="sxs-lookup"><span data-stu-id="3c715-108">The **New-AzOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet adds a Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="3c715-109">示例</span><span class="sxs-lookup"><span data-stu-id="3c715-109">EXAMPLES</span></span>

## <span data-ttu-id="3c715-110">參數</span><span class="sxs-lookup"><span data-stu-id="3c715-110">PARAMETERS</span></span>

### <span data-ttu-id="3c715-111">-CounterName</span><span class="sxs-lookup"><span data-stu-id="3c715-111">-CounterName</span></span>
<span data-ttu-id="3c715-112">指定計數器的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c715-112">Specifies the name of a counter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c715-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c715-113">-DefaultProfile</span></span>
<span data-ttu-id="3c715-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3c715-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c715-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3c715-115">-Force</span></span>
<span data-ttu-id="3c715-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="3c715-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3c715-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="3c715-117">-InstanceName</span></span>
<span data-ttu-id="3c715-118">指定實例名稱。</span><span class="sxs-lookup"><span data-stu-id="3c715-118">Specifies an instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c715-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="3c715-119">-IntervalSeconds</span></span>
<span data-ttu-id="3c715-120">指定集合的間隔。</span><span class="sxs-lookup"><span data-stu-id="3c715-120">Specifies the interval of collection.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c715-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="3c715-121">-Name</span></span>
<span data-ttu-id="3c715-122">指定資料來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c715-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="3c715-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="3c715-123">-ObjectName</span></span>
<span data-ttu-id="3c715-124">指定物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c715-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="3c715-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c715-125">-ResourceGroupName</span></span>
<span data-ttu-id="3c715-126">指定包含電腦之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c715-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="3c715-127">-UseLegacyCollector</span><span class="sxs-lookup"><span data-stu-id="3c715-127">-UseLegacyCollector</span></span>
<span data-ttu-id="3c715-128">使用舊版收集器或預設收集器。</span><span class="sxs-lookup"><span data-stu-id="3c715-128">Use legacy collector or the default collector.</span></span>

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

### <span data-ttu-id="3c715-129">-工作區</span><span class="sxs-lookup"><span data-stu-id="3c715-129">-Workspace</span></span>
<span data-ttu-id="3c715-130">指定這個 Cmdlet 在其中運作的工作區。</span><span class="sxs-lookup"><span data-stu-id="3c715-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3c715-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3c715-131">-WorkspaceName</span></span>
<span data-ttu-id="3c715-132">指定此 Cmdlet 作用中的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="3c715-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3c715-133">-確認</span><span class="sxs-lookup"><span data-stu-id="3c715-133">-Confirm</span></span>
<span data-ttu-id="3c715-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3c715-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c715-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c715-135">-WhatIf</span></span>
<span data-ttu-id="3c715-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3c715-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c715-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3c715-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c715-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c715-138">CommonParameters</span></span>
<span data-ttu-id="3c715-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3c715-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c715-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3c715-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c715-141">輸入</span><span class="sxs-lookup"><span data-stu-id="3c715-141">INPUTS</span></span>

### <span data-ttu-id="3c715-142">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="3c715-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="3c715-143">System.object</span><span class="sxs-lookup"><span data-stu-id="3c715-143">System.String</span></span>

### <span data-ttu-id="3c715-144">System.object</span><span class="sxs-lookup"><span data-stu-id="3c715-144">System.Int32</span></span>

## <span data-ttu-id="3c715-145">輸出</span><span class="sxs-lookup"><span data-stu-id="3c715-145">OUTPUTS</span></span>

### <span data-ttu-id="3c715-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="3c715-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="3c715-147">筆記</span><span class="sxs-lookup"><span data-stu-id="3c715-147">NOTES</span></span>

## <span data-ttu-id="3c715-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="3c715-148">RELATED LINKS</span></span>
