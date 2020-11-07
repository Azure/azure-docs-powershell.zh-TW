---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueueStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 78815aaa29c46e455f24ce0daac167b2806b6c20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624863"
---
# <span data-ttu-id="ff683-101">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ff683-101">Get-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="ff683-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ff683-102">SYNOPSIS</span></span>
<span data-ttu-id="ff683-103">取得 Azure 儲存空間佇列的儲存存取原則或原則。</span><span class="sxs-lookup"><span data-stu-id="ff683-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff683-104">句法</span><span class="sxs-lookup"><span data-stu-id="ff683-104">SYNTAX</span></span>

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff683-105">說明</span><span class="sxs-lookup"><span data-stu-id="ff683-105">DESCRIPTION</span></span>
<span data-ttu-id="ff683-106">**AzureStorageQueueStoredAccessPolicy** Cmdlet 會列出 Azure 儲存空間佇列的已儲存存取原則或原則。</span><span class="sxs-lookup"><span data-stu-id="ff683-106">The **Get-AzureStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="ff683-107">示例</span><span class="sxs-lookup"><span data-stu-id="ff683-107">EXAMPLES</span></span>

### <span data-ttu-id="ff683-108">範例1：在佇列中取得儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="ff683-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="ff683-109">這個命令會在名為 MyQueue 的儲存佇列中取得名為 Policy12 的存取原則。</span><span class="sxs-lookup"><span data-stu-id="ff683-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="ff683-110">範例2：取得佇列中所有已儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="ff683-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="ff683-111">這個命令會取得名為 MyQueue 的佇列中所有已儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="ff683-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="ff683-112">參數</span><span class="sxs-lookup"><span data-stu-id="ff683-112">PARAMETERS</span></span>

### <span data-ttu-id="ff683-113">-內容</span><span class="sxs-lookup"><span data-stu-id="ff683-113">-Context</span></span>
<span data-ttu-id="ff683-114">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="ff683-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ff683-115">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ff683-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff683-116">-原則</span><span class="sxs-lookup"><span data-stu-id="ff683-116">-Policy</span></span>
<span data-ttu-id="ff683-117">指定儲存的存取原則，包括此共用存取簽名 (SAS) 權杖的許可權。</span><span class="sxs-lookup"><span data-stu-id="ff683-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff683-118">-佇列</span><span class="sxs-lookup"><span data-stu-id="ff683-118">-Queue</span></span>
<span data-ttu-id="ff683-119">指定 Azure 儲存空間佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="ff683-119">Specifies the Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff683-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff683-120">CommonParameters</span></span>
<span data-ttu-id="ff683-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ff683-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff683-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ff683-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff683-123">輸入</span><span class="sxs-lookup"><span data-stu-id="ff683-123">INPUTS</span></span>

### <span data-ttu-id="ff683-124">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="ff683-124">IStorageContext</span></span>

<span data-ttu-id="ff683-125">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ff683-125">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="ff683-126">字串</span><span class="sxs-lookup"><span data-stu-id="ff683-126">String</span></span>

<span data-ttu-id="ff683-127">形參 "Queue" 接受來自管線的 "String" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ff683-127">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="ff683-128">輸出</span><span class="sxs-lookup"><span data-stu-id="ff683-128">OUTPUTS</span></span>

### <span data-ttu-id="ff683-129">[WindowsAzure] SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="ff683-129">Microsoft.WindowsAzure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="ff683-130">筆記</span><span class="sxs-lookup"><span data-stu-id="ff683-130">NOTES</span></span>

## <span data-ttu-id="ff683-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="ff683-131">RELATED LINKS</span></span>

[<span data-ttu-id="ff683-132">新-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ff683-132">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ff683-133">移除-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ff683-133">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ff683-134">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ff683-134">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ff683-135">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="ff683-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


