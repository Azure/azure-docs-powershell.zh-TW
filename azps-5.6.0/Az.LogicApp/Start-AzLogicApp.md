---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/powershell/module/az.logicapp/start-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
ms.openlocfilehash: c109839692ea20f1fbbcced50df9c4167322b1b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902037"
---
# <span data-ttu-id="09867-101">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="09867-101">Start-AzLogicApp</span></span>

## <span data-ttu-id="09867-102">簡介</span><span class="sxs-lookup"><span data-stu-id="09867-102">SYNOPSIS</span></span>
<span data-ttu-id="09867-103">在資源群組中執行邏輯應用程式。</span><span class="sxs-lookup"><span data-stu-id="09867-103">Runs a logic app in a resource group.</span></span>

## <span data-ttu-id="09867-104">語法</span><span class="sxs-lookup"><span data-stu-id="09867-104">SYNTAX</span></span>

```
Start-AzLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09867-105">描述</span><span class="sxs-lookup"><span data-stu-id="09867-105">DESCRIPTION</span></span>
<span data-ttu-id="09867-106">**Start-AzLogicApp** Cmdlet 會使用邏輯應用程式功能執行邏輯應用程式。</span><span class="sxs-lookup"><span data-stu-id="09867-106">The **Start-AzLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="09867-107">指定名稱、資源群組和觸發項。</span><span class="sxs-lookup"><span data-stu-id="09867-107">Specify a name, resource group, and trigger.</span></span>
<span data-ttu-id="09867-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="09867-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="09867-109">若要使用動態參數，請于命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="09867-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="09867-110">若要探索動態參數的名稱，在 Cmdlet 名稱之後輸入連字號 (-) ，然後重複按 Tab 鍵以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="09867-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="09867-111">如果您省略必要的範本參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="09867-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="09867-112">例子</span><span class="sxs-lookup"><span data-stu-id="09867-112">EXAMPLES</span></span>

### <span data-ttu-id="09867-113">範例 1：執行邏輯應用程式</span><span class="sxs-lookup"><span data-stu-id="09867-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="09867-114">此命令在名為 ResourceGroup11 的資源群組中執行邏輯應用程式。</span><span class="sxs-lookup"><span data-stu-id="09867-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="09867-115">參數</span><span class="sxs-lookup"><span data-stu-id="09867-115">PARAMETERS</span></span>

### <span data-ttu-id="09867-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09867-116">-DefaultProfile</span></span>
<span data-ttu-id="09867-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="09867-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09867-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="09867-118">-Name</span></span>
<span data-ttu-id="09867-119">指定此 Cmdlet 啟動的邏輯應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="09867-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="09867-120">-參數</span><span class="sxs-lookup"><span data-stu-id="09867-120">-Parameters</span></span>
<span data-ttu-id="09867-121">指定邏輯應用程式的參數集合物件。</span><span class="sxs-lookup"><span data-stu-id="09867-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="09867-122">指定雜湊表、字典 \<string\> 或字典 \<string, WorkflowParameter\> 。</span><span class="sxs-lookup"><span data-stu-id="09867-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="09867-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09867-123">-ResourceGroupName</span></span>
<span data-ttu-id="09867-124">指定包含此 Cmdlet 啟動之邏輯應用程式的資源組名。</span><span class="sxs-lookup"><span data-stu-id="09867-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="09867-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="09867-125">-TriggerName</span></span>
<span data-ttu-id="09867-126">指定此 Cmdlet 啟動之邏輯應用程式的觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="09867-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="09867-127">-確認</span><span class="sxs-lookup"><span data-stu-id="09867-127">-Confirm</span></span>
<span data-ttu-id="09867-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="09867-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09867-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09867-129">-WhatIf</span></span>
<span data-ttu-id="09867-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="09867-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09867-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="09867-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09867-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09867-132">CommonParameters</span></span>
<span data-ttu-id="09867-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="09867-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09867-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="09867-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09867-135">輸入</span><span class="sxs-lookup"><span data-stu-id="09867-135">INPUTS</span></span>

### <span data-ttu-id="09867-136">System.String</span><span class="sxs-lookup"><span data-stu-id="09867-136">System.String</span></span>

## <span data-ttu-id="09867-137">輸出</span><span class="sxs-lookup"><span data-stu-id="09867-137">OUTPUTS</span></span>

### <span data-ttu-id="09867-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="09867-138">System.Void</span></span>

## <span data-ttu-id="09867-139">筆記</span><span class="sxs-lookup"><span data-stu-id="09867-139">NOTES</span></span>

## <span data-ttu-id="09867-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="09867-140">RELATED LINKS</span></span>

[<span data-ttu-id="09867-141">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="09867-141">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="09867-142">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="09867-142">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="09867-143">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="09867-143">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="09867-144">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="09867-144">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="09867-145">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="09867-145">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="09867-146">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="09867-146">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


