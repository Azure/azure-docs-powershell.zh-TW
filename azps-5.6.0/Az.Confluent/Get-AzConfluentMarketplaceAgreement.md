---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/get-azconfluentmarketplaceagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentMarketplaceAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentMarketplaceAgreement.md
ms.openlocfilehash: 72b60933ee2771278f1e225e4a022def55c3c03a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917073"
---
# <span data-ttu-id="39362-101">Get-AzConfluentMarketplaceAgreement</span><span class="sxs-lookup"><span data-stu-id="39362-101">Get-AzConfluentMarketplaceAgreement</span></span>

## <span data-ttu-id="39362-102">簡介</span><span class="sxs-lookup"><span data-stu-id="39362-102">SYNOPSIS</span></span>
<span data-ttu-id="39362-103">列出訂閱中的 Confluent Marketplace 協定。</span><span class="sxs-lookup"><span data-stu-id="39362-103">List Confluent marketplace agreements in the subscription.</span></span>

## <span data-ttu-id="39362-104">語法</span><span class="sxs-lookup"><span data-stu-id="39362-104">SYNTAX</span></span>

```
Get-AzConfluentMarketplaceAgreement [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="39362-105">描述</span><span class="sxs-lookup"><span data-stu-id="39362-105">DESCRIPTION</span></span>
<span data-ttu-id="39362-106">列出訂閱中的 Confluent Marketplace 協定。</span><span class="sxs-lookup"><span data-stu-id="39362-106">List Confluent marketplace agreements in the subscription.</span></span>

## <span data-ttu-id="39362-107">例子</span><span class="sxs-lookup"><span data-stu-id="39362-107">EXAMPLES</span></span>

### <span data-ttu-id="39362-108">範例 1：在訂閱下列出所有服務商場協定</span><span class="sxs-lookup"><span data-stu-id="39362-108">Example 1: List all confluent marketplace agreement under a subscription</span></span>
```powershell
PS C:\> Get-AzConfluentMarketplaceAgreement

Name        Type
----        ----
marketplace Microsoft.Confluent/agreements
confluent   Microsoft.Confluent/offertypes
```

<span data-ttu-id="39362-109">此命令會列出訂閱下的所有服務商場協定。</span><span class="sxs-lookup"><span data-stu-id="39362-109">This command lists all confluent marketplace agreement under a subscription.</span></span>

## <span data-ttu-id="39362-110">參數</span><span class="sxs-lookup"><span data-stu-id="39362-110">PARAMETERS</span></span>

### <span data-ttu-id="39362-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39362-111">-DefaultProfile</span></span>
<span data-ttu-id="39362-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="39362-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39362-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39362-113">-SubscriptionId</span></span>
<span data-ttu-id="39362-114">Microsoft Azure 訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="39362-114">Microsoft Azure subscription id</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39362-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39362-115">CommonParameters</span></span>
<span data-ttu-id="39362-116">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="39362-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39362-117">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39362-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39362-118">輸入</span><span class="sxs-lookup"><span data-stu-id="39362-118">INPUTS</span></span>

## <span data-ttu-id="39362-119">輸出</span><span class="sxs-lookup"><span data-stu-id="39362-119">OUTPUTS</span></span>

### <span data-ttu-id="39362-120">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IConfluentAgreementResource</span><span class="sxs-lookup"><span data-stu-id="39362-120">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IConfluentAgreementResource</span></span>

## <span data-ttu-id="39362-121">筆記</span><span class="sxs-lookup"><span data-stu-id="39362-121">NOTES</span></span>

<span data-ttu-id="39362-122">別名</span><span class="sxs-lookup"><span data-stu-id="39362-122">ALIASES</span></span>

## <span data-ttu-id="39362-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="39362-123">RELATED LINKS</span></span>

