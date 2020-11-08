---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: 12d9ff89ea87ae24d3817cdd3ec0b706582e4849
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970863"
---
# <span data-ttu-id="7a74f-101">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="7a74f-101">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="7a74f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7a74f-102">SYNOPSIS</span></span>
<span data-ttu-id="7a74f-103">新增資料來源至 Linux 電腦。</span><span class="sxs-lookup"><span data-stu-id="7a74f-103">Adds a data source to Linux computers.</span></span>

## <span data-ttu-id="7a74f-104">句法</span><span class="sxs-lookup"><span data-stu-id="7a74f-104">SYNTAX</span></span>

### <span data-ttu-id="7a74f-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="7a74f-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a74f-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7a74f-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Facility] <String>
 [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning] [-CollectNotice]
 [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a74f-107">說明</span><span class="sxs-lookup"><span data-stu-id="7a74f-107">DESCRIPTION</span></span>
<span data-ttu-id="7a74f-108">**新的-AzOperationalInsightsLinuxSyslogDataSource** Cmdlet 會將 syslog 資料來源新增到工作區中的連線 Linux 電腦。</span><span class="sxs-lookup"><span data-stu-id="7a74f-108">The **New-AzOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="7a74f-109">Azure Operational Insights 可以收集 syslog 資料。</span><span class="sxs-lookup"><span data-stu-id="7a74f-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="7a74f-110">示例</span><span class="sxs-lookup"><span data-stu-id="7a74f-110">EXAMPLES</span></span>

### <span data-ttu-id="7a74f-111">範例1：建立 syslog 資料來源</span><span class="sxs-lookup"><span data-stu-id="7a74f-111">Example 1: Create syslog data sources</span></span>
```
$FacilityNames       = @()
$FacilityNames      += 'auth'
$FacilityNames      += 'authpriv'
$FacilityNames      += 'cron'
$FacilityNames      += 'daemon'
$FacilityNames      += 'ftp'
$FacilityNames      += 'kern'
$FacilityNames      += 'mail'
$FacilityNames      += 'syslog'
$FacilityNames      += 'user'
$FacilityNames      += 'uucp'
$ResourceGroupName   = 'MyResourceGroup'
$WorkspaceName       = 'MyWorkspaceName'

$Count = 0
foreach ($FacilityName in $FacilityNames) {
    $Count++
    $null = New-AzOperationalInsightsLinuxSyslogDataSource `
    -ResourceGroupName $ResourceGroupName `
    -WorkspaceName $WorkspaceName `
    -Name "Linux-syslog-$($Count)" `
    -Facility $FacilityName `
    -CollectEmergency `
    -CollectAlert `
    -CollectCritical `
    -CollectError `
    -CollectWarning `
    -CollectNotice `
    -CollectDebug `
    -CollectInformational
}

Get-AzOperationalInsightsDataSource `
   -ResourceGroupName $ResourceGroupName `
   -WorkspaceName $WorkspaceName `
   -Kind 'LinuxSyslog'
```

## <span data-ttu-id="7a74f-112">參數</span><span class="sxs-lookup"><span data-stu-id="7a74f-112">PARAMETERS</span></span>

### <span data-ttu-id="7a74f-113">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="7a74f-113">-CollectAlert</span></span>
<span data-ttu-id="7a74f-114">指示 Operational Insights 會收集通知訊息。</span><span class="sxs-lookup"><span data-stu-id="7a74f-114">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="7a74f-115">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="7a74f-115">-CollectCritical</span></span>
<span data-ttu-id="7a74f-116">指示 Operational Insights 會收集重要的訊息。</span><span class="sxs-lookup"><span data-stu-id="7a74f-116">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="7a74f-117">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="7a74f-117">-CollectDebug</span></span>
<span data-ttu-id="7a74f-118">指示 Operational Insights 會收集調試訊息。</span><span class="sxs-lookup"><span data-stu-id="7a74f-118">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="7a74f-119">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="7a74f-119">-CollectEmergency</span></span>
<span data-ttu-id="7a74f-120">表示 Operational Insights 會收集緊急訊息。</span><span class="sxs-lookup"><span data-stu-id="7a74f-120">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="7a74f-121">-CollectError</span><span class="sxs-lookup"><span data-stu-id="7a74f-121">-CollectError</span></span>
<span data-ttu-id="7a74f-122">表示 Operational Insights 會收集錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="7a74f-122">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="7a74f-123">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="7a74f-123">-CollectInformational</span></span>
<span data-ttu-id="7a74f-124">表示 Operational Insights 會收集資訊性訊息。</span><span class="sxs-lookup"><span data-stu-id="7a74f-124">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="7a74f-125">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="7a74f-125">-CollectNotice</span></span>
<span data-ttu-id="7a74f-126">指示 Operational Insights 會收集通知訊息。</span><span class="sxs-lookup"><span data-stu-id="7a74f-126">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="7a74f-127">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="7a74f-127">-CollectWarning</span></span>
<span data-ttu-id="7a74f-128">表示 syslog 包含警告訊息。</span><span class="sxs-lookup"><span data-stu-id="7a74f-128">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="7a74f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a74f-129">-DefaultProfile</span></span>
<span data-ttu-id="7a74f-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="7a74f-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a74f-131">-設施</span><span class="sxs-lookup"><span data-stu-id="7a74f-131">-Facility</span></span>
<span data-ttu-id="7a74f-132">指定資金融通代碼。</span><span class="sxs-lookup"><span data-stu-id="7a74f-132">Specifies a facility code.</span></span>

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

### <span data-ttu-id="7a74f-133">-Force</span><span class="sxs-lookup"><span data-stu-id="7a74f-133">-Force</span></span>
<span data-ttu-id="7a74f-134">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="7a74f-134">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7a74f-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="7a74f-135">-Name</span></span>
<span data-ttu-id="7a74f-136">指定資料來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="7a74f-136">Specifies a name for the data source.</span></span> <span data-ttu-id="7a74f-137">此名稱不會在 Azure 入口網站中公開，而且任何字串只要是唯一的，就可以使用。</span><span class="sxs-lookup"><span data-stu-id="7a74f-137">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

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

### <span data-ttu-id="7a74f-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a74f-138">-ResourceGroupName</span></span>
<span data-ttu-id="7a74f-139">指定包含 Linux 電腦之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7a74f-139">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="7a74f-140">-工作區</span><span class="sxs-lookup"><span data-stu-id="7a74f-140">-Workspace</span></span>
<span data-ttu-id="7a74f-141">指定這個 Cmdlet 在其中運作的工作區。</span><span class="sxs-lookup"><span data-stu-id="7a74f-141">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="7a74f-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7a74f-142">-WorkspaceName</span></span>
<span data-ttu-id="7a74f-143">指定此 Cmdlet 作用中的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="7a74f-143">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="7a74f-144">-確認</span><span class="sxs-lookup"><span data-stu-id="7a74f-144">-Confirm</span></span>
<span data-ttu-id="7a74f-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7a74f-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a74f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a74f-146">-WhatIf</span></span>
<span data-ttu-id="7a74f-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7a74f-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a74f-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7a74f-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a74f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a74f-149">CommonParameters</span></span>
<span data-ttu-id="7a74f-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7a74f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a74f-151">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7a74f-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a74f-152">輸入</span><span class="sxs-lookup"><span data-stu-id="7a74f-152">INPUTS</span></span>

### <span data-ttu-id="7a74f-153">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="7a74f-153">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="7a74f-154">System.object</span><span class="sxs-lookup"><span data-stu-id="7a74f-154">System.String</span></span>

## <span data-ttu-id="7a74f-155">輸出</span><span class="sxs-lookup"><span data-stu-id="7a74f-155">OUTPUTS</span></span>

### <span data-ttu-id="7a74f-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="7a74f-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="7a74f-157">筆記</span><span class="sxs-lookup"><span data-stu-id="7a74f-157">NOTES</span></span>

## <span data-ttu-id="7a74f-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="7a74f-158">RELATED LINKS</span></span>

[<span data-ttu-id="7a74f-159">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="7a74f-159">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="7a74f-160">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="7a74f-160">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)


