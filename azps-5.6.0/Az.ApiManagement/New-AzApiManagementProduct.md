---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
ms.openlocfilehash: 12de4862e91555b90a4168ac7ac5908b897d6e49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911202"
---
# <span data-ttu-id="c6477-101">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c6477-101">New-AzApiManagementProduct</span></span>

## <span data-ttu-id="c6477-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c6477-102">SYNOPSIS</span></span>
<span data-ttu-id="c6477-103">建立 API 管理產品。</span><span class="sxs-lookup"><span data-stu-id="c6477-103">Creates an API Management product.</span></span>

## <span data-ttu-id="c6477-104">語法</span><span class="sxs-lookup"><span data-stu-id="c6477-104">SYNTAX</span></span>

```
New-AzApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6477-105">描述</span><span class="sxs-lookup"><span data-stu-id="c6477-105">DESCRIPTION</span></span>
<span data-ttu-id="c6477-106">**New-AzApiManagementProduct** Cmdlet 會建立 API 管理產品。</span><span class="sxs-lookup"><span data-stu-id="c6477-106">The **New-AzApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="c6477-107">例子</span><span class="sxs-lookup"><span data-stu-id="c6477-107">EXAMPLES</span></span>

### <span data-ttu-id="c6477-108">範例 1：建立不需要訂閱的產品</span><span class="sxs-lookup"><span data-stu-id="c6477-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="c6477-109">此命令會建立 API 管理產品。</span><span class="sxs-lookup"><span data-stu-id="c6477-109">This command creates an API Management product.</span></span>
<span data-ttu-id="c6477-110">不需要訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6477-110">No subscription is required.</span></span>

### <span data-ttu-id="c6477-111">範例 2：建立需要訂閱和核准的產品</span><span class="sxs-lookup"><span data-stu-id="c6477-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="c6477-112">此命令會建立產品。</span><span class="sxs-lookup"><span data-stu-id="c6477-112">This command creates a product.</span></span>
<span data-ttu-id="c6477-113">需要訂閱和核准。</span><span class="sxs-lookup"><span data-stu-id="c6477-113">A subscription and approval are required.</span></span>
<span data-ttu-id="c6477-114">此命令將通知期間設定為 10 天。</span><span class="sxs-lookup"><span data-stu-id="c6477-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="c6477-115">訂閱持續時間設定為一年。</span><span class="sxs-lookup"><span data-stu-id="c6477-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="c6477-116">參數</span><span class="sxs-lookup"><span data-stu-id="c6477-116">PARAMETERS</span></span>

### <span data-ttu-id="c6477-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="c6477-117">-ApprovalRequired</span></span>
<span data-ttu-id="c6477-118">指出產品的訂閱是否需要核准。</span><span class="sxs-lookup"><span data-stu-id="c6477-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="c6477-119">根據預設，此 **參數會**$False。</span><span class="sxs-lookup"><span data-stu-id="c6477-119">By default, this parameter is **$False**.</span></span>

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

### <span data-ttu-id="c6477-120">-內容</span><span class="sxs-lookup"><span data-stu-id="c6477-120">-Context</span></span>
<span data-ttu-id="c6477-121">指定 **PsApiManagementCoNtext 物件的** 實例。</span><span class="sxs-lookup"><span data-stu-id="c6477-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c6477-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6477-122">-DefaultProfile</span></span>
<span data-ttu-id="c6477-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6477-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6477-124">-描述</span><span class="sxs-lookup"><span data-stu-id="c6477-124">-Description</span></span>
<span data-ttu-id="c6477-125">指定產品描述。</span><span class="sxs-lookup"><span data-stu-id="c6477-125">Specifies the product description.</span></span>

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

### <span data-ttu-id="c6477-126">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="c6477-126">-LegalTerms</span></span>
<span data-ttu-id="c6477-127">指定產品的法律使用條款。</span><span class="sxs-lookup"><span data-stu-id="c6477-127">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="c6477-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="c6477-128">-ProductId</span></span>
<span data-ttu-id="c6477-129">指定新產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6477-129">Specifies the identifier of new product.</span></span>
<span data-ttu-id="c6477-130">如果您未指定此參數，即會產生新產品。</span><span class="sxs-lookup"><span data-stu-id="c6477-130">If you do not specify this parameter, a new product is generated.</span></span>

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

### <span data-ttu-id="c6477-131">-State</span><span class="sxs-lookup"><span data-stu-id="c6477-131">-State</span></span>
<span data-ttu-id="c6477-132">指定產品狀態。</span><span class="sxs-lookup"><span data-stu-id="c6477-132">Specifies the product state.</span></span>
<span data-ttu-id="c6477-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="c6477-133">psdx_paramvalues</span></span>
- <span data-ttu-id="c6477-134">未發佈</span><span class="sxs-lookup"><span data-stu-id="c6477-134">NotPublished</span></span>
- <span data-ttu-id="c6477-135">已發佈預設值為未發佈。</span><span class="sxs-lookup"><span data-stu-id="c6477-135">Published The default value is NotPublished.</span></span>

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

### <span data-ttu-id="c6477-136">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="c6477-136">-SubscriptionRequired</span></span>
<span data-ttu-id="c6477-137">指出產品是否需要訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6477-137">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="c6477-138">預設值為 **$True。**</span><span class="sxs-lookup"><span data-stu-id="c6477-138">The default value is **$True**.</span></span>

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

### <span data-ttu-id="c6477-139">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="c6477-139">-SubscriptionsLimit</span></span>
<span data-ttu-id="c6477-140">指定同時訂閱的數量上限。</span><span class="sxs-lookup"><span data-stu-id="c6477-140">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="c6477-141">預設值為 None。</span><span class="sxs-lookup"><span data-stu-id="c6477-141">The default value is None.</span></span>

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

### <span data-ttu-id="c6477-142">-標題</span><span class="sxs-lookup"><span data-stu-id="c6477-142">-Title</span></span>
<span data-ttu-id="c6477-143">指定產品標題。</span><span class="sxs-lookup"><span data-stu-id="c6477-143">Specifies the product title.</span></span>

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

### <span data-ttu-id="c6477-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6477-144">CommonParameters</span></span>
<span data-ttu-id="c6477-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c6477-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6477-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6477-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6477-147">輸入</span><span class="sxs-lookup"><span data-stu-id="c6477-147">INPUTS</span></span>

### <span data-ttu-id="c6477-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="c6477-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c6477-149">System.String</span><span class="sxs-lookup"><span data-stu-id="c6477-149">System.String</span></span>

### <span data-ttu-id="c6477-150">System.Nullable'1[[System.Boolean， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c6477-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c6477-151">System.Nullable'1[[System.Int32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c6477-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c6477-152">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="c6477-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c6477-153">輸出</span><span class="sxs-lookup"><span data-stu-id="c6477-153">OUTPUTS</span></span>

### <span data-ttu-id="c6477-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c6477-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="c6477-155">筆記</span><span class="sxs-lookup"><span data-stu-id="c6477-155">NOTES</span></span>

## <span data-ttu-id="c6477-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6477-156">RELATED LINKS</span></span>

[<span data-ttu-id="c6477-157">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c6477-157">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="c6477-158">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c6477-158">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="c6477-159">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c6477-159">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


