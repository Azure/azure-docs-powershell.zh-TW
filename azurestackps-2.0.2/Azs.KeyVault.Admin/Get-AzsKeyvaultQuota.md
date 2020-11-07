---
external help file: ''
Module Name: Azs.KeyVault.Admin
online version: https://docs.microsoft.com/powershell/module/azs.keyvault.admin/get-azskeyvaultquota
schema: 2.0.0
ms.openlocfilehash: 813e0e7dc2535b3c7cd424e55ff924c380d84e2f
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968548"
---
# <span data-ttu-id="7ce26-101">Get-AzsKeyvaultQuota</span><span class="sxs-lookup"><span data-stu-id="7ce26-101">Get-AzsKeyvaultQuota</span></span>

## <span data-ttu-id="7ce26-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7ce26-102">SYNOPSIS</span></span>
<span data-ttu-id="7ce26-103">取得位置上 KeyVault 的所有配額物件的清單。</span><span class="sxs-lookup"><span data-stu-id="7ce26-103">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="7ce26-104">句法</span><span class="sxs-lookup"><span data-stu-id="7ce26-104">SYNTAX</span></span>

```
Get-AzsKeyvaultQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ce26-105">說明</span><span class="sxs-lookup"><span data-stu-id="7ce26-105">DESCRIPTION</span></span>
<span data-ttu-id="7ce26-106">取得位置上 KeyVault 的所有配額物件的清單。</span><span class="sxs-lookup"><span data-stu-id="7ce26-106">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="7ce26-107">示例</span><span class="sxs-lookup"><span data-stu-id="7ce26-107">EXAMPLES</span></span>

### <span data-ttu-id="7ce26-108">範例1：</span><span class="sxs-lookup"><span data-stu-id="7ce26-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsKeyVaultQuota

Location  Name                Type
--------  ----                ----
northwest northwest/Unlimited Microsoft.KeyVault.Admin/locations/quotas

```

<span data-ttu-id="7ce26-109">取得位置上 KeyVault 的所有配額物件的清單。</span><span class="sxs-lookup"><span data-stu-id="7ce26-109">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="7ce26-110">參數</span><span class="sxs-lookup"><span data-stu-id="7ce26-110">PARAMETERS</span></span>

### <span data-ttu-id="7ce26-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ce26-111">-DefaultProfile</span></span>
<span data-ttu-id="7ce26-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7ce26-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ce26-113">-位置</span><span class="sxs-lookup"><span data-stu-id="7ce26-113">-Location</span></span>
<span data-ttu-id="7ce26-114">配額的位置。</span><span class="sxs-lookup"><span data-stu-id="7ce26-114">The location of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7ce26-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7ce26-115">-SubscriptionId</span></span>
<span data-ttu-id="7ce26-116">可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="7ce26-116">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7ce26-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ce26-117">CommonParameters</span></span>
<span data-ttu-id="7ce26-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7ce26-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ce26-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7ce26-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ce26-120">輸入</span><span class="sxs-lookup"><span data-stu-id="7ce26-120">INPUTS</span></span>

## <span data-ttu-id="7ce26-121">輸出</span><span class="sxs-lookup"><span data-stu-id="7ce26-121">OUTPUTS</span></span>

### <span data-ttu-id="7ce26-122">IQuota （KeyVaultAdmin）。 Api20170201Preview。</span><span class="sxs-lookup"><span data-stu-id="7ce26-122">Microsoft.Azure.PowerShell.Cmdlets.KeyVaultAdmin.Models.Api20170201Preview.IQuota</span></span>



## <span data-ttu-id="7ce26-123">筆記</span><span class="sxs-lookup"><span data-stu-id="7ce26-123">NOTES</span></span>

## <span data-ttu-id="7ce26-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="7ce26-124">RELATED LINKS</span></span>

