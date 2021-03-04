---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
ms.openlocfilehash: 2361196f2e8b904f2403aaf06118122931e83afd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913646"
---
# <span data-ttu-id="b97b4-101">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="b97b4-101">Get-AzStorageQueue</span></span>

## <span data-ttu-id="b97b4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b97b4-102">SYNOPSIS</span></span>
<span data-ttu-id="b97b4-103">列出儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="b97b4-103">Lists storage queues.</span></span>

## <span data-ttu-id="b97b4-104">語法</span><span class="sxs-lookup"><span data-stu-id="b97b4-104">SYNTAX</span></span>

### <span data-ttu-id="b97b4-105">QueueName (預設) </span><span class="sxs-lookup"><span data-stu-id="b97b4-105">QueueName (Default)</span></span>
```
Get-AzStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b97b4-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="b97b4-106">QueuePrefix</span></span>
```
Get-AzStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b97b4-107">描述</span><span class="sxs-lookup"><span data-stu-id="b97b4-107">DESCRIPTION</span></span>
<span data-ttu-id="b97b4-108">**Get-AzStorageQueue** Cmdlet 會列出與 Azure 儲存體帳戶相關聯的儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="b97b4-108">The **Get-AzStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="b97b4-109">例子</span><span class="sxs-lookup"><span data-stu-id="b97b4-109">EXAMPLES</span></span>

### <span data-ttu-id="b97b4-110">範例 1：列出所有 Azure 儲存佇列</span><span class="sxs-lookup"><span data-stu-id="b97b4-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzStorageQueue
```

<span data-ttu-id="b97b4-111">此命令會獲得目前儲存空間帳戶的所有儲存佇列清單。</span><span class="sxs-lookup"><span data-stu-id="b97b4-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="b97b4-112">範例 2：使用萬用字元列出 Azure 儲存佇列</span><span class="sxs-lookup"><span data-stu-id="b97b4-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzStorageQueue -Name queue*
```

<span data-ttu-id="b97b4-113">此命令使用萬用字元來取得名稱以佇列開頭的儲存佇列清單。</span><span class="sxs-lookup"><span data-stu-id="b97b4-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="b97b4-114">範例 3：使用佇列名稱首碼列出 Azure 儲存佇列</span><span class="sxs-lookup"><span data-stu-id="b97b4-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzStorageQueue -Prefix "queue"
```

<span data-ttu-id="b97b4-115">此範例使用 *首碼* 參數取得名稱以佇列開頭的儲存佇列清單。</span><span class="sxs-lookup"><span data-stu-id="b97b4-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="b97b4-116">參數</span><span class="sxs-lookup"><span data-stu-id="b97b4-116">PARAMETERS</span></span>

### <span data-ttu-id="b97b4-117">-內容</span><span class="sxs-lookup"><span data-stu-id="b97b4-117">-Context</span></span>
<span data-ttu-id="b97b4-118">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="b97b4-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="b97b4-119">您可以使用 **New-AzStorageCoNtext** Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="b97b4-119">You can create it by using the **New-AzStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="b97b4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b97b4-120">-DefaultProfile</span></span>
<span data-ttu-id="b97b4-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b97b4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b97b4-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="b97b4-122">-Name</span></span>
<span data-ttu-id="b97b4-123">指定名稱。</span><span class="sxs-lookup"><span data-stu-id="b97b4-123">Specifies a name.</span></span>
<span data-ttu-id="b97b4-124">如果未指定名稱，Cmdlet 會獲得所有佇列的清單。</span><span class="sxs-lookup"><span data-stu-id="b97b4-124">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="b97b4-125">如果指定完整或部分名稱，Cmdlet 會獲得符合名稱模式的所有佇列。</span><span class="sxs-lookup"><span data-stu-id="b97b4-125">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

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

### <span data-ttu-id="b97b4-126">-首碼</span><span class="sxs-lookup"><span data-stu-id="b97b4-126">-Prefix</span></span>
<span data-ttu-id="b97b4-127">指定您想要取得之佇列名稱中使用的首碼。</span><span class="sxs-lookup"><span data-stu-id="b97b4-127">Specifies a prefix used in the name of the queues you want to get.</span></span>

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

### <span data-ttu-id="b97b4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b97b4-128">CommonParameters</span></span>
<span data-ttu-id="b97b4-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b97b4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b97b4-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b97b4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b97b4-131">輸入</span><span class="sxs-lookup"><span data-stu-id="b97b4-131">INPUTS</span></span>

### <span data-ttu-id="b97b4-132">System.String</span><span class="sxs-lookup"><span data-stu-id="b97b4-132">System.String</span></span>

### <span data-ttu-id="b97b4-133">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="b97b4-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b97b4-134">輸出</span><span class="sxs-lookup"><span data-stu-id="b97b4-134">OUTPUTS</span></span>

### <span data-ttu-id="b97b4-135">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="b97b4-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="b97b4-136">筆記</span><span class="sxs-lookup"><span data-stu-id="b97b4-136">NOTES</span></span>

## <span data-ttu-id="b97b4-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="b97b4-137">RELATED LINKS</span></span>

[<span data-ttu-id="b97b4-138">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="b97b4-138">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)

[<span data-ttu-id="b97b4-139">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="b97b4-139">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


