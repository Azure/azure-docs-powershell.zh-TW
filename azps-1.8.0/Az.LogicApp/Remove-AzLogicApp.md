---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
ms.openlocfilehash: 3458eef92b18ea5407724a2ad1b0cb2e10024233
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787045"
---
# <span data-ttu-id="d58ef-101">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="d58ef-101">Remove-AzLogicApp</span></span>

## <span data-ttu-id="d58ef-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d58ef-102">SYNOPSIS</span></span>
<span data-ttu-id="d58ef-103">從資源群組中移除邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="d58ef-103">Removes a logic app from a resource group.</span></span>

## <span data-ttu-id="d58ef-104">句法</span><span class="sxs-lookup"><span data-stu-id="d58ef-104">SYNTAX</span></span>

```
Remove-AzLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d58ef-105">說明</span><span class="sxs-lookup"><span data-stu-id="d58ef-105">DESCRIPTION</span></span>
<span data-ttu-id="d58ef-106">**AzLogicApp** Cmdlet 會使用邏輯應用程式功能，從資源群組中移除邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="d58ef-106">The **Remove-AzLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="d58ef-107">指定邏輯 app 與資源群組。</span><span class="sxs-lookup"><span data-stu-id="d58ef-107">Specify the logic app and resource group.</span></span>
<span data-ttu-id="d58ef-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="d58ef-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d58ef-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="d58ef-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d58ef-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="d58ef-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d58ef-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="d58ef-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d58ef-112">示例</span><span class="sxs-lookup"><span data-stu-id="d58ef-112">EXAMPLES</span></span>

### <span data-ttu-id="d58ef-113">範例1：移除邏輯 app</span><span class="sxs-lookup"><span data-stu-id="d58ef-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="d58ef-114">這個命令會從資源群組中移除邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="d58ef-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="d58ef-115">此命令包含 *Force* 參數，可防止命令提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d58ef-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="d58ef-116">參數</span><span class="sxs-lookup"><span data-stu-id="d58ef-116">PARAMETERS</span></span>

### <span data-ttu-id="d58ef-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d58ef-117">-DefaultProfile</span></span>
<span data-ttu-id="d58ef-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d58ef-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d58ef-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d58ef-119">-Force</span></span>
<span data-ttu-id="d58ef-120">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="d58ef-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d58ef-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d58ef-121">-Name</span></span>
<span data-ttu-id="d58ef-122">指定此 Cmdlet 移除之邏輯應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="d58ef-122">Specifies the name of the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d58ef-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d58ef-123">-ResourceGroupName</span></span>
<span data-ttu-id="d58ef-124">指定包含此 Cmdlet 移除之邏輯 app 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d58ef-124">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d58ef-125">-確認</span><span class="sxs-lookup"><span data-stu-id="d58ef-125">-Confirm</span></span>
<span data-ttu-id="d58ef-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d58ef-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d58ef-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d58ef-127">-WhatIf</span></span>
<span data-ttu-id="d58ef-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d58ef-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d58ef-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d58ef-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d58ef-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d58ef-130">CommonParameters</span></span>
<span data-ttu-id="d58ef-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d58ef-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d58ef-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d58ef-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d58ef-133">輸入</span><span class="sxs-lookup"><span data-stu-id="d58ef-133">INPUTS</span></span>

### <span data-ttu-id="d58ef-134">System.object</span><span class="sxs-lookup"><span data-stu-id="d58ef-134">System.String</span></span>

## <span data-ttu-id="d58ef-135">輸出</span><span class="sxs-lookup"><span data-stu-id="d58ef-135">OUTPUTS</span></span>

### <span data-ttu-id="d58ef-136">System.void</span><span class="sxs-lookup"><span data-stu-id="d58ef-136">System.Void</span></span>

## <span data-ttu-id="d58ef-137">筆記</span><span class="sxs-lookup"><span data-stu-id="d58ef-137">NOTES</span></span>

## <span data-ttu-id="d58ef-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="d58ef-138">RELATED LINKS</span></span>

[<span data-ttu-id="d58ef-139">AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="d58ef-139">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="d58ef-140">新-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="d58ef-140">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="d58ef-141">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="d58ef-141">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="d58ef-142">開始-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="d58ef-142">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

