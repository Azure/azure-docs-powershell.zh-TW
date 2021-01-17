---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
ms.openlocfilehash: 8d7e63ed8bc24f772afa84106592ede5f9da9250
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447175"
---
# <span data-ttu-id="90967-101">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="90967-101">Remove-AzAutomationModule</span></span>

## <span data-ttu-id="90967-102">摘要</span><span class="sxs-lookup"><span data-stu-id="90967-102">SYNOPSIS</span></span>
<span data-ttu-id="90967-103">從自動化中移除模組。</span><span class="sxs-lookup"><span data-stu-id="90967-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="90967-104">句法</span><span class="sxs-lookup"><span data-stu-id="90967-104">SYNTAX</span></span>

```
Remove-AzAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="90967-105">說明</span><span class="sxs-lookup"><span data-stu-id="90967-105">DESCRIPTION</span></span>
<span data-ttu-id="90967-106">**AzAutomationModule** Cmdlet 會從 Azure 自動化的自動化帳戶中移除模組。</span><span class="sxs-lookup"><span data-stu-id="90967-106">The **Remove-AzAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="90967-107">示例</span><span class="sxs-lookup"><span data-stu-id="90967-107">EXAMPLES</span></span>

### <span data-ttu-id="90967-108">範例1：移除模組</span><span class="sxs-lookup"><span data-stu-id="90967-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="90967-109">這個命令會從名為 Contoso17 的自動化帳戶中移除名為 ContosoModule 的模組。</span><span class="sxs-lookup"><span data-stu-id="90967-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="90967-110">參數</span><span class="sxs-lookup"><span data-stu-id="90967-110">PARAMETERS</span></span>

### <span data-ttu-id="90967-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="90967-111">-AutomationAccountName</span></span>
<span data-ttu-id="90967-112">指定此 Cmdlet 從中移除模組的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="90967-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="90967-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90967-113">-DefaultProfile</span></span>
<span data-ttu-id="90967-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="90967-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90967-115">-Force</span><span class="sxs-lookup"><span data-stu-id="90967-115">-Force</span></span>
<span data-ttu-id="90967-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="90967-116">ps_force</span></span>

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

### <span data-ttu-id="90967-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="90967-117">-Name</span></span>
<span data-ttu-id="90967-118">指定此 Cmdlet 移除的模組名稱。</span><span class="sxs-lookup"><span data-stu-id="90967-118">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="90967-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90967-119">-ResourceGroupName</span></span>
<span data-ttu-id="90967-120">指定此 Cmdlet 移除模組的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="90967-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="90967-121">-確認</span><span class="sxs-lookup"><span data-stu-id="90967-121">-Confirm</span></span>
<span data-ttu-id="90967-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="90967-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90967-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90967-123">-WhatIf</span></span>
<span data-ttu-id="90967-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="90967-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90967-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90967-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90967-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90967-126">CommonParameters</span></span>
<span data-ttu-id="90967-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="90967-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90967-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="90967-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90967-129">輸入</span><span class="sxs-lookup"><span data-stu-id="90967-129">INPUTS</span></span>

### <span data-ttu-id="90967-130">System.object</span><span class="sxs-lookup"><span data-stu-id="90967-130">System.String</span></span>

## <span data-ttu-id="90967-131">輸出</span><span class="sxs-lookup"><span data-stu-id="90967-131">OUTPUTS</span></span>

### <span data-ttu-id="90967-132">System.void</span><span class="sxs-lookup"><span data-stu-id="90967-132">System.Void</span></span>

## <span data-ttu-id="90967-133">筆記</span><span class="sxs-lookup"><span data-stu-id="90967-133">NOTES</span></span>

## <span data-ttu-id="90967-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="90967-134">RELATED LINKS</span></span>

[<span data-ttu-id="90967-135">AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="90967-135">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="90967-136">新-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="90967-136">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="90967-137">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="90967-137">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


