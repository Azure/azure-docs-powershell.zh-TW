---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: 26e555be760a71defc7f21f5ffc84cada7a21d04
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917137"
---
# <span data-ttu-id="3cb9a-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="3cb9a-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="3cb9a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3cb9a-102">SYNOPSIS</span></span>
<span data-ttu-id="3cb9a-103">獲得訂閱。</span><span class="sxs-lookup"><span data-stu-id="3cb9a-103">Gets subscriptions.</span></span>

## <span data-ttu-id="3cb9a-104">語法</span><span class="sxs-lookup"><span data-stu-id="3cb9a-104">SYNTAX</span></span>

### <span data-ttu-id="3cb9a-105">GetAllSubscriptions (預設) </span><span class="sxs-lookup"><span data-stu-id="3cb9a-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3cb9a-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3cb9a-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3cb9a-107">GetByProductIdAndUser</span><span class="sxs-lookup"><span data-stu-id="3cb9a-107">GetByProductIdAndUser</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -UserId <String> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3cb9a-108">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="3cb9a-108">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3cb9a-109">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="3cb9a-109">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3cb9a-110">GetByScope</span><span class="sxs-lookup"><span data-stu-id="3cb9a-110">GetByScope</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -Scope <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3cb9a-111">描述</span><span class="sxs-lookup"><span data-stu-id="3cb9a-111">DESCRIPTION</span></span>
<span data-ttu-id="3cb9a-112">**Get-AzApiManagementSubscription** Cmdlet 會取得指定的訂閱，或所有訂閱 ，如果沒有指定訂閱。</span><span class="sxs-lookup"><span data-stu-id="3cb9a-112">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>
<span data-ttu-id="3cb9a-113">按鍵不會包含在結果詳細資料中。</span><span class="sxs-lookup"><span data-stu-id="3cb9a-113">Keys will not be included into result details.</span></span> <span data-ttu-id="3cb9a-114">若要取得金鑰，請使用 **Get-AzApiManagementSubscriptionKey。**</span><span class="sxs-lookup"><span data-stu-id="3cb9a-114">To get keys, use **Get-AzApiManagementSubscriptionKey**.</span></span>

## <span data-ttu-id="3cb9a-115">例子</span><span class="sxs-lookup"><span data-stu-id="3cb9a-115">EXAMPLES</span></span>

### <span data-ttu-id="3cb9a-116">範例 1：取得所有訂閱</span><span class="sxs-lookup"><span data-stu-id="3cb9a-116">Example 1: Get all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="3cb9a-117">此命令會獲得所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="3cb9a-117">This command gets all subscriptions.</span></span>

### <span data-ttu-id="3cb9a-118">範例 2：取得具有指定識別碼的訂閱</span><span class="sxs-lookup"><span data-stu-id="3cb9a-118">Example 2: Get a subscription with a specified ID</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="3cb9a-119">此命令會按識別碼獲得訂閱。</span><span class="sxs-lookup"><span data-stu-id="3cb9a-119">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="3cb9a-120">範例 3：取得使用者的所有訂閱</span><span class="sxs-lookup"><span data-stu-id="3cb9a-120">Example 3: Get all subscriptions for a user</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="3cb9a-121">此命令會獲得使用者的訂閱。</span><span class="sxs-lookup"><span data-stu-id="3cb9a-121">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="3cb9a-122">範例 4：取得產品的所有訂閱</span><span class="sxs-lookup"><span data-stu-id="3cb9a-122">Example 4: Get all subscriptions for a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="3cb9a-123">此命令會獲得產品的所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="3cb9a-123">This command gets all subscriptions for the product.</span></span>

### <span data-ttu-id="3cb9a-124">範例 5：取得範圍的所有訂閱</span><span class="sxs-lookup"><span data-stu-id="3cb9a-124">Example 5: Get all subscriptions for a Scope</span></span>
```powershell
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

<span data-ttu-id="3cb9a-125">此命令會獲得所有已針對全域 api 範圍所配置的訂閱</span><span class="sxs-lookup"><span data-stu-id="3cb9a-125">This command gets all subscriptions which are configured for global api scope</span></span>

### <span data-ttu-id="3cb9a-126">範例 6：取得產品和使用者範圍的所有訂閱</span><span class="sxs-lookup"><span data-stu-id="3cb9a-126">Example 6: Get all subscriptions for a product and user scope</span></span>
```powershell
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

