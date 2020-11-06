---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76876cb76e65c913401d62fc7f08b3cb8b5626c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443087"
---
# <span data-ttu-id="3d8fe-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="3d8fe-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="3d8fe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3d8fe-102">SYNOPSIS</span></span>
<span data-ttu-id="3d8fe-103">建立儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="3d8fe-103">Creates a storage queue.</span></span>

## <span data-ttu-id="3d8fe-104">句法</span><span class="sxs-lookup"><span data-stu-id="3d8fe-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="3d8fe-105">說明</span><span class="sxs-lookup"><span data-stu-id="3d8fe-105">DESCRIPTION</span></span>
<span data-ttu-id="3d8fe-106">**新的-AzureStorageQueue** Cmdlet 會在 Azure 中建立儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="3d8fe-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="3d8fe-107">示例</span><span class="sxs-lookup"><span data-stu-id="3d8fe-107">EXAMPLES</span></span>

### <span data-ttu-id="3d8fe-108">範例1：建立 Azure 儲存空間佇列</span><span class="sxs-lookup"><span data-stu-id="3d8fe-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="3d8fe-109">這個範例會建立名為 queueabc 的儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="3d8fe-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="3d8fe-110">範例2：建立多個 azure 存儲佇列</span><span class="sxs-lookup"><span data-stu-id="3d8fe-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="3d8fe-111">這個範例會建立多個儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="3d8fe-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="3d8fe-112">它會使用 .NET 字串類別的 Split 方法，然後傳送管線上的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d8fe-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="3d8fe-113">參數</span><span class="sxs-lookup"><span data-stu-id="3d8fe-113">PARAMETERS</span></span>

### <span data-ttu-id="3d8fe-114">-內容</span><span class="sxs-lookup"><span data-stu-id="3d8fe-114">-Context</span></span>
<span data-ttu-id="3d8fe-115">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="3d8fe-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="3d8fe-116">您可以使用 New-AzureStorageContext Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="3d8fe-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3d8fe-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="3d8fe-117">-Name</span></span>
<span data-ttu-id="3d8fe-118">指定佇列的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d8fe-118">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="3d8fe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d8fe-119">CommonParameters</span></span>
<span data-ttu-id="3d8fe-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3d8fe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d8fe-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3d8fe-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d8fe-122">輸入</span><span class="sxs-lookup"><span data-stu-id="3d8fe-122">INPUTS</span></span>

## <span data-ttu-id="3d8fe-123">輸出</span><span class="sxs-lookup"><span data-stu-id="3d8fe-123">OUTPUTS</span></span>

## <span data-ttu-id="3d8fe-124">筆記</span><span class="sxs-lookup"><span data-stu-id="3d8fe-124">NOTES</span></span>

## <span data-ttu-id="3d8fe-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="3d8fe-125">RELATED LINKS</span></span>

[<span data-ttu-id="3d8fe-126">AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="3d8fe-126">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="3d8fe-127">移除-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="3d8fe-127">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


