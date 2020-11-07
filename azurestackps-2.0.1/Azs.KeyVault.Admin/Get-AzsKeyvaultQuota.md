---
external help file: ''
Module Name: Azs.KeyVault.Admin
online version: https://docs.microsoft.com/powershell/module/azs.keyvault.admin/get-azskeyvaultquota
schema: 2.0.0
ms.openlocfilehash: 813e0e7dc2535b3c7cd424e55ff924c380d84e2f
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966662"
---
# <span data-ttu-id="f8a33-101">Get-AzsKeyvaultQuota</span><span class="sxs-lookup"><span data-stu-id="f8a33-101">Get-AzsKeyvaultQuota</span></span>

## <span data-ttu-id="f8a33-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f8a33-102">SYNOPSIS</span></span>
<span data-ttu-id="f8a33-103">取得位置上 KeyVault 的所有配額物件的清單。</span><span class="sxs-lookup"><span data-stu-id="f8a33-103">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="f8a33-104">句法</span><span class="sxs-lookup"><span data-stu-id="f8a33-104">SYNTAX</span></span>

```
Get-AzsKeyvaultQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8a33-105">說明</span><span class="sxs-lookup"><span data-stu-id="f8a33-105">DESCRIPTION</span></span>
<span data-ttu-id="f8a33-106">取得位置上 KeyVault 的所有配額物件的清單。</span><span class="sxs-lookup"><span data-stu-id="f8a33-106">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="f8a33-107">示例</span><span class="sxs-lookup"><span data-stu-id="f8a33-107">EXAMPLES</span></span>

### <span data-ttu-id="f8a33-108">範例1：</span><span class="sxs-lookup"><span data-stu-id="f8a33-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsKeyVaultQuota

Location  Name                Type
--------  ----                ----
northwest northwest/Unlimited Microsoft.KeyVault.Admin/locations/quotas

```

<span data-ttu-id="f8a33-109">取得位置上 KeyVault 的所有配額物件的清單。</span><span class="sxs-lookup"><span data-stu-id="f8a33-109">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="f8a33-110">參數</span><span class="sxs-lookup"><span data-stu-id="f8a33-110">PARAMETERS</span></span>

### <span data-ttu-id="f8a33-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8a33-111">-DefaultProfile</span></span>
<span data-ttu-id="f8a33-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f8a33-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8a33-113">-位置</span><span class="sxs-lookup"><span data-stu-id="f8a33-113">-Location</span></span>
<span data-ttu-id="f8a33-114">配額的位置。</span><span class="sxs-lookup"><span data-stu-id="f8a33-114">The location of the quota.</span></span>

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

### <span data-ttu-id="f8a33-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f8a33-115">-SubscriptionId</span></span>
<span data-ttu-id="f8a33-116">可唯一識別 Microsoft Azure 訂閱的訂閱認證。[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="f8a33-116">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f8a33-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8a33-117">CommonParameters</span></span>
<span data-ttu-id="f8a33-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f8a33-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8a33-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f8a33-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8a33-120">輸入</span><span class="sxs-lookup"><span data-stu-id="f8a33-120">INPUTS</span></span>

## <span data-ttu-id="f8a33-121">輸出</span><span class="sxs-lookup"><span data-stu-id="f8a33-121">OUTPUTS</span></span>

### <span data-ttu-id="f8a33-122">IQuota （KeyVaultAdmin）。 Api20170201Preview。</span><span class="sxs-lookup"><span data-stu-id="f8a33-122">Microsoft.Azure.PowerShell.Cmdlets.KeyVaultAdmin.Models.Api20170201Preview.IQuota</span></span>



## <span data-ttu-id="f8a33-123">筆記</span><span class="sxs-lookup"><span data-stu-id="f8a33-123">NOTES</span></span>

## <span data-ttu-id="f8a33-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8a33-124">RELATED LINKS</span></span>

