---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightslinuxperformanceobjectdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: a1f37a96d5be5443d2fb28c5a52964dd1612fc6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450199"
---
# <span data-ttu-id="b119c-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="b119c-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="b119c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b119c-102">SYNOPSIS</span></span>
<span data-ttu-id="b119c-103">新增效能計數器至工作區中的所有 Linux 電腦。</span><span class="sxs-lookup"><span data-stu-id="b119c-103">Adds performance counters to all Linux computers in a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b119c-104">句法</span><span class="sxs-lookup"><span data-stu-id="b119c-104">SYNTAX</span></span>

### <span data-ttu-id="b119c-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="b119c-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b119c-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b119c-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b119c-107">說明</span><span class="sxs-lookup"><span data-stu-id="b119c-107">DESCRIPTION</span></span>
<span data-ttu-id="b119c-108">**AzureRmOperationalInsightsLinuxPerformanceObjectDataSource** Cmdlet 會新增可供 Azure Operational Insights 在工作區中的所有 Linux 電腦收集資料的效能計數器。</span><span class="sxs-lookup"><span data-stu-id="b119c-108">The **New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="b119c-109">示例</span><span class="sxs-lookup"><span data-stu-id="b119c-109">EXAMPLES</span></span>

## <span data-ttu-id="b119c-110">參數</span><span class="sxs-lookup"><span data-stu-id="b119c-110">PARAMETERS</span></span>

### <span data-ttu-id="b119c-111">-CounterNames</span><span class="sxs-lookup"><span data-stu-id="b119c-111">-CounterNames</span></span>
<span data-ttu-id="b119c-112">指定計數器名稱的陣列。</span><span class="sxs-lookup"><span data-stu-id="b119c-112">Specifies an array of names of counters.</span></span>

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

### <span data-ttu-id="b119c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b119c-113">-DefaultProfile</span></span>
<span data-ttu-id="b119c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b119c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b119c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b119c-115">-Force</span></span>
<span data-ttu-id="b119c-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b119c-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b119c-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b119c-117">-InstanceName</span></span>
<span data-ttu-id="b119c-118">指定實例名稱。</span><span class="sxs-lookup"><span data-stu-id="b119c-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="b119c-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="b119c-119">-IntervalSeconds</span></span>
<span data-ttu-id="b119c-120">指定集合的間隔。</span><span class="sxs-lookup"><span data-stu-id="b119c-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="b119c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b119c-121">-Name</span></span>
<span data-ttu-id="b119c-122">指定資料來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="b119c-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="b119c-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="b119c-123">-ObjectName</span></span>
<span data-ttu-id="b119c-124">指定物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="b119c-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="b119c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b119c-125">-ResourceGroupName</span></span>
<span data-ttu-id="b119c-126">指定包含 Linux 電腦之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b119c-126">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="b119c-127">-工作區</span><span class="sxs-lookup"><span data-stu-id="b119c-127">-Workspace</span></span>
<span data-ttu-id="b119c-128">指定這個 Cmdlet 在其中運作的工作區。</span><span class="sxs-lookup"><span data-stu-id="b119c-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="b119c-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b119c-129">-WorkspaceName</span></span>
<span data-ttu-id="b119c-130">指定此 Cmdlet 作用中的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="b119c-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="b119c-131">-確認</span><span class="sxs-lookup"><span data-stu-id="b119c-131">-Confirm</span></span>
<span data-ttu-id="b119c-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b119c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b119c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b119c-133">-WhatIf</span></span>
<span data-ttu-id="b119c-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b119c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b119c-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b119c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b119c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b119c-136">CommonParameters</span></span>
<span data-ttu-id="b119c-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b119c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b119c-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b119c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b119c-139">輸入</span><span class="sxs-lookup"><span data-stu-id="b119c-139">INPUTS</span></span>

### <span data-ttu-id="b119c-140">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="b119c-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="b119c-141">參數：工作區 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="b119c-141">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="b119c-142">System.object</span><span class="sxs-lookup"><span data-stu-id="b119c-142">System.String</span></span>

### <span data-ttu-id="b119c-143">System.object []</span><span class="sxs-lookup"><span data-stu-id="b119c-143">System.String[]</span></span>

### <span data-ttu-id="b119c-144">System.object</span><span class="sxs-lookup"><span data-stu-id="b119c-144">System.Int32</span></span>

## <span data-ttu-id="b119c-145">輸出</span><span class="sxs-lookup"><span data-stu-id="b119c-145">OUTPUTS</span></span>

### <span data-ttu-id="b119c-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="b119c-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="b119c-147">筆記</span><span class="sxs-lookup"><span data-stu-id="b119c-147">NOTES</span></span>

## <span data-ttu-id="b119c-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="b119c-148">RELATED LINKS</span></span>

[<span data-ttu-id="b119c-149">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="b119c-149">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="b119c-150">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="b119c-150">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)


