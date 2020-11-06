---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
ms.openlocfilehash: 673aa943263a789e7d8be0a63634ddd176e09cae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444824"
---
# <span data-ttu-id="adc5f-101">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="adc5f-101">New-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="adc5f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="adc5f-102">SYNOPSIS</span></span>
<span data-ttu-id="adc5f-103">建立 API 管理產品。</span><span class="sxs-lookup"><span data-stu-id="adc5f-103">Creates an API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="adc5f-104">句法</span><span class="sxs-lookup"><span data-stu-id="adc5f-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adc5f-105">說明</span><span class="sxs-lookup"><span data-stu-id="adc5f-105">DESCRIPTION</span></span>
<span data-ttu-id="adc5f-106">**新的-AzureRmApiManagementProduct** Cmdlet 會建立 API 管理產品。</span><span class="sxs-lookup"><span data-stu-id="adc5f-106">The **New-AzureRmApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="adc5f-107">示例</span><span class="sxs-lookup"><span data-stu-id="adc5f-107">EXAMPLES</span></span>

### <span data-ttu-id="adc5f-108">範例1：建立不需要訂閱的產品</span><span class="sxs-lookup"><span data-stu-id="adc5f-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="adc5f-109">這個命令會建立 API 管理產品。</span><span class="sxs-lookup"><span data-stu-id="adc5f-109">This command creates an API Management product.</span></span>
<span data-ttu-id="adc5f-110">不需要訂閱。</span><span class="sxs-lookup"><span data-stu-id="adc5f-110">No subscription is required.</span></span>

### <span data-ttu-id="adc5f-111">範例2：建立需要訂閱與核准的產品</span><span class="sxs-lookup"><span data-stu-id="adc5f-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProduct -Context $apimContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="adc5f-112">這個命令會建立產品。</span><span class="sxs-lookup"><span data-stu-id="adc5f-112">This command creates a product.</span></span>
<span data-ttu-id="adc5f-113">訂閱與核准是必要的。</span><span class="sxs-lookup"><span data-stu-id="adc5f-113">A subscription and approval are required.</span></span>
<span data-ttu-id="adc5f-114">這個命令會將通知期間設定為10天。</span><span class="sxs-lookup"><span data-stu-id="adc5f-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="adc5f-115">訂閱持續時間已設定為一年。</span><span class="sxs-lookup"><span data-stu-id="adc5f-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="adc5f-116">參數</span><span class="sxs-lookup"><span data-stu-id="adc5f-116">PARAMETERS</span></span>

### <span data-ttu-id="adc5f-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="adc5f-117">-ApprovalRequired</span></span>
<span data-ttu-id="adc5f-118">指出該產品的訂閱是否需要核准。</span><span class="sxs-lookup"><span data-stu-id="adc5f-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="adc5f-119">根據預設，此參數是 **$False** 的。</span><span class="sxs-lookup"><span data-stu-id="adc5f-119">By default, this parameter is **$False**.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adc5f-120">-內容</span><span class="sxs-lookup"><span data-stu-id="adc5f-120">-Context</span></span>
<span data-ttu-id="adc5f-121">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="adc5f-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adc5f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adc5f-122">-DefaultProfile</span></span>
<span data-ttu-id="adc5f-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="adc5f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="adc5f-124">-描述</span><span class="sxs-lookup"><span data-stu-id="adc5f-124">-Description</span></span>
<span data-ttu-id="adc5f-125">指定產品描述。</span><span class="sxs-lookup"><span data-stu-id="adc5f-125">Specifies the product description.</span></span>

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

### <span data-ttu-id="adc5f-126">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="adc5f-126">-LegalTerms</span></span>
<span data-ttu-id="adc5f-127">指定產品的使用條款。</span><span class="sxs-lookup"><span data-stu-id="adc5f-127">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="adc5f-128">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="adc5f-128">-ProductId</span></span>
<span data-ttu-id="adc5f-129">指定新產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="adc5f-129">Specifies the identifier of new product.</span></span>
<span data-ttu-id="adc5f-130">如果您沒有指定此參數，則會產生新的產品。</span><span class="sxs-lookup"><span data-stu-id="adc5f-130">If you do not specify this parameter, a new product is generated.</span></span>

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

### <span data-ttu-id="adc5f-131">-State</span><span class="sxs-lookup"><span data-stu-id="adc5f-131">-State</span></span>
<span data-ttu-id="adc5f-132">指定產品狀態。</span><span class="sxs-lookup"><span data-stu-id="adc5f-132">Specifies the product state.</span></span>
<span data-ttu-id="adc5f-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="adc5f-133">psdx_paramvalues</span></span>

- <span data-ttu-id="adc5f-134">NotPublished</span><span class="sxs-lookup"><span data-stu-id="adc5f-134">NotPublished</span></span>
- <span data-ttu-id="adc5f-135">時間</span><span class="sxs-lookup"><span data-stu-id="adc5f-135">Published</span></span> 

<span data-ttu-id="adc5f-136">預設值為 NotPublished。</span><span class="sxs-lookup"><span data-stu-id="adc5f-136">The default value is NotPublished.</span></span>

```yaml
Type: PsApiManagementProductState
Parameter Sets: (All)
Aliases: 
Accepted values: NotPublished, Published

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adc5f-137">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="adc5f-137">-SubscriptionRequired</span></span>
<span data-ttu-id="adc5f-138">指出產品是否需要訂閱。</span><span class="sxs-lookup"><span data-stu-id="adc5f-138">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="adc5f-139">預設值為 [ **$True** ]。</span><span class="sxs-lookup"><span data-stu-id="adc5f-139">The default value is **$True**.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adc5f-140">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="adc5f-140">-SubscriptionsLimit</span></span>
<span data-ttu-id="adc5f-141">指定同時進行的訂閱數目上限。</span><span class="sxs-lookup"><span data-stu-id="adc5f-141">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="adc5f-142">預設值為1。</span><span class="sxs-lookup"><span data-stu-id="adc5f-142">The default value is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adc5f-143">-標題</span><span class="sxs-lookup"><span data-stu-id="adc5f-143">-Title</span></span>
<span data-ttu-id="adc5f-144">指定產品標題。</span><span class="sxs-lookup"><span data-stu-id="adc5f-144">Specifies the product title.</span></span>

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

### <span data-ttu-id="adc5f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adc5f-145">CommonParameters</span></span>
<span data-ttu-id="adc5f-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="adc5f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adc5f-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="adc5f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adc5f-148">輸入</span><span class="sxs-lookup"><span data-stu-id="adc5f-148">INPUTS</span></span>

### <span data-ttu-id="adc5f-149">所有</span><span class="sxs-lookup"><span data-stu-id="adc5f-149">None</span></span>
<span data-ttu-id="adc5f-150">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="adc5f-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="adc5f-151">輸出</span><span class="sxs-lookup"><span data-stu-id="adc5f-151">OUTPUTS</span></span>

### <span data-ttu-id="adc5f-152">ServiceManagement. PsApiManagementProduct （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="adc5f-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="adc5f-153">筆記</span><span class="sxs-lookup"><span data-stu-id="adc5f-153">NOTES</span></span>

## <span data-ttu-id="adc5f-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="adc5f-154">RELATED LINKS</span></span>

[<span data-ttu-id="adc5f-155">AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="adc5f-155">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="adc5f-156">移除-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="adc5f-156">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="adc5f-157">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="adc5f-157">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


