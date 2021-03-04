---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
ms.openlocfilehash: f9feca370a2672b14252691711810f5de241aa78
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905382"
---
# <span data-ttu-id="9e410-101">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="9e410-101">Remove-AzLogicApp</span></span>

## <span data-ttu-id="9e410-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9e410-102">SYNOPSIS</span></span>
<span data-ttu-id="9e410-103">從資源群組移除邏輯應用程式。</span><span class="sxs-lookup"><span data-stu-id="9e410-103">Removes a logic app from a resource group.</span></span>

## <span data-ttu-id="9e410-104">語法</span><span class="sxs-lookup"><span data-stu-id="9e410-104">SYNTAX</span></span>

```
Remove-AzLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e410-105">描述</span><span class="sxs-lookup"><span data-stu-id="9e410-105">DESCRIPTION</span></span>
<span data-ttu-id="9e410-106">**Remove-AzLogicApp** Cmdlet 會使用邏輯應用程式功能，從資源群組移除邏輯應用程式。</span><span class="sxs-lookup"><span data-stu-id="9e410-106">The **Remove-AzLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="9e410-107">指定邏輯應用程式和資源群組。</span><span class="sxs-lookup"><span data-stu-id="9e410-107">Specify the logic app and resource group.</span></span>
<span data-ttu-id="9e410-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="9e410-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="9e410-109">若要使用動態參數，請于命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="9e410-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="9e410-110">若要探索動態參數的名稱，在 Cmdlet 名稱之後輸入連字號 (-) ，然後重複按 Tab 鍵以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="9e410-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="9e410-111">如果您省略必要的範本參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="9e410-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="9e410-112">例子</span><span class="sxs-lookup"><span data-stu-id="9e410-112">EXAMPLES</span></span>

### <span data-ttu-id="9e410-113">範例 1：移除邏輯應用程式</span><span class="sxs-lookup"><span data-stu-id="9e410-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="9e410-114">此命令會從資源群組移除邏輯應用程式。</span><span class="sxs-lookup"><span data-stu-id="9e410-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="9e410-115">命令包含 *Force* 參數，可防止命令提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9e410-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="9e410-116">參數</span><span class="sxs-lookup"><span data-stu-id="9e410-116">PARAMETERS</span></span>

### <span data-ttu-id="9e410-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e410-117">-DefaultProfile</span></span>
<span data-ttu-id="9e410-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="9e410-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e410-119">-強制</span><span class="sxs-lookup"><span data-stu-id="9e410-119">-Force</span></span>
<span data-ttu-id="9e410-120">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="9e410-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e410-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="9e410-121">-Name</span></span>
<span data-ttu-id="9e410-122">指定此 Cmdlet 移除的邏輯應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="9e410-122">Specifies the name of the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9e410-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e410-123">-ResourceGroupName</span></span>
<span data-ttu-id="9e410-124">指定包含此 Cmdlet 移除之邏輯應用程式的資源組名。</span><span class="sxs-lookup"><span data-stu-id="9e410-124">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9e410-125">-確認</span><span class="sxs-lookup"><span data-stu-id="9e410-125">-Confirm</span></span>
<span data-ttu-id="9e410-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9e410-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e410-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e410-127">-WhatIf</span></span>
<span data-ttu-id="9e410-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9e410-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e410-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9e410-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e410-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e410-130">CommonParameters</span></span>
<span data-ttu-id="9e410-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9e410-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e410-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="9e410-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e410-133">輸入</span><span class="sxs-lookup"><span data-stu-id="9e410-133">INPUTS</span></span>

### <span data-ttu-id="9e410-134">System.String</span><span class="sxs-lookup"><span data-stu-id="9e410-134">System.String</span></span>

## <span data-ttu-id="9e410-135">輸出</span><span class="sxs-lookup"><span data-stu-id="9e410-135">OUTPUTS</span></span>

### <span data-ttu-id="9e410-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="9e410-136">System.Void</span></span>

## <span data-ttu-id="9e410-137">筆記</span><span class="sxs-lookup"><span data-stu-id="9e410-137">NOTES</span></span>

## <span data-ttu-id="9e410-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e410-138">RELATED LINKS</span></span>

[<span data-ttu-id="9e410-139">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="9e410-139">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="9e410-140">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="9e410-140">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="9e410-141">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="9e410-141">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="9e410-142">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="9e410-142">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


