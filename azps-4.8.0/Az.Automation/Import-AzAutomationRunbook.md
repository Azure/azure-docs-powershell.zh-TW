---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/import-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationRunbook.md
ms.openlocfilehash: 772806c772328ef707352e0fd866b0c423308f43
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969390"
---
# <span data-ttu-id="60609-101">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="60609-101">Import-AzAutomationRunbook</span></span>

## <span data-ttu-id="60609-102">摘要</span><span class="sxs-lookup"><span data-stu-id="60609-102">SYNOPSIS</span></span>
<span data-ttu-id="60609-103">匯入自動化 runbook。</span><span class="sxs-lookup"><span data-stu-id="60609-103">Imports an Automation runbook.</span></span>

## <span data-ttu-id="60609-104">句法</span><span class="sxs-lookup"><span data-stu-id="60609-104">SYNTAX</span></span>

```
Import-AzAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60609-105">說明</span><span class="sxs-lookup"><span data-stu-id="60609-105">DESCRIPTION</span></span>
<span data-ttu-id="60609-106">匯 **入-AzAutomationRunbook** Cmdlet 會匯入 Azure 自動化 runbook。</span><span class="sxs-lookup"><span data-stu-id="60609-106">The **Import-AzAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="60609-107">指定 wps_2 腳本的路徑 ( ps1) 要匯入 wps_2 和 wps_2 工作流程 runbook、 () 檔案的圖形 runbook，或 (. .py) 檔案。</span><span class="sxs-lookup"><span data-stu-id="60609-107">Specify the path to a wps_2 script (.ps1) file to import for wps_2 and wps_2 Workflow runbooks, (.graphrunbook) file for graphical runbooks, or (.py) file for python 2 runbooks.</span></span> <span data-ttu-id="60609-108">針對 wps_2 工作流程 runbook，此腳本必須包含與檔案名稱相符的單一 wps_2 工作流程定義。</span><span class="sxs-lookup"><span data-stu-id="60609-108">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="60609-109">示例</span><span class="sxs-lookup"><span data-stu-id="60609-109">EXAMPLES</span></span>

### <span data-ttu-id="60609-110">範例1：從檔案匯入 runbook</span><span class="sxs-lookup"><span data-stu-id="60609-110">Example 1: Import a runbook from a file</span></span>
```powershell
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="60609-111">第一個命令會將兩個鍵/值對指派給 $Tags 變數。</span><span class="sxs-lookup"><span data-stu-id="60609-111">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="60609-112">第二個命令會將一個名為 GraphicalRunbook06 的圖形 runbook 匯入到名為 AutomationAccount01 的自動化帳戶中。</span><span class="sxs-lookup"><span data-stu-id="60609-112">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="60609-113">該命令也會指派儲存在 $Tags 中的標籤。</span><span class="sxs-lookup"><span data-stu-id="60609-113">The command also assigns the tags stored in $Tags.</span></span>

### <span data-ttu-id="60609-114">範例2</span><span class="sxs-lookup"><span data-stu-id="60609-114">Example 2</span></span>

