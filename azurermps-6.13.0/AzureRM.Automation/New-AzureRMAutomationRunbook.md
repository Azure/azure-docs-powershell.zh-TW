---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
ms.openlocfilehash: 73945c02c5c5802e169e0868908874374080b344
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450332"
---
# <span data-ttu-id="9dd4f-101">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9dd4f-101">New-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="9dd4f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9dd4f-102">SYNOPSIS</span></span>
<span data-ttu-id="9dd4f-103">建立自動化 runbook。</span><span class="sxs-lookup"><span data-stu-id="9dd4f-103">Creates an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9dd4f-104">句法</span><span class="sxs-lookup"><span data-stu-id="9dd4f-104">SYNTAX</span></span>

```
New-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9dd4f-105">說明</span><span class="sxs-lookup"><span data-stu-id="9dd4f-105">DESCRIPTION</span></span>
<span data-ttu-id="9dd4f-106">**新的-AzureRmAutomationRunbook** Cmdlet 會使用 ap 建立空白的 Azure 自動化 runbook。</span><span class="sxs-lookup"><span data-stu-id="9dd4f-106">The **New-AzureRmAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="9dd4f-107">指定 runbook 的名稱。</span><span class="sxs-lookup"><span data-stu-id="9dd4f-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="9dd4f-108">示例</span><span class="sxs-lookup"><span data-stu-id="9dd4f-108">EXAMPLES</span></span>

### <span data-ttu-id="9dd4f-109">範例1：建立 runbook</span><span class="sxs-lookup"><span data-stu-id="9dd4f-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9dd4f-110">這個命令會在 Azure 自動化帳戶（名為 Contoso17）中建立名為 Runbook02 的 runbook。</span><span class="sxs-lookup"><span data-stu-id="9dd4f-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="9dd4f-111">參數</span><span class="sxs-lookup"><span data-stu-id="9dd4f-111">PARAMETERS</span></span>

### <span data-ttu-id="9dd4f-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9dd4f-112">-AutomationAccountName</span></span>
<span data-ttu-id="9dd4f-113">指定此 Cmdlet 建立 runbook 所用之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="9dd4f-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="9dd4f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dd4f-114">-DefaultProfile</span></span>
<span data-ttu-id="9dd4f-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9dd4f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9dd4f-116">-描述</span><span class="sxs-lookup"><span data-stu-id="9dd4f-116">-Description</span></span>
<span data-ttu-id="9dd4f-117">指定 runbook 的描述。</span><span class="sxs-lookup"><span data-stu-id="9dd4f-117">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="9dd4f-118">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="9dd4f-118">-LogProgress</span></span>
<span data-ttu-id="9dd4f-119">指定 runbook 是否要記錄進度。</span><span class="sxs-lookup"><span data-stu-id="9dd4f-119">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="9dd4f-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="9dd4f-120">-LogVerbose</span></span>
<span data-ttu-id="9dd4f-121">指定記錄是否包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="9dd4f-121">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="9dd4f-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="9dd4f-122">-Name</span></span>
<span data-ttu-id="9dd4f-123">指定 runbook 的名稱。</span><span class="sxs-lookup"><span data-stu-id="9dd4f-123">Specifies a name for the runbook.</span></span>

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

### <span data-ttu-id="9dd4f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dd4f-124">-ResourceGroupName</span></span>
<span data-ttu-id="9dd4f-125">指定此 Cmdlet 建立 runbook 的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9dd4f-125">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="9dd4f-126">-標記</span><span class="sxs-lookup"><span data-stu-id="9dd4f-126">-Tags</span></span>
<span data-ttu-id="9dd4f-127">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="9dd4f-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9dd4f-128">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="9dd4f-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9dd4f-129">-類型</span><span class="sxs-lookup"><span data-stu-id="9dd4f-129">-Type</span></span>
<span data-ttu-id="9dd4f-130">指定此 Cmdlet 建立的 runbook 類型。</span><span class="sxs-lookup"><span data-stu-id="9dd4f-130">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="9dd4f-131">有效值為：</span><span class="sxs-lookup"><span data-stu-id="9dd4f-131">Valid values are:</span></span>
- <span data-ttu-id="9dd4f-132">PowerShell</span><span class="sxs-lookup"><span data-stu-id="9dd4f-132">PowerShell</span></span>
- <span data-ttu-id="9dd4f-133">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="9dd4f-133">GraphicalPowerShell</span></span>
- <span data-ttu-id="9dd4f-134">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="9dd4f-134">PowerShellWorkflow</span></span>
- <span data-ttu-id="9dd4f-135">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="9dd4f-135">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="9dd4f-136">圖形值圖形已過時。</span><span class="sxs-lookup"><span data-stu-id="9dd4f-136">Graph The value Graph is obsolete.</span></span>
<span data-ttu-id="9dd4f-137">它相當於 GraphicalPowerShellWorkflow。</span><span class="sxs-lookup"><span data-stu-id="9dd4f-137">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd4f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dd4f-138">CommonParameters</span></span>
<span data-ttu-id="9dd4f-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9dd4f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dd4f-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9dd4f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dd4f-141">輸入</span><span class="sxs-lookup"><span data-stu-id="9dd4f-141">INPUTS</span></span>

### <span data-ttu-id="9dd4f-142">System.object</span><span class="sxs-lookup"><span data-stu-id="9dd4f-142">System.String</span></span>

### <span data-ttu-id="9dd4f-143">System.object</span><span class="sxs-lookup"><span data-stu-id="9dd4f-143">System.Collections.IDictionary</span></span>

### <span data-ttu-id="9dd4f-144">系統為 Nullable "1 [[System.object，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9dd4f-144">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="9dd4f-145">輸出</span><span class="sxs-lookup"><span data-stu-id="9dd4f-145">OUTPUTS</span></span>

### <span data-ttu-id="9dd4f-146">[-Azure. 命令介面]。</span><span class="sxs-lookup"><span data-stu-id="9dd4f-146">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="9dd4f-147">筆記</span><span class="sxs-lookup"><span data-stu-id="9dd4f-147">NOTES</span></span>

## <span data-ttu-id="9dd4f-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="9dd4f-148">RELATED LINKS</span></span>

[<span data-ttu-id="9dd4f-149">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9dd4f-149">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9dd4f-150">AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9dd4f-150">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9dd4f-151">匯入-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9dd4f-151">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9dd4f-152">發佈-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9dd4f-152">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9dd4f-153">移除-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9dd4f-153">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9dd4f-154">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9dd4f-154">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9dd4f-155">開始-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9dd4f-155">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
