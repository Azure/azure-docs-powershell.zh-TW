---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/powershell/module/az.managementpartner/get-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
ms.openlocfilehash: e09e63ed68ac87156fd03f73c992043b8a0271cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909693"
---
# <span data-ttu-id="c8ec8-101">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="c8ec8-101">Get-AzManagementPartner</span></span>

## <span data-ttu-id="c8ec8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c8ec8-102">SYNOPSIS</span></span>
<span data-ttu-id="c8ec8-103">從目前已驗證 (或) 的 MPN 識別碼中，獲得 Microsoft 合作夥伴網路。</span><span class="sxs-lookup"><span data-stu-id="c8ec8-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="c8ec8-104">語法</span><span class="sxs-lookup"><span data-stu-id="c8ec8-104">SYNTAX</span></span>

```
Get-AzManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8ec8-105">描述</span><span class="sxs-lookup"><span data-stu-id="c8ec8-105">DESCRIPTION</span></span>
<span data-ttu-id="c8ec8-106">從目前已驗證 (或) 的 MPN 識別碼中，獲得 Microsoft 合作夥伴網路。</span><span class="sxs-lookup"><span data-stu-id="c8ec8-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="c8ec8-107">例子</span><span class="sxs-lookup"><span data-stu-id="c8ec8-107">EXAMPLES</span></span>

### <span data-ttu-id="c8ec8-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="c8ec8-108">Example 1</span></span>
```powershell
PS C:\> Get-AzManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="c8ec8-109">取得目前的管理合作夥伴識別碼</span><span class="sxs-lookup"><span data-stu-id="c8ec8-109">Get the current management partner id</span></span>

### <span data-ttu-id="c8ec8-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="c8ec8-110">Example 2</span></span>
```powershell
PS C:\> Get-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="c8ec8-111">使用合作夥伴識別碼取得目前的管理合作夥伴識別碼，如果它們不相符，將會失敗</span><span class="sxs-lookup"><span data-stu-id="c8ec8-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="c8ec8-112">參數</span><span class="sxs-lookup"><span data-stu-id="c8ec8-112">PARAMETERS</span></span>

### <span data-ttu-id="c8ec8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8ec8-113">-DefaultProfile</span></span>
<span data-ttu-id="c8ec8-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c8ec8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8ec8-115">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="c8ec8-115">-PartnerId</span></span>
<span data-ttu-id="c8ec8-116">管理合作夥伴識別碼，為 6 位數號碼</span><span class="sxs-lookup"><span data-stu-id="c8ec8-116">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8ec8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8ec8-117">CommonParameters</span></span>
<span data-ttu-id="c8ec8-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c8ec8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8ec8-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c8ec8-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8ec8-120">輸入</span><span class="sxs-lookup"><span data-stu-id="c8ec8-120">INPUTS</span></span>

### <span data-ttu-id="c8ec8-121">沒有</span><span class="sxs-lookup"><span data-stu-id="c8ec8-121">None</span></span>

## <span data-ttu-id="c8ec8-122">輸出</span><span class="sxs-lookup"><span data-stu-id="c8ec8-122">OUTPUTS</span></span>

### <span data-ttu-id="c8ec8-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="c8ec8-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="c8ec8-124">筆記</span><span class="sxs-lookup"><span data-stu-id="c8ec8-124">NOTES</span></span>

## <span data-ttu-id="c8ec8-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8ec8-125">RELATED LINKS</span></span>

[<span data-ttu-id="c8ec8-126">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="c8ec8-126">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="c8ec8-127">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="c8ec8-127">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="c8ec8-128">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="c8ec8-128">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)