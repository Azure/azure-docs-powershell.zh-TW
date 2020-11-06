---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2cabb88c490c7fdea56fd5ffde280cfd55bc8f3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442816"
---
# <span data-ttu-id="7683a-101">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="7683a-101">Get-AzureRmTenant</span></span>

## <span data-ttu-id="7683a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7683a-102">SYNOPSIS</span></span>
<span data-ttu-id="7683a-103">取得目前使用者的授權承租人。</span><span class="sxs-lookup"><span data-stu-id="7683a-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="7683a-104">句法</span><span class="sxs-lookup"><span data-stu-id="7683a-104">SYNTAX</span></span>

```
Get-AzureRmTenant [[-TenantId] <String>] [<CommonParameters>]
```

## <span data-ttu-id="7683a-105">說明</span><span class="sxs-lookup"><span data-stu-id="7683a-105">DESCRIPTION</span></span>
<span data-ttu-id="7683a-106">Get-AzureRmTenant Cmdlet 會取得目前使用者的授權承租人。</span><span class="sxs-lookup"><span data-stu-id="7683a-106">The Get-AzureRmTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="7683a-107">示例</span><span class="sxs-lookup"><span data-stu-id="7683a-107">EXAMPLES</span></span>

### <span data-ttu-id="7683a-108">範例1：取得所有承租人</span><span class="sxs-lookup"><span data-stu-id="7683a-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com

TenantId : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Domain   : microsoft.com
```

<span data-ttu-id="7683a-109">此範例說明如何取得 Azure 帳戶的所有授權租使用者。</span><span class="sxs-lookup"><span data-stu-id="7683a-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="7683a-110">範例2：取得特定的租使用者</span><span class="sxs-lookup"><span data-stu-id="7683a-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com
```

<span data-ttu-id="7683a-111">此範例說明如何取得 Azure 帳戶的特定授權租使用者。</span><span class="sxs-lookup"><span data-stu-id="7683a-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="7683a-112">參數</span><span class="sxs-lookup"><span data-stu-id="7683a-112">PARAMETERS</span></span>

### <span data-ttu-id="7683a-113">-TenantId</span><span class="sxs-lookup"><span data-stu-id="7683a-113">-TenantId</span></span>
<span data-ttu-id="7683a-114">指定此 Cmdlet 取得的租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="7683a-114">Specifies the ID of the tenant that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Domain, Tenant

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7683a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7683a-115">CommonParameters</span></span>
<span data-ttu-id="7683a-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7683a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7683a-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7683a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7683a-118">輸入</span><span class="sxs-lookup"><span data-stu-id="7683a-118">INPUTS</span></span>

## <span data-ttu-id="7683a-119">輸出</span><span class="sxs-lookup"><span data-stu-id="7683a-119">OUTPUTS</span></span>

### <span data-ttu-id="7683a-120">PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="7683a-120">PSAzureTenant</span></span>
<span data-ttu-id="7683a-121">這個 Cmdlet 會傳回授權給目前帳戶之租使用者的租使用者識別碼及相關聯的網域資訊。</span><span class="sxs-lookup"><span data-stu-id="7683a-121">This cmdlet returns the tenant ID and associated domain information for tenants authorized for the current account.</span></span>

## <span data-ttu-id="7683a-122">筆記</span><span class="sxs-lookup"><span data-stu-id="7683a-122">NOTES</span></span>

## <span data-ttu-id="7683a-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="7683a-123">RELATED LINKS</span></span>

