---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
ms.openlocfilehash: c382b4bb9a02150beaa6880fd88d8f7b376b7c34
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281221"
---
# <span data-ttu-id="db126-101">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="db126-101">Get-AzLogicAppRunAction</span></span>

## <span data-ttu-id="db126-102">摘要</span><span class="sxs-lookup"><span data-stu-id="db126-102">SYNOPSIS</span></span>
<span data-ttu-id="db126-103">從邏輯 app 執行中取得動作。</span><span class="sxs-lookup"><span data-stu-id="db126-103">Gets an action from a logic app run.</span></span>

## <span data-ttu-id="db126-104">句法</span><span class="sxs-lookup"><span data-stu-id="db126-104">SYNTAX</span></span>

```
Get-AzLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String> [-ActionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db126-105">說明</span><span class="sxs-lookup"><span data-stu-id="db126-105">DESCRIPTION</span></span>
<span data-ttu-id="db126-106">**AzLogicAppRunAction** Cmdlet 會從邏輯 app 執行中取得動作。</span><span class="sxs-lookup"><span data-stu-id="db126-106">The **Get-AzLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="db126-107">這個 Cmdlet 會傳回 **WorkflowRunAction** 物件。</span><span class="sxs-lookup"><span data-stu-id="db126-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="db126-108">指定邏輯 app、資源群組和執行。</span><span class="sxs-lookup"><span data-stu-id="db126-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="db126-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="db126-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="db126-110">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="db126-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="db126-111">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="db126-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="db126-112">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="db126-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="db126-113">示例</span><span class="sxs-lookup"><span data-stu-id="db126-113">EXAMPLES</span></span>

### <span data-ttu-id="db126-114">範例1：從邏輯 App 執行中取得動作</span><span class="sxs-lookup"><span data-stu-id="db126-114">Example 1: Get an action from a Logic App run</span></span>
```powershell
PS C:\>Get-AzLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56" -ActionName "LogicAppAction01"
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

<span data-ttu-id="db126-115">這個命令會從執行命名 LogicAppRun56 的名為 LogicApp05 的邏輯 app 取得特定的邏輯 App 動作。</span><span class="sxs-lookup"><span data-stu-id="db126-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run named LogicAppRun56.</span></span>

### <span data-ttu-id="db126-116">範例2：從邏輯 App 執行中取得所有動作</span><span class="sxs-lookup"><span data-stu-id="db126-116">Example 2: Get all the actions from a Logic App run</span></span>
```powershell
PS C:\>Get-AzLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56"
Code        : NotFound
EndTime     : 1/13/2016 2:42:56 PM
Error       : 
InputsLink  : Microsoft.Azure.Management.Logic.Models.ContentLink
Name        : LogicAppAction1
OutputsLink : Microsoft.Azure.Management.Logic.Models.ContentLink
StartTime   : 1/13/2016 2:42:55 PM
Status      : Failed
TrackingId  : 
Type        :
```

<span data-ttu-id="db126-117">這個命令會從名為 LogicApp05 的邏輯 app 的 run 命名 LogicAppRun56 中取得所有邏輯 App 動作。</span><span class="sxs-lookup"><span data-stu-id="db126-117">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span>

### <span data-ttu-id="db126-118">範例3</span><span class="sxs-lookup"><span data-stu-id="db126-118">Example 3</span></span>

<span data-ttu-id="db126-119">這個命令會從名為 LogicApp05 的邏輯 app 的 run 命名 LogicAppRun56 中取得所有邏輯 App 動作。</span><span class="sxs-lookup"><span data-stu-id="db126-119">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span> <span data-ttu-id="db126-120"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="db126-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzLogicAppRunAction -Name 'IntegrationAccount31' -ResourceGroupName MyResourceGroup -RunName '08587489104702792076'
```

## <span data-ttu-id="db126-121">參數</span><span class="sxs-lookup"><span data-stu-id="db126-121">PARAMETERS</span></span>

### <span data-ttu-id="db126-122">-ActionName</span><span class="sxs-lookup"><span data-stu-id="db126-122">-ActionName</span></span>
<span data-ttu-id="db126-123">指定邏輯 app 執行中動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="db126-123">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="db126-124">這個 Cmdlet 會取得此參數指定的動作。</span><span class="sxs-lookup"><span data-stu-id="db126-124">This cmdlet gets the action that this parameter specifies.</span></span>

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

### <span data-ttu-id="db126-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db126-125">-DefaultProfile</span></span>
<span data-ttu-id="db126-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="db126-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db126-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="db126-127">-Name</span></span>
<span data-ttu-id="db126-128">指定此 Cmdlet 取得動作的邏輯 app 名稱。</span><span class="sxs-lookup"><span data-stu-id="db126-128">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="db126-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db126-129">-ResourceGroupName</span></span>
<span data-ttu-id="db126-130">指定此 Cmdlet 在其中取得動作之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="db126-130">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="db126-131">-RunName</span><span class="sxs-lookup"><span data-stu-id="db126-131">-RunName</span></span>
<span data-ttu-id="db126-132">指定邏輯 app 執行的名稱。</span><span class="sxs-lookup"><span data-stu-id="db126-132">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="db126-133">這個 Cmdlet 會取得此參數指定的執行動作。</span><span class="sxs-lookup"><span data-stu-id="db126-133">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="db126-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db126-134">CommonParameters</span></span>
<span data-ttu-id="db126-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="db126-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db126-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="db126-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db126-137">輸入</span><span class="sxs-lookup"><span data-stu-id="db126-137">INPUTS</span></span>

### <span data-ttu-id="db126-138">System.object</span><span class="sxs-lookup"><span data-stu-id="db126-138">System.String</span></span>

## <span data-ttu-id="db126-139">輸出</span><span class="sxs-lookup"><span data-stu-id="db126-139">OUTPUTS</span></span>

### <span data-ttu-id="db126-140">WorkflowRunAction 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="db126-140">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="db126-141">筆記</span><span class="sxs-lookup"><span data-stu-id="db126-141">NOTES</span></span>

## <span data-ttu-id="db126-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="db126-142">RELATED LINKS</span></span>

[<span data-ttu-id="db126-143">AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="db126-143">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="db126-144">停止 AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="db126-144">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


