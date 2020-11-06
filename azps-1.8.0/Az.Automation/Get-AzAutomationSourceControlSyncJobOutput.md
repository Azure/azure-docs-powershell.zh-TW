---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrolsyncjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
ms.openlocfilehash: 63ff1ea82f3167738161191900e9516513b034bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93623035"
---
# <span data-ttu-id="9a67e-101">Get-AzAutomationSourceControlSyncJobOutput</span><span class="sxs-lookup"><span data-stu-id="9a67e-101">Get-AzAutomationSourceControlSyncJobOutput</span></span>

## <span data-ttu-id="9a67e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9a67e-102">SYNOPSIS</span></span>
<span data-ttu-id="9a67e-103">取得 Azure 自動化來源控制同步作業的輸出。</span><span class="sxs-lookup"><span data-stu-id="9a67e-103">Gets the output of an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="9a67e-104">句法</span><span class="sxs-lookup"><span data-stu-id="9a67e-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJobOutput -SourceControlName <String> -JobId <Guid>
 [-Stream <SourceControlSyncJobStreamType>] [-StreamId <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a67e-105">說明</span><span class="sxs-lookup"><span data-stu-id="9a67e-105">DESCRIPTION</span></span>
<span data-ttu-id="9a67e-106">**AzAutomationSourceControlSyncJobOutput** Cmdlet 會取得 Azure 自動化來源控制同步作業的輸出。</span><span class="sxs-lookup"><span data-stu-id="9a67e-106">The **Get-AzAutomationSourceControlSyncJobOutput** cmdlet gets the output for a Azure Automation source control sync job.</span></span>

## <span data-ttu-id="9a67e-107">示例</span><span class="sxs-lookup"><span data-stu-id="9a67e-107">EXAMPLES</span></span>

### <span data-ttu-id="9a67e-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9a67e-108">Example 1</span></span>
<span data-ttu-id="9a67e-109">這個命令會取得原始程式碼管理同步處理作業的輸出（含來源控制項 VSTSNative 的識別碼08d6d266-27b6-463c-beea-bc48a67ace15）。</span><span class="sxs-lookup"><span data-stu-id="9a67e-109">This command gets the output of source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJobOutput -ResourceGroupName "rg1" `
                                                        -AutomationAccountName "devAccount" `
                                                        -Name "VSTSNative"
                                                        -Id "08d6d266-27b6-463c-beea-bc48a67ace15" `
                                                        -Stream Output | ForEach-Object {$_.summary}

========================================================================================================

Azure Automation Source Control Public Preview.
Supported runbooks to sync: PowerShell Workflow, PowerShell Scripts, DSC Configurations, Graphical, and Python 2.
Setting AzureRmEnvironment.
Getting AzureRunAsConnection.
Logging in to Azure...
Source control information for syncing:
[RepoUrl = https://contoso.visualstudio.com/_git/GitDemo] [Branch  = master] [FolderPath = /]
Verifying url: https://fcontoso.visualstudio.com/_git/GitDemo
Connecting to VSTS...

Source Control Sync Summary:

2 files synced:
 - RunbookA.ps1
 - RunbookB.ps1

Failed to import runbook:
 - RunbookC.ps1

File is not a runbook:
 - README.md
 - text_file.txt

File size exceeds 1Mb:
 - RunbookD_GreatherThan1MB.ps1

Invalid runbook name:
 - RunbookZ_ĈĦŕĬŞ.ps1

========================================================================================================
```

## <span data-ttu-id="9a67e-110">參數</span><span class="sxs-lookup"><span data-stu-id="9a67e-110">PARAMETERS</span></span>

### <span data-ttu-id="9a67e-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9a67e-111">-AutomationAccountName</span></span>
<span data-ttu-id="9a67e-112">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="9a67e-112">The automation account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a67e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a67e-113">-DefaultProfile</span></span>
<span data-ttu-id="9a67e-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9a67e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a67e-115">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="9a67e-115">-JobId</span></span>
<span data-ttu-id="9a67e-116">來源控制項同步作業 id。</span><span class="sxs-lookup"><span data-stu-id="9a67e-116">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a67e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a67e-117">-ResourceGroupName</span></span>
<span data-ttu-id="9a67e-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a67e-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a67e-119">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="9a67e-119">-SourceControlName</span></span>
<span data-ttu-id="9a67e-120">來源控制項名稱。</span><span class="sxs-lookup"><span data-stu-id="9a67e-120">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a67e-121">資料流程</span><span class="sxs-lookup"><span data-stu-id="9a67e-121">-Stream</span></span>
<span data-ttu-id="9a67e-122">資料流程類型。</span><span class="sxs-lookup"><span data-stu-id="9a67e-122">The stream type.</span></span>
<span data-ttu-id="9a67e-123">預設為 [任何]。</span><span class="sxs-lookup"><span data-stu-id="9a67e-123">Defaults to Any.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType
Parameter Sets: (All)
Aliases:
Accepted values: Any, Output, Error

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a67e-124">-StreamId</span><span class="sxs-lookup"><span data-stu-id="9a67e-124">-StreamId</span></span>
<span data-ttu-id="9a67e-125">串流 id。</span><span class="sxs-lookup"><span data-stu-id="9a67e-125">The stream id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceControlSyncJobStreamId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a67e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a67e-126">CommonParameters</span></span>
<span data-ttu-id="9a67e-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9a67e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a67e-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9a67e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a67e-129">輸入</span><span class="sxs-lookup"><span data-stu-id="9a67e-129">INPUTS</span></span>

### <span data-ttu-id="9a67e-130">System.object</span><span class="sxs-lookup"><span data-stu-id="9a67e-130">System.String</span></span>

### <span data-ttu-id="9a67e-131">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="9a67e-131">System.Guid</span></span>

### <span data-ttu-id="9a67e-132">SourceControlSyncJobStreamType （自動化）。</span><span class="sxs-lookup"><span data-stu-id="9a67e-132">Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType</span></span>

## <span data-ttu-id="9a67e-133">輸出</span><span class="sxs-lookup"><span data-stu-id="9a67e-133">OUTPUTS</span></span>

### <span data-ttu-id="9a67e-134">SourceControlSyncJobStream 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9a67e-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStream</span></span>

### <span data-ttu-id="9a67e-135">SourceControlSyncJobStreamRecord 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9a67e-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStreamRecord</span></span>

## <span data-ttu-id="9a67e-136">筆記</span><span class="sxs-lookup"><span data-stu-id="9a67e-136">NOTES</span></span>

## <span data-ttu-id="9a67e-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="9a67e-137">RELATED LINKS</span></span>
