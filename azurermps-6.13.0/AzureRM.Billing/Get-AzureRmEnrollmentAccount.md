---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
ms.openlocfilehash: d5d43a0aebcc553a230655d52399081548aae209
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625355"
---
# <span data-ttu-id="01ded-101">Get-AzureRmEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="01ded-101">Get-AzureRmEnrollmentAccount</span></span>

## <span data-ttu-id="01ded-102">摘要</span><span class="sxs-lookup"><span data-stu-id="01ded-102">SYNOPSIS</span></span>
<span data-ttu-id="01ded-103">取得註冊帳戶。</span><span class="sxs-lookup"><span data-stu-id="01ded-103">Get enrollment accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01ded-104">句法</span><span class="sxs-lookup"><span data-stu-id="01ded-104">SYNTAX</span></span>

### <span data-ttu-id="01ded-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="01ded-105">List (Default)</span></span>
```
Get-AzureRmEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01ded-106">通過</span><span class="sxs-lookup"><span data-stu-id="01ded-106">Single</span></span>
```
Get-AzureRmEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01ded-107">說明</span><span class="sxs-lookup"><span data-stu-id="01ded-107">DESCRIPTION</span></span>
<span data-ttu-id="01ded-108">**AzureRmEnrollmentAccount** Cmdlet 會取得註冊帳戶。</span><span class="sxs-lookup"><span data-stu-id="01ded-108">The **Get-AzureRmEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="01ded-109">示例</span><span class="sxs-lookup"><span data-stu-id="01ded-109">EXAMPLES</span></span>

### <span data-ttu-id="01ded-110">範例1</span><span class="sxs-lookup"><span data-stu-id="01ded-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="01ded-111">取得所有可用的登記帳戶。</span><span class="sxs-lookup"><span data-stu-id="01ded-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="01ded-112">範例2</span><span class="sxs-lookup"><span data-stu-id="01ded-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="01ded-113">取得具有指定物件識別碼的登記帳戶。</span><span class="sxs-lookup"><span data-stu-id="01ded-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="01ded-114">參數</span><span class="sxs-lookup"><span data-stu-id="01ded-114">PARAMETERS</span></span>

### <span data-ttu-id="01ded-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01ded-115">-DefaultProfile</span></span>
<span data-ttu-id="01ded-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="01ded-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01ded-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="01ded-117">-ObjectId</span></span>
<span data-ttu-id="01ded-118">要取得之特定註冊帳戶的 ObjectId。</span><span class="sxs-lookup"><span data-stu-id="01ded-118">ObjectId of a specific enrollment account to get.</span></span>

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

### <span data-ttu-id="01ded-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01ded-119">CommonParameters</span></span>
<span data-ttu-id="01ded-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="01ded-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01ded-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="01ded-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01ded-122">輸入</span><span class="sxs-lookup"><span data-stu-id="01ded-122">INPUTS</span></span>

### <span data-ttu-id="01ded-123">所有</span><span class="sxs-lookup"><span data-stu-id="01ded-123">None</span></span>

## <span data-ttu-id="01ded-124">輸出</span><span class="sxs-lookup"><span data-stu-id="01ded-124">OUTPUTS</span></span>

### <span data-ttu-id="01ded-125">PSBillingPeriod 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="01ded-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="01ded-126">筆記</span><span class="sxs-lookup"><span data-stu-id="01ded-126">NOTES</span></span>

## <span data-ttu-id="01ded-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="01ded-127">RELATED LINKS</span></span>
