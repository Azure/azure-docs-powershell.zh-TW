---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
ms.openlocfilehash: d2a859740d2e5627eca3ca0748aab8e72c1ee9af
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911753"
---
# <span data-ttu-id="85c85-101">Get-AzBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="85c85-101">Get-AzBillingPeriod</span></span>

## <span data-ttu-id="85c85-102">簡介</span><span class="sxs-lookup"><span data-stu-id="85c85-102">SYNOPSIS</span></span>
<span data-ttu-id="85c85-103">取得訂閱的計費期間。</span><span class="sxs-lookup"><span data-stu-id="85c85-103">Get billing periods of the subscription.</span></span>

## <span data-ttu-id="85c85-104">語法</span><span class="sxs-lookup"><span data-stu-id="85c85-104">SYNTAX</span></span>

### <span data-ttu-id="85c85-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="85c85-105">List (Default)</span></span>
```
Get-AzBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85c85-106">單</span><span class="sxs-lookup"><span data-stu-id="85c85-106">Single</span></span>
```
Get-AzBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85c85-107">描述</span><span class="sxs-lookup"><span data-stu-id="85c85-107">DESCRIPTION</span></span>
<span data-ttu-id="85c85-108">**Get-AzBillingPeriod** Cmdlet 會取得訂閱的計費期間。</span><span class="sxs-lookup"><span data-stu-id="85c85-108">The **Get-AzBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="85c85-109">例子</span><span class="sxs-lookup"><span data-stu-id="85c85-109">EXAMPLES</span></span>

### <span data-ttu-id="85c85-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="85c85-110">Example 1</span></span>
```
PS C:\> Get-AzBillingPeriod
```

<span data-ttu-id="85c85-111">取得訂閱的所有可用計費期間。</span><span class="sxs-lookup"><span data-stu-id="85c85-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="85c85-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="85c85-112">Example 2</span></span>
```
PS C:\> Get-AzBillingPeriod -Name 201704-1
```

<span data-ttu-id="85c85-113">取得具有指定名稱之訂閱的計費期間。</span><span class="sxs-lookup"><span data-stu-id="85c85-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="85c85-114">範例 3</span><span class="sxs-lookup"><span data-stu-id="85c85-114">Example 3</span></span>
```
PS C:\> Get-AzBillingPeriod -MaxCount 2
```

<span data-ttu-id="85c85-115">取得訂閱最多 2 個計費期間。</span><span class="sxs-lookup"><span data-stu-id="85c85-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="85c85-116">參數</span><span class="sxs-lookup"><span data-stu-id="85c85-116">PARAMETERS</span></span>

### <span data-ttu-id="85c85-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85c85-117">-DefaultProfile</span></span>
<span data-ttu-id="85c85-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="85c85-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85c85-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="85c85-119">-MaxCount</span></span>
<span data-ttu-id="85c85-120">決定要退回的記錄數目上限。</span><span class="sxs-lookup"><span data-stu-id="85c85-120">Determine the maximum number of records to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85c85-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="85c85-121">-Name</span></span>
<span data-ttu-id="85c85-122">要取得的特定計費期間名稱。</span><span class="sxs-lookup"><span data-stu-id="85c85-122">Name of a specific billing period to get.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85c85-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85c85-123">CommonParameters</span></span>
<span data-ttu-id="85c85-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="85c85-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85c85-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="85c85-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85c85-126">輸入</span><span class="sxs-lookup"><span data-stu-id="85c85-126">INPUTS</span></span>

### <span data-ttu-id="85c85-127">沒有</span><span class="sxs-lookup"><span data-stu-id="85c85-127">None</span></span>

## <span data-ttu-id="85c85-128">輸出</span><span class="sxs-lookup"><span data-stu-id="85c85-128">OUTPUTS</span></span>

### <span data-ttu-id="85c85-129">Microsoft.Azure.Commands.Billing.models.PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="85c85-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="85c85-130">筆記</span><span class="sxs-lookup"><span data-stu-id="85c85-130">NOTES</span></span>

## <span data-ttu-id="85c85-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="85c85-131">RELATED LINKS</span></span>
