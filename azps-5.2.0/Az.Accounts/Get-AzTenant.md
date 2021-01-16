---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-aztenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
ms.openlocfilehash: 936eb5bb7f49c2530a325b3bfa8c369b8f097711
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284531"
---
# <span data-ttu-id="24ae0-101">Get-AzTenant</span><span class="sxs-lookup"><span data-stu-id="24ae0-101">Get-AzTenant</span></span>

## <span data-ttu-id="24ae0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="24ae0-102">SYNOPSIS</span></span>
<span data-ttu-id="24ae0-103">取得目前使用者的授權承租人。</span><span class="sxs-lookup"><span data-stu-id="24ae0-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="24ae0-104">句法</span><span class="sxs-lookup"><span data-stu-id="24ae0-104">SYNTAX</span></span>

```
Get-AzTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24ae0-105">說明</span><span class="sxs-lookup"><span data-stu-id="24ae0-105">DESCRIPTION</span></span>
<span data-ttu-id="24ae0-106">Get-AzTenant Cmdlet 會取得目前使用者的授權承租人。</span><span class="sxs-lookup"><span data-stu-id="24ae0-106">The Get-AzTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="24ae0-107">示例</span><span class="sxs-lookup"><span data-stu-id="24ae0-107">EXAMPLES</span></span>

### <span data-ttu-id="24ae0-108">範例1：取得所有承租人</span><span class="sxs-lookup"><span data-stu-id="24ae0-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy Testhost    Home     testhost.onmicrosoft.com
```

<span data-ttu-id="24ae0-109">此範例說明如何取得 Azure 帳戶的所有授權租使用者。</span><span class="sxs-lookup"><span data-stu-id="24ae0-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="24ae0-110">範例2：取得特定的租使用者</span><span class="sxs-lookup"><span data-stu-id="24ae0-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
```

<span data-ttu-id="24ae0-111">此範例說明如何取得 Azure 帳戶的特定授權租使用者。</span><span class="sxs-lookup"><span data-stu-id="24ae0-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="24ae0-112">參數</span><span class="sxs-lookup"><span data-stu-id="24ae0-112">PARAMETERS</span></span>

### <span data-ttu-id="24ae0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24ae0-113">-DefaultProfile</span></span>
<span data-ttu-id="24ae0-114">用於與 azure 進行通訊的認證、租使用者與訂閱</span><span class="sxs-lookup"><span data-stu-id="24ae0-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24ae0-115">-TenantId</span><span class="sxs-lookup"><span data-stu-id="24ae0-115">-TenantId</span></span>
<span data-ttu-id="24ae0-116">指定此 Cmdlet 取得的租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="24ae0-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="24ae0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24ae0-117">CommonParameters</span></span>
<span data-ttu-id="24ae0-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="24ae0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24ae0-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="24ae0-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24ae0-120">輸入</span><span class="sxs-lookup"><span data-stu-id="24ae0-120">INPUTS</span></span>

### <span data-ttu-id="24ae0-121">System.object</span><span class="sxs-lookup"><span data-stu-id="24ae0-121">System.String</span></span>

## <span data-ttu-id="24ae0-122">輸出</span><span class="sxs-lookup"><span data-stu-id="24ae0-122">OUTPUTS</span></span>

### <span data-ttu-id="24ae0-123">PSAzureTenant 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="24ae0-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="24ae0-124">筆記</span><span class="sxs-lookup"><span data-stu-id="24ae0-124">NOTES</span></span>

## <span data-ttu-id="24ae0-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="24ae0-125">RELATED LINKS</span></span>
