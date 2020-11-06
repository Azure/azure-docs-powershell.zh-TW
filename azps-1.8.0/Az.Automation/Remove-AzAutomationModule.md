---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
ms.openlocfilehash: 798e5f37fdeb53030d43f132eae59c94ea855fc1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622975"
---
# <span data-ttu-id="a31b2-101">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="a31b2-101">Remove-AzAutomationModule</span></span>

## <span data-ttu-id="a31b2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a31b2-102">SYNOPSIS</span></span>
<span data-ttu-id="a31b2-103">從自動化中移除模組。</span><span class="sxs-lookup"><span data-stu-id="a31b2-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="a31b2-104">句法</span><span class="sxs-lookup"><span data-stu-id="a31b2-104">SYNTAX</span></span>

```
Remove-AzAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a31b2-105">說明</span><span class="sxs-lookup"><span data-stu-id="a31b2-105">DESCRIPTION</span></span>
<span data-ttu-id="a31b2-106">**AzAutomationModule** Cmdlet 會從 Azure 自動化的自動化帳戶中移除模組。</span><span class="sxs-lookup"><span data-stu-id="a31b2-106">The **Remove-AzAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="a31b2-107">示例</span><span class="sxs-lookup"><span data-stu-id="a31b2-107">EXAMPLES</span></span>

### <span data-ttu-id="a31b2-108">範例1：移除模組</span><span class="sxs-lookup"><span data-stu-id="a31b2-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a31b2-109">這個命令會從名為 Contoso17 的自動化帳戶中移除名為 ContosoModule 的模組。</span><span class="sxs-lookup"><span data-stu-id="a31b2-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="a31b2-110">參數</span><span class="sxs-lookup"><span data-stu-id="a31b2-110">PARAMETERS</span></span>

### <span data-ttu-id="a31b2-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a31b2-111">-AutomationAccountName</span></span>
<span data-ttu-id="a31b2-112">指定此 Cmdlet 從中移除模組的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a31b2-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="a31b2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a31b2-113">-DefaultProfile</span></span>
<span data-ttu-id="a31b2-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a31b2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a31b2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a31b2-115">-Force</span></span>
<span data-ttu-id="a31b2-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="a31b2-116">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a31b2-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="a31b2-117">-Name</span></span>
<span data-ttu-id="a31b2-118">指定此 Cmdlet 移除的模組名稱。</span><span class="sxs-lookup"><span data-stu-id="a31b2-118">Specifies the name of the module that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a31b2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a31b2-119">-ResourceGroupName</span></span>
<span data-ttu-id="a31b2-120">指定此 Cmdlet 移除模組的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a31b2-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="a31b2-121">-確認</span><span class="sxs-lookup"><span data-stu-id="a31b2-121">-Confirm</span></span>
<span data-ttu-id="a31b2-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a31b2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a31b2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a31b2-123">-WhatIf</span></span>
<span data-ttu-id="a31b2-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a31b2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a31b2-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a31b2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a31b2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a31b2-126">CommonParameters</span></span>
<span data-ttu-id="a31b2-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a31b2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a31b2-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a31b2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a31b2-129">輸入</span><span class="sxs-lookup"><span data-stu-id="a31b2-129">INPUTS</span></span>

### <span data-ttu-id="a31b2-130">System.object</span><span class="sxs-lookup"><span data-stu-id="a31b2-130">System.String</span></span>

## <span data-ttu-id="a31b2-131">輸出</span><span class="sxs-lookup"><span data-stu-id="a31b2-131">OUTPUTS</span></span>

### <span data-ttu-id="a31b2-132">System.void</span><span class="sxs-lookup"><span data-stu-id="a31b2-132">System.Void</span></span>

## <span data-ttu-id="a31b2-133">筆記</span><span class="sxs-lookup"><span data-stu-id="a31b2-133">NOTES</span></span>

## <span data-ttu-id="a31b2-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="a31b2-134">RELATED LINKS</span></span>

[<span data-ttu-id="a31b2-135">AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="a31b2-135">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="a31b2-136">新-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="a31b2-136">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="a31b2-137">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="a31b2-137">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


