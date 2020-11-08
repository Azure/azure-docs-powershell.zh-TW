---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 4285EF77-FA70-4BE7-96E0-89E2E8FC5AD6
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationdscnodereportcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
ms.openlocfilehash: dd29a092ec0ca3b24614b363147d4c50bf14dcbe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958665"
---
# <span data-ttu-id="289cd-101">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="289cd-101">Export-AzAutomationDscNodeReportContent</span></span>

## <span data-ttu-id="289cd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="289cd-102">SYNOPSIS</span></span>
<span data-ttu-id="289cd-103">匯出從 DSC 節點傳送給自動化的 DSC 報表原始內容。</span><span class="sxs-lookup"><span data-stu-id="289cd-103">Exports the raw content of a DSC report sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="289cd-104">句法</span><span class="sxs-lookup"><span data-stu-id="289cd-104">SYNTAX</span></span>

```
Export-AzAutomationDscNodeReportContent -NodeId <Guid> -ReportId <Guid> [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="289cd-105">說明</span><span class="sxs-lookup"><span data-stu-id="289cd-105">DESCRIPTION</span></span>
<span data-ttu-id="289cd-106">**Export AzAutomationDscNodeReportContent** Cmdlet 會將所需的 ap 狀態設定的原始內容匯出 (DSC) 報告。</span><span class="sxs-lookup"><span data-stu-id="289cd-106">The **Export-AzAutomationDscNodeReportContent** cmdlet exports the raw contents of an APS Desired State Configuration (DSC) report.</span></span>
<span data-ttu-id="289cd-107">DSC 節點會將 DSC 報告傳送至 Azure 自動化。</span><span class="sxs-lookup"><span data-stu-id="289cd-107">A DSC node sends a DSC report to Azure Automation.</span></span>

## <span data-ttu-id="289cd-108">示例</span><span class="sxs-lookup"><span data-stu-id="289cd-108">EXAMPLES</span></span>

### <span data-ttu-id="289cd-109">範例1：匯出來自 DSC 節點的報表</span><span class="sxs-lookup"><span data-stu-id="289cd-109">Example 1: Export a report from a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "AutomationAccount01" -Name "Computer14"
PS C:\> $Report = Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "ContosoAutomationAccount" -NodeId $Node.Id -Latest
PS C:\> $Report | Export-AzAutomationDscNodeReportContent -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="289cd-110">這組命令會將名為 Computer14 的 DSC 節點中的最新報表匯出到桌面。</span><span class="sxs-lookup"><span data-stu-id="289cd-110">This set of commands exports the latest report from the DSC node named Computer14 to the desktop.</span></span>

## <span data-ttu-id="289cd-111">參數</span><span class="sxs-lookup"><span data-stu-id="289cd-111">PARAMETERS</span></span>

### <span data-ttu-id="289cd-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="289cd-112">-AutomationAccountName</span></span>
<span data-ttu-id="289cd-113">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="289cd-113">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="289cd-114">這個 Cmdlet 會匯出屬於此參數指定之自動化帳戶之 DSC 節點的報告內容。</span><span class="sxs-lookup"><span data-stu-id="289cd-114">This cmdlet exports report content for a DSC node that belongs to the Automation account that this parameter specifies.</span></span>

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

### <span data-ttu-id="289cd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="289cd-115">-DefaultProfile</span></span>
<span data-ttu-id="289cd-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="289cd-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="289cd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="289cd-117">-Force</span></span>
<span data-ttu-id="289cd-118">表示此 Cmdlet 會將現有的本機檔案替換成具有相同名稱的新檔案。</span><span class="sxs-lookup"><span data-stu-id="289cd-118">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="289cd-119">-</span><span class="sxs-lookup"><span data-stu-id="289cd-119">-NodeId</span></span>
<span data-ttu-id="289cd-120">指定此 Cmdlet 匯出報告內容的 DSC 節點的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="289cd-120">Specifies the unique ID of the DSC node for which this cmdlet exports report contents.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="289cd-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="289cd-121">-OutputFolder</span></span>
<span data-ttu-id="289cd-122">指定此 Cmdlet 匯出報告內容的輸出檔案夾。</span><span class="sxs-lookup"><span data-stu-id="289cd-122">Specifies the output folder where this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="289cd-123">-ReportId</span><span class="sxs-lookup"><span data-stu-id="289cd-123">-ReportId</span></span>
<span data-ttu-id="289cd-124">指定此 Cmdlet 匯出之 DSC 節點報告的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="289cd-124">Specifies the unique ID of the DSC node report that this cmdlet exports.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="289cd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="289cd-125">-ResourceGroupName</span></span>
<span data-ttu-id="289cd-126">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="289cd-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="289cd-127">這個 Cmdlet 會匯出屬於此 Cmdlet 所指定之資源群組之 DSC 節點的報表內容。</span><span class="sxs-lookup"><span data-stu-id="289cd-127">This cmdlet exports the contents of a report for the DSC node that belongs to the resource group that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="289cd-128">-確認</span><span class="sxs-lookup"><span data-stu-id="289cd-128">-Confirm</span></span>
<span data-ttu-id="289cd-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="289cd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="289cd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="289cd-130">-WhatIf</span></span>
<span data-ttu-id="289cd-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="289cd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="289cd-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="289cd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="289cd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="289cd-133">CommonParameters</span></span>
<span data-ttu-id="289cd-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="289cd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="289cd-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="289cd-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="289cd-136">輸入</span><span class="sxs-lookup"><span data-stu-id="289cd-136">INPUTS</span></span>

### <span data-ttu-id="289cd-137">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="289cd-137">System.Guid</span></span>

### <span data-ttu-id="289cd-138">System.object</span><span class="sxs-lookup"><span data-stu-id="289cd-138">System.String</span></span>

## <span data-ttu-id="289cd-139">輸出</span><span class="sxs-lookup"><span data-stu-id="289cd-139">OUTPUTS</span></span>

### <span data-ttu-id="289cd-140">DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="289cd-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="289cd-141">筆記</span><span class="sxs-lookup"><span data-stu-id="289cd-141">NOTES</span></span>

## <span data-ttu-id="289cd-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="289cd-142">RELATED LINKS</span></span>

[<span data-ttu-id="289cd-143">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="289cd-143">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)

[<span data-ttu-id="289cd-144">AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="289cd-144">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="289cd-145">AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="289cd-145">Get-AzAutomationDscNodeReport</span></span>](./Get-AzAutomationDscNodeReport.md)

