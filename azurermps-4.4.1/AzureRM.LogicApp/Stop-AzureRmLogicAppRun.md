---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 3308F901-4C9F-424D-8BEB-877A6038B246
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Stop-AzureRmLogicAppRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Stop-AzureRmLogicAppRun.md
ms.openlocfilehash: c6c2c356557d2d9d40a4012a7deee5aec0e73aa4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457559"
---
# <span data-ttu-id="b3210-101">Stop-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="b3210-101">Stop-AzureRmLogicAppRun</span></span>

## <span data-ttu-id="b3210-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b3210-102">SYNOPSIS</span></span>
<span data-ttu-id="b3210-103">取消邏輯 app 的執行。</span><span class="sxs-lookup"><span data-stu-id="b3210-103">Cancels a run of a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3210-104">句法</span><span class="sxs-lookup"><span data-stu-id="b3210-104">SYNTAX</span></span>

```
Stop-AzureRmLogicAppRun -ResourceGroupName <String> -Name <String> -RunName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3210-105">說明</span><span class="sxs-lookup"><span data-stu-id="b3210-105">DESCRIPTION</span></span>
<span data-ttu-id="b3210-106">**AzureRmLogicAppRun** Cmdlet 會取消邏輯 app 的執行。</span><span class="sxs-lookup"><span data-stu-id="b3210-106">The **Stop-AzureRmLogicAppRun** cmdlet cancels a run of a logic app.</span></span>
<span data-ttu-id="b3210-107">指定邏輯 app、資源群組和執行。</span><span class="sxs-lookup"><span data-stu-id="b3210-107">Specify the logic app, resource group, and run.</span></span>

<span data-ttu-id="b3210-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="b3210-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b3210-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="b3210-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b3210-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="b3210-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b3210-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="b3210-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b3210-112">示例</span><span class="sxs-lookup"><span data-stu-id="b3210-112">EXAMPLES</span></span>

### <span data-ttu-id="b3210-113">範例1：取消邏輯 app 的執行</span><span class="sxs-lookup"><span data-stu-id="b3210-113">Example 1: Cancel a run of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -RunName "08587489104702792076"
```

<span data-ttu-id="b3210-114">這個命令會取消一個名為 LogicApp03 的邏輯 app 執行。</span><span class="sxs-lookup"><span data-stu-id="b3210-114">This command cancels a run of the logic app named LogicApp03.</span></span>

## <span data-ttu-id="b3210-115">參數</span><span class="sxs-lookup"><span data-stu-id="b3210-115">PARAMETERS</span></span>

### <span data-ttu-id="b3210-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b3210-116">-Force</span></span>
<span data-ttu-id="b3210-117">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b3210-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b3210-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="b3210-118">-Name</span></span>
<span data-ttu-id="b3210-119">指定此 Cmdlet 取消執行的邏輯 app 名稱。</span><span class="sxs-lookup"><span data-stu-id="b3210-119">Specifies the name of a logic app for which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="b3210-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3210-120">-ResourceGroupName</span></span>
<span data-ttu-id="b3210-121">指定此 Cmdlet 在其中取消執行的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3210-121">Specifies the name for a resource group in which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="b3210-122">-RunName</span><span class="sxs-lookup"><span data-stu-id="b3210-122">-RunName</span></span>
<span data-ttu-id="b3210-123">指定此 Cmdlet 取消的邏輯 app 執行的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3210-123">Specifies the name of a logic app run that this cmdlet cancels.</span></span>

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

### <span data-ttu-id="b3210-124">-確認</span><span class="sxs-lookup"><span data-stu-id="b3210-124">-Confirm</span></span>
<span data-ttu-id="b3210-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b3210-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3210-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3210-126">-WhatIf</span></span>
<span data-ttu-id="b3210-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b3210-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3210-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3210-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3210-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3210-129">-DefaultProfile</span></span>
<span data-ttu-id="b3210-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3210-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3210-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3210-131">CommonParameters</span></span>
<span data-ttu-id="b3210-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b3210-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3210-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b3210-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3210-134">輸入</span><span class="sxs-lookup"><span data-stu-id="b3210-134">INPUTS</span></span>

## <span data-ttu-id="b3210-135">輸出</span><span class="sxs-lookup"><span data-stu-id="b3210-135">OUTPUTS</span></span>

### <span data-ttu-id="b3210-136">System.object</span><span class="sxs-lookup"><span data-stu-id="b3210-136">System.Object</span></span>

## <span data-ttu-id="b3210-137">筆記</span><span class="sxs-lookup"><span data-stu-id="b3210-137">NOTES</span></span>

## <span data-ttu-id="b3210-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3210-138">RELATED LINKS</span></span>

[<span data-ttu-id="b3210-139">開始-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="b3210-139">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


