---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationsourcecontrolsyncjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
ms.openlocfilehash: 369dfd85b88b079e32e9ea65513d37c99f64b6fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917458"
---
# <span data-ttu-id="5106d-101">Get-AzAutomationSourceControlSyncJobOutput</span><span class="sxs-lookup"><span data-stu-id="5106d-101">Get-AzAutomationSourceControlSyncJobOutput</span></span>

## <span data-ttu-id="5106d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5106d-102">SYNOPSIS</span></span>
<span data-ttu-id="5106d-103">獲得 Azure 自動化原始程式碼管理同步作業的輸出結果。</span><span class="sxs-lookup"><span data-stu-id="5106d-103">Gets the output of an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="5106d-104">語法</span><span class="sxs-lookup"><span data-stu-id="5106d-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJobOutput -SourceControlName <String> -JobId <Guid>
 [-Stream <SourceControlSyncJobStreamType>] [-StreamId <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5106d-105">描述</span><span class="sxs-lookup"><span data-stu-id="5106d-105">DESCRIPTION</span></span>
<span data-ttu-id="5106d-106">**Get-AzAutomationSourceControlSyncJobOutput** Cmdlet 會取得 Azure 自動化原始程式碼管理同步作業的輸出結果。</span><span class="sxs-lookup"><span data-stu-id="5106d-106">The **Get-AzAutomationSourceControlSyncJobOutput** cmdlet gets the output for a Azure Automation source control sync job.</span></span>

## <span data-ttu-id="5106d-107">例子</span><span class="sxs-lookup"><span data-stu-id="5106d-107">EXAMPLES</span></span>

### <span data-ttu-id="5106d-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="5106d-108">Example 1</span></span>
<span data-ttu-id="5106d-109">此命令會獲得原始程式碼管理同步處理工作的輸出，以及原始程式碼管理 VSTSNative 的 id 08d6d266-27b6-463c-beea-bc48a67ace15。</span><span class="sxs-lookup"><span data-stu-id="5106d-109">This command gets the output of source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


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

## <span data-ttu-id="5106d-110">參數</span><span class="sxs-lookup"><span data-stu-id="5106d-110">PARAMETERS</span></span>

### <span data-ttu-id="5106d-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5106d-111">-AutomationAccountName</span></span>
<span data-ttu-id="5106d-112">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="5106d-112">The automation account name.</span></span>

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

### <span data-ttu-id="5106d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5106d-113">-DefaultProfile</span></span>
<span data-ttu-id="5106d-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5106d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5106d-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="5106d-115">-JobId</span></span>
<span data-ttu-id="5106d-116">原始程式碼管理同步作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="5106d-116">The source control sync job id.</span></span>

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

### <span data-ttu-id="5106d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5106d-117">-ResourceGroupName</span></span>
<span data-ttu-id="5106d-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="5106d-118">The resource group name.</span></span>

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

### <span data-ttu-id="5106d-119">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="5106d-119">-SourceControlName</span></span>
<span data-ttu-id="5106d-120">原始程式碼管理名稱。</span><span class="sxs-lookup"><span data-stu-id="5106d-120">The source control name.</span></span>

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

### <span data-ttu-id="5106d-121">-Stream</span><span class="sxs-lookup"><span data-stu-id="5106d-121">-Stream</span></span>
<span data-ttu-id="5106d-122">串流類型。</span><span class="sxs-lookup"><span data-stu-id="5106d-122">The stream type.</span></span>
<span data-ttu-id="5106d-123">預設值為 Any。</span><span class="sxs-lookup"><span data-stu-id="5106d-123">Defaults to Any.</span></span>

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

### <span data-ttu-id="5106d-124">-StreamId</span><span class="sxs-lookup"><span data-stu-id="5106d-124">-StreamId</span></span>
<span data-ttu-id="5106d-125">串流識別碼。</span><span class="sxs-lookup"><span data-stu-id="5106d-125">The stream id.</span></span>

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

### <span data-ttu-id="5106d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5106d-126">CommonParameters</span></span>
<span data-ttu-id="5106d-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5106d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5106d-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5106d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5106d-129">輸入</span><span class="sxs-lookup"><span data-stu-id="5106d-129">INPUTS</span></span>

### <span data-ttu-id="5106d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5106d-130">System.String</span></span>

### <span data-ttu-id="5106d-131">System.Guid</span><span class="sxs-lookup"><span data-stu-id="5106d-131">System.Guid</span></span>

### <span data-ttu-id="5106d-132">Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType</span><span class="sxs-lookup"><span data-stu-id="5106d-132">Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType</span></span>

## <span data-ttu-id="5106d-133">輸出</span><span class="sxs-lookup"><span data-stu-id="5106d-133">OUTPUTS</span></span>

### <span data-ttu-id="5106d-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStream</span><span class="sxs-lookup"><span data-stu-id="5106d-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStream</span></span>

### <span data-ttu-id="5106d-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="5106d-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStreamRecord</span></span>

## <span data-ttu-id="5106d-136">筆記</span><span class="sxs-lookup"><span data-stu-id="5106d-136">NOTES</span></span>

## <span data-ttu-id="5106d-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="5106d-137">RELATED LINKS</span></span>
