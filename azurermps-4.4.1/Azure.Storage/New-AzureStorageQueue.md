---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: f6a9aff40d2cff62e683439b3f28f9e782b2de05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457359"
---
# <span data-ttu-id="a8abf-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a8abf-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="a8abf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a8abf-102">SYNOPSIS</span></span>
<span data-ttu-id="a8abf-103">建立儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="a8abf-103">Creates a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8abf-104">句法</span><span class="sxs-lookup"><span data-stu-id="a8abf-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="a8abf-105">說明</span><span class="sxs-lookup"><span data-stu-id="a8abf-105">DESCRIPTION</span></span>
<span data-ttu-id="a8abf-106">**新的-AzureStorageQueue** Cmdlet 會在 Azure 中建立儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="a8abf-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="a8abf-107">示例</span><span class="sxs-lookup"><span data-stu-id="a8abf-107">EXAMPLES</span></span>

### <span data-ttu-id="a8abf-108">範例1：建立 Azure 儲存空間佇列</span><span class="sxs-lookup"><span data-stu-id="a8abf-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="a8abf-109">這個範例會建立名為 queueabc 的儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="a8abf-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="a8abf-110">範例2：建立多個 azure 存儲佇列</span><span class="sxs-lookup"><span data-stu-id="a8abf-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="a8abf-111">這個範例會建立多個儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="a8abf-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="a8abf-112">它會使用 .NET 字串類別的 Split 方法，然後傳送管線上的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8abf-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="a8abf-113">參數</span><span class="sxs-lookup"><span data-stu-id="a8abf-113">PARAMETERS</span></span>

### <span data-ttu-id="a8abf-114">-內容</span><span class="sxs-lookup"><span data-stu-id="a8abf-114">-Context</span></span>
<span data-ttu-id="a8abf-115">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="a8abf-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="a8abf-116">您可以使用 New-AzureStorageContext Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="a8abf-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a8abf-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="a8abf-117">-Name</span></span>
<span data-ttu-id="a8abf-118">指定佇列的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8abf-118">Specifies a name for the queue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8abf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8abf-119">CommonParameters</span></span>
<span data-ttu-id="a8abf-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a8abf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8abf-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a8abf-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8abf-122">輸入</span><span class="sxs-lookup"><span data-stu-id="a8abf-122">INPUTS</span></span>

### <span data-ttu-id="a8abf-123">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="a8abf-123">IStorageContext</span></span>

<span data-ttu-id="a8abf-124">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="a8abf-124">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="a8abf-125">字串</span><span class="sxs-lookup"><span data-stu-id="a8abf-125">String</span></span>

<span data-ttu-id="a8abf-126">形參 "Name" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="a8abf-126">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="a8abf-127">輸出</span><span class="sxs-lookup"><span data-stu-id="a8abf-127">OUTPUTS</span></span>

### <span data-ttu-id="a8abf-128">AzureStorageQueue WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="a8abf-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="a8abf-129">筆記</span><span class="sxs-lookup"><span data-stu-id="a8abf-129">NOTES</span></span>

## <span data-ttu-id="a8abf-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="a8abf-130">RELATED LINKS</span></span>

[<span data-ttu-id="a8abf-131">AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a8abf-131">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="a8abf-132">移除-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a8abf-132">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


