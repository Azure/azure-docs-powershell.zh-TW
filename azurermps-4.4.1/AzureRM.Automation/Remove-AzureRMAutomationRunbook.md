---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationRunbook.md
ms.openlocfilehash: 96a82f4cc39952517bf5cfaeca24191cc4dd2d9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450887"
---
# <span data-ttu-id="c33dd-101">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c33dd-101">Remove-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="c33dd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c33dd-102">SYNOPSIS</span></span>
<span data-ttu-id="c33dd-103">移除 runbook。</span><span class="sxs-lookup"><span data-stu-id="c33dd-103">Removes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c33dd-104">句法</span><span class="sxs-lookup"><span data-stu-id="c33dd-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c33dd-105">說明</span><span class="sxs-lookup"><span data-stu-id="c33dd-105">DESCRIPTION</span></span>
<span data-ttu-id="c33dd-106">**AzureRmAutomationRunbook** Cmdlet 會將 Runbook 從 Azure 自動化中移除。</span><span class="sxs-lookup"><span data-stu-id="c33dd-106">The **Remove-AzureRmAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="c33dd-107">示例</span><span class="sxs-lookup"><span data-stu-id="c33dd-107">EXAMPLES</span></span>

### <span data-ttu-id="c33dd-108">範例1：移除 runbook</span><span class="sxs-lookup"><span data-stu-id="c33dd-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c33dd-109">這個命令會從 Azure 自動化帳戶（名為 Contoso17）中移除名為 Runbook03 的 runbook。</span><span class="sxs-lookup"><span data-stu-id="c33dd-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="c33dd-110">參數</span><span class="sxs-lookup"><span data-stu-id="c33dd-110">PARAMETERS</span></span>

### <span data-ttu-id="c33dd-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c33dd-111">-AutomationAccountName</span></span>
<span data-ttu-id="c33dd-112">指定此 Cmdlet 移除 runbook 之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="c33dd-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="c33dd-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c33dd-113">-Force</span></span>
<span data-ttu-id="c33dd-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="c33dd-114">ps_force</span></span>

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

### <span data-ttu-id="c33dd-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="c33dd-115">-Name</span></span>
<span data-ttu-id="c33dd-116">指定此 Cmdlet 移除的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="c33dd-116">Specifies the name of the runbook that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c33dd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c33dd-117">-ResourceGroupName</span></span>
<span data-ttu-id="c33dd-118">指定此 Cmdlet 發佈 runbook 的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c33dd-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="c33dd-119">-確認</span><span class="sxs-lookup"><span data-stu-id="c33dd-119">-Confirm</span></span>
<span data-ttu-id="c33dd-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c33dd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c33dd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c33dd-121">-WhatIf</span></span>
<span data-ttu-id="c33dd-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c33dd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c33dd-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c33dd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c33dd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c33dd-124">-DefaultProfile</span></span>
<span data-ttu-id="c33dd-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c33dd-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c33dd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c33dd-126">CommonParameters</span></span>
<span data-ttu-id="c33dd-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c33dd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c33dd-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c33dd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c33dd-129">輸入</span><span class="sxs-lookup"><span data-stu-id="c33dd-129">INPUTS</span></span>

## <span data-ttu-id="c33dd-130">輸出</span><span class="sxs-lookup"><span data-stu-id="c33dd-130">OUTPUTS</span></span>

## <span data-ttu-id="c33dd-131">筆記</span><span class="sxs-lookup"><span data-stu-id="c33dd-131">NOTES</span></span>

## <span data-ttu-id="c33dd-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="c33dd-132">RELATED LINKS</span></span>

[<span data-ttu-id="c33dd-133">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c33dd-133">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c33dd-134">AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c33dd-134">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c33dd-135">匯入-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c33dd-135">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c33dd-136">新-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c33dd-136">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c33dd-137">新-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c33dd-137">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c33dd-138">發佈-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c33dd-138">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c33dd-139">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c33dd-139">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c33dd-140">開始-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c33dd-140">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


