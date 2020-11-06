---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5307F1F1-E84C-4949-A557-99EF0012C3DF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapptrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTrigger.md
ms.openlocfilehash: 6066a08774be9f5e3fa67a07b0d868947384f518
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455271"
---
# <span data-ttu-id="08e56-101">Get-AzureRmLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="08e56-101">Get-AzureRmLogicAppTrigger</span></span>

## <span data-ttu-id="08e56-102">摘要</span><span class="sxs-lookup"><span data-stu-id="08e56-102">SYNOPSIS</span></span>
<span data-ttu-id="08e56-103">取得邏輯 app 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="08e56-103">Gets the triggers of a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08e56-104">句法</span><span class="sxs-lookup"><span data-stu-id="08e56-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppTrigger -ResourceGroupName <String> -Name <String> [-TriggerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08e56-105">說明</span><span class="sxs-lookup"><span data-stu-id="08e56-105">DESCRIPTION</span></span>
<span data-ttu-id="08e56-106">**AzureRmLogicAppTrigger** Cmdlet 會從邏輯 app 取得觸發程式。</span><span class="sxs-lookup"><span data-stu-id="08e56-106">The **Get-AzureRmLogicAppTrigger** cmdlet gets triggers from a logic app.</span></span>
<span data-ttu-id="08e56-107">這個 Cmdlet 會傳回 **WorkflowTrigger** 物件。</span><span class="sxs-lookup"><span data-stu-id="08e56-107">This cmdlet returns a **WorkflowTrigger** object.</span></span>
<span data-ttu-id="08e56-108">指定工作流程、資源群組及觸發程式。</span><span class="sxs-lookup"><span data-stu-id="08e56-108">Specify the workflow, resource group, and trigger.</span></span>
<span data-ttu-id="08e56-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="08e56-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="08e56-110">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="08e56-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="08e56-111">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="08e56-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="08e56-112">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="08e56-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="08e56-113">示例</span><span class="sxs-lookup"><span data-stu-id="08e56-113">EXAMPLES</span></span>

### <span data-ttu-id="08e56-114">範例1：取得邏輯 app 的觸發程式</span><span class="sxs-lookup"><span data-stu-id="08e56-114">Example 1: Get a trigger of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -TriggerName "Trigger01"
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

<span data-ttu-id="08e56-115">這個命令會從名為 LogicApp05 的邏輯 app 取得名為 Trigger01 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="08e56-115">This command gets the trigger named Trigger01 from the logic app named LogicApp05.</span></span>

### <span data-ttu-id="08e56-116">範例2：取得邏輯 app 的所有觸發程式</span><span class="sxs-lookup"><span data-stu-id="08e56-116">Example 2: Get all triggers of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp07"
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

<span data-ttu-id="08e56-117">這個命令會取得名為 LogicApp07 的邏輯 app 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="08e56-117">This command gets the triggers of the logic app named LogicApp07.</span></span>

## <span data-ttu-id="08e56-118">參數</span><span class="sxs-lookup"><span data-stu-id="08e56-118">PARAMETERS</span></span>

### <span data-ttu-id="08e56-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08e56-119">-DefaultProfile</span></span>
<span data-ttu-id="08e56-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="08e56-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08e56-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="08e56-121">-Name</span></span>
<span data-ttu-id="08e56-122">指定這個 Cmdlet 取得觸發程式的邏輯 app 名稱。</span><span class="sxs-lookup"><span data-stu-id="08e56-122">Specifies the name of the logic app from which this cmdlet gets a trigger.</span></span>

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

### <span data-ttu-id="08e56-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08e56-123">-ResourceGroupName</span></span>
<span data-ttu-id="08e56-124">指定此 Cmdlet 取得觸發程式之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="08e56-124">Specifies the name of a resource group in which this cmdlet gets a trigger.</span></span>

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

### <span data-ttu-id="08e56-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="08e56-125">-TriggerName</span></span>
<span data-ttu-id="08e56-126">指定此 Cmdlet 所取得之觸發程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="08e56-126">Specifies the name of the trigger that this cmdlet gets.</span></span>

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

### <span data-ttu-id="08e56-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08e56-127">CommonParameters</span></span>
<span data-ttu-id="08e56-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="08e56-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08e56-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="08e56-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08e56-130">輸入</span><span class="sxs-lookup"><span data-stu-id="08e56-130">INPUTS</span></span>

### <span data-ttu-id="08e56-131">System.object</span><span class="sxs-lookup"><span data-stu-id="08e56-131">System.String</span></span>

## <span data-ttu-id="08e56-132">輸出</span><span class="sxs-lookup"><span data-stu-id="08e56-132">OUTPUTS</span></span>

### <span data-ttu-id="08e56-133">WorkflowTrigger 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="08e56-133">Microsoft.Azure.Management.Logic.Models.WorkflowTrigger</span></span>

## <span data-ttu-id="08e56-134">筆記</span><span class="sxs-lookup"><span data-stu-id="08e56-134">NOTES</span></span>

## <span data-ttu-id="08e56-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="08e56-135">RELATED LINKS</span></span>

[<span data-ttu-id="08e56-136">AzureRmLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="08e56-136">Get-AzureRmLogicAppTriggerHistory</span></span>](./Get-AzureRmLogicAppTriggerHistory.md)

[<span data-ttu-id="08e56-137">開始-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="08e56-137">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


