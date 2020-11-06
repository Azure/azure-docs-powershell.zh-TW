---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/publish-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
ms.openlocfilehash: e3d60cf277402ac23764b538ba6492ef5c424219
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450322"
---
# <span data-ttu-id="7bd8e-101">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7bd8e-101">Publish-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="7bd8e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7bd8e-102">SYNOPSIS</span></span>
<span data-ttu-id="7bd8e-103">發佈 runbook。</span><span class="sxs-lookup"><span data-stu-id="7bd8e-103">Publishes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bd8e-104">句法</span><span class="sxs-lookup"><span data-stu-id="7bd8e-104">SYNTAX</span></span>

```
Publish-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bd8e-105">說明</span><span class="sxs-lookup"><span data-stu-id="7bd8e-105">DESCRIPTION</span></span>
<span data-ttu-id="7bd8e-106">**AzureRmAutomationRunbook** Cmdlet 發佈 runbook，以用於 Azure 自動化的生產環境。</span><span class="sxs-lookup"><span data-stu-id="7bd8e-106">The **Publish-AzureRmAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="7bd8e-107">示例</span><span class="sxs-lookup"><span data-stu-id="7bd8e-107">EXAMPLES</span></span>

### <span data-ttu-id="7bd8e-108">範例1：發佈 runbook</span><span class="sxs-lookup"><span data-stu-id="7bd8e-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7bd8e-109">這個命令會在名為 Contoso17 的 Azure 自動化帳戶中發佈名為 Runbk01 的 runbook。</span><span class="sxs-lookup"><span data-stu-id="7bd8e-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="7bd8e-110">參數</span><span class="sxs-lookup"><span data-stu-id="7bd8e-110">PARAMETERS</span></span>

### <span data-ttu-id="7bd8e-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7bd8e-111">-AutomationAccountName</span></span>
<span data-ttu-id="7bd8e-112">指定此 Cmdlet 發佈 runbook 的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="7bd8e-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="7bd8e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bd8e-113">-DefaultProfile</span></span>
<span data-ttu-id="7bd8e-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="7bd8e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7bd8e-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="7bd8e-115">-Name</span></span>
<span data-ttu-id="7bd8e-116">指定此 Cmdlet 發佈的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="7bd8e-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="7bd8e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bd8e-117">-ResourceGroupName</span></span>
<span data-ttu-id="7bd8e-118">指定此 Cmdlet 發佈 runbook 的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7bd8e-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="7bd8e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bd8e-119">CommonParameters</span></span>
<span data-ttu-id="7bd8e-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7bd8e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bd8e-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7bd8e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bd8e-122">輸入</span><span class="sxs-lookup"><span data-stu-id="7bd8e-122">INPUTS</span></span>

### <span data-ttu-id="7bd8e-123">System.object</span><span class="sxs-lookup"><span data-stu-id="7bd8e-123">System.String</span></span>

## <span data-ttu-id="7bd8e-124">輸出</span><span class="sxs-lookup"><span data-stu-id="7bd8e-124">OUTPUTS</span></span>

### <span data-ttu-id="7bd8e-125">[-Azure. 命令介面]。</span><span class="sxs-lookup"><span data-stu-id="7bd8e-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="7bd8e-126">筆記</span><span class="sxs-lookup"><span data-stu-id="7bd8e-126">NOTES</span></span>

## <span data-ttu-id="7bd8e-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="7bd8e-127">RELATED LINKS</span></span>

[<span data-ttu-id="7bd8e-128">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7bd8e-128">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7bd8e-129">AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7bd8e-129">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7bd8e-130">匯入-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7bd8e-130">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7bd8e-131">新-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7bd8e-131">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7bd8e-132">新-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7bd8e-132">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7bd8e-133">移除-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7bd8e-133">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7bd8e-134">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7bd8e-134">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7bd8e-135">開始-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7bd8e-135">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


