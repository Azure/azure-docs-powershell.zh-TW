---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C1F6BBF9-0DB5-46FD-B8A8-9029B0AB6166
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapptriggerhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
ms.openlocfilehash: d20d6ba980b424109e33fd4380eec9be4f7728ee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135932"
---
# <span data-ttu-id="75483-101">Get-AzLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="75483-101">Get-AzLogicAppTriggerHistory</span></span>

## <span data-ttu-id="75483-102">摘要</span><span class="sxs-lookup"><span data-stu-id="75483-102">SYNOPSIS</span></span>
<span data-ttu-id="75483-103">取得邏輯 app 中的觸發程式歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="75483-103">Gets the history of triggers in a logic app.</span></span>

## <span data-ttu-id="75483-104">句法</span><span class="sxs-lookup"><span data-stu-id="75483-104">SYNTAX</span></span>

```
Get-AzLogicAppTriggerHistory -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-HistoryName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75483-105">說明</span><span class="sxs-lookup"><span data-stu-id="75483-105">DESCRIPTION</span></span>
<span data-ttu-id="75483-106">**AzLogicAppTriggerHistory** Cmdlet 會在邏輯應用程式功能中取得邏輯 app 中的觸發程式歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="75483-106">The **Get-AzLogicAppTriggerHistory** cmdlet gets the history of triggers in a logic app in the Logic Apps feature.</span></span>
<span data-ttu-id="75483-107">這個 Cmdlet 會傳回 **WorkflowTriggerHistory** 物件。</span><span class="sxs-lookup"><span data-stu-id="75483-107">This cmdlet returns a **WorkflowTriggerHistory** object.</span></span>
<span data-ttu-id="75483-108">指定邏輯 app、資源群組及觸發程式。</span><span class="sxs-lookup"><span data-stu-id="75483-108">Specify the logic app, resource group, and trigger.</span></span>
<span data-ttu-id="75483-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="75483-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="75483-110">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="75483-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="75483-111">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="75483-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="75483-112">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="75483-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="75483-113">示例</span><span class="sxs-lookup"><span data-stu-id="75483-113">EXAMPLES</span></span>

### <span data-ttu-id="75483-114">範例1：取得邏輯 app 的觸發歷程記錄</span><span class="sxs-lookup"><span data-stu-id="75483-114">Example 1: Get a trigger history of a logic app</span></span>
```
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

<span data-ttu-id="75483-115">這個命令會在名為 LogicApp03 的邏輯 app 中，取得觸發程式的特定邏輯 app 觸發歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="75483-115">This command gets a specific logic app trigger history for a trigger in the logic app named LogicApp03.</span></span>

### <span data-ttu-id="75483-116">範例2：取得邏輯 app 的觸發記錄</span><span class="sxs-lookup"><span data-stu-id="75483-116">Example 2: Get trigger histories of a logic app</span></span>
```
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

<span data-ttu-id="75483-117">這個命令會在名為 LogicApp07 的邏輯 app 中，取得觸發程式的工作流程觸發記錄。</span><span class="sxs-lookup"><span data-stu-id="75483-117">This command gets the workflow trigger histories for a trigger in the logic app named LogicApp07.</span></span>

## <span data-ttu-id="75483-118">參數</span><span class="sxs-lookup"><span data-stu-id="75483-118">PARAMETERS</span></span>

### <span data-ttu-id="75483-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75483-119">-DefaultProfile</span></span>
<span data-ttu-id="75483-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="75483-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75483-121">-HistoryName</span><span class="sxs-lookup"><span data-stu-id="75483-121">-HistoryName</span></span>
<span data-ttu-id="75483-122">指定此 Cmdlet 取得的記錄名稱。</span><span class="sxs-lookup"><span data-stu-id="75483-122">Specifies the name of the history that this cmdlet gets.</span></span>

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

### <span data-ttu-id="75483-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="75483-123">-Name</span></span>
<span data-ttu-id="75483-124">指定此 Cmdlet 取得觸發歷程記錄的邏輯 app 名稱。</span><span class="sxs-lookup"><span data-stu-id="75483-124">Specifies the name of the logic app for which this cmdlet gets trigger history.</span></span>

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

### <span data-ttu-id="75483-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75483-125">-ResourceGroupName</span></span>
<span data-ttu-id="75483-126">指定此 Cmdlet 在其中取得歷程記錄的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="75483-126">Specifies the name of the resource group in which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="75483-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="75483-127">-TriggerName</span></span>
<span data-ttu-id="75483-128">指定此 Cmdlet 取得其歷程記錄的觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="75483-128">Specifies the name of the trigger for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="75483-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75483-129">CommonParameters</span></span>
<span data-ttu-id="75483-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="75483-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75483-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="75483-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75483-132">輸入</span><span class="sxs-lookup"><span data-stu-id="75483-132">INPUTS</span></span>

### <span data-ttu-id="75483-133">System.object</span><span class="sxs-lookup"><span data-stu-id="75483-133">System.String</span></span>

## <span data-ttu-id="75483-134">輸出</span><span class="sxs-lookup"><span data-stu-id="75483-134">OUTPUTS</span></span>

### <span data-ttu-id="75483-135">WorkflowTriggerHistory 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="75483-135">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span></span>

## <span data-ttu-id="75483-136">筆記</span><span class="sxs-lookup"><span data-stu-id="75483-136">NOTES</span></span>

## <span data-ttu-id="75483-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="75483-137">RELATED LINKS</span></span>

[<span data-ttu-id="75483-138">AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="75483-138">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="75483-139">AzLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="75483-139">Get-AzLogicAppTrigger</span></span>](./Get-AzLogicAppTrigger.md)

[<span data-ttu-id="75483-140">開始-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="75483-140">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


