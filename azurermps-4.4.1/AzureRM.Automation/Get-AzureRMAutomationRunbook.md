---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
ms.openlocfilehash: e543a7da3ce5502e0f78619ca4fbb455b29b82d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446892"
---
# <span data-ttu-id="4a7c8-101">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4a7c8-101">Get-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="4a7c8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4a7c8-102">SYNOPSIS</span></span>
<span data-ttu-id="4a7c8-103">取得 runbook。</span><span class="sxs-lookup"><span data-stu-id="4a7c8-103">Gets a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a7c8-104">句法</span><span class="sxs-lookup"><span data-stu-id="4a7c8-104">SYNTAX</span></span>

### <span data-ttu-id="4a7c8-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="4a7c8-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a7c8-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="4a7c8-106">ByRunbookName</span></span>
```
Get-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a7c8-107">說明</span><span class="sxs-lookup"><span data-stu-id="4a7c8-107">DESCRIPTION</span></span>
<span data-ttu-id="4a7c8-108">**AzureRmAutomationRunbook** Cmdlet 會取得 Azure 自動化 runbook。</span><span class="sxs-lookup"><span data-stu-id="4a7c8-108">The **Get-AzureRmAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="4a7c8-109">若要取得特定的 runbook，請指定其名稱。</span><span class="sxs-lookup"><span data-stu-id="4a7c8-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="4a7c8-110">示例</span><span class="sxs-lookup"><span data-stu-id="4a7c8-110">EXAMPLES</span></span>

### <span data-ttu-id="4a7c8-111">範例1：取得所有 runbook</span><span class="sxs-lookup"><span data-stu-id="4a7c8-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4a7c8-112">這個命令會取得 Azure 自動化帳戶（名為 Contoso17）中的所有 runbook。</span><span class="sxs-lookup"><span data-stu-id="4a7c8-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="4a7c8-113">參數</span><span class="sxs-lookup"><span data-stu-id="4a7c8-113">PARAMETERS</span></span>

### <span data-ttu-id="4a7c8-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4a7c8-114">-AutomationAccountName</span></span>
<span data-ttu-id="4a7c8-115">指定此 Cmdlet 在其中取得 runbook 的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="4a7c8-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="4a7c8-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="4a7c8-116">-Name</span></span>
<span data-ttu-id="4a7c8-117">指定此 Cmdlet 取得的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="4a7c8-117">Specifies the name of a runbook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4a7c8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a7c8-118">-ResourceGroupName</span></span>
<span data-ttu-id="4a7c8-119">指定此 Cmdlet 取得 runbook 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4a7c8-119">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="4a7c8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a7c8-120">-DefaultProfile</span></span>
<span data-ttu-id="4a7c8-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4a7c8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a7c8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a7c8-122">CommonParameters</span></span>
<span data-ttu-id="4a7c8-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4a7c8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a7c8-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4a7c8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a7c8-125">輸入</span><span class="sxs-lookup"><span data-stu-id="4a7c8-125">INPUTS</span></span>

## <span data-ttu-id="4a7c8-126">輸出</span><span class="sxs-lookup"><span data-stu-id="4a7c8-126">OUTPUTS</span></span>

### <span data-ttu-id="4a7c8-127">[-Azure. 命令介面]。</span><span class="sxs-lookup"><span data-stu-id="4a7c8-127">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="4a7c8-128">筆記</span><span class="sxs-lookup"><span data-stu-id="4a7c8-128">NOTES</span></span>

## <span data-ttu-id="4a7c8-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="4a7c8-129">RELATED LINKS</span></span>

[<span data-ttu-id="4a7c8-130">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4a7c8-130">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="4a7c8-131">匯入-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4a7c8-131">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="4a7c8-132">新-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4a7c8-132">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="4a7c8-133">新-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4a7c8-133">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="4a7c8-134">發佈-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4a7c8-134">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="4a7c8-135">移除-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4a7c8-135">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="4a7c8-136">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4a7c8-136">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="4a7c8-137">開始-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4a7c8-137">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


