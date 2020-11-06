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
ms.locfileid: "93613702"
---
# <span data-ttu-id="3b4fa-101">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="3b4fa-101">Remove-AzAutomationModule</span></span>

## <span data-ttu-id="3b4fa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3b4fa-102">SYNOPSIS</span></span>
<span data-ttu-id="3b4fa-103">從自動化中移除模組。</span><span class="sxs-lookup"><span data-stu-id="3b4fa-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="3b4fa-104">句法</span><span class="sxs-lookup"><span data-stu-id="3b4fa-104">SYNTAX</span></span>

```
Remove-AzAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3b4fa-105">說明</span><span class="sxs-lookup"><span data-stu-id="3b4fa-105">DESCRIPTION</span></span>
<span data-ttu-id="3b4fa-106">**AzAutomationModule** Cmdlet 會從 Azure 自動化的自動化帳戶中移除模組。</span><span class="sxs-lookup"><span data-stu-id="3b4fa-106">The **Remove-AzAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="3b4fa-107">示例</span><span class="sxs-lookup"><span data-stu-id="3b4fa-107">EXAMPLES</span></span>

### <span data-ttu-id="3b4fa-108">範例1：移除模組</span><span class="sxs-lookup"><span data-stu-id="3b4fa-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3b4fa-109">這個命令會從名為 Contoso17 的自動化帳戶中移除名為 ContosoModule 的模組。</span><span class="sxs-lookup"><span data-stu-id="3b4fa-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="3b4fa-110">參數</span><span class="sxs-lookup"><span data-stu-id="3b4fa-110">PARAMETERS</span></span>

### <span data-ttu-id="3b4fa-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3b4fa-111">-AutomationAccountName</span></span>
<span data-ttu-id="3b4fa-112">指定此 Cmdlet 從中移除模組的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="3b4fa-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="3b4fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b4fa-113">-DefaultProfile</span></span>
<span data-ttu-id="3b4fa-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3b4fa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b4fa-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3b4fa-115">-Force</span></span>
<span data-ttu-id="3b4fa-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="3b4fa-116">ps_force</span></span>

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

### <span data-ttu-id="3b4fa-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="3b4fa-117">-Name</span></span>
<span data-ttu-id="3b4fa-118">指定此 Cmdlet 移除的模組名稱。</span><span class="sxs-lookup"><span data-stu-id="3b4fa-118">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3b4fa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b4fa-119">-ResourceGroupName</span></span>
<span data-ttu-id="3b4fa-120">指定此 Cmdlet 移除模組的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b4fa-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="3b4fa-121">-確認</span><span class="sxs-lookup"><span data-stu-id="3b4fa-121">-Confirm</span></span>
<span data-ttu-id="3b4fa-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3b4fa-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b4fa-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b4fa-123">-WhatIf</span></span>
<span data-ttu-id="3b4fa-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3b4fa-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b4fa-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3b4fa-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b4fa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b4fa-126">CommonParameters</span></span>
<span data-ttu-id="3b4fa-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3b4fa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b4fa-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3b4fa-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b4fa-129">輸入</span><span class="sxs-lookup"><span data-stu-id="3b4fa-129">INPUTS</span></span>

### <span data-ttu-id="3b4fa-130">System.object</span><span class="sxs-lookup"><span data-stu-id="3b4fa-130">System.String</span></span>

## <span data-ttu-id="3b4fa-131">輸出</span><span class="sxs-lookup"><span data-stu-id="3b4fa-131">OUTPUTS</span></span>

### <span data-ttu-id="3b4fa-132">System.void</span><span class="sxs-lookup"><span data-stu-id="3b4fa-132">System.Void</span></span>

## <span data-ttu-id="3b4fa-133">筆記</span><span class="sxs-lookup"><span data-stu-id="3b4fa-133">NOTES</span></span>

## <span data-ttu-id="3b4fa-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b4fa-134">RELATED LINKS</span></span>

[<span data-ttu-id="3b4fa-135">AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="3b4fa-135">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="3b4fa-136">新-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="3b4fa-136">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="3b4fa-137">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="3b4fa-137">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


