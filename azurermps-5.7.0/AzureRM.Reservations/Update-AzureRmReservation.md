---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/update-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Update-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Update-AzureRmReservation.md
ms.openlocfilehash: 76abdc2f7a7099529af87f69af8e37319685aea7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448573"
---
# <span data-ttu-id="ca277-101">Update-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="ca277-101">Update-AzureRmReservation</span></span>

## <span data-ttu-id="ca277-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ca277-102">SYNOPSIS</span></span>
<span data-ttu-id="ca277-103">更新 `Reservation` 。</span><span class="sxs-lookup"><span data-stu-id="ca277-103">Update a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca277-104">句法</span><span class="sxs-lookup"><span data-stu-id="ca277-104">SYNTAX</span></span>

### <span data-ttu-id="ca277-105">[命令列 (預設) </span><span class="sxs-lookup"><span data-stu-id="ca277-105">CommandLine (Default)</span></span>
```
Update-AzureRmReservation -ReservationOrderId <String> -ReservationId <String> -AppliedScopeType <String>
 [-AppliedScope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca277-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="ca277-106">PipeObject</span></span>
```
Update-AzureRmReservation -AppliedScopeType <String> [-AppliedScope <String>] -Reservation <PSReservation>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca277-107">說明</span><span class="sxs-lookup"><span data-stu-id="ca277-107">DESCRIPTION</span></span>
<span data-ttu-id="ca277-108">更新已套用的範圍 `Reservation` 。</span><span class="sxs-lookup"><span data-stu-id="ca277-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="ca277-109">示例</span><span class="sxs-lookup"><span data-stu-id="ca277-109">EXAMPLES</span></span>

### <span data-ttu-id="ca277-110">範例1</span><span class="sxs-lookup"><span data-stu-id="ca277-110">Example 1</span></span>
```
PS C:\> Update-AzureRmReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="ca277-111">將指定保留的 AppliedScopeType 更新為 Single</span><span class="sxs-lookup"><span data-stu-id="ca277-111">Updates the AppliedScopeType of the specified reservation to Single</span></span>

### <span data-ttu-id="ca277-112">範例2</span><span class="sxs-lookup"><span data-stu-id="ca277-112">Example 2</span></span>
```
PS C:\> Update-AzureRmReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared"
```

<span data-ttu-id="ca277-113">將指定保留的 AppliedScopeType 更新為 [共用]</span><span class="sxs-lookup"><span data-stu-id="ca277-113">Updates the AppliedScopeType of the specified reservation to Shared</span></span>

## <span data-ttu-id="ca277-114">參數</span><span class="sxs-lookup"><span data-stu-id="ca277-114">PARAMETERS</span></span>

### <span data-ttu-id="ca277-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="ca277-115">-AppliedScope</span></span>
<span data-ttu-id="ca277-116">要套用此應用程式的 SubscriptionId `Reservation`</span><span class="sxs-lookup"><span data-stu-id="ca277-116">SubscriptionId for this `Reservation` to be applied</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca277-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="ca277-117">-AppliedScopeType</span></span>
<span data-ttu-id="ca277-118">`Reservation`要更新的類型</span><span class="sxs-lookup"><span data-stu-id="ca277-118">Type of the `Reservation` to be updated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Single, Shared

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca277-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca277-119">-DefaultProfile</span></span>
<span data-ttu-id="ca277-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ca277-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca277-121">預留</span><span class="sxs-lookup"><span data-stu-id="ca277-121">-Reservation</span></span>
<span data-ttu-id="ca277-122">的 Pipe 物件參數 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="ca277-122">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: PSReservation
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca277-123">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="ca277-123">-ReservationId</span></span>
<span data-ttu-id="ca277-124">`Reservation`要更新的識別碼</span><span class="sxs-lookup"><span data-stu-id="ca277-124">Id of the `Reservation` to update</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca277-125">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="ca277-125">-ReservationOrderId</span></span>
<span data-ttu-id="ca277-126">`ReservationOrder`要更新的識別碼</span><span class="sxs-lookup"><span data-stu-id="ca277-126">Id of the `ReservationOrder` to update</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca277-127">-確認</span><span class="sxs-lookup"><span data-stu-id="ca277-127">-Confirm</span></span>
<span data-ttu-id="ca277-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ca277-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca277-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca277-129">-WhatIf</span></span>
<span data-ttu-id="ca277-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ca277-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca277-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca277-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca277-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca277-132">CommonParameters</span></span>
<span data-ttu-id="ca277-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ca277-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca277-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ca277-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca277-135">輸入</span><span class="sxs-lookup"><span data-stu-id="ca277-135">INPUTS</span></span>

### <span data-ttu-id="ca277-136">PSReservation 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="ca277-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="ca277-137">輸出</span><span class="sxs-lookup"><span data-stu-id="ca277-137">OUTPUTS</span></span>

### <span data-ttu-id="ca277-138">PSReservation 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="ca277-138">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="ca277-139">筆記</span><span class="sxs-lookup"><span data-stu-id="ca277-139">NOTES</span></span>

## <span data-ttu-id="ca277-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca277-140">RELATED LINKS</span></span>

