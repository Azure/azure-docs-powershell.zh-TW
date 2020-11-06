---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
ms.openlocfilehash: 78e34c5d3d94a964fbff6d0cbaa74c9dd3dd2177
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452879"
---
# <span data-ttu-id="0a9ab-101">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="0a9ab-101">Get-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="0a9ab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0a9ab-102">SYNOPSIS</span></span>
<span data-ttu-id="0a9ab-103">取得自動化排程。</span><span class="sxs-lookup"><span data-stu-id="0a9ab-103">Gets an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a9ab-104">句法</span><span class="sxs-lookup"><span data-stu-id="0a9ab-104">SYNTAX</span></span>

### <span data-ttu-id="0a9ab-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="0a9ab-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a9ab-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0a9ab-106">ByName</span></span>
```
Get-AzureRmAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a9ab-107">說明</span><span class="sxs-lookup"><span data-stu-id="0a9ab-107">DESCRIPTION</span></span>
<span data-ttu-id="0a9ab-108">**AzureRmAutomationSchedule** Cmdlet 會取得 Azure 自動化排程。</span><span class="sxs-lookup"><span data-stu-id="0a9ab-108">The **Get-AzureRmAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="0a9ab-109">示例</span><span class="sxs-lookup"><span data-stu-id="0a9ab-109">EXAMPLES</span></span>

### <span data-ttu-id="0a9ab-110">範例1：取得排程</span><span class="sxs-lookup"><span data-stu-id="0a9ab-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0a9ab-111">這個命令會取得名為 DailySchedule08 的排程。</span><span class="sxs-lookup"><span data-stu-id="0a9ab-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="0a9ab-112">參數</span><span class="sxs-lookup"><span data-stu-id="0a9ab-112">PARAMETERS</span></span>

### <span data-ttu-id="0a9ab-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0a9ab-113">-AutomationAccountName</span></span>
<span data-ttu-id="0a9ab-114">指定此 Cmdlet 取得排程之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a9ab-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="0a9ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a9ab-115">-DefaultProfile</span></span>
<span data-ttu-id="0a9ab-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0a9ab-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a9ab-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="0a9ab-117">-Name</span></span>
<span data-ttu-id="0a9ab-118">指定此 Cmdlet 所取得之排程的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a9ab-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0a9ab-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a9ab-119">-ResourceGroupName</span></span>
<span data-ttu-id="0a9ab-120">指定此 Cmdlet 取得排程之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a9ab-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="0a9ab-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a9ab-121">CommonParameters</span></span>
<span data-ttu-id="0a9ab-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0a9ab-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a9ab-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0a9ab-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a9ab-124">輸入</span><span class="sxs-lookup"><span data-stu-id="0a9ab-124">INPUTS</span></span>

### <span data-ttu-id="0a9ab-125">System.object</span><span class="sxs-lookup"><span data-stu-id="0a9ab-125">System.String</span></span>

## <span data-ttu-id="0a9ab-126">輸出</span><span class="sxs-lookup"><span data-stu-id="0a9ab-126">OUTPUTS</span></span>

### <span data-ttu-id="0a9ab-127">[-Azure. 命令. 自動化. 模型]。排程</span><span class="sxs-lookup"><span data-stu-id="0a9ab-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="0a9ab-128">筆記</span><span class="sxs-lookup"><span data-stu-id="0a9ab-128">NOTES</span></span>

## <span data-ttu-id="0a9ab-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a9ab-129">RELATED LINKS</span></span>

[<span data-ttu-id="0a9ab-130">新-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="0a9ab-130">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="0a9ab-131">移除-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="0a9ab-131">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="0a9ab-132">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="0a9ab-132">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


