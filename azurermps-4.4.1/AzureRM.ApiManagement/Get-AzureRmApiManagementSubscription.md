---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 173a8a7ab41b044d2a9442a9345ec59ab80329ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454976"
---
# <span data-ttu-id="445e4-101">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="445e4-101">Get-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="445e4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="445e4-102">SYNOPSIS</span></span>
<span data-ttu-id="445e4-103">取得訂閱。</span><span class="sxs-lookup"><span data-stu-id="445e4-103">Gets subscriptions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="445e4-104">句法</span><span class="sxs-lookup"><span data-stu-id="445e4-104">SYNTAX</span></span>

### <span data-ttu-id="445e4-105">取得所有訂閱 (預設) </span><span class="sxs-lookup"><span data-stu-id="445e4-105">Get all subscriptions (Default)</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="445e4-106">透過 subsctiption 識別碼取得</span><span class="sxs-lookup"><span data-stu-id="445e4-106">Get by subsctiption ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="445e4-107">透過使用者識別碼取得</span><span class="sxs-lookup"><span data-stu-id="445e4-107">Get by user ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="445e4-108">依產品識別碼取得</span><span class="sxs-lookup"><span data-stu-id="445e4-108">Get by product ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="445e4-109">說明</span><span class="sxs-lookup"><span data-stu-id="445e4-109">DESCRIPTION</span></span>
<span data-ttu-id="445e4-110">如果沒有指定訂閱， **AzureRmApiManagementSubscription** Cmdlet 會取得指定的訂閱或所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="445e4-110">The **Get-AzureRmApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="445e4-111">示例</span><span class="sxs-lookup"><span data-stu-id="445e4-111">EXAMPLES</span></span>

### <span data-ttu-id="445e4-112">範例1：取得所有訂閱</span><span class="sxs-lookup"><span data-stu-id="445e4-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="445e4-113">這個命令會取得所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="445e4-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="445e4-114">範例2：取得具有指定識別碼的訂閱</span><span class="sxs-lookup"><span data-stu-id="445e4-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="445e4-115">這個命令透過識別碼取得訂閱。</span><span class="sxs-lookup"><span data-stu-id="445e4-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="445e4-116">範例3：取得使用者的所有訂閱</span><span class="sxs-lookup"><span data-stu-id="445e4-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="445e4-117">這個命令會取得使用者的訂閱。</span><span class="sxs-lookup"><span data-stu-id="445e4-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="445e4-118">範例4：取得產品的所有訂閱</span><span class="sxs-lookup"><span data-stu-id="445e4-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="445e4-119">這個命令會取得該產品的所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="445e4-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="445e4-120">參數</span><span class="sxs-lookup"><span data-stu-id="445e4-120">PARAMETERS</span></span>

### <span data-ttu-id="445e4-121">-內容</span><span class="sxs-lookup"><span data-stu-id="445e4-121">-Context</span></span>
<span data-ttu-id="445e4-122">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="445e4-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="445e4-123">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="445e4-123">-ProductId</span></span>
<span data-ttu-id="445e4-124">指定產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="445e4-124">Specifies a product identifier.</span></span>
<span data-ttu-id="445e4-125">如果已指定，此 Cmdlet 會依產品識別碼尋找所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="445e4-125">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by product ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="445e4-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="445e4-126">-SubscriptionId</span></span>
<span data-ttu-id="445e4-127">指定訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="445e4-127">Specifies a subscription identifier.</span></span>
<span data-ttu-id="445e4-128">如果已指定，此 Cmdlet 會依識別碼尋找訂閱。</span><span class="sxs-lookup"><span data-stu-id="445e4-128">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by subsctiption ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="445e4-129">-UserId</span><span class="sxs-lookup"><span data-stu-id="445e4-129">-UserId</span></span>
<span data-ttu-id="445e4-130">指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="445e4-130">Specifies a user identifier.</span></span>
<span data-ttu-id="445e4-131">如果已指定，此 Cmdlet 會依使用者識別碼尋找所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="445e4-131">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by user ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="445e4-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="445e4-132">-DefaultProfile</span></span>
<span data-ttu-id="445e4-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="445e4-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="445e4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="445e4-134">CommonParameters</span></span>
<span data-ttu-id="445e4-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="445e4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="445e4-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="445e4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="445e4-137">輸入</span><span class="sxs-lookup"><span data-stu-id="445e4-137">INPUTS</span></span>

## <span data-ttu-id="445e4-138">輸出</span><span class="sxs-lookup"><span data-stu-id="445e4-138">OUTPUTS</span></span>

### <span data-ttu-id="445e4-139">IList<ApiManagement. ServiceManagement. PsApiManagementSubscription]></span><span class="sxs-lookup"><span data-stu-id="445e4-139">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription></span></span>

## <span data-ttu-id="445e4-140">筆記</span><span class="sxs-lookup"><span data-stu-id="445e4-140">NOTES</span></span>

## <span data-ttu-id="445e4-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="445e4-141">RELATED LINKS</span></span>

[<span data-ttu-id="445e4-142">新-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="445e4-142">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="445e4-143">移除-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="445e4-143">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="445e4-144">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="445e4-144">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


