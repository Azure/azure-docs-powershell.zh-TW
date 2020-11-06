---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: 13ca3444a48d79b3708042f6cf8fd0229f80676a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614036"
---
# <span data-ttu-id="e8106-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e8106-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="e8106-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8106-102">SYNOPSIS</span></span>
<span data-ttu-id="e8106-103">取得訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8106-103">Gets subscriptions.</span></span>

## <span data-ttu-id="e8106-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8106-104">SYNTAX</span></span>

### <span data-ttu-id="e8106-105">GetAllSubscriptions (預設) </span><span class="sxs-lookup"><span data-stu-id="e8106-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8106-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e8106-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8106-107">GetByProductIdAndUser</span><span class="sxs-lookup"><span data-stu-id="e8106-107">GetByProductIdAndUser</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -UserId <String> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8106-108">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="e8106-108">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8106-109">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="e8106-109">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8106-110">GetByScope</span><span class="sxs-lookup"><span data-stu-id="e8106-110">GetByScope</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -Scope <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8106-111">說明</span><span class="sxs-lookup"><span data-stu-id="e8106-111">DESCRIPTION</span></span>
<span data-ttu-id="e8106-112">如果沒有指定訂閱， **AzApiManagementSubscription** Cmdlet 會取得指定的訂閱或所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8106-112">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="e8106-113">示例</span><span class="sxs-lookup"><span data-stu-id="e8106-113">EXAMPLES</span></span>

### <span data-ttu-id="e8106-114">範例1：取得所有訂閱</span><span class="sxs-lookup"><span data-stu-id="e8106-114">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="e8106-115">這個命令會取得所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8106-115">This command gets all subscriptions.</span></span>

### <span data-ttu-id="e8106-116">範例2：取得具有指定識別碼的訂閱</span><span class="sxs-lookup"><span data-stu-id="e8106-116">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="e8106-117">這個命令透過識別碼取得訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8106-117">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="e8106-118">範例3：取得使用者的所有訂閱</span><span class="sxs-lookup"><span data-stu-id="e8106-118">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="e8106-119">這個命令會取得使用者的訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8106-119">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="e8106-120">範例4：取得產品的所有訂閱</span><span class="sxs-lookup"><span data-stu-id="e8106-120">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="e8106-121">這個命令會取得該產品的所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8106-121">This command gets all subscriptions for the product.</span></span>

### <span data-ttu-id="e8106-122">範例5：取得作用中的所有訂閱</span><span class="sxs-lookup"><span data-stu-id="e8106-122">Example 5: Get all subscriptions for a Scope</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -Scope "/apis"

SubscriptionId    : allApScope
UserId            :
OwnerId           :
ProductId         :
Scope             : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apis
Name              : All Api Scope
State             : Active
CreatedDate       : 6/18/2019 5:53:49 PM
StartDate         :
ExpirationDate    :
EndDate           :
NotificationDate  :
PrimaryKey        : 5e48532634114fe999a6979ce0d63a64
SecondaryKey      : 0a8efaf85a664aa0a412241015c7c8f6
StateComment      :
AllowTracing      : False
Id                : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/subscriptions/allApScope
ResourceGroupName : Api-Default-East-US
ServiceName       : contoso
```

<span data-ttu-id="e8106-123">這個命令會取得所有針對全域 api 範圍設定的訂閱</span><span class="sxs-lookup"><span data-stu-id="e8106-123">This command gets all subscriptions which are configured for global api scope</span></span>

### <span data-ttu-id="e8106-124">範例5：取得產品和使用者範圍的所有訂閱</span><span class="sxs-lookup"><span data-stu-id="e8106-124">Example 5: Get all subscriptions for a product and user scope</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId 59b872f28a82740f547e6270 -UserId 1

SubscriptionId    : 59b872f38a82741750c8da56
UserId            : 1
OwnerId           : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/users/1
ProductId         : 59b872f28a82740f547e6270
Scope             : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/products/59b872f28a82740f547e6270
Name              :
State             : Active
CreatedDate       : 9/12/2017 11:51:15 PM
StartDate         : 9/12/2017 12:00:00 AM
ExpirationDate    :
EndDate           :
NotificationDate  :
PrimaryKey        : 7e64ef904b194706835febf87f729bb0
SecondaryKey      : 0354fccef73e43feb82e5c5da17674d5
StateComment      :
AllowTracing      : True
Id                : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/subscriptions/59b872f38a82741750c8da56
ResourceGroupName : Api-Default-East-US
ServiceName       : contoso
```

