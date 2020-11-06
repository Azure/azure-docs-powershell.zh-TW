---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 3308F901-4C9F-424D-8BEB-877A6038B246
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/stop-azurermlogicapprun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Stop-AzureRmLogicAppRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Stop-AzureRmLogicAppRun.md
ms.openlocfilehash: cd269c015870ab2a030ee44ebfd0f01874b674f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449779"
---
# <span data-ttu-id="0da2b-101">Stop-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="0da2b-101">Stop-AzureRmLogicAppRun</span></span>

## <span data-ttu-id="0da2b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0da2b-102">SYNOPSIS</span></span>
<span data-ttu-id="0da2b-103">取消邏輯 app 的執行。</span><span class="sxs-lookup"><span data-stu-id="0da2b-103">Cancels a run of a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0da2b-104">句法</span><span class="sxs-lookup"><span data-stu-id="0da2b-104">SYNTAX</span></span>

```
Stop-AzureRmLogicAppRun -ResourceGroupName <String> -Name <String> -RunName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0da2b-105">說明</span><span class="sxs-lookup"><span data-stu-id="0da2b-105">DESCRIPTION</span></span>
<span data-ttu-id="0da2b-106">**AzureRmLogicAppRun** Cmdlet 會取消邏輯 app 的執行。</span><span class="sxs-lookup"><span data-stu-id="0da2b-106">The **Stop-AzureRmLogicAppRun** cmdlet cancels a run of a logic app.</span></span>
<span data-ttu-id="0da2b-107">指定邏輯 app、資源群組和執行。</span><span class="sxs-lookup"><span data-stu-id="0da2b-107">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="0da2b-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="0da2b-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0da2b-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="0da2b-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0da2b-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="0da2b-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0da2b-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="0da2b-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0da2b-112">示例</span><span class="sxs-lookup"><span data-stu-id="0da2b-112">EXAMPLES</span></span>

### <span data-ttu-id="0da2b-113">範例1：取消邏輯 app 的執行</span><span class="sxs-lookup"><span data-stu-id="0da2b-113">Example 1: Cancel a run of a logic app</span></span>
```
PS C:\>Stop-AzureRmLogicAppRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -RunName "08587489104702792076" -Force
```

<span data-ttu-id="0da2b-114">這個命令會取消一個名為 LogicApp03 的邏輯 app 執行。</span><span class="sxs-lookup"><span data-stu-id="0da2b-114">This command cancels a run of the logic app named LogicApp03.</span></span>

## <span data-ttu-id="0da2b-115">參數</span><span class="sxs-lookup"><span data-stu-id="0da2b-115">PARAMETERS</span></span>

### <span data-ttu-id="0da2b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0da2b-116">-DefaultProfile</span></span>
<span data-ttu-id="0da2b-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0da2b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0da2b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0da2b-118">-Force</span></span>
<span data-ttu-id="0da2b-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="0da2b-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0da2b-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="0da2b-120">-Name</span></span>
<span data-ttu-id="0da2b-121">指定此 Cmdlet 取消執行的邏輯 app 名稱。</span><span class="sxs-lookup"><span data-stu-id="0da2b-121">Specifies the name of a logic app for which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="0da2b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0da2b-122">-ResourceGroupName</span></span>
<span data-ttu-id="0da2b-123">指定此 Cmdlet 在其中取消執行的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0da2b-123">Specifies the name for a resource group in which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="0da2b-124">-RunName</span><span class="sxs-lookup"><span data-stu-id="0da2b-124">-RunName</span></span>
<span data-ttu-id="0da2b-125">指定此 Cmdlet 取消的邏輯 app 執行的名稱。</span><span class="sxs-lookup"><span data-stu-id="0da2b-125">Specifies the name of a logic app run that this cmdlet cancels.</span></span>

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

### <span data-ttu-id="0da2b-126">-確認</span><span class="sxs-lookup"><span data-stu-id="0da2b-126">-Confirm</span></span>
<span data-ttu-id="0da2b-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0da2b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0da2b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0da2b-128">-WhatIf</span></span>
<span data-ttu-id="0da2b-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0da2b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0da2b-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0da2b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0da2b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0da2b-131">CommonParameters</span></span>
<span data-ttu-id="0da2b-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0da2b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0da2b-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0da2b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0da2b-134">輸入</span><span class="sxs-lookup"><span data-stu-id="0da2b-134">INPUTS</span></span>

### <span data-ttu-id="0da2b-135">System.object</span><span class="sxs-lookup"><span data-stu-id="0da2b-135">System.String</span></span>

## <span data-ttu-id="0da2b-136">輸出</span><span class="sxs-lookup"><span data-stu-id="0da2b-136">OUTPUTS</span></span>

### <span data-ttu-id="0da2b-137">System.void</span><span class="sxs-lookup"><span data-stu-id="0da2b-137">System.Void</span></span>

## <span data-ttu-id="0da2b-138">筆記</span><span class="sxs-lookup"><span data-stu-id="0da2b-138">NOTES</span></span>

## <span data-ttu-id="0da2b-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="0da2b-139">RELATED LINKS</span></span>

[<span data-ttu-id="0da2b-140">開始-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="0da2b-140">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)

