---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/publish-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
ms.openlocfilehash: 1202ecbdaaf07b9ba5704a01449784172204bf73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446547"
---
# <span data-ttu-id="58caa-101">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="58caa-101">Publish-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="58caa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58caa-102">SYNOPSIS</span></span>
<span data-ttu-id="58caa-103">發佈 runbook。</span><span class="sxs-lookup"><span data-stu-id="58caa-103">Publishes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58caa-104">句法</span><span class="sxs-lookup"><span data-stu-id="58caa-104">SYNTAX</span></span>

```
Publish-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58caa-105">說明</span><span class="sxs-lookup"><span data-stu-id="58caa-105">DESCRIPTION</span></span>
<span data-ttu-id="58caa-106">**AzureRmAutomationRunbook** Cmdlet 發佈 runbook，以用於 Azure 自動化的生產環境。</span><span class="sxs-lookup"><span data-stu-id="58caa-106">The **Publish-AzureRmAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="58caa-107">示例</span><span class="sxs-lookup"><span data-stu-id="58caa-107">EXAMPLES</span></span>

### <span data-ttu-id="58caa-108">範例1：發佈 runbook</span><span class="sxs-lookup"><span data-stu-id="58caa-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="58caa-109">這個命令會在名為 Contoso17 的 Azure 自動化帳戶中發佈名為 Runbk01 的 runbook。</span><span class="sxs-lookup"><span data-stu-id="58caa-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="58caa-110">參數</span><span class="sxs-lookup"><span data-stu-id="58caa-110">PARAMETERS</span></span>

### <span data-ttu-id="58caa-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="58caa-111">-AutomationAccountName</span></span>
<span data-ttu-id="58caa-112">指定此 Cmdlet 發佈 runbook 的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="58caa-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="58caa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58caa-113">-DefaultProfile</span></span>
<span data-ttu-id="58caa-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="58caa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58caa-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="58caa-115">-Name</span></span>
<span data-ttu-id="58caa-116">指定此 Cmdlet 發佈的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="58caa-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="58caa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58caa-117">-ResourceGroupName</span></span>
<span data-ttu-id="58caa-118">指定此 Cmdlet 發佈 runbook 的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="58caa-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="58caa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58caa-119">CommonParameters</span></span>
<span data-ttu-id="58caa-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58caa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58caa-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="58caa-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58caa-122">輸入</span><span class="sxs-lookup"><span data-stu-id="58caa-122">INPUTS</span></span>

### <span data-ttu-id="58caa-123">所有</span><span class="sxs-lookup"><span data-stu-id="58caa-123">None</span></span>
<span data-ttu-id="58caa-124">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="58caa-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="58caa-125">輸出</span><span class="sxs-lookup"><span data-stu-id="58caa-125">OUTPUTS</span></span>

### <span data-ttu-id="58caa-126">[-Azure. 命令介面]。</span><span class="sxs-lookup"><span data-stu-id="58caa-126">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="58caa-127">筆記</span><span class="sxs-lookup"><span data-stu-id="58caa-127">NOTES</span></span>

## <span data-ttu-id="58caa-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="58caa-128">RELATED LINKS</span></span>

[<span data-ttu-id="58caa-129">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="58caa-129">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="58caa-130">AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="58caa-130">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="58caa-131">匯入-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="58caa-131">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="58caa-132">新-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="58caa-132">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="58caa-133">新-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="58caa-133">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="58caa-134">移除-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="58caa-134">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="58caa-135">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="58caa-135">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="58caa-136">開始-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="58caa-136">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


