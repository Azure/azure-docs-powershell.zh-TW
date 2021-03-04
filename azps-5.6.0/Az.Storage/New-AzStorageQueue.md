---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
ms.openlocfilehash: 55cee15e3b5327fa0a10def6e2090a77b68b207e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915058"
---
# <span data-ttu-id="129eb-101">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="129eb-101">New-AzStorageQueue</span></span>

## <span data-ttu-id="129eb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="129eb-102">SYNOPSIS</span></span>
<span data-ttu-id="129eb-103">建立儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="129eb-103">Creates a storage queue.</span></span>

## <span data-ttu-id="129eb-104">語法</span><span class="sxs-lookup"><span data-stu-id="129eb-104">SYNTAX</span></span>

```
New-AzStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="129eb-105">描述</span><span class="sxs-lookup"><span data-stu-id="129eb-105">DESCRIPTION</span></span>
<span data-ttu-id="129eb-106">**New-AzStorageQueue** Cmdlet 在 Azure 中建立儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="129eb-106">The **New-AzStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="129eb-107">例子</span><span class="sxs-lookup"><span data-stu-id="129eb-107">EXAMPLES</span></span>

### <span data-ttu-id="129eb-108">範例 1：建立 Azure 儲存佇列</span><span class="sxs-lookup"><span data-stu-id="129eb-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzStorageQueue -Name "queueabc"
```

<span data-ttu-id="129eb-109">此範例會建立名為 queueabc 的儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="129eb-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="129eb-110">範例 2：建立多個 Azure 儲存佇列</span><span class="sxs-lookup"><span data-stu-id="129eb-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzStorageQueue
```

<span data-ttu-id="129eb-111">此範例會建立多個儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="129eb-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="129eb-112">它使用 .NET String 類的 Split 方法，然後傳遞管線上的名稱。</span><span class="sxs-lookup"><span data-stu-id="129eb-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="129eb-113">參數</span><span class="sxs-lookup"><span data-stu-id="129eb-113">PARAMETERS</span></span>

### <span data-ttu-id="129eb-114">-內容</span><span class="sxs-lookup"><span data-stu-id="129eb-114">-Context</span></span>
<span data-ttu-id="129eb-115">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="129eb-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="129eb-116">您可以使用 Cmdlet New-AzStorageContext建立。</span><span class="sxs-lookup"><span data-stu-id="129eb-116">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="129eb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="129eb-117">-DefaultProfile</span></span>
<span data-ttu-id="129eb-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="129eb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="129eb-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="129eb-119">-Name</span></span>
<span data-ttu-id="129eb-120">指定佇列的名稱。</span><span class="sxs-lookup"><span data-stu-id="129eb-120">Specifies a name for the queue.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="129eb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="129eb-121">CommonParameters</span></span>
<span data-ttu-id="129eb-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="129eb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="129eb-123">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="129eb-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="129eb-124">輸入</span><span class="sxs-lookup"><span data-stu-id="129eb-124">INPUTS</span></span>

### <span data-ttu-id="129eb-125">System.String</span><span class="sxs-lookup"><span data-stu-id="129eb-125">System.String</span></span>

### <span data-ttu-id="129eb-126">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="129eb-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="129eb-127">輸出</span><span class="sxs-lookup"><span data-stu-id="129eb-127">OUTPUTS</span></span>

### <span data-ttu-id="129eb-128">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="129eb-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="129eb-129">筆記</span><span class="sxs-lookup"><span data-stu-id="129eb-129">NOTES</span></span>

## <span data-ttu-id="129eb-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="129eb-130">RELATED LINKS</span></span>

[<span data-ttu-id="129eb-131">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="129eb-131">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="129eb-132">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="129eb-132">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


