---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/new-azconfluentmarketplaceagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentMarketplaceAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentMarketplaceAgreement.md
ms.openlocfilehash: f8c293870fa4eeb6f0df8a543473c8a9bda314c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917069"
---
# <span data-ttu-id="f1139-101">New-AzConfluentMarketplaceAgreement</span><span class="sxs-lookup"><span data-stu-id="f1139-101">New-AzConfluentMarketplaceAgreement</span></span>

## <span data-ttu-id="f1139-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f1139-102">SYNOPSIS</span></span>
<span data-ttu-id="f1139-103">接受服務商場條款。</span><span class="sxs-lookup"><span data-stu-id="f1139-103">Accept marketplace terms.</span></span>

## <span data-ttu-id="f1139-104">語法</span><span class="sxs-lookup"><span data-stu-id="f1139-104">SYNTAX</span></span>

```
New-AzConfluentMarketplaceAgreement [-SubscriptionId <String>] [-Accepted] [-LicenseTextLink <String>]
 [-Plan <String>] [-PrivacyPolicyLink <String>] [-Product <String>] [-Publisher <String>]
 [-RetrieveDatetime <DateTime>] [-Signature <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="f1139-105">描述</span><span class="sxs-lookup"><span data-stu-id="f1139-105">DESCRIPTION</span></span>
<span data-ttu-id="f1139-106">接受服務商場條款。</span><span class="sxs-lookup"><span data-stu-id="f1139-106">Accept marketplace terms.</span></span>

## <span data-ttu-id="f1139-107">例子</span><span class="sxs-lookup"><span data-stu-id="f1139-107">EXAMPLES</span></span>

### <span data-ttu-id="f1139-108">範例 1：在訂閱下建立集市協定</span><span class="sxs-lookup"><span data-stu-id="f1139-108">Example 1: Create confluent marketplace agreement under a subscription</span></span>
```powershell
PS C:\> New-AzConfluentMarketplaceAgreement -Accepted

Name    Type
----    ----
default Microsoft.Confluent/agreement
```

<span data-ttu-id="f1139-109">此命令在訂閱下建立一份不必要的服務商場協定。</span><span class="sxs-lookup"><span data-stu-id="f1139-109">This command create confluent marketplace agreement under a subscription.</span></span>

## <span data-ttu-id="f1139-110">參數</span><span class="sxs-lookup"><span data-stu-id="f1139-110">PARAMETERS</span></span>

### <span data-ttu-id="f1139-111">-已接受</span><span class="sxs-lookup"><span data-stu-id="f1139-111">-Accepted</span></span>
<span data-ttu-id="f1139-112">若已接受任何版本的條款，否則為 False。</span><span class="sxs-lookup"><span data-stu-id="f1139-112">If any version of the terms have been accepted, otherwise false.</span></span>

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

### <span data-ttu-id="f1139-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1139-113">-DefaultProfile</span></span>
<span data-ttu-id="f1139-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f1139-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1139-115">-LicenseTextLink</span><span class="sxs-lookup"><span data-stu-id="f1139-115">-LicenseTextLink</span></span>
<span data-ttu-id="f1139-116">使用 Microsoft 和 Publisher 條款連結至 HTML。</span><span class="sxs-lookup"><span data-stu-id="f1139-116">Link to HTML with Microsoft and Publisher terms.</span></span>

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

### <span data-ttu-id="f1139-117">-規劃</span><span class="sxs-lookup"><span data-stu-id="f1139-117">-Plan</span></span>
<span data-ttu-id="f1139-118">計畫識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="f1139-118">Plan identifier string.</span></span>

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

### <span data-ttu-id="f1139-119">-PrivacyPolicyLink</span><span class="sxs-lookup"><span data-stu-id="f1139-119">-PrivacyPolicyLink</span></span>
<span data-ttu-id="f1139-120">連結至發行者的隱私權原則。</span><span class="sxs-lookup"><span data-stu-id="f1139-120">Link to the privacy policy of the publisher.</span></span>

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

### <span data-ttu-id="f1139-121">-產品</span><span class="sxs-lookup"><span data-stu-id="f1139-121">-Product</span></span>
<span data-ttu-id="f1139-122">產品識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="f1139-122">Product identifier string.</span></span>

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

### <span data-ttu-id="f1139-123">-Publisher</span><span class="sxs-lookup"><span data-stu-id="f1139-123">-Publisher</span></span>
<span data-ttu-id="f1139-124">Publisher 識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="f1139-124">Publisher identifier string.</span></span>

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

### <span data-ttu-id="f1139-125">-RetrieveDatetime</span><span class="sxs-lookup"><span data-stu-id="f1139-125">-RetrieveDatetime</span></span>
<span data-ttu-id="f1139-126">接受條款的日期和時間 ，以 UTC 表示。</span><span class="sxs-lookup"><span data-stu-id="f1139-126">Date and time in UTC of when the terms were accepted.</span></span>
<span data-ttu-id="f1139-127">如果接受為 False，則此為空白。</span><span class="sxs-lookup"><span data-stu-id="f1139-127">This is empty if Accepted is false.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1139-128">-簽章</span><span class="sxs-lookup"><span data-stu-id="f1139-128">-Signature</span></span>
<span data-ttu-id="f1139-129">條款簽章。</span><span class="sxs-lookup"><span data-stu-id="f1139-129">Terms signature.</span></span>

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

### <span data-ttu-id="f1139-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f1139-130">-SubscriptionId</span></span>
<span data-ttu-id="f1139-131">Microsoft Azure 訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="f1139-131">Microsoft Azure subscription id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1139-132">-確認</span><span class="sxs-lookup"><span data-stu-id="f1139-132">-Confirm</span></span>
<span data-ttu-id="f1139-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f1139-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1139-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1139-134">-WhatIf</span></span>
<span data-ttu-id="f1139-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f1139-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1139-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1139-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1139-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1139-137">CommonParameters</span></span>
<span data-ttu-id="f1139-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f1139-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1139-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1139-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1139-140">輸入</span><span class="sxs-lookup"><span data-stu-id="f1139-140">INPUTS</span></span>

## <span data-ttu-id="f1139-141">輸出</span><span class="sxs-lookup"><span data-stu-id="f1139-141">OUTPUTS</span></span>

### <span data-ttu-id="f1139-142">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IConfluentAgreementResource</span><span class="sxs-lookup"><span data-stu-id="f1139-142">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IConfluentAgreementResource</span></span>

## <span data-ttu-id="f1139-143">筆記</span><span class="sxs-lookup"><span data-stu-id="f1139-143">NOTES</span></span>

<span data-ttu-id="f1139-144">別名</span><span class="sxs-lookup"><span data-stu-id="f1139-144">ALIASES</span></span>

## <span data-ttu-id="f1139-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1139-145">RELATED LINKS</span></span>

