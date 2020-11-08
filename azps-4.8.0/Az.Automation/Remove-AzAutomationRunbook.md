---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
ms.openlocfilehash: d6ce3a737063763d77ed408072d275c52ee5884c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969364"
---
# <span data-ttu-id="04934-101">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="04934-101">Remove-AzAutomationRunbook</span></span>

## <span data-ttu-id="04934-102">摘要</span><span class="sxs-lookup"><span data-stu-id="04934-102">SYNOPSIS</span></span>
<span data-ttu-id="04934-103">移除 runbook。</span><span class="sxs-lookup"><span data-stu-id="04934-103">Removes a runbook.</span></span>

## <span data-ttu-id="04934-104">句法</span><span class="sxs-lookup"><span data-stu-id="04934-104">SYNTAX</span></span>

```
Remove-AzAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="04934-105">說明</span><span class="sxs-lookup"><span data-stu-id="04934-105">DESCRIPTION</span></span>
<span data-ttu-id="04934-106">**AzAutomationRunbook** Cmdlet 會將 Runbook 從 Azure 自動化中移除。</span><span class="sxs-lookup"><span data-stu-id="04934-106">The **Remove-AzAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="04934-107">示例</span><span class="sxs-lookup"><span data-stu-id="04934-107">EXAMPLES</span></span>

### <span data-ttu-id="04934-108">範例1：移除 runbook</span><span class="sxs-lookup"><span data-stu-id="04934-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="04934-109">這個命令會從 Azure 自動化帳戶（名為 Contoso17）中移除名為 Runbook03 的 runbook。</span><span class="sxs-lookup"><span data-stu-id="04934-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="04934-110">參數</span><span class="sxs-lookup"><span data-stu-id="04934-110">PARAMETERS</span></span>

### <span data-ttu-id="04934-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="04934-111">-AutomationAccountName</span></span>
<span data-ttu-id="04934-112">指定此 Cmdlet 移除 runbook 之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="04934-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="04934-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04934-113">-DefaultProfile</span></span>
<span data-ttu-id="04934-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="04934-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04934-115">-Force</span><span class="sxs-lookup"><span data-stu-id="04934-115">-Force</span></span>
<span data-ttu-id="04934-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="04934-116">ps_force</span></span>

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

### <span data-ttu-id="04934-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="04934-117">-Name</span></span>
<span data-ttu-id="04934-118">指定此 Cmdlet 移除的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="04934-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="04934-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04934-119">-ResourceGroupName</span></span>
<span data-ttu-id="04934-120">指定此 Cmdlet 發佈 runbook 的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="04934-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="04934-121">-確認</span><span class="sxs-lookup"><span data-stu-id="04934-121">-Confirm</span></span>
<span data-ttu-id="04934-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="04934-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04934-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04934-123">-WhatIf</span></span>
<span data-ttu-id="04934-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="04934-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04934-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="04934-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04934-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04934-126">CommonParameters</span></span>
<span data-ttu-id="04934-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="04934-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04934-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="04934-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04934-129">輸入</span><span class="sxs-lookup"><span data-stu-id="04934-129">INPUTS</span></span>

### <span data-ttu-id="04934-130">System.object</span><span class="sxs-lookup"><span data-stu-id="04934-130">System.String</span></span>

## <span data-ttu-id="04934-131">輸出</span><span class="sxs-lookup"><span data-stu-id="04934-131">OUTPUTS</span></span>

### <span data-ttu-id="04934-132">System.void</span><span class="sxs-lookup"><span data-stu-id="04934-132">System.Void</span></span>

## <span data-ttu-id="04934-133">筆記</span><span class="sxs-lookup"><span data-stu-id="04934-133">NOTES</span></span>

## <span data-ttu-id="04934-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="04934-134">RELATED LINKS</span></span>

[<span data-ttu-id="04934-135">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="04934-135">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="04934-136">AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="04934-136">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="04934-137">匯入-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="04934-137">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="04934-138">新-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="04934-138">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="04934-139">新-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="04934-139">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="04934-140">發佈-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="04934-140">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="04934-141">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="04934-141">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="04934-142">開始-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="04934-142">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)

