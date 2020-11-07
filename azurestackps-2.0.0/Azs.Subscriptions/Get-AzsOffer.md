---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azsoffer
schema: 2.0.0
ms.openlocfilehash: 7b2fcb224486915e78bdd90a84941ac0207a45c3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796410"
---
# <span data-ttu-id="889f9-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="889f9-101">Get-AzsOffer</span></span>

## <span data-ttu-id="889f9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="889f9-102">SYNOPSIS</span></span>
<span data-ttu-id="889f9-103">取得根提供者的公開優惠清單。</span><span class="sxs-lookup"><span data-stu-id="889f9-103">Get the list of public offers for the root provider.</span></span>

## <span data-ttu-id="889f9-104">句法</span><span class="sxs-lookup"><span data-stu-id="889f9-104">SYNTAX</span></span>

```
Get-AzsOffer [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="889f9-105">說明</span><span class="sxs-lookup"><span data-stu-id="889f9-105">DESCRIPTION</span></span>
<span data-ttu-id="889f9-106">取得根提供者的公開優惠清單。</span><span class="sxs-lookup"><span data-stu-id="889f9-106">Get the list of public offers for the root provider.</span></span>

## <span data-ttu-id="889f9-107">示例</span><span class="sxs-lookup"><span data-stu-id="889f9-107">EXAMPLES</span></span>

### <span data-ttu-id="889f9-108">範例1</span><span class="sxs-lookup"><span data-stu-id="889f9-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsOffer | fl *

Description : 
DisplayName : TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
Id          : /delegatedProviders/default/offers/TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
Name        : TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6

Description : 
DisplayName : TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
Id          : /delegatedProviders/default/offers/TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
Name        : TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
```

<span data-ttu-id="889f9-109">取得公開優惠清單</span><span class="sxs-lookup"><span data-stu-id="889f9-109">Get the list of public offers</span></span>

## <span data-ttu-id="889f9-110">參數</span><span class="sxs-lookup"><span data-stu-id="889f9-110">PARAMETERS</span></span>

### <span data-ttu-id="889f9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="889f9-111">-DefaultProfile</span></span>
<span data-ttu-id="889f9-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="889f9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="889f9-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="889f9-113">CommonParameters</span></span>
<span data-ttu-id="889f9-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="889f9-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="889f9-115">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="889f9-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="889f9-116">輸入</span><span class="sxs-lookup"><span data-stu-id="889f9-116">INPUTS</span></span>

## <span data-ttu-id="889f9-117">輸出</span><span class="sxs-lookup"><span data-stu-id="889f9-117">OUTPUTS</span></span>

### <span data-ttu-id="889f9-118">IOffer 中的 [Api20151101] （訂閱）。</span><span class="sxs-lookup"><span data-stu-id="889f9-118">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.IOffer</span></span>



## <span data-ttu-id="889f9-119">筆記</span><span class="sxs-lookup"><span data-stu-id="889f9-119">NOTES</span></span>

## <span data-ttu-id="889f9-120">相關連結</span><span class="sxs-lookup"><span data-stu-id="889f9-120">RELATED LINKS</span></span>

