---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: ''
schema: 2.0.0
ms.openlocfilehash: 552b1e638034cf0cec5825b742af4984b688cec3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443440"
---
# <span data-ttu-id="b3ed2-101">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b3ed2-101">Get-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="b3ed2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b3ed2-102">SYNOPSIS</span></span>
<span data-ttu-id="b3ed2-103">取得 Azure 儲存空間佇列的儲存存取原則或原則。</span><span class="sxs-lookup"><span data-stu-id="b3ed2-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="b3ed2-104">句法</span><span class="sxs-lookup"><span data-stu-id="b3ed2-104">SYNTAX</span></span>

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3ed2-105">說明</span><span class="sxs-lookup"><span data-stu-id="b3ed2-105">DESCRIPTION</span></span>
<span data-ttu-id="b3ed2-106">**AzureStorageQueueStoredAccessPolicy** Cmdlet 會列出 Azure 儲存空間佇列的已儲存存取原則或原則。</span><span class="sxs-lookup"><span data-stu-id="b3ed2-106">The **Get-AzureStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="b3ed2-107">示例</span><span class="sxs-lookup"><span data-stu-id="b3ed2-107">EXAMPLES</span></span>

### <span data-ttu-id="b3ed2-108">範例1：在佇列中取得儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="b3ed2-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="b3ed2-109">這個命令會在名為 MyQueue 的儲存佇列中取得名為 Policy12 的存取原則。</span><span class="sxs-lookup"><span data-stu-id="b3ed2-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="b3ed2-110">範例2：取得佇列中所有已儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="b3ed2-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="b3ed2-111">這個命令會取得名為 MyQueue 的佇列中所有已儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="b3ed2-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="b3ed2-112">參數</span><span class="sxs-lookup"><span data-stu-id="b3ed2-112">PARAMETERS</span></span>

### <span data-ttu-id="b3ed2-113">-內容</span><span class="sxs-lookup"><span data-stu-id="b3ed2-113">-Context</span></span>
<span data-ttu-id="b3ed2-114">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="b3ed2-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="b3ed2-115">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3ed2-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b3ed2-116">-原則</span><span class="sxs-lookup"><span data-stu-id="b3ed2-116">-Policy</span></span>
<span data-ttu-id="b3ed2-117">指定儲存的存取原則，包括此共用存取簽名 (SAS) 權杖的許可權。</span><span class="sxs-lookup"><span data-stu-id="b3ed2-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="b3ed2-118">-佇列</span><span class="sxs-lookup"><span data-stu-id="b3ed2-118">-Queue</span></span>
<span data-ttu-id="b3ed2-119">指定 Azure 儲存空間佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="b3ed2-119">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="b3ed2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3ed2-120">CommonParameters</span></span>
<span data-ttu-id="b3ed2-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b3ed2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3ed2-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b3ed2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3ed2-123">輸入</span><span class="sxs-lookup"><span data-stu-id="b3ed2-123">INPUTS</span></span>

## <span data-ttu-id="b3ed2-124">輸出</span><span class="sxs-lookup"><span data-stu-id="b3ed2-124">OUTPUTS</span></span>

## <span data-ttu-id="b3ed2-125">筆記</span><span class="sxs-lookup"><span data-stu-id="b3ed2-125">NOTES</span></span>

## <span data-ttu-id="b3ed2-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3ed2-126">RELATED LINKS</span></span>

[<span data-ttu-id="b3ed2-127">新-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b3ed2-127">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="b3ed2-128">移除-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b3ed2-128">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="b3ed2-129">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b3ed2-129">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="b3ed2-130">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="b3ed2-130">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


