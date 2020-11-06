---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
ms.openlocfilehash: 71d66c6440091e50da2809f4b8c0669410d09d50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452604"
---
# <span data-ttu-id="22a64-101">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="22a64-101">Publish-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="22a64-102">摘要</span><span class="sxs-lookup"><span data-stu-id="22a64-102">SYNOPSIS</span></span>
<span data-ttu-id="22a64-103">發佈 runbook。</span><span class="sxs-lookup"><span data-stu-id="22a64-103">Publishes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22a64-104">句法</span><span class="sxs-lookup"><span data-stu-id="22a64-104">SYNTAX</span></span>

```
Publish-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22a64-105">說明</span><span class="sxs-lookup"><span data-stu-id="22a64-105">DESCRIPTION</span></span>
<span data-ttu-id="22a64-106">**AzureRmAutomationRunbook** Cmdlet 發佈 runbook，以用於 Azure 自動化的生產環境。</span><span class="sxs-lookup"><span data-stu-id="22a64-106">The **Publish-AzureRmAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="22a64-107">示例</span><span class="sxs-lookup"><span data-stu-id="22a64-107">EXAMPLES</span></span>

### <span data-ttu-id="22a64-108">範例1：發佈 runbook</span><span class="sxs-lookup"><span data-stu-id="22a64-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="22a64-109">這個命令會在名為 Contoso17 的 Azure 自動化帳戶中發佈名為 Runbk01 的 runbook。</span><span class="sxs-lookup"><span data-stu-id="22a64-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="22a64-110">參數</span><span class="sxs-lookup"><span data-stu-id="22a64-110">PARAMETERS</span></span>

### <span data-ttu-id="22a64-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="22a64-111">-AutomationAccountName</span></span>
<span data-ttu-id="22a64-112">指定此 Cmdlet 發佈 runbook 的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="22a64-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="22a64-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="22a64-113">-Name</span></span>
<span data-ttu-id="22a64-114">指定此 Cmdlet 發佈的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="22a64-114">Specifies the name of the runbook that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="22a64-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22a64-115">-ResourceGroupName</span></span>
<span data-ttu-id="22a64-116">指定此 Cmdlet 發佈 runbook 的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="22a64-116">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="22a64-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22a64-117">-DefaultProfile</span></span>
<span data-ttu-id="22a64-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="22a64-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22a64-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22a64-119">CommonParameters</span></span>
<span data-ttu-id="22a64-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="22a64-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22a64-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="22a64-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22a64-122">輸入</span><span class="sxs-lookup"><span data-stu-id="22a64-122">INPUTS</span></span>

## <span data-ttu-id="22a64-123">輸出</span><span class="sxs-lookup"><span data-stu-id="22a64-123">OUTPUTS</span></span>

### <span data-ttu-id="22a64-124">[-Azure. 命令介面]。</span><span class="sxs-lookup"><span data-stu-id="22a64-124">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="22a64-125">筆記</span><span class="sxs-lookup"><span data-stu-id="22a64-125">NOTES</span></span>

## <span data-ttu-id="22a64-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="22a64-126">RELATED LINKS</span></span>

[<span data-ttu-id="22a64-127">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="22a64-127">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="22a64-128">AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="22a64-128">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="22a64-129">匯入-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="22a64-129">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="22a64-130">新-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="22a64-130">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="22a64-131">新-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="22a64-131">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="22a64-132">移除-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="22a64-132">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="22a64-133">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="22a64-133">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="22a64-134">開始-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="22a64-134">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


