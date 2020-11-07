---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: C1F6BBF9-0DB5-46FD-B8A8-9029B0AB6166
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerHistory.md
ms.openlocfilehash: 23ccef6dedf1a0be0f7d7cf1b565c936e76a0309
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625166"
---
# <span data-ttu-id="c0786-101">Get-AzureRmLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="c0786-101">Get-AzureRmLogicAppTriggerHistory</span></span>

## <span data-ttu-id="c0786-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c0786-102">SYNOPSIS</span></span>
<span data-ttu-id="c0786-103">取得邏輯 app 中的觸發程式歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="c0786-103">Gets the history of triggers in a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0786-104">句法</span><span class="sxs-lookup"><span data-stu-id="c0786-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppTriggerHistory -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-HistoryName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0786-105">說明</span><span class="sxs-lookup"><span data-stu-id="c0786-105">DESCRIPTION</span></span>
<span data-ttu-id="c0786-106">**AzureRmLogicAppTriggerHistory** Cmdlet 會在邏輯應用程式功能中取得邏輯 app 中的觸發程式歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="c0786-106">The **Get-AzureRmLogicAppTriggerHistory** cmdlet gets the history of triggers in a logic app in the Logic Apps feature.</span></span>
<span data-ttu-id="c0786-107">這個 Cmdlet 會傳回 **WorkflowTriggerHistory** 物件。</span><span class="sxs-lookup"><span data-stu-id="c0786-107">This cmdlet returns a **WorkflowTriggerHistory** object.</span></span>
<span data-ttu-id="c0786-108">指定邏輯 app、資源群組及觸發程式。</span><span class="sxs-lookup"><span data-stu-id="c0786-108">Specify the logic app, resource group, and trigger.</span></span>

<span data-ttu-id="c0786-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="c0786-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c0786-110">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="c0786-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c0786-111">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="c0786-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c0786-112">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="c0786-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c0786-113">示例</span><span class="sxs-lookup"><span data-stu-id="c0786-113">EXAMPLES</span></span>

### <span data-ttu-id="c0786-114">範例1：取得邏輯 app 的觸發歷程記錄</span><span class="sxs-lookup"><span data-stu-id="c0786-114">Example 1: Get a trigger history of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTriggerHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -TriggerName "Trigger01" -HistoryName "08587489107387695768"
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

<span data-ttu-id="c0786-115">這個命令會在名為 LogicApp03 的邏輯 app 中，取得觸發程式的特定邏輯 app 觸發歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="c0786-115">This command gets a specific logic app trigger history for a trigger in the logic app named LogicApp03.</span></span>

### <span data-ttu-id="c0786-116">範例2：取得邏輯 app 的觸發記錄</span><span class="sxs-lookup"><span data-stu-id="c0786-116">Example 2: Get trigger histories of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp07" -TriggerName "Trigger01"
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

<span data-ttu-id="c0786-117">這個命令會在名為 LogicApp07 的邏輯 app 中，取得觸發程式的工作流程觸發記錄。</span><span class="sxs-lookup"><span data-stu-id="c0786-117">This command gets the workflow trigger histories for a trigger in the logic app named LogicApp07.</span></span>

## <span data-ttu-id="c0786-118">參數</span><span class="sxs-lookup"><span data-stu-id="c0786-118">PARAMETERS</span></span>

### <span data-ttu-id="c0786-119">-HistoryName</span><span class="sxs-lookup"><span data-stu-id="c0786-119">-HistoryName</span></span>
<span data-ttu-id="c0786-120">指定此 Cmdlet 取得的記錄名稱。</span><span class="sxs-lookup"><span data-stu-id="c0786-120">Specifies the name of the history that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c0786-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="c0786-121">-Name</span></span>
<span data-ttu-id="c0786-122">指定此 Cmdlet 取得觸發歷程記錄的邏輯 app 名稱。</span><span class="sxs-lookup"><span data-stu-id="c0786-122">Specifies the name of the logic app for which this cmdlet gets trigger history.</span></span>

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

### <span data-ttu-id="c0786-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0786-123">-ResourceGroupName</span></span>
<span data-ttu-id="c0786-124">指定此 Cmdlet 在其中取得歷程記錄的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0786-124">Specifies the name of the resource group in which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="c0786-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="c0786-125">-TriggerName</span></span>
<span data-ttu-id="c0786-126">指定此 Cmdlet 取得其歷程記錄的觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="c0786-126">Specifies the name of the trigger for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="c0786-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0786-127">-DefaultProfile</span></span>
<span data-ttu-id="c0786-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0786-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0786-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0786-129">CommonParameters</span></span>
<span data-ttu-id="c0786-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c0786-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0786-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c0786-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0786-132">輸入</span><span class="sxs-lookup"><span data-stu-id="c0786-132">INPUTS</span></span>

## <span data-ttu-id="c0786-133">輸出</span><span class="sxs-lookup"><span data-stu-id="c0786-133">OUTPUTS</span></span>

### <span data-ttu-id="c0786-134">WorkflowTriggerHistory 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="c0786-134">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span></span>

## <span data-ttu-id="c0786-135">筆記</span><span class="sxs-lookup"><span data-stu-id="c0786-135">NOTES</span></span>

## <span data-ttu-id="c0786-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0786-136">RELATED LINKS</span></span>

[<span data-ttu-id="c0786-137">AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="c0786-137">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="c0786-138">AzureRmLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="c0786-138">Get-AzureRmLogicAppTrigger</span></span>](./Get-AzureRmLogicAppTrigger.md)

[<span data-ttu-id="c0786-139">開始-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="c0786-139">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


