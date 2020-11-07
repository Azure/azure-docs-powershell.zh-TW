---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 0ec79b50d47a86b23e7c55e7277fe567ba46b9d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623947"
---
# <span data-ttu-id="3dcf9-101">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3dcf9-101">Get-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="3dcf9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3dcf9-102">SYNOPSIS</span></span>
<span data-ttu-id="3dcf9-103">取得 Azure 儲存空間資料表的儲存存取原則或原則。</span><span class="sxs-lookup"><span data-stu-id="3dcf9-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3dcf9-104">句法</span><span class="sxs-lookup"><span data-stu-id="3dcf9-104">SYNTAX</span></span>

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3dcf9-105">說明</span><span class="sxs-lookup"><span data-stu-id="3dcf9-105">DESCRIPTION</span></span>
<span data-ttu-id="3dcf9-106">**AzureStorageTableStoredAccessPolicy** Cmdlet 會列出 Azure 儲存空間資料表的儲存存取原則或原則。</span><span class="sxs-lookup"><span data-stu-id="3dcf9-106">The **Get-AzureStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="3dcf9-107">示例</span><span class="sxs-lookup"><span data-stu-id="3dcf9-107">EXAMPLES</span></span>

### <span data-ttu-id="3dcf9-108">範例1：在儲存空間資料表中取得儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="3dcf9-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="3dcf9-109">這個命令會在名為 Table02 的儲存空間資料表中取得名為 Policy50 的存取原則。</span><span class="sxs-lookup"><span data-stu-id="3dcf9-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="3dcf9-110">範例2：取得儲存空間資料表中所有已儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="3dcf9-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="3dcf9-111">這個命令會取得名為 Table02 的資料表中的所有存取原則。</span><span class="sxs-lookup"><span data-stu-id="3dcf9-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="3dcf9-112">參數</span><span class="sxs-lookup"><span data-stu-id="3dcf9-112">PARAMETERS</span></span>

### <span data-ttu-id="3dcf9-113">-內容</span><span class="sxs-lookup"><span data-stu-id="3dcf9-113">-Context</span></span>
<span data-ttu-id="3dcf9-114">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="3dcf9-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="3dcf9-115">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3dcf9-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3dcf9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dcf9-116">-DefaultProfile</span></span>
<span data-ttu-id="3dcf9-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3dcf9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dcf9-118">-原則</span><span class="sxs-lookup"><span data-stu-id="3dcf9-118">-Policy</span></span>
<span data-ttu-id="3dcf9-119">指定儲存的存取原則，包括此共用存取簽名 (SAS) 權杖的許可權。</span><span class="sxs-lookup"><span data-stu-id="3dcf9-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="3dcf9-120">-資料表</span><span class="sxs-lookup"><span data-stu-id="3dcf9-120">-Table</span></span>
<span data-ttu-id="3dcf9-121">指定 Azure 儲存空間資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="3dcf9-121">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="3dcf9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dcf9-122">CommonParameters</span></span>
<span data-ttu-id="3dcf9-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3dcf9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dcf9-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3dcf9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dcf9-125">輸入</span><span class="sxs-lookup"><span data-stu-id="3dcf9-125">INPUTS</span></span>

### <span data-ttu-id="3dcf9-126">System.object</span><span class="sxs-lookup"><span data-stu-id="3dcf9-126">System.String</span></span>

### <span data-ttu-id="3dcf9-127">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="3dcf9-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3dcf9-128">輸出</span><span class="sxs-lookup"><span data-stu-id="3dcf9-128">OUTPUTS</span></span>

### <span data-ttu-id="3dcf9-129">[WindowsAzure] SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="3dcf9-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="3dcf9-130">筆記</span><span class="sxs-lookup"><span data-stu-id="3dcf9-130">NOTES</span></span>

## <span data-ttu-id="3dcf9-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="3dcf9-131">RELATED LINKS</span></span>

[<span data-ttu-id="3dcf9-132">新-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3dcf9-132">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="3dcf9-133">移除-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3dcf9-133">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="3dcf9-134">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3dcf9-134">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="3dcf9-135">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="3dcf9-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


