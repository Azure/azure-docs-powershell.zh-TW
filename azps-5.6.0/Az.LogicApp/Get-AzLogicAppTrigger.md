---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5307F1F1-E84C-4949-A557-99EF0012C3DF
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapptrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTrigger.md
ms.openlocfilehash: 28a7cd76f03dd3b6d2fc79e5d0b8d4d963a7f55c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916542"
---
# <span data-ttu-id="79aa3-101">Get-AzLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="79aa3-101">Get-AzLogicAppTrigger</span></span>

## <span data-ttu-id="79aa3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="79aa3-102">SYNOPSIS</span></span>
<span data-ttu-id="79aa3-103">獲得邏輯應用程式的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="79aa3-103">Gets the triggers of a logic app.</span></span>

## <span data-ttu-id="79aa3-104">語法</span><span class="sxs-lookup"><span data-stu-id="79aa3-104">SYNTAX</span></span>

```
Get-AzLogicAppTrigger -ResourceGroupName <String> -Name <String> [-TriggerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79aa3-105">描述</span><span class="sxs-lookup"><span data-stu-id="79aa3-105">DESCRIPTION</span></span>
<span data-ttu-id="79aa3-106">**Get-AzLogicAppTrigger Cmdlet** 會從邏輯應用程式觸發程式。</span><span class="sxs-lookup"><span data-stu-id="79aa3-106">The **Get-AzLogicAppTrigger** cmdlet gets triggers from a logic app.</span></span>
<span data-ttu-id="79aa3-107">此 Cmdlet 會返回 **WorkflowTrigger 物件** 。</span><span class="sxs-lookup"><span data-stu-id="79aa3-107">This cmdlet returns a **WorkflowTrigger** object.</span></span>
<span data-ttu-id="79aa3-108">指定工作流程、資源群組和觸發。</span><span class="sxs-lookup"><span data-stu-id="79aa3-108">Specify the workflow, resource group, and trigger.</span></span>
<span data-ttu-id="79aa3-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="79aa3-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="79aa3-110">若要使用動態參數，請于命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="79aa3-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="79aa3-111">若要探索動態參數的名稱，在 Cmdlet 名稱之後輸入連字號 (-) ，然後重複按 Tab 鍵以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="79aa3-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="79aa3-112">如果您省略必要的範本參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="79aa3-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="79aa3-113">例子</span><span class="sxs-lookup"><span data-stu-id="79aa3-113">EXAMPLES</span></span>

### <span data-ttu-id="79aa3-114">範例 1：取得邏輯應用程式的觸發程式</span><span class="sxs-lookup"><span data-stu-id="79aa3-114">Example 1: Get a trigger of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -TriggerName "Trigger01"
ChangedTime         : 1/14/2016 11:45:07 AM
CreatedTime         : 1/13/2016 2:42:26 PM
LastExecutionTime   : 1/14/2016 11:45:07 AM
Name                : Trigger01
NextExecutionTime   : 1/14/2016 12:45:07 PM
RecurrenceFrequency : Minute
RecurrenceInterval  : 60
Status              : Waiting
Type                : Microsoft.Logic/workflows/triggers
LogicAppName        : LogicApp05
LogicAppVersion     : 08587489107406290826
```

<span data-ttu-id="79aa3-115">此命令會從名為 LogicApp05 的邏輯應用程式獲得名為 Trigger01 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="79aa3-115">This command gets the trigger named Trigger01 from the logic app named LogicApp05.</span></span>

### <span data-ttu-id="79aa3-116">範例 2：取得邏輯應用程式的所有觸發程式</span><span class="sxs-lookup"><span data-stu-id="79aa3-116">Example 2: Get all triggers of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp07"
ChangedTime         : 1/14/2016 11:45:07 AM
CreatedTime         : 1/13/2016 2:42:26 PM
LastExecutionTime   : 1/14/2016 11:45:07 AM
Name                : Trigger02
NextExecutionTime   : 1/14/2016 12:45:07 PM
RecurrenceFrequency : Minute
RecurrenceInterval  : 60
Status              : Waiting
Type                : Microsoft.Logic/workflows/triggers
LogicAppName        : LogicApp07
LogicAppVersion     : 08587489107406290826
```

<span data-ttu-id="79aa3-117">此命令會觸發名為 LogicApp07 的邏輯應用程式。</span><span class="sxs-lookup"><span data-stu-id="79aa3-117">This command gets the triggers of the logic app named LogicApp07.</span></span>

## <span data-ttu-id="79aa3-118">參數</span><span class="sxs-lookup"><span data-stu-id="79aa3-118">PARAMETERS</span></span>

### <span data-ttu-id="79aa3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79aa3-119">-DefaultProfile</span></span>
<span data-ttu-id="79aa3-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="79aa3-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79aa3-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="79aa3-121">-Name</span></span>
<span data-ttu-id="79aa3-122">指定此 Cmdlet 可觸發的邏輯應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="79aa3-122">Specifies the name of the logic app from which this cmdlet gets a trigger.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79aa3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79aa3-123">-ResourceGroupName</span></span>
<span data-ttu-id="79aa3-124">指定此 Cmdlet 可觸發之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="79aa3-124">Specifies the name of a resource group in which this cmdlet gets a trigger.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79aa3-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="79aa3-125">-TriggerName</span></span>
<span data-ttu-id="79aa3-126">指定此 Cmdlet 所獲取的觸發名稱。</span><span class="sxs-lookup"><span data-stu-id="79aa3-126">Specifies the name of the trigger that this cmdlet gets.</span></span>

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

### <span data-ttu-id="79aa3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79aa3-127">CommonParameters</span></span>
<span data-ttu-id="79aa3-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="79aa3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79aa3-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="79aa3-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79aa3-130">輸入</span><span class="sxs-lookup"><span data-stu-id="79aa3-130">INPUTS</span></span>

### <span data-ttu-id="79aa3-131">System.String</span><span class="sxs-lookup"><span data-stu-id="79aa3-131">System.String</span></span>

## <span data-ttu-id="79aa3-132">輸出</span><span class="sxs-lookup"><span data-stu-id="79aa3-132">OUTPUTS</span></span>

### <span data-ttu-id="79aa3-133">Microsoft.Azure.management.Logic.models.WorkflowTrigger</span><span class="sxs-lookup"><span data-stu-id="79aa3-133">Microsoft.Azure.Management.Logic.Models.WorkflowTrigger</span></span>

## <span data-ttu-id="79aa3-134">筆記</span><span class="sxs-lookup"><span data-stu-id="79aa3-134">NOTES</span></span>

## <span data-ttu-id="79aa3-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="79aa3-135">RELATED LINKS</span></span>

[<span data-ttu-id="79aa3-136">Get-AzLogicAppTritoryHistory</span><span class="sxs-lookup"><span data-stu-id="79aa3-136">Get-AzLogicAppTriggerHistory</span></span>](./Get-AzLogicAppTriggerHistory.md)

[<span data-ttu-id="79aa3-137">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="79aa3-137">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


