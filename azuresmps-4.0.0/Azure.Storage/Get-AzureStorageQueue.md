---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 11a8ffe26a65bf2ecabab7807d8e54bc23b629fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443443"
---
# <span data-ttu-id="d8473-101">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="d8473-101">Get-AzureStorageQueue</span></span>

## <span data-ttu-id="d8473-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d8473-102">SYNOPSIS</span></span>
<span data-ttu-id="d8473-103">列出 [儲存佇列]。</span><span class="sxs-lookup"><span data-stu-id="d8473-103">Lists storage queues.</span></span>

## <span data-ttu-id="d8473-104">句法</span><span class="sxs-lookup"><span data-stu-id="d8473-104">SYNTAX</span></span>

### <span data-ttu-id="d8473-105">QueueName (預設) </span><span class="sxs-lookup"><span data-stu-id="d8473-105">QueueName (Default)</span></span>
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="d8473-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="d8473-106">QueuePrefix</span></span>
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="d8473-107">說明</span><span class="sxs-lookup"><span data-stu-id="d8473-107">DESCRIPTION</span></span>
<span data-ttu-id="d8473-108">**AzureStorageQueue** Cmdlet 會列出與 Azure 儲存空間帳戶相關聯的儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="d8473-108">The **Get-AzureStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="d8473-109">示例</span><span class="sxs-lookup"><span data-stu-id="d8473-109">EXAMPLES</span></span>

### <span data-ttu-id="d8473-110">範例1：列出所有 Azure 儲存空間佇列</span><span class="sxs-lookup"><span data-stu-id="d8473-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue
```

<span data-ttu-id="d8473-111">這個命令會取得目前儲存空間帳戶的所有儲存佇列清單。</span><span class="sxs-lookup"><span data-stu-id="d8473-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="d8473-112">範例2：使用萬用字元列出 Azure 儲存空間佇列</span><span class="sxs-lookup"><span data-stu-id="d8473-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

<span data-ttu-id="d8473-113">這個命令使用萬用字元來取得名稱以 queue 開頭的儲存佇列清單。</span><span class="sxs-lookup"><span data-stu-id="d8473-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="d8473-114">範例3：使用佇列名稱首碼列出 Azure 儲存空間佇列</span><span class="sxs-lookup"><span data-stu-id="d8473-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

<span data-ttu-id="d8473-115">這個範例使用 *Prefix* 參數來取得名稱以 queue 開頭的儲存佇列清單。</span><span class="sxs-lookup"><span data-stu-id="d8473-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="d8473-116">參數</span><span class="sxs-lookup"><span data-stu-id="d8473-116">PARAMETERS</span></span>

### <span data-ttu-id="d8473-117">-內容</span><span class="sxs-lookup"><span data-stu-id="d8473-117">-Context</span></span>
<span data-ttu-id="d8473-118">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="d8473-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="d8473-119">您可以使用 **新的 AzureStorageCoNtext** Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="d8473-119">You can create it by using the **New-AzureStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="d8473-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="d8473-120">-Name</span></span>
<span data-ttu-id="d8473-121">指定名稱。</span><span class="sxs-lookup"><span data-stu-id="d8473-121">Specifies a name.</span></span>
<span data-ttu-id="d8473-122">如果沒有指定名稱，則 Cmdlet 會取得所有佇列的清單。</span><span class="sxs-lookup"><span data-stu-id="d8473-122">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="d8473-123">如果指定完整或部分名稱，則 Cmdlet 會取得符合名稱模式的所有佇列。</span><span class="sxs-lookup"><span data-stu-id="d8473-123">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

```yaml
Type: String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8473-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="d8473-124">-Prefix</span></span>
<span data-ttu-id="d8473-125">指定要取得的佇列名稱中所用的首碼。</span><span class="sxs-lookup"><span data-stu-id="d8473-125">Specifies a prefix used in the name of the queues you want to get.</span></span>

```yaml
Type: String
Parameter Sets: QueuePrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8473-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8473-126">CommonParameters</span></span>
<span data-ttu-id="d8473-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d8473-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8473-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d8473-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8473-129">輸入</span><span class="sxs-lookup"><span data-stu-id="d8473-129">INPUTS</span></span>

## <span data-ttu-id="d8473-130">輸出</span><span class="sxs-lookup"><span data-stu-id="d8473-130">OUTPUTS</span></span>

## <span data-ttu-id="d8473-131">筆記</span><span class="sxs-lookup"><span data-stu-id="d8473-131">NOTES</span></span>

## <span data-ttu-id="d8473-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8473-132">RELATED LINKS</span></span>

[<span data-ttu-id="d8473-133">新-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="d8473-133">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)

[<span data-ttu-id="d8473-134">移除-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="d8473-134">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


