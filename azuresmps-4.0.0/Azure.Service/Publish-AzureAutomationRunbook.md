---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 454948A7-CE50-4C5A-AEBF-789B1A94F27E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 62507f18e21c1e528f93f5de512e8ffc1fa2dfa3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967331"
---
# <span data-ttu-id="b5d14-101">Publish-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b5d14-101">Publish-AzureAutomationRunbook</span></span>

## <span data-ttu-id="b5d14-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b5d14-102">SYNOPSIS</span></span>

<span data-ttu-id="b5d14-103">發佈 runbook。</span><span class="sxs-lookup"><span data-stu-id="b5d14-103">Publishes a runbook.</span></span>

## <span data-ttu-id="b5d14-104">句法</span><span class="sxs-lookup"><span data-stu-id="b5d14-104">SYNTAX</span></span>

```
Publish-AzureAutomationRunbook -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5d14-105">說明</span><span class="sxs-lookup"><span data-stu-id="b5d14-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="b5d14-106">**AzureAutomationRunbook** Cmdlet 發佈 runbook，以用於 Microsoft Azure 自動化的生產環境。</span><span class="sxs-lookup"><span data-stu-id="b5d14-106">The **Publish-AzureAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Microsoft Azure Automation.</span></span>

## <span data-ttu-id="b5d14-107">示例</span><span class="sxs-lookup"><span data-stu-id="b5d14-107">EXAMPLES</span></span>

### <span data-ttu-id="b5d14-108">範例1：發佈 runbook</span><span class="sxs-lookup"><span data-stu-id="b5d14-108">Example 1: Publish a runbook</span></span>
```
PS C:\> Publish-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01"
```

<span data-ttu-id="b5d14-109">這個命令會在名為 Contoso17 的自動化帳戶中發佈名為 Runbk01 的 runbook。</span><span class="sxs-lookup"><span data-stu-id="b5d14-109">This command publishes the runbook named Runbk01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="b5d14-110">參數</span><span class="sxs-lookup"><span data-stu-id="b5d14-110">PARAMETERS</span></span>

### <span data-ttu-id="b5d14-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b5d14-111">-AutomationAccountName</span></span>
<span data-ttu-id="b5d14-112">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5d14-112">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="b5d14-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="b5d14-113">-Name</span></span>
<span data-ttu-id="b5d14-114">指定 runbook 的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5d14-114">Specifies the name of the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5d14-115">-設定檔</span><span class="sxs-lookup"><span data-stu-id="b5d14-115">-Profile</span></span>
<span data-ttu-id="b5d14-116">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b5d14-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b5d14-117">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="b5d14-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b5d14-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5d14-118">CommonParameters</span></span>
<span data-ttu-id="b5d14-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b5d14-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5d14-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b5d14-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5d14-121">輸入</span><span class="sxs-lookup"><span data-stu-id="b5d14-121">INPUTS</span></span>

## <span data-ttu-id="b5d14-122">輸出</span><span class="sxs-lookup"><span data-stu-id="b5d14-122">OUTPUTS</span></span>

## <span data-ttu-id="b5d14-123">筆記</span><span class="sxs-lookup"><span data-stu-id="b5d14-123">NOTES</span></span>

## <span data-ttu-id="b5d14-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5d14-124">RELATED LINKS</span></span>

[<span data-ttu-id="b5d14-125">AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b5d14-125">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="b5d14-126">新-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b5d14-126">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="b5d14-127">移除-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b5d14-127">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="b5d14-128">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b5d14-128">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="b5d14-129">開始-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b5d14-129">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


