---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
ms.openlocfilehash: a7dc06e4ddbeac224daf9b8a80be40d343514a18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916662"
---
# <span data-ttu-id="c63e7-101">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c63e7-101">Remove-AzAutomationRunbook</span></span>

## <span data-ttu-id="c63e7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c63e7-102">SYNOPSIS</span></span>
<span data-ttu-id="c63e7-103">移除執行簿。</span><span class="sxs-lookup"><span data-stu-id="c63e7-103">Removes a runbook.</span></span>

## <span data-ttu-id="c63e7-104">語法</span><span class="sxs-lookup"><span data-stu-id="c63e7-104">SYNTAX</span></span>

```
Remove-AzAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c63e7-105">描述</span><span class="sxs-lookup"><span data-stu-id="c63e7-105">DESCRIPTION</span></span>
<span data-ttu-id="c63e7-106">**Remove-AzAutomationRunbook** Cmdlet 會從 Azure Automation 移除 runbook。</span><span class="sxs-lookup"><span data-stu-id="c63e7-106">The **Remove-AzAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="c63e7-107">例子</span><span class="sxs-lookup"><span data-stu-id="c63e7-107">EXAMPLES</span></span>

### <span data-ttu-id="c63e7-108">範例 1：移除 runbook</span><span class="sxs-lookup"><span data-stu-id="c63e7-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c63e7-109">此命令會移除 Azure Automation 帳戶中名為 Contoso17 的 Runbook03。</span><span class="sxs-lookup"><span data-stu-id="c63e7-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="c63e7-110">參數</span><span class="sxs-lookup"><span data-stu-id="c63e7-110">PARAMETERS</span></span>

### <span data-ttu-id="c63e7-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c63e7-111">-AutomationAccountName</span></span>
<span data-ttu-id="c63e7-112">指定此 Cmdlet 移除 runbook 的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="c63e7-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="c63e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c63e7-113">-DefaultProfile</span></span>
<span data-ttu-id="c63e7-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="c63e7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c63e7-115">-強制</span><span class="sxs-lookup"><span data-stu-id="c63e7-115">-Force</span></span>
<span data-ttu-id="c63e7-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="c63e7-116">ps_force</span></span>

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

### <span data-ttu-id="c63e7-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="c63e7-117">-Name</span></span>
<span data-ttu-id="c63e7-118">指定此 Cmdlet 移除的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="c63e7-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c63e7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c63e7-119">-ResourceGroupName</span></span>
<span data-ttu-id="c63e7-120">指定此 Cmdlet 發佈 Runbook 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="c63e7-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="c63e7-121">-確認</span><span class="sxs-lookup"><span data-stu-id="c63e7-121">-Confirm</span></span>
<span data-ttu-id="c63e7-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c63e7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c63e7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c63e7-123">-WhatIf</span></span>
<span data-ttu-id="c63e7-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c63e7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c63e7-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c63e7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c63e7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c63e7-126">CommonParameters</span></span>
<span data-ttu-id="c63e7-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c63e7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c63e7-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c63e7-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c63e7-129">輸入</span><span class="sxs-lookup"><span data-stu-id="c63e7-129">INPUTS</span></span>

### <span data-ttu-id="c63e7-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c63e7-130">System.String</span></span>

## <span data-ttu-id="c63e7-131">輸出</span><span class="sxs-lookup"><span data-stu-id="c63e7-131">OUTPUTS</span></span>

### <span data-ttu-id="c63e7-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="c63e7-132">System.Void</span></span>

## <span data-ttu-id="c63e7-133">筆記</span><span class="sxs-lookup"><span data-stu-id="c63e7-133">NOTES</span></span>

## <span data-ttu-id="c63e7-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="c63e7-134">RELATED LINKS</span></span>

[<span data-ttu-id="c63e7-135">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c63e7-135">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="c63e7-136">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c63e7-136">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="c63e7-137">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c63e7-137">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="c63e7-138">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c63e7-138">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="c63e7-139">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c63e7-139">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="c63e7-140">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c63e7-140">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="c63e7-141">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c63e7-141">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="c63e7-142">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c63e7-142">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


