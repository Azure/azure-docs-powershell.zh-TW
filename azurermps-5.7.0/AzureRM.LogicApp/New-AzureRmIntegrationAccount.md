---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5F1A4FE0-CB57-45D3-9F08-879469A61E1E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccount.md
ms.openlocfilehash: 44dc417521b49d47b9c060b987c82ddd06b7f8dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447079"
---
# <span data-ttu-id="45d7f-101">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="45d7f-101">New-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="45d7f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="45d7f-102">SYNOPSIS</span></span>
<span data-ttu-id="45d7f-103">建立整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="45d7f-103">Creates an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45d7f-104">句法</span><span class="sxs-lookup"><span data-stu-id="45d7f-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45d7f-105">說明</span><span class="sxs-lookup"><span data-stu-id="45d7f-105">DESCRIPTION</span></span>
<span data-ttu-id="45d7f-106">**新的-AzureRmIntegrationAccount** Cmdlet 會建立整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="45d7f-106">The **New-AzureRmIntegrationAccount** cmdlet creates an integration account.</span></span>
<span data-ttu-id="45d7f-107">這個 Cmdlet 會傳回代表整合帳戶的物件。指定名稱、位置、資源群組名稱及 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="45d7f-107">This cmdlet returns an object that represents the integration account.Specify a name, location, resource group name, and SKU name.</span></span>

<span data-ttu-id="45d7f-108">您在命令列中指定的範本參數檔值優先于 template 參數物件中的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="45d7f-108">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="45d7f-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="45d7f-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="45d7f-110">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="45d7f-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="45d7f-111">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="45d7f-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="45d7f-112">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="45d7f-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="45d7f-113">示例</span><span class="sxs-lookup"><span data-stu-id="45d7f-113">EXAMPLES</span></span>

### <span data-ttu-id="45d7f-114">範例1：建立整合帳戶</span><span class="sxs-lookup"><span data-stu-id="45d7f-114">Example 1: Create an integration account</span></span>
```
PS C:\>New-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Location "brazilsouth" -Sku "Standard"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="45d7f-115">這個命令會在指定的資源群組中建立名為 IntegrationAccount31 的整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="45d7f-115">This command creates an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="45d7f-116">參數</span><span class="sxs-lookup"><span data-stu-id="45d7f-116">PARAMETERS</span></span>

### <span data-ttu-id="45d7f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45d7f-117">-DefaultProfile</span></span>
<span data-ttu-id="45d7f-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="45d7f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45d7f-119">-位置</span><span class="sxs-lookup"><span data-stu-id="45d7f-119">-Location</span></span>
<span data-ttu-id="45d7f-120">指定整合帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="45d7f-120">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="45d7f-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="45d7f-121">-Name</span></span>
<span data-ttu-id="45d7f-122">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="45d7f-122">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="45d7f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45d7f-123">-ResourceGroupName</span></span>
<span data-ttu-id="45d7f-124">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="45d7f-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="45d7f-125">-Sku</span><span class="sxs-lookup"><span data-stu-id="45d7f-125">-Sku</span></span>
<span data-ttu-id="45d7f-126">指定整合帳戶的 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="45d7f-126">Specifies a SKU name for the integration account.</span></span>

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

### <span data-ttu-id="45d7f-127">-確認</span><span class="sxs-lookup"><span data-stu-id="45d7f-127">-Confirm</span></span>
<span data-ttu-id="45d7f-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="45d7f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45d7f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45d7f-129">-WhatIf</span></span>
<span data-ttu-id="45d7f-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="45d7f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45d7f-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="45d7f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45d7f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45d7f-132">CommonParameters</span></span>
<span data-ttu-id="45d7f-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="45d7f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45d7f-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="45d7f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45d7f-135">輸入</span><span class="sxs-lookup"><span data-stu-id="45d7f-135">INPUTS</span></span>

### <span data-ttu-id="45d7f-136">所有</span><span class="sxs-lookup"><span data-stu-id="45d7f-136">None</span></span>
<span data-ttu-id="45d7f-137">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="45d7f-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="45d7f-138">輸出</span><span class="sxs-lookup"><span data-stu-id="45d7f-138">OUTPUTS</span></span>

### <span data-ttu-id="45d7f-139">IntegrationAccount 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="45d7f-139">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="45d7f-140">筆記</span><span class="sxs-lookup"><span data-stu-id="45d7f-140">NOTES</span></span>

## <span data-ttu-id="45d7f-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="45d7f-141">RELATED LINKS</span></span>

[<span data-ttu-id="45d7f-142">AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="45d7f-142">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)

[<span data-ttu-id="45d7f-143">移除-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="45d7f-143">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)

[<span data-ttu-id="45d7f-144">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="45d7f-144">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)


