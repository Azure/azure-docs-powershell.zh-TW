---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2412F6BC-E338-4D9C-8982-C0668C1CA4C2
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2b8ae09c79b420d7273fc6db23e23a6846a542e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967616"
---
# <span data-ttu-id="1e6be-101">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="1e6be-101">Remove-AzureAutomationSchedule</span></span>

## <span data-ttu-id="1e6be-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1e6be-102">SYNOPSIS</span></span>

<span data-ttu-id="1e6be-103">刪除 Azure 自動化排程。</span><span class="sxs-lookup"><span data-stu-id="1e6be-103">Deletes an Azure Automation schedule.</span></span>

## <span data-ttu-id="1e6be-104">句法</span><span class="sxs-lookup"><span data-stu-id="1e6be-104">SYNTAX</span></span>

```
Remove-AzureAutomationSchedule -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e6be-105">說明</span><span class="sxs-lookup"><span data-stu-id="1e6be-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="1e6be-106">**AzureAutomationSchedule** Cmdlet 會從 Microsoft Azure 自動化中刪除排程。</span><span class="sxs-lookup"><span data-stu-id="1e6be-106">The **Remove-AzureAutomationSchedule** cmdlet deletes a schedule from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="1e6be-107">示例</span><span class="sxs-lookup"><span data-stu-id="1e6be-107">EXAMPLES</span></span>

### <span data-ttu-id="1e6be-108">範例1：移除排程</span><span class="sxs-lookup"><span data-stu-id="1e6be-108">Example 1: Remove a schedule</span></span>
```
PS C:\> Remove-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "MySchedule"
```

<span data-ttu-id="1e6be-109">這個命令會移除名為 MySchedule 的排程。</span><span class="sxs-lookup"><span data-stu-id="1e6be-109">This command removes the schedule named MySchedule.</span></span>

## <span data-ttu-id="1e6be-110">參數</span><span class="sxs-lookup"><span data-stu-id="1e6be-110">PARAMETERS</span></span>

### <span data-ttu-id="1e6be-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1e6be-111">-AutomationAccountName</span></span>
<span data-ttu-id="1e6be-112">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e6be-112">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="1e6be-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1e6be-113">-Force</span></span>
<span data-ttu-id="1e6be-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="1e6be-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1e6be-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="1e6be-115">-Name</span></span>
<span data-ttu-id="1e6be-116">指定要移除排程的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e6be-116">Specifies the name of the schedule to remove.</span></span>

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

### <span data-ttu-id="1e6be-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="1e6be-117">-Profile</span></span>
<span data-ttu-id="1e6be-118">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="1e6be-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1e6be-119">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="1e6be-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1e6be-120">-確認</span><span class="sxs-lookup"><span data-stu-id="1e6be-120">-Confirm</span></span>
<span data-ttu-id="1e6be-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1e6be-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e6be-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e6be-122">-WhatIf</span></span>
<span data-ttu-id="1e6be-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1e6be-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e6be-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e6be-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e6be-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e6be-125">CommonParameters</span></span>
<span data-ttu-id="1e6be-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1e6be-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e6be-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1e6be-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e6be-128">輸入</span><span class="sxs-lookup"><span data-stu-id="1e6be-128">INPUTS</span></span>

## <span data-ttu-id="1e6be-129">輸出</span><span class="sxs-lookup"><span data-stu-id="1e6be-129">OUTPUTS</span></span>

## <span data-ttu-id="1e6be-130">筆記</span><span class="sxs-lookup"><span data-stu-id="1e6be-130">NOTES</span></span>

## <span data-ttu-id="1e6be-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e6be-131">RELATED LINKS</span></span>

[<span data-ttu-id="1e6be-132">AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="1e6be-132">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="1e6be-133">新-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="1e6be-133">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="1e6be-134">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="1e6be-134">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)


