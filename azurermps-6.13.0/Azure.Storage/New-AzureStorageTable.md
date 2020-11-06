---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
ms.openlocfilehash: 14f42ae951fe25f7594eb6e314ac65bb678e29c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445860"
---
# <span data-ttu-id="3479f-101">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="3479f-101">New-AzureStorageTable</span></span>

## <span data-ttu-id="3479f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3479f-102">SYNOPSIS</span></span>
<span data-ttu-id="3479f-103">建立儲存空間表。</span><span class="sxs-lookup"><span data-stu-id="3479f-103">Creates a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3479f-104">句法</span><span class="sxs-lookup"><span data-stu-id="3479f-104">SYNTAX</span></span>

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3479f-105">說明</span><span class="sxs-lookup"><span data-stu-id="3479f-105">DESCRIPTION</span></span>
<span data-ttu-id="3479f-106">**新的-AzureStorageTable** Cmdlet 會建立與 Azure 中的儲存空間帳戶相關聯的儲存空間表。</span><span class="sxs-lookup"><span data-stu-id="3479f-106">The **New-AzureStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="3479f-107">示例</span><span class="sxs-lookup"><span data-stu-id="3479f-107">EXAMPLES</span></span>

### <span data-ttu-id="3479f-108">範例1：建立 azure 儲存空間資料表</span><span class="sxs-lookup"><span data-stu-id="3479f-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

<span data-ttu-id="3479f-109">這個命令會建立名稱為 tableabc 的儲存空間資料表。</span><span class="sxs-lookup"><span data-stu-id="3479f-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="3479f-110">範例2：建立多個 azure 儲存空間資料表</span><span class="sxs-lookup"><span data-stu-id="3479f-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

<span data-ttu-id="3479f-111">這個命令會建立多個資料表。</span><span class="sxs-lookup"><span data-stu-id="3479f-111">This command creates multiple tables.</span></span>
<span data-ttu-id="3479f-112">它會使用 .NET **字串** 類別的 **Split** 方法，然後傳送管線上的名稱。</span><span class="sxs-lookup"><span data-stu-id="3479f-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="3479f-113">參數</span><span class="sxs-lookup"><span data-stu-id="3479f-113">PARAMETERS</span></span>

### <span data-ttu-id="3479f-114">-內容</span><span class="sxs-lookup"><span data-stu-id="3479f-114">-Context</span></span>
<span data-ttu-id="3479f-115">指定儲存內容。</span><span class="sxs-lookup"><span data-stu-id="3479f-115">Specifies the storage context.</span></span>
<span data-ttu-id="3479f-116">若要建立它，您可以使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3479f-116">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3479f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3479f-117">-DefaultProfile</span></span>
<span data-ttu-id="3479f-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3479f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3479f-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="3479f-119">-Name</span></span>
<span data-ttu-id="3479f-120">指定新資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="3479f-120">Specifies a name for the new table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3479f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3479f-121">CommonParameters</span></span>
<span data-ttu-id="3479f-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3479f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3479f-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3479f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3479f-124">輸入</span><span class="sxs-lookup"><span data-stu-id="3479f-124">INPUTS</span></span>

### <span data-ttu-id="3479f-125">System.object</span><span class="sxs-lookup"><span data-stu-id="3479f-125">System.String</span></span>

### <span data-ttu-id="3479f-126">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="3479f-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3479f-127">輸出</span><span class="sxs-lookup"><span data-stu-id="3479f-127">OUTPUTS</span></span>

### <span data-ttu-id="3479f-128">AzureStorageTable WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="3479f-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="3479f-129">筆記</span><span class="sxs-lookup"><span data-stu-id="3479f-129">NOTES</span></span>

## <span data-ttu-id="3479f-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="3479f-130">RELATED LINKS</span></span>

[<span data-ttu-id="3479f-131">AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="3479f-131">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

[<span data-ttu-id="3479f-132">移除-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="3479f-132">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


