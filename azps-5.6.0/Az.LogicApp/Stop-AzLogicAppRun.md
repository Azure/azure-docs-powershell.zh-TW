---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 3308F901-4C9F-424D-8BEB-877A6038B246
online version: https://docs.microsoft.com/powershell/module/az.logicapp/stop-azlogicapprun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Stop-AzLogicAppRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Stop-AzLogicAppRun.md
ms.openlocfilehash: 975e819e4b52e1fa09bd8068b630f540e34e72bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902029"
---
# <span data-ttu-id="43da2-101">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="43da2-101">Stop-AzLogicAppRun</span></span>

## <span data-ttu-id="43da2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="43da2-102">SYNOPSIS</span></span>
<span data-ttu-id="43da2-103">取消邏輯應用程式的執行。</span><span class="sxs-lookup"><span data-stu-id="43da2-103">Cancels a run of a logic app.</span></span>

## <span data-ttu-id="43da2-104">語法</span><span class="sxs-lookup"><span data-stu-id="43da2-104">SYNTAX</span></span>

```
Stop-AzLogicAppRun -ResourceGroupName <String> -Name <String> -RunName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43da2-105">描述</span><span class="sxs-lookup"><span data-stu-id="43da2-105">DESCRIPTION</span></span>
<span data-ttu-id="43da2-106">**Stop-AzLogicAppRun** Cmdlet 會取消邏輯應用程式的執行。</span><span class="sxs-lookup"><span data-stu-id="43da2-106">The **Stop-AzLogicAppRun** cmdlet cancels a run of a logic app.</span></span>
<span data-ttu-id="43da2-107">指定邏輯應用程式、資源群組及執行。</span><span class="sxs-lookup"><span data-stu-id="43da2-107">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="43da2-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="43da2-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="43da2-109">若要使用動態參數，請于命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="43da2-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="43da2-110">若要探索動態參數的名稱，在 Cmdlet 名稱之後輸入連字號 (-) ，然後重複按 Tab 鍵以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="43da2-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="43da2-111">如果您省略必要的範本參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="43da2-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="43da2-112">例子</span><span class="sxs-lookup"><span data-stu-id="43da2-112">EXAMPLES</span></span>

### <span data-ttu-id="43da2-113">範例 1：取消執行邏輯應用程式</span><span class="sxs-lookup"><span data-stu-id="43da2-113">Example 1: Cancel a run of a logic app</span></span>
```
PS C:\>Stop-AzLogicAppRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -RunName "08587489104702792076" -Force
```

<span data-ttu-id="43da2-114">此命令會取消邏輯應用程式 LogicApp03 的執行。</span><span class="sxs-lookup"><span data-stu-id="43da2-114">This command cancels a run of the logic app named LogicApp03.</span></span>

## <span data-ttu-id="43da2-115">參數</span><span class="sxs-lookup"><span data-stu-id="43da2-115">PARAMETERS</span></span>

### <span data-ttu-id="43da2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43da2-116">-DefaultProfile</span></span>
<span data-ttu-id="43da2-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="43da2-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43da2-118">-強制</span><span class="sxs-lookup"><span data-stu-id="43da2-118">-Force</span></span>
<span data-ttu-id="43da2-119">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="43da2-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="43da2-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="43da2-120">-Name</span></span>
<span data-ttu-id="43da2-121">指定此 Cmdlet 取消執行的邏輯應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="43da2-121">Specifies the name of a logic app for which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="43da2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43da2-122">-ResourceGroupName</span></span>
<span data-ttu-id="43da2-123">指定此 Cmdlet 取消執行的資源組名。</span><span class="sxs-lookup"><span data-stu-id="43da2-123">Specifies the name for a resource group in which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="43da2-124">-RunName</span><span class="sxs-lookup"><span data-stu-id="43da2-124">-RunName</span></span>
<span data-ttu-id="43da2-125">指定此 Cmdlet 取消的邏輯應用程式執行名稱。</span><span class="sxs-lookup"><span data-stu-id="43da2-125">Specifies the name of a logic app run that this cmdlet cancels.</span></span>

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

### <span data-ttu-id="43da2-126">-確認</span><span class="sxs-lookup"><span data-stu-id="43da2-126">-Confirm</span></span>
<span data-ttu-id="43da2-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="43da2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43da2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43da2-128">-WhatIf</span></span>
<span data-ttu-id="43da2-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="43da2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43da2-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="43da2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43da2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43da2-131">CommonParameters</span></span>
<span data-ttu-id="43da2-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="43da2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43da2-133">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="43da2-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43da2-134">輸入</span><span class="sxs-lookup"><span data-stu-id="43da2-134">INPUTS</span></span>

### <span data-ttu-id="43da2-135">System.String</span><span class="sxs-lookup"><span data-stu-id="43da2-135">System.String</span></span>

## <span data-ttu-id="43da2-136">輸出</span><span class="sxs-lookup"><span data-stu-id="43da2-136">OUTPUTS</span></span>

### <span data-ttu-id="43da2-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="43da2-137">System.Void</span></span>

## <span data-ttu-id="43da2-138">筆記</span><span class="sxs-lookup"><span data-stu-id="43da2-138">NOTES</span></span>

## <span data-ttu-id="43da2-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="43da2-139">RELATED LINKS</span></span>

[<span data-ttu-id="43da2-140">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="43da2-140">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


