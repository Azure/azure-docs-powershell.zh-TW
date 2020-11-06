---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: 86bc4b8bedbaafb6da1267d94ffa01b3d0ca95c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447307"
---
# <span data-ttu-id="12e2a-101">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="12e2a-101">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="12e2a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="12e2a-102">SYNOPSIS</span></span>
<span data-ttu-id="12e2a-103">新增資料來源至 Linux 電腦。</span><span class="sxs-lookup"><span data-stu-id="12e2a-103">Adds a data source to Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12e2a-104">句法</span><span class="sxs-lookup"><span data-stu-id="12e2a-104">SYNTAX</span></span>

### <span data-ttu-id="12e2a-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="12e2a-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12e2a-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="12e2a-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning]
 [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12e2a-107">說明</span><span class="sxs-lookup"><span data-stu-id="12e2a-107">DESCRIPTION</span></span>
<span data-ttu-id="12e2a-108">**新的-AzureRmOperationalInsightsLinuxSyslogDataSource** Cmdlet 會將 syslog 資料來源新增到工作區中的連線 Linux 電腦。</span><span class="sxs-lookup"><span data-stu-id="12e2a-108">The **New-AzureRmOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="12e2a-109">Azure Operational Insights 可以收集 syslog 資料。</span><span class="sxs-lookup"><span data-stu-id="12e2a-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="12e2a-110">示例</span><span class="sxs-lookup"><span data-stu-id="12e2a-110">EXAMPLES</span></span>

## <span data-ttu-id="12e2a-111">參數</span><span class="sxs-lookup"><span data-stu-id="12e2a-111">PARAMETERS</span></span>

### <span data-ttu-id="12e2a-112">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="12e2a-112">-CollectAlert</span></span>
<span data-ttu-id="12e2a-113">指示 Operational Insights 會收集通知訊息。</span><span class="sxs-lookup"><span data-stu-id="12e2a-113">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="12e2a-114">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="12e2a-114">-CollectCritical</span></span>
<span data-ttu-id="12e2a-115">指示 Operational Insights 會收集重要的訊息。</span><span class="sxs-lookup"><span data-stu-id="12e2a-115">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="12e2a-116">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="12e2a-116">-CollectDebug</span></span>
<span data-ttu-id="12e2a-117">指示 Operational Insights 會收集調試訊息。</span><span class="sxs-lookup"><span data-stu-id="12e2a-117">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="12e2a-118">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="12e2a-118">-CollectEmergency</span></span>
<span data-ttu-id="12e2a-119">表示 Operational Insights 會收集緊急訊息。</span><span class="sxs-lookup"><span data-stu-id="12e2a-119">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="12e2a-120">-CollectError</span><span class="sxs-lookup"><span data-stu-id="12e2a-120">-CollectError</span></span>
<span data-ttu-id="12e2a-121">表示 Operational Insights 會收集錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="12e2a-121">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="12e2a-122">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="12e2a-122">-CollectInformational</span></span>
<span data-ttu-id="12e2a-123">表示 Operational Insights 會收集資訊性訊息。</span><span class="sxs-lookup"><span data-stu-id="12e2a-123">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="12e2a-124">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="12e2a-124">-CollectNotice</span></span>
<span data-ttu-id="12e2a-125">指示 Operational Insights 會收集通知訊息。</span><span class="sxs-lookup"><span data-stu-id="12e2a-125">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="12e2a-126">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="12e2a-126">-CollectWarning</span></span>
<span data-ttu-id="12e2a-127">表示 syslog 包含警告訊息。</span><span class="sxs-lookup"><span data-stu-id="12e2a-127">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="12e2a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12e2a-128">-DefaultProfile</span></span>
<span data-ttu-id="12e2a-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="12e2a-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12e2a-130">-設施</span><span class="sxs-lookup"><span data-stu-id="12e2a-130">-Facility</span></span>
<span data-ttu-id="12e2a-131">指定資金融通代碼。</span><span class="sxs-lookup"><span data-stu-id="12e2a-131">Specifies a facility code.</span></span>

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

### <span data-ttu-id="12e2a-132">-Force</span><span class="sxs-lookup"><span data-stu-id="12e2a-132">-Force</span></span>
<span data-ttu-id="12e2a-133">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="12e2a-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="12e2a-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="12e2a-134">-Name</span></span>
<span data-ttu-id="12e2a-135">指定資料來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="12e2a-135">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="12e2a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12e2a-136">-ResourceGroupName</span></span>
<span data-ttu-id="12e2a-137">指定包含 Linux 電腦之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="12e2a-137">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="12e2a-138">-工作區</span><span class="sxs-lookup"><span data-stu-id="12e2a-138">-Workspace</span></span>
<span data-ttu-id="12e2a-139">指定這個 Cmdlet 在其中運作的工作區。</span><span class="sxs-lookup"><span data-stu-id="12e2a-139">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="12e2a-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="12e2a-140">-WorkspaceName</span></span>
<span data-ttu-id="12e2a-141">指定此 Cmdlet 作用中的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="12e2a-141">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="12e2a-142">-確認</span><span class="sxs-lookup"><span data-stu-id="12e2a-142">-Confirm</span></span>
<span data-ttu-id="12e2a-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="12e2a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12e2a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12e2a-144">-WhatIf</span></span>
<span data-ttu-id="12e2a-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="12e2a-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12e2a-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="12e2a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12e2a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e2a-147">CommonParameters</span></span>
<span data-ttu-id="12e2a-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="12e2a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e2a-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="12e2a-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e2a-150">輸入</span><span class="sxs-lookup"><span data-stu-id="12e2a-150">INPUTS</span></span>

### <span data-ttu-id="12e2a-151">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="12e2a-151">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="12e2a-152">參數：工作區 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="12e2a-152">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="12e2a-153">System.object</span><span class="sxs-lookup"><span data-stu-id="12e2a-153">System.String</span></span>

## <span data-ttu-id="12e2a-154">輸出</span><span class="sxs-lookup"><span data-stu-id="12e2a-154">OUTPUTS</span></span>

### <span data-ttu-id="12e2a-155">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="12e2a-155">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="12e2a-156">筆記</span><span class="sxs-lookup"><span data-stu-id="12e2a-156">NOTES</span></span>

## <span data-ttu-id="12e2a-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="12e2a-157">RELATED LINKS</span></span>

[<span data-ttu-id="12e2a-158">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="12e2a-158">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="12e2a-159">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="12e2a-159">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxSyslogCollection.md)


