---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
ms.openlocfilehash: 49b4a02210105529dff2aae2b895d4059ced97f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916675"
---
# <span data-ttu-id="8e697-101">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8e697-101">Remove-AzAutomationAccount</span></span>

## <span data-ttu-id="8e697-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8e697-102">SYNOPSIS</span></span>
<span data-ttu-id="8e697-103">移除自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="8e697-103">Removes an Automation account.</span></span>

## <span data-ttu-id="8e697-104">語法</span><span class="sxs-lookup"><span data-stu-id="8e697-104">SYNTAX</span></span>

```
Remove-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e697-105">描述</span><span class="sxs-lookup"><span data-stu-id="8e697-105">DESCRIPTION</span></span>
<span data-ttu-id="8e697-106">**Remove-AzAutomationAccount** Cmdlet 會從資源群組移除 Azure 自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="8e697-106">The **Remove-AzAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>
<span data-ttu-id="8e697-107">有關自動化帳戶的資訊，請參閱 New-AzAutomationAccount Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e697-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="8e697-108">例子</span><span class="sxs-lookup"><span data-stu-id="8e697-108">EXAMPLES</span></span>

### <span data-ttu-id="8e697-109">範例 1：移除自動化帳戶</span><span class="sxs-lookup"><span data-stu-id="8e697-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8e697-110">此命令會移除名為 ContosoAutomationAccount的自動化帳戶，而不會提示使用者驗證。</span><span class="sxs-lookup"><span data-stu-id="8e697-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="8e697-111">參數</span><span class="sxs-lookup"><span data-stu-id="8e697-111">PARAMETERS</span></span>

### <span data-ttu-id="8e697-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e697-112">-DefaultProfile</span></span>
<span data-ttu-id="8e697-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="8e697-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e697-114">-強制</span><span class="sxs-lookup"><span data-stu-id="8e697-114">-Force</span></span>
<span data-ttu-id="8e697-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="8e697-115">ps_force</span></span>

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

### <span data-ttu-id="8e697-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="8e697-116">-Name</span></span>
<span data-ttu-id="8e697-117">指定此 Cmdlet 移除的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="8e697-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8e697-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e697-118">-ResourceGroupName</span></span>
<span data-ttu-id="8e697-119">指定此 Cmdlet 移除自動化帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="8e697-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="8e697-120">-確認</span><span class="sxs-lookup"><span data-stu-id="8e697-120">-Confirm</span></span>
<span data-ttu-id="8e697-121">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8e697-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e697-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e697-122">-WhatIf</span></span>
<span data-ttu-id="8e697-123">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8e697-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e697-124">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e697-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e697-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e697-125">CommonParameters</span></span>
<span data-ttu-id="8e697-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8e697-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e697-127">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="8e697-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e697-128">輸入</span><span class="sxs-lookup"><span data-stu-id="8e697-128">INPUTS</span></span>

### <span data-ttu-id="8e697-129">System.String</span><span class="sxs-lookup"><span data-stu-id="8e697-129">System.String</span></span>

## <span data-ttu-id="8e697-130">輸出</span><span class="sxs-lookup"><span data-stu-id="8e697-130">OUTPUTS</span></span>

### <span data-ttu-id="8e697-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8e697-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="8e697-132">筆記</span><span class="sxs-lookup"><span data-stu-id="8e697-132">NOTES</span></span>

## <span data-ttu-id="8e697-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e697-133">RELATED LINKS</span></span>

[<span data-ttu-id="8e697-134">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8e697-134">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="8e697-135">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8e697-135">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="8e697-136">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8e697-136">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


