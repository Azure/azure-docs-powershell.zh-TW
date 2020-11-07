---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
ms.openlocfilehash: 3d14ef7dca35796baa3e3aecf0c3df98674bfb9b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958167"
---
# <span data-ttu-id="514e7-101">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="514e7-101">New-AzApiManagementProduct</span></span>

## <span data-ttu-id="514e7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="514e7-102">SYNOPSIS</span></span>
<span data-ttu-id="514e7-103">建立 API 管理產品。</span><span class="sxs-lookup"><span data-stu-id="514e7-103">Creates an API Management product.</span></span>

## <span data-ttu-id="514e7-104">句法</span><span class="sxs-lookup"><span data-stu-id="514e7-104">SYNTAX</span></span>

```
New-AzApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="514e7-105">說明</span><span class="sxs-lookup"><span data-stu-id="514e7-105">DESCRIPTION</span></span>
<span data-ttu-id="514e7-106">**新的-AzApiManagementProduct** Cmdlet 會建立 API 管理產品。</span><span class="sxs-lookup"><span data-stu-id="514e7-106">The **New-AzApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="514e7-107">示例</span><span class="sxs-lookup"><span data-stu-id="514e7-107">EXAMPLES</span></span>

### <span data-ttu-id="514e7-108">範例1：建立不需要訂閱的產品</span><span class="sxs-lookup"><span data-stu-id="514e7-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="514e7-109">這個命令會建立 API 管理產品。</span><span class="sxs-lookup"><span data-stu-id="514e7-109">This command creates an API Management product.</span></span>
<span data-ttu-id="514e7-110">不需要訂閱。</span><span class="sxs-lookup"><span data-stu-id="514e7-110">No subscription is required.</span></span>

### <span data-ttu-id="514e7-111">範例2：建立需要訂閱與核准的產品</span><span class="sxs-lookup"><span data-stu-id="514e7-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="514e7-112">這個命令會建立產品。</span><span class="sxs-lookup"><span data-stu-id="514e7-112">This command creates a product.</span></span>
<span data-ttu-id="514e7-113">訂閱與核准是必要的。</span><span class="sxs-lookup"><span data-stu-id="514e7-113">A subscription and approval are required.</span></span>
<span data-ttu-id="514e7-114">這個命令會將通知期間設定為10天。</span><span class="sxs-lookup"><span data-stu-id="514e7-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="514e7-115">訂閱持續時間已設定為一年。</span><span class="sxs-lookup"><span data-stu-id="514e7-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="514e7-116">參數</span><span class="sxs-lookup"><span data-stu-id="514e7-116">PARAMETERS</span></span>

### <span data-ttu-id="514e7-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="514e7-117">-ApprovalRequired</span></span>
<span data-ttu-id="514e7-118">指出該產品的訂閱是否需要核准。</span><span class="sxs-lookup"><span data-stu-id="514e7-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="514e7-119">根據預設，此參數是 **$False** 的。</span><span class="sxs-lookup"><span data-stu-id="514e7-119">By default, this parameter is **$False**.</span></span>

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

### <span data-ttu-id="514e7-120">-內容</span><span class="sxs-lookup"><span data-stu-id="514e7-120">-Context</span></span>
<span data-ttu-id="514e7-121">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="514e7-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="514e7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="514e7-122">-DefaultProfile</span></span>
<span data-ttu-id="514e7-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="514e7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="514e7-124">-描述</span><span class="sxs-lookup"><span data-stu-id="514e7-124">-Description</span></span>
<span data-ttu-id="514e7-125">指定產品描述。</span><span class="sxs-lookup"><span data-stu-id="514e7-125">Specifies the product description.</span></span>

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

### <span data-ttu-id="514e7-126">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="514e7-126">-LegalTerms</span></span>
<span data-ttu-id="514e7-127">指定產品的使用條款。</span><span class="sxs-lookup"><span data-stu-id="514e7-127">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="514e7-128">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="514e7-128">-ProductId</span></span>
<span data-ttu-id="514e7-129">指定新產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="514e7-129">Specifies the identifier of new product.</span></span>
<span data-ttu-id="514e7-130">如果您沒有指定此參數，則會產生新的產品。</span><span class="sxs-lookup"><span data-stu-id="514e7-130">If you do not specify this parameter, a new product is generated.</span></span>

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

### <span data-ttu-id="514e7-131">-State</span><span class="sxs-lookup"><span data-stu-id="514e7-131">-State</span></span>
<span data-ttu-id="514e7-132">指定產品狀態。</span><span class="sxs-lookup"><span data-stu-id="514e7-132">Specifies the product state.</span></span>
<span data-ttu-id="514e7-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="514e7-133">psdx_paramvalues</span></span>
- <span data-ttu-id="514e7-134">NotPublished</span><span class="sxs-lookup"><span data-stu-id="514e7-134">NotPublished</span></span>
- <span data-ttu-id="514e7-135">已發佈預設值為 NotPublished。</span><span class="sxs-lookup"><span data-stu-id="514e7-135">Published The default value is NotPublished.</span></span>

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

### <span data-ttu-id="514e7-136">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="514e7-136">-SubscriptionRequired</span></span>
<span data-ttu-id="514e7-137">指出產品是否需要訂閱。</span><span class="sxs-lookup"><span data-stu-id="514e7-137">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="514e7-138">預設值為 [ **$True** ]。</span><span class="sxs-lookup"><span data-stu-id="514e7-138">The default value is **$True**.</span></span>

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

### <span data-ttu-id="514e7-139">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="514e7-139">-SubscriptionsLimit</span></span>
<span data-ttu-id="514e7-140">指定同時進行的訂閱數目上限。</span><span class="sxs-lookup"><span data-stu-id="514e7-140">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="514e7-141">預設值為 [無]。</span><span class="sxs-lookup"><span data-stu-id="514e7-141">The default value is None.</span></span>

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

### <span data-ttu-id="514e7-142">-標題</span><span class="sxs-lookup"><span data-stu-id="514e7-142">-Title</span></span>
<span data-ttu-id="514e7-143">指定產品標題。</span><span class="sxs-lookup"><span data-stu-id="514e7-143">Specifies the product title.</span></span>

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

### <span data-ttu-id="514e7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="514e7-144">CommonParameters</span></span>
<span data-ttu-id="514e7-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="514e7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="514e7-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="514e7-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="514e7-147">輸入</span><span class="sxs-lookup"><span data-stu-id="514e7-147">INPUTS</span></span>

### <span data-ttu-id="514e7-148">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="514e7-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="514e7-149">System.object</span><span class="sxs-lookup"><span data-stu-id="514e7-149">System.String</span></span>

### <span data-ttu-id="514e7-150">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="514e7-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="514e7-151">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="514e7-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="514e7-152">ApiManagement 為 Nullable "1 [PsApiManagementProductState，，ServiceManagement，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]]。）））））））</span><span class="sxs-lookup"><span data-stu-id="514e7-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="514e7-153">輸出</span><span class="sxs-lookup"><span data-stu-id="514e7-153">OUTPUTS</span></span>

### <span data-ttu-id="514e7-154">ServiceManagement. PsApiManagementProduct （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="514e7-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="514e7-155">筆記</span><span class="sxs-lookup"><span data-stu-id="514e7-155">NOTES</span></span>

## <span data-ttu-id="514e7-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="514e7-156">RELATED LINKS</span></span>

[<span data-ttu-id="514e7-157">AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="514e7-157">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="514e7-158">移除-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="514e7-158">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="514e7-159">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="514e7-159">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


