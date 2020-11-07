---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: 59afc363d040724bbd525afc6e1f599a995cfdcb
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966782"
---
# <span data-ttu-id="90ac6-101">Set-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="90ac6-101">Set-AzsOfferDelegation</span></span>

## <span data-ttu-id="90ac6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="90ac6-102">SYNOPSIS</span></span>
<span data-ttu-id="90ac6-103">建立或更新 [優惠委派]。</span><span class="sxs-lookup"><span data-stu-id="90ac6-103">Create or update the offer delegation.</span></span>

## <span data-ttu-id="90ac6-104">句法</span><span class="sxs-lookup"><span data-stu-id="90ac6-104">SYNTAX</span></span>

### <span data-ttu-id="90ac6-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="90ac6-105">UpdateExpanded (Default)</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-PropertiesSubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="90ac6-106">時更新</span><span class="sxs-lookup"><span data-stu-id="90ac6-106">Update</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 -OfferDelegationDefinition <IOfferDelegation> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="90ac6-107">說明</span><span class="sxs-lookup"><span data-stu-id="90ac6-107">DESCRIPTION</span></span>
<span data-ttu-id="90ac6-108">建立或更新 [優惠委派]。</span><span class="sxs-lookup"><span data-stu-id="90ac6-108">Create or update the offer delegation.</span></span>

## <span data-ttu-id="90ac6-109">示例</span><span class="sxs-lookup"><span data-stu-id="90ac6-109">EXAMPLES</span></span>

### <span data-ttu-id="90ac6-110">範例1</span><span class="sxs-lookup"><span data-stu-id="90ac6-110">Example 1</span></span>
```powershell
PS C:\> Set-AzsOfferDelegation -Offer offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946" -Location "local"

{{ Add output here }}
```

<span data-ttu-id="90ac6-111">更新 [提供委派]。</span><span class="sxs-lookup"><span data-stu-id="90ac6-111">Updates the offer delegation.</span></span>

## <span data-ttu-id="90ac6-112">參數</span><span class="sxs-lookup"><span data-stu-id="90ac6-112">PARAMETERS</span></span>

### <span data-ttu-id="90ac6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90ac6-113">-DefaultProfile</span></span>
<span data-ttu-id="90ac6-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="90ac6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90ac6-115">-位置</span><span class="sxs-lookup"><span data-stu-id="90ac6-115">-Location</span></span>
<span data-ttu-id="90ac6-116">資源的位置</span><span class="sxs-lookup"><span data-stu-id="90ac6-116">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="90ac6-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="90ac6-117">-Name</span></span>
<span data-ttu-id="90ac6-118">優惠委派的名稱。</span><span class="sxs-lookup"><span data-stu-id="90ac6-118">Name of a offer delegation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="90ac6-119">-OfferDelegationDefinition</span><span class="sxs-lookup"><span data-stu-id="90ac6-119">-OfferDelegationDefinition</span></span>
<span data-ttu-id="90ac6-120">提供委派。</span><span class="sxs-lookup"><span data-stu-id="90ac6-120">Offer delegation.</span></span>
<span data-ttu-id="90ac6-121">若要建立，請參閱 OFFERDELEGATIONDEFINITION 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="90ac6-121">To construct, see NOTES section for OFFERDELEGATIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="90ac6-122">-OfferName</span><span class="sxs-lookup"><span data-stu-id="90ac6-122">-OfferName</span></span>
<span data-ttu-id="90ac6-123">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="90ac6-123">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="90ac6-124">-PropertiesSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="90ac6-124">-PropertiesSubscriptionId</span></span>
<span data-ttu-id="90ac6-125">接收委派優惠之訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="90ac6-125">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="90ac6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90ac6-126">-ResourceGroupName</span></span>
<span data-ttu-id="90ac6-127">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="90ac6-127">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="90ac6-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="90ac6-128">-SubscriptionId</span></span>
<span data-ttu-id="90ac6-129">可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="90ac6-129">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="90ac6-130">-確認</span><span class="sxs-lookup"><span data-stu-id="90ac6-130">-Confirm</span></span>
<span data-ttu-id="90ac6-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="90ac6-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="90ac6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90ac6-132">-WhatIf</span></span>
<span data-ttu-id="90ac6-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="90ac6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90ac6-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90ac6-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="90ac6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90ac6-135">CommonParameters</span></span>
<span data-ttu-id="90ac6-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="90ac6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90ac6-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="90ac6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90ac6-138">輸入</span><span class="sxs-lookup"><span data-stu-id="90ac6-138">INPUTS</span></span>

### <span data-ttu-id="90ac6-139">IOfferDelegation （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="90ac6-139">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

## <span data-ttu-id="90ac6-140">輸出</span><span class="sxs-lookup"><span data-stu-id="90ac6-140">OUTPUTS</span></span>

### <span data-ttu-id="90ac6-141">IOfferDelegation （SubscriptionsAdmin）。 Api20151101。</span><span class="sxs-lookup"><span data-stu-id="90ac6-141">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

<span data-ttu-id="90ac6-142">別名</span><span class="sxs-lookup"><span data-stu-id="90ac6-142">ALIASES</span></span>

## <span data-ttu-id="90ac6-143">筆記</span><span class="sxs-lookup"><span data-stu-id="90ac6-143">NOTES</span></span>

<span data-ttu-id="90ac6-144">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="90ac6-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="90ac6-145">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="90ac6-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="90ac6-146">OFFERDELEGATIONDEFINITION <IOfferDelegation> ：提供委派。</span><span class="sxs-lookup"><span data-stu-id="90ac6-146">OFFERDELEGATIONDEFINITION <IOfferDelegation>: Offer delegation.</span></span>
  - <span data-ttu-id="90ac6-147">`[Location <String>]`：資源的位置</span><span class="sxs-lookup"><span data-stu-id="90ac6-147">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="90ac6-148">`[SubscriptionId <String>]`：接收委派優惠之訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="90ac6-148">`[SubscriptionId <String>]`: Identifier of the subscription receiving the delegated offer.</span></span>

## <span data-ttu-id="90ac6-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="90ac6-149">RELATED LINKS</span></span>

