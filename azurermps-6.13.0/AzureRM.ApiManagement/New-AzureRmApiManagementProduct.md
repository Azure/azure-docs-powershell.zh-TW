---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
ms.openlocfilehash: 636a969f6aef013ee947afbb43d398871848818a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451963"
---
# <span data-ttu-id="a2ba1-101">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a2ba1-101">New-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="a2ba1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a2ba1-102">SYNOPSIS</span></span>
<span data-ttu-id="a2ba1-103">建立 API 管理產品。</span><span class="sxs-lookup"><span data-stu-id="a2ba1-103">Creates an API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2ba1-104">句法</span><span class="sxs-lookup"><span data-stu-id="a2ba1-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2ba1-105">說明</span><span class="sxs-lookup"><span data-stu-id="a2ba1-105">DESCRIPTION</span></span>
<span data-ttu-id="a2ba1-106">**新的-AzureRmApiManagementProduct** Cmdlet 會建立 API 管理產品。</span><span class="sxs-lookup"><span data-stu-id="a2ba1-106">The **New-AzureRmApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="a2ba1-107">示例</span><span class="sxs-lookup"><span data-stu-id="a2ba1-107">EXAMPLES</span></span>

### <span data-ttu-id="a2ba1-108">範例1：建立不需要訂閱的產品</span><span class="sxs-lookup"><span data-stu-id="a2ba1-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="a2ba1-109">這個命令會建立 API 管理產品。</span><span class="sxs-lookup"><span data-stu-id="a2ba1-109">This command creates an API Management product.</span></span>
<span data-ttu-id="a2ba1-110">不需要訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2ba1-110">No subscription is required.</span></span>

### <span data-ttu-id="a2ba1-111">範例2：建立需要訂閱與核准的產品</span><span class="sxs-lookup"><span data-stu-id="a2ba1-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProduct -Context $apimContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="a2ba1-112">這個命令會建立產品。</span><span class="sxs-lookup"><span data-stu-id="a2ba1-112">This command creates a product.</span></span>
<span data-ttu-id="a2ba1-113">訂閱與核准是必要的。</span><span class="sxs-lookup"><span data-stu-id="a2ba1-113">A subscription and approval are required.</span></span>
<span data-ttu-id="a2ba1-114">這個命令會將通知期間設定為10天。</span><span class="sxs-lookup"><span data-stu-id="a2ba1-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="a2ba1-115">訂閱持續時間已設定為一年。</span><span class="sxs-lookup"><span data-stu-id="a2ba1-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="a2ba1-116">參數</span><span class="sxs-lookup"><span data-stu-id="a2ba1-116">PARAMETERS</span></span>

### <span data-ttu-id="a2ba1-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="a2ba1-117">-ApprovalRequired</span></span>
<span data-ttu-id="a2ba1-118">指出該產品的訂閱是否需要核准。</span><span class="sxs-lookup"><span data-stu-id="a2ba1-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="a2ba1-119">根據預設，此參數是 **$False** 的。</span><span class="sxs-lookup"><span data-stu-id="a2ba1-119">By default, this parameter is **$False**.</span></span>

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

### <span data-ttu-id="a2ba1-120">-內容</span><span class="sxs-lookup"><span data-stu-id="a2ba1-120">-Context</span></span>
<span data-ttu-id="a2ba1-121">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="a2ba1-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2ba1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2ba1-122">-DefaultProfile</span></span>
<span data-ttu-id="a2ba1-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2ba1-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2ba1-124">-描述</span><span class="sxs-lookup"><span data-stu-id="a2ba1-124">-Description</span></span>
<span data-ttu-id="a2ba1-125">指定產品描述。</span><span class="sxs-lookup"><span data-stu-id="a2ba1-125">Specifies the product description.</span></span>

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

