---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 2de23408aef9d9af4ebd23eb520261760883cf3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912990"
---
# <span data-ttu-id="60ca1-101">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="60ca1-101">Get-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="60ca1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="60ca1-102">SYNOPSIS</span></span>
<span data-ttu-id="60ca1-103">取得 Azure 儲存資料表的儲存存取策略或策略。</span><span class="sxs-lookup"><span data-stu-id="60ca1-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="60ca1-104">語法</span><span class="sxs-lookup"><span data-stu-id="60ca1-104">SYNTAX</span></span>

```
Get-AzStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60ca1-105">描述</span><span class="sxs-lookup"><span data-stu-id="60ca1-105">DESCRIPTION</span></span>
<span data-ttu-id="60ca1-106">**Get-AzStorageTableStoredAccessPolicy** Cmdlet 會列出 Azure 儲存資料表的儲存存取策略或策略。</span><span class="sxs-lookup"><span data-stu-id="60ca1-106">The **Get-AzStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="60ca1-107">例子</span><span class="sxs-lookup"><span data-stu-id="60ca1-107">EXAMPLES</span></span>

### <span data-ttu-id="60ca1-108">範例 1：取得儲存資料表中的儲存存取策略</span><span class="sxs-lookup"><span data-stu-id="60ca1-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="60ca1-109">此命令會取得名為 Table02 的儲存資料表中名為 Policy50 的存取策略。</span><span class="sxs-lookup"><span data-stu-id="60ca1-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="60ca1-110">範例 2：取得儲存資料表中所有儲存的存取策略</span><span class="sxs-lookup"><span data-stu-id="60ca1-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="60ca1-111">此命令會取得資料表中名為 Table02 的所有存取策略。</span><span class="sxs-lookup"><span data-stu-id="60ca1-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="60ca1-112">參數</span><span class="sxs-lookup"><span data-stu-id="60ca1-112">PARAMETERS</span></span>

### <span data-ttu-id="60ca1-113">-內容</span><span class="sxs-lookup"><span data-stu-id="60ca1-113">-Context</span></span>
<span data-ttu-id="60ca1-114">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="60ca1-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="60ca1-115">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="60ca1-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60ca1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60ca1-116">-DefaultProfile</span></span>
<span data-ttu-id="60ca1-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="60ca1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ca1-118">-策略</span><span class="sxs-lookup"><span data-stu-id="60ca1-118">-Policy</span></span>
<span data-ttu-id="60ca1-119">指定儲存的存取策略，包括此共用存取簽章的許可權 (SAS) 權杖。</span><span class="sxs-lookup"><span data-stu-id="60ca1-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60ca1-120">-表格</span><span class="sxs-lookup"><span data-stu-id="60ca1-120">-Table</span></span>
<span data-ttu-id="60ca1-121">指定 Azure 儲存資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="60ca1-121">Specifies the Azure storage table name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60ca1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60ca1-122">CommonParameters</span></span>
<span data-ttu-id="60ca1-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="60ca1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60ca1-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="60ca1-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60ca1-125">輸入</span><span class="sxs-lookup"><span data-stu-id="60ca1-125">INPUTS</span></span>

### <span data-ttu-id="60ca1-126">System.String</span><span class="sxs-lookup"><span data-stu-id="60ca1-126">System.String</span></span>

### <span data-ttu-id="60ca1-127">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="60ca1-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="60ca1-128">輸出</span><span class="sxs-lookup"><span data-stu-id="60ca1-128">OUTPUTS</span></span>

### <span data-ttu-id="60ca1-129">Microsoft.WindowsAzure.storage.Table.SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="60ca1-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="60ca1-130">筆記</span><span class="sxs-lookup"><span data-stu-id="60ca1-130">NOTES</span></span>

## <span data-ttu-id="60ca1-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="60ca1-131">RELATED LINKS</span></span>

[<span data-ttu-id="60ca1-132">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="60ca1-132">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="60ca1-133">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="60ca1-133">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="60ca1-134">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="60ca1-134">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="60ca1-135">New-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="60ca1-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


