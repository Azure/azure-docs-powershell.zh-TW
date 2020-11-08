---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/update-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
ms.openlocfilehash: 4d4228ebcdf007485e35b45b93ea738c828c9c4d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126253"
---
# <span data-ttu-id="d6b60-101">Update-AzReservation</span><span class="sxs-lookup"><span data-stu-id="d6b60-101">Update-AzReservation</span></span>

## <span data-ttu-id="d6b60-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d6b60-102">SYNOPSIS</span></span>
<span data-ttu-id="d6b60-103">更新 `Reservation` 。</span><span class="sxs-lookup"><span data-stu-id="d6b60-103">Update a `Reservation`.</span></span>

## <span data-ttu-id="d6b60-104">句法</span><span class="sxs-lookup"><span data-stu-id="d6b60-104">SYNTAX</span></span>

### <span data-ttu-id="d6b60-105">[命令列 (預設) </span><span class="sxs-lookup"><span data-stu-id="d6b60-105">CommandLine (Default)</span></span>
```
Update-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -AppliedScopeType <String>
 [-AppliedScope <String>] [-InstanceFlexibility <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6b60-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="d6b60-106">PipeObject</span></span>
```
Update-AzReservation -AppliedScopeType <String> [-AppliedScope <String>] [-InstanceFlexibility <String>]
 -Reservation <PSReservation> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6b60-107">說明</span><span class="sxs-lookup"><span data-stu-id="d6b60-107">DESCRIPTION</span></span>
<span data-ttu-id="d6b60-108">更新已套用的範圍 `Reservation` 。</span><span class="sxs-lookup"><span data-stu-id="d6b60-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="d6b60-109">示例</span><span class="sxs-lookup"><span data-stu-id="d6b60-109">EXAMPLES</span></span>

### <span data-ttu-id="d6b60-110">範例1</span><span class="sxs-lookup"><span data-stu-id="d6b60-110">Example 1</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff" -InstanceFlexibility "On"
```

<span data-ttu-id="d6b60-111">更新指定 `Reservation` 到單一和 InstanceFlexibility 的 AppliedScopeType。</span><span class="sxs-lookup"><span data-stu-id="d6b60-111">Updates the AppliedScopeType of the specified `Reservation` to Single and InstanceFlexibility to On.</span></span>

### <span data-ttu-id="d6b60-112">範例2</span><span class="sxs-lookup"><span data-stu-id="d6b60-112">Example 2</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared" -InstanceFlexibility "Off"
```

<span data-ttu-id="d6b60-113">將指定的 AppliedScopeType 更新 `Reservation` 為 [共用]，然後 InstanceFlexibility [關閉]。</span><span class="sxs-lookup"><span data-stu-id="d6b60-113">Updates the AppliedScopeType of the specified `Reservation` to Shared and InstanceFlexibility to Off.</span></span>

## <span data-ttu-id="d6b60-114">參數</span><span class="sxs-lookup"><span data-stu-id="d6b60-114">PARAMETERS</span></span>

### <span data-ttu-id="d6b60-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="d6b60-115">-AppliedScope</span></span>
<span data-ttu-id="d6b60-116">要套用此應用程式的 SubscriptionId `Reservation`</span><span class="sxs-lookup"><span data-stu-id="d6b60-116">SubscriptionId for this `Reservation` to be applied</span></span>

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

### <span data-ttu-id="d6b60-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="d6b60-117">-AppliedScopeType</span></span>
<span data-ttu-id="d6b60-118">已套用的範圍類型</span><span class="sxs-lookup"><span data-stu-id="d6b60-118">Type of the Applied Scope</span></span>

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

### <span data-ttu-id="d6b60-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6b60-119">-DefaultProfile</span></span>
<span data-ttu-id="d6b60-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d6b60-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6b60-121">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="d6b60-121">-InstanceFlexibility</span></span>
<span data-ttu-id="d6b60-122">如果有的話，請更新的 InstanceFlexibility 值 `Reservation` 。</span><span class="sxs-lookup"><span data-stu-id="d6b60-122">If present, updates the InstanceFlexibility value of the `Reservation`.</span></span> <span data-ttu-id="d6b60-123">如果未指定，現有的值會保持不變。</span><span class="sxs-lookup"><span data-stu-id="d6b60-123">If not specified, the existing value remains unchanged.</span></span>

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

### <span data-ttu-id="d6b60-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="d6b60-124">-Name</span></span>
<span data-ttu-id="d6b60-125">保留名稱</span><span class="sxs-lookup"><span data-stu-id="d6b60-125">Name of Reservation</span></span>

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

### <span data-ttu-id="d6b60-126">預留</span><span class="sxs-lookup"><span data-stu-id="d6b60-126">-Reservation</span></span>
<span data-ttu-id="d6b60-127">的 Pipe 物件參數 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="d6b60-127">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="d6b60-128">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="d6b60-128">-ReservationId</span></span>
<span data-ttu-id="d6b60-129">`Reservation`要更新的識別碼</span><span class="sxs-lookup"><span data-stu-id="d6b60-129">Id of the `Reservation` to update</span></span>

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

### <span data-ttu-id="d6b60-130">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="d6b60-130">-ReservationOrderId</span></span>
<span data-ttu-id="d6b60-131">`ReservationOrder`要更新的識別碼</span><span class="sxs-lookup"><span data-stu-id="d6b60-131">Id of the `ReservationOrder` to update</span></span>

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

### <span data-ttu-id="d6b60-132">-確認</span><span class="sxs-lookup"><span data-stu-id="d6b60-132">-Confirm</span></span>
<span data-ttu-id="d6b60-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d6b60-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6b60-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6b60-134">-WhatIf</span></span>
<span data-ttu-id="d6b60-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d6b60-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d6b60-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d6b60-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6b60-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6b60-137">CommonParameters</span></span>
<span data-ttu-id="d6b60-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d6b60-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6b60-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d6b60-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6b60-140">輸入</span><span class="sxs-lookup"><span data-stu-id="d6b60-140">INPUTS</span></span>

### <span data-ttu-id="d6b60-141">PSReservation 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="d6b60-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="d6b60-142">輸出</span><span class="sxs-lookup"><span data-stu-id="d6b60-142">OUTPUTS</span></span>

### <span data-ttu-id="d6b60-143">PSReservation 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="d6b60-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="d6b60-144">筆記</span><span class="sxs-lookup"><span data-stu-id="d6b60-144">NOTES</span></span>

## <span data-ttu-id="d6b60-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="d6b60-145">RELATED LINKS</span></span>