### <span data-ttu-id="a2ba1-126">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="a2ba1-126">-LegalTerms</span></span>
<span data-ttu-id="a2ba1-127">指定產品的使用條款。</span><span class="sxs-lookup"><span data-stu-id="a2ba1-127">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="a2ba1-128">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="a2ba1-128">-ProductId</span></span>
<span data-ttu-id="a2ba1-129">指定新產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a2ba1-129">Specifies the identifier of new product.</span></span>
<span data-ttu-id="a2ba1-130">如果您沒有指定此參數，則會產生新的產品。</span><span class="sxs-lookup"><span data-stu-id="a2ba1-130">If you do not specify this parameter, a new product is generated.</span></span>

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

### <span data-ttu-id="a2ba1-131">-State</span><span class="sxs-lookup"><span data-stu-id="a2ba1-131">-State</span></span>
<span data-ttu-id="a2ba1-132">指定產品狀態。</span><span class="sxs-lookup"><span data-stu-id="a2ba1-132">Specifies the product state.</span></span>
<span data-ttu-id="a2ba1-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="a2ba1-133">psdx_paramvalues</span></span>
- <span data-ttu-id="a2ba1-134">NotPublished</span><span class="sxs-lookup"><span data-stu-id="a2ba1-134">NotPublished</span></span>
- <span data-ttu-id="a2ba1-135">已發佈預設值為 NotPublished。</span><span class="sxs-lookup"><span data-stu-id="a2ba1-135">Published The default value is NotPublished.</span></span>

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

### <span data-ttu-id="a2ba1-136">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="a2ba1-136">-SubscriptionRequired</span></span>
<span data-ttu-id="a2ba1-137">指出產品是否需要訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2ba1-137">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="a2ba1-138">預設值為 [ **$True** ]。</span><span class="sxs-lookup"><span data-stu-id="a2ba1-138">The default value is **$True**.</span></span>

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

### <span data-ttu-id="a2ba1-139">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="a2ba1-139">-SubscriptionsLimit</span></span>
<span data-ttu-id="a2ba1-140">指定同時進行的訂閱數目上限。</span><span class="sxs-lookup"><span data-stu-id="a2ba1-140">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="a2ba1-141">預設值為1。</span><span class="sxs-lookup"><span data-stu-id="a2ba1-141">The default value is 1.</span></span>

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

### <span data-ttu-id="a2ba1-142">-標題</span><span class="sxs-lookup"><span data-stu-id="a2ba1-142">-Title</span></span>
<span data-ttu-id="a2ba1-143">指定產品標題。</span><span class="sxs-lookup"><span data-stu-id="a2ba1-143">Specifies the product title.</span></span>

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

### <span data-ttu-id="a2ba1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2ba1-144">CommonParameters</span></span>
<span data-ttu-id="a2ba1-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a2ba1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2ba1-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a2ba1-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2ba1-147">輸入</span><span class="sxs-lookup"><span data-stu-id="a2ba1-147">INPUTS</span></span>

### <span data-ttu-id="a2ba1-148">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="a2ba1-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a2ba1-149">System.object</span><span class="sxs-lookup"><span data-stu-id="a2ba1-149">System.String</span></span>

### <span data-ttu-id="a2ba1-150">系統為 Nullable "1 [[System.object，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a2ba1-150">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="a2ba1-151">System.object "1 [[System. Int32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a2ba1-151">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="a2ba1-152">ApiManagement 為 Nullable "1 [PsApiManagementProductState，，，ServiceManagement，Version = ServiceManagement，Culture = 中性，PublicKeyToken = null]]。））。</span><span class="sxs-lookup"><span data-stu-id="a2ba1-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a2ba1-153">輸出</span><span class="sxs-lookup"><span data-stu-id="a2ba1-153">OUTPUTS</span></span>

### <span data-ttu-id="a2ba1-154">ServiceManagement. PsApiManagementProduct （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="a2ba1-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="a2ba1-155">筆記</span><span class="sxs-lookup"><span data-stu-id="a2ba1-155">NOTES</span></span>

## <span data-ttu-id="a2ba1-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2ba1-156">RELATED LINKS</span></span>

[<span data-ttu-id="a2ba1-157">AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a2ba1-157">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="a2ba1-158">移除-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a2ba1-158">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="a2ba1-159">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a2ba1-159">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


