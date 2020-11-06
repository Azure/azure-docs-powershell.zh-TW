---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
ms.openlocfilehash: 1f7c50f0f5b11c80fce203b0c44128e380834bdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444791"
---
# <span data-ttu-id="adc22-101">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="adc22-101">Import-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="adc22-102">摘要</span><span class="sxs-lookup"><span data-stu-id="adc22-102">SYNOPSIS</span></span>
<span data-ttu-id="adc22-103">匯入自動化 runbook。</span><span class="sxs-lookup"><span data-stu-id="adc22-103">Imports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="adc22-104">句法</span><span class="sxs-lookup"><span data-stu-id="adc22-104">SYNTAX</span></span>

```
Import-AzureRmAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adc22-105">說明</span><span class="sxs-lookup"><span data-stu-id="adc22-105">DESCRIPTION</span></span>
<span data-ttu-id="adc22-106">匯 **入-AzureRmAutomationRunbook** Cmdlet 會匯入 Azure 自動化 runbook。</span><span class="sxs-lookup"><span data-stu-id="adc22-106">The **Import-AzureRmAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="adc22-107">指定 wps_2 腳本的路徑 ( ps1) 要匯入 wps_2 和 wps_2 工作流程 runbook、 () 檔案的圖形 runbook，或 (. .py) 檔案。</span><span class="sxs-lookup"><span data-stu-id="adc22-107">Specify the path to a wps_2 script (.ps1) file to import for wps_2 and wps_2 Workflow runbooks, (.graphrunbook) file for graphical runbooks, or (.py) file for python 2 runbooks.</span></span> <span data-ttu-id="adc22-108">針對 wps_2 工作流程 runbook，此腳本必須包含與檔案名稱相符的單一 wps_2 工作流程定義。</span><span class="sxs-lookup"><span data-stu-id="adc22-108">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="adc22-109">示例</span><span class="sxs-lookup"><span data-stu-id="adc22-109">EXAMPLES</span></span>

### <span data-ttu-id="adc22-110">範例1：從檔案匯入 runbook</span><span class="sxs-lookup"><span data-stu-id="adc22-110">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzureRmAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="adc22-111">第一個命令會將兩個鍵/值對指派給 $Tags 變數。</span><span class="sxs-lookup"><span data-stu-id="adc22-111">The first command assigns two key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="adc22-112">第二個命令會將一個名為 GraphicalRunbook06 的圖形 runbook 匯入到名為 AutomationAccount01 的自動化帳戶中。</span><span class="sxs-lookup"><span data-stu-id="adc22-112">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="adc22-113">該命令也會指派儲存在 $Tags 中的標籤。</span><span class="sxs-lookup"><span data-stu-id="adc22-113">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="adc22-114">參數</span><span class="sxs-lookup"><span data-stu-id="adc22-114">PARAMETERS</span></span>

### <span data-ttu-id="adc22-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="adc22-115">-AutomationAccountName</span></span>
<span data-ttu-id="adc22-116">指定此 Cmdlet 要匯入 runbook 之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="adc22-116">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adc22-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adc22-117">-DefaultProfile</span></span>
<span data-ttu-id="adc22-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="adc22-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adc22-119">-描述</span><span class="sxs-lookup"><span data-stu-id="adc22-119">-Description</span></span>
<span data-ttu-id="adc22-120">指定匯入的 runbook 的描述。</span><span class="sxs-lookup"><span data-stu-id="adc22-120">Specifies a description for the imported runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adc22-121">-Force</span><span class="sxs-lookup"><span data-stu-id="adc22-121">-Force</span></span>
<span data-ttu-id="adc22-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="adc22-122">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adc22-123">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="adc22-123">-LogProgress</span></span>
<span data-ttu-id="adc22-124">指定 runbook 是否要記錄進度資訊。</span><span class="sxs-lookup"><span data-stu-id="adc22-124">Specifies whether the runbook logs progress information.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adc22-125">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="adc22-125">-LogVerbose</span></span>
<span data-ttu-id="adc22-126">指定 runbook 是否記錄詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="adc22-126">Specifies whether the runbook logs detailed information.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adc22-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="adc22-127">-Name</span></span>
<span data-ttu-id="adc22-128">指定此 Cmdlet 所匯入的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="adc22-128">Specifies the name of the runbook that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adc22-129">-Path</span><span class="sxs-lookup"><span data-stu-id="adc22-129">-Path</span></span>
<span data-ttu-id="adc22-130">指定此 Cmdlet 所匯入的 ps1 或 graphrunbook 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="adc22-130">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourcePath

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adc22-131">-已發佈</span><span class="sxs-lookup"><span data-stu-id="adc22-131">-Published</span></span>
<span data-ttu-id="adc22-132">表示此 Cmdlet 會發佈它所匯入的 runbook。</span><span class="sxs-lookup"><span data-stu-id="adc22-132">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adc22-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adc22-133">-ResourceGroupName</span></span>
<span data-ttu-id="adc22-134">指定此 Cmdlet 要匯入 runbook 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="adc22-134">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adc22-135">-標記</span><span class="sxs-lookup"><span data-stu-id="adc22-135">-Tags</span></span>
<span data-ttu-id="adc22-136">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="adc22-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="adc22-137">例如：</span><span class="sxs-lookup"><span data-stu-id="adc22-137">For example:</span></span>

<span data-ttu-id="adc22-138">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="adc22-138">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adc22-139">-類型</span><span class="sxs-lookup"><span data-stu-id="adc22-139">-Type</span></span>
<span data-ttu-id="adc22-140">指定此 Cmdlet 建立的 runbook 類型。</span><span class="sxs-lookup"><span data-stu-id="adc22-140">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="adc22-141">有效值為：</span><span class="sxs-lookup"><span data-stu-id="adc22-141">Valid values are:</span></span>

- <span data-ttu-id="adc22-142">PowerShell</span><span class="sxs-lookup"><span data-stu-id="adc22-142">PowerShell</span></span>
- <span data-ttu-id="adc22-143">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="adc22-143">GraphicalPowerShell</span></span>
- <span data-ttu-id="adc22-144">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="adc22-144">PowerShellWorkflow</span></span>
- <span data-ttu-id="adc22-145">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="adc22-145">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="adc22-146">]</span><span class="sxs-lookup"><span data-stu-id="adc22-146">Graph</span></span>
- <span data-ttu-id="adc22-147">Python2</span><span class="sxs-lookup"><span data-stu-id="adc22-147">Python2</span></span>

<span data-ttu-id="adc22-148">值圖形已過時。</span><span class="sxs-lookup"><span data-stu-id="adc22-148">The value Graph is obsolete.</span></span>
<span data-ttu-id="adc22-149">它相當於 GraphicalPowerShellWorkflow。</span><span class="sxs-lookup"><span data-stu-id="adc22-149">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph, Python

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adc22-150">-確認</span><span class="sxs-lookup"><span data-stu-id="adc22-150">-Confirm</span></span>
<span data-ttu-id="adc22-151">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="adc22-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adc22-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adc22-152">-WhatIf</span></span>
<span data-ttu-id="adc22-153">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="adc22-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adc22-154">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="adc22-154">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adc22-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adc22-155">CommonParameters</span></span>
<span data-ttu-id="adc22-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="adc22-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adc22-157">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="adc22-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adc22-158">輸入</span><span class="sxs-lookup"><span data-stu-id="adc22-158">INPUTS</span></span>

### <span data-ttu-id="adc22-159">所有</span><span class="sxs-lookup"><span data-stu-id="adc22-159">None</span></span>
<span data-ttu-id="adc22-160">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="adc22-160">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="adc22-161">輸出</span><span class="sxs-lookup"><span data-stu-id="adc22-161">OUTPUTS</span></span>

### <span data-ttu-id="adc22-162">[-Azure. 命令介面]。</span><span class="sxs-lookup"><span data-stu-id="adc22-162">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="adc22-163">筆記</span><span class="sxs-lookup"><span data-stu-id="adc22-163">NOTES</span></span>

## <span data-ttu-id="adc22-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="adc22-164">RELATED LINKS</span></span>

[<span data-ttu-id="adc22-165">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="adc22-165">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="adc22-166">AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="adc22-166">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="adc22-167">新-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="adc22-167">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="adc22-168">新-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="adc22-168">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="adc22-169">發佈-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="adc22-169">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="adc22-170">移除-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="adc22-170">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="adc22-171">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="adc22-171">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="adc22-172">開始-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="adc22-172">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
