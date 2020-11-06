---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6429C564-1995-4D9B-BF9B-963B4F5FB3BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationSchedule.md
ms.openlocfilehash: b311554fa5aeeae67829055506b85766fd6f9670
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450743"
---
# <span data-ttu-id="0ad0a-101">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="0ad0a-101">Set-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="0ad0a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0ad0a-102">SYNOPSIS</span></span>
<span data-ttu-id="0ad0a-103">修改自動化排程。</span><span class="sxs-lookup"><span data-stu-id="0ad0a-103">Modifies an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ad0a-104">句法</span><span class="sxs-lookup"><span data-stu-id="0ad0a-104">SYNTAX</span></span>

```
Set-AzureRmAutomationSchedule [-Name] <String> [-IsEnabled <Boolean>] [-Description <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ad0a-105">說明</span><span class="sxs-lookup"><span data-stu-id="0ad0a-105">DESCRIPTION</span></span>
<span data-ttu-id="0ad0a-106">**AzureRmAutomationSchedule** Cmdlet 會修改 Azure 自動化中的排程。</span><span class="sxs-lookup"><span data-stu-id="0ad0a-106">The **Set-AzureRmAutomationSchedule** cmdlet modifies a schedule in Azure Automation.</span></span>

## <span data-ttu-id="0ad0a-107">示例</span><span class="sxs-lookup"><span data-stu-id="0ad0a-107">EXAMPLES</span></span>

### <span data-ttu-id="0ad0a-108">範例1：修改排程</span><span class="sxs-lookup"><span data-stu-id="0ad0a-108">Example 1: Modify a schedule</span></span>
```
PS C:\>Set-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0ad0a-109">這個命令會修改名為 Schedule01 的排程的描述。</span><span class="sxs-lookup"><span data-stu-id="0ad0a-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="0ad0a-110">參數</span><span class="sxs-lookup"><span data-stu-id="0ad0a-110">PARAMETERS</span></span>

### <span data-ttu-id="0ad0a-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0ad0a-111">-AutomationAccountName</span></span>
<span data-ttu-id="0ad0a-112">指定此 Cmdlet 修改排程的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="0ad0a-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="0ad0a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ad0a-113">-DefaultProfile</span></span>
<span data-ttu-id="0ad0a-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0ad0a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ad0a-115">-描述</span><span class="sxs-lookup"><span data-stu-id="0ad0a-115">-Description</span></span>
<span data-ttu-id="0ad0a-116">指定排程的描述。</span><span class="sxs-lookup"><span data-stu-id="0ad0a-116">Specifies a description for the schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad0a-117">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="0ad0a-117">-IsEnabled</span></span>
<span data-ttu-id="0ad0a-118">指定此 Cmdlet 是否啟用排程。</span><span class="sxs-lookup"><span data-stu-id="0ad0a-118">Specifies whether this cmdlet enables the schedule.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad0a-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="0ad0a-119">-Name</span></span>
<span data-ttu-id="0ad0a-120">指定此 Cmdlet 所修改之排程的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ad0a-120">Specifies the name for the schedule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0ad0a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ad0a-121">-ResourceGroupName</span></span>
<span data-ttu-id="0ad0a-122">指定此 Cmdlet 修改排程之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ad0a-122">Specifies the name of a resource group for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="0ad0a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ad0a-123">CommonParameters</span></span>
<span data-ttu-id="0ad0a-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0ad0a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ad0a-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0ad0a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ad0a-126">輸入</span><span class="sxs-lookup"><span data-stu-id="0ad0a-126">INPUTS</span></span>

### <span data-ttu-id="0ad0a-127">所有</span><span class="sxs-lookup"><span data-stu-id="0ad0a-127">None</span></span>
<span data-ttu-id="0ad0a-128">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="0ad0a-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0ad0a-129">輸出</span><span class="sxs-lookup"><span data-stu-id="0ad0a-129">OUTPUTS</span></span>

### <span data-ttu-id="0ad0a-130">[-Azure. 命令. 自動化. 模型]。排程</span><span class="sxs-lookup"><span data-stu-id="0ad0a-130">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="0ad0a-131">筆記</span><span class="sxs-lookup"><span data-stu-id="0ad0a-131">NOTES</span></span>

## <span data-ttu-id="0ad0a-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="0ad0a-132">RELATED LINKS</span></span>

[<span data-ttu-id="0ad0a-133">AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="0ad0a-133">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="0ad0a-134">新-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="0ad0a-134">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="0ad0a-135">移除-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="0ad0a-135">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)


