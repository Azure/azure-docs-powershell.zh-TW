---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
ms.openlocfilehash: df6f616aacb066ec17aa089b8d91226a5bd171b8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791666"
---
# <span data-ttu-id="0834a-101">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="0834a-101">New-AzStorageQueue</span></span>

## <span data-ttu-id="0834a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0834a-102">SYNOPSIS</span></span>
<span data-ttu-id="0834a-103">建立儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="0834a-103">Creates a storage queue.</span></span>

## <span data-ttu-id="0834a-104">句法</span><span class="sxs-lookup"><span data-stu-id="0834a-104">SYNTAX</span></span>

```
New-AzStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0834a-105">說明</span><span class="sxs-lookup"><span data-stu-id="0834a-105">DESCRIPTION</span></span>
<span data-ttu-id="0834a-106">**新的-AzStorageQueue** Cmdlet 會在 Azure 中建立儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="0834a-106">The **New-AzStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="0834a-107">示例</span><span class="sxs-lookup"><span data-stu-id="0834a-107">EXAMPLES</span></span>

### <span data-ttu-id="0834a-108">範例1：建立 Azure 儲存空間佇列</span><span class="sxs-lookup"><span data-stu-id="0834a-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzStorageQueue -Name "queueabc"
```

<span data-ttu-id="0834a-109">這個範例會建立名為 queueabc 的儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="0834a-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="0834a-110">範例2：建立多個 azure 存儲佇列</span><span class="sxs-lookup"><span data-stu-id="0834a-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzStorageQueue
```

<span data-ttu-id="0834a-111">這個範例會建立多個儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="0834a-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="0834a-112">它會使用 .NET 字串類別的 Split 方法，然後傳送管線上的名稱。</span><span class="sxs-lookup"><span data-stu-id="0834a-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="0834a-113">參數</span><span class="sxs-lookup"><span data-stu-id="0834a-113">PARAMETERS</span></span>

### <span data-ttu-id="0834a-114">-內容</span><span class="sxs-lookup"><span data-stu-id="0834a-114">-Context</span></span>
<span data-ttu-id="0834a-115">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="0834a-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="0834a-116">您可以使用 New-AzStorageContext Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="0834a-116">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0834a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0834a-117">-DefaultProfile</span></span>
<span data-ttu-id="0834a-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0834a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0834a-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="0834a-119">-Name</span></span>
<span data-ttu-id="0834a-120">指定佇列的名稱。</span><span class="sxs-lookup"><span data-stu-id="0834a-120">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="0834a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0834a-121">CommonParameters</span></span>
<span data-ttu-id="0834a-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0834a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0834a-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0834a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0834a-124">輸入</span><span class="sxs-lookup"><span data-stu-id="0834a-124">INPUTS</span></span>

### <span data-ttu-id="0834a-125">System.object</span><span class="sxs-lookup"><span data-stu-id="0834a-125">System.String</span></span>

### <span data-ttu-id="0834a-126">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="0834a-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0834a-127">輸出</span><span class="sxs-lookup"><span data-stu-id="0834a-127">OUTPUTS</span></span>

### <span data-ttu-id="0834a-128">AzureStorageQueue WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="0834a-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="0834a-129">筆記</span><span class="sxs-lookup"><span data-stu-id="0834a-129">NOTES</span></span>

## <span data-ttu-id="0834a-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="0834a-130">RELATED LINKS</span></span>

[<span data-ttu-id="0834a-131">AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="0834a-131">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="0834a-132">移除-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="0834a-132">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


