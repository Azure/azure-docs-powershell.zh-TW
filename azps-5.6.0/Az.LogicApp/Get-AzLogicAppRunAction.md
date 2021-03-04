---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
ms.openlocfilehash: 6835fb2ce58e834e9270af293fdc4f0d07fc01aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916547"
---
# <span data-ttu-id="249d5-101">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="249d5-101">Get-AzLogicAppRunAction</span></span>

## <span data-ttu-id="249d5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="249d5-102">SYNOPSIS</span></span>

<span data-ttu-id="249d5-103">從邏輯應用程式執行中執行動作。</span><span class="sxs-lookup"><span data-stu-id="249d5-103">Gets an action from a logic app run.</span></span>

## <span data-ttu-id="249d5-104">語法</span><span class="sxs-lookup"><span data-stu-id="249d5-104">SYNTAX</span></span>

```powershell
Get-AzLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String> [-ActionName <String>]
 [-FollowNextPageLink] [-MaximumFollowNextPageLink <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="249d5-105">描述</span><span class="sxs-lookup"><span data-stu-id="249d5-105">DESCRIPTION</span></span>

<span data-ttu-id="249d5-106">**Get-AzLogicAppRunAction** Cmdlet 會從邏輯應用程式執行中取得動作。</span><span class="sxs-lookup"><span data-stu-id="249d5-106">The **Get-AzLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="249d5-107">此 Cmdlet 會返回 **WorkflowRunAction** 物件。</span><span class="sxs-lookup"><span data-stu-id="249d5-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="249d5-108">指定邏輯應用程式、資源群組及執行。</span><span class="sxs-lookup"><span data-stu-id="249d5-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="249d5-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="249d5-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="249d5-110">若要使用動態參數，請于命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="249d5-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="249d5-111">若要探索動態參數的名稱，在 Cmdlet 名稱之後輸入連字號 (-) ，然後重複按 Tab 鍵以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="249d5-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="249d5-112">如果您省略必要的範本參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="249d5-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="249d5-113">例子</span><span class="sxs-lookup"><span data-stu-id="249d5-113">EXAMPLES</span></span>

### <span data-ttu-id="249d5-114">範例 1：從邏輯應用程式執行取得動作</span><span class="sxs-lookup"><span data-stu-id="249d5-114">Example 1: Get an action from a Logic App run</span></span>

```powershell
PS C:\>Get-AzLogicAppRunAction -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "08585925184423369718380498702CU26" -ActionName "LogicAppAction01"
Code        : NotFound
EndTime     : 1/13/2016 2:42:56 PM
Error       : 
InputsLink  : Microsoft.Azure.Management.Logic.Models.ContentLink
Name        : LogicAppAction01
OutputsLink : Microsoft.Azure.Management.Logic.Models.ContentLink
StartTime   : 1/13/2016 2:42:55 PM
Status      : Failed
TrackingId  : 
Type        :
```

<span data-ttu-id="249d5-115">此命令會從名為 LogicApp05 的邏輯應用程式，從識別碼 0858592518442369718380498702CU26 執行時，從名為 LogicApp05 的邏輯 App 中，獲得特定的邏輯 App 動作。</span><span class="sxs-lookup"><span data-stu-id="249d5-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run with identifier 08585925184423369718380498702CU26.</span></span>

### <span data-ttu-id="249d5-116">範例 2：執行邏輯應用程式的所有動作</span><span class="sxs-lookup"><span data-stu-id="249d5-116">Example 2: Get all the actions from a Logic App run</span></span>

```powershell
PS C:\>Get-AzLogicAppRunAction -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "08585925184423369718380498702CU26" -FollowNextPageLink
```

<span data-ttu-id="249d5-117">此命令會從具有識別碼 0858592518442369718380498702CU26 的邏輯應用程式名稱為 LogicApp05 的邏輯應用程式中，獲得所有邏輯 App 動作。</span><span class="sxs-lookup"><span data-stu-id="249d5-117">This command gets all Logic App actions from a run with identifier 08585925184423369718380498702CU26 of a logic app named LogicApp05.</span></span>

## <span data-ttu-id="249d5-118">參數</span><span class="sxs-lookup"><span data-stu-id="249d5-118">PARAMETERS</span></span>

### <span data-ttu-id="249d5-119">-ActionName</span><span class="sxs-lookup"><span data-stu-id="249d5-119">-ActionName</span></span>

<span data-ttu-id="249d5-120">指定邏輯應用程式執行中動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="249d5-120">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="249d5-121">此 Cmdlet 會獲得此參數指定的動作。</span><span class="sxs-lookup"><span data-stu-id="249d5-121">This cmdlet gets the action that this parameter specifies.</span></span>

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

### <span data-ttu-id="249d5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="249d5-122">-DefaultProfile</span></span>

<span data-ttu-id="249d5-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="249d5-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="249d5-124">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="249d5-124">-FollowNextPageLink</span></span>

<span data-ttu-id="249d5-125">表示 Cmdlet 應該遵循下一頁連結。</span><span class="sxs-lookup"><span data-stu-id="249d5-125">Indicates the cmdlet should follow next page links.</span></span>

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

### <span data-ttu-id="249d5-126">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="249d5-126">-MaximumFollowNextPageLink</span></span>

<span data-ttu-id="249d5-127">指定使用 FollowNextPageLink 時，追蹤下一頁連結的時間。</span><span class="sxs-lookup"><span data-stu-id="249d5-127">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

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

### <span data-ttu-id="249d5-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="249d5-128">-Name</span></span>

<span data-ttu-id="249d5-129">指定此 Cmdlet 會執行動作的邏輯應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="249d5-129">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="249d5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="249d5-130">-ResourceGroupName</span></span>

<span data-ttu-id="249d5-131">指定在此 Cmdlet 中執行動作的資源組名。</span><span class="sxs-lookup"><span data-stu-id="249d5-131">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="249d5-132">-RunName</span><span class="sxs-lookup"><span data-stu-id="249d5-132">-RunName</span></span>

<span data-ttu-id="249d5-133">指定邏輯應用程式執行的名稱。</span><span class="sxs-lookup"><span data-stu-id="249d5-133">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="249d5-134">此 Cmdlet 會針對此參數指定的執行獲得動作。</span><span class="sxs-lookup"><span data-stu-id="249d5-134">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="249d5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="249d5-135">CommonParameters</span></span>

<span data-ttu-id="249d5-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="249d5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="249d5-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="249d5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="249d5-138">輸入</span><span class="sxs-lookup"><span data-stu-id="249d5-138">INPUTS</span></span>

### <span data-ttu-id="249d5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="249d5-139">System.String</span></span>

## <span data-ttu-id="249d5-140">輸出</span><span class="sxs-lookup"><span data-stu-id="249d5-140">OUTPUTS</span></span>

### <span data-ttu-id="249d5-141">Microsoft.Azure.management.Logic.models.WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="249d5-141">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="249d5-142">筆記</span><span class="sxs-lookup"><span data-stu-id="249d5-142">NOTES</span></span>

## <span data-ttu-id="249d5-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="249d5-143">RELATED LINKS</span></span>

[<span data-ttu-id="249d5-144">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="249d5-144">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="249d5-145">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="249d5-145">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)
