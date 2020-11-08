---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
ms.openlocfilehash: 48ae8b87671e52abe4d109025048fe1e4aeca117
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138630"
---
# <span data-ttu-id="14be5-101">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="14be5-101">New-AzStorageAccountManagementPolicyFilter</span></span>

## <span data-ttu-id="14be5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="14be5-102">SYNOPSIS</span></span>
<span data-ttu-id="14be5-103">建立 ManagementPolicy 規則篩選物件，可在新的-AzStorageAccountManagementPolicyRule 中使用。</span><span class="sxs-lookup"><span data-stu-id="14be5-103">Creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="14be5-104">句法</span><span class="sxs-lookup"><span data-stu-id="14be5-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyFilter [-PrefixMatch <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="14be5-105">說明</span><span class="sxs-lookup"><span data-stu-id="14be5-105">DESCRIPTION</span></span>
<span data-ttu-id="14be5-106">**新的 AzStorageAccountManagementPolicyFilter** Cmdlet 會建立 ManagementPolicy 規則篩選物件，可在新的-AzStorageAccountManagementPolicyRule 中使用。</span><span class="sxs-lookup"><span data-stu-id="14be5-106">The **New-AzStorageAccountManagementPolicyFilter** cmdlet creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="14be5-107">示例</span><span class="sxs-lookup"><span data-stu-id="14be5-107">EXAMPLES</span></span>

### <span data-ttu-id="14be5-108">範例1：建立 ManagementPolicy 規則篩選物件，然後將它新增到管理原則規則，並設定為儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="14be5-108">Example 1: Creates a ManagementPolicy rule filter object, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter -PrefixMatch blobprefix1,blobprefix2
PS C:\>$filter 

PrefixMatch                BlobTypes  
-----------                ---------  
{blobprefix1, blobprefix2} {blockBlob}

PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="14be5-109">這個命令會建立 ManagementPolicy 規則篩選物件。</span><span class="sxs-lookup"><span data-stu-id="14be5-109">This command create a ManagementPolicy rule filter object.</span></span> <span data-ttu-id="14be5-110">然後將它新增到管理原則規則，並設定為儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="14be5-110">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="14be5-111">參數</span><span class="sxs-lookup"><span data-stu-id="14be5-111">PARAMETERS</span></span>

### <span data-ttu-id="14be5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14be5-112">-DefaultProfile</span></span>
<span data-ttu-id="14be5-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="14be5-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14be5-114">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="14be5-114">-PrefixMatch</span></span>
<span data-ttu-id="14be5-115">要相符的首碼字串陣列。</span><span class="sxs-lookup"><span data-stu-id="14be5-115">An array of strings for prefixes to be match.</span></span>
<span data-ttu-id="14be5-116">前置詞字串必須以容器名稱開頭。</span><span class="sxs-lookup"><span data-stu-id="14be5-116">A prefix string must start with a container name.</span></span>

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

### <span data-ttu-id="14be5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14be5-117">CommonParameters</span></span>
<span data-ttu-id="14be5-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="14be5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14be5-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="14be5-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14be5-120">輸入</span><span class="sxs-lookup"><span data-stu-id="14be5-120">INPUTS</span></span>

### <span data-ttu-id="14be5-121">所有</span><span class="sxs-lookup"><span data-stu-id="14be5-121">None</span></span>

## <span data-ttu-id="14be5-122">輸出</span><span class="sxs-lookup"><span data-stu-id="14be5-122">OUTPUTS</span></span>

### <span data-ttu-id="14be5-123">PSManagementPolicyRuleFilter 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="14be5-123">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span></span>

## <span data-ttu-id="14be5-124">筆記</span><span class="sxs-lookup"><span data-stu-id="14be5-124">NOTES</span></span>

## <span data-ttu-id="14be5-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="14be5-125">RELATED LINKS</span></span>
