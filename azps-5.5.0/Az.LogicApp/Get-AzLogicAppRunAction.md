---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
ms.openlocfilehash: 175667480977e55cc93486f252a8f84080c64b5e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129199"
---
# <span data-ttu-id="9edb8-101">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="9edb8-101">Get-AzLogicAppRunAction</span></span>

## <span data-ttu-id="9edb8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9edb8-102">SYNOPSIS</span></span>

<span data-ttu-id="9edb8-103">從邏輯 app 執行中取得動作。</span><span class="sxs-lookup"><span data-stu-id="9edb8-103">Gets an action from a logic app run.</span></span>

## <span data-ttu-id="9edb8-104">句法</span><span class="sxs-lookup"><span data-stu-id="9edb8-104">SYNTAX</span></span>

```powershell
Get-AzLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String> [-ActionName <String>]
 [-FollowNextPageLink] [-MaximumFollowNextPageLink <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9edb8-105">說明</span><span class="sxs-lookup"><span data-stu-id="9edb8-105">DESCRIPTION</span></span>

<span data-ttu-id="9edb8-106">**AzLogicAppRunAction** Cmdlet 會從邏輯 app 執行中取得動作。</span><span class="sxs-lookup"><span data-stu-id="9edb8-106">The **Get-AzLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="9edb8-107">這個 Cmdlet 會傳回 **WorkflowRunAction** 物件。</span><span class="sxs-lookup"><span data-stu-id="9edb8-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="9edb8-108">指定邏輯 app、資源群組和執行。</span><span class="sxs-lookup"><span data-stu-id="9edb8-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="9edb8-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="9edb8-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="9edb8-110">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="9edb8-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="9edb8-111">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="9edb8-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="9edb8-112">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="9edb8-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="9edb8-113">示例</span><span class="sxs-lookup"><span data-stu-id="9edb8-113">EXAMPLES</span></span>

### <span data-ttu-id="9edb8-114">範例1：從邏輯 App 執行中取得動作</span><span class="sxs-lookup"><span data-stu-id="9edb8-114">Example 1: Get an action from a Logic App run</span></span>

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

<span data-ttu-id="9edb8-115">這個命令會針對執行識別碼08585925184423369718380498702CU26 的 LogicApp05，從名為 [run] 的邏輯 app 取得特定的邏輯 App 動作。</span><span class="sxs-lookup"><span data-stu-id="9edb8-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run with identifier 08585925184423369718380498702CU26.</span></span>

### <span data-ttu-id="9edb8-116">範例2：從邏輯 App 執行中取得所有動作</span><span class="sxs-lookup"><span data-stu-id="9edb8-116">Example 2: Get all the actions from a Logic App run</span></span>

```powershell
PS C:\>Get-AzLogicAppRunAction -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "08585925184423369718380498702CU26" -FollowNextPageLink
```

<span data-ttu-id="9edb8-117">這個命令會從執行中取得名為 LogicApp05 之邏輯 app 之識別碼08585925184423369718380498702CU26 的所有邏輯 App 動作。</span><span class="sxs-lookup"><span data-stu-id="9edb8-117">This command gets all Logic App actions from a run with identifier 08585925184423369718380498702CU26 of a logic app named LogicApp05.</span></span>

## <span data-ttu-id="9edb8-118">參數</span><span class="sxs-lookup"><span data-stu-id="9edb8-118">PARAMETERS</span></span>

### <span data-ttu-id="9edb8-119">-ActionName</span><span class="sxs-lookup"><span data-stu-id="9edb8-119">-ActionName</span></span>

<span data-ttu-id="9edb8-120">指定邏輯 app 執行中動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="9edb8-120">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="9edb8-121">這個 Cmdlet 會取得此參數指定的動作。</span><span class="sxs-lookup"><span data-stu-id="9edb8-121">This cmdlet gets the action that this parameter specifies.</span></span>

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

### <span data-ttu-id="9edb8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9edb8-122">-DefaultProfile</span></span>

<span data-ttu-id="9edb8-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9edb8-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9edb8-124">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="9edb8-124">-FollowNextPageLink</span></span>

<span data-ttu-id="9edb8-125">表示 Cmdlet 應該跟隨 [下一頁連結]。</span><span class="sxs-lookup"><span data-stu-id="9edb8-125">Indicates the cmdlet should follow next page links.</span></span>

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

### <span data-ttu-id="9edb8-126">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="9edb8-126">-MaximumFollowNextPageLink</span></span>

<span data-ttu-id="9edb8-127">指定在使用 FollowNextPageLink 時，追蹤下一個頁面連結的次數。</span><span class="sxs-lookup"><span data-stu-id="9edb8-127">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

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

### <span data-ttu-id="9edb8-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="9edb8-128">-Name</span></span>

<span data-ttu-id="9edb8-129">指定此 Cmdlet 取得動作的邏輯 app 名稱。</span><span class="sxs-lookup"><span data-stu-id="9edb8-129">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="9edb8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9edb8-130">-ResourceGroupName</span></span>

<span data-ttu-id="9edb8-131">指定此 Cmdlet 在其中取得動作之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9edb8-131">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="9edb8-132">-RunName</span><span class="sxs-lookup"><span data-stu-id="9edb8-132">-RunName</span></span>

<span data-ttu-id="9edb8-133">指定邏輯 app 執行的名稱。</span><span class="sxs-lookup"><span data-stu-id="9edb8-133">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="9edb8-134">這個 Cmdlet 會取得此參數指定的執行動作。</span><span class="sxs-lookup"><span data-stu-id="9edb8-134">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="9edb8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9edb8-135">CommonParameters</span></span>

<span data-ttu-id="9edb8-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9edb8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9edb8-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9edb8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9edb8-138">輸入</span><span class="sxs-lookup"><span data-stu-id="9edb8-138">INPUTS</span></span>

### <span data-ttu-id="9edb8-139">System.object</span><span class="sxs-lookup"><span data-stu-id="9edb8-139">System.String</span></span>

## <span data-ttu-id="9edb8-140">輸出</span><span class="sxs-lookup"><span data-stu-id="9edb8-140">OUTPUTS</span></span>

### <span data-ttu-id="9edb8-141">WorkflowRunAction 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="9edb8-141">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="9edb8-142">筆記</span><span class="sxs-lookup"><span data-stu-id="9edb8-142">NOTES</span></span>

## <span data-ttu-id="9edb8-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="9edb8-143">RELATED LINKS</span></span>

[<span data-ttu-id="9edb8-144">AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="9edb8-144">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="9edb8-145">停止 AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="9edb8-145">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)
