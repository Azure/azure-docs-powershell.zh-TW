---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
ms.openlocfilehash: df4d31c1a90808e4d289cab60c5edf9785de1182
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93968966"
---
# <span data-ttu-id="435be-101">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="435be-101">Get-AzStorageQueue</span></span>

## <span data-ttu-id="435be-102">摘要</span><span class="sxs-lookup"><span data-stu-id="435be-102">SYNOPSIS</span></span>
<span data-ttu-id="435be-103">列出 [儲存佇列]。</span><span class="sxs-lookup"><span data-stu-id="435be-103">Lists storage queues.</span></span>

## <span data-ttu-id="435be-104">句法</span><span class="sxs-lookup"><span data-stu-id="435be-104">SYNTAX</span></span>

### <span data-ttu-id="435be-105">QueueName (預設) </span><span class="sxs-lookup"><span data-stu-id="435be-105">QueueName (Default)</span></span>
```
Get-AzStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="435be-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="435be-106">QueuePrefix</span></span>
```
Get-AzStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="435be-107">說明</span><span class="sxs-lookup"><span data-stu-id="435be-107">DESCRIPTION</span></span>
<span data-ttu-id="435be-108">**AzStorageQueue** Cmdlet 會列出與 Azure 儲存空間帳戶相關聯的儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="435be-108">The **Get-AzStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="435be-109">示例</span><span class="sxs-lookup"><span data-stu-id="435be-109">EXAMPLES</span></span>

### <span data-ttu-id="435be-110">範例1：列出所有 Azure 儲存空間佇列</span><span class="sxs-lookup"><span data-stu-id="435be-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzStorageQueue
```

<span data-ttu-id="435be-111">這個命令會取得目前儲存空間帳戶的所有儲存佇列清單。</span><span class="sxs-lookup"><span data-stu-id="435be-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="435be-112">範例2：使用萬用字元列出 Azure 儲存空間佇列</span><span class="sxs-lookup"><span data-stu-id="435be-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzStorageQueue -Name queue*
```

<span data-ttu-id="435be-113">這個命令使用萬用字元來取得名稱以 queue 開頭的儲存佇列清單。</span><span class="sxs-lookup"><span data-stu-id="435be-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="435be-114">範例3：使用佇列名稱首碼列出 Azure 儲存空間佇列</span><span class="sxs-lookup"><span data-stu-id="435be-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzStorageQueue -Prefix "queue"
```

<span data-ttu-id="435be-115">這個範例使用 *Prefix* 參數來取得名稱以 queue 開頭的儲存佇列清單。</span><span class="sxs-lookup"><span data-stu-id="435be-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="435be-116">參數</span><span class="sxs-lookup"><span data-stu-id="435be-116">PARAMETERS</span></span>

### <span data-ttu-id="435be-117">-內容</span><span class="sxs-lookup"><span data-stu-id="435be-117">-Context</span></span>
<span data-ttu-id="435be-118">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="435be-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="435be-119">您可以使用 **新的 AzStorageCoNtext** Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="435be-119">You can create it by using the **New-AzStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="435be-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="435be-120">-DefaultProfile</span></span>
<span data-ttu-id="435be-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="435be-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="435be-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="435be-122">-Name</span></span>
<span data-ttu-id="435be-123">指定名稱。</span><span class="sxs-lookup"><span data-stu-id="435be-123">Specifies a name.</span></span>
<span data-ttu-id="435be-124">如果沒有指定名稱，則 Cmdlet 會取得所有佇列的清單。</span><span class="sxs-lookup"><span data-stu-id="435be-124">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="435be-125">如果指定完整或部分名稱，則 Cmdlet 會取得符合名稱模式的所有佇列。</span><span class="sxs-lookup"><span data-stu-id="435be-125">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

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

### <span data-ttu-id="435be-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="435be-126">-Prefix</span></span>
<span data-ttu-id="435be-127">指定要取得的佇列名稱中所用的首碼。</span><span class="sxs-lookup"><span data-stu-id="435be-127">Specifies a prefix used in the name of the queues you want to get.</span></span>

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

### <span data-ttu-id="435be-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="435be-128">CommonParameters</span></span>
<span data-ttu-id="435be-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="435be-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="435be-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="435be-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="435be-131">輸入</span><span class="sxs-lookup"><span data-stu-id="435be-131">INPUTS</span></span>

### <span data-ttu-id="435be-132">System.object</span><span class="sxs-lookup"><span data-stu-id="435be-132">System.String</span></span>

### <span data-ttu-id="435be-133">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="435be-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="435be-134">輸出</span><span class="sxs-lookup"><span data-stu-id="435be-134">OUTPUTS</span></span>

### <span data-ttu-id="435be-135">AzureStorageQueue WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="435be-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="435be-136">筆記</span><span class="sxs-lookup"><span data-stu-id="435be-136">NOTES</span></span>

## <span data-ttu-id="435be-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="435be-137">RELATED LINKS</span></span>

[<span data-ttu-id="435be-138">新-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="435be-138">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)

[<span data-ttu-id="435be-139">移除-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="435be-139">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


