---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
ms.openlocfilehash: 01bba193f763eff784bdd5f3f67118d84c6235a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916544"
---
# <span data-ttu-id="cc00f-101">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="cc00f-101">Get-AzLogicAppRunHistory</span></span>

## <span data-ttu-id="cc00f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cc00f-102">SYNOPSIS</span></span>

<span data-ttu-id="cc00f-103">獲得邏輯應用程式的執行歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="cc00f-103">Gets the run history of a logic app.</span></span>

## <span data-ttu-id="cc00f-104">語法</span><span class="sxs-lookup"><span data-stu-id="cc00f-104">SYNTAX</span></span>

```powershell
Get-AzLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>] [-FollowNextPageLink]
 [-MaximumFollowNextPageLink <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc00f-105">描述</span><span class="sxs-lookup"><span data-stu-id="cc00f-105">DESCRIPTION</span></span>

<span data-ttu-id="cc00f-106">**Get-AzLogicAppRunHistory** Cmdlet 會取得邏輯應用程式的執行歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="cc00f-106">The **Get-AzLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="cc00f-107">此 Cmdlet 會返回 **WorkflowRun 物件** 的集合。</span><span class="sxs-lookup"><span data-stu-id="cc00f-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="cc00f-108">指定邏輯應用程式和資源群組。</span><span class="sxs-lookup"><span data-stu-id="cc00f-108">Specify the logic app and resource group.</span></span>
<span data-ttu-id="cc00f-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="cc00f-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="cc00f-110">若要使用動態參數，請于命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="cc00f-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="cc00f-111">若要探索動態參數的名稱，在 Cmdlet 名稱之後輸入連字號 (-) ，然後重複按 Tab 鍵以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="cc00f-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="cc00f-112">如果您省略必要的範本參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="cc00f-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="cc00f-113">例子</span><span class="sxs-lookup"><span data-stu-id="cc00f-113">EXAMPLES</span></span>

### <span data-ttu-id="cc00f-114">範例 1：取得邏輯應用程式的執行歷程記錄</span><span class="sxs-lookup"><span data-stu-id="cc00f-114">Example 1: Get the run history of a logic app</span></span>

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

<span data-ttu-id="cc00f-115">此命令會獲得名為 LogicApp03 的邏輯應用程式的執行歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="cc00f-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="cc00f-116">範例 2：執行邏輯應用程式</span><span class="sxs-lookup"><span data-stu-id="cc00f-116">Example 2: Get a logic app run</span></span>

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

<span data-ttu-id="cc00f-117">此命令會針對名為 LogicApp03 的邏輯應用程式執行特定的邏輯應用程式。</span><span class="sxs-lookup"><span data-stu-id="cc00f-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

### <span data-ttu-id="cc00f-118">範例 3</span><span class="sxs-lookup"><span data-stu-id="cc00f-118">Example 3</span></span>

```powershell
Get-AzLogicAppRunHistory -Name 'LogicApp03' -ResourceGroupName MyResourceGroup -FollowNextPageLink
```

<span data-ttu-id="cc00f-119">此命令會遵循 NextPageLink，獲得名為 LogicApp03 的邏輯應用程式完整執行歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="cc00f-119">This command gets the entire run history of a logic app named LogicApp03 by following the NextPageLink.</span></span>

### <span data-ttu-id="cc00f-120">範例 4</span><span class="sxs-lookup"><span data-stu-id="cc00f-120">Example 4</span></span>

```powershell
Get-AzLogicAppRunHistory -Name 'LogicApp03' -ResourceGroupName MyResourceGroup -FollowNextPageLink -MaximumFollowNextPageLink 1
```

<span data-ttu-id="cc00f-121">此命令會遵循 NextPageLink，將結果大小限制為兩頁，以取得邏輯應用程式邏輯 App 的前兩頁執行歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="cc00f-121">This command gets the first two pages of run history of a logic app named LogicApp03 by following the NextPageLink and limiting the result size to two pages.</span></span>
<span data-ttu-id="cc00f-122">每頁包含三十個結果。</span><span class="sxs-lookup"><span data-stu-id="cc00f-122">Each page contains thirty results.</span></span>

## <span data-ttu-id="cc00f-123">參數</span><span class="sxs-lookup"><span data-stu-id="cc00f-123">PARAMETERS</span></span>

### <span data-ttu-id="cc00f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc00f-124">-DefaultProfile</span></span>

<span data-ttu-id="cc00f-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="cc00f-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc00f-126">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="cc00f-126">-FollowNextPageLink</span></span>

<span data-ttu-id="cc00f-127">表示 Cmdlet 應該遵循下一頁連結。</span><span class="sxs-lookup"><span data-stu-id="cc00f-127">Indicates the cmdlet should follow next page links.</span></span>

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

### <span data-ttu-id="cc00f-128">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="cc00f-128">-MaximumFollowNextPageLink</span></span>

<span data-ttu-id="cc00f-129">指定使用 FollowNextPageLink 時，追蹤下一頁連結的時間。</span><span class="sxs-lookup"><span data-stu-id="cc00f-129">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

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

### <span data-ttu-id="cc00f-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="cc00f-130">-Name</span></span>

<span data-ttu-id="cc00f-131">指定此 Cmdlet 執行歷程記錄的邏輯應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="cc00f-131">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

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

### <span data-ttu-id="cc00f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc00f-132">-ResourceGroupName</span></span>

<span data-ttu-id="cc00f-133">指定包含邏輯應用程式的資源組名。</span><span class="sxs-lookup"><span data-stu-id="cc00f-133">Specifies the name of a resource group that contains the logic app.</span></span>

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

### <span data-ttu-id="cc00f-134">-RunName</span><span class="sxs-lookup"><span data-stu-id="cc00f-134">-RunName</span></span>

<span data-ttu-id="cc00f-135">指定邏輯應用程式的執行名稱。</span><span class="sxs-lookup"><span data-stu-id="cc00f-135">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="cc00f-136">此 Cmdlet 會執行此 Cmdlet 指定的工作流程。</span><span class="sxs-lookup"><span data-stu-id="cc00f-136">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="cc00f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc00f-137">CommonParameters</span></span>

<span data-ttu-id="cc00f-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cc00f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc00f-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc00f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc00f-140">輸入</span><span class="sxs-lookup"><span data-stu-id="cc00f-140">INPUTS</span></span>

### <span data-ttu-id="cc00f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="cc00f-141">System.String</span></span>

## <span data-ttu-id="cc00f-142">輸出</span><span class="sxs-lookup"><span data-stu-id="cc00f-142">OUTPUTS</span></span>

### <span data-ttu-id="cc00f-143">Microsoft.Azure.management.Logic.models.WorkflowRun</span><span class="sxs-lookup"><span data-stu-id="cc00f-143">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="cc00f-144">筆記</span><span class="sxs-lookup"><span data-stu-id="cc00f-144">NOTES</span></span>

## <span data-ttu-id="cc00f-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc00f-145">RELATED LINKS</span></span>

[<span data-ttu-id="cc00f-146">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="cc00f-146">Get-AzLogicAppRunAction</span></span>](./Get-AzLogicAppRunAction.md)

[<span data-ttu-id="cc00f-147">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="cc00f-147">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

[<span data-ttu-id="cc00f-148">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="cc00f-148">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)
