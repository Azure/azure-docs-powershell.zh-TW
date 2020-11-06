---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 1f863ad8e85a89b0a0af9290649944426709bf31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444832"
---
# <span data-ttu-id="9d5dd-101">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9d5dd-101">Get-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="9d5dd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9d5dd-102">SYNOPSIS</span></span>
<span data-ttu-id="9d5dd-103">取得訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d5dd-103">Gets subscriptions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d5dd-104">句法</span><span class="sxs-lookup"><span data-stu-id="9d5dd-104">SYNTAX</span></span>

### <span data-ttu-id="9d5dd-105">GetAllSubscriptions (預設) </span><span class="sxs-lookup"><span data-stu-id="9d5dd-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d5dd-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9d5dd-106">GetBySubscriptionId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d5dd-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="9d5dd-107">GetByUserId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d5dd-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="9d5dd-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d5dd-109">說明</span><span class="sxs-lookup"><span data-stu-id="9d5dd-109">DESCRIPTION</span></span>
<span data-ttu-id="9d5dd-110">如果沒有指定訂閱， **AzureRmApiManagementSubscription** Cmdlet 會取得指定的訂閱或所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d5dd-110">The **Get-AzureRmApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="9d5dd-111">示例</span><span class="sxs-lookup"><span data-stu-id="9d5dd-111">EXAMPLES</span></span>

### <span data-ttu-id="9d5dd-112">範例1：取得所有訂閱</span><span class="sxs-lookup"><span data-stu-id="9d5dd-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="9d5dd-113">這個命令會取得所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d5dd-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="9d5dd-114">範例2：取得具有指定識別碼的訂閱</span><span class="sxs-lookup"><span data-stu-id="9d5dd-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="9d5dd-115">這個命令透過識別碼取得訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d5dd-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="9d5dd-116">範例3：取得使用者的所有訂閱</span><span class="sxs-lookup"><span data-stu-id="9d5dd-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="9d5dd-117">這個命令會取得使用者的訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d5dd-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="9d5dd-118">範例4：取得產品的所有訂閱</span><span class="sxs-lookup"><span data-stu-id="9d5dd-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="9d5dd-119">這個命令會取得該產品的所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d5dd-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="9d5dd-120">參數</span><span class="sxs-lookup"><span data-stu-id="9d5dd-120">PARAMETERS</span></span>

### <span data-ttu-id="9d5dd-121">-內容</span><span class="sxs-lookup"><span data-stu-id="9d5dd-121">-Context</span></span>
<span data-ttu-id="9d5dd-122">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="9d5dd-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9d5dd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d5dd-123">-DefaultProfile</span></span>
<span data-ttu-id="9d5dd-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d5dd-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="9d5dd-125">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="9d5dd-125">-ProductId</span></span>
<span data-ttu-id="9d5dd-126">指定產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="9d5dd-126">Specifies a product identifier.</span></span>
<span data-ttu-id="9d5dd-127">如果已指定，此 Cmdlet 會依產品識別碼尋找所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d5dd-127">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d5dd-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9d5dd-128">-SubscriptionId</span></span>
<span data-ttu-id="9d5dd-129">指定訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="9d5dd-129">Specifies a subscription identifier.</span></span>
<span data-ttu-id="9d5dd-130">如果已指定，此 Cmdlet 會依識別碼尋找訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d5dd-130">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetBySubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d5dd-131">-UserId</span><span class="sxs-lookup"><span data-stu-id="9d5dd-131">-UserId</span></span>
<span data-ttu-id="9d5dd-132">指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="9d5dd-132">Specifies a user identifier.</span></span>
<span data-ttu-id="9d5dd-133">如果已指定，此 Cmdlet 會依使用者識別碼尋找所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d5dd-133">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetByUserId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d5dd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d5dd-134">CommonParameters</span></span>
<span data-ttu-id="9d5dd-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9d5dd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d5dd-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9d5dd-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d5dd-137">輸入</span><span class="sxs-lookup"><span data-stu-id="9d5dd-137">INPUTS</span></span>

### <span data-ttu-id="9d5dd-138">所有</span><span class="sxs-lookup"><span data-stu-id="9d5dd-138">None</span></span>
<span data-ttu-id="9d5dd-139">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="9d5dd-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9d5dd-140">輸出</span><span class="sxs-lookup"><span data-stu-id="9d5dd-140">OUTPUTS</span></span>

### <span data-ttu-id="9d5dd-141">ServiceManagement. PsApiManagementSubscription （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="9d5dd-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>
<span data-ttu-id="9d5dd-142">API 管理服務中訂閱的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9d5dd-142">The detail of the subscription in the API Management service.</span></span>

### <span data-ttu-id="9d5dd-143">IList<ApiManagement. ServiceManagement. PsApiManagementSubscription]></span><span class="sxs-lookup"><span data-stu-id="9d5dd-143">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription></span></span>
<span data-ttu-id="9d5dd-144">[API 管理服務] 中的訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="9d5dd-144">The list of subscription in API Management service.</span></span>

## <span data-ttu-id="9d5dd-145">筆記</span><span class="sxs-lookup"><span data-stu-id="9d5dd-145">NOTES</span></span>

## <span data-ttu-id="9d5dd-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="9d5dd-146">RELATED LINKS</span></span>

[<span data-ttu-id="9d5dd-147">新-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9d5dd-147">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="9d5dd-148">移除-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9d5dd-148">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="9d5dd-149">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9d5dd-149">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


