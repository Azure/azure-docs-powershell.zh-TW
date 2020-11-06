---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5F1A4FE0-CB57-45D3-9F08-879469A61E1E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccount.md
ms.openlocfilehash: ec1e223359c3d83a3cfb77810e0e680f7142bc60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453459"
---
# <span data-ttu-id="1272e-101">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="1272e-101">New-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="1272e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1272e-102">SYNOPSIS</span></span>
<span data-ttu-id="1272e-103">建立整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="1272e-103">Creates an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1272e-104">句法</span><span class="sxs-lookup"><span data-stu-id="1272e-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1272e-105">說明</span><span class="sxs-lookup"><span data-stu-id="1272e-105">DESCRIPTION</span></span>
<span data-ttu-id="1272e-106">**新的-AzureRmIntegrationAccount** Cmdlet 會建立整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="1272e-106">The **New-AzureRmIntegrationAccount** cmdlet creates an integration account.</span></span>
<span data-ttu-id="1272e-107">這個 Cmdlet 會傳回代表整合帳戶的物件。指定名稱、位置、資源群組名稱及 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="1272e-107">This cmdlet returns an object that represents the integration account.Specify a name, location, resource group name, and SKU name.</span></span>

<span data-ttu-id="1272e-108">您在命令列中指定的範本參數檔值優先于 template 參數物件中的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="1272e-108">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="1272e-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="1272e-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="1272e-110">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="1272e-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="1272e-111">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="1272e-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1272e-112">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="1272e-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="1272e-113">示例</span><span class="sxs-lookup"><span data-stu-id="1272e-113">EXAMPLES</span></span>

### <span data-ttu-id="1272e-114">範例1：建立整合帳戶</span><span class="sxs-lookup"><span data-stu-id="1272e-114">Example 1: Create an integration account</span></span>
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

<span data-ttu-id="1272e-115">這個命令會在指定的資源群組中建立名為 IntegrationAccount31 的整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="1272e-115">This command creates an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="1272e-116">參數</span><span class="sxs-lookup"><span data-stu-id="1272e-116">PARAMETERS</span></span>

### <span data-ttu-id="1272e-117">-位置</span><span class="sxs-lookup"><span data-stu-id="1272e-117">-Location</span></span>
<span data-ttu-id="1272e-118">指定整合帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="1272e-118">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="1272e-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="1272e-119">-Name</span></span>
<span data-ttu-id="1272e-120">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="1272e-120">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="1272e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1272e-121">-ResourceGroupName</span></span>
<span data-ttu-id="1272e-122">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1272e-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1272e-123">-Sku</span><span class="sxs-lookup"><span data-stu-id="1272e-123">-Sku</span></span>
<span data-ttu-id="1272e-124">指定整合帳戶的 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="1272e-124">Specifies a SKU name for the integration account.</span></span>

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

### <span data-ttu-id="1272e-125">-確認</span><span class="sxs-lookup"><span data-stu-id="1272e-125">-Confirm</span></span>
<span data-ttu-id="1272e-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1272e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1272e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1272e-127">-WhatIf</span></span>
<span data-ttu-id="1272e-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1272e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1272e-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1272e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1272e-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1272e-130">-DefaultProfile</span></span>
<span data-ttu-id="1272e-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1272e-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1272e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1272e-132">CommonParameters</span></span>
<span data-ttu-id="1272e-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1272e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1272e-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1272e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1272e-135">輸入</span><span class="sxs-lookup"><span data-stu-id="1272e-135">INPUTS</span></span>

## <span data-ttu-id="1272e-136">輸出</span><span class="sxs-lookup"><span data-stu-id="1272e-136">OUTPUTS</span></span>

### <span data-ttu-id="1272e-137">IntegrationAccount 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="1272e-137">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="1272e-138">筆記</span><span class="sxs-lookup"><span data-stu-id="1272e-138">NOTES</span></span>

## <span data-ttu-id="1272e-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="1272e-139">RELATED LINKS</span></span>

[<span data-ttu-id="1272e-140">AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="1272e-140">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)

[<span data-ttu-id="1272e-141">移除-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="1272e-141">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)

[<span data-ttu-id="1272e-142">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="1272e-142">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)

