---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
ms.openlocfilehash: 00186ae370b7f5ccaac14bbdc85ba6b1f7aaa762
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912918"
---
# <span data-ttu-id="a9686-101">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a9686-101">New-AzApiManagementSubscription</span></span>

## <span data-ttu-id="a9686-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a9686-102">SYNOPSIS</span></span>
<span data-ttu-id="a9686-103">建立訂閱。</span><span class="sxs-lookup"><span data-stu-id="a9686-103">Creates a subscription.</span></span>

## <span data-ttu-id="a9686-104">語法</span><span class="sxs-lookup"><span data-stu-id="a9686-104">SYNTAX</span></span>

### <span data-ttu-id="a9686-105">OldSubscriptionModel (預設) </span><span class="sxs-lookup"><span data-stu-id="a9686-105">OldSubscriptionModel (Default)</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9686-106">NewSubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="a9686-106">NewSubscriptionModel</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 [-UserId <String>] -Scope <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9686-107">描述</span><span class="sxs-lookup"><span data-stu-id="a9686-107">DESCRIPTION</span></span>
<span data-ttu-id="a9686-108">**New-AzApiManagementSubscription** Cmdlet 會建立訂閱。</span><span class="sxs-lookup"><span data-stu-id="a9686-108">The **New-AzApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="a9686-109">例子</span><span class="sxs-lookup"><span data-stu-id="a9686-109">EXAMPLES</span></span>

### <span data-ttu-id="a9686-110">範例 1：訂閱使用者至產品</span><span class="sxs-lookup"><span data-stu-id="a9686-110">Example 1: Subscribe a user to a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="a9686-111">此命令會為現有使用者訂閱產品。</span><span class="sxs-lookup"><span data-stu-id="a9686-111">This command subscribes an existing user to a product.</span></span>

### <span data-ttu-id="a9686-112">範例 2：建立所有 Api 範圍的訂閱</span><span class="sxs-lookup"><span data-stu-id="a9686-112">Example 2: Create a subscription for all Api Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/apis" -Name "GlobalApiScope"
```

### <span data-ttu-id="a9686-113">範例 3：建立產品範圍的訂閱</span><span class="sxs-lookup"><span data-stu-id="a9686-113">Example 3: Create a subscription for Product Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/products/starter" -Name "UnlimitedProductSub"
```

## <span data-ttu-id="a9686-114">參數</span><span class="sxs-lookup"><span data-stu-id="a9686-114">PARAMETERS</span></span>

### <span data-ttu-id="a9686-115">-AllowTracing</span><span class="sxs-lookup"><span data-stu-id="a9686-115">-AllowTracing</span></span>
<span data-ttu-id="a9686-116">可決定是否可以在訂閱層級啟用追蹤的標標。</span><span class="sxs-lookup"><span data-stu-id="a9686-116">Flag which determines whether Tracing can be enabled at the Subscription Level.</span></span> <span data-ttu-id="a9686-117">這是選擇性參數，預設為$null。</span><span class="sxs-lookup"><span data-stu-id="a9686-117">This is optional parameter and default is $null.</span></span>

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

### <span data-ttu-id="a9686-118">-內容</span><span class="sxs-lookup"><span data-stu-id="a9686-118">-Context</span></span>
<span data-ttu-id="a9686-119">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="a9686-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a9686-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9686-120">-DefaultProfile</span></span>
<span data-ttu-id="a9686-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a9686-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9686-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="a9686-122">-Name</span></span>
<span data-ttu-id="a9686-123">指定訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="a9686-123">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="a9686-124">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="a9686-124">-PrimaryKey</span></span>
<span data-ttu-id="a9686-125">指定訂閱主鍵。</span><span class="sxs-lookup"><span data-stu-id="a9686-125">Specifies the subscription primary key.</span></span>
<span data-ttu-id="a9686-126">如果未指定此參數，系統會自動產生金鑰。</span><span class="sxs-lookup"><span data-stu-id="a9686-126">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="a9686-127">此參數必須長 1 到 300 個字元。</span><span class="sxs-lookup"><span data-stu-id="a9686-127">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="a9686-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="a9686-128">-ProductId</span></span>
<span data-ttu-id="a9686-129">指定要訂閱的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="a9686-129">Specifies the ID of the product to which to subscribe.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9686-130">-範圍</span><span class="sxs-lookup"><span data-stu-id="a9686-130">-Scope</span></span>
<span data-ttu-id="a9686-131">訂閱的範圍，無論是 Api 範圍 /apis/{apiId} 或產品範圍 /products/{productId} 或全域 API 範圍 /apis 或全域範圍 /。</span><span class="sxs-lookup"><span data-stu-id="a9686-131">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="a9686-132">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="a9686-132">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9686-133">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="a9686-133">-SecondaryKey</span></span>
<span data-ttu-id="a9686-134">指定訂閱次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="a9686-134">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="a9686-135">如果未指定，系統會自動產生此參數。</span><span class="sxs-lookup"><span data-stu-id="a9686-135">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="a9686-136">此參數必須長 1 到 300 個字元。</span><span class="sxs-lookup"><span data-stu-id="a9686-136">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="a9686-137">-State</span><span class="sxs-lookup"><span data-stu-id="a9686-137">-State</span></span>
<span data-ttu-id="a9686-138">指定訂閱狀態。</span><span class="sxs-lookup"><span data-stu-id="a9686-138">Specifies the subscription state.</span></span>
<span data-ttu-id="a9686-139">預設值為$Null。</span><span class="sxs-lookup"><span data-stu-id="a9686-139">The default value is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState]
Parameter Sets: (All)
Aliases:
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9686-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a9686-140">-SubscriptionId</span></span>
<span data-ttu-id="a9686-141">指定訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="a9686-141">Specifies the subscription ID.</span></span>
<span data-ttu-id="a9686-142">如果未指定，會產生此參數。</span><span class="sxs-lookup"><span data-stu-id="a9686-142">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="a9686-143">-UserId</span><span class="sxs-lookup"><span data-stu-id="a9686-143">-UserId</span></span>
<span data-ttu-id="a9686-144">指定訂閱者識別碼。</span><span class="sxs-lookup"><span data-stu-id="a9686-144">Specifies the subscriber ID.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NewSubscriptionModel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9686-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9686-145">CommonParameters</span></span>
<span data-ttu-id="a9686-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a9686-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9686-147">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9686-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9686-148">輸入</span><span class="sxs-lookup"><span data-stu-id="a9686-148">INPUTS</span></span>

### <span data-ttu-id="a9686-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="a9686-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a9686-150">System.String</span><span class="sxs-lookup"><span data-stu-id="a9686-150">System.String</span></span>

### <span data-ttu-id="a9686-151">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="a9686-151">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a9686-152">輸出</span><span class="sxs-lookup"><span data-stu-id="a9686-152">OUTPUTS</span></span>

### <span data-ttu-id="a9686-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a9686-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="a9686-154">筆記</span><span class="sxs-lookup"><span data-stu-id="a9686-154">NOTES</span></span>

## <span data-ttu-id="a9686-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9686-155">RELATED LINKS</span></span>

[<span data-ttu-id="a9686-156">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a9686-156">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="a9686-157">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a9686-157">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="a9686-158">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a9686-158">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


