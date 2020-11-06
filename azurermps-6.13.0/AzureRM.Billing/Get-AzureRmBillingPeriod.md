---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
ms.openlocfilehash: 66c9a0bb9ba4aa2f17c48ffb737f1c8d72034f1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452848"
---
# <span data-ttu-id="3b6f9-101">Get-AzureRmBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="3b6f9-101">Get-AzureRmBillingPeriod</span></span>

## <span data-ttu-id="3b6f9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3b6f9-102">SYNOPSIS</span></span>
<span data-ttu-id="3b6f9-103">取得訂閱的計費期間。</span><span class="sxs-lookup"><span data-stu-id="3b6f9-103">Get billing periods of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b6f9-104">句法</span><span class="sxs-lookup"><span data-stu-id="3b6f9-104">SYNTAX</span></span>

### <span data-ttu-id="3b6f9-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="3b6f9-105">List (Default)</span></span>
```
Get-AzureRmBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b6f9-106">通過</span><span class="sxs-lookup"><span data-stu-id="3b6f9-106">Single</span></span>
```
Get-AzureRmBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b6f9-107">說明</span><span class="sxs-lookup"><span data-stu-id="3b6f9-107">DESCRIPTION</span></span>
<span data-ttu-id="3b6f9-108">**AzureRmBillingPeriod** Cmdlet 會取得訂閱的計費期間。</span><span class="sxs-lookup"><span data-stu-id="3b6f9-108">The **Get-AzureRmBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="3b6f9-109">示例</span><span class="sxs-lookup"><span data-stu-id="3b6f9-109">EXAMPLES</span></span>

### <span data-ttu-id="3b6f9-110">範例1</span><span class="sxs-lookup"><span data-stu-id="3b6f9-110">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingPeriod
```

<span data-ttu-id="3b6f9-111">取得訂閱的所有可用帳單週期。</span><span class="sxs-lookup"><span data-stu-id="3b6f9-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="3b6f9-112">範例2</span><span class="sxs-lookup"><span data-stu-id="3b6f9-112">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -Name 201704-1
```

<span data-ttu-id="3b6f9-113">以指定名稱取得訂閱的帳單期限。</span><span class="sxs-lookup"><span data-stu-id="3b6f9-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="3b6f9-114">範例3</span><span class="sxs-lookup"><span data-stu-id="3b6f9-114">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -MaxCount 2
```

<span data-ttu-id="3b6f9-115">最多可以取得訂閱的2個帳單期間。</span><span class="sxs-lookup"><span data-stu-id="3b6f9-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="3b6f9-116">參數</span><span class="sxs-lookup"><span data-stu-id="3b6f9-116">PARAMETERS</span></span>

### <span data-ttu-id="3b6f9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b6f9-117">-DefaultProfile</span></span>
<span data-ttu-id="3b6f9-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3b6f9-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b6f9-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="3b6f9-119">-MaxCount</span></span>
<span data-ttu-id="3b6f9-120">決定要傳回的最大記錄數。</span><span class="sxs-lookup"><span data-stu-id="3b6f9-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="3b6f9-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="3b6f9-121">-Name</span></span>
<span data-ttu-id="3b6f9-122">要取得之特定帳單期間的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b6f9-122">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="3b6f9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b6f9-123">CommonParameters</span></span>
<span data-ttu-id="3b6f9-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3b6f9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b6f9-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3b6f9-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b6f9-126">輸入</span><span class="sxs-lookup"><span data-stu-id="3b6f9-126">INPUTS</span></span>

### <span data-ttu-id="3b6f9-127">所有</span><span class="sxs-lookup"><span data-stu-id="3b6f9-127">None</span></span>

## <span data-ttu-id="3b6f9-128">輸出</span><span class="sxs-lookup"><span data-stu-id="3b6f9-128">OUTPUTS</span></span>

### <span data-ttu-id="3b6f9-129">PSBillingPeriod 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3b6f9-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="3b6f9-130">筆記</span><span class="sxs-lookup"><span data-stu-id="3b6f9-130">NOTES</span></span>

## <span data-ttu-id="3b6f9-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b6f9-131">RELATED LINKS</span></span>
