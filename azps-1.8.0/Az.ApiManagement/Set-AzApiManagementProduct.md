---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
ms.openlocfilehash: f60bf40cd6226979955f71e413be3914fc05c417
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788741"
---
# <span data-ttu-id="a472c-101">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a472c-101">Set-AzApiManagementProduct</span></span>

## <span data-ttu-id="a472c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a472c-102">SYNOPSIS</span></span>
<span data-ttu-id="a472c-103">設定 API 管理產品詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a472c-103">Sets the API Management product details.</span></span>

## <span data-ttu-id="a472c-104">句法</span><span class="sxs-lookup"><span data-stu-id="a472c-104">SYNTAX</span></span>

```
Set-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a472c-105">說明</span><span class="sxs-lookup"><span data-stu-id="a472c-105">DESCRIPTION</span></span>
<span data-ttu-id="a472c-106">**AzApiManagementProduct** Cmdlet 會設定 API 管理產品的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a472c-106">The **Set-AzApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="a472c-107">示例</span><span class="sxs-lookup"><span data-stu-id="a472c-107">EXAMPLES</span></span>

### <span data-ttu-id="a472c-108">範例1：更新產品詳細資料</span><span class="sxs-lookup"><span data-stu-id="a472c-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="a472c-109">這個命令會更新 API 管理產品詳細資料、需要訂閱，然後 unpublishes。</span><span class="sxs-lookup"><span data-stu-id="a472c-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="a472c-110">參數</span><span class="sxs-lookup"><span data-stu-id="a472c-110">PARAMETERS</span></span>

### <span data-ttu-id="a472c-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="a472c-111">-ApprovalRequired</span></span>
<span data-ttu-id="a472c-112">指出產品的訂閱是否需要核准。</span><span class="sxs-lookup"><span data-stu-id="a472c-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="a472c-113">預設值為 [ **$False** ]。</span><span class="sxs-lookup"><span data-stu-id="a472c-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="a472c-114">-內容</span><span class="sxs-lookup"><span data-stu-id="a472c-114">-Context</span></span>
<span data-ttu-id="a472c-115">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="a472c-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a472c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a472c-116">-DefaultProfile</span></span>
<span data-ttu-id="a472c-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a472c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a472c-118">-描述</span><span class="sxs-lookup"><span data-stu-id="a472c-118">-Description</span></span>
<span data-ttu-id="a472c-119">指定產品描述。</span><span class="sxs-lookup"><span data-stu-id="a472c-119">Specifies the product description.</span></span>

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

### <span data-ttu-id="a472c-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="a472c-120">-LegalTerms</span></span>
<span data-ttu-id="a472c-121">指定產品的使用條款。</span><span class="sxs-lookup"><span data-stu-id="a472c-121">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="a472c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a472c-122">-PassThru</span></span>
<span data-ttu-id="a472c-123">passthru</span><span class="sxs-lookup"><span data-stu-id="a472c-123">passthru</span></span>

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

### <span data-ttu-id="a472c-124">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="a472c-124">-ProductId</span></span>
<span data-ttu-id="a472c-125">指定現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a472c-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="a472c-126">-State</span><span class="sxs-lookup"><span data-stu-id="a472c-126">-State</span></span>
<span data-ttu-id="a472c-127">指定產品狀態。</span><span class="sxs-lookup"><span data-stu-id="a472c-127">Specifies the product state.</span></span>
<span data-ttu-id="a472c-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="a472c-128">psdx_paramvalues</span></span>
- <span data-ttu-id="a472c-129">NotPublished</span><span class="sxs-lookup"><span data-stu-id="a472c-129">NotPublished</span></span>
- <span data-ttu-id="a472c-130">時間</span><span class="sxs-lookup"><span data-stu-id="a472c-130">Published</span></span>

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

### <span data-ttu-id="a472c-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="a472c-131">-SubscriptionRequired</span></span>
<span data-ttu-id="a472c-132">指出產品是否需要訂閱。</span><span class="sxs-lookup"><span data-stu-id="a472c-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="a472c-133">此參數的預設值為 [ **$True** ]。</span><span class="sxs-lookup"><span data-stu-id="a472c-133">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="a472c-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="a472c-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="a472c-135">指定同時進行的訂閱數目上限。</span><span class="sxs-lookup"><span data-stu-id="a472c-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="a472c-136">此參數的預設值為1。</span><span class="sxs-lookup"><span data-stu-id="a472c-136">The default value for this parameter is 1.</span></span>

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

### <span data-ttu-id="a472c-137">-標題</span><span class="sxs-lookup"><span data-stu-id="a472c-137">-Title</span></span>
<span data-ttu-id="a472c-138">指定此 Cmdlet 所設定的產品標題。</span><span class="sxs-lookup"><span data-stu-id="a472c-138">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="a472c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a472c-139">CommonParameters</span></span>
<span data-ttu-id="a472c-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a472c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a472c-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a472c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a472c-142">輸入</span><span class="sxs-lookup"><span data-stu-id="a472c-142">INPUTS</span></span>

### <span data-ttu-id="a472c-143">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="a472c-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a472c-144">System.object</span><span class="sxs-lookup"><span data-stu-id="a472c-144">System.String</span></span>

### <span data-ttu-id="a472c-145">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a472c-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a472c-146">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a472c-146">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a472c-147">ApiManagement 為 Nullable "1 [PsApiManagementProductState，，ServiceManagement，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]]。）））））））</span><span class="sxs-lookup"><span data-stu-id="a472c-147">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="a472c-148">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="a472c-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a472c-149">輸出</span><span class="sxs-lookup"><span data-stu-id="a472c-149">OUTPUTS</span></span>

### <span data-ttu-id="a472c-150">ServiceManagement. PsApiManagementProduct （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="a472c-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="a472c-151">筆記</span><span class="sxs-lookup"><span data-stu-id="a472c-151">NOTES</span></span>

## <span data-ttu-id="a472c-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="a472c-152">RELATED LINKS</span></span>

[<span data-ttu-id="a472c-153">AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a472c-153">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="a472c-154">新-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a472c-154">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="a472c-155">移除-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a472c-155">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)


