---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
ms.openlocfilehash: 4714b97773583197807d6ca54152ee25ab520909
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448582"
---
# <span data-ttu-id="e8a03-101">Get-AzureRmReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="e8a03-101">Get-AzureRmReservationCatalog</span></span>

## <span data-ttu-id="e8a03-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8a03-102">SYNOPSIS</span></span>
<span data-ttu-id="e8a03-103">取得可用保留的目錄</span><span class="sxs-lookup"><span data-stu-id="e8a03-103">Get the catalog of available reservation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8a03-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8a03-104">SYNTAX</span></span>

```
Get-AzureRmReservationCatalog [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="e8a03-105">說明</span><span class="sxs-lookup"><span data-stu-id="e8a03-105">DESCRIPTION</span></span>
<span data-ttu-id="e8a03-106">取得適用于指定 Azure 訂閱之保留實例購買的地區和 sku。</span><span class="sxs-lookup"><span data-stu-id="e8a03-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="e8a03-107">示例</span><span class="sxs-lookup"><span data-stu-id="e8a03-107">EXAMPLES</span></span>

### <span data-ttu-id="e8a03-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e8a03-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationCatalog
```

<span data-ttu-id="e8a03-109">取得預設訂閱的目錄</span><span class="sxs-lookup"><span data-stu-id="e8a03-109">Get the catalog for the default subscription</span></span>

### <span data-ttu-id="e8a03-110">範例2</span><span class="sxs-lookup"><span data-stu-id="e8a03-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="e8a03-111">取得指定訂閱的目錄</span><span class="sxs-lookup"><span data-stu-id="e8a03-111">Get the catalog for the specified subscription</span></span>

## <span data-ttu-id="e8a03-112">參數</span><span class="sxs-lookup"><span data-stu-id="e8a03-112">PARAMETERS</span></span>

### <span data-ttu-id="e8a03-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e8a03-113">-SubscriptionId</span></span>
<span data-ttu-id="e8a03-114">訂閱的識別碼</span><span class="sxs-lookup"><span data-stu-id="e8a03-114">Id of the subscription</span></span>

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

### <span data-ttu-id="e8a03-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8a03-115">CommonParameters</span></span>
<span data-ttu-id="e8a03-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8a03-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8a03-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e8a03-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8a03-118">輸入</span><span class="sxs-lookup"><span data-stu-id="e8a03-118">INPUTS</span></span>

### <span data-ttu-id="e8a03-119">所有</span><span class="sxs-lookup"><span data-stu-id="e8a03-119">None</span></span>

## <span data-ttu-id="e8a03-120">輸出</span><span class="sxs-lookup"><span data-stu-id="e8a03-120">OUTPUTS</span></span>

### <span data-ttu-id="e8a03-121">[System.object]。清單 ' 1 [PSCatalog，#........ = 1.0.0.0，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e8a03-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Reservations.Models.PSCatalog, Microsoft.Azure.Commands.Reservations, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e8a03-122">筆記</span><span class="sxs-lookup"><span data-stu-id="e8a03-122">NOTES</span></span>

## <span data-ttu-id="e8a03-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8a03-123">RELATED LINKS</span></span>

