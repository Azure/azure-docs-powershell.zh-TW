---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
ms.openlocfilehash: 77c089e4ab46972892a7fe9ad3cc519dc7f20551
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625636"
---
# <span data-ttu-id="a687c-101">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a687c-101">New-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="a687c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a687c-102">SYNOPSIS</span></span>
<span data-ttu-id="a687c-103">建立自動化 runbook。</span><span class="sxs-lookup"><span data-stu-id="a687c-103">Creates an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a687c-104">句法</span><span class="sxs-lookup"><span data-stu-id="a687c-104">SYNTAX</span></span>

```
New-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a687c-105">說明</span><span class="sxs-lookup"><span data-stu-id="a687c-105">DESCRIPTION</span></span>
<span data-ttu-id="a687c-106">**新的-AzureRmAutomationRunbook** Cmdlet 會使用 ap 建立空白的 Azure 自動化 runbook。</span><span class="sxs-lookup"><span data-stu-id="a687c-106">The **New-AzureRmAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="a687c-107">指定 runbook 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a687c-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="a687c-108">示例</span><span class="sxs-lookup"><span data-stu-id="a687c-108">EXAMPLES</span></span>

### <span data-ttu-id="a687c-109">範例1：建立 runbook</span><span class="sxs-lookup"><span data-stu-id="a687c-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a687c-110">這個命令會在 Azure 自動化帳戶（名為 Contoso17）中建立名為 Runbook02 的 runbook。</span><span class="sxs-lookup"><span data-stu-id="a687c-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="a687c-111">參數</span><span class="sxs-lookup"><span data-stu-id="a687c-111">PARAMETERS</span></span>

### <span data-ttu-id="a687c-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a687c-112">-AutomationAccountName</span></span>
<span data-ttu-id="a687c-113">指定此 Cmdlet 建立 runbook 所用之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="a687c-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="a687c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a687c-114">-DefaultProfile</span></span>
<span data-ttu-id="a687c-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a687c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a687c-116">-描述</span><span class="sxs-lookup"><span data-stu-id="a687c-116">-Description</span></span>
<span data-ttu-id="a687c-117">指定 runbook 的描述。</span><span class="sxs-lookup"><span data-stu-id="a687c-117">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="a687c-118">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="a687c-118">-LogProgress</span></span>
<span data-ttu-id="a687c-119">指定 runbook 是否要記錄進度。</span><span class="sxs-lookup"><span data-stu-id="a687c-119">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="a687c-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="a687c-120">-LogVerbose</span></span>
<span data-ttu-id="a687c-121">指定記錄是否包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="a687c-121">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="a687c-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="a687c-122">-Name</span></span>
<span data-ttu-id="a687c-123">指定 runbook 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a687c-123">Specifies a name for the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a687c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a687c-124">-ResourceGroupName</span></span>
<span data-ttu-id="a687c-125">指定此 Cmdlet 建立 runbook 的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a687c-125">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="a687c-126">-標記</span><span class="sxs-lookup"><span data-stu-id="a687c-126">-Tags</span></span>
<span data-ttu-id="a687c-127">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="a687c-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a687c-128">例如：</span><span class="sxs-lookup"><span data-stu-id="a687c-128">For example:</span></span>

<span data-ttu-id="a687c-129">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="a687c-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a687c-130">-類型</span><span class="sxs-lookup"><span data-stu-id="a687c-130">-Type</span></span>
<span data-ttu-id="a687c-131">指定此 Cmdlet 建立的 runbook 類型。</span><span class="sxs-lookup"><span data-stu-id="a687c-131">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="a687c-132">有效值為：</span><span class="sxs-lookup"><span data-stu-id="a687c-132">Valid values are:</span></span>

- <span data-ttu-id="a687c-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="a687c-133">PowerShell</span></span>
- <span data-ttu-id="a687c-134">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="a687c-134">GraphicalPowerShell</span></span>
- <span data-ttu-id="a687c-135">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="a687c-135">PowerShellWorkflow</span></span>
- <span data-ttu-id="a687c-136">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="a687c-136">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="a687c-137">]</span><span class="sxs-lookup"><span data-stu-id="a687c-137">Graph</span></span>

<span data-ttu-id="a687c-138">值圖形已過時。</span><span class="sxs-lookup"><span data-stu-id="a687c-138">The value Graph is obsolete.</span></span>
<span data-ttu-id="a687c-139">它相當於 GraphicalPowerShellWorkflow。</span><span class="sxs-lookup"><span data-stu-id="a687c-139">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a687c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a687c-140">CommonParameters</span></span>
<span data-ttu-id="a687c-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a687c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a687c-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a687c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a687c-143">輸入</span><span class="sxs-lookup"><span data-stu-id="a687c-143">INPUTS</span></span>

### <span data-ttu-id="a687c-144">所有</span><span class="sxs-lookup"><span data-stu-id="a687c-144">None</span></span>
<span data-ttu-id="a687c-145">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="a687c-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a687c-146">輸出</span><span class="sxs-lookup"><span data-stu-id="a687c-146">OUTPUTS</span></span>

### <span data-ttu-id="a687c-147">[作為] 的 [自動化] 工作</span><span class="sxs-lookup"><span data-stu-id="a687c-147">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="a687c-148">筆記</span><span class="sxs-lookup"><span data-stu-id="a687c-148">NOTES</span></span>

## <span data-ttu-id="a687c-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="a687c-149">RELATED LINKS</span></span>

[<span data-ttu-id="a687c-150">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a687c-150">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="a687c-151">AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a687c-151">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="a687c-152">匯入-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a687c-152">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="a687c-153">發佈-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a687c-153">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="a687c-154">移除-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a687c-154">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="a687c-155">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a687c-155">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="a687c-156">開始-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a687c-156">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
