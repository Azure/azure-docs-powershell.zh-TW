---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 09CC097E-0210-4443-BCDB-5CF6C8300288
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightswindowsperformancecounterdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource.md
ms.openlocfilehash: 5a772007850342bd400666a5815d6d8b936f7c5d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450194"
---
# <span data-ttu-id="3f9a3-101">New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource</span><span class="sxs-lookup"><span data-stu-id="3f9a3-101">New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource</span></span>

## <span data-ttu-id="3f9a3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3f9a3-102">SYNOPSIS</span></span>
<span data-ttu-id="3f9a3-103">新增執行 Windows 作業系統之已連接的電腦的 Windows 效能計數器資料來源。</span><span class="sxs-lookup"><span data-stu-id="3f9a3-103">Adds Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f9a3-104">句法</span><span class="sxs-lookup"><span data-stu-id="3f9a3-104">SYNTAX</span></span>

### <span data-ttu-id="3f9a3-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="3f9a3-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterName] <String>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-UseLegacyCollector] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f9a3-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3f9a3-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterName] <String> [-InstanceName <String>] [-IntervalSeconds <Int32>]
 [-UseLegacyCollector] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3f9a3-107">說明</span><span class="sxs-lookup"><span data-stu-id="3f9a3-107">DESCRIPTION</span></span>
<span data-ttu-id="3f9a3-108">**新的-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource** Cmdlet 會針對執行 windows 作業系統的已連接電腦新增 Windows 效能計數器資料來源。</span><span class="sxs-lookup"><span data-stu-id="3f9a3-108">The **New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet adds a Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="3f9a3-109">示例</span><span class="sxs-lookup"><span data-stu-id="3f9a3-109">EXAMPLES</span></span>

## <span data-ttu-id="3f9a3-110">參數</span><span class="sxs-lookup"><span data-stu-id="3f9a3-110">PARAMETERS</span></span>

### <span data-ttu-id="3f9a3-111">-CounterName</span><span class="sxs-lookup"><span data-stu-id="3f9a3-111">-CounterName</span></span>
<span data-ttu-id="3f9a3-112">指定計數器的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f9a3-112">Specifies the name of a counter.</span></span>

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

### <span data-ttu-id="3f9a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f9a3-113">-DefaultProfile</span></span>
<span data-ttu-id="3f9a3-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3f9a3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f9a3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3f9a3-115">-Force</span></span>
<span data-ttu-id="3f9a3-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="3f9a3-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3f9a3-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="3f9a3-117">-InstanceName</span></span>
<span data-ttu-id="3f9a3-118">指定實例名稱。</span><span class="sxs-lookup"><span data-stu-id="3f9a3-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="3f9a3-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="3f9a3-119">-IntervalSeconds</span></span>
<span data-ttu-id="3f9a3-120">指定集合的間隔。</span><span class="sxs-lookup"><span data-stu-id="3f9a3-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="3f9a3-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="3f9a3-121">-Name</span></span>
<span data-ttu-id="3f9a3-122">指定資料來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f9a3-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="3f9a3-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="3f9a3-123">-ObjectName</span></span>
<span data-ttu-id="3f9a3-124">指定物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f9a3-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="3f9a3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f9a3-125">-ResourceGroupName</span></span>
<span data-ttu-id="3f9a3-126">指定包含電腦之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f9a3-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="3f9a3-127">-UseLegacyCollector</span><span class="sxs-lookup"><span data-stu-id="3f9a3-127">-UseLegacyCollector</span></span>
<span data-ttu-id="3f9a3-128">使用舊版收集器或預設收集器。</span><span class="sxs-lookup"><span data-stu-id="3f9a3-128">Use legacy collector or the default collector.</span></span>

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

### <span data-ttu-id="3f9a3-129">-工作區</span><span class="sxs-lookup"><span data-stu-id="3f9a3-129">-Workspace</span></span>
<span data-ttu-id="3f9a3-130">指定這個 Cmdlet 在其中運作的工作區。</span><span class="sxs-lookup"><span data-stu-id="3f9a3-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3f9a3-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3f9a3-131">-WorkspaceName</span></span>
<span data-ttu-id="3f9a3-132">指定此 Cmdlet 作用中的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="3f9a3-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3f9a3-133">-確認</span><span class="sxs-lookup"><span data-stu-id="3f9a3-133">-Confirm</span></span>
<span data-ttu-id="3f9a3-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3f9a3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f9a3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f9a3-135">-WhatIf</span></span>
<span data-ttu-id="3f9a3-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3f9a3-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f9a3-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3f9a3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f9a3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f9a3-138">CommonParameters</span></span>
<span data-ttu-id="3f9a3-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3f9a3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f9a3-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3f9a3-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f9a3-141">輸入</span><span class="sxs-lookup"><span data-stu-id="3f9a3-141">INPUTS</span></span>

### <span data-ttu-id="3f9a3-142">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="3f9a3-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="3f9a3-143">參數：工作區 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="3f9a3-143">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="3f9a3-144">System.object</span><span class="sxs-lookup"><span data-stu-id="3f9a3-144">System.String</span></span>

### <span data-ttu-id="3f9a3-145">System.object</span><span class="sxs-lookup"><span data-stu-id="3f9a3-145">System.Int32</span></span>

## <span data-ttu-id="3f9a3-146">輸出</span><span class="sxs-lookup"><span data-stu-id="3f9a3-146">OUTPUTS</span></span>

### <span data-ttu-id="3f9a3-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="3f9a3-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="3f9a3-148">筆記</span><span class="sxs-lookup"><span data-stu-id="3f9a3-148">NOTES</span></span>

## <span data-ttu-id="3f9a3-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="3f9a3-149">RELATED LINKS</span></span>
