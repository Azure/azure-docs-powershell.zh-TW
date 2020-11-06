---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: 1e9114b9f6b62f6900c975b39e5f8c67b4d9051a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448067"
---
# <span data-ttu-id="1ae4b-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="1ae4b-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="1ae4b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1ae4b-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae4b-103">新增效能計數器至工作區中的所有 Linux 電腦。</span><span class="sxs-lookup"><span data-stu-id="1ae4b-103">Adds performance counters to all Linux computers in a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ae4b-104">句法</span><span class="sxs-lookup"><span data-stu-id="1ae4b-104">SYNTAX</span></span>

### <span data-ttu-id="1ae4b-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="1ae4b-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ae4b-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1ae4b-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ae4b-107">說明</span><span class="sxs-lookup"><span data-stu-id="1ae4b-107">DESCRIPTION</span></span>
<span data-ttu-id="1ae4b-108">**AzureRmOperationalInsightsLinuxPerformanceObjectDataSource** Cmdlet 會新增可供 Azure Operational Insights 在工作區中的所有 Linux 電腦收集資料的效能計數器。</span><span class="sxs-lookup"><span data-stu-id="1ae4b-108">The **New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="1ae4b-109">示例</span><span class="sxs-lookup"><span data-stu-id="1ae4b-109">EXAMPLES</span></span>

## <span data-ttu-id="1ae4b-110">參數</span><span class="sxs-lookup"><span data-stu-id="1ae4b-110">PARAMETERS</span></span>

### <span data-ttu-id="1ae4b-111">-CounterNames</span><span class="sxs-lookup"><span data-stu-id="1ae4b-111">-CounterNames</span></span>
<span data-ttu-id="1ae4b-112">指定計數器名稱的陣列。</span><span class="sxs-lookup"><span data-stu-id="1ae4b-112">Specifies an array of names of counters.</span></span>

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

### <span data-ttu-id="1ae4b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1ae4b-113">-Force</span></span>
<span data-ttu-id="1ae4b-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="1ae4b-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1ae4b-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="1ae4b-115">-InstanceName</span></span>
<span data-ttu-id="1ae4b-116">指定實例名稱。</span><span class="sxs-lookup"><span data-stu-id="1ae4b-116">Specifies an instance name.</span></span>

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

### <span data-ttu-id="1ae4b-117">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="1ae4b-117">-IntervalSeconds</span></span>
<span data-ttu-id="1ae4b-118">指定集合的間隔。</span><span class="sxs-lookup"><span data-stu-id="1ae4b-118">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="1ae4b-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="1ae4b-119">-Name</span></span>
<span data-ttu-id="1ae4b-120">指定資料來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ae4b-120">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="1ae4b-121">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="1ae4b-121">-ObjectName</span></span>
<span data-ttu-id="1ae4b-122">指定物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ae4b-122">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="1ae4b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ae4b-123">-ResourceGroupName</span></span>
<span data-ttu-id="1ae4b-124">指定包含 Linux 電腦之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ae4b-124">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="1ae4b-125">-工作區</span><span class="sxs-lookup"><span data-stu-id="1ae4b-125">-Workspace</span></span>
<span data-ttu-id="1ae4b-126">指定這個 Cmdlet 在其中運作的工作區。</span><span class="sxs-lookup"><span data-stu-id="1ae4b-126">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="1ae4b-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1ae4b-127">-WorkspaceName</span></span>
<span data-ttu-id="1ae4b-128">指定此 Cmdlet 作用中的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="1ae4b-128">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="1ae4b-129">-確認</span><span class="sxs-lookup"><span data-stu-id="1ae4b-129">-Confirm</span></span>
<span data-ttu-id="1ae4b-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1ae4b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ae4b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ae4b-131">-WhatIf</span></span>
<span data-ttu-id="1ae4b-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1ae4b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ae4b-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1ae4b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ae4b-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae4b-134">-DefaultProfile</span></span>
<span data-ttu-id="1ae4b-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1ae4b-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ae4b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae4b-136">CommonParameters</span></span>
<span data-ttu-id="1ae4b-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1ae4b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae4b-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1ae4b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae4b-139">輸入</span><span class="sxs-lookup"><span data-stu-id="1ae4b-139">INPUTS</span></span>

### <span data-ttu-id="1ae4b-140">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1ae4b-140">PSWorkspace</span></span>
<span data-ttu-id="1ae4b-141">形參 "Workspace" 接受管線中類型 ' PSWorkspace」的值</span><span class="sxs-lookup"><span data-stu-id="1ae4b-141">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="1ae4b-142">輸出</span><span class="sxs-lookup"><span data-stu-id="1ae4b-142">OUTPUTS</span></span>

### <span data-ttu-id="1ae4b-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="1ae4b-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="1ae4b-144">筆記</span><span class="sxs-lookup"><span data-stu-id="1ae4b-144">NOTES</span></span>

## <span data-ttu-id="1ae4b-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ae4b-145">RELATED LINKS</span></span>

[<span data-ttu-id="1ae4b-146">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="1ae4b-146">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="1ae4b-147">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="1ae4b-147">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)


