---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
ms.openlocfilehash: 9bee67dd299163b8e660b0e17c4e3bc11da5b40e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98287624"
---
# <span data-ttu-id="d3b88-101">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="d3b88-101">Set-AzApiManagementProduct</span></span>

## <span data-ttu-id="d3b88-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d3b88-102">SYNOPSIS</span></span>
<span data-ttu-id="d3b88-103">設定 API 管理產品詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d3b88-103">Sets the API Management product details.</span></span>

## <span data-ttu-id="d3b88-104">句法</span><span class="sxs-lookup"><span data-stu-id="d3b88-104">SYNTAX</span></span>

```
Set-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3b88-105">說明</span><span class="sxs-lookup"><span data-stu-id="d3b88-105">DESCRIPTION</span></span>
<span data-ttu-id="d3b88-106">**AzApiManagementProduct** Cmdlet 會設定 API 管理產品的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d3b88-106">The **Set-AzApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="d3b88-107">示例</span><span class="sxs-lookup"><span data-stu-id="d3b88-107">EXAMPLES</span></span>

### <span data-ttu-id="d3b88-108">範例1：更新產品詳細資料</span><span class="sxs-lookup"><span data-stu-id="d3b88-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="d3b88-109">這個命令會更新 API 管理產品詳細資料、需要訂閱，然後 unpublishes。</span><span class="sxs-lookup"><span data-stu-id="d3b88-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="d3b88-110">參數</span><span class="sxs-lookup"><span data-stu-id="d3b88-110">PARAMETERS</span></span>

### <span data-ttu-id="d3b88-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="d3b88-111">-ApprovalRequired</span></span>
<span data-ttu-id="d3b88-112">指出產品的訂閱是否需要核准。</span><span class="sxs-lookup"><span data-stu-id="d3b88-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="d3b88-113">預設值為 [ **$False**]。</span><span class="sxs-lookup"><span data-stu-id="d3b88-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="d3b88-114">-內容</span><span class="sxs-lookup"><span data-stu-id="d3b88-114">-Context</span></span>
<span data-ttu-id="d3b88-115">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="d3b88-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d3b88-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3b88-116">-DefaultProfile</span></span>
<span data-ttu-id="d3b88-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d3b88-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3b88-118">-描述</span><span class="sxs-lookup"><span data-stu-id="d3b88-118">-Description</span></span>
<span data-ttu-id="d3b88-119">指定產品描述。</span><span class="sxs-lookup"><span data-stu-id="d3b88-119">Specifies the product description.</span></span>

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

### <span data-ttu-id="d3b88-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="d3b88-120">-LegalTerms</span></span>
<span data-ttu-id="d3b88-121">指定產品的使用條款。</span><span class="sxs-lookup"><span data-stu-id="d3b88-121">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="d3b88-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3b88-122">-PassThru</span></span>
<span data-ttu-id="d3b88-123">passthru</span><span class="sxs-lookup"><span data-stu-id="d3b88-123">passthru</span></span>

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

### <span data-ttu-id="d3b88-124">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="d3b88-124">-ProductId</span></span>
<span data-ttu-id="d3b88-125">指定現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d3b88-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="d3b88-126">-State</span><span class="sxs-lookup"><span data-stu-id="d3b88-126">-State</span></span>
<span data-ttu-id="d3b88-127">指定產品狀態。</span><span class="sxs-lookup"><span data-stu-id="d3b88-127">Specifies the product state.</span></span>
<span data-ttu-id="d3b88-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="d3b88-128">psdx_paramvalues</span></span>
- <span data-ttu-id="d3b88-129">NotPublished</span><span class="sxs-lookup"><span data-stu-id="d3b88-129">NotPublished</span></span>
- <span data-ttu-id="d3b88-130">時間</span><span class="sxs-lookup"><span data-stu-id="d3b88-130">Published</span></span>

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

### <span data-ttu-id="d3b88-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="d3b88-131">-SubscriptionRequired</span></span>
<span data-ttu-id="d3b88-132">指出產品是否需要訂閱。</span><span class="sxs-lookup"><span data-stu-id="d3b88-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="d3b88-133">此參數的預設值為 [ **$True**]。</span><span class="sxs-lookup"><span data-stu-id="d3b88-133">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="d3b88-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="d3b88-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="d3b88-135">指定同時進行的訂閱數目上限。</span><span class="sxs-lookup"><span data-stu-id="d3b88-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="d3b88-136">此參數的預設值為 [無]。</span><span class="sxs-lookup"><span data-stu-id="d3b88-136">The default value for this parameter is None.</span></span>

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

### <span data-ttu-id="d3b88-137">-標題</span><span class="sxs-lookup"><span data-stu-id="d3b88-137">-Title</span></span>
<span data-ttu-id="d3b88-138">指定此 Cmdlet 所設定的產品標題。</span><span class="sxs-lookup"><span data-stu-id="d3b88-138">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="d3b88-139">-確認</span><span class="sxs-lookup"><span data-stu-id="d3b88-139">-Confirm</span></span>
<span data-ttu-id="d3b88-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d3b88-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3b88-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3b88-141">-WhatIf</span></span>
<span data-ttu-id="d3b88-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d3b88-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3b88-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d3b88-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3b88-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3b88-144">CommonParameters</span></span>
<span data-ttu-id="d3b88-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d3b88-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3b88-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d3b88-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3b88-147">輸入</span><span class="sxs-lookup"><span data-stu-id="d3b88-147">INPUTS</span></span>

### <span data-ttu-id="d3b88-148">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="d3b88-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d3b88-149">System.object</span><span class="sxs-lookup"><span data-stu-id="d3b88-149">System.String</span></span>

### <span data-ttu-id="d3b88-150">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d3b88-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d3b88-151">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d3b88-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d3b88-152">ApiManagement 為 Nullable "1 [PsApiManagementProductState，，ServiceManagement，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]]。）））））））</span><span class="sxs-lookup"><span data-stu-id="d3b88-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="d3b88-153">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="d3b88-153">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d3b88-154">輸出</span><span class="sxs-lookup"><span data-stu-id="d3b88-154">OUTPUTS</span></span>

### <span data-ttu-id="d3b88-155">ServiceManagement. PsApiManagementProduct （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="d3b88-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="d3b88-156">筆記</span><span class="sxs-lookup"><span data-stu-id="d3b88-156">NOTES</span></span>

## <span data-ttu-id="d3b88-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="d3b88-157">RELATED LINKS</span></span>

[<span data-ttu-id="d3b88-158">AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="d3b88-158">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="d3b88-159">新-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="d3b88-159">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="d3b88-160">移除-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="d3b88-160">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)


