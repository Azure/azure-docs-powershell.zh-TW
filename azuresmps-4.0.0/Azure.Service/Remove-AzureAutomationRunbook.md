---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 0C156A1C-72DC-4B3C-9033-1B985139A732
online version: ''
schema: 2.0.0
ms.openlocfilehash: 43f371e44876c8927edc4f30fcfe0095a28cb27b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967617"
---
# <span data-ttu-id="81c46-101">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="81c46-101">Remove-AzureAutomationRunbook</span></span>

## <span data-ttu-id="81c46-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81c46-102">SYNOPSIS</span></span>

<span data-ttu-id="81c46-103">移除 runbook。</span><span class="sxs-lookup"><span data-stu-id="81c46-103">Removes a runbook.</span></span>

## <span data-ttu-id="81c46-104">句法</span><span class="sxs-lookup"><span data-stu-id="81c46-104">SYNTAX</span></span>

```
Remove-AzureAutomationRunbook -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81c46-105">說明</span><span class="sxs-lookup"><span data-stu-id="81c46-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="81c46-106">**AzureAutomationRunbook** Cmdlet 會從 Microsoft Azure 自動化中移除 runbook。</span><span class="sxs-lookup"><span data-stu-id="81c46-106">The **Remove-AzureAutomationRunbook** cmdlet removes a runbook from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="81c46-107">示例</span><span class="sxs-lookup"><span data-stu-id="81c46-107">EXAMPLES</span></span>

### <span data-ttu-id="81c46-108">範例1：移除 runbook</span><span class="sxs-lookup"><span data-stu-id="81c46-108">Example 1: Remove a runbook</span></span>
```
PS C:\> Remove-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "MyRunbook"
```

<span data-ttu-id="81c46-109">這個命令會移除名為 Contoso17 的自動化帳戶中名為 MyRunbook 的 runbook。</span><span class="sxs-lookup"><span data-stu-id="81c46-109">This command removes the runbook named MyRunbook in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="81c46-110">參數</span><span class="sxs-lookup"><span data-stu-id="81c46-110">PARAMETERS</span></span>

### <span data-ttu-id="81c46-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="81c46-111">-AutomationAccountName</span></span>
<span data-ttu-id="81c46-112">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="81c46-112">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="81c46-113">-Force</span><span class="sxs-lookup"><span data-stu-id="81c46-113">-Force</span></span>
<span data-ttu-id="81c46-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="81c46-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="81c46-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="81c46-115">-Name</span></span>
<span data-ttu-id="81c46-116">指定要移除的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="81c46-116">Specifies the name of the runbook to remove.</span></span>

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

### <span data-ttu-id="81c46-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="81c46-117">-Profile</span></span>
<span data-ttu-id="81c46-118">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="81c46-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="81c46-119">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="81c46-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="81c46-120">-確認</span><span class="sxs-lookup"><span data-stu-id="81c46-120">-Confirm</span></span>
<span data-ttu-id="81c46-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="81c46-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81c46-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81c46-122">-WhatIf</span></span>
<span data-ttu-id="81c46-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="81c46-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81c46-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81c46-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81c46-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81c46-125">CommonParameters</span></span>
<span data-ttu-id="81c46-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81c46-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81c46-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="81c46-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81c46-128">輸入</span><span class="sxs-lookup"><span data-stu-id="81c46-128">INPUTS</span></span>

## <span data-ttu-id="81c46-129">輸出</span><span class="sxs-lookup"><span data-stu-id="81c46-129">OUTPUTS</span></span>

## <span data-ttu-id="81c46-130">筆記</span><span class="sxs-lookup"><span data-stu-id="81c46-130">NOTES</span></span>

## <span data-ttu-id="81c46-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="81c46-131">RELATED LINKS</span></span>

[<span data-ttu-id="81c46-132">AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="81c46-132">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="81c46-133">新-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="81c46-133">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="81c46-134">發佈-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="81c46-134">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="81c46-135">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="81c46-135">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="81c46-136">開始-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="81c46-136">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


