---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/import-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationRunbook.md
ms.openlocfilehash: 9ec19ee8e1e6a74de83f77b8dca4e2536af8e425
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613750"
---
# <span data-ttu-id="f7d17-101">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f7d17-101">Import-AzAutomationRunbook</span></span>

## <span data-ttu-id="f7d17-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f7d17-102">SYNOPSIS</span></span>
<span data-ttu-id="f7d17-103">匯入自動化 runbook。</span><span class="sxs-lookup"><span data-stu-id="f7d17-103">Imports an Automation runbook.</span></span>

## <span data-ttu-id="f7d17-104">句法</span><span class="sxs-lookup"><span data-stu-id="f7d17-104">SYNTAX</span></span>

```
Import-AzAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7d17-105">說明</span><span class="sxs-lookup"><span data-stu-id="f7d17-105">DESCRIPTION</span></span>
<span data-ttu-id="f7d17-106">匯 **入-AzAutomationRunbook** Cmdlet 會匯入 Azure 自動化 runbook。</span><span class="sxs-lookup"><span data-stu-id="f7d17-106">The **Import-AzAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="f7d17-107">指定 wps_2 腳本的路徑 ( ps1) 要匯入 wps_2 和 wps_2 工作流程 runbook、 () 檔案的圖形 runbook，或 (. .py) 檔案。</span><span class="sxs-lookup"><span data-stu-id="f7d17-107">Specify the path to a wps_2 script (.ps1) file to import for wps_2 and wps_2 Workflow runbooks, (.graphrunbook) file for graphical runbooks, or (.py) file for python 2 runbooks.</span></span> <span data-ttu-id="f7d17-108">針對 wps_2 工作流程 runbook，此腳本必須包含與檔案名稱相符的單一 wps_2 工作流程定義。</span><span class="sxs-lookup"><span data-stu-id="f7d17-108">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="f7d17-109">示例</span><span class="sxs-lookup"><span data-stu-id="f7d17-109">EXAMPLES</span></span>

### <span data-ttu-id="f7d17-110">範例1：從檔案匯入 runbook</span><span class="sxs-lookup"><span data-stu-id="f7d17-110">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="f7d17-111">第一個命令會將兩個鍵/值對指派給 $Tags 變數。</span><span class="sxs-lookup"><span data-stu-id="f7d17-111">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="f7d17-112">第二個命令會將一個名為 GraphicalRunbook06 的圖形 runbook 匯入到名為 AutomationAccount01 的自動化帳戶中。</span><span class="sxs-lookup"><span data-stu-id="f7d17-112">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="f7d17-113">該命令也會指派儲存在 $Tags 中的標籤。</span><span class="sxs-lookup"><span data-stu-id="f7d17-113">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="f7d17-114">參數</span><span class="sxs-lookup"><span data-stu-id="f7d17-114">PARAMETERS</span></span>

### <span data-ttu-id="f7d17-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f7d17-115">-AutomationAccountName</span></span>
<span data-ttu-id="f7d17-116">指定此 Cmdlet 要匯入 runbook 之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7d17-116">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="f7d17-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7d17-117">-DefaultProfile</span></span>
<span data-ttu-id="f7d17-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f7d17-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7d17-119">-描述</span><span class="sxs-lookup"><span data-stu-id="f7d17-119">-Description</span></span>
<span data-ttu-id="f7d17-120">指定匯入的 runbook 的描述。</span><span class="sxs-lookup"><span data-stu-id="f7d17-120">Specifies a description for the imported runbook.</span></span>

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

### <span data-ttu-id="f7d17-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f7d17-121">-Force</span></span>
<span data-ttu-id="f7d17-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="f7d17-122">ps_force</span></span>

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

### <span data-ttu-id="f7d17-123">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="f7d17-123">-LogProgress</span></span>
<span data-ttu-id="f7d17-124">指定 runbook 是否要記錄進度資訊。</span><span class="sxs-lookup"><span data-stu-id="f7d17-124">Specifies whether the runbook logs progress information.</span></span>

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

### <span data-ttu-id="f7d17-125">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="f7d17-125">-LogVerbose</span></span>
<span data-ttu-id="f7d17-126">指定 runbook 是否記錄詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f7d17-126">Specifies whether the runbook logs detailed information.</span></span>

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

### <span data-ttu-id="f7d17-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="f7d17-127">-Name</span></span>
<span data-ttu-id="f7d17-128">指定此 Cmdlet 所匯入的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="f7d17-128">Specifies the name of the runbook that this cmdlet imports.</span></span>

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

### <span data-ttu-id="f7d17-129">-Path</span><span class="sxs-lookup"><span data-stu-id="f7d17-129">-Path</span></span>
<span data-ttu-id="f7d17-130">指定此 Cmdlet 所匯入的 ps1 或 graphrunbook 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="f7d17-130">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

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

### <span data-ttu-id="f7d17-131">-已發佈</span><span class="sxs-lookup"><span data-stu-id="f7d17-131">-Published</span></span>
<span data-ttu-id="f7d17-132">表示此 Cmdlet 會發佈它所匯入的 runbook。</span><span class="sxs-lookup"><span data-stu-id="f7d17-132">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

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

### <span data-ttu-id="f7d17-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7d17-133">-ResourceGroupName</span></span>
<span data-ttu-id="f7d17-134">指定此 Cmdlet 要匯入 runbook 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7d17-134">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="f7d17-135">-標記</span><span class="sxs-lookup"><span data-stu-id="f7d17-135">-Tags</span></span>
<span data-ttu-id="f7d17-136">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="f7d17-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f7d17-137">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="f7d17-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f7d17-138">-類型</span><span class="sxs-lookup"><span data-stu-id="f7d17-138">-Type</span></span>
<span data-ttu-id="f7d17-139">指定此 Cmdlet 建立的 runbook 類型。</span><span class="sxs-lookup"><span data-stu-id="f7d17-139">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="f7d17-140">有效值為：</span><span class="sxs-lookup"><span data-stu-id="f7d17-140">Valid values are:</span></span>
- <span data-ttu-id="f7d17-141">PowerShell</span><span class="sxs-lookup"><span data-stu-id="f7d17-141">PowerShell</span></span>
- <span data-ttu-id="f7d17-142">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="f7d17-142">GraphicalPowerShell</span></span>
- <span data-ttu-id="f7d17-143">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="f7d17-143">PowerShellWorkflow</span></span>
- <span data-ttu-id="f7d17-144">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="f7d17-144">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="f7d17-145">]</span><span class="sxs-lookup"><span data-stu-id="f7d17-145">Graph</span></span>
- <span data-ttu-id="f7d17-146">Python2 值 Graph 已過時。</span><span class="sxs-lookup"><span data-stu-id="f7d17-146">Python2 The value Graph is obsolete.</span></span>
<span data-ttu-id="f7d17-147">它相當於 GraphicalPowerShellWorkflow。</span><span class="sxs-lookup"><span data-stu-id="f7d17-147">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

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

### <span data-ttu-id="f7d17-148">-確認</span><span class="sxs-lookup"><span data-stu-id="f7d17-148">-Confirm</span></span>
<span data-ttu-id="f7d17-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f7d17-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7d17-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7d17-150">-WhatIf</span></span>
<span data-ttu-id="f7d17-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f7d17-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7d17-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f7d17-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7d17-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7d17-153">CommonParameters</span></span>
<span data-ttu-id="f7d17-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f7d17-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7d17-155">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f7d17-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7d17-156">輸入</span><span class="sxs-lookup"><span data-stu-id="f7d17-156">INPUTS</span></span>

### <span data-ttu-id="f7d17-157">System.object</span><span class="sxs-lookup"><span data-stu-id="f7d17-157">System.String</span></span>

### <span data-ttu-id="f7d17-158">System.object</span><span class="sxs-lookup"><span data-stu-id="f7d17-158">System.Collections.IDictionary</span></span>

### <span data-ttu-id="f7d17-159">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f7d17-159">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f7d17-160">輸出</span><span class="sxs-lookup"><span data-stu-id="f7d17-160">OUTPUTS</span></span>

### <span data-ttu-id="f7d17-161">[-Azure. 命令介面]。</span><span class="sxs-lookup"><span data-stu-id="f7d17-161">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="f7d17-162">筆記</span><span class="sxs-lookup"><span data-stu-id="f7d17-162">NOTES</span></span>

## <span data-ttu-id="f7d17-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7d17-163">RELATED LINKS</span></span>

[<span data-ttu-id="f7d17-164">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f7d17-164">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="f7d17-165">AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f7d17-165">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="f7d17-166">新-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f7d17-166">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="f7d17-167">發佈-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f7d17-167">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="f7d17-168">移除-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f7d17-168">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="f7d17-169">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f7d17-169">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="f7d17-170">開始-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f7d17-170">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)
