---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
ms.openlocfilehash: 6a7f7d47976608b521e69e7aaf926a9600b35382
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98450013"
---
# <span data-ttu-id="aac8c-101">Get-AzBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="aac8c-101">Get-AzBillingPeriod</span></span>

## <span data-ttu-id="aac8c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aac8c-102">SYNOPSIS</span></span>
<span data-ttu-id="aac8c-103">取得訂閱的計費期間。</span><span class="sxs-lookup"><span data-stu-id="aac8c-103">Get billing periods of the subscription.</span></span>

## <span data-ttu-id="aac8c-104">句法</span><span class="sxs-lookup"><span data-stu-id="aac8c-104">SYNTAX</span></span>

### <span data-ttu-id="aac8c-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="aac8c-105">List (Default)</span></span>
```
Get-AzBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aac8c-106">通過</span><span class="sxs-lookup"><span data-stu-id="aac8c-106">Single</span></span>
```
Get-AzBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aac8c-107">說明</span><span class="sxs-lookup"><span data-stu-id="aac8c-107">DESCRIPTION</span></span>
<span data-ttu-id="aac8c-108">**AzBillingPeriod** Cmdlet 會取得訂閱的計費期間。</span><span class="sxs-lookup"><span data-stu-id="aac8c-108">The **Get-AzBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="aac8c-109">示例</span><span class="sxs-lookup"><span data-stu-id="aac8c-109">EXAMPLES</span></span>

### <span data-ttu-id="aac8c-110">範例1</span><span class="sxs-lookup"><span data-stu-id="aac8c-110">Example 1</span></span>
```
PS C:\> Get-AzBillingPeriod
```

<span data-ttu-id="aac8c-111">取得訂閱的所有可用帳單週期。</span><span class="sxs-lookup"><span data-stu-id="aac8c-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="aac8c-112">範例2</span><span class="sxs-lookup"><span data-stu-id="aac8c-112">Example 2</span></span>
```
PS C:\> Get-AzBillingPeriod -Name 201704-1
```

<span data-ttu-id="aac8c-113">以指定名稱取得訂閱的帳單期限。</span><span class="sxs-lookup"><span data-stu-id="aac8c-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="aac8c-114">範例3</span><span class="sxs-lookup"><span data-stu-id="aac8c-114">Example 3</span></span>
```
PS C:\> Get-AzBillingPeriod -MaxCount 2
```

<span data-ttu-id="aac8c-115">最多可以取得訂閱的2個帳單期間。</span><span class="sxs-lookup"><span data-stu-id="aac8c-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="aac8c-116">參數</span><span class="sxs-lookup"><span data-stu-id="aac8c-116">PARAMETERS</span></span>

### <span data-ttu-id="aac8c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aac8c-117">-DefaultProfile</span></span>
<span data-ttu-id="aac8c-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="aac8c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aac8c-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="aac8c-119">-MaxCount</span></span>
<span data-ttu-id="aac8c-120">決定要傳回的最大記錄數。</span><span class="sxs-lookup"><span data-stu-id="aac8c-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="aac8c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="aac8c-121">-Name</span></span>
<span data-ttu-id="aac8c-122">要取得之特定帳單期間的名稱。</span><span class="sxs-lookup"><span data-stu-id="aac8c-122">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="aac8c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aac8c-123">CommonParameters</span></span>
<span data-ttu-id="aac8c-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aac8c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aac8c-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aac8c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aac8c-126">輸入</span><span class="sxs-lookup"><span data-stu-id="aac8c-126">INPUTS</span></span>

### <span data-ttu-id="aac8c-127">所有</span><span class="sxs-lookup"><span data-stu-id="aac8c-127">None</span></span>

## <span data-ttu-id="aac8c-128">輸出</span><span class="sxs-lookup"><span data-stu-id="aac8c-128">OUTPUTS</span></span>

### <span data-ttu-id="aac8c-129">PSBillingPeriod 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="aac8c-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="aac8c-130">筆記</span><span class="sxs-lookup"><span data-stu-id="aac8c-130">NOTES</span></span>

## <span data-ttu-id="aac8c-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="aac8c-131">RELATED LINKS</span></span>
