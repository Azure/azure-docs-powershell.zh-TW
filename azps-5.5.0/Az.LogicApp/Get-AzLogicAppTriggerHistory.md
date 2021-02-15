---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C1F6BBF9-0DB5-46FD-B8A8-9029B0AB6166
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapptriggerhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
ms.openlocfilehash: 33102de45a929db4016b7e9cf523f0395f335875
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136134"
---
# <span data-ttu-id="d0a50-101">Get-AzLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="d0a50-101">Get-AzLogicAppTriggerHistory</span></span>

## <span data-ttu-id="d0a50-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d0a50-102">SYNOPSIS</span></span>

<span data-ttu-id="d0a50-103">取得邏輯 app 中的觸發程式歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="d0a50-103">Gets the history of triggers in a logic app.</span></span>

## <span data-ttu-id="d0a50-104">句法</span><span class="sxs-lookup"><span data-stu-id="d0a50-104">SYNTAX</span></span>

```powershell
Get-AzLogicAppTriggerHistory -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-HistoryName <String>] [-FollowNextPageLink] [-MaximumFollowNextPageLink <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0a50-105">說明</span><span class="sxs-lookup"><span data-stu-id="d0a50-105">DESCRIPTION</span></span>

<span data-ttu-id="d0a50-106">**AzLogicAppTriggerHistory** Cmdlet 會在邏輯應用程式功能中取得邏輯 app 中的觸發程式歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="d0a50-106">The **Get-AzLogicAppTriggerHistory** cmdlet gets the history of triggers in a logic app in the Logic Apps feature.</span></span>
<span data-ttu-id="d0a50-107">這個 Cmdlet 會傳回 **WorkflowTriggerHistory** 物件。</span><span class="sxs-lookup"><span data-stu-id="d0a50-107">This cmdlet returns a **WorkflowTriggerHistory** object.</span></span>
<span data-ttu-id="d0a50-108">指定邏輯 app、資源群組及觸發程式。</span><span class="sxs-lookup"><span data-stu-id="d0a50-108">Specify the logic app, resource group, and trigger.</span></span>
<span data-ttu-id="d0a50-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="d0a50-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d0a50-110">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="d0a50-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d0a50-111">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="d0a50-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d0a50-112">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="d0a50-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d0a50-113">示例</span><span class="sxs-lookup"><span data-stu-id="d0a50-113">EXAMPLES</span></span>

### <span data-ttu-id="d0a50-114">範例1：取得邏輯 app 的觸發歷程記錄</span><span class="sxs-lookup"><span data-stu-id="d0a50-114">Example 1: Get a trigger history of a logic app</span></span>

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

<span data-ttu-id="d0a50-115">這個命令會在名為 LogicApp03 的邏輯 app 中，取得觸發程式的特定邏輯 app 觸發歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="d0a50-115">This command gets a specific logic app trigger history for a trigger in the logic app named LogicApp03.</span></span>

### <span data-ttu-id="d0a50-116">範例2：取得邏輯 app 的觸發記錄</span><span class="sxs-lookup"><span data-stu-id="d0a50-116">Example 2: Get trigger histories of a logic app</span></span>

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

<span data-ttu-id="d0a50-117">這個命令會在名為 LogicApp07 的邏輯 app 中，取得觸發程式的工作流程觸發記錄。</span><span class="sxs-lookup"><span data-stu-id="d0a50-117">This command gets the workflow trigger histories for a trigger in the logic app named LogicApp07.</span></span>

### <span data-ttu-id="d0a50-118">範例3：取得邏輯 app 的整個觸發歷程記錄</span><span class="sxs-lookup"><span data-stu-id="d0a50-118">Example 3: Get entire trigger history of a logic app</span></span>

```powershell
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp08" -TriggerName "Trigger01" -FollowNextPageLink
```

<span data-ttu-id="d0a50-119">這個命令會透過遵循 NextPageLink 來取得名為 LogicApp08 之邏輯 app 中之觸發程式的整個工作流程觸發歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="d0a50-119">This command gets the entire workflow trigger history for a trigger in the logic app named LogicApp08 by following the NextPageLink.</span></span>

### <span data-ttu-id="d0a50-120">範例4</span><span class="sxs-lookup"><span data-stu-id="d0a50-120">Example 4</span></span>

```powershell
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp08" -TriggerName "Trigger01" -FollowNextPageLink -MaximumFollowNextPageLink 1
```

<span data-ttu-id="d0a50-121">這個命令會透過遵循 NextPageLink 並將結果大小限制為兩個頁面，以取得名為 LogicApp09 之邏輯 app 中之觸發程式的前兩頁的工作流程觸發歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="d0a50-121">This command gets the first two pages of workflow trigger history for a trigger in the logic app named LogicApp09 by following the NextPageLink and limiting the result size to two pages.</span></span>
<span data-ttu-id="d0a50-122">每個頁面都包含三十個結果。</span><span class="sxs-lookup"><span data-stu-id="d0a50-122">Each page contains thirty results.</span></span>

## <span data-ttu-id="d0a50-123">參數</span><span class="sxs-lookup"><span data-stu-id="d0a50-123">PARAMETERS</span></span>

### <span data-ttu-id="d0a50-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0a50-124">-DefaultProfile</span></span>

<span data-ttu-id="d0a50-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d0a50-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0a50-126">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="d0a50-126">-FollowNextPageLink</span></span>

<span data-ttu-id="d0a50-127">表示 Cmdlet 應該跟隨 [下一頁連結]。</span><span class="sxs-lookup"><span data-stu-id="d0a50-127">Indicates the cmdlet should follow next page links.</span></span>

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

### <span data-ttu-id="d0a50-128">-HistoryName</span><span class="sxs-lookup"><span data-stu-id="d0a50-128">-HistoryName</span></span>

<span data-ttu-id="d0a50-129">指定此 Cmdlet 取得的記錄名稱。</span><span class="sxs-lookup"><span data-stu-id="d0a50-129">Specifies the name of the history that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d0a50-130">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="d0a50-130">-MaximumFollowNextPageLink</span></span>

<span data-ttu-id="d0a50-131">指定在使用 FollowNextPageLink 時，追蹤下一個頁面連結的次數。</span><span class="sxs-lookup"><span data-stu-id="d0a50-131">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

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

### <span data-ttu-id="d0a50-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="d0a50-132">-Name</span></span>

<span data-ttu-id="d0a50-133">指定此 Cmdlet 取得觸發歷程記錄的邏輯 app 名稱。</span><span class="sxs-lookup"><span data-stu-id="d0a50-133">Specifies the name of the logic app for which this cmdlet gets trigger history.</span></span>

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

### <span data-ttu-id="d0a50-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0a50-134">-ResourceGroupName</span></span>

<span data-ttu-id="d0a50-135">指定此 Cmdlet 在其中取得歷程記錄的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0a50-135">Specifies the name of the resource group in which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="d0a50-136">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="d0a50-136">-TriggerName</span></span>

<span data-ttu-id="d0a50-137">指定此 Cmdlet 取得其歷程記錄的觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="d0a50-137">Specifies the name of the trigger for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="d0a50-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0a50-138">CommonParameters</span></span>

<span data-ttu-id="d0a50-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d0a50-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0a50-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d0a50-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0a50-141">輸入</span><span class="sxs-lookup"><span data-stu-id="d0a50-141">INPUTS</span></span>

### <span data-ttu-id="d0a50-142">System.object</span><span class="sxs-lookup"><span data-stu-id="d0a50-142">System.String</span></span>

## <span data-ttu-id="d0a50-143">輸出</span><span class="sxs-lookup"><span data-stu-id="d0a50-143">OUTPUTS</span></span>

### <span data-ttu-id="d0a50-144">WorkflowTriggerHistory 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="d0a50-144">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span></span>

## <span data-ttu-id="d0a50-145">筆記</span><span class="sxs-lookup"><span data-stu-id="d0a50-145">NOTES</span></span>

## <span data-ttu-id="d0a50-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="d0a50-146">RELATED LINKS</span></span>

[<span data-ttu-id="d0a50-147">AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="d0a50-147">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="d0a50-148">AzLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="d0a50-148">Get-AzLogicAppTrigger</span></span>](./Get-AzLogicAppTrigger.md)

[<span data-ttu-id="d0a50-149">開始-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="d0a50-149">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)
