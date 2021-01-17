---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: 1f685307ae1d6f9a030ac5c242af9fcec97c032b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447087"
---
# <span data-ttu-id="76a31-101">Start-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="76a31-101">Start-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="76a31-102">摘要</span><span class="sxs-lookup"><span data-stu-id="76a31-102">SYNOPSIS</span></span>
<span data-ttu-id="76a31-103">啟動 Azure 自動化來源控制同步作業。</span><span class="sxs-lookup"><span data-stu-id="76a31-103">Starts an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="76a31-104">句法</span><span class="sxs-lookup"><span data-stu-id="76a31-104">SYNTAX</span></span>

```
Start-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76a31-105">說明</span><span class="sxs-lookup"><span data-stu-id="76a31-105">DESCRIPTION</span></span>
<span data-ttu-id="76a31-106">Start-AzAutomationSourceControlSyncJob Cmdlet 會針對指定的來源控制項名稱啟動 Azure 自動化來源控制同步作業。</span><span class="sxs-lookup"><span data-stu-id="76a31-106">The Start-AzAutomationSourceControlSyncJob cmdlet starts a Azure Automation source control sync job for the given source control name.</span></span>

## <span data-ttu-id="76a31-107">示例</span><span class="sxs-lookup"><span data-stu-id="76a31-107">EXAMPLES</span></span>

### <span data-ttu-id="76a31-108">範例1</span><span class="sxs-lookup"><span data-stu-id="76a31-108">Example 1</span></span>
```powershell
PS C:\> Start-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="76a31-109">參數</span><span class="sxs-lookup"><span data-stu-id="76a31-109">PARAMETERS</span></span>

### <span data-ttu-id="76a31-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="76a31-110">-AutomationAccountName</span></span>
<span data-ttu-id="76a31-111">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="76a31-111">The automation account name.</span></span>

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

### <span data-ttu-id="76a31-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76a31-112">-DefaultProfile</span></span>
<span data-ttu-id="76a31-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="76a31-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76a31-114">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="76a31-114">-JobId</span></span>
<span data-ttu-id="76a31-115">來源控制項同步作業 id。</span><span class="sxs-lookup"><span data-stu-id="76a31-115">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a31-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76a31-116">-ResourceGroupName</span></span>
<span data-ttu-id="76a31-117">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="76a31-117">The resource group name.</span></span>

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

### <span data-ttu-id="76a31-118">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="76a31-118">-SourceControlName</span></span>
<span data-ttu-id="76a31-119">來源控制項名稱。</span><span class="sxs-lookup"><span data-stu-id="76a31-119">The source control name.</span></span>

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

### <span data-ttu-id="76a31-120">-確認</span><span class="sxs-lookup"><span data-stu-id="76a31-120">-Confirm</span></span>
<span data-ttu-id="76a31-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="76a31-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76a31-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76a31-122">-WhatIf</span></span>
<span data-ttu-id="76a31-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="76a31-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76a31-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="76a31-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a31-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76a31-125">CommonParameters</span></span>
<span data-ttu-id="76a31-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="76a31-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76a31-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="76a31-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76a31-128">輸入</span><span class="sxs-lookup"><span data-stu-id="76a31-128">INPUTS</span></span>

### <span data-ttu-id="76a31-129">System.object</span><span class="sxs-lookup"><span data-stu-id="76a31-129">System.String</span></span>

## <span data-ttu-id="76a31-130">輸出</span><span class="sxs-lookup"><span data-stu-id="76a31-130">OUTPUTS</span></span>

### <span data-ttu-id="76a31-131">SourceControlSyncJob 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="76a31-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="76a31-132">筆記</span><span class="sxs-lookup"><span data-stu-id="76a31-132">NOTES</span></span>

## <span data-ttu-id="76a31-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="76a31-133">RELATED LINKS</span></span>
