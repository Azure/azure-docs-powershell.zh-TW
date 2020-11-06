---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
ms.openlocfilehash: c77413f27bcde145334221465cbe792a5e1eaa5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613701"
---
# <span data-ttu-id="e5dda-101">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e5dda-101">Remove-AzAutomationRunbook</span></span>

## <span data-ttu-id="e5dda-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5dda-102">SYNOPSIS</span></span>
<span data-ttu-id="e5dda-103">移除 runbook。</span><span class="sxs-lookup"><span data-stu-id="e5dda-103">Removes a runbook.</span></span>

## <span data-ttu-id="e5dda-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5dda-104">SYNTAX</span></span>

```
Remove-AzAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5dda-105">說明</span><span class="sxs-lookup"><span data-stu-id="e5dda-105">DESCRIPTION</span></span>
<span data-ttu-id="e5dda-106">**AzAutomationRunbook** Cmdlet 會將 Runbook 從 Azure 自動化中移除。</span><span class="sxs-lookup"><span data-stu-id="e5dda-106">The **Remove-AzAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="e5dda-107">示例</span><span class="sxs-lookup"><span data-stu-id="e5dda-107">EXAMPLES</span></span>

### <span data-ttu-id="e5dda-108">範例1：移除 runbook</span><span class="sxs-lookup"><span data-stu-id="e5dda-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e5dda-109">這個命令會從 Azure 自動化帳戶（名為 Contoso17）中移除名為 Runbook03 的 runbook。</span><span class="sxs-lookup"><span data-stu-id="e5dda-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="e5dda-110">參數</span><span class="sxs-lookup"><span data-stu-id="e5dda-110">PARAMETERS</span></span>

### <span data-ttu-id="e5dda-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e5dda-111">-AutomationAccountName</span></span>
<span data-ttu-id="e5dda-112">指定此 Cmdlet 移除 runbook 之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5dda-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="e5dda-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5dda-113">-DefaultProfile</span></span>
<span data-ttu-id="e5dda-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e5dda-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5dda-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e5dda-115">-Force</span></span>
<span data-ttu-id="e5dda-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="e5dda-116">ps_force</span></span>

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

### <span data-ttu-id="e5dda-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="e5dda-117">-Name</span></span>
<span data-ttu-id="e5dda-118">指定此 Cmdlet 移除的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="e5dda-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e5dda-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5dda-119">-ResourceGroupName</span></span>
<span data-ttu-id="e5dda-120">指定此 Cmdlet 發佈 runbook 的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5dda-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="e5dda-121">-確認</span><span class="sxs-lookup"><span data-stu-id="e5dda-121">-Confirm</span></span>
<span data-ttu-id="e5dda-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e5dda-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5dda-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5dda-123">-WhatIf</span></span>
<span data-ttu-id="e5dda-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e5dda-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5dda-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5dda-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5dda-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5dda-126">CommonParameters</span></span>
<span data-ttu-id="e5dda-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5dda-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5dda-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e5dda-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5dda-129">輸入</span><span class="sxs-lookup"><span data-stu-id="e5dda-129">INPUTS</span></span>

### <span data-ttu-id="e5dda-130">System.object</span><span class="sxs-lookup"><span data-stu-id="e5dda-130">System.String</span></span>

## <span data-ttu-id="e5dda-131">輸出</span><span class="sxs-lookup"><span data-stu-id="e5dda-131">OUTPUTS</span></span>

### <span data-ttu-id="e5dda-132">System.void</span><span class="sxs-lookup"><span data-stu-id="e5dda-132">System.Void</span></span>

## <span data-ttu-id="e5dda-133">筆記</span><span class="sxs-lookup"><span data-stu-id="e5dda-133">NOTES</span></span>

## <span data-ttu-id="e5dda-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5dda-134">RELATED LINKS</span></span>

[<span data-ttu-id="e5dda-135">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e5dda-135">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="e5dda-136">AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e5dda-136">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="e5dda-137">匯入-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e5dda-137">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="e5dda-138">新-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e5dda-138">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="e5dda-139">新-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e5dda-139">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="e5dda-140">發佈-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e5dda-140">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="e5dda-141">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e5dda-141">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="e5dda-142">開始-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e5dda-142">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


