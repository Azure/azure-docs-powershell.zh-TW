---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/powershell/module/az.automation/publish-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
ms.openlocfilehash: fa10c44186de06de758e4f7878bb7c8da61c4d6c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915654"
---
# <span data-ttu-id="a7542-101">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a7542-101">Publish-AzAutomationRunbook</span></span>

## <span data-ttu-id="a7542-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a7542-102">SYNOPSIS</span></span>
<span data-ttu-id="a7542-103">發佈執行簿。</span><span class="sxs-lookup"><span data-stu-id="a7542-103">Publishes a runbook.</span></span>

## <span data-ttu-id="a7542-104">語法</span><span class="sxs-lookup"><span data-stu-id="a7542-104">SYNTAX</span></span>

```
Publish-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7542-105">描述</span><span class="sxs-lookup"><span data-stu-id="a7542-105">DESCRIPTION</span></span>
<span data-ttu-id="a7542-106">**Publish-AzAutomationRunbook** Cmdlet 會發佈用於 Azure Automation 生產環境的 Runbook。</span><span class="sxs-lookup"><span data-stu-id="a7542-106">The **Publish-AzAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="a7542-107">例子</span><span class="sxs-lookup"><span data-stu-id="a7542-107">EXAMPLES</span></span>

### <span data-ttu-id="a7542-108">範例 1：發佈 runbook</span><span class="sxs-lookup"><span data-stu-id="a7542-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a7542-109">此命令在名為 Contoso17 的 Azure 自動化帳戶中發佈名為 Runbk01 的 runbook。</span><span class="sxs-lookup"><span data-stu-id="a7542-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="a7542-110">參數</span><span class="sxs-lookup"><span data-stu-id="a7542-110">PARAMETERS</span></span>

### <span data-ttu-id="a7542-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a7542-111">-AutomationAccountName</span></span>
<span data-ttu-id="a7542-112">指定此 Cmdlet 發佈 Runbook 的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a7542-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="a7542-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7542-113">-DefaultProfile</span></span>
<span data-ttu-id="a7542-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a7542-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7542-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="a7542-115">-Name</span></span>
<span data-ttu-id="a7542-116">指定此 Cmdlet 所發佈之 runbook 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7542-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="a7542-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7542-117">-ResourceGroupName</span></span>
<span data-ttu-id="a7542-118">指定此 Cmdlet 發佈 Runbook 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a7542-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="a7542-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7542-119">CommonParameters</span></span>
<span data-ttu-id="a7542-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a7542-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7542-121">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a7542-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7542-122">輸入</span><span class="sxs-lookup"><span data-stu-id="a7542-122">INPUTS</span></span>

### <span data-ttu-id="a7542-123">System.String</span><span class="sxs-lookup"><span data-stu-id="a7542-123">System.String</span></span>

## <span data-ttu-id="a7542-124">輸出</span><span class="sxs-lookup"><span data-stu-id="a7542-124">OUTPUTS</span></span>

### <span data-ttu-id="a7542-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span><span class="sxs-lookup"><span data-stu-id="a7542-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="a7542-126">筆記</span><span class="sxs-lookup"><span data-stu-id="a7542-126">NOTES</span></span>

## <span data-ttu-id="a7542-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7542-127">RELATED LINKS</span></span>

[<span data-ttu-id="a7542-128">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a7542-128">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="a7542-129">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a7542-129">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="a7542-130">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a7542-130">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="a7542-131">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a7542-131">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="a7542-132">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a7542-132">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="a7542-133">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a7542-133">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="a7542-134">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a7542-134">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="a7542-135">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a7542-135">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


