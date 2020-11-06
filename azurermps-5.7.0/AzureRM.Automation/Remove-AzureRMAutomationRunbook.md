---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationRunbook.md
ms.openlocfilehash: a4f65e20253ef979cba5d3907faeba3fb58e7fe6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456244"
---
# <span data-ttu-id="5f409-101">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5f409-101">Remove-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="5f409-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5f409-102">SYNOPSIS</span></span>
<span data-ttu-id="5f409-103">移除 runbook。</span><span class="sxs-lookup"><span data-stu-id="5f409-103">Removes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f409-104">句法</span><span class="sxs-lookup"><span data-stu-id="5f409-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5f409-105">說明</span><span class="sxs-lookup"><span data-stu-id="5f409-105">DESCRIPTION</span></span>
<span data-ttu-id="5f409-106">**AzureRmAutomationRunbook** Cmdlet 會將 Runbook 從 Azure 自動化中移除。</span><span class="sxs-lookup"><span data-stu-id="5f409-106">The **Remove-AzureRmAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="5f409-107">示例</span><span class="sxs-lookup"><span data-stu-id="5f409-107">EXAMPLES</span></span>

### <span data-ttu-id="5f409-108">範例1：移除 runbook</span><span class="sxs-lookup"><span data-stu-id="5f409-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5f409-109">這個命令會從 Azure 自動化帳戶（名為 Contoso17）中移除名為 Runbook03 的 runbook。</span><span class="sxs-lookup"><span data-stu-id="5f409-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="5f409-110">參數</span><span class="sxs-lookup"><span data-stu-id="5f409-110">PARAMETERS</span></span>

### <span data-ttu-id="5f409-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5f409-111">-AutomationAccountName</span></span>
<span data-ttu-id="5f409-112">指定此 Cmdlet 移除 runbook 之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f409-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="5f409-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f409-113">-DefaultProfile</span></span>
<span data-ttu-id="5f409-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5f409-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f409-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5f409-115">-Force</span></span>
<span data-ttu-id="5f409-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="5f409-116">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f409-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="5f409-117">-Name</span></span>
<span data-ttu-id="5f409-118">指定此 Cmdlet 移除的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="5f409-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f409-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f409-119">-ResourceGroupName</span></span>
<span data-ttu-id="5f409-120">指定此 Cmdlet 發佈 runbook 的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f409-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="5f409-121">-確認</span><span class="sxs-lookup"><span data-stu-id="5f409-121">-Confirm</span></span>
<span data-ttu-id="5f409-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5f409-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f409-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f409-123">-WhatIf</span></span>
<span data-ttu-id="5f409-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5f409-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f409-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5f409-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f409-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f409-126">CommonParameters</span></span>
<span data-ttu-id="5f409-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5f409-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f409-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5f409-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f409-129">輸入</span><span class="sxs-lookup"><span data-stu-id="5f409-129">INPUTS</span></span>

### <span data-ttu-id="5f409-130">所有</span><span class="sxs-lookup"><span data-stu-id="5f409-130">None</span></span>
<span data-ttu-id="5f409-131">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="5f409-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5f409-132">輸出</span><span class="sxs-lookup"><span data-stu-id="5f409-132">OUTPUTS</span></span>

## <span data-ttu-id="5f409-133">筆記</span><span class="sxs-lookup"><span data-stu-id="5f409-133">NOTES</span></span>

## <span data-ttu-id="5f409-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="5f409-134">RELATED LINKS</span></span>

[<span data-ttu-id="5f409-135">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5f409-135">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5f409-136">AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5f409-136">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5f409-137">匯入-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5f409-137">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5f409-138">新-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5f409-138">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5f409-139">新-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5f409-139">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5f409-140">發佈-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5f409-140">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5f409-141">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5f409-141">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5f409-142">開始-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5f409-142">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


