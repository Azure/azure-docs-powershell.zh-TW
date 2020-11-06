---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F6D9EA59-BA61-4117-8771-9B190424BFF8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccount.md
ms.openlocfilehash: d2948378f9312687e2dbbe09bd7c583cbe085778
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448635"
---
# <span data-ttu-id="f3141-101">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="f3141-101">Set-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="f3141-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3141-102">SYNOPSIS</span></span>
<span data-ttu-id="f3141-103">修改整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="f3141-103">Modifies an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3141-104">句法</span><span class="sxs-lookup"><span data-stu-id="f3141-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> [-Location <String>] [-Sku <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3141-105">說明</span><span class="sxs-lookup"><span data-stu-id="f3141-105">DESCRIPTION</span></span>
<span data-ttu-id="f3141-106">**AzureRmIntegrationAccount** Cmdlet 會修改整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="f3141-106">The **Set-AzureRmIntegrationAccount** cmdlet modifies an integration account.</span></span>
<span data-ttu-id="f3141-107">這個 Cmdlet 會傳回代表整合帳戶的物件。</span><span class="sxs-lookup"><span data-stu-id="f3141-107">This cmdlet returns an object that represents the integration account.</span></span>

<span data-ttu-id="f3141-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="f3141-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="f3141-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="f3141-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="f3141-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="f3141-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f3141-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="f3141-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f3141-112">示例</span><span class="sxs-lookup"><span data-stu-id="f3141-112">EXAMPLES</span></span>

### <span data-ttu-id="f3141-113">範例1：修改整合帳戶</span><span class="sxs-lookup"><span data-stu-id="f3141-113">Example 1: Modify an integration account</span></span>
```
PS C:\>Set-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Sku "Free"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="f3141-114">這個命令會修改指定資源群組中名為 IntegrationAccount31 的整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="f3141-114">This command modifies an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="f3141-115">參數</span><span class="sxs-lookup"><span data-stu-id="f3141-115">PARAMETERS</span></span>

### <span data-ttu-id="f3141-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3141-116">-DefaultProfile</span></span>
<span data-ttu-id="f3141-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f3141-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3141-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f3141-118">-Force</span></span>
<span data-ttu-id="f3141-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="f3141-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3141-120">-位置</span><span class="sxs-lookup"><span data-stu-id="f3141-120">-Location</span></span>
<span data-ttu-id="f3141-121">指定整合帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="f3141-121">Specifies a location for the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3141-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="f3141-122">-Name</span></span>
<span data-ttu-id="f3141-123">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3141-123">Specifies the name of the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3141-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3141-124">-ResourceGroupName</span></span>
<span data-ttu-id="f3141-125">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3141-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f3141-126">-Sku</span><span class="sxs-lookup"><span data-stu-id="f3141-126">-Sku</span></span>
<span data-ttu-id="f3141-127">指定整合帳戶的 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="f3141-127">Specifies a SKU name for the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3141-128">-確認</span><span class="sxs-lookup"><span data-stu-id="f3141-128">-Confirm</span></span>
<span data-ttu-id="f3141-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f3141-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3141-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3141-130">-WhatIf</span></span>
<span data-ttu-id="f3141-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f3141-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3141-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f3141-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3141-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3141-133">CommonParameters</span></span>
<span data-ttu-id="f3141-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3141-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3141-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f3141-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3141-136">輸入</span><span class="sxs-lookup"><span data-stu-id="f3141-136">INPUTS</span></span>

### <span data-ttu-id="f3141-137">所有</span><span class="sxs-lookup"><span data-stu-id="f3141-137">None</span></span>
<span data-ttu-id="f3141-138">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="f3141-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f3141-139">輸出</span><span class="sxs-lookup"><span data-stu-id="f3141-139">OUTPUTS</span></span>

### <span data-ttu-id="f3141-140">IntegrationAccount 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="f3141-140">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="f3141-141">筆記</span><span class="sxs-lookup"><span data-stu-id="f3141-141">NOTES</span></span>

## <span data-ttu-id="f3141-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3141-142">RELATED LINKS</span></span>

[<span data-ttu-id="f3141-143">AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="f3141-143">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)

[<span data-ttu-id="f3141-144">新-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="f3141-144">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="f3141-145">移除-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="f3141-145">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)


