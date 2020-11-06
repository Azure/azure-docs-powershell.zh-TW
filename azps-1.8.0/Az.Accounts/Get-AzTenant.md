---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-aztenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
ms.openlocfilehash: 7764b9c1226d86e44631ed3114fffde5bddc21f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611732"
---
# <span data-ttu-id="599b8-101">Get-AzTenant</span><span class="sxs-lookup"><span data-stu-id="599b8-101">Get-AzTenant</span></span>

## <span data-ttu-id="599b8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="599b8-102">SYNOPSIS</span></span>
<span data-ttu-id="599b8-103">取得目前使用者的授權承租人。</span><span class="sxs-lookup"><span data-stu-id="599b8-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="599b8-104">句法</span><span class="sxs-lookup"><span data-stu-id="599b8-104">SYNTAX</span></span>

```
Get-AzTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="599b8-105">說明</span><span class="sxs-lookup"><span data-stu-id="599b8-105">DESCRIPTION</span></span>
<span data-ttu-id="599b8-106">Get-AzTenant Cmdlet 會取得目前使用者的授權承租人。</span><span class="sxs-lookup"><span data-stu-id="599b8-106">The Get-AzTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="599b8-107">示例</span><span class="sxs-lookup"><span data-stu-id="599b8-107">EXAMPLES</span></span>

### <span data-ttu-id="599b8-108">範例1：取得所有承租人</span><span class="sxs-lookup"><span data-stu-id="599b8-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant

Id                                   Directory
--                                   ---------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx microsoft.com
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy microsoft.com
```

<span data-ttu-id="599b8-109">此範例說明如何取得 Azure 帳戶的所有授權租使用者。</span><span class="sxs-lookup"><span data-stu-id="599b8-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="599b8-110">範例2：取得特定的租使用者</span><span class="sxs-lookup"><span data-stu-id="599b8-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Directory
--                                   ---------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx microsoft.com
```

<span data-ttu-id="599b8-111">此範例說明如何取得 Azure 帳戶的特定授權租使用者。</span><span class="sxs-lookup"><span data-stu-id="599b8-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="599b8-112">參數</span><span class="sxs-lookup"><span data-stu-id="599b8-112">PARAMETERS</span></span>

### <span data-ttu-id="599b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="599b8-113">-DefaultProfile</span></span>
<span data-ttu-id="599b8-114">用於與 azure 進行通訊的認證、租使用者與訂閱</span><span class="sxs-lookup"><span data-stu-id="599b8-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="599b8-115">-TenantId</span><span class="sxs-lookup"><span data-stu-id="599b8-115">-TenantId</span></span>
<span data-ttu-id="599b8-116">指定此 Cmdlet 取得的租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="599b8-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="599b8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="599b8-117">CommonParameters</span></span>
<span data-ttu-id="599b8-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="599b8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="599b8-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="599b8-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="599b8-120">輸入</span><span class="sxs-lookup"><span data-stu-id="599b8-120">INPUTS</span></span>

### <span data-ttu-id="599b8-121">System.object</span><span class="sxs-lookup"><span data-stu-id="599b8-121">System.String</span></span>

## <span data-ttu-id="599b8-122">輸出</span><span class="sxs-lookup"><span data-stu-id="599b8-122">OUTPUTS</span></span>

### <span data-ttu-id="599b8-123">PSAzureTenant 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="599b8-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="599b8-124">筆記</span><span class="sxs-lookup"><span data-stu-id="599b8-124">NOTES</span></span>

## <span data-ttu-id="599b8-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="599b8-125">RELATED LINKS</span></span>
