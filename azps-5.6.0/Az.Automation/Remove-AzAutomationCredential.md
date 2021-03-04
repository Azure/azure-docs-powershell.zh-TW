---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
ms.openlocfilehash: 3fb795f614e6ccd7c4e97470d89c6c8923fa9165
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916669"
---
# <span data-ttu-id="f8df8-101">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="f8df8-101">Remove-AzAutomationCredential</span></span>

## <span data-ttu-id="f8df8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f8df8-102">SYNOPSIS</span></span>
<span data-ttu-id="f8df8-103">移除自動化認證。</span><span class="sxs-lookup"><span data-stu-id="f8df8-103">Removes an Automation credential.</span></span>

## <span data-ttu-id="f8df8-104">語法</span><span class="sxs-lookup"><span data-stu-id="f8df8-104">SYNTAX</span></span>

```
Remove-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8df8-105">描述</span><span class="sxs-lookup"><span data-stu-id="f8df8-105">DESCRIPTION</span></span>
<span data-ttu-id="f8df8-106">**Remove-AzAutomationCredential Cmdlet** 會從 Azure Automation 移除認證。</span><span class="sxs-lookup"><span data-stu-id="f8df8-106">The **Remove-AzAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="f8df8-107">例子</span><span class="sxs-lookup"><span data-stu-id="f8df8-107">EXAMPLES</span></span>

### <span data-ttu-id="f8df8-108">範例 1：移除認證</span><span class="sxs-lookup"><span data-stu-id="f8df8-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f8df8-109">此命令會移除 Azure 自動化帳戶中名為 Contoso17 的認證 ContosoCredential。</span><span class="sxs-lookup"><span data-stu-id="f8df8-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="f8df8-110">參數</span><span class="sxs-lookup"><span data-stu-id="f8df8-110">PARAMETERS</span></span>

### <span data-ttu-id="f8df8-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f8df8-111">-AutomationAccountName</span></span>
<span data-ttu-id="f8df8-112">指定此 Cmdlet 移除認證之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8df8-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="f8df8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8df8-113">-DefaultProfile</span></span>
<span data-ttu-id="f8df8-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="f8df8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8df8-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="f8df8-115">-Name</span></span>
<span data-ttu-id="f8df8-116">指定此 Cmdlet 移除的認證名稱。</span><span class="sxs-lookup"><span data-stu-id="f8df8-116">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f8df8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8df8-117">-ResourceGroupName</span></span>
<span data-ttu-id="f8df8-118">指定此 Cmdlet 會移除認證的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f8df8-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="f8df8-119">-確認</span><span class="sxs-lookup"><span data-stu-id="f8df8-119">-Confirm</span></span>
<span data-ttu-id="f8df8-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f8df8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8df8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8df8-121">-WhatIf</span></span>
<span data-ttu-id="f8df8-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f8df8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8df8-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f8df8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8df8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8df8-124">CommonParameters</span></span>
<span data-ttu-id="f8df8-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f8df8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8df8-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f8df8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8df8-127">輸入</span><span class="sxs-lookup"><span data-stu-id="f8df8-127">INPUTS</span></span>

### <span data-ttu-id="f8df8-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f8df8-128">System.String</span></span>

## <span data-ttu-id="f8df8-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f8df8-129">OUTPUTS</span></span>

### <span data-ttu-id="f8df8-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="f8df8-130">System.Void</span></span>

## <span data-ttu-id="f8df8-131">筆記</span><span class="sxs-lookup"><span data-stu-id="f8df8-131">NOTES</span></span>

## <span data-ttu-id="f8df8-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8df8-132">RELATED LINKS</span></span>

[<span data-ttu-id="f8df8-133">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="f8df8-133">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="f8df8-134">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="f8df8-134">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="f8df8-135">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="f8df8-135">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


