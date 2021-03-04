---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
ms.openlocfilehash: e827fcf43c151f0812d96456de430f57686d4562
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903881"
---
# <span data-ttu-id="175ee-101">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="175ee-101">Set-AzApiManagementProduct</span></span>

## <span data-ttu-id="175ee-102">簡介</span><span class="sxs-lookup"><span data-stu-id="175ee-102">SYNOPSIS</span></span>
<span data-ttu-id="175ee-103">設定 API 管理產品詳細資料。</span><span class="sxs-lookup"><span data-stu-id="175ee-103">Sets the API Management product details.</span></span>

## <span data-ttu-id="175ee-104">語法</span><span class="sxs-lookup"><span data-stu-id="175ee-104">SYNTAX</span></span>

```
Set-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="175ee-105">描述</span><span class="sxs-lookup"><span data-stu-id="175ee-105">DESCRIPTION</span></span>
<span data-ttu-id="175ee-106">**Set-AzApiManagementProduct** Cmdlet 會設定 API 管理產品詳細資料。</span><span class="sxs-lookup"><span data-stu-id="175ee-106">The **Set-AzApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="175ee-107">例子</span><span class="sxs-lookup"><span data-stu-id="175ee-107">EXAMPLES</span></span>

### <span data-ttu-id="175ee-108">範例 1：更新產品詳細資料</span><span class="sxs-lookup"><span data-stu-id="175ee-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="175ee-109">此命令會更新 API 管理產品詳細資料、需要訂閱，然後取消發佈。</span><span class="sxs-lookup"><span data-stu-id="175ee-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="175ee-110">參數</span><span class="sxs-lookup"><span data-stu-id="175ee-110">PARAMETERS</span></span>

### <span data-ttu-id="175ee-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="175ee-111">-ApprovalRequired</span></span>
<span data-ttu-id="175ee-112">指出產品的訂閱是否需要核准。</span><span class="sxs-lookup"><span data-stu-id="175ee-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="175ee-113">預設值為 **$False。**</span><span class="sxs-lookup"><span data-stu-id="175ee-113">The default value is **$False**.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="175ee-114">-內容</span><span class="sxs-lookup"><span data-stu-id="175ee-114">-Context</span></span>
<span data-ttu-id="175ee-115">指定 **PsApiManagementCoNtext 物件的** 實例。</span><span class="sxs-lookup"><span data-stu-id="175ee-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="175ee-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="175ee-116">-DefaultProfile</span></span>
<span data-ttu-id="175ee-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="175ee-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="175ee-118">-描述</span><span class="sxs-lookup"><span data-stu-id="175ee-118">-Description</span></span>
<span data-ttu-id="175ee-119">指定產品描述。</span><span class="sxs-lookup"><span data-stu-id="175ee-119">Specifies the product description.</span></span>

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

### <span data-ttu-id="175ee-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="175ee-120">-LegalTerms</span></span>
<span data-ttu-id="175ee-121">指定產品的法律使用條款。</span><span class="sxs-lookup"><span data-stu-id="175ee-121">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="175ee-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="175ee-122">-PassThru</span></span>
<span data-ttu-id="175ee-123">Passthru</span><span class="sxs-lookup"><span data-stu-id="175ee-123">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="175ee-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="175ee-124">-ProductId</span></span>
<span data-ttu-id="175ee-125">指定現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="175ee-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="175ee-126">-State</span><span class="sxs-lookup"><span data-stu-id="175ee-126">-State</span></span>
<span data-ttu-id="175ee-127">指定產品狀態。</span><span class="sxs-lookup"><span data-stu-id="175ee-127">Specifies the product state.</span></span>
<span data-ttu-id="175ee-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="175ee-128">psdx_paramvalues</span></span>
- <span data-ttu-id="175ee-129">未發佈</span><span class="sxs-lookup"><span data-stu-id="175ee-129">NotPublished</span></span>
- <span data-ttu-id="175ee-130">發表</span><span class="sxs-lookup"><span data-stu-id="175ee-130">Published</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState]
Parameter Sets: (All)
Aliases:
Accepted values: NotPublished, Published

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="175ee-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="175ee-131">-SubscriptionRequired</span></span>
<span data-ttu-id="175ee-132">指出產品是否需要訂閱。</span><span class="sxs-lookup"><span data-stu-id="175ee-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="175ee-133">此參數的預設值為 **$True。**</span><span class="sxs-lookup"><span data-stu-id="175ee-133">The default value for this parameter is **$True**.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="175ee-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="175ee-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="175ee-135">指定同時訂閱的數量上限。</span><span class="sxs-lookup"><span data-stu-id="175ee-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="175ee-136">此參數的預設值為 None。</span><span class="sxs-lookup"><span data-stu-id="175ee-136">The default value for this parameter is None.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="175ee-137">-標題</span><span class="sxs-lookup"><span data-stu-id="175ee-137">-Title</span></span>
<span data-ttu-id="175ee-138">指定此 Cmdlet 集的產品標題。</span><span class="sxs-lookup"><span data-stu-id="175ee-138">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="175ee-139">-確認</span><span class="sxs-lookup"><span data-stu-id="175ee-139">-Confirm</span></span>
<span data-ttu-id="175ee-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="175ee-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="175ee-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="175ee-141">-WhatIf</span></span>
<span data-ttu-id="175ee-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="175ee-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="175ee-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="175ee-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="175ee-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="175ee-144">CommonParameters</span></span>
<span data-ttu-id="175ee-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="175ee-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="175ee-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="175ee-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="175ee-147">輸入</span><span class="sxs-lookup"><span data-stu-id="175ee-147">INPUTS</span></span>

### <span data-ttu-id="175ee-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="175ee-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="175ee-149">System.String</span><span class="sxs-lookup"><span data-stu-id="175ee-149">System.String</span></span>

### <span data-ttu-id="175ee-150">System.Nullable'1[[System.Boolean， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="175ee-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="175ee-151">System.Nullable'1[[System.Int32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="175ee-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="175ee-152">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="175ee-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="175ee-153">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="175ee-153">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="175ee-154">輸出</span><span class="sxs-lookup"><span data-stu-id="175ee-154">OUTPUTS</span></span>

### <span data-ttu-id="175ee-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="175ee-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="175ee-156">筆記</span><span class="sxs-lookup"><span data-stu-id="175ee-156">NOTES</span></span>

## <span data-ttu-id="175ee-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="175ee-157">RELATED LINKS</span></span>

[<span data-ttu-id="175ee-158">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="175ee-158">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="175ee-159">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="175ee-159">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="175ee-160">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="175ee-160">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)


