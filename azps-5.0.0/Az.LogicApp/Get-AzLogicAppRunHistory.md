---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
ms.openlocfilehash: de1c40dc7c9f8fefb1a275394b066e8af96de211
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139156"
---
# <span data-ttu-id="efe88-101">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="efe88-101">Get-AzLogicAppRunHistory</span></span>

## <span data-ttu-id="efe88-102">摘要</span><span class="sxs-lookup"><span data-stu-id="efe88-102">SYNOPSIS</span></span>
<span data-ttu-id="efe88-103">取得邏輯 app 的執行歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="efe88-103">Gets the run history of a logic app.</span></span>

## <span data-ttu-id="efe88-104">句法</span><span class="sxs-lookup"><span data-stu-id="efe88-104">SYNTAX</span></span>

```
Get-AzLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efe88-105">說明</span><span class="sxs-lookup"><span data-stu-id="efe88-105">DESCRIPTION</span></span>
<span data-ttu-id="efe88-106">**AzLogicAppRunHistory** Cmdlet 會取得邏輯 app 的執行歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="efe88-106">The **Get-AzLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="efe88-107">這個 Cmdlet 會傳回 **WorkflowRun** 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="efe88-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="efe88-108">指定邏輯 app 與資源群組。</span><span class="sxs-lookup"><span data-stu-id="efe88-108">Specify the logic app and resource group.</span></span>
<span data-ttu-id="efe88-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="efe88-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="efe88-110">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="efe88-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="efe88-111">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="efe88-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="efe88-112">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="efe88-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="efe88-113">示例</span><span class="sxs-lookup"><span data-stu-id="efe88-113">EXAMPLES</span></span>

### <span data-ttu-id="efe88-114">範例1：取得邏輯 app 的執行歷程記錄</span><span class="sxs-lookup"><span data-stu-id="efe88-114">Example 1: Get the run history of a logic app</span></span>
```powershell
PS C:\>Get-AzLogicAppRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952540

CorrelationId    : d3ddc917-9aaa-47b3-8814-c621c2ae530b
EndTime          : 1/13/2016 2:42:56 PM
Error            : {code, message}
Name             : 08587489107100664541
Outputs          : {}
StartTime        : 1/13/2016 2:42:55 PM
Status           : Failed
TriggerName      : httpTrigger
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

<span data-ttu-id="efe88-115">這個命令會取得名為 LogicApp03 的邏輯 app 的執行歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="efe88-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="efe88-116">範例2：取得邏輯 app 執行</span><span class="sxs-lookup"><span data-stu-id="efe88-116">Example 2: Get a logic app run</span></span>
```powershell
PS C:\>Get-AzLogicAppRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -RunName "08587489104702792076"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

<span data-ttu-id="efe88-117">這個命令會針對名為 LogicApp03 的邏輯 app 取得特定的邏輯 app 執行。</span><span class="sxs-lookup"><span data-stu-id="efe88-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

### <span data-ttu-id="efe88-118">範例3</span><span class="sxs-lookup"><span data-stu-id="efe88-118">Example 3</span></span>

<span data-ttu-id="efe88-119">這個命令會取得名為 LogicApp03 的邏輯 app 的執行歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="efe88-119">This command gets the run history of a logic app named LogicApp03.</span></span> <span data-ttu-id="efe88-120"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="efe88-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzLogicAppRunHistory -Name 'IntegrationAccount31' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="efe88-121">參數</span><span class="sxs-lookup"><span data-stu-id="efe88-121">PARAMETERS</span></span>

### <span data-ttu-id="efe88-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efe88-122">-DefaultProfile</span></span>
<span data-ttu-id="efe88-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="efe88-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="efe88-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="efe88-124">-Name</span></span>
<span data-ttu-id="efe88-125">指定此 Cmdlet 取得其 [執行歷程記錄] 的邏輯 app 名稱。</span><span class="sxs-lookup"><span data-stu-id="efe88-125">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efe88-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efe88-126">-ResourceGroupName</span></span>
<span data-ttu-id="efe88-127">指定包含邏輯 app 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="efe88-127">Specifies the name of a resource group that contains the logic app.</span></span>

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

### <span data-ttu-id="efe88-128">-RunName</span><span class="sxs-lookup"><span data-stu-id="efe88-128">-RunName</span></span>
<span data-ttu-id="efe88-129">指定邏輯 app 的 [執行名稱]。</span><span class="sxs-lookup"><span data-stu-id="efe88-129">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="efe88-130">這個 Cmdlet 會取得這個 Cmdlet 所指定的工作流程執行。</span><span class="sxs-lookup"><span data-stu-id="efe88-130">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="efe88-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efe88-131">CommonParameters</span></span>
<span data-ttu-id="efe88-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="efe88-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efe88-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="efe88-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efe88-134">輸入</span><span class="sxs-lookup"><span data-stu-id="efe88-134">INPUTS</span></span>

### <span data-ttu-id="efe88-135">System.object</span><span class="sxs-lookup"><span data-stu-id="efe88-135">System.String</span></span>

## <span data-ttu-id="efe88-136">輸出</span><span class="sxs-lookup"><span data-stu-id="efe88-136">OUTPUTS</span></span>

### <span data-ttu-id="efe88-137">WorkflowRun 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="efe88-137">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="efe88-138">筆記</span><span class="sxs-lookup"><span data-stu-id="efe88-138">NOTES</span></span>

## <span data-ttu-id="efe88-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="efe88-139">RELATED LINKS</span></span>

[<span data-ttu-id="efe88-140">AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="efe88-140">Get-AzLogicAppRunAction</span></span>](./Get-AzLogicAppRunAction.md)

[<span data-ttu-id="efe88-141">開始-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="efe88-141">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

[<span data-ttu-id="efe88-142">停止 AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="efe88-142">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


