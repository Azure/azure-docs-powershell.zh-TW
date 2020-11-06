---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationRunbook.md
ms.openlocfilehash: bbf86c6744e064b2958acaf5fe7928d537548805
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93623010"
---
# <span data-ttu-id="36a47-101">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="36a47-101">New-AzAutomationRunbook</span></span>

## <span data-ttu-id="36a47-102">摘要</span><span class="sxs-lookup"><span data-stu-id="36a47-102">SYNOPSIS</span></span>
<span data-ttu-id="36a47-103">建立自動化 runbook。</span><span class="sxs-lookup"><span data-stu-id="36a47-103">Creates an Automation runbook.</span></span>

## <span data-ttu-id="36a47-104">句法</span><span class="sxs-lookup"><span data-stu-id="36a47-104">SYNTAX</span></span>

```
New-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36a47-105">說明</span><span class="sxs-lookup"><span data-stu-id="36a47-105">DESCRIPTION</span></span>
<span data-ttu-id="36a47-106">**新的-AzAutomationRunbook** Cmdlet 會使用 ap 建立空白的 Azure 自動化 runbook。</span><span class="sxs-lookup"><span data-stu-id="36a47-106">The **New-AzAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="36a47-107">指定 runbook 的名稱。</span><span class="sxs-lookup"><span data-stu-id="36a47-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="36a47-108">示例</span><span class="sxs-lookup"><span data-stu-id="36a47-108">EXAMPLES</span></span>

### <span data-ttu-id="36a47-109">範例1：建立 runbook</span><span class="sxs-lookup"><span data-stu-id="36a47-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="36a47-110">這個命令會在 Azure 自動化帳戶（名為 Contoso17）中建立名為 Runbook02 的 runbook。</span><span class="sxs-lookup"><span data-stu-id="36a47-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="36a47-111">參數</span><span class="sxs-lookup"><span data-stu-id="36a47-111">PARAMETERS</span></span>

### <span data-ttu-id="36a47-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="36a47-112">-AutomationAccountName</span></span>
<span data-ttu-id="36a47-113">指定此 Cmdlet 建立 runbook 所用之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="36a47-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="36a47-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36a47-114">-DefaultProfile</span></span>
<span data-ttu-id="36a47-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="36a47-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36a47-116">-描述</span><span class="sxs-lookup"><span data-stu-id="36a47-116">-Description</span></span>
<span data-ttu-id="36a47-117">指定 runbook 的描述。</span><span class="sxs-lookup"><span data-stu-id="36a47-117">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="36a47-118">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="36a47-118">-LogProgress</span></span>
<span data-ttu-id="36a47-119">指定 runbook 是否要記錄進度。</span><span class="sxs-lookup"><span data-stu-id="36a47-119">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="36a47-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="36a47-120">-LogVerbose</span></span>
<span data-ttu-id="36a47-121">指定記錄是否包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="36a47-121">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="36a47-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="36a47-122">-Name</span></span>
<span data-ttu-id="36a47-123">指定 runbook 的名稱。</span><span class="sxs-lookup"><span data-stu-id="36a47-123">Specifies a name for the runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36a47-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36a47-124">-ResourceGroupName</span></span>
<span data-ttu-id="36a47-125">指定此 Cmdlet 建立 runbook 的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="36a47-125">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="36a47-126">-標記</span><span class="sxs-lookup"><span data-stu-id="36a47-126">-Tags</span></span>
<span data-ttu-id="36a47-127">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="36a47-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="36a47-128">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="36a47-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="36a47-129">-類型</span><span class="sxs-lookup"><span data-stu-id="36a47-129">-Type</span></span>
<span data-ttu-id="36a47-130">指定此 Cmdlet 建立的 runbook 類型。</span><span class="sxs-lookup"><span data-stu-id="36a47-130">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="36a47-131">有效值為：</span><span class="sxs-lookup"><span data-stu-id="36a47-131">Valid values are:</span></span>
- <span data-ttu-id="36a47-132">PowerShell</span><span class="sxs-lookup"><span data-stu-id="36a47-132">PowerShell</span></span>
- <span data-ttu-id="36a47-133">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="36a47-133">GraphicalPowerShell</span></span>
- <span data-ttu-id="36a47-134">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="36a47-134">PowerShellWorkflow</span></span>
- <span data-ttu-id="36a47-135">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="36a47-135">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="36a47-136">]</span><span class="sxs-lookup"><span data-stu-id="36a47-136">Graph</span></span>
- <span data-ttu-id="36a47-137">Python2 值 Graph 已過時。</span><span class="sxs-lookup"><span data-stu-id="36a47-137">Python2 The value Graph is obsolete.</span></span>
<span data-ttu-id="36a47-138">它相當於 GraphicalPowerShellWorkflow。</span><span class="sxs-lookup"><span data-stu-id="36a47-138">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

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

### <span data-ttu-id="36a47-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36a47-139">CommonParameters</span></span>
<span data-ttu-id="36a47-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="36a47-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36a47-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="36a47-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36a47-142">輸入</span><span class="sxs-lookup"><span data-stu-id="36a47-142">INPUTS</span></span>

### <span data-ttu-id="36a47-143">System.object</span><span class="sxs-lookup"><span data-stu-id="36a47-143">System.String</span></span>

### <span data-ttu-id="36a47-144">System.object</span><span class="sxs-lookup"><span data-stu-id="36a47-144">System.Collections.IDictionary</span></span>

### <span data-ttu-id="36a47-145">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="36a47-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="36a47-146">輸出</span><span class="sxs-lookup"><span data-stu-id="36a47-146">OUTPUTS</span></span>

### <span data-ttu-id="36a47-147">[-Azure. 命令介面]。</span><span class="sxs-lookup"><span data-stu-id="36a47-147">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="36a47-148">筆記</span><span class="sxs-lookup"><span data-stu-id="36a47-148">NOTES</span></span>

## <span data-ttu-id="36a47-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="36a47-149">RELATED LINKS</span></span>

[<span data-ttu-id="36a47-150">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="36a47-150">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="36a47-151">AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="36a47-151">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="36a47-152">匯入-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="36a47-152">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="36a47-153">發佈-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="36a47-153">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="36a47-154">移除-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="36a47-154">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="36a47-155">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="36a47-155">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="36a47-156">開始-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="36a47-156">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)
