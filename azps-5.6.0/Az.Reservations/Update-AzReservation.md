---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/update-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
ms.openlocfilehash: b93dd1462bb019b12fe761e0bdd6cc4172c01b89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914498"
---
# <span data-ttu-id="9427b-101">Update-AzReservation</span><span class="sxs-lookup"><span data-stu-id="9427b-101">Update-AzReservation</span></span>

## <span data-ttu-id="9427b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9427b-102">SYNOPSIS</span></span>
<span data-ttu-id="9427b-103">更新 `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="9427b-103">Update a `Reservation`.</span></span>

## <span data-ttu-id="9427b-104">語法</span><span class="sxs-lookup"><span data-stu-id="9427b-104">SYNTAX</span></span>

### <span data-ttu-id="9427b-105">CommandLine (預設) </span><span class="sxs-lookup"><span data-stu-id="9427b-105">CommandLine (Default)</span></span>
```
Update-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -AppliedScopeType <String>
 [-AppliedScope <String>] [-InstanceFlexibility <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9427b-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="9427b-106">PipeObject</span></span>
```
Update-AzReservation -AppliedScopeType <String> [-AppliedScope <String>] [-InstanceFlexibility <String>]
 -Reservation <PSReservation> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9427b-107">描述</span><span class="sxs-lookup"><span data-stu-id="9427b-107">DESCRIPTION</span></span>
<span data-ttu-id="9427b-108">更新的已使用範圍 `Reservation` 。</span><span class="sxs-lookup"><span data-stu-id="9427b-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="9427b-109">例子</span><span class="sxs-lookup"><span data-stu-id="9427b-109">EXAMPLES</span></span>

### <span data-ttu-id="9427b-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="9427b-110">Example 1</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff" -InstanceFlexibility "On"
```

<span data-ttu-id="9427b-111">將指定為單一和 `Reservation` InstanceFlexibility 的 AppliedScopeType 更新為 On。</span><span class="sxs-lookup"><span data-stu-id="9427b-111">Updates the AppliedScopeType of the specified `Reservation` to Single and InstanceFlexibility to On.</span></span>

### <span data-ttu-id="9427b-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="9427b-112">Example 2</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared" -InstanceFlexibility "Off"
```

<span data-ttu-id="9427b-113">將指定給 Shared 和 `Reservation` InstanceFlexibility 的 AppliedScopeType 更新為 Off。</span><span class="sxs-lookup"><span data-stu-id="9427b-113">Updates the AppliedScopeType of the specified `Reservation` to Shared and InstanceFlexibility to Off.</span></span>

## <span data-ttu-id="9427b-114">參數</span><span class="sxs-lookup"><span data-stu-id="9427b-114">PARAMETERS</span></span>

### <span data-ttu-id="9427b-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="9427b-115">-AppliedScope</span></span>
<span data-ttu-id="9427b-116">要針對此 `Reservation` 進行申請的 SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9427b-116">SubscriptionId for this `Reservation` to be applied</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9427b-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="9427b-117">-AppliedScopeType</span></span>
<span data-ttu-id="9427b-118">已使用範圍的類型</span><span class="sxs-lookup"><span data-stu-id="9427b-118">Type of the Applied Scope</span></span>

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

### <span data-ttu-id="9427b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9427b-119">-DefaultProfile</span></span>
<span data-ttu-id="9427b-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9427b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9427b-121">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="9427b-121">-InstanceFlexibility</span></span>
<span data-ttu-id="9427b-122">如果有，請更新的 InstanceFlexibility 值 `Reservation` 。</span><span class="sxs-lookup"><span data-stu-id="9427b-122">If present, updates the InstanceFlexibility value of the `Reservation`.</span></span> <span data-ttu-id="9427b-123">如果未指定，現有值會維持不變。</span><span class="sxs-lookup"><span data-stu-id="9427b-123">If not specified, the existing value remains unchanged.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9427b-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="9427b-124">-Name</span></span>
<span data-ttu-id="9427b-125">預約名稱</span><span class="sxs-lookup"><span data-stu-id="9427b-125">Name of Reservation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9427b-126">-預約</span><span class="sxs-lookup"><span data-stu-id="9427b-126">-Reservation</span></span>
<span data-ttu-id="9427b-127">的管道物件參數 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="9427b-127">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9427b-128">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="9427b-128">-ReservationId</span></span>
<span data-ttu-id="9427b-129">要更新 `Reservation` 的識別碼</span><span class="sxs-lookup"><span data-stu-id="9427b-129">Id of the `Reservation` to update</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9427b-130">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="9427b-130">-ReservationOrderId</span></span>
<span data-ttu-id="9427b-131">要更新 `ReservationOrder` 的識別碼</span><span class="sxs-lookup"><span data-stu-id="9427b-131">Id of the `ReservationOrder` to update</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9427b-132">-確認</span><span class="sxs-lookup"><span data-stu-id="9427b-132">-Confirm</span></span>
<span data-ttu-id="9427b-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9427b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9427b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9427b-134">-WhatIf</span></span>
<span data-ttu-id="9427b-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9427b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9427b-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9427b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9427b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9427b-137">CommonParameters</span></span>
<span data-ttu-id="9427b-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9427b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9427b-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9427b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9427b-140">輸入</span><span class="sxs-lookup"><span data-stu-id="9427b-140">INPUTS</span></span>

### <span data-ttu-id="9427b-141">Microsoft.Azure.Commands.Reservations.models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="9427b-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="9427b-142">輸出</span><span class="sxs-lookup"><span data-stu-id="9427b-142">OUTPUTS</span></span>

### <span data-ttu-id="9427b-143">Microsoft.Azure.Commands.Reservations.models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="9427b-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="9427b-144">筆記</span><span class="sxs-lookup"><span data-stu-id="9427b-144">NOTES</span></span>

## <span data-ttu-id="9427b-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="9427b-145">RELATED LINKS</span></span>
