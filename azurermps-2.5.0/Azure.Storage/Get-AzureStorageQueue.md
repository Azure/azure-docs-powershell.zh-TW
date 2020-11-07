---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeue
schema: 2.0.0
ms.openlocfilehash: 59a035a7af56a333a1ef91b5ce4aa2d1afbe5086
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802653"
---
# <span data-ttu-id="e66c3-101">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="e66c3-101">Get-AzureStorageQueue</span></span>

## <span data-ttu-id="e66c3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e66c3-102">SYNOPSIS</span></span>
<span data-ttu-id="e66c3-103">列出 [儲存佇列]。</span><span class="sxs-lookup"><span data-stu-id="e66c3-103">Lists storage queues.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e66c3-104">句法</span><span class="sxs-lookup"><span data-stu-id="e66c3-104">SYNTAX</span></span>

### <span data-ttu-id="e66c3-105">QueueName (預設) </span><span class="sxs-lookup"><span data-stu-id="e66c3-105">QueueName (Default)</span></span>
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e66c3-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="e66c3-106">QueuePrefix</span></span>
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e66c3-107">說明</span><span class="sxs-lookup"><span data-stu-id="e66c3-107">DESCRIPTION</span></span>
<span data-ttu-id="e66c3-108">**AzureStorageQueue** Cmdlet 會列出與 Azure 儲存空間帳戶相關聯的儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="e66c3-108">The **Get-AzureStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="e66c3-109">示例</span><span class="sxs-lookup"><span data-stu-id="e66c3-109">EXAMPLES</span></span>

### <span data-ttu-id="e66c3-110">範例1：列出所有 Azure 儲存空間佇列</span><span class="sxs-lookup"><span data-stu-id="e66c3-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue
```

<span data-ttu-id="e66c3-111">這個命令會取得目前儲存空間帳戶的所有儲存佇列清單。</span><span class="sxs-lookup"><span data-stu-id="e66c3-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="e66c3-112">範例2：使用萬用字元列出 Azure 儲存空間佇列</span><span class="sxs-lookup"><span data-stu-id="e66c3-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

<span data-ttu-id="e66c3-113">這個命令使用萬用字元來取得名稱以 queue 開頭的儲存佇列清單。</span><span class="sxs-lookup"><span data-stu-id="e66c3-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="e66c3-114">範例3：使用佇列名稱首碼列出 Azure 儲存空間佇列</span><span class="sxs-lookup"><span data-stu-id="e66c3-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

<span data-ttu-id="e66c3-115">這個範例使用 *Prefix* 參數來取得名稱以 queue 開頭的儲存佇列清單。</span><span class="sxs-lookup"><span data-stu-id="e66c3-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="e66c3-116">參數</span><span class="sxs-lookup"><span data-stu-id="e66c3-116">PARAMETERS</span></span>

### <span data-ttu-id="e66c3-117">-內容</span><span class="sxs-lookup"><span data-stu-id="e66c3-117">-Context</span></span>
<span data-ttu-id="e66c3-118">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="e66c3-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="e66c3-119">您可以使用 **新的 AzureStorageCoNtext** Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="e66c3-119">You can create it by using the **New-AzureStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="e66c3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e66c3-120">-DefaultProfile</span></span>
<span data-ttu-id="e66c3-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e66c3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e66c3-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="e66c3-122">-Name</span></span>
<span data-ttu-id="e66c3-123">指定名稱。</span><span class="sxs-lookup"><span data-stu-id="e66c3-123">Specifies a name.</span></span>
<span data-ttu-id="e66c3-124">如果沒有指定名稱，則 Cmdlet 會取得所有佇列的清單。</span><span class="sxs-lookup"><span data-stu-id="e66c3-124">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="e66c3-125">如果指定完整或部分名稱，則 Cmdlet 會取得符合名稱模式的所有佇列。</span><span class="sxs-lookup"><span data-stu-id="e66c3-125">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e66c3-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="e66c3-126">-Prefix</span></span>
<span data-ttu-id="e66c3-127">指定要取得的佇列名稱中所用的首碼。</span><span class="sxs-lookup"><span data-stu-id="e66c3-127">Specifies a prefix used in the name of the queues you want to get.</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e66c3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e66c3-128">CommonParameters</span></span>
<span data-ttu-id="e66c3-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e66c3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e66c3-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e66c3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e66c3-131">輸入</span><span class="sxs-lookup"><span data-stu-id="e66c3-131">INPUTS</span></span>

### <span data-ttu-id="e66c3-132">System.object</span><span class="sxs-lookup"><span data-stu-id="e66c3-132">System.String</span></span>

### <span data-ttu-id="e66c3-133">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="e66c3-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e66c3-134">輸出</span><span class="sxs-lookup"><span data-stu-id="e66c3-134">OUTPUTS</span></span>

### <span data-ttu-id="e66c3-135">AzureStorageQueue WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="e66c3-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="e66c3-136">筆記</span><span class="sxs-lookup"><span data-stu-id="e66c3-136">NOTES</span></span>

## <span data-ttu-id="e66c3-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="e66c3-137">RELATED LINKS</span></span>

[<span data-ttu-id="e66c3-138">新-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="e66c3-138">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)

[<span data-ttu-id="e66c3-139">移除-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="e66c3-139">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


