---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzSubscription.md
ms.openlocfilehash: f2d080373bef1abda3ea5af91076b024261d3eeb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902682"
---
# <span data-ttu-id="11182-101">Get-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="11182-101">Get-AzSubscription</span></span>

## <span data-ttu-id="11182-102">簡介</span><span class="sxs-lookup"><span data-stu-id="11182-102">SYNOPSIS</span></span>
<span data-ttu-id="11182-103">取得目前帳戶可存取的訂閱。</span><span class="sxs-lookup"><span data-stu-id="11182-103">Get subscriptions that the current account can access.</span></span>

## <span data-ttu-id="11182-104">語法</span><span class="sxs-lookup"><span data-stu-id="11182-104">SYNTAX</span></span>

### <span data-ttu-id="11182-105">ListByIdInTenant (預設) </span><span class="sxs-lookup"><span data-stu-id="11182-105">ListByIdInTenant (Default)</span></span>
```
Get-AzSubscription [-SubscriptionId <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11182-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="11182-106">ListByNameInTenant</span></span>
```
Get-AzSubscription [-SubscriptionName <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11182-107">描述</span><span class="sxs-lookup"><span data-stu-id="11182-107">DESCRIPTION</span></span>
<span data-ttu-id="11182-108">Cmdlet Get-AzSubscription取得目前帳戶可存取之訂閱的訂閱識別碼、訂閱名稱和家用租使用者。</span><span class="sxs-lookup"><span data-stu-id="11182-108">The Get-AzSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="11182-109">例子</span><span class="sxs-lookup"><span data-stu-id="11182-109">EXAMPLES</span></span>

### <span data-ttu-id="11182-110">範例 1：取得所有租使用者的所有訂閱</span><span class="sxs-lookup"><span data-stu-id="11182-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription3                      zzzz-zzzz-zzzz-zzzz     bbbb-bbbb-bbbb-bbbb             Enabled
```

<span data-ttu-id="11182-111">此命令會在所有租使用者中，獲得目前帳戶授權的所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="11182-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="11182-112">範例 2：取得特定租使用者的所有訂閱</span><span class="sxs-lookup"><span data-stu-id="11182-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzSubscription -TenantId "aaaa-aaaa-aaaa-aaaa"

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="11182-113">列出獲授權目前帳戶之租使用者內的所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="11182-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="11182-114">範例 3：取得目前租使用者的所有訂閱</span><span class="sxs-lookup"><span data-stu-id="11182-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="11182-115">此命令會獲得目前租使用者中已授權目前使用者的所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="11182-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="11182-116">範例 4：將目前內容變更為使用特定訂閱</span><span class="sxs-lookup"><span data-stu-id="11182-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxx-xxxx-xxxx-xxxx)      azureuser@micros... Subscription1       AzureCloud          yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="11182-117">此命令會獲得指定的訂閱，然後設定目前的上下文來使用它。</span><span class="sxs-lookup"><span data-stu-id="11182-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="11182-118">此會話的所有後續 Cmdlet 預設 (Contoso 訂閱 1) 訂閱。</span><span class="sxs-lookup"><span data-stu-id="11182-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="11182-119">參數</span><span class="sxs-lookup"><span data-stu-id="11182-119">PARAMETERS</span></span>

### <span data-ttu-id="11182-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11182-120">-AsJob</span></span>
<span data-ttu-id="11182-121">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="11182-121">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11182-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11182-122">-DefaultProfile</span></span>
<span data-ttu-id="11182-123">用於與 Azure 通訊的認證、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="11182-123">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11182-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="11182-124">-SubscriptionId</span></span>
<span data-ttu-id="11182-125">指定要取得之訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="11182-125">Specifies the ID of the subscription to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByIdInTenant
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11182-126">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="11182-126">-SubscriptionName</span></span>
<span data-ttu-id="11182-127">指定要取得之訂閱的名稱。</span><span class="sxs-lookup"><span data-stu-id="11182-127">Specifies the name of the subscription to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByNameInTenant
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11182-128">-TenantId</span><span class="sxs-lookup"><span data-stu-id="11182-128">-TenantId</span></span>
<span data-ttu-id="11182-129">指定包含要取得之訂閱的租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="11182-129">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

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

### <span data-ttu-id="11182-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11182-130">CommonParameters</span></span>
<span data-ttu-id="11182-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="11182-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11182-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11182-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11182-133">輸入</span><span class="sxs-lookup"><span data-stu-id="11182-133">INPUTS</span></span>

### <span data-ttu-id="11182-134">System.String</span><span class="sxs-lookup"><span data-stu-id="11182-134">System.String</span></span>

## <span data-ttu-id="11182-135">輸出</span><span class="sxs-lookup"><span data-stu-id="11182-135">OUTPUTS</span></span>

### <span data-ttu-id="11182-136">Microsoft.Azure.Commands.Profile.models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="11182-136">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="11182-137">筆記</span><span class="sxs-lookup"><span data-stu-id="11182-137">NOTES</span></span>

## <span data-ttu-id="11182-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="11182-138">RELATED LINKS</span></span>
