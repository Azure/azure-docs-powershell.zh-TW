---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/start-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
ms.openlocfilehash: fefe9da2d0339c22d0f41e1526d8664ff27a52d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626439"
---
# <span data-ttu-id="a94c0-101">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a94c0-101">Start-AzureRmLogicApp</span></span>

## <span data-ttu-id="a94c0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a94c0-102">SYNOPSIS</span></span>
<span data-ttu-id="a94c0-103">在資源群組中執行邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="a94c0-103">Runs a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a94c0-104">句法</span><span class="sxs-lookup"><span data-stu-id="a94c0-104">SYNTAX</span></span>

```
Start-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a94c0-105">說明</span><span class="sxs-lookup"><span data-stu-id="a94c0-105">DESCRIPTION</span></span>
<span data-ttu-id="a94c0-106">**AzureRmLogicApp** Cmdlet 會使用邏輯應用程式功能來執行邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="a94c0-106">The **Start-AzureRmLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="a94c0-107">指定名稱、資源群組及觸發程式。</span><span class="sxs-lookup"><span data-stu-id="a94c0-107">Specify a name, resource group, and trigger.</span></span>

<span data-ttu-id="a94c0-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="a94c0-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a94c0-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="a94c0-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a94c0-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="a94c0-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a94c0-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="a94c0-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a94c0-112">示例</span><span class="sxs-lookup"><span data-stu-id="a94c0-112">EXAMPLES</span></span>

### <span data-ttu-id="a94c0-113">範例1：執行邏輯 app</span><span class="sxs-lookup"><span data-stu-id="a94c0-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="a94c0-114">這個命令會在名為 ResourceGroup11 的資源群組中執行邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="a94c0-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="a94c0-115">參數</span><span class="sxs-lookup"><span data-stu-id="a94c0-115">PARAMETERS</span></span>

### <span data-ttu-id="a94c0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a94c0-116">-DefaultProfile</span></span>
<span data-ttu-id="a94c0-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a94c0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a94c0-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="a94c0-118">-Name</span></span>
<span data-ttu-id="a94c0-119">指定此 Cmdlet 啟動之邏輯應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="a94c0-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a94c0-120">-參數</span><span class="sxs-lookup"><span data-stu-id="a94c0-120">-Parameters</span></span>
<span data-ttu-id="a94c0-121">指定邏輯 app 的參數集合物件。</span><span class="sxs-lookup"><span data-stu-id="a94c0-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="a94c0-122">指定雜湊資料表、字典 \<string\> 或字典 \<string, WorkflowParameter\> 。</span><span class="sxs-lookup"><span data-stu-id="a94c0-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a94c0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a94c0-123">-ResourceGroupName</span></span>
<span data-ttu-id="a94c0-124">指定包含此 Cmdlet 啟動之邏輯 app 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a94c0-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a94c0-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="a94c0-125">-TriggerName</span></span>
<span data-ttu-id="a94c0-126">指定此 Cmdlet 啟動之邏輯 app 之觸發程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="a94c0-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a94c0-127">-確認</span><span class="sxs-lookup"><span data-stu-id="a94c0-127">-Confirm</span></span>
<span data-ttu-id="a94c0-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a94c0-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a94c0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a94c0-129">-WhatIf</span></span>
<span data-ttu-id="a94c0-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a94c0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a94c0-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a94c0-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a94c0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a94c0-132">CommonParameters</span></span>
<span data-ttu-id="a94c0-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a94c0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a94c0-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a94c0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a94c0-135">輸入</span><span class="sxs-lookup"><span data-stu-id="a94c0-135">INPUTS</span></span>

### <span data-ttu-id="a94c0-136">所有</span><span class="sxs-lookup"><span data-stu-id="a94c0-136">None</span></span>
<span data-ttu-id="a94c0-137">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="a94c0-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a94c0-138">輸出</span><span class="sxs-lookup"><span data-stu-id="a94c0-138">OUTPUTS</span></span>

### <span data-ttu-id="a94c0-139">System.object</span><span class="sxs-lookup"><span data-stu-id="a94c0-139">System.Object</span></span>

## <span data-ttu-id="a94c0-140">筆記</span><span class="sxs-lookup"><span data-stu-id="a94c0-140">NOTES</span></span>

## <span data-ttu-id="a94c0-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="a94c0-141">RELATED LINKS</span></span>

[<span data-ttu-id="a94c0-142">AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a94c0-142">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="a94c0-143">AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="a94c0-143">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="a94c0-144">新-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a94c0-144">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="a94c0-145">移除-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a94c0-145">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="a94c0-146">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a94c0-146">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="a94c0-147">停止 AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="a94c0-147">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)

