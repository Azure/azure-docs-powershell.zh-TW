---
external help file: Microsoft.Azure.Commands.SubscriptionDefinition.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.subscription.preview/get-azurermsubscriptiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/Get-AzureRmSubscriptionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/Get-AzureRmSubscriptionDefinition.md
ms.openlocfilehash: 8f9cfda051542327fdb6175da081c99e6b8b6b3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445915"
---
# <span data-ttu-id="34941-101">Get-AzureRmSubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="34941-101">Get-AzureRmSubscriptionDefinition</span></span>

## <span data-ttu-id="34941-102">摘要</span><span class="sxs-lookup"><span data-stu-id="34941-102">SYNOPSIS</span></span>
<span data-ttu-id="34941-103">取得訂閱定義。</span><span class="sxs-lookup"><span data-stu-id="34941-103">Get a subscription definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34941-104">句法</span><span class="sxs-lookup"><span data-stu-id="34941-104">SYNTAX</span></span>

### <span data-ttu-id="34941-105">取得訂閱定義。</span><span class="sxs-lookup"><span data-stu-id="34941-105">Get subscription definitions.</span></span>
```
Get-AzureRmSubscriptionDefinition
```

## <span data-ttu-id="34941-106">示例</span><span class="sxs-lookup"><span data-stu-id="34941-106">EXAMPLES</span></span>

### <span data-ttu-id="34941-107">範例1</span><span class="sxs-lookup"><span data-stu-id="34941-107">Example 1</span></span>
```
PS C:\> Get-AzureRmSubscriptionDefinition

Name                    : MyProdSubscription1
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MyProdSubscription1
OfferType               : MS-AZR-0017P

Name                    : MyProdSubscription2
SubscriptionId          : 368425df-b536-4f42-b1ba-64613cfcc4b5
SubscriptionDisplayName : MyProdSubscription2
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="34941-108">取得所有訂閱定義。</span><span class="sxs-lookup"><span data-stu-id="34941-108">Gets all subscription definitions.</span></span>

### <span data-ttu-id="34941-109">範例2</span><span class="sxs-lookup"><span data-stu-id="34941-109">Example 2</span></span>
```
PS C:\> Get-AzureRmSubscriptionDefinition -Name MyProdSubscription2

Name                    : MyProdSubscription2
SubscriptionId          : 368425df-b536-4f42-b1ba-64613cfcc4b5
SubscriptionDisplayName : MyProdSubscription2
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="34941-110">取得名為 MyProdSubscription2 的訂閱定義。</span><span class="sxs-lookup"><span data-stu-id="34941-110">Gets a subscription definition with the name MyProdSubscription2.</span></span>

## <span data-ttu-id="34941-111">參數</span><span class="sxs-lookup"><span data-stu-id="34941-111">PARAMETERS</span></span>

### <span data-ttu-id="34941-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="34941-112">-Name</span></span>
<span data-ttu-id="34941-113">要檢索之訂閱定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="34941-113">The name of the subscription definition to retrieve.</span></span>

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

### <span data-ttu-id="34941-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34941-114">CommonParameters</span></span>
<span data-ttu-id="34941-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="34941-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34941-116">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="34941-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34941-117">輸入</span><span class="sxs-lookup"><span data-stu-id="34941-117">INPUTS</span></span>

### <span data-ttu-id="34941-118">所有</span><span class="sxs-lookup"><span data-stu-id="34941-118">None</span></span>

## <span data-ttu-id="34941-119">輸出</span><span class="sxs-lookup"><span data-stu-id="34941-119">OUTPUTS</span></span>

### <span data-ttu-id="34941-120">[System.object]。清單 ' 1 [SubscriptionDefinition. PSSubscriptionDefinition，SubscriptionDefinition，版本 = 0.1.0.0，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="34941-120">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.SubscriptionDefinition.Models.PSSubscriptionDefinition, Microsoft.Azure.Commands.SubscriptionDefinition, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="34941-121">筆記</span><span class="sxs-lookup"><span data-stu-id="34941-121">NOTES</span></span>

## <span data-ttu-id="34941-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="34941-122">RELATED LINKS</span></span>

