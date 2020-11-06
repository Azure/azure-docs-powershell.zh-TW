---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: a0268931d276c74560acd5cb04cac1d1e5778b81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621290"
---
# <span data-ttu-id="65273-101">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="65273-101">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="65273-102">摘要</span><span class="sxs-lookup"><span data-stu-id="65273-102">SYNOPSIS</span></span>
<span data-ttu-id="65273-103">新增資料來源至 Linux 電腦。</span><span class="sxs-lookup"><span data-stu-id="65273-103">Adds a data source to Linux computers.</span></span>

## <span data-ttu-id="65273-104">句法</span><span class="sxs-lookup"><span data-stu-id="65273-104">SYNTAX</span></span>

### <span data-ttu-id="65273-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="65273-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65273-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="65273-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Facility] <String>
 [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning] [-CollectNotice]
 [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65273-107">說明</span><span class="sxs-lookup"><span data-stu-id="65273-107">DESCRIPTION</span></span>
<span data-ttu-id="65273-108">**新的-AzOperationalInsightsLinuxSyslogDataSource** Cmdlet 會將 syslog 資料來源新增到工作區中的連線 Linux 電腦。</span><span class="sxs-lookup"><span data-stu-id="65273-108">The **New-AzOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="65273-109">Azure Operational Insights 可以收集 syslog 資料。</span><span class="sxs-lookup"><span data-stu-id="65273-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="65273-110">示例</span><span class="sxs-lookup"><span data-stu-id="65273-110">EXAMPLES</span></span>

## <span data-ttu-id="65273-111">參數</span><span class="sxs-lookup"><span data-stu-id="65273-111">PARAMETERS</span></span>

### <span data-ttu-id="65273-112">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="65273-112">-CollectAlert</span></span>
<span data-ttu-id="65273-113">指示 Operational Insights 會收集通知訊息。</span><span class="sxs-lookup"><span data-stu-id="65273-113">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="65273-114">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="65273-114">-CollectCritical</span></span>
<span data-ttu-id="65273-115">指示 Operational Insights 會收集重要的訊息。</span><span class="sxs-lookup"><span data-stu-id="65273-115">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="65273-116">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="65273-116">-CollectDebug</span></span>
<span data-ttu-id="65273-117">指示 Operational Insights 會收集調試訊息。</span><span class="sxs-lookup"><span data-stu-id="65273-117">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="65273-118">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="65273-118">-CollectEmergency</span></span>
<span data-ttu-id="65273-119">表示 Operational Insights 會收集緊急訊息。</span><span class="sxs-lookup"><span data-stu-id="65273-119">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="65273-120">-CollectError</span><span class="sxs-lookup"><span data-stu-id="65273-120">-CollectError</span></span>
<span data-ttu-id="65273-121">表示 Operational Insights 會收集錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="65273-121">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="65273-122">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="65273-122">-CollectInformational</span></span>
<span data-ttu-id="65273-123">表示 Operational Insights 會收集資訊性訊息。</span><span class="sxs-lookup"><span data-stu-id="65273-123">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="65273-124">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="65273-124">-CollectNotice</span></span>
<span data-ttu-id="65273-125">指示 Operational Insights 會收集通知訊息。</span><span class="sxs-lookup"><span data-stu-id="65273-125">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="65273-126">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="65273-126">-CollectWarning</span></span>
<span data-ttu-id="65273-127">表示 syslog 包含警告訊息。</span><span class="sxs-lookup"><span data-stu-id="65273-127">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="65273-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65273-128">-DefaultProfile</span></span>
<span data-ttu-id="65273-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="65273-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65273-130">-設施</span><span class="sxs-lookup"><span data-stu-id="65273-130">-Facility</span></span>
<span data-ttu-id="65273-131">指定資金融通代碼。</span><span class="sxs-lookup"><span data-stu-id="65273-131">Specifies a facility code.</span></span>

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

### <span data-ttu-id="65273-132">-Force</span><span class="sxs-lookup"><span data-stu-id="65273-132">-Force</span></span>
<span data-ttu-id="65273-133">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="65273-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="65273-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="65273-134">-Name</span></span>
<span data-ttu-id="65273-135">指定資料來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="65273-135">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="65273-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65273-136">-ResourceGroupName</span></span>
<span data-ttu-id="65273-137">指定包含 Linux 電腦之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="65273-137">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="65273-138">-工作區</span><span class="sxs-lookup"><span data-stu-id="65273-138">-Workspace</span></span>
<span data-ttu-id="65273-139">指定這個 Cmdlet 在其中運作的工作區。</span><span class="sxs-lookup"><span data-stu-id="65273-139">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="65273-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="65273-140">-WorkspaceName</span></span>
<span data-ttu-id="65273-141">指定此 Cmdlet 作用中的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="65273-141">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="65273-142">-確認</span><span class="sxs-lookup"><span data-stu-id="65273-142">-Confirm</span></span>
<span data-ttu-id="65273-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="65273-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65273-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65273-144">-WhatIf</span></span>
<span data-ttu-id="65273-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="65273-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65273-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="65273-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65273-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65273-147">CommonParameters</span></span>
<span data-ttu-id="65273-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="65273-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65273-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="65273-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65273-150">輸入</span><span class="sxs-lookup"><span data-stu-id="65273-150">INPUTS</span></span>

### <span data-ttu-id="65273-151">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="65273-151">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="65273-152">System.object</span><span class="sxs-lookup"><span data-stu-id="65273-152">System.String</span></span>

## <span data-ttu-id="65273-153">輸出</span><span class="sxs-lookup"><span data-stu-id="65273-153">OUTPUTS</span></span>

### <span data-ttu-id="65273-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="65273-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="65273-155">筆記</span><span class="sxs-lookup"><span data-stu-id="65273-155">NOTES</span></span>

## <span data-ttu-id="65273-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="65273-156">RELATED LINKS</span></span>

[<span data-ttu-id="65273-157">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="65273-157">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="65273-158">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="65273-158">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)


