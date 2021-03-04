---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C1F6BBF9-0DB5-46FD-B8A8-9029B0AB6166
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapptriggerhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
ms.openlocfilehash: 7c0d34ad56021e2fb4f74aef1bed41ca38c918c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916536"
---
# <span data-ttu-id="0b54e-101">Get-AzLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="0b54e-101">Get-AzLogicAppTriggerHistory</span></span>

## <span data-ttu-id="0b54e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0b54e-102">SYNOPSIS</span></span>

<span data-ttu-id="0b54e-103">在邏輯應用程式中獲得觸發程式歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="0b54e-103">Gets the history of triggers in a logic app.</span></span>

## <span data-ttu-id="0b54e-104">語法</span><span class="sxs-lookup"><span data-stu-id="0b54e-104">SYNTAX</span></span>

```powershell
Get-AzLogicAppTriggerHistory -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-HistoryName <String>] [-FollowNextPageLink] [-MaximumFollowNextPageLink <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b54e-105">描述</span><span class="sxs-lookup"><span data-stu-id="0b54e-105">DESCRIPTION</span></span>

<span data-ttu-id="0b54e-106">**Get-AzLogicAppTritoryHistory Cmdlet** 在邏輯 App 功能中取得觸發程式歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="0b54e-106">The **Get-AzLogicAppTriggerHistory** cmdlet gets the history of triggers in a logic app in the Logic Apps feature.</span></span>
<span data-ttu-id="0b54e-107">此 Cmdlet 會返回 **WorkflowTritoryHistory** 物件。</span><span class="sxs-lookup"><span data-stu-id="0b54e-107">This cmdlet returns a **WorkflowTriggerHistory** object.</span></span>
<span data-ttu-id="0b54e-108">指定邏輯應用程式、資源群組和觸發程式。</span><span class="sxs-lookup"><span data-stu-id="0b54e-108">Specify the logic app, resource group, and trigger.</span></span>
<span data-ttu-id="0b54e-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="0b54e-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0b54e-110">若要使用動態參數，請于命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="0b54e-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0b54e-111">若要探索動態參數的名稱，在 Cmdlet 名稱之後輸入連字號 (-) ，然後重複按 Tab 鍵以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="0b54e-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0b54e-112">如果您省略必要的範本參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="0b54e-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0b54e-113">例子</span><span class="sxs-lookup"><span data-stu-id="0b54e-113">EXAMPLES</span></span>

### <span data-ttu-id="0b54e-114">範例 1：取得邏輯應用程式的觸發程式歷程記錄</span><span class="sxs-lookup"><span data-stu-id="0b54e-114">Example 1: Get a trigger history of a logic app</span></span>

```powershell
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -TriggerName "Trigger01" -HistoryName "08587489107387695768"
Code        : BadRequest
EndTime     : 1/13/2016 2:42:26 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/A7392_d1e831de68ac4ef89d19a40f05e663
              cb_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A15%3A16Z&sp=r
Name        : 08587489107387695768
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:42:26 PM
Status      : Failed
TrackingId  : f88a499b-f80f-4a28-9bbf-c4cc0d129700
Type        : Microsoft.Logic/workflows/triggers/histories
```

<span data-ttu-id="0b54e-115">此命令會針對邏輯應用程式中名為 LogicApp03 的觸發程式，獲得特定的邏輯應用程式觸發程式歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="0b54e-115">This command gets a specific logic app trigger history for a trigger in the logic app named LogicApp03.</span></span>

### <span data-ttu-id="0b54e-116">範例 2：取得邏輯應用程式的觸發程式記錄</span><span class="sxs-lookup"><span data-stu-id="0b54e-116">Example 2: Get trigger histories of a logic app</span></span>

```powershell
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp07" -TriggerName "Trigger01"
Code        : BadRequest
EndTime     : 1/13/2016 2:43:33 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/CAB46_60e2ad0f0e1947e8b5798716914c5d
              b6_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A18%3A27Z&sp=r
Name        : 08587489106716457817
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:43:33 PM
Status      : Failed
TrackingId  : c91a63f1-48b4-4eae-91eb-8f6dbfa9fe06
Type        : Microsoft.Logic/workflows/triggers/histories

Code        : BadRequest
EndTime     : 1/13/2016 2:42:26 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/A7392_d1e831de68ac4ef89d19a40f05e663
              cb_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A18%3A27Z&sp=r