<span data-ttu-id="60609-115">匯入自動化 runbook。</span><span class="sxs-lookup"><span data-stu-id="60609-115">Imports an Automation runbook.</span></span> <span data-ttu-id="60609-116"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="60609-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Import-AzAutomationRunbook -AutomationAccountName 'AutomationAccount01' -Name 'Configuration01' -Path .\GraphicalRunbook06.graphrunbook -Published -ResourceGroupName 'ResourceGroup01' -Type PowerShell
```

## <span data-ttu-id="60609-117">參數</span><span class="sxs-lookup"><span data-stu-id="60609-117">PARAMETERS</span></span>

### <span data-ttu-id="60609-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="60609-118">-AutomationAccountName</span></span>
<span data-ttu-id="60609-119">指定此 Cmdlet 要匯入 runbook 之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="60609-119">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="60609-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60609-120">-DefaultProfile</span></span>
<span data-ttu-id="60609-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="60609-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60609-122">-描述</span><span class="sxs-lookup"><span data-stu-id="60609-122">-Description</span></span>
<span data-ttu-id="60609-123">指定匯入的 runbook 的描述。</span><span class="sxs-lookup"><span data-stu-id="60609-123">Specifies a description for the imported runbook.</span></span>

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

### <span data-ttu-id="60609-124">-Force</span><span class="sxs-lookup"><span data-stu-id="60609-124">-Force</span></span>
<span data-ttu-id="60609-125">ps_force</span><span class="sxs-lookup"><span data-stu-id="60609-125">ps_force</span></span>

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

### <span data-ttu-id="60609-126">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="60609-126">-LogProgress</span></span>
<span data-ttu-id="60609-127">指定 runbook 是否要記錄進度資訊。</span><span class="sxs-lookup"><span data-stu-id="60609-127">Specifies whether the runbook logs progress information.</span></span>

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

### <span data-ttu-id="60609-128">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="60609-128">-LogVerbose</span></span>
<span data-ttu-id="60609-129">指定 runbook 是否記錄詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="60609-129">Specifies whether the runbook logs detailed information.</span></span>

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

### <span data-ttu-id="60609-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="60609-130">-Name</span></span>
<span data-ttu-id="60609-131">指定此 Cmdlet 所匯入的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="60609-131">Specifies the name of the runbook that this cmdlet imports.</span></span>

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

### <span data-ttu-id="60609-132">-Path</span><span class="sxs-lookup"><span data-stu-id="60609-132">-Path</span></span>
<span data-ttu-id="60609-133">指定此 Cmdlet 所匯入的 ps1 或 graphrunbook 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="60609-133">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

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

### <span data-ttu-id="60609-134">-已發佈</span><span class="sxs-lookup"><span data-stu-id="60609-134">-Published</span></span>
<span data-ttu-id="60609-135">表示此 Cmdlet 會發佈它所匯入的 runbook。</span><span class="sxs-lookup"><span data-stu-id="60609-135">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

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

### <span data-ttu-id="60609-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60609-136">-ResourceGroupName</span></span>
<span data-ttu-id="60609-137">指定此 Cmdlet 要匯入 runbook 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="60609-137">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="60609-138">-標記</span><span class="sxs-lookup"><span data-stu-id="60609-138">-Tags</span></span>
<span data-ttu-id="60609-139">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="60609-139">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="60609-140">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="60609-140">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="60609-141">-類型</span><span class="sxs-lookup"><span data-stu-id="60609-141">-Type</span></span>
<span data-ttu-id="60609-142">指定此 Cmdlet 建立的 runbook 類型。</span><span class="sxs-lookup"><span data-stu-id="60609-142">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="60609-143">有效值為：</span><span class="sxs-lookup"><span data-stu-id="60609-143">Valid values are:</span></span>
- <span data-ttu-id="60609-144">PowerShell</span><span class="sxs-lookup"><span data-stu-id="60609-144">PowerShell</span></span>
- <span data-ttu-id="60609-145">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="60609-145">GraphicalPowerShell</span></span>
- <span data-ttu-id="60609-146">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="60609-146">PowerShellWorkflow</span></span>
- <span data-ttu-id="60609-147">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="60609-147">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="60609-148">]</span><span class="sxs-lookup"><span data-stu-id="60609-148">Graph</span></span>
- <span data-ttu-id="60609-149">Python2 值 Graph 已過時。</span><span class="sxs-lookup"><span data-stu-id="60609-149">Python2 The value Graph is obsolete.</span></span>
<span data-ttu-id="60609-150">它相當於 GraphicalPowerShellWorkflow。</span><span class="sxs-lookup"><span data-stu-id="60609-150">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

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

### <span data-ttu-id="60609-151">-確認</span><span class="sxs-lookup"><span data-stu-id="60609-151">-Confirm</span></span>
<span data-ttu-id="60609-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="60609-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60609-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60609-153">-WhatIf</span></span>
<span data-ttu-id="60609-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="60609-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60609-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="60609-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60609-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60609-156">CommonParameters</span></span>
<span data-ttu-id="60609-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="60609-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60609-158">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="60609-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60609-159">輸入</span><span class="sxs-lookup"><span data-stu-id="60609-159">INPUTS</span></span>

### <span data-ttu-id="60609-160">System.object</span><span class="sxs-lookup"><span data-stu-id="60609-160">System.String</span></span>

### <span data-ttu-id="60609-161">System.object</span><span class="sxs-lookup"><span data-stu-id="60609-161">System.Collections.IDictionary</span></span>

### <span data-ttu-id="60609-162">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="60609-162">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="60609-163">輸出</span><span class="sxs-lookup"><span data-stu-id="60609-163">OUTPUTS</span></span>

### <span data-ttu-id="60609-164">[-Azure. 命令介面]。</span><span class="sxs-lookup"><span data-stu-id="60609-164">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="60609-165">筆記</span><span class="sxs-lookup"><span data-stu-id="60609-165">NOTES</span></span>

## <span data-ttu-id="60609-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="60609-166">RELATED LINKS</span></span>

[<span data-ttu-id="60609-167">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="60609-167">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="60609-168">AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="60609-168">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="60609-169">新-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="60609-169">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="60609-170">發佈-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="60609-170">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="60609-171">移除-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="60609-171">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="60609-172">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="60609-172">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="60609-173">開始-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="60609-173">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)