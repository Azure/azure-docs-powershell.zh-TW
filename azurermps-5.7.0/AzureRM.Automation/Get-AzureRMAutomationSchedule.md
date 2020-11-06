---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
ms.openlocfilehash: 2b35281cd276be9149f2d4c4e17cb38f48eadc25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454771"
---
# <span data-ttu-id="c8489-101">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="c8489-101">Get-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="c8489-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c8489-102">SYNOPSIS</span></span>
<span data-ttu-id="c8489-103">取得自動化排程。</span><span class="sxs-lookup"><span data-stu-id="c8489-103">Gets an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8489-104">句法</span><span class="sxs-lookup"><span data-stu-id="c8489-104">SYNTAX</span></span>

### <span data-ttu-id="c8489-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="c8489-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8489-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c8489-106">ByName</span></span>
```
Get-AzureRmAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8489-107">說明</span><span class="sxs-lookup"><span data-stu-id="c8489-107">DESCRIPTION</span></span>
<span data-ttu-id="c8489-108">**AzureRmAutomationSchedule** Cmdlet 會取得 Azure 自動化排程。</span><span class="sxs-lookup"><span data-stu-id="c8489-108">The **Get-AzureRmAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="c8489-109">示例</span><span class="sxs-lookup"><span data-stu-id="c8489-109">EXAMPLES</span></span>

### <span data-ttu-id="c8489-110">範例1：取得排程</span><span class="sxs-lookup"><span data-stu-id="c8489-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c8489-111">這個命令會取得名為 DailySchedule08 的排程。</span><span class="sxs-lookup"><span data-stu-id="c8489-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="c8489-112">參數</span><span class="sxs-lookup"><span data-stu-id="c8489-112">PARAMETERS</span></span>

### <span data-ttu-id="c8489-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c8489-113">-AutomationAccountName</span></span>
<span data-ttu-id="c8489-114">指定此 Cmdlet 取得排程之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8489-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="c8489-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8489-115">-DefaultProfile</span></span>
<span data-ttu-id="c8489-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c8489-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8489-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="c8489-117">-Name</span></span>
<span data-ttu-id="c8489-118">指定此 Cmdlet 所取得之排程的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8489-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8489-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8489-119">-ResourceGroupName</span></span>
<span data-ttu-id="c8489-120">指定此 Cmdlet 取得排程之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8489-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="c8489-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8489-121">CommonParameters</span></span>
<span data-ttu-id="c8489-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c8489-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8489-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c8489-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8489-124">輸入</span><span class="sxs-lookup"><span data-stu-id="c8489-124">INPUTS</span></span>

### <span data-ttu-id="c8489-125">所有</span><span class="sxs-lookup"><span data-stu-id="c8489-125">None</span></span>
<span data-ttu-id="c8489-126">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="c8489-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c8489-127">輸出</span><span class="sxs-lookup"><span data-stu-id="c8489-127">OUTPUTS</span></span>

### <span data-ttu-id="c8489-128">[-Azure. 命令. 自動化. 模型]。排程</span><span class="sxs-lookup"><span data-stu-id="c8489-128">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="c8489-129">筆記</span><span class="sxs-lookup"><span data-stu-id="c8489-129">NOTES</span></span>

## <span data-ttu-id="c8489-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8489-130">RELATED LINKS</span></span>

[<span data-ttu-id="c8489-131">新-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="c8489-131">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="c8489-132">移除-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="c8489-132">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="c8489-133">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="c8489-133">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