<span data-ttu-id="3cb9a-127">此命令會獲得所有已針對全域 api 範圍所配置的訂閱</span><span class="sxs-lookup"><span data-stu-id="3cb9a-127">This command gets all subscriptions which are configured for global api scope</span></span>

## <span data-ttu-id="3cb9a-128">參數</span><span class="sxs-lookup"><span data-stu-id="3cb9a-128">PARAMETERS</span></span>

### <span data-ttu-id="3cb9a-129">-內容</span><span class="sxs-lookup"><span data-stu-id="3cb9a-129">-Context</span></span>
<span data-ttu-id="3cb9a-130">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="3cb9a-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3cb9a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cb9a-131">-DefaultProfile</span></span>
<span data-ttu-id="3cb9a-132">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3cb9a-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cb9a-133">-ProductId</span><span class="sxs-lookup"><span data-stu-id="3cb9a-133">-ProductId</span></span>
<span data-ttu-id="3cb9a-134">指定產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="3cb9a-134">Specifies a product identifier.</span></span>
<span data-ttu-id="3cb9a-135">如果指定，此 Cmdlet 會根據產品識別碼尋找所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="3cb9a-135">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

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

### <span data-ttu-id="3cb9a-136">-範圍</span><span class="sxs-lookup"><span data-stu-id="3cb9a-136">-Scope</span></span>
<span data-ttu-id="3cb9a-137">範圍識別碼。</span><span class="sxs-lookup"><span data-stu-id="3cb9a-137">Scope identifier.</span></span> <span data-ttu-id="3cb9a-138">訂閱的範圍，無論是 Api 範圍 /apis/{apiId} 或產品範圍 /products/{productId} 或全域 API 範圍 /apis 或全域範圍 /。</span><span class="sxs-lookup"><span data-stu-id="3cb9a-138">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span>

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

### <span data-ttu-id="3cb9a-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3cb9a-139">-SubscriptionId</span></span>
<span data-ttu-id="3cb9a-140">指定訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="3cb9a-140">Specifies a subscription identifier.</span></span>
<span data-ttu-id="3cb9a-141">如果指定，此 Cmdlet 會根據識別碼尋找訂閱。</span><span class="sxs-lookup"><span data-stu-id="3cb9a-141">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="3cb9a-142">-UserId</span><span class="sxs-lookup"><span data-stu-id="3cb9a-142">-UserId</span></span>
<span data-ttu-id="3cb9a-143">指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="3cb9a-143">Specifies a user identifier.</span></span>
<span data-ttu-id="3cb9a-144">如果指定，此 Cmdlet 會根據使用者識別碼尋找所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="3cb9a-144">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

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

### <span data-ttu-id="3cb9a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cb9a-145">CommonParameters</span></span>
<span data-ttu-id="3cb9a-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3cb9a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cb9a-147">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3cb9a-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cb9a-148">輸入</span><span class="sxs-lookup"><span data-stu-id="3cb9a-148">INPUTS</span></span>

### <span data-ttu-id="3cb9a-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="3cb9a-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3cb9a-150">System.String</span><span class="sxs-lookup"><span data-stu-id="3cb9a-150">System.String</span></span>

## <span data-ttu-id="3cb9a-151">輸出</span><span class="sxs-lookup"><span data-stu-id="3cb9a-151">OUTPUTS</span></span>

### <span data-ttu-id="3cb9a-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="3cb9a-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="3cb9a-153">筆記</span><span class="sxs-lookup"><span data-stu-id="3cb9a-153">NOTES</span></span>

## <span data-ttu-id="3cb9a-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="3cb9a-154">RELATED LINKS</span></span>

[<span data-ttu-id="3cb9a-155">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="3cb9a-155">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="3cb9a-156">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="3cb9a-156">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="3cb9a-157">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="3cb9a-157">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


