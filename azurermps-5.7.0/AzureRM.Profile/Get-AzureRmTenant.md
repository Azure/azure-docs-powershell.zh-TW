---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermtenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
ms.openlocfilehash: 7d9687877e3a27d175719a7a7b9ec6c78a529e52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452128"
---
# <span data-ttu-id="10c0f-101">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="10c0f-101">Get-AzureRmTenant</span></span>

## <span data-ttu-id="10c0f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="10c0f-102">SYNOPSIS</span></span>
<span data-ttu-id="10c0f-103">取得目前使用者的授權承租人。</span><span class="sxs-lookup"><span data-stu-id="10c0f-103">Gets tenants that are authorized for the current user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10c0f-104">句法</span><span class="sxs-lookup"><span data-stu-id="10c0f-104">SYNTAX</span></span>

```
Get-AzureRmTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10c0f-105">說明</span><span class="sxs-lookup"><span data-stu-id="10c0f-105">DESCRIPTION</span></span>
<span data-ttu-id="10c0f-106">Get-AzureRmTenant Cmdlet 會取得目前使用者的授權承租人。</span><span class="sxs-lookup"><span data-stu-id="10c0f-106">The Get-AzureRmTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="10c0f-107">示例</span><span class="sxs-lookup"><span data-stu-id="10c0f-107">EXAMPLES</span></span>

### <span data-ttu-id="10c0f-108">範例1：取得所有承租人</span><span class="sxs-lookup"><span data-stu-id="10c0f-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmTenant

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com

TenantId : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Domain   : microsoft.com
```

<span data-ttu-id="10c0f-109">此範例說明如何取得 Azure 帳戶的所有授權租使用者。</span><span class="sxs-lookup"><span data-stu-id="10c0f-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="10c0f-110">範例2：取得特定的租使用者</span><span class="sxs-lookup"><span data-stu-id="10c0f-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com
```

<span data-ttu-id="10c0f-111">此範例說明如何取得 Azure 帳戶的特定授權租使用者。</span><span class="sxs-lookup"><span data-stu-id="10c0f-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="10c0f-112">參數</span><span class="sxs-lookup"><span data-stu-id="10c0f-112">PARAMETERS</span></span>

### <span data-ttu-id="10c0f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10c0f-113">-DefaultProfile</span></span>
<span data-ttu-id="10c0f-114">用於與 azure 進行通訊的認證、租使用者與訂閱</span><span class="sxs-lookup"><span data-stu-id="10c0f-114">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10c0f-115">-TenantId</span><span class="sxs-lookup"><span data-stu-id="10c0f-115">-TenantId</span></span>
<span data-ttu-id="10c0f-116">指定此 Cmdlet 取得的租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="10c0f-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="10c0f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10c0f-117">CommonParameters</span></span>
<span data-ttu-id="10c0f-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="10c0f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10c0f-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="10c0f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10c0f-120">輸入</span><span class="sxs-lookup"><span data-stu-id="10c0f-120">INPUTS</span></span>

### <span data-ttu-id="10c0f-121">所有</span><span class="sxs-lookup"><span data-stu-id="10c0f-121">None</span></span>
<span data-ttu-id="10c0f-122">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="10c0f-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="10c0f-123">輸出</span><span class="sxs-lookup"><span data-stu-id="10c0f-123">OUTPUTS</span></span>

### <span data-ttu-id="10c0f-124">PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="10c0f-124">PSAzureTenant</span></span>
<span data-ttu-id="10c0f-125">這個 Cmdlet 會傳回授權給目前帳戶之租使用者的租使用者識別碼及相關聯的網域資訊。</span><span class="sxs-lookup"><span data-stu-id="10c0f-125">This cmdlet returns the tenant ID and associated domain information for tenants authorized for the current account.</span></span>

## <span data-ttu-id="10c0f-126">筆記</span><span class="sxs-lookup"><span data-stu-id="10c0f-126">NOTES</span></span>

## <span data-ttu-id="10c0f-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="10c0f-127">RELATED LINKS</span></span>

