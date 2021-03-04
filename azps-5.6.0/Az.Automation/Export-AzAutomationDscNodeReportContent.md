---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 4285EF77-FA70-4BE7-96E0-89E2E8FC5AD6
online version: https://docs.microsoft.com/powershell/module/az.automation/export-azautomationdscnodereportcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
ms.openlocfilehash: c4006c13130cecb27c35d466c43cfd75583644b4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907821"
---
# <span data-ttu-id="cdc95-101">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="cdc95-101">Export-AzAutomationDscNodeReportContent</span></span>

## <span data-ttu-id="cdc95-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cdc95-102">SYNOPSIS</span></span>
<span data-ttu-id="cdc95-103">將從 DSC 節點所送出之 DSC 報表的原始內容匯出至自動化。</span><span class="sxs-lookup"><span data-stu-id="cdc95-103">Exports the raw content of a DSC report sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="cdc95-104">語法</span><span class="sxs-lookup"><span data-stu-id="cdc95-104">SYNTAX</span></span>

```
Export-AzAutomationDscNodeReportContent -NodeId <Guid> -ReportId <Guid> [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdc95-105">描述</span><span class="sxs-lookup"><span data-stu-id="cdc95-105">DESCRIPTION</span></span>
<span data-ttu-id="cdc95-106">**Export-AzAutomationDscNodeReportContent** Cmdlet 會匯出 APS 想要狀態組態 (DSC) 報表的原始內容。</span><span class="sxs-lookup"><span data-stu-id="cdc95-106">The **Export-AzAutomationDscNodeReportContent** cmdlet exports the raw contents of an APS Desired State Configuration (DSC) report.</span></span>
<span data-ttu-id="cdc95-107">DSC 節點會傳送 DSC 報表至 Azure Automation。</span><span class="sxs-lookup"><span data-stu-id="cdc95-107">A DSC node sends a DSC report to Azure Automation.</span></span>

## <span data-ttu-id="cdc95-108">例子</span><span class="sxs-lookup"><span data-stu-id="cdc95-108">EXAMPLES</span></span>

### <span data-ttu-id="cdc95-109">範例 1：從 DSC 節點匯出報表</span><span class="sxs-lookup"><span data-stu-id="cdc95-109">Example 1: Export a report from a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "AutomationAccount01" -Name "Computer14"
PS C:\> $Report = Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "ContosoAutomationAccount" -NodeId $Node.Id -Latest
PS C:\> $Report | Export-AzAutomationDscNodeReportContent -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="cdc95-110">這組命令會從名為 Computer14 的 DSC 節點匯出最新的報表至桌面。</span><span class="sxs-lookup"><span data-stu-id="cdc95-110">This set of commands exports the latest report from the DSC node named Computer14 to the desktop.</span></span>

## <span data-ttu-id="cdc95-111">參數</span><span class="sxs-lookup"><span data-stu-id="cdc95-111">PARAMETERS</span></span>

### <span data-ttu-id="cdc95-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cdc95-112">-AutomationAccountName</span></span>
<span data-ttu-id="cdc95-113">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdc95-113">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="cdc95-114">此 Cmdlet 會針對屬於此參數指定的自動化帳戶的 DSC 節點匯出報表內容。</span><span class="sxs-lookup"><span data-stu-id="cdc95-114">This cmdlet exports report content for a DSC node that belongs to the Automation account that this parameter specifies.</span></span>

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

### <span data-ttu-id="cdc95-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdc95-115">-DefaultProfile</span></span>
<span data-ttu-id="cdc95-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="cdc95-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cdc95-117">-強制</span><span class="sxs-lookup"><span data-stu-id="cdc95-117">-Force</span></span>
<span data-ttu-id="cdc95-118">表示此 Cmdlet 會以名稱相同的新檔案取代現有的本地檔案。</span><span class="sxs-lookup"><span data-stu-id="cdc95-118">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="cdc95-119">-NodeId</span><span class="sxs-lookup"><span data-stu-id="cdc95-119">-NodeId</span></span>
<span data-ttu-id="cdc95-120">指定此 Cmdlet 匯出報表內容之 DSC 節點的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="cdc95-120">Specifies the unique ID of the DSC node for which this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="cdc95-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="cdc95-121">-OutputFolder</span></span>
<span data-ttu-id="cdc95-122">指定此 Cmdlet 匯出報表內容的輸出檔案夾。</span><span class="sxs-lookup"><span data-stu-id="cdc95-122">Specifies the output folder where this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="cdc95-123">-ReportId</span><span class="sxs-lookup"><span data-stu-id="cdc95-123">-ReportId</span></span>
<span data-ttu-id="cdc95-124">指定此 Cmdlet 匯出之 DSC 節點報表的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="cdc95-124">Specifies the unique ID of the DSC node report that this cmdlet exports.</span></span>

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

### <span data-ttu-id="cdc95-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdc95-125">-ResourceGroupName</span></span>
<span data-ttu-id="cdc95-126">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdc95-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="cdc95-127">此 Cmdlet 會匯出屬於此 Cmdlet 指定之資源群組之 DSC 節點之報表的內容。</span><span class="sxs-lookup"><span data-stu-id="cdc95-127">This cmdlet exports the contents of a report for the DSC node that belongs to the resource group that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="cdc95-128">-確認</span><span class="sxs-lookup"><span data-stu-id="cdc95-128">-Confirm</span></span>
<span data-ttu-id="cdc95-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cdc95-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdc95-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdc95-130">-WhatIf</span></span>
<span data-ttu-id="cdc95-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cdc95-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdc95-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cdc95-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdc95-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdc95-133">CommonParameters</span></span>
<span data-ttu-id="cdc95-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cdc95-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdc95-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="cdc95-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdc95-136">輸入</span><span class="sxs-lookup"><span data-stu-id="cdc95-136">INPUTS</span></span>

### <span data-ttu-id="cdc95-137">System.Guid</span><span class="sxs-lookup"><span data-stu-id="cdc95-137">System.Guid</span></span>

### <span data-ttu-id="cdc95-138">System.String</span><span class="sxs-lookup"><span data-stu-id="cdc95-138">System.String</span></span>

## <span data-ttu-id="cdc95-139">輸出</span><span class="sxs-lookup"><span data-stu-id="cdc95-139">OUTPUTS</span></span>

### <span data-ttu-id="cdc95-140">System.IO.DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="cdc95-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="cdc95-141">筆記</span><span class="sxs-lookup"><span data-stu-id="cdc95-141">NOTES</span></span>

## <span data-ttu-id="cdc95-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="cdc95-142">RELATED LINKS</span></span>

[<span data-ttu-id="cdc95-143">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="cdc95-143">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)

[<span data-ttu-id="cdc95-144">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="cdc95-144">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="cdc95-145">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="cdc95-145">Get-AzAutomationDscNodeReport</span></span>](./Get-AzAutomationDscNodeReport.md)


