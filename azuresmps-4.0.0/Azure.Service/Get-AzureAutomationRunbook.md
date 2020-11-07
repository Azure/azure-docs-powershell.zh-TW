---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 304F71E0-9E89-46E6-BD25-7584601CC845
online version: ''
schema: 2.0.0
ms.openlocfilehash: e507b1b35bf8739c80bbdf92f02f29099ceb3284
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967103"
---
# <span data-ttu-id="11c52-101">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="11c52-101">Get-AzureAutomationRunbook</span></span>

## <span data-ttu-id="11c52-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11c52-102">SYNOPSIS</span></span>

<span data-ttu-id="11c52-103">取得 runbook。</span><span class="sxs-lookup"><span data-stu-id="11c52-103">Gets a runbook.</span></span>

## <span data-ttu-id="11c52-104">句法</span><span class="sxs-lookup"><span data-stu-id="11c52-104">SYNTAX</span></span>

### <span data-ttu-id="11c52-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="11c52-105">ByAll (Default)</span></span>
```
Get-AzureAutomationRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="11c52-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="11c52-106">ByRunbookName</span></span>
```
Get-AzureAutomationRunbook -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="11c52-107">說明</span><span class="sxs-lookup"><span data-stu-id="11c52-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="11c52-108">**AzureAutomationRunbook** Cmdlet 會取得一或多個 Microsoft Azure 自動化 runbook。</span><span class="sxs-lookup"><span data-stu-id="11c52-108">The **Get-AzureAutomationRunbook** cmdlet gets one or more Microsoft Azure Automation runbooks.</span></span>
<span data-ttu-id="11c52-109">根據預設，會傳回所有的 runbook。</span><span class="sxs-lookup"><span data-stu-id="11c52-109">By default, all runbooks are returned.</span></span>
<span data-ttu-id="11c52-110">若要取得特定的 runbook，請指定其名稱或 ID。</span><span class="sxs-lookup"><span data-stu-id="11c52-110">To get a specific runbook, specify its name or ID.</span></span>
<span data-ttu-id="11c52-111">若要取得連結至特定排程的所有 runbook，請指定排程名稱。</span><span class="sxs-lookup"><span data-stu-id="11c52-111">To get all runbooks linked to a specific schedule, specify the schedule name.</span></span>

## <span data-ttu-id="11c52-112">示例</span><span class="sxs-lookup"><span data-stu-id="11c52-112">EXAMPLES</span></span>

### <span data-ttu-id="11c52-113">範例1：取得所有 runbook</span><span class="sxs-lookup"><span data-stu-id="11c52-113">Example 1: Get all runbooks</span></span>
```
PS C:\> Get-AzureAutomationRunbook -AutomationAccountName "Contoso17"
```

<span data-ttu-id="11c52-114">這個命令會取得 Azure 自動化帳戶（名為 Contoso17）中的所有 runbook。</span><span class="sxs-lookup"><span data-stu-id="11c52-114">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="11c52-115">參數</span><span class="sxs-lookup"><span data-stu-id="11c52-115">PARAMETERS</span></span>

### <span data-ttu-id="11c52-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="11c52-116">-AutomationAccountName</span></span>
<span data-ttu-id="11c52-117">指定 Azure 自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="11c52-117">Specifies the name of an Azure Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11c52-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="11c52-118">-Name</span></span>
<span data-ttu-id="11c52-119">指定 runbook 的名稱。</span><span class="sxs-lookup"><span data-stu-id="11c52-119">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11c52-120">-設定檔</span><span class="sxs-lookup"><span data-stu-id="11c52-120">-Profile</span></span>
<span data-ttu-id="11c52-121">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="11c52-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="11c52-122">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="11c52-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c52-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11c52-123">CommonParameters</span></span>
<span data-ttu-id="11c52-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="11c52-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11c52-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="11c52-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11c52-126">輸入</span><span class="sxs-lookup"><span data-stu-id="11c52-126">INPUTS</span></span>

## <span data-ttu-id="11c52-127">輸出</span><span class="sxs-lookup"><span data-stu-id="11c52-127">OUTPUTS</span></span>

### <span data-ttu-id="11c52-128">[-Azure. 命令介面]。</span><span class="sxs-lookup"><span data-stu-id="11c52-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="11c52-129">筆記</span><span class="sxs-lookup"><span data-stu-id="11c52-129">NOTES</span></span>

## <span data-ttu-id="11c52-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="11c52-130">RELATED LINKS</span></span>

[<span data-ttu-id="11c52-131">新-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="11c52-131">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="11c52-132">發佈-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="11c52-132">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="11c52-133">移除-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="11c52-133">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="11c52-134">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="11c52-134">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="11c52-135">開始-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="11c52-135">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


