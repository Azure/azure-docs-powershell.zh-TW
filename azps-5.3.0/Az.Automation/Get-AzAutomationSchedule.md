---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
ms.openlocfilehash: a07208db434a43730b75542bb0f8959ae68423d1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447320"
---
# <span data-ttu-id="160dd-101">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="160dd-101">Get-AzAutomationSchedule</span></span>

## <span data-ttu-id="160dd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="160dd-102">SYNOPSIS</span></span>
<span data-ttu-id="160dd-103">取得自動化排程。</span><span class="sxs-lookup"><span data-stu-id="160dd-103">Gets an Automation schedule.</span></span>

## <span data-ttu-id="160dd-104">句法</span><span class="sxs-lookup"><span data-stu-id="160dd-104">SYNTAX</span></span>

### <span data-ttu-id="160dd-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="160dd-105">ByAll (Default)</span></span>
```
Get-AzAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="160dd-106">ByName</span><span class="sxs-lookup"><span data-stu-id="160dd-106">ByName</span></span>
```
Get-AzAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="160dd-107">說明</span><span class="sxs-lookup"><span data-stu-id="160dd-107">DESCRIPTION</span></span>
<span data-ttu-id="160dd-108">**AzAutomationSchedule** Cmdlet 會取得 Azure 自動化排程。</span><span class="sxs-lookup"><span data-stu-id="160dd-108">The **Get-AzAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="160dd-109">示例</span><span class="sxs-lookup"><span data-stu-id="160dd-109">EXAMPLES</span></span>

### <span data-ttu-id="160dd-110">範例1：取得排程</span><span class="sxs-lookup"><span data-stu-id="160dd-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="160dd-111">這個命令會取得名為 DailySchedule08 的排程。</span><span class="sxs-lookup"><span data-stu-id="160dd-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="160dd-112">參數</span><span class="sxs-lookup"><span data-stu-id="160dd-112">PARAMETERS</span></span>

### <span data-ttu-id="160dd-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="160dd-113">-AutomationAccountName</span></span>
<span data-ttu-id="160dd-114">指定此 Cmdlet 取得排程之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="160dd-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="160dd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="160dd-115">-DefaultProfile</span></span>
<span data-ttu-id="160dd-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="160dd-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="160dd-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="160dd-117">-Name</span></span>
<span data-ttu-id="160dd-118">指定此 Cmdlet 所取得之排程的名稱。</span><span class="sxs-lookup"><span data-stu-id="160dd-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

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

### <span data-ttu-id="160dd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="160dd-119">-ResourceGroupName</span></span>
<span data-ttu-id="160dd-120">指定此 Cmdlet 取得排程之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="160dd-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="160dd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="160dd-121">CommonParameters</span></span>
<span data-ttu-id="160dd-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="160dd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="160dd-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="160dd-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="160dd-124">輸入</span><span class="sxs-lookup"><span data-stu-id="160dd-124">INPUTS</span></span>

### <span data-ttu-id="160dd-125">System.object</span><span class="sxs-lookup"><span data-stu-id="160dd-125">System.String</span></span>

## <span data-ttu-id="160dd-126">輸出</span><span class="sxs-lookup"><span data-stu-id="160dd-126">OUTPUTS</span></span>

### <span data-ttu-id="160dd-127">[-Azure. 命令. 自動化. 模型]。排程</span><span class="sxs-lookup"><span data-stu-id="160dd-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="160dd-128">筆記</span><span class="sxs-lookup"><span data-stu-id="160dd-128">NOTES</span></span>

## <span data-ttu-id="160dd-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="160dd-129">RELATED LINKS</span></span>

[<span data-ttu-id="160dd-130">新-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="160dd-130">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="160dd-131">移除-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="160dd-131">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="160dd-132">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="160dd-132">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


