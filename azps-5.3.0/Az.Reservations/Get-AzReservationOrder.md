---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
ms.openlocfilehash: 15faf94ae7e0afac7200423dcd36d8edf2964c21
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437240"
---
# <span data-ttu-id="2780a-101">Get-AzReservationOrder</span><span class="sxs-lookup"><span data-stu-id="2780a-101">Get-AzReservationOrder</span></span>

## <span data-ttu-id="2780a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2780a-102">SYNOPSIS</span></span>
<span data-ttu-id="2780a-103">獲取 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="2780a-103">Get `ReservationOrder`</span></span>

## <span data-ttu-id="2780a-104">句法</span><span class="sxs-lookup"><span data-stu-id="2780a-104">SYNTAX</span></span>

```
Get-AzReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2780a-105">說明</span><span class="sxs-lookup"><span data-stu-id="2780a-105">DESCRIPTION</span></span>
<span data-ttu-id="2780a-106">`ReservationOrder`使用者在目前租使用者中可存取的所有 s 的清單。</span><span class="sxs-lookup"><span data-stu-id="2780a-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="2780a-107">如果已設定 ReservationOrderId 參數，請取得該特定 ReservationOrder。</span><span class="sxs-lookup"><span data-stu-id="2780a-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="2780a-108">示例</span><span class="sxs-lookup"><span data-stu-id="2780a-108">EXAMPLES</span></span>

### <span data-ttu-id="2780a-109">範例1</span><span class="sxs-lookup"><span data-stu-id="2780a-109">Example 1</span></span>
```
PS C:\> Get-AzReservationOrder
```

<span data-ttu-id="2780a-110">列出 `ReservationOrder` 使用者在目前租使用者中可存取的所有內容</span><span class="sxs-lookup"><span data-stu-id="2780a-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="2780a-111">範例2</span><span class="sxs-lookup"><span data-stu-id="2780a-111">Example 2</span></span>
```
PS C:\> Get-AzReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="2780a-112">取得 `ReservationOrder` 指定的 ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="2780a-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="2780a-113">參數</span><span class="sxs-lookup"><span data-stu-id="2780a-113">PARAMETERS</span></span>

### <span data-ttu-id="2780a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2780a-114">-DefaultProfile</span></span>
<span data-ttu-id="2780a-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2780a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2780a-116">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="2780a-116">-ReservationOrderId</span></span>
<span data-ttu-id="2780a-117">使用者想要查看的特定 ReservationOrder 識別碼</span><span class="sxs-lookup"><span data-stu-id="2780a-117">Id of the specific ReservationOrder that user wants to see</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2780a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2780a-118">CommonParameters</span></span>
<span data-ttu-id="2780a-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2780a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2780a-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2780a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2780a-121">輸入</span><span class="sxs-lookup"><span data-stu-id="2780a-121">INPUTS</span></span>

### <span data-ttu-id="2780a-122">所有</span><span class="sxs-lookup"><span data-stu-id="2780a-122">None</span></span>

## <span data-ttu-id="2780a-123">輸出</span><span class="sxs-lookup"><span data-stu-id="2780a-123">OUTPUTS</span></span>

### <span data-ttu-id="2780a-124">PSReservationOrderPage 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="2780a-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="2780a-125">PSReservationOrder 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="2780a-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="2780a-126">筆記</span><span class="sxs-lookup"><span data-stu-id="2780a-126">NOTES</span></span>

## <span data-ttu-id="2780a-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="2780a-127">RELATED LINKS</span></span>
