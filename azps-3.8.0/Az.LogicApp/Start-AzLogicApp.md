---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/start-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
ms.openlocfilehash: e93efdaf8ec55c3b7c8fb0793a24e062553545ff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956357"
---
# <span data-ttu-id="387b0-101">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="387b0-101">Start-AzLogicApp</span></span>

## <span data-ttu-id="387b0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="387b0-102">SYNOPSIS</span></span>
<span data-ttu-id="387b0-103">在資源群組中執行邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="387b0-103">Runs a logic app in a resource group.</span></span>

## <span data-ttu-id="387b0-104">句法</span><span class="sxs-lookup"><span data-stu-id="387b0-104">SYNTAX</span></span>

```
Start-AzLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="387b0-105">說明</span><span class="sxs-lookup"><span data-stu-id="387b0-105">DESCRIPTION</span></span>
<span data-ttu-id="387b0-106">**AzLogicApp** Cmdlet 會使用邏輯應用程式功能來執行邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="387b0-106">The **Start-AzLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="387b0-107">指定名稱、資源群組及觸發程式。</span><span class="sxs-lookup"><span data-stu-id="387b0-107">Specify a name, resource group, and trigger.</span></span>
<span data-ttu-id="387b0-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="387b0-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="387b0-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="387b0-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="387b0-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="387b0-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="387b0-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="387b0-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="387b0-112">示例</span><span class="sxs-lookup"><span data-stu-id="387b0-112">EXAMPLES</span></span>

### <span data-ttu-id="387b0-113">範例1：執行邏輯 app</span><span class="sxs-lookup"><span data-stu-id="387b0-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="387b0-114">這個命令會在名為 ResourceGroup11 的資源群組中執行邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="387b0-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="387b0-115">參數</span><span class="sxs-lookup"><span data-stu-id="387b0-115">PARAMETERS</span></span>

### <span data-ttu-id="387b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="387b0-116">-DefaultProfile</span></span>
<span data-ttu-id="387b0-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="387b0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="387b0-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="387b0-118">-Name</span></span>
<span data-ttu-id="387b0-119">指定此 Cmdlet 啟動之邏輯應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="387b0-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="387b0-120">-參數</span><span class="sxs-lookup"><span data-stu-id="387b0-120">-Parameters</span></span>
<span data-ttu-id="387b0-121">指定邏輯 app 的參數集合物件。</span><span class="sxs-lookup"><span data-stu-id="387b0-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="387b0-122">指定雜湊資料表、字典 \< 字串 \> 或字典 \< 字串（WorkflowParameter） \> 。</span><span class="sxs-lookup"><span data-stu-id="387b0-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387b0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="387b0-123">-ResourceGroupName</span></span>
<span data-ttu-id="387b0-124">指定包含此 Cmdlet 啟動之邏輯 app 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="387b0-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="387b0-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="387b0-125">-TriggerName</span></span>
<span data-ttu-id="387b0-126">指定此 Cmdlet 啟動之邏輯 app 之觸發程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="387b0-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="387b0-127">-確認</span><span class="sxs-lookup"><span data-stu-id="387b0-127">-Confirm</span></span>
<span data-ttu-id="387b0-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="387b0-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387b0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="387b0-129">-WhatIf</span></span>
<span data-ttu-id="387b0-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="387b0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="387b0-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="387b0-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387b0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="387b0-132">CommonParameters</span></span>
<span data-ttu-id="387b0-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="387b0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="387b0-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="387b0-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="387b0-135">輸入</span><span class="sxs-lookup"><span data-stu-id="387b0-135">INPUTS</span></span>

### <span data-ttu-id="387b0-136">System.object</span><span class="sxs-lookup"><span data-stu-id="387b0-136">System.String</span></span>

## <span data-ttu-id="387b0-137">輸出</span><span class="sxs-lookup"><span data-stu-id="387b0-137">OUTPUTS</span></span>

### <span data-ttu-id="387b0-138">System.void</span><span class="sxs-lookup"><span data-stu-id="387b0-138">System.Void</span></span>

## <span data-ttu-id="387b0-139">筆記</span><span class="sxs-lookup"><span data-stu-id="387b0-139">NOTES</span></span>

## <span data-ttu-id="387b0-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="387b0-140">RELATED LINKS</span></span>

[<span data-ttu-id="387b0-141">AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="387b0-141">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="387b0-142">AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="387b0-142">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="387b0-143">新-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="387b0-143">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="387b0-144">移除-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="387b0-144">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="387b0-145">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="387b0-145">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="387b0-146">停止 AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="387b0-146">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)

