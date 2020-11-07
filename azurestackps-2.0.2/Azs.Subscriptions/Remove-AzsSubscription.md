---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/remove-azssubscription
schema: 2.0.0
ms.openlocfilehash: b6fddf677cd619dad577b7bca8286671b85d0791
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968467"
---
# <span data-ttu-id="b1016-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="b1016-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="b1016-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b1016-102">SYNOPSIS</span></span>


## <span data-ttu-id="b1016-103">句法</span><span class="sxs-lookup"><span data-stu-id="b1016-103">SYNTAX</span></span>

### <span data-ttu-id="b1016-104">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="b1016-104">Delete (Default)</span></span>
```
Remove-AzsSubscription -SubscriptionId <String> [-DefaultProfile <PSObject>] [-Force] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b1016-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b1016-105">DeleteViaIdentity</span></span>
```
Remove-AzsSubscription -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>] [-Force] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b1016-106">說明</span><span class="sxs-lookup"><span data-stu-id="b1016-106">DESCRIPTION</span></span>


## <span data-ttu-id="b1016-107">示例</span><span class="sxs-lookup"><span data-stu-id="b1016-107">EXAMPLES</span></span>

### <span data-ttu-id="b1016-108">範例1</span><span class="sxs-lookup"><span data-stu-id="b1016-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9

```

<span data-ttu-id="b1016-109">刪除指定的訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1016-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="b1016-110">參數</span><span class="sxs-lookup"><span data-stu-id="b1016-110">PARAMETERS</span></span>

### <span data-ttu-id="b1016-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1016-111">-DefaultProfile</span></span>


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

### <span data-ttu-id="b1016-112">-Force</span><span class="sxs-lookup"><span data-stu-id="b1016-112">-Force</span></span>


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

### <span data-ttu-id="b1016-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1016-113">-InputObject</span></span>
<span data-ttu-id="b1016-114">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b1016-114">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="b1016-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1016-115">-PassThru</span></span>


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

### <span data-ttu-id="b1016-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b1016-116">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b1016-117">-確認</span><span class="sxs-lookup"><span data-stu-id="b1016-117">-Confirm</span></span>
<span data-ttu-id="b1016-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b1016-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1016-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1016-119">-WhatIf</span></span>
<span data-ttu-id="b1016-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b1016-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1016-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1016-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1016-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1016-122">CommonParameters</span></span>
<span data-ttu-id="b1016-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b1016-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1016-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b1016-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1016-125">輸入</span><span class="sxs-lookup"><span data-stu-id="b1016-125">INPUTS</span></span>

### <span data-ttu-id="b1016-126">ISubscriptionIdentity 中的 [Azure.]</span><span class="sxs-lookup"><span data-stu-id="b1016-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="b1016-127">輸出</span><span class="sxs-lookup"><span data-stu-id="b1016-127">OUTPUTS</span></span>

### <span data-ttu-id="b1016-128">System.object</span><span class="sxs-lookup"><span data-stu-id="b1016-128">System.Boolean</span></span>



## <span data-ttu-id="b1016-129">筆記</span><span class="sxs-lookup"><span data-stu-id="b1016-129">NOTES</span></span>

<span data-ttu-id="b1016-130">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="b1016-130">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b1016-131">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b1016-131">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b1016-132">INPUTOBJECT <ISubscriptionIdentity> ：</span><span class="sxs-lookup"><span data-stu-id="b1016-132">INPUTOBJECT <ISubscriptionIdentity>:</span></span> 
  - <span data-ttu-id="b1016-133">`[DelegatedProviderId <String>]`：委派提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b1016-133">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="b1016-134">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="b1016-134">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b1016-135">`[OfferName <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1016-135">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="b1016-136">`[SubscriptionId <String>]`：訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b1016-136">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="b1016-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1016-137">RELATED LINKS</span></span>

