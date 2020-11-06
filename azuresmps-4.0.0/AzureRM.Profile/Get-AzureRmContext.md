---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 914b75e3952f7841aaf3ff505f51f7b4ebdc6044
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442823"
---
# <span data-ttu-id="ba887-101">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="ba887-101">Get-AzureRmContext</span></span>

## <span data-ttu-id="ba887-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ba887-102">SYNOPSIS</span></span>
<span data-ttu-id="ba887-103">取得用來驗證 Azure 資源管理器要求的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ba887-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="ba887-104">句法</span><span class="sxs-lookup"><span data-stu-id="ba887-104">SYNTAX</span></span>

```
Get-AzureRmContext [<CommonParameters>]
```

## <span data-ttu-id="ba887-105">說明</span><span class="sxs-lookup"><span data-stu-id="ba887-105">DESCRIPTION</span></span>
<span data-ttu-id="ba887-106">Get-AzureRmContext Cmdlet 會取得目前用來驗證 Azure 資源管理器要求的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ba887-106">The Get-AzureRmContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>

<span data-ttu-id="ba887-107">這個 Cmdlet 會取得 Active Directory 帳戶、Active Directory 租使用者、Azure 訂閱及目標 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="ba887-107">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="ba887-108">Azure 資源管理器 Cmdlet 會在進行 Azure 資源管理員要求時預設使用這些設定。</span><span class="sxs-lookup"><span data-stu-id="ba887-108">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="ba887-109">示例</span><span class="sxs-lookup"><span data-stu-id="ba887-109">EXAMPLES</span></span>

### <span data-ttu-id="ba887-110">範例1：取得目前的內容</span><span class="sxs-lookup"><span data-stu-id="ba887-110">Example 1: Getting the current context</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="ba887-111">在這個範例中，我們使用 AzureRmAccount，透過 Azure 訂閱登入我們的帳戶，然後透過呼叫 AzureRmCoNtext 來取得目前會話的內容。</span><span class="sxs-lookup"><span data-stu-id="ba887-111">In this example we are logging into our account with an Azure subscription using Add-AzureRmAccount, and then we are getting the context of the current session by calling Get-AzureRmContext.</span></span>

## <span data-ttu-id="ba887-112">參數</span><span class="sxs-lookup"><span data-stu-id="ba887-112">PARAMETERS</span></span>

### <span data-ttu-id="ba887-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba887-113">CommonParameters</span></span>
<span data-ttu-id="ba887-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ba887-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba887-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ba887-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba887-116">輸入</span><span class="sxs-lookup"><span data-stu-id="ba887-116">INPUTS</span></span>

## <span data-ttu-id="ba887-117">輸出</span><span class="sxs-lookup"><span data-stu-id="ba887-117">OUTPUTS</span></span>

### <span data-ttu-id="ba887-118">PSAzureCoNtext</span><span class="sxs-lookup"><span data-stu-id="ba887-118">PSAzureContext</span></span>
<span data-ttu-id="ba887-119">這個 Cmdlet 會傳回 Azure 資源管理器 Cmdlet 所使用的帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ba887-119">This cmdlet returns the account, tenant, and subscription used by Azure Resource Manager cmdlets.</span></span>

## <span data-ttu-id="ba887-120">筆記</span><span class="sxs-lookup"><span data-stu-id="ba887-120">NOTES</span></span>

## <span data-ttu-id="ba887-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba887-121">RELATED LINKS</span></span>

[<span data-ttu-id="ba887-122">Set-AzureRMCoNtext</span><span class="sxs-lookup"><span data-stu-id="ba887-122">Set-AzureRMContext</span></span>]()

