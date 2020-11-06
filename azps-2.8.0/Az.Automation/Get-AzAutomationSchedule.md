---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
ms.openlocfilehash: 237cd5dfa3ae64273361bb2f79f301ffa93dd29c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613779"
---
# <span data-ttu-id="c94cc-101">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="c94cc-101">Get-AzAutomationSchedule</span></span>

## <span data-ttu-id="c94cc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c94cc-102">SYNOPSIS</span></span>
<span data-ttu-id="c94cc-103">取得自動化排程。</span><span class="sxs-lookup"><span data-stu-id="c94cc-103">Gets an Automation schedule.</span></span>

## <span data-ttu-id="c94cc-104">句法</span><span class="sxs-lookup"><span data-stu-id="c94cc-104">SYNTAX</span></span>

### <span data-ttu-id="c94cc-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="c94cc-105">ByAll (Default)</span></span>
```
Get-AzAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c94cc-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c94cc-106">ByName</span></span>
```
Get-AzAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c94cc-107">說明</span><span class="sxs-lookup"><span data-stu-id="c94cc-107">DESCRIPTION</span></span>
<span data-ttu-id="c94cc-108">**AzAutomationSchedule** Cmdlet 會取得 Azure 自動化排程。</span><span class="sxs-lookup"><span data-stu-id="c94cc-108">The **Get-AzAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="c94cc-109">示例</span><span class="sxs-lookup"><span data-stu-id="c94cc-109">EXAMPLES</span></span>

### <span data-ttu-id="c94cc-110">範例1：取得排程</span><span class="sxs-lookup"><span data-stu-id="c94cc-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c94cc-111">這個命令會取得名為 DailySchedule08 的排程。</span><span class="sxs-lookup"><span data-stu-id="c94cc-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="c94cc-112">參數</span><span class="sxs-lookup"><span data-stu-id="c94cc-112">PARAMETERS</span></span>

### <span data-ttu-id="c94cc-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c94cc-113">-AutomationAccountName</span></span>
<span data-ttu-id="c94cc-114">指定此 Cmdlet 取得排程之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="c94cc-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="c94cc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c94cc-115">-DefaultProfile</span></span>
<span data-ttu-id="c94cc-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c94cc-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c94cc-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="c94cc-117">-Name</span></span>
<span data-ttu-id="c94cc-118">指定此 Cmdlet 所取得之排程的名稱。</span><span class="sxs-lookup"><span data-stu-id="c94cc-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c94cc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c94cc-119">-ResourceGroupName</span></span>
<span data-ttu-id="c94cc-120">指定此 Cmdlet 取得排程之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c94cc-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="c94cc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c94cc-121">CommonParameters</span></span>
<span data-ttu-id="c94cc-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c94cc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c94cc-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c94cc-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c94cc-124">輸入</span><span class="sxs-lookup"><span data-stu-id="c94cc-124">INPUTS</span></span>

### <span data-ttu-id="c94cc-125">System.object</span><span class="sxs-lookup"><span data-stu-id="c94cc-125">System.String</span></span>

## <span data-ttu-id="c94cc-126">輸出</span><span class="sxs-lookup"><span data-stu-id="c94cc-126">OUTPUTS</span></span>

### <span data-ttu-id="c94cc-127">[-Azure. 命令. 自動化. 模型]。排程</span><span class="sxs-lookup"><span data-stu-id="c94cc-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="c94cc-128">筆記</span><span class="sxs-lookup"><span data-stu-id="c94cc-128">NOTES</span></span>

## <span data-ttu-id="c94cc-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="c94cc-129">RELATED LINKS</span></span>

[<span data-ttu-id="c94cc-130">新-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="c94cc-130">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="c94cc-131">移除-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="c94cc-131">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="c94cc-132">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="c94cc-132">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)

