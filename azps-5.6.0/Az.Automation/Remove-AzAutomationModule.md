---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
ms.openlocfilehash: 9fa84ffed6352dfb566ad02aa2393a7cba7f393b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916663"
---
# <span data-ttu-id="0bab1-101">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="0bab1-101">Remove-AzAutomationModule</span></span>

## <span data-ttu-id="0bab1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0bab1-102">SYNOPSIS</span></span>
<span data-ttu-id="0bab1-103">從自動化移除模組。</span><span class="sxs-lookup"><span data-stu-id="0bab1-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="0bab1-104">語法</span><span class="sxs-lookup"><span data-stu-id="0bab1-104">SYNTAX</span></span>

```
Remove-AzAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0bab1-105">描述</span><span class="sxs-lookup"><span data-stu-id="0bab1-105">DESCRIPTION</span></span>
<span data-ttu-id="0bab1-106">**Remove-AzAutomationModule Cmdlet** 會從 Azure Automation 中的自動化帳戶移除模組。</span><span class="sxs-lookup"><span data-stu-id="0bab1-106">The **Remove-AzAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="0bab1-107">例子</span><span class="sxs-lookup"><span data-stu-id="0bab1-107">EXAMPLES</span></span>

### <span data-ttu-id="0bab1-108">範例 1：移除模組</span><span class="sxs-lookup"><span data-stu-id="0bab1-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0bab1-109">此命令會從名為 Contoso17 的自動化帳戶移除名為 ContosoModule 的模組。</span><span class="sxs-lookup"><span data-stu-id="0bab1-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="0bab1-110">參數</span><span class="sxs-lookup"><span data-stu-id="0bab1-110">PARAMETERS</span></span>

### <span data-ttu-id="0bab1-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0bab1-111">-AutomationAccountName</span></span>
<span data-ttu-id="0bab1-112">指定此 Cmdlet 移除模組的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="0bab1-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="0bab1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bab1-113">-DefaultProfile</span></span>
<span data-ttu-id="0bab1-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="0bab1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0bab1-115">-強制</span><span class="sxs-lookup"><span data-stu-id="0bab1-115">-Force</span></span>
<span data-ttu-id="0bab1-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="0bab1-116">ps_force</span></span>

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

### <span data-ttu-id="0bab1-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="0bab1-117">-Name</span></span>
<span data-ttu-id="0bab1-118">指定此 Cmdlet 移除的模組名稱。</span><span class="sxs-lookup"><span data-stu-id="0bab1-118">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0bab1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bab1-119">-ResourceGroupName</span></span>
<span data-ttu-id="0bab1-120">指定此 Cmdlet 移除模組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="0bab1-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="0bab1-121">-確認</span><span class="sxs-lookup"><span data-stu-id="0bab1-121">-Confirm</span></span>
<span data-ttu-id="0bab1-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0bab1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bab1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bab1-123">-WhatIf</span></span>
<span data-ttu-id="0bab1-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0bab1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bab1-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0bab1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bab1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bab1-126">CommonParameters</span></span>
<span data-ttu-id="0bab1-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0bab1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bab1-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0bab1-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bab1-129">輸入</span><span class="sxs-lookup"><span data-stu-id="0bab1-129">INPUTS</span></span>

### <span data-ttu-id="0bab1-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0bab1-130">System.String</span></span>

## <span data-ttu-id="0bab1-131">輸出</span><span class="sxs-lookup"><span data-stu-id="0bab1-131">OUTPUTS</span></span>

### <span data-ttu-id="0bab1-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="0bab1-132">System.Void</span></span>

## <span data-ttu-id="0bab1-133">筆記</span><span class="sxs-lookup"><span data-stu-id="0bab1-133">NOTES</span></span>

## <span data-ttu-id="0bab1-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="0bab1-134">RELATED LINKS</span></span>

[<span data-ttu-id="0bab1-135">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="0bab1-135">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="0bab1-136">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="0bab1-136">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="0bab1-137">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="0bab1-137">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


