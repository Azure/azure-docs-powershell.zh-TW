---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
ms.openlocfilehash: f28bfc223ed187724aa8702c378bfce5d88755fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623572"
---
# <span data-ttu-id="cc24b-101">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="cc24b-101">Set-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="cc24b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cc24b-102">SYNOPSIS</span></span>
<span data-ttu-id="cc24b-103">設定 API 管理產品詳細資料。</span><span class="sxs-lookup"><span data-stu-id="cc24b-103">Sets the API Management product details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc24b-104">句法</span><span class="sxs-lookup"><span data-stu-id="cc24b-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc24b-105">說明</span><span class="sxs-lookup"><span data-stu-id="cc24b-105">DESCRIPTION</span></span>
<span data-ttu-id="cc24b-106">**AzureRmApiManagementProduct** Cmdlet 會設定 API 管理產品的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="cc24b-106">The **Set-AzureRmApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="cc24b-107">示例</span><span class="sxs-lookup"><span data-stu-id="cc24b-107">EXAMPLES</span></span>

### <span data-ttu-id="cc24b-108">範例1：更新產品詳細資料</span><span class="sxs-lookup"><span data-stu-id="cc24b-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="cc24b-109">這個命令會更新 API 管理產品詳細資料、需要訂閱，然後 unpublishes。</span><span class="sxs-lookup"><span data-stu-id="cc24b-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="cc24b-110">參數</span><span class="sxs-lookup"><span data-stu-id="cc24b-110">PARAMETERS</span></span>

### <span data-ttu-id="cc24b-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="cc24b-111">-ApprovalRequired</span></span>
<span data-ttu-id="cc24b-112">指出產品的訂閱是否需要核准。</span><span class="sxs-lookup"><span data-stu-id="cc24b-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="cc24b-113">預設值為 [ **$False** ]。</span><span class="sxs-lookup"><span data-stu-id="cc24b-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="cc24b-114">-內容</span><span class="sxs-lookup"><span data-stu-id="cc24b-114">-Context</span></span>
<span data-ttu-id="cc24b-115">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="cc24b-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="cc24b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc24b-116">-DefaultProfile</span></span>
<span data-ttu-id="cc24b-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc24b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc24b-118">-描述</span><span class="sxs-lookup"><span data-stu-id="cc24b-118">-Description</span></span>
<span data-ttu-id="cc24b-119">指定產品描述。</span><span class="sxs-lookup"><span data-stu-id="cc24b-119">Specifies the product description.</span></span>

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

### <span data-ttu-id="cc24b-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="cc24b-120">-LegalTerms</span></span>
<span data-ttu-id="cc24b-121">指定產品的使用條款。</span><span class="sxs-lookup"><span data-stu-id="cc24b-121">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="cc24b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc24b-122">-PassThru</span></span>
<span data-ttu-id="cc24b-123">passthru</span><span class="sxs-lookup"><span data-stu-id="cc24b-123">passthru</span></span>

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

### <span data-ttu-id="cc24b-124">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="cc24b-124">-ProductId</span></span>
<span data-ttu-id="cc24b-125">指定現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cc24b-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="cc24b-126">-State</span><span class="sxs-lookup"><span data-stu-id="cc24b-126">-State</span></span>
<span data-ttu-id="cc24b-127">指定產品狀態。</span><span class="sxs-lookup"><span data-stu-id="cc24b-127">Specifies the product state.</span></span>
<span data-ttu-id="cc24b-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="cc24b-128">psdx_paramvalues</span></span>
- <span data-ttu-id="cc24b-129">NotPublished</span><span class="sxs-lookup"><span data-stu-id="cc24b-129">NotPublished</span></span>
- <span data-ttu-id="cc24b-130">時間</span><span class="sxs-lookup"><span data-stu-id="cc24b-130">Published</span></span>

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

### <span data-ttu-id="cc24b-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="cc24b-131">-SubscriptionRequired</span></span>
<span data-ttu-id="cc24b-132">指出產品是否需要訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc24b-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="cc24b-133">此參數的預設值為 [ **$True** ]。</span><span class="sxs-lookup"><span data-stu-id="cc24b-133">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="cc24b-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="cc24b-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="cc24b-135">指定同時進行的訂閱數目上限。</span><span class="sxs-lookup"><span data-stu-id="cc24b-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="cc24b-136">此參數的預設值為1。</span><span class="sxs-lookup"><span data-stu-id="cc24b-136">The default value for this parameter is 1.</span></span>

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

### <span data-ttu-id="cc24b-137">-標題</span><span class="sxs-lookup"><span data-stu-id="cc24b-137">-Title</span></span>
<span data-ttu-id="cc24b-138">指定此 Cmdlet 所設定的產品標題。</span><span class="sxs-lookup"><span data-stu-id="cc24b-138">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="cc24b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc24b-139">CommonParameters</span></span>
<span data-ttu-id="cc24b-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cc24b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc24b-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cc24b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc24b-142">輸入</span><span class="sxs-lookup"><span data-stu-id="cc24b-142">INPUTS</span></span>

### <span data-ttu-id="cc24b-143">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="cc24b-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cc24b-144">System.object</span><span class="sxs-lookup"><span data-stu-id="cc24b-144">System.String</span></span>

### <span data-ttu-id="cc24b-145">系統為 Nullable "1 [[System.object，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="cc24b-145">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="cc24b-146">System.object "1 [[System. Int32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="cc24b-146">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="cc24b-147">ApiManagement 為 Nullable "1 [PsApiManagementProductState，，，ServiceManagement，Version = ServiceManagement，Culture = 中性，PublicKeyToken = null]]。））。</span><span class="sxs-lookup"><span data-stu-id="cc24b-147">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="cc24b-148">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="cc24b-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cc24b-149">輸出</span><span class="sxs-lookup"><span data-stu-id="cc24b-149">OUTPUTS</span></span>

### <span data-ttu-id="cc24b-150">ServiceManagement. PsApiManagementProduct （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="cc24b-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="cc24b-151">筆記</span><span class="sxs-lookup"><span data-stu-id="cc24b-151">NOTES</span></span>

## <span data-ttu-id="cc24b-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc24b-152">RELATED LINKS</span></span>

[<span data-ttu-id="cc24b-153">AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="cc24b-153">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="cc24b-154">新-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="cc24b-154">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="cc24b-155">移除-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="cc24b-155">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)


