---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/start-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: f232f876ff77944beb1d506e5763621f9470cd21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903338"
---
# <span data-ttu-id="b5405-101">Start-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="b5405-101">Start-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="b5405-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b5405-102">SYNOPSIS</span></span>
<span data-ttu-id="b5405-103">啟動 Azure 自動化原始程式碼管理同步作業。</span><span class="sxs-lookup"><span data-stu-id="b5405-103">Starts an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="b5405-104">語法</span><span class="sxs-lookup"><span data-stu-id="b5405-104">SYNTAX</span></span>

```
Start-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5405-105">描述</span><span class="sxs-lookup"><span data-stu-id="b5405-105">DESCRIPTION</span></span>
<span data-ttu-id="b5405-106">Cmdlet Start-AzAutomationSourceControlSyncJob啟動指定原始程式碼管理名稱的 Azure Automation 原始程式碼管理同步作業。</span><span class="sxs-lookup"><span data-stu-id="b5405-106">The Start-AzAutomationSourceControlSyncJob cmdlet starts a Azure Automation source control sync job for the given source control name.</span></span>

## <span data-ttu-id="b5405-107">例子</span><span class="sxs-lookup"><span data-stu-id="b5405-107">EXAMPLES</span></span>

### <span data-ttu-id="b5405-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="b5405-108">Example 1</span></span>
```powershell
PS C:\> Start-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="b5405-109">參數</span><span class="sxs-lookup"><span data-stu-id="b5405-109">PARAMETERS</span></span>

### <span data-ttu-id="b5405-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b5405-110">-AutomationAccountName</span></span>
<span data-ttu-id="b5405-111">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="b5405-111">The automation account name.</span></span>

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

### <span data-ttu-id="b5405-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5405-112">-DefaultProfile</span></span>
<span data-ttu-id="b5405-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b5405-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5405-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="b5405-114">-JobId</span></span>
<span data-ttu-id="b5405-115">原始程式碼管理同步作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="b5405-115">The source control sync job id.</span></span>

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

### <span data-ttu-id="b5405-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5405-116">-ResourceGroupName</span></span>
<span data-ttu-id="b5405-117">資源組名。</span><span class="sxs-lookup"><span data-stu-id="b5405-117">The resource group name.</span></span>

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

### <span data-ttu-id="b5405-118">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="b5405-118">-SourceControlName</span></span>
<span data-ttu-id="b5405-119">原始程式碼管理名稱。</span><span class="sxs-lookup"><span data-stu-id="b5405-119">The source control name.</span></span>

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

### <span data-ttu-id="b5405-120">-確認</span><span class="sxs-lookup"><span data-stu-id="b5405-120">-Confirm</span></span>
<span data-ttu-id="b5405-121">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b5405-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5405-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5405-122">-WhatIf</span></span>
<span data-ttu-id="b5405-123">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b5405-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5405-124">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b5405-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5405-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5405-125">CommonParameters</span></span>
<span data-ttu-id="b5405-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b5405-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5405-127">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b5405-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5405-128">輸入</span><span class="sxs-lookup"><span data-stu-id="b5405-128">INPUTS</span></span>

### <span data-ttu-id="b5405-129">System.String</span><span class="sxs-lookup"><span data-stu-id="b5405-129">System.String</span></span>

## <span data-ttu-id="b5405-130">輸出</span><span class="sxs-lookup"><span data-stu-id="b5405-130">OUTPUTS</span></span>

### <span data-ttu-id="b5405-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="b5405-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="b5405-132">筆記</span><span class="sxs-lookup"><span data-stu-id="b5405-132">NOTES</span></span>

## <span data-ttu-id="b5405-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5405-133">RELATED LINKS</span></span>
