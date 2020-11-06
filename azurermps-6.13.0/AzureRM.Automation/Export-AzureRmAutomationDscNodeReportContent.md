---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 4285EF77-FA70-4BE7-96E0-89E2E8FC5AD6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/export-azurermautomationdscnodereportcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscNodeReportContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscNodeReportContent.md
ms.openlocfilehash: 52ed2c5925758a4d40fdf39dcdadf73eb2fc53b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444088"
---
# <span data-ttu-id="908ed-101">Export-AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="908ed-101">Export-AzureRmAutomationDscNodeReportContent</span></span>

## <span data-ttu-id="908ed-102">摘要</span><span class="sxs-lookup"><span data-stu-id="908ed-102">SYNOPSIS</span></span>
<span data-ttu-id="908ed-103">匯出從 DSC 節點傳送給自動化的 DSC 報表原始內容。</span><span class="sxs-lookup"><span data-stu-id="908ed-103">Exports the raw content of a DSC report sent from a DSC node to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="908ed-104">句法</span><span class="sxs-lookup"><span data-stu-id="908ed-104">SYNTAX</span></span>

```
Export-AzureRmAutomationDscNodeReportContent -NodeId <Guid> -ReportId <Guid> [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="908ed-105">說明</span><span class="sxs-lookup"><span data-stu-id="908ed-105">DESCRIPTION</span></span>
<span data-ttu-id="908ed-106">**Export AzureRmAutomationDscNodeReportContent** Cmdlet 會將所需的 ap 狀態設定的原始內容匯出 (DSC) 報告。</span><span class="sxs-lookup"><span data-stu-id="908ed-106">The **Export-AzureRmAutomationDscNodeReportContent** cmdlet exports the raw contents of an APS Desired State Configuration (DSC) report.</span></span>
<span data-ttu-id="908ed-107">DSC 節點會將 DSC 報告傳送至 Azure 自動化。</span><span class="sxs-lookup"><span data-stu-id="908ed-107">A DSC node sends a DSC report to Azure Automation.</span></span>

## <span data-ttu-id="908ed-108">示例</span><span class="sxs-lookup"><span data-stu-id="908ed-108">EXAMPLES</span></span>

### <span data-ttu-id="908ed-109">範例1：匯出來自 DSC 節點的報表</span><span class="sxs-lookup"><span data-stu-id="908ed-109">Example 1: Export a report from a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "AutomationAccount01" -Name "Computer14"
PS C:\> $Report = Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "ContosoAutomationAccount" -NodeId $Node.Id -Latest
PS C:\> $Report | Export-AzureRmAutomationDscNodeReportContent -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="908ed-110">這組命令會將名為 Computer14 的 DSC 節點中的最新報表匯出到桌面。</span><span class="sxs-lookup"><span data-stu-id="908ed-110">This set of commands exports the latest report from the DSC node named Computer14 to the desktop.</span></span>

## <span data-ttu-id="908ed-111">參數</span><span class="sxs-lookup"><span data-stu-id="908ed-111">PARAMETERS</span></span>

### <span data-ttu-id="908ed-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="908ed-112">-AutomationAccountName</span></span>
<span data-ttu-id="908ed-113">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="908ed-113">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="908ed-114">這個 Cmdlet 會匯出屬於此參數指定之自動化帳戶之 DSC 節點的報告內容。</span><span class="sxs-lookup"><span data-stu-id="908ed-114">This cmdlet exports report content for a DSC node that belongs to the Automation account that this parameter specifies.</span></span>

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

### <span data-ttu-id="908ed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="908ed-115">-DefaultProfile</span></span>
<span data-ttu-id="908ed-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="908ed-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="908ed-117">-Force</span><span class="sxs-lookup"><span data-stu-id="908ed-117">-Force</span></span>
<span data-ttu-id="908ed-118">表示此 Cmdlet 會將現有的本機檔案替換成具有相同名稱的新檔案。</span><span class="sxs-lookup"><span data-stu-id="908ed-118">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="908ed-119">-</span><span class="sxs-lookup"><span data-stu-id="908ed-119">-NodeId</span></span>
<span data-ttu-id="908ed-120">指定此 Cmdlet 匯出報告內容的 DSC 節點的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="908ed-120">Specifies the unique ID of the DSC node for which this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="908ed-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="908ed-121">-OutputFolder</span></span>
<span data-ttu-id="908ed-122">指定此 Cmdlet 匯出報告內容的輸出檔案夾。</span><span class="sxs-lookup"><span data-stu-id="908ed-122">Specifies the output folder where this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="908ed-123">-ReportId</span><span class="sxs-lookup"><span data-stu-id="908ed-123">-ReportId</span></span>
<span data-ttu-id="908ed-124">指定此 Cmdlet 匯出之 DSC 節點報告的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="908ed-124">Specifies the unique ID of the DSC node report that this cmdlet exports.</span></span>

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

### <span data-ttu-id="908ed-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="908ed-125">-ResourceGroupName</span></span>
<span data-ttu-id="908ed-126">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="908ed-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="908ed-127">這個 Cmdlet 會匯出屬於此 Cmdlet 所指定之資源群組之 DSC 節點的報表內容。</span><span class="sxs-lookup"><span data-stu-id="908ed-127">This cmdlet exports the contents of a report for the DSC node that belongs to the resource group that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="908ed-128">-確認</span><span class="sxs-lookup"><span data-stu-id="908ed-128">-Confirm</span></span>
<span data-ttu-id="908ed-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="908ed-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="908ed-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="908ed-130">-WhatIf</span></span>
<span data-ttu-id="908ed-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="908ed-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="908ed-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="908ed-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="908ed-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="908ed-133">CommonParameters</span></span>
<span data-ttu-id="908ed-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="908ed-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="908ed-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="908ed-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="908ed-136">輸入</span><span class="sxs-lookup"><span data-stu-id="908ed-136">INPUTS</span></span>

### <span data-ttu-id="908ed-137">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="908ed-137">System.Guid</span></span>

### <span data-ttu-id="908ed-138">System.object</span><span class="sxs-lookup"><span data-stu-id="908ed-138">System.String</span></span>

## <span data-ttu-id="908ed-139">輸出</span><span class="sxs-lookup"><span data-stu-id="908ed-139">OUTPUTS</span></span>

### <span data-ttu-id="908ed-140">DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="908ed-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="908ed-141">筆記</span><span class="sxs-lookup"><span data-stu-id="908ed-141">NOTES</span></span>

## <span data-ttu-id="908ed-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="908ed-142">RELATED LINKS</span></span>

[<span data-ttu-id="908ed-143">Export-AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="908ed-143">Export-AzureRmAutomationDscNodeReportContent</span></span>](./Export-AzureRmAutomationDscNodeReportContent.md)

[<span data-ttu-id="908ed-144">AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="908ed-144">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="908ed-145">AzureRmAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="908ed-145">Get-AzureRmAutomationDscNodeReport</span></span>](./Get-AzureRmAutomationDscNodeReport.md)


