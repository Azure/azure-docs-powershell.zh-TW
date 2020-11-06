---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: 4230eadc005ca53600feb2e6bc7ee2e001d7b209
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621288"
---
# <span data-ttu-id="ffcb1-101">New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="ffcb1-101">New-AzOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="ffcb1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ffcb1-102">SYNOPSIS</span></span>
<span data-ttu-id="ffcb1-103">從執行 Windows 作業系統的電腦收集事件記錄。</span><span class="sxs-lookup"><span data-stu-id="ffcb1-103">Collects event logs from computers that run the Windows operating system.</span></span>

## <span data-ttu-id="ffcb1-104">句法</span><span class="sxs-lookup"><span data-stu-id="ffcb1-104">SYNTAX</span></span>

### <span data-ttu-id="ffcb1-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="ffcb1-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffcb1-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ffcb1-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffcb1-107">說明</span><span class="sxs-lookup"><span data-stu-id="ffcb1-107">DESCRIPTION</span></span>
<span data-ttu-id="ffcb1-108">**新的-AzOperationalInsightsWindowsEventDataSource** Cmdlet 會新增一個資料來源，從已連接的電腦，收集在 Azure Operational Insights 中執行 Windows 作業系統的 windows 事件記錄。</span><span class="sxs-lookup"><span data-stu-id="ffcb1-108">The **New-AzOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="ffcb1-109">示例</span><span class="sxs-lookup"><span data-stu-id="ffcb1-109">EXAMPLES</span></span>

## <span data-ttu-id="ffcb1-110">參數</span><span class="sxs-lookup"><span data-stu-id="ffcb1-110">PARAMETERS</span></span>

### <span data-ttu-id="ffcb1-111">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="ffcb1-111">-CollectErrors</span></span>
<span data-ttu-id="ffcb1-112">表示 Operational Insights 會收集錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="ffcb1-112">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="ffcb1-113">-CollectInformation</span><span class="sxs-lookup"><span data-stu-id="ffcb1-113">-CollectInformation</span></span>
<span data-ttu-id="ffcb1-114">指示 Operational Insights 會收集資訊訊息。</span><span class="sxs-lookup"><span data-stu-id="ffcb1-114">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="ffcb1-115">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="ffcb1-115">-CollectWarnings</span></span>
<span data-ttu-id="ffcb1-116">指示 Operational Insights 會收集警告訊息。</span><span class="sxs-lookup"><span data-stu-id="ffcb1-116">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="ffcb1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffcb1-117">-DefaultProfile</span></span>
<span data-ttu-id="ffcb1-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ffcb1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ffcb1-119">-EventLogName</span><span class="sxs-lookup"><span data-stu-id="ffcb1-119">-EventLogName</span></span>
<span data-ttu-id="ffcb1-120">指定事件記錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="ffcb1-120">Specifies the name of the event log.</span></span>

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

### <span data-ttu-id="ffcb1-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ffcb1-121">-Force</span></span>
<span data-ttu-id="ffcb1-122">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ffcb1-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ffcb1-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="ffcb1-123">-Name</span></span>
<span data-ttu-id="ffcb1-124">指定資料來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="ffcb1-124">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="ffcb1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffcb1-125">-ResourceGroupName</span></span>
<span data-ttu-id="ffcb1-126">指定包含電腦之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ffcb1-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="ffcb1-127">-工作區</span><span class="sxs-lookup"><span data-stu-id="ffcb1-127">-Workspace</span></span>
<span data-ttu-id="ffcb1-128">指定這個 Cmdlet 在其中運作的工作區。</span><span class="sxs-lookup"><span data-stu-id="ffcb1-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ffcb1-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ffcb1-129">-WorkspaceName</span></span>
<span data-ttu-id="ffcb1-130">指定此 Cmdlet 作用中的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="ffcb1-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ffcb1-131">-確認</span><span class="sxs-lookup"><span data-stu-id="ffcb1-131">-Confirm</span></span>
<span data-ttu-id="ffcb1-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ffcb1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffcb1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffcb1-133">-WhatIf</span></span>
<span data-ttu-id="ffcb1-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ffcb1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffcb1-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ffcb1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffcb1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffcb1-136">CommonParameters</span></span>
<span data-ttu-id="ffcb1-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ffcb1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffcb1-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ffcb1-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffcb1-139">輸入</span><span class="sxs-lookup"><span data-stu-id="ffcb1-139">INPUTS</span></span>

### <span data-ttu-id="ffcb1-140">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="ffcb1-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="ffcb1-141">System.object</span><span class="sxs-lookup"><span data-stu-id="ffcb1-141">System.String</span></span>

## <span data-ttu-id="ffcb1-142">輸出</span><span class="sxs-lookup"><span data-stu-id="ffcb1-142">OUTPUTS</span></span>

### <span data-ttu-id="ffcb1-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="ffcb1-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="ffcb1-144">筆記</span><span class="sxs-lookup"><span data-stu-id="ffcb1-144">NOTES</span></span>

## <span data-ttu-id="ffcb1-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="ffcb1-145">RELATED LINKS</span></span>
