---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
ms.openlocfilehash: ea68d17d482a73a528cfe450a84700e48bfdd9f9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971328"
---
# <span data-ttu-id="739db-101">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="739db-101">New-AzApiManagementSubscription</span></span>

## <span data-ttu-id="739db-102">摘要</span><span class="sxs-lookup"><span data-stu-id="739db-102">SYNOPSIS</span></span>
<span data-ttu-id="739db-103">建立訂閱。</span><span class="sxs-lookup"><span data-stu-id="739db-103">Creates a subscription.</span></span>

## <span data-ttu-id="739db-104">句法</span><span class="sxs-lookup"><span data-stu-id="739db-104">SYNTAX</span></span>

### <span data-ttu-id="739db-105">OldSubscriptionModel (預設) </span><span class="sxs-lookup"><span data-stu-id="739db-105">OldSubscriptionModel (Default)</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="739db-106">NewSubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="739db-106">NewSubscriptionModel</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 [-UserId <String>] -Scope <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="739db-107">說明</span><span class="sxs-lookup"><span data-stu-id="739db-107">DESCRIPTION</span></span>
<span data-ttu-id="739db-108">**新的-AzApiManagementSubscription** Cmdlet 會建立訂閱。</span><span class="sxs-lookup"><span data-stu-id="739db-108">The **New-AzApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="739db-109">示例</span><span class="sxs-lookup"><span data-stu-id="739db-109">EXAMPLES</span></span>

### <span data-ttu-id="739db-110">範例1：為使用者訂閱產品</span><span class="sxs-lookup"><span data-stu-id="739db-110">Example 1: Subscribe a user to a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="739db-111">這個命令會將現有的使用者訂閱至產品。</span><span class="sxs-lookup"><span data-stu-id="739db-111">This command subscribes an existing user to a product.</span></span>

### <span data-ttu-id="739db-112">範例2：為所有 Api 範圍建立訂閱</span><span class="sxs-lookup"><span data-stu-id="739db-112">Example 2: Create a subscription for all Api Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/apis" -Name "GlobalApiScope"
```

### <span data-ttu-id="739db-113">範例3：建立產品範圍的訂閱</span><span class="sxs-lookup"><span data-stu-id="739db-113">Example 3: Create a subscription for Product Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/products/starter" -Name "UnlimitedProductSub"
```

## <span data-ttu-id="739db-114">參數</span><span class="sxs-lookup"><span data-stu-id="739db-114">PARAMETERS</span></span>

### <span data-ttu-id="739db-115">-AllowTracing</span><span class="sxs-lookup"><span data-stu-id="739db-115">-AllowTracing</span></span>
<span data-ttu-id="739db-116">判斷是否可在訂閱層級啟用追蹤的標誌。</span><span class="sxs-lookup"><span data-stu-id="739db-116">Flag which determines whether Tracing can be enabled at the Subscription Level.</span></span> <span data-ttu-id="739db-117">此為選用的參數，預設值為 $null。</span><span class="sxs-lookup"><span data-stu-id="739db-117">This is optional parameter and default is $null.</span></span>

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

### <span data-ttu-id="739db-118">-內容</span><span class="sxs-lookup"><span data-stu-id="739db-118">-Context</span></span>
<span data-ttu-id="739db-119">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="739db-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="739db-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="739db-120">-DefaultProfile</span></span>
<span data-ttu-id="739db-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="739db-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="739db-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="739db-122">-Name</span></span>
<span data-ttu-id="739db-123">指定訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="739db-123">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="739db-124">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="739db-124">-PrimaryKey</span></span>
<span data-ttu-id="739db-125">指定訂閱主鍵。</span><span class="sxs-lookup"><span data-stu-id="739db-125">Specifies the subscription primary key.</span></span>
<span data-ttu-id="739db-126">如果未指定此參數，則會自動產生金鑰。</span><span class="sxs-lookup"><span data-stu-id="739db-126">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="739db-127">這個參數必須是1到300個字元長。</span><span class="sxs-lookup"><span data-stu-id="739db-127">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="739db-128">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="739db-128">-ProductId</span></span>
<span data-ttu-id="739db-129">指定要訂閱的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="739db-129">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="739db-130">-範圍</span><span class="sxs-lookup"><span data-stu-id="739db-130">-Scope</span></span>
<span data-ttu-id="739db-131">訂閱的範圍（無論是 Api 範圍/apis/{apiId} 或產品範圍/products/{productId}），還是全域 API 範圍/apis 或全域作用中。</span><span class="sxs-lookup"><span data-stu-id="739db-131">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="739db-132">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="739db-132">This parameter is required.</span></span>

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

### <span data-ttu-id="739db-133">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="739db-133">-SecondaryKey</span></span>
<span data-ttu-id="739db-134">指定訂閱次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="739db-134">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="739db-135">如果沒有指定，則會自動產生此參數。</span><span class="sxs-lookup"><span data-stu-id="739db-135">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="739db-136">這個參數必須是1到300個字元長。</span><span class="sxs-lookup"><span data-stu-id="739db-136">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="739db-137">-State</span><span class="sxs-lookup"><span data-stu-id="739db-137">-State</span></span>
<span data-ttu-id="739db-138">指定訂閱狀態。</span><span class="sxs-lookup"><span data-stu-id="739db-138">Specifies the subscription state.</span></span>
<span data-ttu-id="739db-139">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="739db-139">The default value is $Null.</span></span>

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

### <span data-ttu-id="739db-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="739db-140">-SubscriptionId</span></span>
<span data-ttu-id="739db-141">指定訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="739db-141">Specifies the subscription ID.</span></span>
<span data-ttu-id="739db-142">如果沒有指定，則會產生此參數。</span><span class="sxs-lookup"><span data-stu-id="739db-142">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="739db-143">-UserId</span><span class="sxs-lookup"><span data-stu-id="739db-143">-UserId</span></span>
<span data-ttu-id="739db-144">指定訂閱者 ID。</span><span class="sxs-lookup"><span data-stu-id="739db-144">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="739db-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="739db-145">CommonParameters</span></span>
<span data-ttu-id="739db-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="739db-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="739db-147">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="739db-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="739db-148">輸入</span><span class="sxs-lookup"><span data-stu-id="739db-148">INPUTS</span></span>

### <span data-ttu-id="739db-149">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="739db-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="739db-150">System.object</span><span class="sxs-lookup"><span data-stu-id="739db-150">System.String</span></span>

### <span data-ttu-id="739db-151">ApiManagement 為 Nullable "1 [PsApiManagementSubscriptionState，，ServiceManagement，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]]。）））））））</span><span class="sxs-lookup"><span data-stu-id="739db-151">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="739db-152">輸出</span><span class="sxs-lookup"><span data-stu-id="739db-152">OUTPUTS</span></span>

### <span data-ttu-id="739db-153">ServiceManagement. PsApiManagementSubscription （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="739db-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="739db-154">筆記</span><span class="sxs-lookup"><span data-stu-id="739db-154">NOTES</span></span>

## <span data-ttu-id="739db-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="739db-155">RELATED LINKS</span></span>

[<span data-ttu-id="739db-156">AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="739db-156">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="739db-157">移除-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="739db-157">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="739db-158">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="739db-158">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


