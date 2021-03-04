---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
ms.openlocfilehash: 40a2420803197b21bb9f0f8d20b771482b4e694b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915113"
---
# <span data-ttu-id="06c2d-101">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="06c2d-101">New-AzStorageAccountManagementPolicyFilter</span></span>

## <span data-ttu-id="06c2d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="06c2d-102">SYNOPSIS</span></span>
<span data-ttu-id="06c2d-103">建立 ManagementPolicy 規則篩選物件，可用於 New-AzStorageAccountManagementPolicyRule。</span><span class="sxs-lookup"><span data-stu-id="06c2d-103">Creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="06c2d-104">語法</span><span class="sxs-lookup"><span data-stu-id="06c2d-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyFilter [-PrefixMatch <String[]>] [-BlobType <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06c2d-105">描述</span><span class="sxs-lookup"><span data-stu-id="06c2d-105">DESCRIPTION</span></span>
<span data-ttu-id="06c2d-106">**New-AzStorageAccountManagementPolicyFilter** Cmdlet 會建立 ManagementPolicy 規則篩選物件，可用於 New-AzStorageAccountManagementPolicyRule。</span><span class="sxs-lookup"><span data-stu-id="06c2d-106">The **New-AzStorageAccountManagementPolicyFilter** cmdlet creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="06c2d-107">例子</span><span class="sxs-lookup"><span data-stu-id="06c2d-107">EXAMPLES</span></span>

### <span data-ttu-id="06c2d-108">範例 1：建立 ManagementPolicy 規則篩選物件，然後將它新增到管理原則規則，並設定為儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="06c2d-108">Example 1: Creates a ManagementPolicy rule filter object, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter -PrefixMatch blobprefix1,blobprefix2 -BlobType appendBlob,blockBlob
PS C:\>$filter 

PrefixMatch                BlobTypes  
-----------                ---------  
{blobprefix1, blobprefix2} {appendBlob, blockBlob}

PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="06c2d-109">此命令會建立 ManagementPolicy 規則篩選物件。</span><span class="sxs-lookup"><span data-stu-id="06c2d-109">This command create a ManagementPolicy rule filter object.</span></span> <span data-ttu-id="06c2d-110">然後將它新增到管理原則規則，並設定為儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="06c2d-110">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="06c2d-111">參數</span><span class="sxs-lookup"><span data-stu-id="06c2d-111">PARAMETERS</span></span>

### <span data-ttu-id="06c2d-112">-BlobType</span><span class="sxs-lookup"><span data-stu-id="06c2d-112">-BlobType</span></span>
<span data-ttu-id="06c2d-113">Blob 類型要相符的字串陣列。</span><span class="sxs-lookup"><span data-stu-id="06c2d-113">An array of strings for blobtypes to be match.</span></span> <span data-ttu-id="06c2d-114">目前 blockBlob 支援所有分層和刪除動作。</span><span class="sxs-lookup"><span data-stu-id="06c2d-114">Currently blockBlob supports all tiering and delete actions.</span></span> <span data-ttu-id="06c2d-115">只支援追加Blob 的刪除動作。</span><span class="sxs-lookup"><span data-stu-id="06c2d-115">Only delete actions are supported for appendBlob.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: blockBlob, appendBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06c2d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06c2d-116">-DefaultProfile</span></span>
<span data-ttu-id="06c2d-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="06c2d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06c2d-118">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="06c2d-118">-PrefixMatch</span></span>
<span data-ttu-id="06c2d-119">首碼要相符的字串陣列。</span><span class="sxs-lookup"><span data-stu-id="06c2d-119">An array of strings for prefixes to be match.</span></span>
<span data-ttu-id="06c2d-120">首碼字串必須以容器名稱開頭。</span><span class="sxs-lookup"><span data-stu-id="06c2d-120">A prefix string must start with a container name.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06c2d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06c2d-121">CommonParameters</span></span>
<span data-ttu-id="06c2d-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="06c2d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06c2d-123">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="06c2d-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06c2d-124">輸入</span><span class="sxs-lookup"><span data-stu-id="06c2d-124">INPUTS</span></span>

### <span data-ttu-id="06c2d-125">沒有</span><span class="sxs-lookup"><span data-stu-id="06c2d-125">None</span></span>

## <span data-ttu-id="06c2d-126">輸出</span><span class="sxs-lookup"><span data-stu-id="06c2d-126">OUTPUTS</span></span>

### <span data-ttu-id="06c2d-127">Microsoft.Azure.Commands.management.storage.models.PSManagementPolicyRuleFilter</span><span class="sxs-lookup"><span data-stu-id="06c2d-127">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span></span>

## <span data-ttu-id="06c2d-128">筆記</span><span class="sxs-lookup"><span data-stu-id="06c2d-128">NOTES</span></span>

## <span data-ttu-id="06c2d-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="06c2d-129">RELATED LINKS</span></span>
