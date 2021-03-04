---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/get-azreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
ms.openlocfilehash: 77fb1806ba2cbdd2e0398bcdf8289aed62c085fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914530"
---
# <span data-ttu-id="5b4d6-101">Get-AzReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="5b4d6-101">Get-AzReservationCatalog</span></span>

## <span data-ttu-id="5b4d6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5b4d6-102">SYNOPSIS</span></span>
<span data-ttu-id="5b4d6-103">取得可用預約的目錄</span><span class="sxs-lookup"><span data-stu-id="5b4d6-103">Get the catalog of available reservations</span></span>

## <span data-ttu-id="5b4d6-104">語法</span><span class="sxs-lookup"><span data-stu-id="5b4d6-104">SYNTAX</span></span>

```
Get-AzReservationCatalog [-SubscriptionId <Guid>] -ReservedResourceType <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b4d6-105">描述</span><span class="sxs-lookup"><span data-stu-id="5b4d6-105">DESCRIPTION</span></span>
<span data-ttu-id="5b4d6-106">取得指定 Azure 訂閱的保留實例購買可用的地區和 SKU。</span><span class="sxs-lookup"><span data-stu-id="5b4d6-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="5b4d6-107">例子</span><span class="sxs-lookup"><span data-stu-id="5b4d6-107">EXAMPLES</span></span>

### <span data-ttu-id="5b4d6-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="5b4d6-108">Example 1</span></span>
```
PS C:\> Get-AzReservationCatalog -ReservedResourceType VirtualMachines -Location westus
```

<span data-ttu-id="5b4d6-109">取得 Westus 中預設訂閱的 VirtualMachines 目錄</span><span class="sxs-lookup"><span data-stu-id="5b4d6-109">Get the VirtualMachines catalog in westus for the default subscription</span></span>

### <span data-ttu-id="5b4d6-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="5b4d6-110">Example 2</span></span>
```
PS C:\> Get-AzReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservedResourceType SuseLinux
```

<span data-ttu-id="5b4d6-111">取得指定訂閱的 Suse 版 Azure 目錄</span><span class="sxs-lookup"><span data-stu-id="5b4d6-111">Get the SuseLinux catalog for the specified subscription</span></span>

## <span data-ttu-id="5b4d6-112">參數</span><span class="sxs-lookup"><span data-stu-id="5b4d6-112">PARAMETERS</span></span>

### <span data-ttu-id="5b4d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b4d6-113">-DefaultProfile</span></span>
<span data-ttu-id="5b4d6-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5b4d6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b4d6-115">-位置</span><span class="sxs-lookup"><span data-stu-id="5b4d6-115">-Location</span></span>
<span data-ttu-id="5b4d6-116">指定目錄中保留資源的位置</span><span class="sxs-lookup"><span data-stu-id="5b4d6-116">Specifies the location of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="5b4d6-117">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="5b4d6-117">-ReservedResourceType</span></span>
<span data-ttu-id="5b4d6-118">指定目錄中保留資源的類型</span><span class="sxs-lookup"><span data-stu-id="5b4d6-118">Specifies the type of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="5b4d6-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5b4d6-119">-SubscriptionId</span></span>
<span data-ttu-id="5b4d6-120">訂閱的識別碼</span><span class="sxs-lookup"><span data-stu-id="5b4d6-120">Id of the subscription</span></span>

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

### <span data-ttu-id="5b4d6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b4d6-121">CommonParameters</span></span>
<span data-ttu-id="5b4d6-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5b4d6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b4d6-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b4d6-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b4d6-124">輸入</span><span class="sxs-lookup"><span data-stu-id="5b4d6-124">INPUTS</span></span>

### <span data-ttu-id="5b4d6-125">沒有</span><span class="sxs-lookup"><span data-stu-id="5b4d6-125">None</span></span>

## <span data-ttu-id="5b4d6-126">輸出</span><span class="sxs-lookup"><span data-stu-id="5b4d6-126">OUTPUTS</span></span>

### <span data-ttu-id="5b4d6-127">Microsoft.Azure.Commands.Reservations.models.PSCatalog</span><span class="sxs-lookup"><span data-stu-id="5b4d6-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span></span>

## <span data-ttu-id="5b4d6-128">筆記</span><span class="sxs-lookup"><span data-stu-id="5b4d6-128">NOTES</span></span>

## <span data-ttu-id="5b4d6-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b4d6-129">RELATED LINKS</span></span>
