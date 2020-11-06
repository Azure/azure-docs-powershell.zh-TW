---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
ms.openlocfilehash: 2d3a8d2b247da8f1a2149fd15372858a3b2b3775
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447496"
---
# <span data-ttu-id="02aae-101">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="02aae-101">Remove-AzureRmAutomationModule</span></span>

## <span data-ttu-id="02aae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="02aae-102">SYNOPSIS</span></span>
<span data-ttu-id="02aae-103">從自動化中移除模組。</span><span class="sxs-lookup"><span data-stu-id="02aae-103">Removes a module from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02aae-104">句法</span><span class="sxs-lookup"><span data-stu-id="02aae-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02aae-105">說明</span><span class="sxs-lookup"><span data-stu-id="02aae-105">DESCRIPTION</span></span>
<span data-ttu-id="02aae-106">**AzureRmAutomationModule** Cmdlet 會從 Azure 自動化的自動化帳戶中移除模組。</span><span class="sxs-lookup"><span data-stu-id="02aae-106">The **Remove-AzureRmAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="02aae-107">示例</span><span class="sxs-lookup"><span data-stu-id="02aae-107">EXAMPLES</span></span>

### <span data-ttu-id="02aae-108">範例1：移除模組</span><span class="sxs-lookup"><span data-stu-id="02aae-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="02aae-109">這個命令會從名為 Contoso17 的自動化帳戶中移除名為 ContosoModule 的模組。</span><span class="sxs-lookup"><span data-stu-id="02aae-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="02aae-110">參數</span><span class="sxs-lookup"><span data-stu-id="02aae-110">PARAMETERS</span></span>

### <span data-ttu-id="02aae-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="02aae-111">-AutomationAccountName</span></span>
<span data-ttu-id="02aae-112">指定此 Cmdlet 從中移除模組的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="02aae-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="02aae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02aae-113">-DefaultProfile</span></span>
<span data-ttu-id="02aae-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="02aae-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02aae-115">-Force</span><span class="sxs-lookup"><span data-stu-id="02aae-115">-Force</span></span>
<span data-ttu-id="02aae-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="02aae-116">ps_force</span></span>

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

### <span data-ttu-id="02aae-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="02aae-117">-Name</span></span>
<span data-ttu-id="02aae-118">指定此 Cmdlet 移除的模組名稱。</span><span class="sxs-lookup"><span data-stu-id="02aae-118">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="02aae-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02aae-119">-ResourceGroupName</span></span>
<span data-ttu-id="02aae-120">指定此 Cmdlet 移除模組的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="02aae-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="02aae-121">-確認</span><span class="sxs-lookup"><span data-stu-id="02aae-121">-Confirm</span></span>
<span data-ttu-id="02aae-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="02aae-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02aae-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02aae-123">-WhatIf</span></span>
<span data-ttu-id="02aae-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="02aae-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02aae-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02aae-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02aae-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02aae-126">CommonParameters</span></span>
<span data-ttu-id="02aae-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="02aae-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02aae-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="02aae-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02aae-129">輸入</span><span class="sxs-lookup"><span data-stu-id="02aae-129">INPUTS</span></span>

### <span data-ttu-id="02aae-130">System.object</span><span class="sxs-lookup"><span data-stu-id="02aae-130">System.String</span></span>

## <span data-ttu-id="02aae-131">輸出</span><span class="sxs-lookup"><span data-stu-id="02aae-131">OUTPUTS</span></span>

### <span data-ttu-id="02aae-132">System.void</span><span class="sxs-lookup"><span data-stu-id="02aae-132">System.Void</span></span>

## <span data-ttu-id="02aae-133">筆記</span><span class="sxs-lookup"><span data-stu-id="02aae-133">NOTES</span></span>

## <span data-ttu-id="02aae-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="02aae-134">RELATED LINKS</span></span>

[<span data-ttu-id="02aae-135">AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="02aae-135">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="02aae-136">新-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="02aae-136">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="02aae-137">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="02aae-137">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


