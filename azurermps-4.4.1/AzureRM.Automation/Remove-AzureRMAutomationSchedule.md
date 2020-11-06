---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
ms.openlocfilehash: 562b5b5986d544f5fa8d91e0f39cb34ef9dababd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450884"
---
# <span data-ttu-id="3caab-101">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="3caab-101">Remove-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="3caab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3caab-102">SYNOPSIS</span></span>
<span data-ttu-id="3caab-103">刪除 [自動化排程]。</span><span class="sxs-lookup"><span data-stu-id="3caab-103">Deletes an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3caab-104">句法</span><span class="sxs-lookup"><span data-stu-id="3caab-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3caab-105">說明</span><span class="sxs-lookup"><span data-stu-id="3caab-105">DESCRIPTION</span></span>
<span data-ttu-id="3caab-106">**AzureRmAutomationSchedule** Cmdlet 會從 Azure 自動化中刪除排程。</span><span class="sxs-lookup"><span data-stu-id="3caab-106">The **Remove-AzureRmAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="3caab-107">示例</span><span class="sxs-lookup"><span data-stu-id="3caab-107">EXAMPLES</span></span>

### <span data-ttu-id="3caab-108">範例1：移除排程</span><span class="sxs-lookup"><span data-stu-id="3caab-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3caab-109">這個命令會修改名為 Schedule01 的排程的描述。</span><span class="sxs-lookup"><span data-stu-id="3caab-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="3caab-110">參數</span><span class="sxs-lookup"><span data-stu-id="3caab-110">PARAMETERS</span></span>

### <span data-ttu-id="3caab-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3caab-111">-AutomationAccountName</span></span>
<span data-ttu-id="3caab-112">指定此 Cmdlet 修改排程的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="3caab-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="3caab-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3caab-113">-Force</span></span>
<span data-ttu-id="3caab-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="3caab-114">ps_force</span></span>

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

### <span data-ttu-id="3caab-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="3caab-115">-Name</span></span>
<span data-ttu-id="3caab-116">指定此 Cmdlet 移除之排程的名稱。</span><span class="sxs-lookup"><span data-stu-id="3caab-116">Specifies the name for the schedule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3caab-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3caab-117">-ResourceGroupName</span></span>
<span data-ttu-id="3caab-118">指定此 Cmdlet 移除排程之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3caab-118">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="3caab-119">-確認</span><span class="sxs-lookup"><span data-stu-id="3caab-119">-Confirm</span></span>
<span data-ttu-id="3caab-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3caab-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3caab-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3caab-121">-WhatIf</span></span>
<span data-ttu-id="3caab-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3caab-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3caab-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3caab-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3caab-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3caab-124">-DefaultProfile</span></span>
<span data-ttu-id="3caab-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3caab-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3caab-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3caab-126">CommonParameters</span></span>
<span data-ttu-id="3caab-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3caab-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3caab-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3caab-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3caab-129">輸入</span><span class="sxs-lookup"><span data-stu-id="3caab-129">INPUTS</span></span>

## <span data-ttu-id="3caab-130">輸出</span><span class="sxs-lookup"><span data-stu-id="3caab-130">OUTPUTS</span></span>

## <span data-ttu-id="3caab-131">筆記</span><span class="sxs-lookup"><span data-stu-id="3caab-131">NOTES</span></span>

## <span data-ttu-id="3caab-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="3caab-132">RELATED LINKS</span></span>

[<span data-ttu-id="3caab-133">AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="3caab-133">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="3caab-134">新-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="3caab-134">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="3caab-135">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="3caab-135">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


