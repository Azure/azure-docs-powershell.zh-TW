---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
ms.openlocfilehash: 83481e1d12782c3381c2d5923aa610072da41d9a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456236"
---
# <span data-ttu-id="dcf26-101">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="dcf26-101">Remove-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="dcf26-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dcf26-102">SYNOPSIS</span></span>
<span data-ttu-id="dcf26-103">刪除 [自動化排程]。</span><span class="sxs-lookup"><span data-stu-id="dcf26-103">Deletes an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcf26-104">句法</span><span class="sxs-lookup"><span data-stu-id="dcf26-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dcf26-105">說明</span><span class="sxs-lookup"><span data-stu-id="dcf26-105">DESCRIPTION</span></span>
<span data-ttu-id="dcf26-106">**AzureRmAutomationSchedule** Cmdlet 會從 Azure 自動化中刪除排程。</span><span class="sxs-lookup"><span data-stu-id="dcf26-106">The **Remove-AzureRmAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="dcf26-107">示例</span><span class="sxs-lookup"><span data-stu-id="dcf26-107">EXAMPLES</span></span>

### <span data-ttu-id="dcf26-108">範例1：移除排程</span><span class="sxs-lookup"><span data-stu-id="dcf26-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="dcf26-109">這個命令會修改名為 Schedule01 的排程的描述。</span><span class="sxs-lookup"><span data-stu-id="dcf26-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="dcf26-110">參數</span><span class="sxs-lookup"><span data-stu-id="dcf26-110">PARAMETERS</span></span>

### <span data-ttu-id="dcf26-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dcf26-111">-AutomationAccountName</span></span>
<span data-ttu-id="dcf26-112">指定此 Cmdlet 修改排程的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="dcf26-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="dcf26-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcf26-113">-DefaultProfile</span></span>
<span data-ttu-id="dcf26-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="dcf26-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dcf26-115">-Force</span><span class="sxs-lookup"><span data-stu-id="dcf26-115">-Force</span></span>
<span data-ttu-id="dcf26-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="dcf26-116">ps_force</span></span>

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

### <span data-ttu-id="dcf26-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="dcf26-117">-Name</span></span>
<span data-ttu-id="dcf26-118">指定此 Cmdlet 移除之排程的名稱。</span><span class="sxs-lookup"><span data-stu-id="dcf26-118">Specifies the name for the schedule that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcf26-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcf26-119">-ResourceGroupName</span></span>
<span data-ttu-id="dcf26-120">指定此 Cmdlet 移除排程之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dcf26-120">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="dcf26-121">-確認</span><span class="sxs-lookup"><span data-stu-id="dcf26-121">-Confirm</span></span>
<span data-ttu-id="dcf26-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dcf26-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcf26-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcf26-123">-WhatIf</span></span>
<span data-ttu-id="dcf26-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dcf26-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcf26-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dcf26-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcf26-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcf26-126">CommonParameters</span></span>
<span data-ttu-id="dcf26-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dcf26-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcf26-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dcf26-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcf26-129">輸入</span><span class="sxs-lookup"><span data-stu-id="dcf26-129">INPUTS</span></span>

### <span data-ttu-id="dcf26-130">所有</span><span class="sxs-lookup"><span data-stu-id="dcf26-130">None</span></span>
<span data-ttu-id="dcf26-131">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="dcf26-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dcf26-132">輸出</span><span class="sxs-lookup"><span data-stu-id="dcf26-132">OUTPUTS</span></span>

## <span data-ttu-id="dcf26-133">筆記</span><span class="sxs-lookup"><span data-stu-id="dcf26-133">NOTES</span></span>

## <span data-ttu-id="dcf26-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="dcf26-134">RELATED LINKS</span></span>

[<span data-ttu-id="dcf26-135">AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="dcf26-135">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="dcf26-136">新-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="dcf26-136">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="dcf26-137">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="dcf26-137">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


