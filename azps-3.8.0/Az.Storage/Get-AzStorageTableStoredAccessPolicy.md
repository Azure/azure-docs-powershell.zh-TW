---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: b17a294392ca4336d4a96e5d136ad4e321eb45a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958219"
---
# <span data-ttu-id="aa058-101">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aa058-101">Get-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="aa058-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aa058-102">SYNOPSIS</span></span>
<span data-ttu-id="aa058-103">取得 Azure 儲存空間資料表的儲存存取原則或原則。</span><span class="sxs-lookup"><span data-stu-id="aa058-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="aa058-104">句法</span><span class="sxs-lookup"><span data-stu-id="aa058-104">SYNTAX</span></span>

```
Get-AzStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa058-105">說明</span><span class="sxs-lookup"><span data-stu-id="aa058-105">DESCRIPTION</span></span>
<span data-ttu-id="aa058-106">**AzStorageTableStoredAccessPolicy** Cmdlet 會列出 Azure 儲存空間資料表的儲存存取原則或原則。</span><span class="sxs-lookup"><span data-stu-id="aa058-106">The **Get-AzStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="aa058-107">示例</span><span class="sxs-lookup"><span data-stu-id="aa058-107">EXAMPLES</span></span>

### <span data-ttu-id="aa058-108">範例1：在儲存空間資料表中取得儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="aa058-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="aa058-109">這個命令會在名為 Table02 的儲存空間資料表中取得名為 Policy50 的存取原則。</span><span class="sxs-lookup"><span data-stu-id="aa058-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="aa058-110">範例2：取得儲存空間資料表中所有已儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="aa058-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="aa058-111">這個命令會取得名為 Table02 的資料表中的所有存取原則。</span><span class="sxs-lookup"><span data-stu-id="aa058-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="aa058-112">參數</span><span class="sxs-lookup"><span data-stu-id="aa058-112">PARAMETERS</span></span>

### <span data-ttu-id="aa058-113">-內容</span><span class="sxs-lookup"><span data-stu-id="aa058-113">-Context</span></span>
<span data-ttu-id="aa058-114">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="aa058-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="aa058-115">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aa058-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="aa058-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa058-116">-DefaultProfile</span></span>
<span data-ttu-id="aa058-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="aa058-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa058-118">-原則</span><span class="sxs-lookup"><span data-stu-id="aa058-118">-Policy</span></span>
<span data-ttu-id="aa058-119">指定儲存的存取原則，包括此共用存取簽名 (SAS) 權杖的許可權。</span><span class="sxs-lookup"><span data-stu-id="aa058-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="aa058-120">-資料表</span><span class="sxs-lookup"><span data-stu-id="aa058-120">-Table</span></span>
<span data-ttu-id="aa058-121">指定 Azure 儲存空間資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="aa058-121">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="aa058-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa058-122">CommonParameters</span></span>
<span data-ttu-id="aa058-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aa058-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa058-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aa058-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa058-125">輸入</span><span class="sxs-lookup"><span data-stu-id="aa058-125">INPUTS</span></span>

### <span data-ttu-id="aa058-126">System.object</span><span class="sxs-lookup"><span data-stu-id="aa058-126">System.String</span></span>

### <span data-ttu-id="aa058-127">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="aa058-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="aa058-128">輸出</span><span class="sxs-lookup"><span data-stu-id="aa058-128">OUTPUTS</span></span>

### <span data-ttu-id="aa058-129">[WindowsAzure] SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="aa058-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="aa058-130">筆記</span><span class="sxs-lookup"><span data-stu-id="aa058-130">NOTES</span></span>

## <span data-ttu-id="aa058-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="aa058-131">RELATED LINKS</span></span>

[<span data-ttu-id="aa058-132">新-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aa058-132">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="aa058-133">移除-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aa058-133">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="aa058-134">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aa058-134">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="aa058-135">新-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="aa058-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


