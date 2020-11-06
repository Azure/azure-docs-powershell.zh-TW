---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
ms.openlocfilehash: cfb8aa96da85cbfe1e9c16277c5c1c3539e04ac3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613688"
---
# <span data-ttu-id="81c3f-101">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="81c3f-101">Remove-AzAutomationVariable</span></span>

## <span data-ttu-id="81c3f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81c3f-102">SYNOPSIS</span></span>
<span data-ttu-id="81c3f-103">移除自動化變數。</span><span class="sxs-lookup"><span data-stu-id="81c3f-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="81c3f-104">句法</span><span class="sxs-lookup"><span data-stu-id="81c3f-104">SYNTAX</span></span>

```
Remove-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81c3f-105">說明</span><span class="sxs-lookup"><span data-stu-id="81c3f-105">DESCRIPTION</span></span>
<span data-ttu-id="81c3f-106">**AzAutomationVariable** Cmdlet 會從 Azure 自動化中移除變數。</span><span class="sxs-lookup"><span data-stu-id="81c3f-106">The **Remove-AzAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="81c3f-107">示例</span><span class="sxs-lookup"><span data-stu-id="81c3f-107">EXAMPLES</span></span>

### <span data-ttu-id="81c3f-108">範例1：移除變數</span><span class="sxs-lookup"><span data-stu-id="81c3f-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="81c3f-109">這個命令會在名為 Contoso17 的自動化帳戶中移除一個名為 StringVariable22 的變數。</span><span class="sxs-lookup"><span data-stu-id="81c3f-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="81c3f-110">這個命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="81c3f-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="81c3f-111">因此，它不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="81c3f-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="81c3f-112">參數</span><span class="sxs-lookup"><span data-stu-id="81c3f-112">PARAMETERS</span></span>

### <span data-ttu-id="81c3f-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="81c3f-113">-AutomationAccountName</span></span>
<span data-ttu-id="81c3f-114">指定包含此 Cmdlet 所刪除變數的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="81c3f-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="81c3f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81c3f-115">-DefaultProfile</span></span>
<span data-ttu-id="81c3f-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="81c3f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81c3f-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="81c3f-117">-Name</span></span>
<span data-ttu-id="81c3f-118">指定此 Cmdlet 刪除的變數名稱。</span><span class="sxs-lookup"><span data-stu-id="81c3f-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="81c3f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81c3f-119">-ResourceGroupName</span></span>
<span data-ttu-id="81c3f-120">指定此 Cmdlet 刪除其變數的資源群組。</span><span class="sxs-lookup"><span data-stu-id="81c3f-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="81c3f-121">-確認</span><span class="sxs-lookup"><span data-stu-id="81c3f-121">-Confirm</span></span>
<span data-ttu-id="81c3f-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="81c3f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81c3f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81c3f-123">-WhatIf</span></span>
<span data-ttu-id="81c3f-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="81c3f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81c3f-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81c3f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81c3f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81c3f-126">CommonParameters</span></span>
<span data-ttu-id="81c3f-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81c3f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81c3f-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="81c3f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81c3f-129">輸入</span><span class="sxs-lookup"><span data-stu-id="81c3f-129">INPUTS</span></span>

### <span data-ttu-id="81c3f-130">System.object</span><span class="sxs-lookup"><span data-stu-id="81c3f-130">System.String</span></span>

## <span data-ttu-id="81c3f-131">輸出</span><span class="sxs-lookup"><span data-stu-id="81c3f-131">OUTPUTS</span></span>

### <span data-ttu-id="81c3f-132">System.void</span><span class="sxs-lookup"><span data-stu-id="81c3f-132">System.Void</span></span>

## <span data-ttu-id="81c3f-133">筆記</span><span class="sxs-lookup"><span data-stu-id="81c3f-133">NOTES</span></span>

## <span data-ttu-id="81c3f-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="81c3f-134">RELATED LINKS</span></span>

[<span data-ttu-id="81c3f-135">AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="81c3f-135">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="81c3f-136">新-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="81c3f-136">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="81c3f-137">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="81c3f-137">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


