---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6429C564-1995-4D9B-BF9B-963B4F5FB3BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationSchedule.md
ms.openlocfilehash: c5f7348d59b18a3e0cedfcf52c22c4328c28944a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622943"
---
# <span data-ttu-id="47b3c-101">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="47b3c-101">Set-AzAutomationSchedule</span></span>

## <span data-ttu-id="47b3c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="47b3c-102">SYNOPSIS</span></span>
<span data-ttu-id="47b3c-103">修改自動化排程。</span><span class="sxs-lookup"><span data-stu-id="47b3c-103">Modifies an Automation schedule.</span></span>

## <span data-ttu-id="47b3c-104">句法</span><span class="sxs-lookup"><span data-stu-id="47b3c-104">SYNTAX</span></span>

```
Set-AzAutomationSchedule [-Name] <String> [-IsEnabled <Boolean>] [-Description <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="47b3c-105">說明</span><span class="sxs-lookup"><span data-stu-id="47b3c-105">DESCRIPTION</span></span>
<span data-ttu-id="47b3c-106">**AzAutomationSchedule** Cmdlet 會修改 Azure 自動化中的排程。</span><span class="sxs-lookup"><span data-stu-id="47b3c-106">The **Set-AzAutomationSchedule** cmdlet modifies a schedule in Azure Automation.</span></span>

## <span data-ttu-id="47b3c-107">示例</span><span class="sxs-lookup"><span data-stu-id="47b3c-107">EXAMPLES</span></span>

### <span data-ttu-id="47b3c-108">範例1：修改排程</span><span class="sxs-lookup"><span data-stu-id="47b3c-108">Example 1: Modify a schedule</span></span>
```
PS C:\>Set-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="47b3c-109">這個命令會修改名為 Schedule01 的排程的描述。</span><span class="sxs-lookup"><span data-stu-id="47b3c-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="47b3c-110">參數</span><span class="sxs-lookup"><span data-stu-id="47b3c-110">PARAMETERS</span></span>

### <span data-ttu-id="47b3c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="47b3c-111">-AutomationAccountName</span></span>
<span data-ttu-id="47b3c-112">指定此 Cmdlet 修改排程的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="47b3c-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="47b3c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47b3c-113">-DefaultProfile</span></span>
<span data-ttu-id="47b3c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="47b3c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47b3c-115">-描述</span><span class="sxs-lookup"><span data-stu-id="47b3c-115">-Description</span></span>
<span data-ttu-id="47b3c-116">指定排程的描述。</span><span class="sxs-lookup"><span data-stu-id="47b3c-116">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="47b3c-117">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="47b3c-117">-IsEnabled</span></span>
<span data-ttu-id="47b3c-118">指定此 Cmdlet 是否啟用排程。</span><span class="sxs-lookup"><span data-stu-id="47b3c-118">Specifies whether this cmdlet enables the schedule.</span></span>

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

### <span data-ttu-id="47b3c-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="47b3c-119">-Name</span></span>
<span data-ttu-id="47b3c-120">指定此 Cmdlet 所修改之排程的名稱。</span><span class="sxs-lookup"><span data-stu-id="47b3c-120">Specifies the name for the schedule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="47b3c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47b3c-121">-ResourceGroupName</span></span>
<span data-ttu-id="47b3c-122">指定此 Cmdlet 修改排程之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="47b3c-122">Specifies the name of a resource group for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="47b3c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47b3c-123">CommonParameters</span></span>
<span data-ttu-id="47b3c-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="47b3c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47b3c-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="47b3c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47b3c-126">輸入</span><span class="sxs-lookup"><span data-stu-id="47b3c-126">INPUTS</span></span>

### <span data-ttu-id="47b3c-127">System.object</span><span class="sxs-lookup"><span data-stu-id="47b3c-127">System.String</span></span>

### <span data-ttu-id="47b3c-128">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="47b3c-128">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="47b3c-129">輸出</span><span class="sxs-lookup"><span data-stu-id="47b3c-129">OUTPUTS</span></span>

### <span data-ttu-id="47b3c-130">[-Azure. 命令. 自動化. 模型]。排程</span><span class="sxs-lookup"><span data-stu-id="47b3c-130">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="47b3c-131">筆記</span><span class="sxs-lookup"><span data-stu-id="47b3c-131">NOTES</span></span>

## <span data-ttu-id="47b3c-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="47b3c-132">RELATED LINKS</span></span>

[<span data-ttu-id="47b3c-133">AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="47b3c-133">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="47b3c-134">新-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="47b3c-134">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="47b3c-135">移除-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="47b3c-135">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)


