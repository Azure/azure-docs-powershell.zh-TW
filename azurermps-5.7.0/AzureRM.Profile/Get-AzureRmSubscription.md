---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
ms.openlocfilehash: 09d51ccf8d4ebdc387977d480be606bf9ed9d9df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454184"
---
# <span data-ttu-id="e23a4-101">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="e23a4-101">Get-AzureRmSubscription</span></span>

## <span data-ttu-id="e23a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e23a4-102">SYNOPSIS</span></span>
<span data-ttu-id="e23a4-103">取得目前帳戶可以存取的訂閱。</span><span class="sxs-lookup"><span data-stu-id="e23a4-103">Get subscriptions that the current account can access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e23a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="e23a4-104">SYNTAX</span></span>

### <span data-ttu-id="e23a4-105">ListByIdInTenant (預設) </span><span class="sxs-lookup"><span data-stu-id="e23a4-105">ListByIdInTenant (Default)</span></span>
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e23a4-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="e23a4-106">ListByNameInTenant</span></span>
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e23a4-107">說明</span><span class="sxs-lookup"><span data-stu-id="e23a4-107">DESCRIPTION</span></span>
<span data-ttu-id="e23a4-108">Get-AzureRmSubscription Cmdlet 會取得目前帳戶可存取之訂閱的訂閱識別碼、訂閱名稱及家用租使用者。</span><span class="sxs-lookup"><span data-stu-id="e23a4-108">The Get-AzureRmSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="e23a4-109">示例</span><span class="sxs-lookup"><span data-stu-id="e23a4-109">EXAMPLES</span></span>

### <span data-ttu-id="e23a4-110">範例1：取得所有承租人中的所有訂閱</span><span class="sxs-lookup"><span data-stu-id="e23a4-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzureRmSubscription

Name     : Contoso Subscription 1
Id       : xxxx-xxxx-xxxx-xxxx
TenantId : yyyy-yyyy-yyyy-yyyy
State    : Enabled
```

<span data-ttu-id="e23a4-111">這個命令會取得所有針對目前帳戶授權的租使用者的訂閱。</span><span class="sxs-lookup"><span data-stu-id="e23a4-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="e23a4-112">範例2：取得特定租使用者的所有訂閱</span><span class="sxs-lookup"><span data-stu-id="e23a4-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Name     : Contoso Subscription 1
Id       : yyyy-yyyy-yyyy-yyyy
TenantId : xxxx-xxxx-xxxx-xxxx
State    : Enabled

Name     : Contoso Subscription 2
Id       : yyyy-yyyy-yyyy-yyyy
TenantId : xxxx-xxxx-xxxx-xxxx
State    : Enabled
```

<span data-ttu-id="e23a4-113">列出已針對目前帳戶授權的指定租使用者中的所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="e23a4-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="e23a4-114">範例3：取得目前租使用者中的所有訂閱</span><span class="sxs-lookup"><span data-stu-id="e23a4-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzureRmSubscription

Name     : Contoso Subscription 1
Id       : yyyy-yyyy-yyyy-yyyy
TenantId : xxxx-xxxx-xxxx-xxxx
State    : Enabled

Name     : Contoso Subscription 2
Id       : yyyy-yyyy-yyyy-yyyy
TenantId : xxxx-xxxx-xxxx-xxxx
State    : Enabled
```

<span data-ttu-id="e23a4-115">這個命令會在目前的租使用者中取得目前已授權的所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="e23a4-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="e23a4-116">範例4：變更目前的內容以使用特定的訂閱</span><span class="sxs-lookup"><span data-stu-id="e23a4-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Environment           : AzureCloud
Account               : user@example.com
TenantId              : yyyy-yyyy-yyyy-yyyy
SubscriptionId        : xxxx-xxxx-xxxx-xxxx
SubscriptionName      : Contoso Subscription 1
CurrentStorageAccount :
```

<span data-ttu-id="e23a4-117">這個命令會取得指定的訂閱，然後設定目前的內容來使用它。</span><span class="sxs-lookup"><span data-stu-id="e23a4-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="e23a4-118">此會話中的所有後續 Cmdlet 都會預設使用 (Contoso 訂閱 1) 的新訂閱。</span><span class="sxs-lookup"><span data-stu-id="e23a4-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="e23a4-119">參數</span><span class="sxs-lookup"><span data-stu-id="e23a4-119">PARAMETERS</span></span>

### <span data-ttu-id="e23a4-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e23a4-120">-AsJob</span></span>
<span data-ttu-id="e23a4-121">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="e23a4-121">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e23a4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e23a4-122">-DefaultProfile</span></span>
<span data-ttu-id="e23a4-123">用於與 azure 進行通訊的認證、租使用者與訂閱</span><span class="sxs-lookup"><span data-stu-id="e23a4-123">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e23a4-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e23a4-124">-SubscriptionId</span></span>
<span data-ttu-id="e23a4-125">指定要取得的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="e23a4-125">Specifies the ID of the subscription to get.</span></span>

```yaml
Type: String
Parameter Sets: ListByIdInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e23a4-126">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="e23a4-126">-SubscriptionName</span></span>
<span data-ttu-id="e23a4-127">指定要取得的訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="e23a4-127">Specifies the name of the subscription to get.</span></span>

```yaml
Type: String
Parameter Sets: ListByNameInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e23a4-128">-TenantId</span><span class="sxs-lookup"><span data-stu-id="e23a4-128">-TenantId</span></span>
<span data-ttu-id="e23a4-129">指定包含要取得之訂閱的租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="e23a4-129">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e23a4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e23a4-130">CommonParameters</span></span>
<span data-ttu-id="e23a4-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e23a4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e23a4-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e23a4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e23a4-133">輸入</span><span class="sxs-lookup"><span data-stu-id="e23a4-133">INPUTS</span></span>

### <span data-ttu-id="e23a4-134">所有</span><span class="sxs-lookup"><span data-stu-id="e23a4-134">None</span></span>
<span data-ttu-id="e23a4-135">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="e23a4-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e23a4-136">輸出</span><span class="sxs-lookup"><span data-stu-id="e23a4-136">OUTPUTS</span></span>

### <span data-ttu-id="e23a4-137">PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="e23a4-137">PSAzureSubscription</span></span>

## <span data-ttu-id="e23a4-138">筆記</span><span class="sxs-lookup"><span data-stu-id="e23a4-138">NOTES</span></span>

## <span data-ttu-id="e23a4-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="e23a4-139">RELATED LINKS</span></span>

