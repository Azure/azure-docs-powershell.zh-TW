---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: d76797f82a14c8efa2f9a3d6a77436fa2f8a1b68
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622889"
---
# <span data-ttu-id="f37b8-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="f37b8-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="f37b8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f37b8-102">SYNOPSIS</span></span>
<span data-ttu-id="f37b8-103">取得註冊帳戶。</span><span class="sxs-lookup"><span data-stu-id="f37b8-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="f37b8-104">句法</span><span class="sxs-lookup"><span data-stu-id="f37b8-104">SYNTAX</span></span>

### <span data-ttu-id="f37b8-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="f37b8-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f37b8-106">通過</span><span class="sxs-lookup"><span data-stu-id="f37b8-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f37b8-107">說明</span><span class="sxs-lookup"><span data-stu-id="f37b8-107">DESCRIPTION</span></span>
<span data-ttu-id="f37b8-108">**AzEnrollmentAccount** Cmdlet 會取得註冊帳戶。</span><span class="sxs-lookup"><span data-stu-id="f37b8-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="f37b8-109">示例</span><span class="sxs-lookup"><span data-stu-id="f37b8-109">EXAMPLES</span></span>

### <span data-ttu-id="f37b8-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f37b8-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="f37b8-111">取得所有可用的登記帳戶。</span><span class="sxs-lookup"><span data-stu-id="f37b8-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="f37b8-112">範例2</span><span class="sxs-lookup"><span data-stu-id="f37b8-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="f37b8-113">取得具有指定物件識別碼的登記帳戶。</span><span class="sxs-lookup"><span data-stu-id="f37b8-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="f37b8-114">參數</span><span class="sxs-lookup"><span data-stu-id="f37b8-114">PARAMETERS</span></span>

### <span data-ttu-id="f37b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f37b8-115">-DefaultProfile</span></span>
<span data-ttu-id="f37b8-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f37b8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f37b8-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f37b8-117">-ObjectId</span></span>
<span data-ttu-id="f37b8-118">要取得之特定註冊帳戶的 ObjectId。</span><span class="sxs-lookup"><span data-stu-id="f37b8-118">ObjectId of a specific enrollment account to get.</span></span>

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

### <span data-ttu-id="f37b8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f37b8-119">CommonParameters</span></span>
<span data-ttu-id="f37b8-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f37b8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f37b8-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f37b8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f37b8-122">輸入</span><span class="sxs-lookup"><span data-stu-id="f37b8-122">INPUTS</span></span>

### <span data-ttu-id="f37b8-123">所有</span><span class="sxs-lookup"><span data-stu-id="f37b8-123">None</span></span>

## <span data-ttu-id="f37b8-124">輸出</span><span class="sxs-lookup"><span data-stu-id="f37b8-124">OUTPUTS</span></span>

### <span data-ttu-id="f37b8-125">PSBillingPeriod 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f37b8-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="f37b8-126">筆記</span><span class="sxs-lookup"><span data-stu-id="f37b8-126">NOTES</span></span>

## <span data-ttu-id="f37b8-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="f37b8-127">RELATED LINKS</span></span>
