---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/import-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationRunbook.md
ms.openlocfilehash: e043496f421ec6602fea61018cbaa254192def10
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93623023"
---
# <span data-ttu-id="b3ee9-101">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b3ee9-101">Import-AzAutomationRunbook</span></span>

## <span data-ttu-id="b3ee9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b3ee9-102">SYNOPSIS</span></span>
<span data-ttu-id="b3ee9-103">匯入自動化 runbook。</span><span class="sxs-lookup"><span data-stu-id="b3ee9-103">Imports an Automation runbook.</span></span>

## <span data-ttu-id="b3ee9-104">句法</span><span class="sxs-lookup"><span data-stu-id="b3ee9-104">SYNTAX</span></span>

```
Import-AzAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3ee9-105">說明</span><span class="sxs-lookup"><span data-stu-id="b3ee9-105">DESCRIPTION</span></span>
<span data-ttu-id="b3ee9-106">匯 **入-AzAutomationRunbook** Cmdlet 會匯入 Azure 自動化 runbook。</span><span class="sxs-lookup"><span data-stu-id="b3ee9-106">The **Import-AzAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="b3ee9-107">指定 wps_2 腳本的路徑 ( ps1) 要匯入 wps_2 和 wps_2 工作流程 runbook、 () 檔案的圖形 runbook，或 (. .py) 檔案。</span><span class="sxs-lookup"><span data-stu-id="b3ee9-107">Specify the path to a wps_2 script (.ps1) file to import for wps_2 and wps_2 Workflow runbooks, (.graphrunbook) file for graphical runbooks, or (.py) file for python 2 runbooks.</span></span> <span data-ttu-id="b3ee9-108">針對 wps_2 工作流程 runbook，此腳本必須包含與檔案名稱相符的單一 wps_2 工作流程定義。</span><span class="sxs-lookup"><span data-stu-id="b3ee9-108">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="b3ee9-109">示例</span><span class="sxs-lookup"><span data-stu-id="b3ee9-109">EXAMPLES</span></span>

### <span data-ttu-id="b3ee9-110">範例1：從檔案匯入 runbook</span><span class="sxs-lookup"><span data-stu-id="b3ee9-110">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="b3ee9-111">第一個命令會將兩個鍵/值對指派給 $Tags 變數。</span><span class="sxs-lookup"><span data-stu-id="b3ee9-111">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="b3ee9-112">第二個命令會將一個名為 GraphicalRunbook06 的圖形 runbook 匯入到名為 AutomationAccount01 的自動化帳戶中。</span><span class="sxs-lookup"><span data-stu-id="b3ee9-112">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="b3ee9-113">該命令也會指派儲存在 $Tags 中的標籤。</span><span class="sxs-lookup"><span data-stu-id="b3ee9-113">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="b3ee9-114">參數</span><span class="sxs-lookup"><span data-stu-id="b3ee9-114">PARAMETERS</span></span>

### <span data-ttu-id="b3ee9-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b3ee9-115">-AutomationAccountName</span></span>
<span data-ttu-id="b3ee9-116">指定此 Cmdlet 要匯入 runbook 之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3ee9-116">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="b3ee9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3ee9-117">-DefaultProfile</span></span>
<span data-ttu-id="b3ee9-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b3ee9-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3ee9-119">-描述</span><span class="sxs-lookup"><span data-stu-id="b3ee9-119">-Description</span></span>
<span data-ttu-id="b3ee9-120">指定匯入的 runbook 的描述。</span><span class="sxs-lookup"><span data-stu-id="b3ee9-120">Specifies a description for the imported runbook.</span></span>

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

### <span data-ttu-id="b3ee9-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b3ee9-121">-Force</span></span>
<span data-ttu-id="b3ee9-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="b3ee9-122">ps_force</span></span>

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

### <span data-ttu-id="b3ee9-123">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="b3ee9-123">-LogProgress</span></span>
<span data-ttu-id="b3ee9-124">指定 runbook 是否要記錄進度資訊。</span><span class="sxs-lookup"><span data-stu-id="b3ee9-124">Specifies whether the runbook logs progress information.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3ee9-125">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="b3ee9-125">-LogVerbose</span></span>
<span data-ttu-id="b3ee9-126">指定 runbook 是否記錄詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="b3ee9-126">Specifies whether the runbook logs detailed information.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3ee9-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="b3ee9-127">-Name</span></span>
<span data-ttu-id="b3ee9-128">指定此 Cmdlet 所匯入的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="b3ee9-128">Specifies the name of the runbook that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3ee9-129">-Path</span><span class="sxs-lookup"><span data-stu-id="b3ee9-129">-Path</span></span>
<span data-ttu-id="b3ee9-130">指定此 Cmdlet 所匯入的 ps1 或 graphrunbook 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="b3ee9-130">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourcePath

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3ee9-131">-已發佈</span><span class="sxs-lookup"><span data-stu-id="b3ee9-131">-Published</span></span>
<span data-ttu-id="b3ee9-132">表示此 Cmdlet 會發佈它所匯入的 runbook。</span><span class="sxs-lookup"><span data-stu-id="b3ee9-132">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

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

### <span data-ttu-id="b3ee9-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3ee9-133">-ResourceGroupName</span></span>
<span data-ttu-id="b3ee9-134">指定此 Cmdlet 要匯入 runbook 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3ee9-134">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="b3ee9-135">-標記</span><span class="sxs-lookup"><span data-stu-id="b3ee9-135">-Tags</span></span>
<span data-ttu-id="b3ee9-136">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="b3ee9-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b3ee9-137">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b3ee9-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3ee9-138">-類型</span><span class="sxs-lookup"><span data-stu-id="b3ee9-138">-Type</span></span>
<span data-ttu-id="b3ee9-139">指定此 Cmdlet 建立的 runbook 類型。</span><span class="sxs-lookup"><span data-stu-id="b3ee9-139">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="b3ee9-140">有效值為：</span><span class="sxs-lookup"><span data-stu-id="b3ee9-140">Valid values are:</span></span>
- <span data-ttu-id="b3ee9-141">PowerShell</span><span class="sxs-lookup"><span data-stu-id="b3ee9-141">PowerShell</span></span>
- <span data-ttu-id="b3ee9-142">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="b3ee9-142">GraphicalPowerShell</span></span>
- <span data-ttu-id="b3ee9-143">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="b3ee9-143">PowerShellWorkflow</span></span>
- <span data-ttu-id="b3ee9-144">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="b3ee9-144">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="b3ee9-145">]</span><span class="sxs-lookup"><span data-stu-id="b3ee9-145">Graph</span></span>
- <span data-ttu-id="b3ee9-146">Python2 值 Graph 已過時。</span><span class="sxs-lookup"><span data-stu-id="b3ee9-146">Python2 The value Graph is obsolete.</span></span>
<span data-ttu-id="b3ee9-147">它相當於 GraphicalPowerShellWorkflow。</span><span class="sxs-lookup"><span data-stu-id="b3ee9-147">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph, Python2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ee9-148">-確認</span><span class="sxs-lookup"><span data-stu-id="b3ee9-148">-Confirm</span></span>
<span data-ttu-id="b3ee9-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b3ee9-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3ee9-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3ee9-150">-WhatIf</span></span>
<span data-ttu-id="b3ee9-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b3ee9-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3ee9-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3ee9-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3ee9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3ee9-153">CommonParameters</span></span>
<span data-ttu-id="b3ee9-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b3ee9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3ee9-155">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b3ee9-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3ee9-156">輸入</span><span class="sxs-lookup"><span data-stu-id="b3ee9-156">INPUTS</span></span>

### <span data-ttu-id="b3ee9-157">System.object</span><span class="sxs-lookup"><span data-stu-id="b3ee9-157">System.String</span></span>

### <span data-ttu-id="b3ee9-158">System.object</span><span class="sxs-lookup"><span data-stu-id="b3ee9-158">System.Collections.IDictionary</span></span>

### <span data-ttu-id="b3ee9-159">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b3ee9-159">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b3ee9-160">輸出</span><span class="sxs-lookup"><span data-stu-id="b3ee9-160">OUTPUTS</span></span>

### <span data-ttu-id="b3ee9-161">[-Azure. 命令介面]。</span><span class="sxs-lookup"><span data-stu-id="b3ee9-161">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="b3ee9-162">筆記</span><span class="sxs-lookup"><span data-stu-id="b3ee9-162">NOTES</span></span>

## <span data-ttu-id="b3ee9-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3ee9-163">RELATED LINKS</span></span>

[<span data-ttu-id="b3ee9-164">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b3ee9-164">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="b3ee9-165">AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b3ee9-165">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="b3ee9-166">新-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b3ee9-166">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="b3ee9-167">新-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b3ee9-167">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="b3ee9-168">發佈-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b3ee9-168">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="b3ee9-169">移除-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b3ee9-169">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="b3ee9-170">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b3ee9-170">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="b3ee9-171">開始-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b3ee9-171">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)
