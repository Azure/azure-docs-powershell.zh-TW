---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
ms.openlocfilehash: 00d6908e244a54fb2dbd501f0d944fc9cfdbdff4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917490"
---
# <span data-ttu-id="a1b41-101">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a1b41-101">Get-AzAutomationRunbook</span></span>

## <span data-ttu-id="a1b41-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a1b41-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b41-103">獲得執行簿。</span><span class="sxs-lookup"><span data-stu-id="a1b41-103">Gets a runbook.</span></span>

## <span data-ttu-id="a1b41-104">語法</span><span class="sxs-lookup"><span data-stu-id="a1b41-104">SYNTAX</span></span>

### <span data-ttu-id="a1b41-105">根據預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="a1b41-105">ByAll (Default)</span></span>
```
Get-AzAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1b41-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="a1b41-106">ByRunbookName</span></span>
```
Get-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1b41-107">描述</span><span class="sxs-lookup"><span data-stu-id="a1b41-107">DESCRIPTION</span></span>
<span data-ttu-id="a1b41-108">**Get-AzAutomationRunbook** Cmdlet 會取得 Azure Automation Runbooks。</span><span class="sxs-lookup"><span data-stu-id="a1b41-108">The **Get-AzAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="a1b41-109">若要取得特定的 runbook，請指定其名稱。</span><span class="sxs-lookup"><span data-stu-id="a1b41-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="a1b41-110">例子</span><span class="sxs-lookup"><span data-stu-id="a1b41-110">EXAMPLES</span></span>

### <span data-ttu-id="a1b41-111">範例 1：取得所有 runbooks</span><span class="sxs-lookup"><span data-stu-id="a1b41-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a1b41-112">此命令會獲得 Azure Automation 帳戶中名為 Contoso17 的所有 runbook。</span><span class="sxs-lookup"><span data-stu-id="a1b41-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="a1b41-113">參數</span><span class="sxs-lookup"><span data-stu-id="a1b41-113">PARAMETERS</span></span>

### <span data-ttu-id="a1b41-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a1b41-114">-AutomationAccountName</span></span>
<span data-ttu-id="a1b41-115">指定此 Cmdlet 可在此獲得 runbooks 的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a1b41-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="a1b41-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b41-116">-DefaultProfile</span></span>
<span data-ttu-id="a1b41-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a1b41-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1b41-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="a1b41-118">-Name</span></span>
<span data-ttu-id="a1b41-119">指定此 Cmdlet 所獲得之 runbook 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1b41-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b41-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1b41-120">-ResourceGroupName</span></span>
<span data-ttu-id="a1b41-121">指定此 Cmdlet 會獲得 runbook 之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1b41-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="a1b41-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b41-122">CommonParameters</span></span>
<span data-ttu-id="a1b41-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a1b41-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b41-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a1b41-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b41-125">輸入</span><span class="sxs-lookup"><span data-stu-id="a1b41-125">INPUTS</span></span>

### <span data-ttu-id="a1b41-126">System.String</span><span class="sxs-lookup"><span data-stu-id="a1b41-126">System.String</span></span>

## <span data-ttu-id="a1b41-127">輸出</span><span class="sxs-lookup"><span data-stu-id="a1b41-127">OUTPUTS</span></span>

### <span data-ttu-id="a1b41-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span><span class="sxs-lookup"><span data-stu-id="a1b41-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="a1b41-129">筆記</span><span class="sxs-lookup"><span data-stu-id="a1b41-129">NOTES</span></span>

## <span data-ttu-id="a1b41-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1b41-130">RELATED LINKS</span></span>

[<span data-ttu-id="a1b41-131">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a1b41-131">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="a1b41-132">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a1b41-132">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="a1b41-133">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a1b41-133">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="a1b41-134">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a1b41-134">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="a1b41-135">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a1b41-135">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="a1b41-136">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a1b41-136">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="a1b41-137">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a1b41-137">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="a1b41-138">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a1b41-138">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


