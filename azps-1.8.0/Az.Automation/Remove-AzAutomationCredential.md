---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
ms.openlocfilehash: 703be26244e61b797f3359ef508d92e38847bf8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622982"
---
# <span data-ttu-id="cec1a-101">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="cec1a-101">Remove-AzAutomationCredential</span></span>

## <span data-ttu-id="cec1a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cec1a-102">SYNOPSIS</span></span>
<span data-ttu-id="cec1a-103">移除自動化認證。</span><span class="sxs-lookup"><span data-stu-id="cec1a-103">Removes an Automation credential.</span></span>

## <span data-ttu-id="cec1a-104">句法</span><span class="sxs-lookup"><span data-stu-id="cec1a-104">SYNTAX</span></span>

```
Remove-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cec1a-105">說明</span><span class="sxs-lookup"><span data-stu-id="cec1a-105">DESCRIPTION</span></span>
<span data-ttu-id="cec1a-106">**AzAutomationCredential** Cmdlet 會從 Azure 自動化中移除認證。</span><span class="sxs-lookup"><span data-stu-id="cec1a-106">The **Remove-AzAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="cec1a-107">示例</span><span class="sxs-lookup"><span data-stu-id="cec1a-107">EXAMPLES</span></span>

### <span data-ttu-id="cec1a-108">範例1：移除認證</span><span class="sxs-lookup"><span data-stu-id="cec1a-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="cec1a-109">這個命令會在 Azure 自動化帳戶（名為 Contoso17）中移除一個名為 ContosoCredential 的認證。</span><span class="sxs-lookup"><span data-stu-id="cec1a-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="cec1a-110">參數</span><span class="sxs-lookup"><span data-stu-id="cec1a-110">PARAMETERS</span></span>

### <span data-ttu-id="cec1a-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cec1a-111">-AutomationAccountName</span></span>
<span data-ttu-id="cec1a-112">指定此 Cmdlet 移除認證的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="cec1a-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="cec1a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cec1a-113">-DefaultProfile</span></span>
<span data-ttu-id="cec1a-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="cec1a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cec1a-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="cec1a-115">-Name</span></span>
<span data-ttu-id="cec1a-116">指定此 Cmdlet 移除之認證的名稱。</span><span class="sxs-lookup"><span data-stu-id="cec1a-116">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cec1a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cec1a-117">-ResourceGroupName</span></span>
<span data-ttu-id="cec1a-118">指定此 Cmdlet 移除認證之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cec1a-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="cec1a-119">-確認</span><span class="sxs-lookup"><span data-stu-id="cec1a-119">-Confirm</span></span>
<span data-ttu-id="cec1a-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cec1a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cec1a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cec1a-121">-WhatIf</span></span>
<span data-ttu-id="cec1a-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cec1a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cec1a-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cec1a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cec1a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cec1a-124">CommonParameters</span></span>
<span data-ttu-id="cec1a-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cec1a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cec1a-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cec1a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cec1a-127">輸入</span><span class="sxs-lookup"><span data-stu-id="cec1a-127">INPUTS</span></span>

### <span data-ttu-id="cec1a-128">System.object</span><span class="sxs-lookup"><span data-stu-id="cec1a-128">System.String</span></span>

## <span data-ttu-id="cec1a-129">輸出</span><span class="sxs-lookup"><span data-stu-id="cec1a-129">OUTPUTS</span></span>

### <span data-ttu-id="cec1a-130">System.void</span><span class="sxs-lookup"><span data-stu-id="cec1a-130">System.Void</span></span>

## <span data-ttu-id="cec1a-131">筆記</span><span class="sxs-lookup"><span data-stu-id="cec1a-131">NOTES</span></span>

## <span data-ttu-id="cec1a-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="cec1a-132">RELATED LINKS</span></span>

[<span data-ttu-id="cec1a-133">AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="cec1a-133">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="cec1a-134">新-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="cec1a-134">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="cec1a-135">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="cec1a-135">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


