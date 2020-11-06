---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: 8fa14eef62ac0e8a296349ff3a47cd67086bc3ca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613764"
---
# <span data-ttu-id="a6ebc-101">Get-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="a6ebc-101">Get-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="a6ebc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a6ebc-102">SYNOPSIS</span></span>
<span data-ttu-id="a6ebc-103">取得 Azure 自動化來源控制同步作業。</span><span class="sxs-lookup"><span data-stu-id="a6ebc-103">Gets Azure Automation source control sync jobs.</span></span>

## <span data-ttu-id="a6ebc-104">句法</span><span class="sxs-lookup"><span data-stu-id="a6ebc-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6ebc-105">說明</span><span class="sxs-lookup"><span data-stu-id="a6ebc-105">DESCRIPTION</span></span>
<span data-ttu-id="a6ebc-106">Get-AzAutomationSourceControlSyncJob Cmdlet 會取得 Azure 自動化來源控制同步作業。</span><span class="sxs-lookup"><span data-stu-id="a6ebc-106">The Get-AzAutomationSourceControlSyncJob cmdlet gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="a6ebc-107">若要取得特定的來源控制同步作業，請指定其識別碼。</span><span class="sxs-lookup"><span data-stu-id="a6ebc-107">To get a specific source control sync job, specify its id.</span></span>

## <span data-ttu-id="a6ebc-108">示例</span><span class="sxs-lookup"><span data-stu-id="a6ebc-108">EXAMPLES</span></span>

### <span data-ttu-id="a6ebc-109">範例1</span><span class="sxs-lookup"><span data-stu-id="a6ebc-109">Example 1</span></span>
<span data-ttu-id="a6ebc-110">這個命令會取得 [來源控制 VSTSNative] 的所有自動化來源控制同步作業。</span><span class="sxs-lookup"><span data-stu-id="a6ebc-110">This command gets all the Automation source control sync jobs for the source control VSTSNative.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status StartTime           EndTime
----------------------               -------- ------ ---------           -------
08d6d266-27b6-463c-beea-bc48a67ace15 FullSync Failed 08/15/2018 09:17 AM 08/15/2018 09:18 AM
b566d564-878a-4641-8c44-25bf7850531e FullSync Failed 08/15/2018 09:09 AM 08/15/2018 09:10 AM
```

### <span data-ttu-id="a6ebc-111">範例2</span><span class="sxs-lookup"><span data-stu-id="a6ebc-111">Example 2</span></span>
<span data-ttu-id="a6ebc-112">這個命令會取得來源控制項 VSTSNative 的來源控制同步作業與 id 08d6d266-27b6-463c-beea-bc48a67ace15。</span><span class="sxs-lookup"><span data-stu-id="a6ebc-112">This command gets the source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"
                                                  -Id "08d6d266-27b6-463c-beea-bc48a67ace15"

Status SyncType Exception
------ -------- ---------
Failed FullSync There were errors while syncing the user runbooks. Please see error streams for more information. (T...
```

## <span data-ttu-id="a6ebc-113">參數</span><span class="sxs-lookup"><span data-stu-id="a6ebc-113">PARAMETERS</span></span>

### <span data-ttu-id="a6ebc-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a6ebc-114">-AutomationAccountName</span></span>
<span data-ttu-id="a6ebc-115">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a6ebc-115">The automation account name.</span></span>

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

### <span data-ttu-id="a6ebc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6ebc-116">-DefaultProfile</span></span>
<span data-ttu-id="a6ebc-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a6ebc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6ebc-118">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="a6ebc-118">-JobId</span></span>
<span data-ttu-id="a6ebc-119">來源控制項同步作業 id。</span><span class="sxs-lookup"><span data-stu-id="a6ebc-119">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6ebc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6ebc-120">-ResourceGroupName</span></span>
<span data-ttu-id="a6ebc-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6ebc-121">The resource group name.</span></span>

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

### <span data-ttu-id="a6ebc-122">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="a6ebc-122">-SourceControlName</span></span>
<span data-ttu-id="a6ebc-123">作業的來源控制項名稱。</span><span class="sxs-lookup"><span data-stu-id="a6ebc-123">The source control name of the job.</span></span>

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

### <span data-ttu-id="a6ebc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6ebc-124">CommonParameters</span></span>
<span data-ttu-id="a6ebc-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a6ebc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6ebc-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a6ebc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6ebc-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a6ebc-127">INPUTS</span></span>

### <span data-ttu-id="a6ebc-128">System.object</span><span class="sxs-lookup"><span data-stu-id="a6ebc-128">System.String</span></span>

### <span data-ttu-id="a6ebc-129">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="a6ebc-129">System.Guid</span></span>

## <span data-ttu-id="a6ebc-130">輸出</span><span class="sxs-lookup"><span data-stu-id="a6ebc-130">OUTPUTS</span></span>

### <span data-ttu-id="a6ebc-131">SourceControlSyncJob 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a6ebc-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

### <span data-ttu-id="a6ebc-132">SourceControlSyncJobRecord 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a6ebc-132">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobRecord</span></span>

## <span data-ttu-id="a6ebc-133">筆記</span><span class="sxs-lookup"><span data-stu-id="a6ebc-133">NOTES</span></span>

## <span data-ttu-id="a6ebc-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6ebc-134">RELATED LINKS</span></span>
