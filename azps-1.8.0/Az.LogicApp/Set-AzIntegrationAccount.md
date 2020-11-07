---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F6D9EA59-BA61-4117-8771-9B190424BFF8
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccount.md
ms.openlocfilehash: 8c4c97b1574777a05560f7faa64f0bb4a3476bb9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787041"
---
# <span data-ttu-id="d3693-101">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="d3693-101">Set-AzIntegrationAccount</span></span>

## <span data-ttu-id="d3693-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d3693-102">SYNOPSIS</span></span>
<span data-ttu-id="d3693-103">修改整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="d3693-103">Modifies an integration account.</span></span>

## <span data-ttu-id="d3693-104">句法</span><span class="sxs-lookup"><span data-stu-id="d3693-104">SYNTAX</span></span>

```
Set-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Location <String>] [-Sku <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3693-105">說明</span><span class="sxs-lookup"><span data-stu-id="d3693-105">DESCRIPTION</span></span>
<span data-ttu-id="d3693-106">**AzIntegrationAccount** Cmdlet 會修改整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="d3693-106">The **Set-AzIntegrationAccount** cmdlet modifies an integration account.</span></span>
<span data-ttu-id="d3693-107">這個 Cmdlet 會傳回代表整合帳戶的物件。</span><span class="sxs-lookup"><span data-stu-id="d3693-107">This cmdlet returns an object that represents the integration account.</span></span>
<span data-ttu-id="d3693-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="d3693-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d3693-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="d3693-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d3693-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="d3693-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d3693-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="d3693-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d3693-112">示例</span><span class="sxs-lookup"><span data-stu-id="d3693-112">EXAMPLES</span></span>

### <span data-ttu-id="d3693-113">範例1：修改整合帳戶</span><span class="sxs-lookup"><span data-stu-id="d3693-113">Example 1: Modify an integration account</span></span>
```
PS C:\>Set-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Sku "Free"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="d3693-114">這個命令會修改指定資源群組中名為 IntegrationAccount31 的整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="d3693-114">This command modifies an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="d3693-115">參數</span><span class="sxs-lookup"><span data-stu-id="d3693-115">PARAMETERS</span></span>

### <span data-ttu-id="d3693-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3693-116">-DefaultProfile</span></span>
<span data-ttu-id="d3693-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d3693-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3693-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d3693-118">-Force</span></span>
<span data-ttu-id="d3693-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="d3693-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d3693-120">-位置</span><span class="sxs-lookup"><span data-stu-id="d3693-120">-Location</span></span>
<span data-ttu-id="d3693-121">指定整合帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="d3693-121">Specifies a location for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3693-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="d3693-122">-Name</span></span>
<span data-ttu-id="d3693-123">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="d3693-123">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3693-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3693-124">-ResourceGroupName</span></span>
<span data-ttu-id="d3693-125">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d3693-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d3693-126">-Sku</span><span class="sxs-lookup"><span data-stu-id="d3693-126">-Sku</span></span>
<span data-ttu-id="d3693-127">指定整合帳戶的 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="d3693-127">Specifies a SKU name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3693-128">-確認</span><span class="sxs-lookup"><span data-stu-id="d3693-128">-Confirm</span></span>
<span data-ttu-id="d3693-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d3693-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3693-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3693-130">-WhatIf</span></span>
<span data-ttu-id="d3693-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d3693-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3693-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d3693-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3693-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3693-133">CommonParameters</span></span>
<span data-ttu-id="d3693-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d3693-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3693-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d3693-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3693-136">輸入</span><span class="sxs-lookup"><span data-stu-id="d3693-136">INPUTS</span></span>

### <span data-ttu-id="d3693-137">System.object</span><span class="sxs-lookup"><span data-stu-id="d3693-137">System.String</span></span>

## <span data-ttu-id="d3693-138">輸出</span><span class="sxs-lookup"><span data-stu-id="d3693-138">OUTPUTS</span></span>

### <span data-ttu-id="d3693-139">IntegrationAccount 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="d3693-139">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="d3693-140">筆記</span><span class="sxs-lookup"><span data-stu-id="d3693-140">NOTES</span></span>

## <span data-ttu-id="d3693-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="d3693-141">RELATED LINKS</span></span>

[<span data-ttu-id="d3693-142">AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="d3693-142">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)

[<span data-ttu-id="d3693-143">新-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="d3693-143">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="d3693-144">移除-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="d3693-144">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)


