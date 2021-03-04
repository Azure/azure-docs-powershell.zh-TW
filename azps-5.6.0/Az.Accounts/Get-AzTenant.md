---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-aztenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
ms.openlocfilehash: 4ef371f26eeca71edda42a6aca5e7d5ad28fe753
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902681"
---
# <span data-ttu-id="ddc11-101">Get-AzTenant</span><span class="sxs-lookup"><span data-stu-id="ddc11-101">Get-AzTenant</span></span>

## <span data-ttu-id="ddc11-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ddc11-102">SYNOPSIS</span></span>
<span data-ttu-id="ddc11-103">為目前使用者獲得授權租使用者。</span><span class="sxs-lookup"><span data-stu-id="ddc11-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="ddc11-104">語法</span><span class="sxs-lookup"><span data-stu-id="ddc11-104">SYNTAX</span></span>

```
Get-AzTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddc11-105">描述</span><span class="sxs-lookup"><span data-stu-id="ddc11-105">DESCRIPTION</span></span>
<span data-ttu-id="ddc11-106">此Get-AzTenant Cmdlet 會為目前使用者授權租使用者。</span><span class="sxs-lookup"><span data-stu-id="ddc11-106">The Get-AzTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="ddc11-107">例子</span><span class="sxs-lookup"><span data-stu-id="ddc11-107">EXAMPLES</span></span>

### <span data-ttu-id="ddc11-108">範例 1：取得所有租使用者</span><span class="sxs-lookup"><span data-stu-id="ddc11-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy Testhost    Home     testhost.onmicrosoft.com
```

<span data-ttu-id="ddc11-109">此範例顯示如何取得 Azure 帳戶的所有授權租使用者。</span><span class="sxs-lookup"><span data-stu-id="ddc11-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="ddc11-110">範例 2：取得特定租使用者</span><span class="sxs-lookup"><span data-stu-id="ddc11-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
```

<span data-ttu-id="ddc11-111">此範例顯示如何取得 Azure 帳戶的特定授權租使用者。</span><span class="sxs-lookup"><span data-stu-id="ddc11-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="ddc11-112">參數</span><span class="sxs-lookup"><span data-stu-id="ddc11-112">PARAMETERS</span></span>

### <span data-ttu-id="ddc11-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddc11-113">-DefaultProfile</span></span>
<span data-ttu-id="ddc11-114">用於與 Azure 通訊的認證、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="ddc11-114">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc11-115">-TenantId</span><span class="sxs-lookup"><span data-stu-id="ddc11-115">-TenantId</span></span>
<span data-ttu-id="ddc11-116">指定此 Cmdlet 所獲得之租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="ddc11-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Domain, Tenant

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc11-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddc11-117">CommonParameters</span></span>
<span data-ttu-id="ddc11-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ddc11-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddc11-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ddc11-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddc11-120">輸入</span><span class="sxs-lookup"><span data-stu-id="ddc11-120">INPUTS</span></span>

### <span data-ttu-id="ddc11-121">System.String</span><span class="sxs-lookup"><span data-stu-id="ddc11-121">System.String</span></span>

## <span data-ttu-id="ddc11-122">輸出</span><span class="sxs-lookup"><span data-stu-id="ddc11-122">OUTPUTS</span></span>

### <span data-ttu-id="ddc11-123">Microsoft.Azure.Commands.Profile.models.PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="ddc11-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="ddc11-124">筆記</span><span class="sxs-lookup"><span data-stu-id="ddc11-124">NOTES</span></span>

## <span data-ttu-id="ddc11-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="ddc11-125">RELATED LINKS</span></span>
