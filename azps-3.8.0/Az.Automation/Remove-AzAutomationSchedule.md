---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
ms.openlocfilehash: 0c37c33b60d430bc1782254401033934552f5663
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966369"
---
# <span data-ttu-id="df53b-101">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="df53b-101">Remove-AzAutomationSchedule</span></span>

## <span data-ttu-id="df53b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="df53b-102">SYNOPSIS</span></span>
<span data-ttu-id="df53b-103">刪除 [自動化排程]。</span><span class="sxs-lookup"><span data-stu-id="df53b-103">Deletes an Automation schedule.</span></span>

## <span data-ttu-id="df53b-104">句法</span><span class="sxs-lookup"><span data-stu-id="df53b-104">SYNTAX</span></span>

```
Remove-AzAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df53b-105">說明</span><span class="sxs-lookup"><span data-stu-id="df53b-105">DESCRIPTION</span></span>
<span data-ttu-id="df53b-106">**AzAutomationSchedule** Cmdlet 會從 Azure 自動化中刪除排程。</span><span class="sxs-lookup"><span data-stu-id="df53b-106">The **Remove-AzAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="df53b-107">示例</span><span class="sxs-lookup"><span data-stu-id="df53b-107">EXAMPLES</span></span>

### <span data-ttu-id="df53b-108">範例1：移除排程</span><span class="sxs-lookup"><span data-stu-id="df53b-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="df53b-109">這個命令會在 [資源群組 ResourceGroup01] 的 [自動化帳戶] Contoso17 中刪除名為 Schedule01 的排程。</span><span class="sxs-lookup"><span data-stu-id="df53b-109">This command deletes the schedule named Schedule01 in automation account Contoso17 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="df53b-110">參數</span><span class="sxs-lookup"><span data-stu-id="df53b-110">PARAMETERS</span></span>

### <span data-ttu-id="df53b-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="df53b-111">-AutomationAccountName</span></span>
<span data-ttu-id="df53b-112">指定此 Cmdlet 移除排程之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="df53b-112">Specifies the name of an Automation account for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="df53b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df53b-113">-DefaultProfile</span></span>
<span data-ttu-id="df53b-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="df53b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df53b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="df53b-115">-Force</span></span>
<span data-ttu-id="df53b-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="df53b-116">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df53b-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="df53b-117">-Name</span></span>
<span data-ttu-id="df53b-118">指定此 Cmdlet 移除之排程的名稱。</span><span class="sxs-lookup"><span data-stu-id="df53b-118">Specifies the name for the schedule that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df53b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df53b-119">-ResourceGroupName</span></span>
<span data-ttu-id="df53b-120">指定此 Cmdlet 移除排程之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="df53b-120">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="df53b-121">-確認</span><span class="sxs-lookup"><span data-stu-id="df53b-121">-Confirm</span></span>
<span data-ttu-id="df53b-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="df53b-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df53b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df53b-123">-WhatIf</span></span>
<span data-ttu-id="df53b-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="df53b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df53b-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="df53b-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df53b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df53b-126">CommonParameters</span></span>
<span data-ttu-id="df53b-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="df53b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df53b-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="df53b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df53b-129">輸入</span><span class="sxs-lookup"><span data-stu-id="df53b-129">INPUTS</span></span>

### <span data-ttu-id="df53b-130">System.object</span><span class="sxs-lookup"><span data-stu-id="df53b-130">System.String</span></span>

## <span data-ttu-id="df53b-131">輸出</span><span class="sxs-lookup"><span data-stu-id="df53b-131">OUTPUTS</span></span>

### <span data-ttu-id="df53b-132">System.void</span><span class="sxs-lookup"><span data-stu-id="df53b-132">System.Void</span></span>

## <span data-ttu-id="df53b-133">筆記</span><span class="sxs-lookup"><span data-stu-id="df53b-133">NOTES</span></span>

## <span data-ttu-id="df53b-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="df53b-134">RELATED LINKS</span></span>

[<span data-ttu-id="df53b-135">AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="df53b-135">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="df53b-136">新-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="df53b-136">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="df53b-137">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="df53b-137">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


