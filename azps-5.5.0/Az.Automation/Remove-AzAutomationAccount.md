---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
ms.openlocfilehash: d3f76fe1e1c482c8d2913266e9c40dc5b41c62f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141619"
---
# <span data-ttu-id="016db-101">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="016db-101">Remove-AzAutomationAccount</span></span>

## <span data-ttu-id="016db-102">摘要</span><span class="sxs-lookup"><span data-stu-id="016db-102">SYNOPSIS</span></span>
<span data-ttu-id="016db-103">移除自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="016db-103">Removes an Automation account.</span></span>

## <span data-ttu-id="016db-104">句法</span><span class="sxs-lookup"><span data-stu-id="016db-104">SYNTAX</span></span>

```
Remove-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="016db-105">說明</span><span class="sxs-lookup"><span data-stu-id="016db-105">DESCRIPTION</span></span>
<span data-ttu-id="016db-106">**AzAutomationAccount** Cmdlet 會從資源群組中移除 Azure 自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="016db-106">The **Remove-AzAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>
<span data-ttu-id="016db-107">如需自動化帳戶的詳細資訊，請參閱 New-AzAutomationAccount Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="016db-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="016db-108">示例</span><span class="sxs-lookup"><span data-stu-id="016db-108">EXAMPLES</span></span>

### <span data-ttu-id="016db-109">範例1：移除自動化帳戶</span><span class="sxs-lookup"><span data-stu-id="016db-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="016db-110">這個命令會移除一個名為 ContosoAutomationAccount 的自動化帳戶，但不會提示使用者驗證。</span><span class="sxs-lookup"><span data-stu-id="016db-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="016db-111">參數</span><span class="sxs-lookup"><span data-stu-id="016db-111">PARAMETERS</span></span>

### <span data-ttu-id="016db-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="016db-112">-DefaultProfile</span></span>
<span data-ttu-id="016db-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="016db-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="016db-114">-Force</span><span class="sxs-lookup"><span data-stu-id="016db-114">-Force</span></span>
<span data-ttu-id="016db-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="016db-115">ps_force</span></span>

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

### <span data-ttu-id="016db-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="016db-116">-Name</span></span>
<span data-ttu-id="016db-117">指定此 Cmdlet 移除之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="016db-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="016db-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="016db-118">-ResourceGroupName</span></span>
<span data-ttu-id="016db-119">指定此 Cmdlet 從中移除自動化帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="016db-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="016db-120">-確認</span><span class="sxs-lookup"><span data-stu-id="016db-120">-Confirm</span></span>
<span data-ttu-id="016db-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="016db-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="016db-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="016db-122">-WhatIf</span></span>
<span data-ttu-id="016db-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="016db-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="016db-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="016db-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="016db-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="016db-125">CommonParameters</span></span>
<span data-ttu-id="016db-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="016db-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="016db-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="016db-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="016db-128">輸入</span><span class="sxs-lookup"><span data-stu-id="016db-128">INPUTS</span></span>

### <span data-ttu-id="016db-129">System.object</span><span class="sxs-lookup"><span data-stu-id="016db-129">System.String</span></span>

## <span data-ttu-id="016db-130">輸出</span><span class="sxs-lookup"><span data-stu-id="016db-130">OUTPUTS</span></span>

### <span data-ttu-id="016db-131">AutomationAccount 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="016db-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="016db-132">筆記</span><span class="sxs-lookup"><span data-stu-id="016db-132">NOTES</span></span>

## <span data-ttu-id="016db-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="016db-133">RELATED LINKS</span></span>

[<span data-ttu-id="016db-134">AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="016db-134">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="016db-135">新-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="016db-135">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="016db-136">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="016db-136">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


