---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5F1A4FE0-CB57-45D3-9F08-879469A61E1E
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccount.md
ms.openlocfilehash: 12fb8ed21365c3fd0decf3272364e30c8b8dc6cb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916534"
---
# <span data-ttu-id="6d42b-101">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="6d42b-101">New-AzIntegrationAccount</span></span>

## <span data-ttu-id="6d42b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6d42b-102">SYNOPSIS</span></span>
<span data-ttu-id="6d42b-103">建立整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="6d42b-103">Creates an integration account.</span></span>

## <span data-ttu-id="6d42b-104">語法</span><span class="sxs-lookup"><span data-stu-id="6d42b-104">SYNTAX</span></span>

```
New-AzIntegrationAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d42b-105">描述</span><span class="sxs-lookup"><span data-stu-id="6d42b-105">DESCRIPTION</span></span>
<span data-ttu-id="6d42b-106">**New-Az一Account** Cmdlet 會建立整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="6d42b-106">The **New-AzIntegrationAccount** cmdlet creates an integration account.</span></span>
<span data-ttu-id="6d42b-107">此 Cmdlet 會返回代表整合帳戶的物件。指定名稱、位置、資源組名和 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="6d42b-107">This cmdlet returns an object that represents the integration account.Specify a name, location, resource group name, and SKU name.</span></span>
<span data-ttu-id="6d42b-108">在命令列中指定的範本參數檔案值優先于範本參數物件的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="6d42b-108">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="6d42b-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="6d42b-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="6d42b-110">若要使用動態參數，請于命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="6d42b-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="6d42b-111">若要探索動態參數的名稱，在 Cmdlet 名稱之後輸入連字號 (-) ，然後重複按 Tab 鍵以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="6d42b-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6d42b-112">如果您省略必要的範本參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="6d42b-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="6d42b-113">例子</span><span class="sxs-lookup"><span data-stu-id="6d42b-113">EXAMPLES</span></span>

### <span data-ttu-id="6d42b-114">範例 1：建立整合帳戶</span><span class="sxs-lookup"><span data-stu-id="6d42b-114">Example 1: Create an integration account</span></span>
```
PS C:\>New-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Location "brazilsouth" -Sku "Standard"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="6d42b-115">此命令會于指定的資源群組中建立一個名為 IntegrationAccount31 的整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="6d42b-115">This command creates an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="6d42b-116">參數</span><span class="sxs-lookup"><span data-stu-id="6d42b-116">PARAMETERS</span></span>

### <span data-ttu-id="6d42b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d42b-117">-DefaultProfile</span></span>
<span data-ttu-id="6d42b-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="6d42b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d42b-119">-位置</span><span class="sxs-lookup"><span data-stu-id="6d42b-119">-Location</span></span>
<span data-ttu-id="6d42b-120">指定整合帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="6d42b-120">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="6d42b-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="6d42b-121">-Name</span></span>
<span data-ttu-id="6d42b-122">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="6d42b-122">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="6d42b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d42b-123">-ResourceGroupName</span></span>
<span data-ttu-id="6d42b-124">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6d42b-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6d42b-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="6d42b-125">-Sku</span></span>
<span data-ttu-id="6d42b-126">指定整合帳戶的 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="6d42b-126">Specifies a SKU name for the integration account.</span></span>

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

### <span data-ttu-id="6d42b-127">-確認</span><span class="sxs-lookup"><span data-stu-id="6d42b-127">-Confirm</span></span>
<span data-ttu-id="6d42b-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6d42b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d42b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d42b-129">-WhatIf</span></span>
<span data-ttu-id="6d42b-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6d42b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d42b-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6d42b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d42b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d42b-132">CommonParameters</span></span>
<span data-ttu-id="6d42b-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6d42b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d42b-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="6d42b-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d42b-135">輸入</span><span class="sxs-lookup"><span data-stu-id="6d42b-135">INPUTS</span></span>

### <span data-ttu-id="6d42b-136">System.String</span><span class="sxs-lookup"><span data-stu-id="6d42b-136">System.String</span></span>

## <span data-ttu-id="6d42b-137">輸出</span><span class="sxs-lookup"><span data-stu-id="6d42b-137">OUTPUTS</span></span>

### <span data-ttu-id="6d42b-138">Microsoft.Azure.management.Logic.models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="6d42b-138">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="6d42b-139">筆記</span><span class="sxs-lookup"><span data-stu-id="6d42b-139">NOTES</span></span>

## <span data-ttu-id="6d42b-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="6d42b-140">RELATED LINKS</span></span>

[<span data-ttu-id="6d42b-141">Get-AzCountAccount</span><span class="sxs-lookup"><span data-stu-id="6d42b-141">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)

[<span data-ttu-id="6d42b-142">Remove-AzCountAccount</span><span class="sxs-lookup"><span data-stu-id="6d42b-142">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="6d42b-143">Set-AzCountAccount</span><span class="sxs-lookup"><span data-stu-id="6d42b-143">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


