---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
ms.openlocfilehash: 46dee36dccc4a6e73620732df18059f64ccb6587
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915641"
---
# <span data-ttu-id="d6fa2-101">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="d6fa2-101">Remove-AzAutomationVariable</span></span>

## <span data-ttu-id="d6fa2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d6fa2-102">SYNOPSIS</span></span>
<span data-ttu-id="d6fa2-103">移除自動化變數。</span><span class="sxs-lookup"><span data-stu-id="d6fa2-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="d6fa2-104">語法</span><span class="sxs-lookup"><span data-stu-id="d6fa2-104">SYNTAX</span></span>

```
Remove-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6fa2-105">描述</span><span class="sxs-lookup"><span data-stu-id="d6fa2-105">DESCRIPTION</span></span>
<span data-ttu-id="d6fa2-106">**Remove-AzAutomationVariable** Cmdlet 會從 Azure Automation 移除變數。</span><span class="sxs-lookup"><span data-stu-id="d6fa2-106">The **Remove-AzAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="d6fa2-107">例子</span><span class="sxs-lookup"><span data-stu-id="d6fa2-107">EXAMPLES</span></span>

### <span data-ttu-id="d6fa2-108">範例 1：移除變數</span><span class="sxs-lookup"><span data-stu-id="d6fa2-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d6fa2-109">此命令會移除自動化帳戶中名為 Contoso17 的 StringVariable22 變數。</span><span class="sxs-lookup"><span data-stu-id="d6fa2-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="d6fa2-110">此命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="d6fa2-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="d6fa2-111">因此，它不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d6fa2-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="d6fa2-112">參數</span><span class="sxs-lookup"><span data-stu-id="d6fa2-112">PARAMETERS</span></span>

### <span data-ttu-id="d6fa2-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d6fa2-113">-AutomationAccountName</span></span>
<span data-ttu-id="d6fa2-114">指定包含此 Cmdlet 刪除之變數的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d6fa2-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="d6fa2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6fa2-115">-DefaultProfile</span></span>
<span data-ttu-id="d6fa2-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="d6fa2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6fa2-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="d6fa2-117">-Name</span></span>
<span data-ttu-id="d6fa2-118">指定此 Cmdlet 刪除的變數名稱。</span><span class="sxs-lookup"><span data-stu-id="d6fa2-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="d6fa2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6fa2-119">-ResourceGroupName</span></span>
<span data-ttu-id="d6fa2-120">指定此 Cmdlet 會刪除變數的資源群組。</span><span class="sxs-lookup"><span data-stu-id="d6fa2-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="d6fa2-121">-確認</span><span class="sxs-lookup"><span data-stu-id="d6fa2-121">-Confirm</span></span>
<span data-ttu-id="d6fa2-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d6fa2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6fa2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6fa2-123">-WhatIf</span></span>
<span data-ttu-id="d6fa2-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d6fa2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6fa2-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d6fa2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6fa2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6fa2-126">CommonParameters</span></span>
<span data-ttu-id="d6fa2-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d6fa2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6fa2-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d6fa2-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6fa2-129">輸入</span><span class="sxs-lookup"><span data-stu-id="d6fa2-129">INPUTS</span></span>

### <span data-ttu-id="d6fa2-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d6fa2-130">System.String</span></span>

## <span data-ttu-id="d6fa2-131">輸出</span><span class="sxs-lookup"><span data-stu-id="d6fa2-131">OUTPUTS</span></span>

### <span data-ttu-id="d6fa2-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="d6fa2-132">System.Void</span></span>

## <span data-ttu-id="d6fa2-133">筆記</span><span class="sxs-lookup"><span data-stu-id="d6fa2-133">NOTES</span></span>

## <span data-ttu-id="d6fa2-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="d6fa2-134">RELATED LINKS</span></span>

[<span data-ttu-id="d6fa2-135">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="d6fa2-135">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="d6fa2-136">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="d6fa2-136">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="d6fa2-137">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="d6fa2-137">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