<span data-ttu-id="e8106-125">這個命令會取得所有針對全域 api 範圍設定的訂閱</span><span class="sxs-lookup"><span data-stu-id="e8106-125">This command gets all subscriptions which are configured for global api scope</span></span>

## <span data-ttu-id="e8106-126">參數</span><span class="sxs-lookup"><span data-stu-id="e8106-126">PARAMETERS</span></span>

### <span data-ttu-id="e8106-127">-內容</span><span class="sxs-lookup"><span data-stu-id="e8106-127">-Context</span></span>
<span data-ttu-id="e8106-128">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="e8106-128">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e8106-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8106-129">-DefaultProfile</span></span>
<span data-ttu-id="e8106-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8106-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8106-131">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="e8106-131">-ProductId</span></span>
<span data-ttu-id="e8106-132">指定產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8106-132">Specifies a product identifier.</span></span>
<span data-ttu-id="e8106-133">如果已指定，此 Cmdlet 會依產品識別碼尋找所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8106-133">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductIdAndUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8106-134">-範圍</span><span class="sxs-lookup"><span data-stu-id="e8106-134">-Scope</span></span>
<span data-ttu-id="e8106-135">範圍識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8106-135">Scope identifier.</span></span> <span data-ttu-id="e8106-136">訂閱的範圍（無論是 Api 範圍/apis/{apiId} 或產品範圍/products/{productId}），還是全域 API 範圍/apis 或全域作用中。</span><span class="sxs-lookup"><span data-stu-id="e8106-136">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8106-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e8106-137">-SubscriptionId</span></span>
<span data-ttu-id="e8106-138">指定訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8106-138">Specifies a subscription identifier.</span></span>
<span data-ttu-id="e8106-139">如果已指定，此 Cmdlet 會依識別碼尋找訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8106-139">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8106-140">-UserId</span><span class="sxs-lookup"><span data-stu-id="e8106-140">-UserId</span></span>
<span data-ttu-id="e8106-141">指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8106-141">Specifies a user identifier.</span></span>
<span data-ttu-id="e8106-142">如果已指定，此 Cmdlet 會依使用者識別碼尋找所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8106-142">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductIdAndUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8106-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8106-143">CommonParameters</span></span>
<span data-ttu-id="e8106-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8106-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8106-145">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e8106-145">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8106-146">輸入</span><span class="sxs-lookup"><span data-stu-id="e8106-146">INPUTS</span></span>

### <span data-ttu-id="e8106-147">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="e8106-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e8106-148">System.object</span><span class="sxs-lookup"><span data-stu-id="e8106-148">System.String</span></span>

## <span data-ttu-id="e8106-149">輸出</span><span class="sxs-lookup"><span data-stu-id="e8106-149">OUTPUTS</span></span>

### <span data-ttu-id="e8106-150">ServiceManagement. PsApiManagementSubscription （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="e8106-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="e8106-151">筆記</span><span class="sxs-lookup"><span data-stu-id="e8106-151">NOTES</span></span>

## <span data-ttu-id="e8106-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8106-152">RELATED LINKS</span></span>

[<span data-ttu-id="e8106-153">新-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e8106-153">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="e8106-154">移除-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e8106-154">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="e8106-155">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e8106-155">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


