---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: d05499ded326787b9930574872dd0681f773d1c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912461"
---
# <span data-ttu-id="fb8aa-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="fb8aa-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="fb8aa-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fb8aa-102">SYNOPSIS</span></span>
<span data-ttu-id="fb8aa-103">取得註冊帳戶。</span><span class="sxs-lookup"><span data-stu-id="fb8aa-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="fb8aa-104">語法</span><span class="sxs-lookup"><span data-stu-id="fb8aa-104">SYNTAX</span></span>

### <span data-ttu-id="fb8aa-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="fb8aa-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb8aa-106">單</span><span class="sxs-lookup"><span data-stu-id="fb8aa-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb8aa-107">描述</span><span class="sxs-lookup"><span data-stu-id="fb8aa-107">DESCRIPTION</span></span>
<span data-ttu-id="fb8aa-108">**Get-AzEnrollmentAccount** Cmdlet 會取得註冊帳戶。</span><span class="sxs-lookup"><span data-stu-id="fb8aa-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="fb8aa-109">例子</span><span class="sxs-lookup"><span data-stu-id="fb8aa-109">EXAMPLES</span></span>

### <span data-ttu-id="fb8aa-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="fb8aa-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="fb8aa-111">取得所有可用的註冊帳戶。</span><span class="sxs-lookup"><span data-stu-id="fb8aa-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="fb8aa-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="fb8aa-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="fb8aa-113">取得具有指定物件識別碼的註冊帳戶。</span><span class="sxs-lookup"><span data-stu-id="fb8aa-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="fb8aa-114">參數</span><span class="sxs-lookup"><span data-stu-id="fb8aa-114">PARAMETERS</span></span>

### <span data-ttu-id="fb8aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb8aa-115">-DefaultProfile</span></span>
<span data-ttu-id="fb8aa-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="fb8aa-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb8aa-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="fb8aa-117">-ObjectId</span></span>
<span data-ttu-id="fb8aa-118">要取得之特定註冊帳戶的 ObjectId。</span><span class="sxs-lookup"><span data-stu-id="fb8aa-118">ObjectId of a specific enrollment account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Single
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb8aa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb8aa-119">CommonParameters</span></span>
<span data-ttu-id="fb8aa-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fb8aa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb8aa-121">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="fb8aa-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb8aa-122">輸入</span><span class="sxs-lookup"><span data-stu-id="fb8aa-122">INPUTS</span></span>

### <span data-ttu-id="fb8aa-123">沒有</span><span class="sxs-lookup"><span data-stu-id="fb8aa-123">None</span></span>

## <span data-ttu-id="fb8aa-124">輸出</span><span class="sxs-lookup"><span data-stu-id="fb8aa-124">OUTPUTS</span></span>

### <span data-ttu-id="fb8aa-125">Microsoft.Azure.Commands.Billing.models.PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="fb8aa-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="fb8aa-126">筆記</span><span class="sxs-lookup"><span data-stu-id="fb8aa-126">NOTES</span></span>

## <span data-ttu-id="fb8aa-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb8aa-127">RELATED LINKS</span></span>
