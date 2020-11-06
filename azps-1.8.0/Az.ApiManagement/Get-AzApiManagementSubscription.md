---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: 885d552f6040d4c88c007a37f839ac030ba671c6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611609"
---
# <span data-ttu-id="28e94-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="28e94-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="28e94-102">摘要</span><span class="sxs-lookup"><span data-stu-id="28e94-102">SYNOPSIS</span></span>
<span data-ttu-id="28e94-103">取得訂閱。</span><span class="sxs-lookup"><span data-stu-id="28e94-103">Gets subscriptions.</span></span>

## <span data-ttu-id="28e94-104">句法</span><span class="sxs-lookup"><span data-stu-id="28e94-104">SYNTAX</span></span>

### <span data-ttu-id="28e94-105">GetAllSubscriptions (預設) </span><span class="sxs-lookup"><span data-stu-id="28e94-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="28e94-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="28e94-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28e94-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="28e94-107">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28e94-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="28e94-108">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28e94-109">說明</span><span class="sxs-lookup"><span data-stu-id="28e94-109">DESCRIPTION</span></span>
<span data-ttu-id="28e94-110">如果沒有指定訂閱， **AzApiManagementSubscription** Cmdlet 會取得指定的訂閱或所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="28e94-110">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="28e94-111">示例</span><span class="sxs-lookup"><span data-stu-id="28e94-111">EXAMPLES</span></span>

### <span data-ttu-id="28e94-112">範例1：取得所有訂閱</span><span class="sxs-lookup"><span data-stu-id="28e94-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="28e94-113">這個命令會取得所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="28e94-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="28e94-114">範例2：取得具有指定識別碼的訂閱</span><span class="sxs-lookup"><span data-stu-id="28e94-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="28e94-115">這個命令透過識別碼取得訂閱。</span><span class="sxs-lookup"><span data-stu-id="28e94-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="28e94-116">範例3：取得使用者的所有訂閱</span><span class="sxs-lookup"><span data-stu-id="28e94-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="28e94-117">這個命令會取得使用者的訂閱。</span><span class="sxs-lookup"><span data-stu-id="28e94-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="28e94-118">範例4：取得產品的所有訂閱</span><span class="sxs-lookup"><span data-stu-id="28e94-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="28e94-119">這個命令會取得該產品的所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="28e94-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="28e94-120">參數</span><span class="sxs-lookup"><span data-stu-id="28e94-120">PARAMETERS</span></span>

### <span data-ttu-id="28e94-121">-內容</span><span class="sxs-lookup"><span data-stu-id="28e94-121">-Context</span></span>
<span data-ttu-id="28e94-122">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="28e94-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="28e94-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28e94-123">-DefaultProfile</span></span>
<span data-ttu-id="28e94-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="28e94-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28e94-125">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="28e94-125">-ProductId</span></span>
<span data-ttu-id="28e94-126">指定產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="28e94-126">Specifies a product identifier.</span></span>
<span data-ttu-id="28e94-127">如果已指定，此 Cmdlet 會依產品識別碼尋找所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="28e94-127">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

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

### <span data-ttu-id="28e94-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="28e94-128">-SubscriptionId</span></span>
<span data-ttu-id="28e94-129">指定訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="28e94-129">Specifies a subscription identifier.</span></span>
<span data-ttu-id="28e94-130">如果已指定，此 Cmdlet 會依識別碼尋找訂閱。</span><span class="sxs-lookup"><span data-stu-id="28e94-130">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="28e94-131">-UserId</span><span class="sxs-lookup"><span data-stu-id="28e94-131">-UserId</span></span>
<span data-ttu-id="28e94-132">指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="28e94-132">Specifies a user identifier.</span></span>
<span data-ttu-id="28e94-133">如果已指定，此 Cmdlet 會依使用者識別碼尋找所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="28e94-133">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

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

### <span data-ttu-id="28e94-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28e94-134">CommonParameters</span></span>
<span data-ttu-id="28e94-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="28e94-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28e94-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="28e94-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28e94-137">輸入</span><span class="sxs-lookup"><span data-stu-id="28e94-137">INPUTS</span></span>

### <span data-ttu-id="28e94-138">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="28e94-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="28e94-139">System.object</span><span class="sxs-lookup"><span data-stu-id="28e94-139">System.String</span></span>

## <span data-ttu-id="28e94-140">輸出</span><span class="sxs-lookup"><span data-stu-id="28e94-140">OUTPUTS</span></span>

### <span data-ttu-id="28e94-141">ServiceManagement. PsApiManagementSubscription （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="28e94-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="28e94-142">筆記</span><span class="sxs-lookup"><span data-stu-id="28e94-142">NOTES</span></span>

## <span data-ttu-id="28e94-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="28e94-143">RELATED LINKS</span></span>

[<span data-ttu-id="28e94-144">新-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="28e94-144">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="28e94-145">移除-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="28e94-145">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="28e94-146">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="28e94-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


