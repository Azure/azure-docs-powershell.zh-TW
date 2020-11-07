---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azsdelegatedprovideroffer
schema: 2.0.0
ms.openlocfilehash: 118834c020a198d355d3f3b9e6dc17699f88e0cc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796413"
---
# <span data-ttu-id="123b9-101">Get-AzsDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="123b9-101">Get-AzsDelegatedProviderOffer</span></span>

## <span data-ttu-id="123b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="123b9-102">SYNOPSIS</span></span>
<span data-ttu-id="123b9-103">取得委派提供者的指定優惠。</span><span class="sxs-lookup"><span data-stu-id="123b9-103">Get the specified offer for the delegated provider.</span></span>

## <span data-ttu-id="123b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="123b9-104">SYNTAX</span></span>

### <span data-ttu-id="123b9-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="123b9-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="123b9-106">獲取</span><span class="sxs-lookup"><span data-stu-id="123b9-106">Get</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> -OfferName <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="123b9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="123b9-107">GetViaIdentity</span></span>
```
Get-AzsDelegatedProviderOffer -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="123b9-108">說明</span><span class="sxs-lookup"><span data-stu-id="123b9-108">DESCRIPTION</span></span>
<span data-ttu-id="123b9-109">取得委派提供者的指定優惠。</span><span class="sxs-lookup"><span data-stu-id="123b9-109">Get the specified offer for the delegated provider.</span></span>

## <span data-ttu-id="123b9-110">示例</span><span class="sxs-lookup"><span data-stu-id="123b9-110">EXAMPLES</span></span>

### <span data-ttu-id="123b9-111">範例1</span><span class="sxs-lookup"><span data-stu-id="123b9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDelegatedProviderOffer -DelegatedProviderId 4b763321-23f5-4a45-a44d-9ccfdd705a3d

{{ Add output here }}
```

<span data-ttu-id="123b9-112">取得指定委派提供者的優惠清單</span><span class="sxs-lookup"><span data-stu-id="123b9-112">Get the list of offers for the specified delegated provider</span></span>

## <span data-ttu-id="123b9-113">參數</span><span class="sxs-lookup"><span data-stu-id="123b9-113">PARAMETERS</span></span>

### <span data-ttu-id="123b9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="123b9-114">-DefaultProfile</span></span>
<span data-ttu-id="123b9-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="123b9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="123b9-116">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="123b9-116">-DelegatedProviderId</span></span>
<span data-ttu-id="123b9-117">委派提供者的 Id。</span><span class="sxs-lookup"><span data-stu-id="123b9-117">Id of the delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="123b9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="123b9-118">-InputObject</span></span>
<span data-ttu-id="123b9-119">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="123b9-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="123b9-120">-OfferName</span><span class="sxs-lookup"><span data-stu-id="123b9-120">-OfferName</span></span>
<span data-ttu-id="123b9-121">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="123b9-121">Name of the offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="123b9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="123b9-122">CommonParameters</span></span>
<span data-ttu-id="123b9-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="123b9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="123b9-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="123b9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="123b9-125">輸入</span><span class="sxs-lookup"><span data-stu-id="123b9-125">INPUTS</span></span>

### <span data-ttu-id="123b9-126">ISubscriptionIdentity 中的 [Azure.]</span><span class="sxs-lookup"><span data-stu-id="123b9-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="123b9-127">輸出</span><span class="sxs-lookup"><span data-stu-id="123b9-127">OUTPUTS</span></span>

### <span data-ttu-id="123b9-128">IOffer 中的 [Api20151101] （訂閱）。</span><span class="sxs-lookup"><span data-stu-id="123b9-128">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.IOffer</span></span>



## <span data-ttu-id="123b9-129">筆記</span><span class="sxs-lookup"><span data-stu-id="123b9-129">NOTES</span></span>

<span data-ttu-id="123b9-130">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="123b9-130">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="123b9-131">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="123b9-131">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="123b9-132">INPUTOBJECT <ISubscriptionIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="123b9-132">INPUTOBJECT <ISubscriptionIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="123b9-133">`[DelegatedProviderId <String>]`：委派提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="123b9-133">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="123b9-134">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="123b9-134">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="123b9-135">`[OfferName <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="123b9-135">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="123b9-136">`[SubscriptionId <String>]`：訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="123b9-136">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="123b9-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="123b9-137">RELATED LINKS</span></span>

