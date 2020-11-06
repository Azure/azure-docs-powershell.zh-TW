---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 8695d8866b83ed6cd7b29a3d94546da1114d3eb5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452908"
---
# <span data-ttu-id="1df18-101">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="1df18-101">Get-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="1df18-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1df18-102">SYNOPSIS</span></span>
<span data-ttu-id="1df18-103">取得訂閱。</span><span class="sxs-lookup"><span data-stu-id="1df18-103">Gets subscriptions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1df18-104">句法</span><span class="sxs-lookup"><span data-stu-id="1df18-104">SYNTAX</span></span>

### <span data-ttu-id="1df18-105">GetAllSubscriptions (預設) </span><span class="sxs-lookup"><span data-stu-id="1df18-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1df18-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1df18-106">GetBySubscriptionId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1df18-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="1df18-107">GetByUserId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1df18-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="1df18-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1df18-109">說明</span><span class="sxs-lookup"><span data-stu-id="1df18-109">DESCRIPTION</span></span>
<span data-ttu-id="1df18-110">如果沒有指定訂閱， **AzureRmApiManagementSubscription** Cmdlet 會取得指定的訂閱或所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="1df18-110">The **Get-AzureRmApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="1df18-111">示例</span><span class="sxs-lookup"><span data-stu-id="1df18-111">EXAMPLES</span></span>

### <span data-ttu-id="1df18-112">範例1：取得所有訂閱</span><span class="sxs-lookup"><span data-stu-id="1df18-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="1df18-113">這個命令會取得所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="1df18-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="1df18-114">範例2：取得具有指定識別碼的訂閱</span><span class="sxs-lookup"><span data-stu-id="1df18-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="1df18-115">這個命令透過識別碼取得訂閱。</span><span class="sxs-lookup"><span data-stu-id="1df18-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="1df18-116">範例3：取得使用者的所有訂閱</span><span class="sxs-lookup"><span data-stu-id="1df18-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="1df18-117">這個命令會取得使用者的訂閱。</span><span class="sxs-lookup"><span data-stu-id="1df18-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="1df18-118">範例4：取得產品的所有訂閱</span><span class="sxs-lookup"><span data-stu-id="1df18-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="1df18-119">這個命令會取得該產品的所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="1df18-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="1df18-120">參數</span><span class="sxs-lookup"><span data-stu-id="1df18-120">PARAMETERS</span></span>

### <span data-ttu-id="1df18-121">-內容</span><span class="sxs-lookup"><span data-stu-id="1df18-121">-Context</span></span>
<span data-ttu-id="1df18-122">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="1df18-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1df18-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1df18-123">-DefaultProfile</span></span>
<span data-ttu-id="1df18-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1df18-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1df18-125">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="1df18-125">-ProductId</span></span>
<span data-ttu-id="1df18-126">指定產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="1df18-126">Specifies a product identifier.</span></span>
<span data-ttu-id="1df18-127">如果已指定，此 Cmdlet 會依產品識別碼尋找所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="1df18-127">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

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

### <span data-ttu-id="1df18-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1df18-128">-SubscriptionId</span></span>
<span data-ttu-id="1df18-129">指定訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="1df18-129">Specifies a subscription identifier.</span></span>
<span data-ttu-id="1df18-130">如果已指定，此 Cmdlet 會依識別碼尋找訂閱。</span><span class="sxs-lookup"><span data-stu-id="1df18-130">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="1df18-131">-UserId</span><span class="sxs-lookup"><span data-stu-id="1df18-131">-UserId</span></span>
<span data-ttu-id="1df18-132">指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="1df18-132">Specifies a user identifier.</span></span>
<span data-ttu-id="1df18-133">如果已指定，此 Cmdlet 會依使用者識別碼尋找所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="1df18-133">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

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

### <span data-ttu-id="1df18-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1df18-134">CommonParameters</span></span>
<span data-ttu-id="1df18-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1df18-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1df18-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1df18-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1df18-137">輸入</span><span class="sxs-lookup"><span data-stu-id="1df18-137">INPUTS</span></span>

### <span data-ttu-id="1df18-138">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="1df18-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1df18-139">System.object</span><span class="sxs-lookup"><span data-stu-id="1df18-139">System.String</span></span>

## <span data-ttu-id="1df18-140">輸出</span><span class="sxs-lookup"><span data-stu-id="1df18-140">OUTPUTS</span></span>

### <span data-ttu-id="1df18-141">ServiceManagement. PsApiManagementSubscription （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="1df18-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="1df18-142">筆記</span><span class="sxs-lookup"><span data-stu-id="1df18-142">NOTES</span></span>

## <span data-ttu-id="1df18-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="1df18-143">RELATED LINKS</span></span>

[<span data-ttu-id="1df18-144">新-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="1df18-144">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="1df18-145">移除-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="1df18-145">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="1df18-146">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="1df18-146">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


