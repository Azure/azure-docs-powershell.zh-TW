---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
ms.openlocfilehash: a32b86ce308f18537ec1acda62c2694e7b621d5c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917477"
---
# <span data-ttu-id="2fe8d-101">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="2fe8d-101">Get-AzAutomationSchedule</span></span>

## <span data-ttu-id="2fe8d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2fe8d-102">SYNOPSIS</span></span>
<span data-ttu-id="2fe8d-103">獲得自動化排程。</span><span class="sxs-lookup"><span data-stu-id="2fe8d-103">Gets an Automation schedule.</span></span>

## <span data-ttu-id="2fe8d-104">語法</span><span class="sxs-lookup"><span data-stu-id="2fe8d-104">SYNTAX</span></span>

### <span data-ttu-id="2fe8d-105">根據預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="2fe8d-105">ByAll (Default)</span></span>
```
Get-AzAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fe8d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2fe8d-106">ByName</span></span>
```
Get-AzAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fe8d-107">描述</span><span class="sxs-lookup"><span data-stu-id="2fe8d-107">DESCRIPTION</span></span>
<span data-ttu-id="2fe8d-108">**Get-AzAutomationSchedule** Cmdlet 會取得 Azure 自動化排程。</span><span class="sxs-lookup"><span data-stu-id="2fe8d-108">The **Get-AzAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="2fe8d-109">例子</span><span class="sxs-lookup"><span data-stu-id="2fe8d-109">EXAMPLES</span></span>

### <span data-ttu-id="2fe8d-110">範例 1：取得排程</span><span class="sxs-lookup"><span data-stu-id="2fe8d-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2fe8d-111">此命令會獲得名為 DailySchedule08 的排程。</span><span class="sxs-lookup"><span data-stu-id="2fe8d-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="2fe8d-112">參數</span><span class="sxs-lookup"><span data-stu-id="2fe8d-112">PARAMETERS</span></span>

### <span data-ttu-id="2fe8d-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2fe8d-113">-AutomationAccountName</span></span>
<span data-ttu-id="2fe8d-114">指定此 Cmdlet 取得排程的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="2fe8d-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="2fe8d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fe8d-115">-DefaultProfile</span></span>
<span data-ttu-id="2fe8d-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="2fe8d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2fe8d-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="2fe8d-117">-Name</span></span>
<span data-ttu-id="2fe8d-118">指定此 Cmdlet 所獲得排程的名稱。</span><span class="sxs-lookup"><span data-stu-id="2fe8d-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2fe8d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fe8d-119">-ResourceGroupName</span></span>
<span data-ttu-id="2fe8d-120">指定此 Cmdlet 會獲得排程的資源組名。</span><span class="sxs-lookup"><span data-stu-id="2fe8d-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="2fe8d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fe8d-121">CommonParameters</span></span>
<span data-ttu-id="2fe8d-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2fe8d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fe8d-123">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2fe8d-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fe8d-124">輸入</span><span class="sxs-lookup"><span data-stu-id="2fe8d-124">INPUTS</span></span>

### <span data-ttu-id="2fe8d-125">System.String</span><span class="sxs-lookup"><span data-stu-id="2fe8d-125">System.String</span></span>

## <span data-ttu-id="2fe8d-126">輸出</span><span class="sxs-lookup"><span data-stu-id="2fe8d-126">OUTPUTS</span></span>

### <span data-ttu-id="2fe8d-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span><span class="sxs-lookup"><span data-stu-id="2fe8d-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="2fe8d-128">筆記</span><span class="sxs-lookup"><span data-stu-id="2fe8d-128">NOTES</span></span>

## <span data-ttu-id="2fe8d-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="2fe8d-129">RELATED LINKS</span></span>

[<span data-ttu-id="2fe8d-130">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="2fe8d-130">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="2fe8d-131">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="2fe8d-131">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="2fe8d-132">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="2fe8d-132">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


