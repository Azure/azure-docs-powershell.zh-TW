---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
ms.openlocfilehash: dac6e48faba1590897161ab59fed05f1f0b331df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450088"
---
# <span data-ttu-id="d810f-101">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="d810f-101">Set-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="d810f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d810f-102">SYNOPSIS</span></span>
<span data-ttu-id="d810f-103">設定 API 管理產品詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d810f-103">Sets the API Management product details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d810f-104">句法</span><span class="sxs-lookup"><span data-stu-id="d810f-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d810f-105">說明</span><span class="sxs-lookup"><span data-stu-id="d810f-105">DESCRIPTION</span></span>
<span data-ttu-id="d810f-106">**AzureRmApiManagementProduct** Cmdlet 會設定 API 管理產品的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d810f-106">The **Set-AzureRmApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="d810f-107">示例</span><span class="sxs-lookup"><span data-stu-id="d810f-107">EXAMPLES</span></span>

### <span data-ttu-id="d810f-108">範例1：更新產品詳細資料</span><span class="sxs-lookup"><span data-stu-id="d810f-108">Example 1: Update the product details</span></span>
```
PS C:\>Set-AzureRmApiManagementProduct -Context $APImContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="d810f-109">這個命令會更新 API 管理產品詳細資料、需要訂閱，然後 unpublishes。</span><span class="sxs-lookup"><span data-stu-id="d810f-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="d810f-110">參數</span><span class="sxs-lookup"><span data-stu-id="d810f-110">PARAMETERS</span></span>

### <span data-ttu-id="d810f-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="d810f-111">-ApprovalRequired</span></span>
<span data-ttu-id="d810f-112">指出產品的訂閱是否需要核准。</span><span class="sxs-lookup"><span data-stu-id="d810f-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="d810f-113">預設值為 [ **$False** ]。</span><span class="sxs-lookup"><span data-stu-id="d810f-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="d810f-114">-內容</span><span class="sxs-lookup"><span data-stu-id="d810f-114">-Context</span></span>
<span data-ttu-id="d810f-115">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="d810f-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d810f-116">-描述</span><span class="sxs-lookup"><span data-stu-id="d810f-116">-Description</span></span>
<span data-ttu-id="d810f-117">指定產品描述。</span><span class="sxs-lookup"><span data-stu-id="d810f-117">Specifies the product description.</span></span>

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

### <span data-ttu-id="d810f-118">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="d810f-118">-LegalTerms</span></span>
<span data-ttu-id="d810f-119">指定產品的使用條款。</span><span class="sxs-lookup"><span data-stu-id="d810f-119">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="d810f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d810f-120">-PassThru</span></span>
<span data-ttu-id="d810f-121">passthru</span><span class="sxs-lookup"><span data-stu-id="d810f-121">passthru</span></span>

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

### <span data-ttu-id="d810f-122">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="d810f-122">-ProductId</span></span>
<span data-ttu-id="d810f-123">指定現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d810f-123">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="d810f-124">-State</span><span class="sxs-lookup"><span data-stu-id="d810f-124">-State</span></span>
<span data-ttu-id="d810f-125">指定產品狀態。</span><span class="sxs-lookup"><span data-stu-id="d810f-125">Specifies the product state.</span></span>
<span data-ttu-id="d810f-126">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="d810f-126">psdx_paramvalues</span></span>

- <span data-ttu-id="d810f-127">NotPublished</span><span class="sxs-lookup"><span data-stu-id="d810f-127">NotPublished</span></span>
- <span data-ttu-id="d810f-128">時間</span><span class="sxs-lookup"><span data-stu-id="d810f-128">Published</span></span>

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

### <span data-ttu-id="d810f-129">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="d810f-129">-SubscriptionRequired</span></span>
<span data-ttu-id="d810f-130">指出產品是否需要訂閱。</span><span class="sxs-lookup"><span data-stu-id="d810f-130">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="d810f-131">此參數的預設值為 [ **$True** ]。</span><span class="sxs-lookup"><span data-stu-id="d810f-131">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="d810f-132">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="d810f-132">-SubscriptionsLimit</span></span>
<span data-ttu-id="d810f-133">指定同時進行的訂閱數目上限。</span><span class="sxs-lookup"><span data-stu-id="d810f-133">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="d810f-134">此參數的預設值為1。</span><span class="sxs-lookup"><span data-stu-id="d810f-134">The default value for this parameter is 1.</span></span>

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

### <span data-ttu-id="d810f-135">-標題</span><span class="sxs-lookup"><span data-stu-id="d810f-135">-Title</span></span>
<span data-ttu-id="d810f-136">指定此 Cmdlet 所設定的產品標題。</span><span class="sxs-lookup"><span data-stu-id="d810f-136">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="d810f-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d810f-137">-DefaultProfile</span></span>
<span data-ttu-id="d810f-138">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d810f-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d810f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d810f-139">CommonParameters</span></span>
<span data-ttu-id="d810f-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d810f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d810f-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d810f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d810f-142">輸入</span><span class="sxs-lookup"><span data-stu-id="d810f-142">INPUTS</span></span>

## <span data-ttu-id="d810f-143">輸出</span><span class="sxs-lookup"><span data-stu-id="d810f-143">OUTPUTS</span></span>

### <span data-ttu-id="d810f-144">ServiceManagement. PsApiManagementProduct （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="d810f-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="d810f-145">筆記</span><span class="sxs-lookup"><span data-stu-id="d810f-145">NOTES</span></span>

## <span data-ttu-id="d810f-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="d810f-146">RELATED LINKS</span></span>

[<span data-ttu-id="d810f-147">AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="d810f-147">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="d810f-148">新-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="d810f-148">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="d810f-149">移除-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="d810f-149">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)


