---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
ms.openlocfilehash: ed8a8c198f626d569d47a9b06b6d9595517f2f69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457563"
---
# <span data-ttu-id="d7df4-101">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="d7df4-101">Start-AzureRmLogicApp</span></span>

## <span data-ttu-id="d7df4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d7df4-102">SYNOPSIS</span></span>
<span data-ttu-id="d7df4-103">在資源群組中執行邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="d7df4-103">Runs a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7df4-104">句法</span><span class="sxs-lookup"><span data-stu-id="d7df4-104">SYNTAX</span></span>

```
Start-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7df4-105">說明</span><span class="sxs-lookup"><span data-stu-id="d7df4-105">DESCRIPTION</span></span>
<span data-ttu-id="d7df4-106">**AzureRmLogicApp** Cmdlet 會使用邏輯應用程式功能來執行邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="d7df4-106">The **Start-AzureRmLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="d7df4-107">指定名稱、資源群組及觸發程式。</span><span class="sxs-lookup"><span data-stu-id="d7df4-107">Specify a name, resource group, and trigger.</span></span>

<span data-ttu-id="d7df4-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="d7df4-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d7df4-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="d7df4-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d7df4-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="d7df4-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d7df4-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="d7df4-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d7df4-112">示例</span><span class="sxs-lookup"><span data-stu-id="d7df4-112">EXAMPLES</span></span>

### <span data-ttu-id="d7df4-113">範例1：執行邏輯 app</span><span class="sxs-lookup"><span data-stu-id="d7df4-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="d7df4-114">這個命令會在名為 ResourceGroup11 的資源群組中執行邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="d7df4-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="d7df4-115">參數</span><span class="sxs-lookup"><span data-stu-id="d7df4-115">PARAMETERS</span></span>

### <span data-ttu-id="d7df4-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="d7df4-116">-Name</span></span>
<span data-ttu-id="d7df4-117">指定此 Cmdlet 啟動之邏輯應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7df4-117">Specifies the name of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="d7df4-118">-參數</span><span class="sxs-lookup"><span data-stu-id="d7df4-118">-Parameters</span></span>
<span data-ttu-id="d7df4-119">指定邏輯 app 的參數集合物件。</span><span class="sxs-lookup"><span data-stu-id="d7df4-119">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="d7df4-120">指定雜湊資料表、字典 \<string\> 或字典 \<string, WorkflowParameter\> 。</span><span class="sxs-lookup"><span data-stu-id="d7df4-120">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="d7df4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7df4-121">-ResourceGroupName</span></span>
<span data-ttu-id="d7df4-122">指定包含此 Cmdlet 啟動之邏輯 app 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7df4-122">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="d7df4-123">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="d7df4-123">-TriggerName</span></span>
<span data-ttu-id="d7df4-124">指定此 Cmdlet 啟動之邏輯 app 之觸發程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7df4-124">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="d7df4-125">-確認</span><span class="sxs-lookup"><span data-stu-id="d7df4-125">-Confirm</span></span>
<span data-ttu-id="d7df4-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d7df4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7df4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7df4-127">-WhatIf</span></span>
<span data-ttu-id="d7df4-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d7df4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7df4-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d7df4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7df4-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7df4-130">-DefaultProfile</span></span>
<span data-ttu-id="d7df4-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d7df4-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7df4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7df4-132">CommonParameters</span></span>
<span data-ttu-id="d7df4-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d7df4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7df4-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d7df4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7df4-135">輸入</span><span class="sxs-lookup"><span data-stu-id="d7df4-135">INPUTS</span></span>

## <span data-ttu-id="d7df4-136">輸出</span><span class="sxs-lookup"><span data-stu-id="d7df4-136">OUTPUTS</span></span>

### <span data-ttu-id="d7df4-137">System.object</span><span class="sxs-lookup"><span data-stu-id="d7df4-137">System.Object</span></span>

## <span data-ttu-id="d7df4-138">筆記</span><span class="sxs-lookup"><span data-stu-id="d7df4-138">NOTES</span></span>

## <span data-ttu-id="d7df4-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="d7df4-139">RELATED LINKS</span></span>

[<span data-ttu-id="d7df4-140">AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="d7df4-140">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="d7df4-141">AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="d7df4-141">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="d7df4-142">新-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="d7df4-142">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="d7df4-143">移除-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="d7df4-143">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="d7df4-144">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="d7df4-144">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="d7df4-145">停止 AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="d7df4-145">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)


