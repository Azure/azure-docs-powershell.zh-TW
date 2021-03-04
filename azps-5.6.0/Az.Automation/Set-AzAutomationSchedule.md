---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6429C564-1995-4D9B-BF9B-963B4F5FB3BD
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationSchedule.md
ms.openlocfilehash: b1eaa41ed238f3b91c68c6bdd28ba259888d7244
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915629"
---
# <span data-ttu-id="e1cc9-101">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="e1cc9-101">Set-AzAutomationSchedule</span></span>

## <span data-ttu-id="e1cc9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e1cc9-102">SYNOPSIS</span></span>
<span data-ttu-id="e1cc9-103">修改自動化排程。</span><span class="sxs-lookup"><span data-stu-id="e1cc9-103">Modifies an Automation schedule.</span></span>

## <span data-ttu-id="e1cc9-104">語法</span><span class="sxs-lookup"><span data-stu-id="e1cc9-104">SYNTAX</span></span>

```
Set-AzAutomationSchedule [-Name] <String> [-IsEnabled <Boolean>] [-Description <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1cc9-105">描述</span><span class="sxs-lookup"><span data-stu-id="e1cc9-105">DESCRIPTION</span></span>
<span data-ttu-id="e1cc9-106">**Set-AzAutomationSchedule** Cmdlet 會修改 Azure Automation 中的排程。</span><span class="sxs-lookup"><span data-stu-id="e1cc9-106">The **Set-AzAutomationSchedule** cmdlet modifies a schedule in Azure Automation.</span></span>

## <span data-ttu-id="e1cc9-107">例子</span><span class="sxs-lookup"><span data-stu-id="e1cc9-107">EXAMPLES</span></span>

### <span data-ttu-id="e1cc9-108">範例 1：修改排程</span><span class="sxs-lookup"><span data-stu-id="e1cc9-108">Example 1: Modify a schedule</span></span>
```
PS C:\>Set-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e1cc9-109">此命令會修改名為 Schedule01 的排程描述。</span><span class="sxs-lookup"><span data-stu-id="e1cc9-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="e1cc9-110">參數</span><span class="sxs-lookup"><span data-stu-id="e1cc9-110">PARAMETERS</span></span>

### <span data-ttu-id="e1cc9-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e1cc9-111">-AutomationAccountName</span></span>
<span data-ttu-id="e1cc9-112">指定此 Cmdlet 修改排程的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="e1cc9-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="e1cc9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1cc9-113">-DefaultProfile</span></span>
<span data-ttu-id="e1cc9-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="e1cc9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1cc9-115">-描述</span><span class="sxs-lookup"><span data-stu-id="e1cc9-115">-Description</span></span>
<span data-ttu-id="e1cc9-116">指定排程的描述。</span><span class="sxs-lookup"><span data-stu-id="e1cc9-116">Specifies a description for the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1cc9-117">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="e1cc9-117">-IsEnabled</span></span>
<span data-ttu-id="e1cc9-118">指定此 Cmdlet 是否啟用排程。</span><span class="sxs-lookup"><span data-stu-id="e1cc9-118">Specifies whether this cmdlet enables the schedule.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1cc9-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="e1cc9-119">-Name</span></span>
<span data-ttu-id="e1cc9-120">指定此 Cmdlet 修改之排程的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1cc9-120">Specifies the name for the schedule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e1cc9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1cc9-121">-ResourceGroupName</span></span>
<span data-ttu-id="e1cc9-122">指定此 Cmdlet 修改排程的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e1cc9-122">Specifies the name of a resource group for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="e1cc9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1cc9-123">CommonParameters</span></span>
<span data-ttu-id="e1cc9-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e1cc9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1cc9-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e1cc9-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1cc9-126">輸入</span><span class="sxs-lookup"><span data-stu-id="e1cc9-126">INPUTS</span></span>

### <span data-ttu-id="e1cc9-127">System.String</span><span class="sxs-lookup"><span data-stu-id="e1cc9-127">System.String</span></span>

### <span data-ttu-id="e1cc9-128">System.Nullable'1[[System.Boolean， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e1cc9-128">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e1cc9-129">輸出</span><span class="sxs-lookup"><span data-stu-id="e1cc9-129">OUTPUTS</span></span>

### <span data-ttu-id="e1cc9-130">Microsoft.Azure.Commands.Automation.Model.Schedule</span><span class="sxs-lookup"><span data-stu-id="e1cc9-130">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="e1cc9-131">筆記</span><span class="sxs-lookup"><span data-stu-id="e1cc9-131">NOTES</span></span>

## <span data-ttu-id="e1cc9-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1cc9-132">RELATED LINKS</span></span>

[<span data-ttu-id="e1cc9-133">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="e1cc9-133">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="e1cc9-134">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="e1cc9-134">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="e1cc9-135">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="e1cc9-135">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)


