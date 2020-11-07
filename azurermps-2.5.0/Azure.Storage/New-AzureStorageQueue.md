---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeue
schema: 2.0.0
ms.openlocfilehash: a028d2528d74e9372bfca28ccfb085f119486ce7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801470"
---
# <span data-ttu-id="af19b-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="af19b-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="af19b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="af19b-102">SYNOPSIS</span></span>
<span data-ttu-id="af19b-103">建立儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="af19b-103">Creates a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af19b-104">句法</span><span class="sxs-lookup"><span data-stu-id="af19b-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af19b-105">說明</span><span class="sxs-lookup"><span data-stu-id="af19b-105">DESCRIPTION</span></span>
<span data-ttu-id="af19b-106">**新的-AzureStorageQueue** Cmdlet 會在 Azure 中建立儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="af19b-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="af19b-107">示例</span><span class="sxs-lookup"><span data-stu-id="af19b-107">EXAMPLES</span></span>

### <span data-ttu-id="af19b-108">範例1：建立 Azure 儲存空間佇列</span><span class="sxs-lookup"><span data-stu-id="af19b-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="af19b-109">這個範例會建立名為 queueabc 的儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="af19b-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="af19b-110">範例2：建立多個 azure 存儲佇列</span><span class="sxs-lookup"><span data-stu-id="af19b-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="af19b-111">這個範例會建立多個儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="af19b-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="af19b-112">它會使用 .NET 字串類別的 Split 方法，然後傳送管線上的名稱。</span><span class="sxs-lookup"><span data-stu-id="af19b-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="af19b-113">參數</span><span class="sxs-lookup"><span data-stu-id="af19b-113">PARAMETERS</span></span>

### <span data-ttu-id="af19b-114">-內容</span><span class="sxs-lookup"><span data-stu-id="af19b-114">-Context</span></span>
<span data-ttu-id="af19b-115">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="af19b-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="af19b-116">您可以使用 New-AzureStorageContext Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="af19b-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="af19b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af19b-117">-DefaultProfile</span></span>
<span data-ttu-id="af19b-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="af19b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af19b-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="af19b-119">-Name</span></span>
<span data-ttu-id="af19b-120">指定佇列的名稱。</span><span class="sxs-lookup"><span data-stu-id="af19b-120">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="af19b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af19b-121">CommonParameters</span></span>
<span data-ttu-id="af19b-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="af19b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af19b-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="af19b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af19b-124">輸入</span><span class="sxs-lookup"><span data-stu-id="af19b-124">INPUTS</span></span>

### <span data-ttu-id="af19b-125">System.object</span><span class="sxs-lookup"><span data-stu-id="af19b-125">System.String</span></span>

### <span data-ttu-id="af19b-126">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="af19b-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="af19b-127">輸出</span><span class="sxs-lookup"><span data-stu-id="af19b-127">OUTPUTS</span></span>

### <span data-ttu-id="af19b-128">AzureStorageQueue WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="af19b-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="af19b-129">筆記</span><span class="sxs-lookup"><span data-stu-id="af19b-129">NOTES</span></span>

## <span data-ttu-id="af19b-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="af19b-130">RELATED LINKS</span></span>

[<span data-ttu-id="af19b-131">AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="af19b-131">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="af19b-132">移除-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="af19b-132">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


