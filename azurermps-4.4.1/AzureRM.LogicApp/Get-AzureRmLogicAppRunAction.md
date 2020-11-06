---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunAction.md
ms.openlocfilehash: 49968330f56fe0891adb9c5a62a1264700f53224
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454347"
---
# <span data-ttu-id="785f7-101">Get-AzureRmLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="785f7-101">Get-AzureRmLogicAppRunAction</span></span>

## <span data-ttu-id="785f7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="785f7-102">SYNOPSIS</span></span>
<span data-ttu-id="785f7-103">從邏輯 app 執行中取得動作。</span><span class="sxs-lookup"><span data-stu-id="785f7-103">Gets an action from a logic app run.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="785f7-104">句法</span><span class="sxs-lookup"><span data-stu-id="785f7-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String>
 [-ActionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="785f7-105">說明</span><span class="sxs-lookup"><span data-stu-id="785f7-105">DESCRIPTION</span></span>
<span data-ttu-id="785f7-106">**AzureRmLogicAppRunAction** Cmdlet 會從邏輯 app 執行中取得動作。</span><span class="sxs-lookup"><span data-stu-id="785f7-106">The **Get-AzureRmLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="785f7-107">這個 Cmdlet 會傳回 **WorkflowRunAction** 物件。</span><span class="sxs-lookup"><span data-stu-id="785f7-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="785f7-108">指定邏輯 app、資源群組和執行。</span><span class="sxs-lookup"><span data-stu-id="785f7-108">Specify the logic app, resource group, and run.</span></span>

<span data-ttu-id="785f7-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="785f7-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="785f7-110">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="785f7-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="785f7-111">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="785f7-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="785f7-112">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="785f7-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="785f7-113">示例</span><span class="sxs-lookup"><span data-stu-id="785f7-113">EXAMPLES</span></span>

### <span data-ttu-id="785f7-114">範例1：從邏輯 App 執行中取得動作</span><span class="sxs-lookup"><span data-stu-id="785f7-114">Example 1: Get an action from a Logic App run</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56" -ActionName "LogicAppAction01"
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

<span data-ttu-id="785f7-115">這個命令會從執行命名 LogicAppRun56 的名為 LogicApp05 的邏輯 app 取得特定的邏輯 App 動作。</span><span class="sxs-lookup"><span data-stu-id="785f7-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run named LogicAppRun56.</span></span>

### <span data-ttu-id="785f7-116">範例2：從邏輯 App 執行中取得所有動作</span><span class="sxs-lookup"><span data-stu-id="785f7-116">Example 2: Get all the actions from a Logic App run</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56"
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

<span data-ttu-id="785f7-117">這個命令會從名為 LogicApp05 的邏輯 app 的 run 命名 LogicAppRun56 中取得所有邏輯 App 動作。</span><span class="sxs-lookup"><span data-stu-id="785f7-117">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span>

## <span data-ttu-id="785f7-118">參數</span><span class="sxs-lookup"><span data-stu-id="785f7-118">PARAMETERS</span></span>

### <span data-ttu-id="785f7-119">-ActionName</span><span class="sxs-lookup"><span data-stu-id="785f7-119">-ActionName</span></span>
<span data-ttu-id="785f7-120">指定邏輯 app 執行中動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="785f7-120">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="785f7-121">這個 Cmdlet 會取得此參數指定的動作。</span><span class="sxs-lookup"><span data-stu-id="785f7-121">This cmdlet gets the action that this parameter specifies.</span></span>

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

### <span data-ttu-id="785f7-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="785f7-122">-Name</span></span>
<span data-ttu-id="785f7-123">指定此 Cmdlet 取得動作的邏輯 app 名稱。</span><span class="sxs-lookup"><span data-stu-id="785f7-123">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="785f7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="785f7-124">-ResourceGroupName</span></span>
<span data-ttu-id="785f7-125">指定此 Cmdlet 在其中取得動作之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="785f7-125">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="785f7-126">-RunName</span><span class="sxs-lookup"><span data-stu-id="785f7-126">-RunName</span></span>
<span data-ttu-id="785f7-127">指定邏輯 app 執行的名稱。</span><span class="sxs-lookup"><span data-stu-id="785f7-127">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="785f7-128">這個 Cmdlet 會取得此參數指定的執行動作。</span><span class="sxs-lookup"><span data-stu-id="785f7-128">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="785f7-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="785f7-129">-DefaultProfile</span></span>
<span data-ttu-id="785f7-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="785f7-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="785f7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="785f7-131">CommonParameters</span></span>
<span data-ttu-id="785f7-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="785f7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="785f7-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="785f7-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="785f7-134">輸入</span><span class="sxs-lookup"><span data-stu-id="785f7-134">INPUTS</span></span>

## <span data-ttu-id="785f7-135">輸出</span><span class="sxs-lookup"><span data-stu-id="785f7-135">OUTPUTS</span></span>

### <span data-ttu-id="785f7-136">WorkflowRunAction 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="785f7-136">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="785f7-137">筆記</span><span class="sxs-lookup"><span data-stu-id="785f7-137">NOTES</span></span>

## <span data-ttu-id="785f7-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="785f7-138">RELATED LINKS</span></span>

[<span data-ttu-id="785f7-139">AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="785f7-139">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="785f7-140">停止 AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="785f7-140">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)


