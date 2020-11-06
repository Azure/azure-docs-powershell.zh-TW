---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
ms.openlocfilehash: 2ce97441769c15ed122dc7921554b4fa1c5a144f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457472"
---
# <span data-ttu-id="dd6b1-101">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="dd6b1-101">Remove-AzureRmAutomationModule</span></span>

## <span data-ttu-id="dd6b1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dd6b1-102">SYNOPSIS</span></span>
<span data-ttu-id="dd6b1-103">從自動化中移除模組。</span><span class="sxs-lookup"><span data-stu-id="dd6b1-103">Removes a module from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd6b1-104">句法</span><span class="sxs-lookup"><span data-stu-id="dd6b1-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd6b1-105">說明</span><span class="sxs-lookup"><span data-stu-id="dd6b1-105">DESCRIPTION</span></span>
<span data-ttu-id="dd6b1-106">**AzureRmAutomationModule** Cmdlet 會從 Azure 自動化的自動化帳戶中移除模組。</span><span class="sxs-lookup"><span data-stu-id="dd6b1-106">The **Remove-AzureRmAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="dd6b1-107">示例</span><span class="sxs-lookup"><span data-stu-id="dd6b1-107">EXAMPLES</span></span>

### <span data-ttu-id="dd6b1-108">範例1：移除模組</span><span class="sxs-lookup"><span data-stu-id="dd6b1-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="dd6b1-109">這個命令會從名為 Contoso17 的自動化帳戶中移除名為 ContosoModule 的模組。</span><span class="sxs-lookup"><span data-stu-id="dd6b1-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="dd6b1-110">參數</span><span class="sxs-lookup"><span data-stu-id="dd6b1-110">PARAMETERS</span></span>

### <span data-ttu-id="dd6b1-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dd6b1-111">-AutomationAccountName</span></span>
<span data-ttu-id="dd6b1-112">指定此 Cmdlet 從中移除模組的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="dd6b1-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd6b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd6b1-113">-DefaultProfile</span></span>
<span data-ttu-id="dd6b1-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="dd6b1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd6b1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="dd6b1-115">-Force</span></span>
<span data-ttu-id="dd6b1-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="dd6b1-116">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd6b1-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="dd6b1-117">-Name</span></span>
<span data-ttu-id="dd6b1-118">指定此 Cmdlet 移除的模組名稱。</span><span class="sxs-lookup"><span data-stu-id="dd6b1-118">Specifies the name of the module that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd6b1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd6b1-119">-ResourceGroupName</span></span>
<span data-ttu-id="dd6b1-120">指定此 Cmdlet 移除模組的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd6b1-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd6b1-121">-確認</span><span class="sxs-lookup"><span data-stu-id="dd6b1-121">-Confirm</span></span>
<span data-ttu-id="dd6b1-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dd6b1-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd6b1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd6b1-123">-WhatIf</span></span>
<span data-ttu-id="dd6b1-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dd6b1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd6b1-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dd6b1-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd6b1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd6b1-126">CommonParameters</span></span>
<span data-ttu-id="dd6b1-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dd6b1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd6b1-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dd6b1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd6b1-129">輸入</span><span class="sxs-lookup"><span data-stu-id="dd6b1-129">INPUTS</span></span>

### <span data-ttu-id="dd6b1-130">所有</span><span class="sxs-lookup"><span data-stu-id="dd6b1-130">None</span></span>
<span data-ttu-id="dd6b1-131">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="dd6b1-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dd6b1-132">輸出</span><span class="sxs-lookup"><span data-stu-id="dd6b1-132">OUTPUTS</span></span>

## <span data-ttu-id="dd6b1-133">筆記</span><span class="sxs-lookup"><span data-stu-id="dd6b1-133">NOTES</span></span>

## <span data-ttu-id="dd6b1-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd6b1-134">RELATED LINKS</span></span>

[<span data-ttu-id="dd6b1-135">AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="dd6b1-135">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="dd6b1-136">新-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="dd6b1-136">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="dd6b1-137">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="dd6b1-137">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