Name        : 08587489107387695768
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:42:26 PM
Status      : Failed
TrackingId  : f88a499b-f80f-4a28-9bbf-c4cc0d129700
Type        : Microsoft.Logic/workflows/triggers/histories
```

<span data-ttu-id="0b54e-117">此命令會針對邏輯 App 中名為 LogicApp07 的觸發程式，獲得工作流程觸發程式記錄。</span><span class="sxs-lookup"><span data-stu-id="0b54e-117">This command gets the workflow trigger histories for a trigger in the logic app named LogicApp07.</span></span>

### <span data-ttu-id="0b54e-118">範例 3：取得邏輯應用程式的整個觸發程式歷程記錄</span><span class="sxs-lookup"><span data-stu-id="0b54e-118">Example 3: Get entire trigger history of a logic app</span></span>

```powershell
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp08" -TriggerName "Trigger01" -FollowNextPageLink
```

<span data-ttu-id="0b54e-119">此命令會遵循 NextPageLink，在邏輯 App 中為邏輯 App 中的觸發程式，獲得觸發程式的整個工作流程觸發程式歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="0b54e-119">This command gets the entire workflow trigger history for a trigger in the logic app named LogicApp08 by following the NextPageLink.</span></span>

### <span data-ttu-id="0b54e-120">範例 4</span><span class="sxs-lookup"><span data-stu-id="0b54e-120">Example 4</span></span>

```powershell
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp08" -TriggerName "Trigger01" -FollowNextPageLink -MaximumFollowNextPageLink 1
```

<span data-ttu-id="0b54e-121">此命令會遵循 NextPageLink，將結果大小限制為兩頁，以取得邏輯 App 中名為 LogicApp09 之觸發程式之工作流程觸發程式歷程記錄前兩頁。</span><span class="sxs-lookup"><span data-stu-id="0b54e-121">This command gets the first two pages of workflow trigger history for a trigger in the logic app named LogicApp09 by following the NextPageLink and limiting the result size to two pages.</span></span>
<span data-ttu-id="0b54e-122">每頁包含三十個結果。</span><span class="sxs-lookup"><span data-stu-id="0b54e-122">Each page contains thirty results.</span></span>

## <span data-ttu-id="0b54e-123">參數</span><span class="sxs-lookup"><span data-stu-id="0b54e-123">PARAMETERS</span></span>

### <span data-ttu-id="0b54e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b54e-124">-DefaultProfile</span></span>

<span data-ttu-id="0b54e-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="0b54e-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b54e-126">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="0b54e-126">-FollowNextPageLink</span></span>

<span data-ttu-id="0b54e-127">表示 Cmdlet 應該遵循下一頁連結。</span><span class="sxs-lookup"><span data-stu-id="0b54e-127">Indicates the cmdlet should follow next page links.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: FL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b54e-128">-HistoryName</span><span class="sxs-lookup"><span data-stu-id="0b54e-128">-HistoryName</span></span>

<span data-ttu-id="0b54e-129">指定此 Cmdlet 所獲得歷程記錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="0b54e-129">Specifies the name of the history that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b54e-130">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="0b54e-130">-MaximumFollowNextPageLink</span></span>

<span data-ttu-id="0b54e-131">指定使用 FollowNextPageLink 時，追蹤下一頁連結的時間。</span><span class="sxs-lookup"><span data-stu-id="0b54e-131">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: ML

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b54e-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="0b54e-132">-Name</span></span>

<span data-ttu-id="0b54e-133">指定此 Cmdlet 會觸發歷程記錄的邏輯應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="0b54e-133">Specifies the name of the logic app for which this cmdlet gets trigger history.</span></span>

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

### <span data-ttu-id="0b54e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b54e-134">-ResourceGroupName</span></span>

<span data-ttu-id="0b54e-135">指定此 Cmdlet 會獲得歷程記錄的資源組名。</span><span class="sxs-lookup"><span data-stu-id="0b54e-135">Specifies the name of the resource group in which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="0b54e-136">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="0b54e-136">-TriggerName</span></span>

<span data-ttu-id="0b54e-137">指定此 Cmdlet 會獲得歷程記錄之觸發者的名稱。</span><span class="sxs-lookup"><span data-stu-id="0b54e-137">Specifies the name of the trigger for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="0b54e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b54e-138">CommonParameters</span></span>

<span data-ttu-id="0b54e-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0b54e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b54e-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b54e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b54e-141">輸入</span><span class="sxs-lookup"><span data-stu-id="0b54e-141">INPUTS</span></span>

### <span data-ttu-id="0b54e-142">System.String</span><span class="sxs-lookup"><span data-stu-id="0b54e-142">System.String</span></span>

## <span data-ttu-id="0b54e-143">輸出</span><span class="sxs-lookup"><span data-stu-id="0b54e-143">OUTPUTS</span></span>

### <span data-ttu-id="0b54e-144">Microsoft.Azure.management.Logic.models.WorkflowTritoryHistory</span><span class="sxs-lookup"><span data-stu-id="0b54e-144">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span></span>

## <span data-ttu-id="0b54e-145">筆記</span><span class="sxs-lookup"><span data-stu-id="0b54e-145">NOTES</span></span>

## <span data-ttu-id="0b54e-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b54e-146">RELATED LINKS</span></span>

[<span data-ttu-id="0b54e-147">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="0b54e-147">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="0b54e-148">Get-AzLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="0b54e-148">Get-AzLogicAppTrigger</span></span>](./Get-AzLogicAppTrigger.md)

[<span data-ttu-id="0b54e-149">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="0b54e-149">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)
