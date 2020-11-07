---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azssubscription
schema: 2.0.0
ms.openlocfilehash: 7dce95be9a936d341e0f063fd6d89701b18c2ce7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968472"
---
# <span data-ttu-id="61b2e-101">Get-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="61b2e-101">Get-AzsSubscription</span></span>

## <span data-ttu-id="61b2e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="61b2e-102">SYNOPSIS</span></span>
<span data-ttu-id="61b2e-103">取得特定訂閱的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="61b2e-103">Gets details about particular subscription.</span></span>

## <span data-ttu-id="61b2e-104">句法</span><span class="sxs-lookup"><span data-stu-id="61b2e-104">SYNTAX</span></span>

### <span data-ttu-id="61b2e-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="61b2e-105">List (Default)</span></span>
```
Get-AzsSubscription [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="61b2e-106">獲取</span><span class="sxs-lookup"><span data-stu-id="61b2e-106">Get</span></span>
```
Get-AzsSubscription -SubscriptionId <String[]> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="61b2e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="61b2e-107">GetViaIdentity</span></span>
```
Get-AzsSubscription -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="61b2e-108">說明</span><span class="sxs-lookup"><span data-stu-id="61b2e-108">DESCRIPTION</span></span>
<span data-ttu-id="61b2e-109">取得特定訂閱的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="61b2e-109">Gets details about particular subscription.</span></span>

## <span data-ttu-id="61b2e-110">示例</span><span class="sxs-lookup"><span data-stu-id="61b2e-110">EXAMPLES</span></span>

### <span data-ttu-id="61b2e-111">範例1</span><span class="sxs-lookup"><span data-stu-id="61b2e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsSubscription | fl *

DisplayName    : Test User
Id             : /subscriptions/97d84f7a-bef7-4f2d-b651-c553be472311
OfferId        : /delegatedProviders/default/offers/TestOffer-590376ac-c8dd-4b3d-9674-b5b8fcde095b
State          : Enabled
SubscriptionId : 97d84f7a-bef7-4f2d-b651-c553be472311
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb

DisplayName    : cnur
Id             : /subscriptions/ed3e275b-87d1-4e94-9962-b3700287bdbc
OfferId        : /delegatedProviders/default/offers/cnur4866tenantsubsvcoffer843
State          : Enabled
SubscriptionId : ed3e275b-87d1-4e94-9962-b3700287bdbc
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="61b2e-112">取得訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="61b2e-112">Get the list of subscriptions.</span></span>

## <span data-ttu-id="61b2e-113">參數</span><span class="sxs-lookup"><span data-stu-id="61b2e-113">PARAMETERS</span></span>

### <span data-ttu-id="61b2e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61b2e-114">-DefaultProfile</span></span>
<span data-ttu-id="61b2e-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="61b2e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="61b2e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61b2e-116">-InputObject</span></span>
<span data-ttu-id="61b2e-117">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="61b2e-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="61b2e-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="61b2e-118">-SubscriptionId</span></span>
<span data-ttu-id="61b2e-119">訂閱的 Id。</span><span class="sxs-lookup"><span data-stu-id="61b2e-119">Id of the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="61b2e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61b2e-120">CommonParameters</span></span>
<span data-ttu-id="61b2e-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="61b2e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61b2e-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="61b2e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61b2e-123">輸入</span><span class="sxs-lookup"><span data-stu-id="61b2e-123">INPUTS</span></span>

### <span data-ttu-id="61b2e-124">ISubscriptionIdentity 中的 [Azure.]</span><span class="sxs-lookup"><span data-stu-id="61b2e-124">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="61b2e-125">輸出</span><span class="sxs-lookup"><span data-stu-id="61b2e-125">OUTPUTS</span></span>

### <span data-ttu-id="61b2e-126">ISubscription 中的 [Api20151101] （訂閱）。</span><span class="sxs-lookup"><span data-stu-id="61b2e-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="61b2e-127">筆記</span><span class="sxs-lookup"><span data-stu-id="61b2e-127">NOTES</span></span>

<span data-ttu-id="61b2e-128">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="61b2e-128">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="61b2e-129">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="61b2e-129">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="61b2e-130">INPUTOBJECT <ISubscriptionIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="61b2e-130">INPUTOBJECT <ISubscriptionIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="61b2e-131">`[DelegatedProviderId <String>]`：委派提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="61b2e-131">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="61b2e-132">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="61b2e-132">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="61b2e-133">`[OfferName <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="61b2e-133">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="61b2e-134">`[SubscriptionId <String>]`：訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="61b2e-134">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="61b2e-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="61b2e-135">RELATED LINKS</span></span>

