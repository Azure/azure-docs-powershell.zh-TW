---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
ms.openlocfilehash: 855cab84e4ab9de2cd7afae2a25dbc867a192e96
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132826"
---
# <span data-ttu-id="877c4-101">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="877c4-101">Get-AzLogicAppRunHistory</span></span>

## <span data-ttu-id="877c4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="877c4-102">SYNOPSIS</span></span>

<span data-ttu-id="877c4-103">取得邏輯 app 的執行歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="877c4-103">Gets the run history of a logic app.</span></span>

## <span data-ttu-id="877c4-104">句法</span><span class="sxs-lookup"><span data-stu-id="877c4-104">SYNTAX</span></span>

```powershell
Get-AzLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>] [-FollowNextPageLink]
 [-MaximumFollowNextPageLink <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="877c4-105">說明</span><span class="sxs-lookup"><span data-stu-id="877c4-105">DESCRIPTION</span></span>

<span data-ttu-id="877c4-106">**AzLogicAppRunHistory** Cmdlet 會取得邏輯 app 的執行歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="877c4-106">The **Get-AzLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="877c4-107">這個 Cmdlet 會傳回 **WorkflowRun** 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="877c4-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="877c4-108">指定邏輯 app 與資源群組。</span><span class="sxs-lookup"><span data-stu-id="877c4-108">Specify the logic app and resource group.</span></span>
<span data-ttu-id="877c4-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="877c4-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="877c4-110">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="877c4-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="877c4-111">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="877c4-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="877c4-112">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="877c4-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="877c4-113">示例</span><span class="sxs-lookup"><span data-stu-id="877c4-113">EXAMPLES</span></span>

### <span data-ttu-id="877c4-114">範例1：取得邏輯 app 的執行歷程記錄</span><span class="sxs-lookup"><span data-stu-id="877c4-114">Example 1: Get the run history of a logic app</span></span>

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

<span data-ttu-id="877c4-115">這個命令會取得名為 LogicApp03 的邏輯 app 的執行歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="877c4-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="877c4-116">範例2：取得邏輯 app 執行</span><span class="sxs-lookup"><span data-stu-id="877c4-116">Example 2: Get a logic app run</span></span>

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

<span data-ttu-id="877c4-117">這個命令會針對名為 LogicApp03 的邏輯 app 取得特定的邏輯 app 執行。</span><span class="sxs-lookup"><span data-stu-id="877c4-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

### <span data-ttu-id="877c4-118">範例3</span><span class="sxs-lookup"><span data-stu-id="877c4-118">Example 3</span></span>

```powershell
Get-AzLogicAppRunHistory -Name 'LogicApp03' -ResourceGroupName MyResourceGroup -FollowNextPageLink
```

<span data-ttu-id="877c4-119">這個命令會透過遵循 NextPageLink 來取得名為 LogicApp03 之邏輯 app 的整個執行歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="877c4-119">This command gets the entire run history of a logic app named LogicApp03 by following the NextPageLink.</span></span>

### <span data-ttu-id="877c4-120">範例4</span><span class="sxs-lookup"><span data-stu-id="877c4-120">Example 4</span></span>

```powershell
Get-AzLogicAppRunHistory -Name 'LogicApp03' -ResourceGroupName MyResourceGroup -FollowNextPageLink -MaximumFollowNextPageLink 1
```

<span data-ttu-id="877c4-121">這個命令會透過遵循 NextPageLink 並將結果大小限制為兩個頁面，以取得名為 LogicApp03 之邏輯 app 的前兩頁。</span><span class="sxs-lookup"><span data-stu-id="877c4-121">This command gets the first two pages of run history of a logic app named LogicApp03 by following the NextPageLink and limiting the result size to two pages.</span></span>
<span data-ttu-id="877c4-122">每個頁面都包含三十個結果。</span><span class="sxs-lookup"><span data-stu-id="877c4-122">Each page contains thirty results.</span></span>

## <span data-ttu-id="877c4-123">參數</span><span class="sxs-lookup"><span data-stu-id="877c4-123">PARAMETERS</span></span>

### <span data-ttu-id="877c4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="877c4-124">-DefaultProfile</span></span>

<span data-ttu-id="877c4-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="877c4-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="877c4-126">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="877c4-126">-FollowNextPageLink</span></span>

<span data-ttu-id="877c4-127">表示 Cmdlet 應該跟隨 [下一頁連結]。</span><span class="sxs-lookup"><span data-stu-id="877c4-127">Indicates the cmdlet should follow next page links.</span></span>

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

### <span data-ttu-id="877c4-128">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="877c4-128">-MaximumFollowNextPageLink</span></span>

<span data-ttu-id="877c4-129">指定在使用 FollowNextPageLink 時，追蹤下一個頁面連結的次數。</span><span class="sxs-lookup"><span data-stu-id="877c4-129">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

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

### <span data-ttu-id="877c4-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="877c4-130">-Name</span></span>

<span data-ttu-id="877c4-131">指定此 Cmdlet 取得其 [執行歷程記錄] 的邏輯 app 名稱。</span><span class="sxs-lookup"><span data-stu-id="877c4-131">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

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

### <span data-ttu-id="877c4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="877c4-132">-ResourceGroupName</span></span>

<span data-ttu-id="877c4-133">指定包含邏輯 app 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="877c4-133">Specifies the name of a resource group that contains the logic app.</span></span>

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

### <span data-ttu-id="877c4-134">-RunName</span><span class="sxs-lookup"><span data-stu-id="877c4-134">-RunName</span></span>

<span data-ttu-id="877c4-135">指定邏輯 app 的 [執行名稱]。</span><span class="sxs-lookup"><span data-stu-id="877c4-135">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="877c4-136">這個 Cmdlet 會取得這個 Cmdlet 所指定的工作流程執行。</span><span class="sxs-lookup"><span data-stu-id="877c4-136">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="877c4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="877c4-137">CommonParameters</span></span>

<span data-ttu-id="877c4-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="877c4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="877c4-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="877c4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="877c4-140">輸入</span><span class="sxs-lookup"><span data-stu-id="877c4-140">INPUTS</span></span>

### <span data-ttu-id="877c4-141">System.object</span><span class="sxs-lookup"><span data-stu-id="877c4-141">System.String</span></span>

## <span data-ttu-id="877c4-142">輸出</span><span class="sxs-lookup"><span data-stu-id="877c4-142">OUTPUTS</span></span>

### <span data-ttu-id="877c4-143">WorkflowRun 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="877c4-143">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="877c4-144">筆記</span><span class="sxs-lookup"><span data-stu-id="877c4-144">NOTES</span></span>

## <span data-ttu-id="877c4-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="877c4-145">RELATED LINKS</span></span>

[<span data-ttu-id="877c4-146">AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="877c4-146">Get-AzLogicAppRunAction</span></span>](./Get-AzLogicAppRunAction.md)

[<span data-ttu-id="877c4-147">開始-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="877c4-147">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

[<span data-ttu-id="877c4-148">停止 AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="877c4-148">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)
