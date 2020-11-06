---
external help file: Microsoft.Azure.Commands.SubscriptionDefinition.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.subscription.preview/new-azurermsubscriptiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscriptionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscriptionDefinition.md
ms.openlocfilehash: 7acaca4977114a1a57f88f5050f658753a9b6214
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452967"
---
# <span data-ttu-id="9e587-101">New-AzureRmSubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="9e587-101">New-AzureRmSubscriptionDefinition</span></span>

## <span data-ttu-id="9e587-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9e587-102">SYNOPSIS</span></span>
<span data-ttu-id="9e587-103">建立訂閱定義。</span><span class="sxs-lookup"><span data-stu-id="9e587-103">Creates a subscription definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e587-104">句法</span><span class="sxs-lookup"><span data-stu-id="9e587-104">SYNTAX</span></span>

### <span data-ttu-id="9e587-105">建立訂閱定義</span><span class="sxs-lookup"><span data-stu-id="9e587-105">Create subscription definition</span></span>
```
New-AzureRmSubscriptionDefinition -Name <String> -OfferType <String> [-SubscriptionDisplayName <String>]
```

## <span data-ttu-id="9e587-106">說明</span><span class="sxs-lookup"><span data-stu-id="9e587-106">DESCRIPTION</span></span>
<span data-ttu-id="9e587-107">**新的-AzureRmSubscriptionDefinition** Cmdlet 會建立訂閱定義。</span><span class="sxs-lookup"><span data-stu-id="9e587-107">The **New-AzureRmSubscriptionDefinition** cmdlet creates a subscription definition.</span></span>

## <span data-ttu-id="9e587-108">示例</span><span class="sxs-lookup"><span data-stu-id="9e587-108">EXAMPLES</span></span>

### <span data-ttu-id="9e587-109">範例1</span><span class="sxs-lookup"><span data-stu-id="9e587-109">Example 1</span></span>
```
PS C:\> New-AzureRmSubscriptionDefinition -Name MySubDef -OfferType MS-AZR-0017P

Name                    : MySubDef
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MySubDef
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="9e587-110">使用預設訂閱顯示名稱建立訂閱定義。</span><span class="sxs-lookup"><span data-stu-id="9e587-110">Creates a subscription definition with a default subscription display name.</span></span>

### <span data-ttu-id="9e587-111">範例2</span><span class="sxs-lookup"><span data-stu-id="9e587-111">Example 2</span></span>
```
PS C:\> New-AzureRmSubscriptionDefinition -Name MySubDef -OfferType MS-AZR-0017P -SubscriptionDisplayName MyPaygoSub

Name                    : MySubDef
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MyPaygoSub
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="9e587-112">使用自訂訂閱顯示名稱建立訂閱定義。</span><span class="sxs-lookup"><span data-stu-id="9e587-112">Creates a subscription definition with a custom subscription display name.</span></span>

## <span data-ttu-id="9e587-113">參數</span><span class="sxs-lookup"><span data-stu-id="9e587-113">PARAMETERS</span></span>

### <span data-ttu-id="9e587-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="9e587-114">-Name</span></span>
<span data-ttu-id="9e587-115">要建立之訂閱定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="9e587-115">The name of the subscription definition to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e587-116">-OfferType</span><span class="sxs-lookup"><span data-stu-id="9e587-116">-OfferType</span></span>
<span data-ttu-id="9e587-117">建立基礎訂閱時要使用的優惠類型。</span><span class="sxs-lookup"><span data-stu-id="9e587-117">The type of offer to use when creating the underlying subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e587-118">-SubscriptionDisplayName</span><span class="sxs-lookup"><span data-stu-id="9e587-118">-SubscriptionDisplayName</span></span>
<span data-ttu-id="9e587-119">建立訂閱定義的基礎訂閱時所要使用的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="9e587-119">The display name to use when creating the subscription definition's underlying subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e587-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e587-120">CommonParameters</span></span>
<span data-ttu-id="9e587-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9e587-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e587-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9e587-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e587-123">輸入</span><span class="sxs-lookup"><span data-stu-id="9e587-123">INPUTS</span></span>

### <span data-ttu-id="9e587-124">所有</span><span class="sxs-lookup"><span data-stu-id="9e587-124">None</span></span>

## <span data-ttu-id="9e587-125">輸出</span><span class="sxs-lookup"><span data-stu-id="9e587-125">OUTPUTS</span></span>

### <span data-ttu-id="9e587-126">PSSubscriptionDefinition 中的 SubscriptionDefinition。</span><span class="sxs-lookup"><span data-stu-id="9e587-126">Microsoft.Azure.Commands.SubscriptionDefinition.Models.PSSubscriptionDefinition</span></span>

## <span data-ttu-id="9e587-127">筆記</span><span class="sxs-lookup"><span data-stu-id="9e587-127">NOTES</span></span>

## <span data-ttu-id="9e587-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e587-128">RELATED LINKS</span></span>

