---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxperformanceobjectdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: 7a6914d6259cafaedff68b28e8691311245ef6f0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911602"
---
# <span data-ttu-id="6b0d6-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="6b0d6-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="6b0d6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6b0d6-102">SYNOPSIS</span></span>
<span data-ttu-id="6b0d6-103">為工作區中所有的 Linux 電腦新增效能計數器。</span><span class="sxs-lookup"><span data-stu-id="6b0d6-103">Adds performance counters to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="6b0d6-104">語法</span><span class="sxs-lookup"><span data-stu-id="6b0d6-104">SYNTAX</span></span>

### <span data-ttu-id="6b0d6-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="6b0d6-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b0d6-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6b0d6-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b0d6-107">描述</span><span class="sxs-lookup"><span data-stu-id="6b0d6-107">DESCRIPTION</span></span>
<span data-ttu-id="6b0d6-108">**New-AzOperationalInsightsDataPerformanceObjectDataSource** Cmdlet 新增了執行計數器，Azure 營運深入資訊會從這些計數器收集資料至工作區內的所有 Linux 電腦。</span><span class="sxs-lookup"><span data-stu-id="6b0d6-108">The **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="6b0d6-109">例子</span><span class="sxs-lookup"><span data-stu-id="6b0d6-109">EXAMPLES</span></span>

## <span data-ttu-id="6b0d6-110">參數</span><span class="sxs-lookup"><span data-stu-id="6b0d6-110">PARAMETERS</span></span>

### <span data-ttu-id="6b0d6-111">-CounterNames</span><span class="sxs-lookup"><span data-stu-id="6b0d6-111">-CounterNames</span></span>
<span data-ttu-id="6b0d6-112">指定計數器名稱的陣列。</span><span class="sxs-lookup"><span data-stu-id="6b0d6-112">Specifies an array of names of counters.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b0d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b0d6-113">-DefaultProfile</span></span>
<span data-ttu-id="6b0d6-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="6b0d6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b0d6-115">-強制</span><span class="sxs-lookup"><span data-stu-id="6b0d6-115">-Force</span></span>
<span data-ttu-id="6b0d6-116">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="6b0d6-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6b0d6-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="6b0d6-117">-InstanceName</span></span>
<span data-ttu-id="6b0d6-118">指定實例名稱。</span><span class="sxs-lookup"><span data-stu-id="6b0d6-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="6b0d6-119">-Interval秒</span><span class="sxs-lookup"><span data-stu-id="6b0d6-119">-IntervalSeconds</span></span>
<span data-ttu-id="6b0d6-120">指定收藏的間隔。</span><span class="sxs-lookup"><span data-stu-id="6b0d6-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="6b0d6-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="6b0d6-121">-Name</span></span>
<span data-ttu-id="6b0d6-122">指定資料來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b0d6-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="6b0d6-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="6b0d6-123">-ObjectName</span></span>
<span data-ttu-id="6b0d6-124">指定物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b0d6-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="6b0d6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b0d6-125">-ResourceGroupName</span></span>
<span data-ttu-id="6b0d6-126">指定包含 Linux 電腦的資源組名。</span><span class="sxs-lookup"><span data-stu-id="6b0d6-126">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="6b0d6-127">-工作區</span><span class="sxs-lookup"><span data-stu-id="6b0d6-127">-Workspace</span></span>
<span data-ttu-id="6b0d6-128">指定此 Cmdlet 在哪個工作區中操作。</span><span class="sxs-lookup"><span data-stu-id="6b0d6-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="6b0d6-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6b0d6-129">-WorkspaceName</span></span>
<span data-ttu-id="6b0d6-130">指定此 Cmdlet 操作之工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b0d6-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="6b0d6-131">-確認</span><span class="sxs-lookup"><span data-stu-id="6b0d6-131">-Confirm</span></span>
<span data-ttu-id="6b0d6-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6b0d6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b0d6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b0d6-133">-WhatIf</span></span>
<span data-ttu-id="6b0d6-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6b0d6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b0d6-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6b0d6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b0d6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b0d6-136">CommonParameters</span></span>
<span data-ttu-id="6b0d6-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6b0d6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b0d6-138">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="6b0d6-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b0d6-139">輸入</span><span class="sxs-lookup"><span data-stu-id="6b0d6-139">INPUTS</span></span>

### <span data-ttu-id="6b0d6-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="6b0d6-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="6b0d6-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6b0d6-141">System.String</span></span>

### <span data-ttu-id="6b0d6-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6b0d6-142">System.String[]</span></span>

### <span data-ttu-id="6b0d6-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="6b0d6-143">System.Int32</span></span>

## <span data-ttu-id="6b0d6-144">輸出</span><span class="sxs-lookup"><span data-stu-id="6b0d6-144">OUTPUTS</span></span>

### <span data-ttu-id="6b0d6-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="6b0d6-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="6b0d6-146">筆記</span><span class="sxs-lookup"><span data-stu-id="6b0d6-146">NOTES</span></span>

## <span data-ttu-id="6b0d6-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="6b0d6-147">RELATED LINKS</span></span>

[<span data-ttu-id="6b0d6-148">Disable-AzOperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6b0d6-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="6b0d6-149">Enable-AzOperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6b0d6-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)


