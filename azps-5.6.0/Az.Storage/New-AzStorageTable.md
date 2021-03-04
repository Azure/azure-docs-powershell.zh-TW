---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
ms.openlocfilehash: 84b5389c4f9b404b4b74783184143af310bf1ba5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915034"
---
# <span data-ttu-id="e85b4-101">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="e85b4-101">New-AzStorageTable</span></span>

## <span data-ttu-id="e85b4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e85b4-102">SYNOPSIS</span></span>
<span data-ttu-id="e85b4-103">建立儲存資料表。</span><span class="sxs-lookup"><span data-stu-id="e85b4-103">Creates a storage table.</span></span>

## <span data-ttu-id="e85b4-104">語法</span><span class="sxs-lookup"><span data-stu-id="e85b4-104">SYNTAX</span></span>

```
New-AzStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e85b4-105">描述</span><span class="sxs-lookup"><span data-stu-id="e85b4-105">DESCRIPTION</span></span>
<span data-ttu-id="e85b4-106">**New-AzStorageTable** Cmdlet 會建立與 Azure 中儲存帳戶相關聯的儲存資料表。</span><span class="sxs-lookup"><span data-stu-id="e85b4-106">The **New-AzStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="e85b4-107">例子</span><span class="sxs-lookup"><span data-stu-id="e85b4-107">EXAMPLES</span></span>

### <span data-ttu-id="e85b4-108">範例 1：建立 Azure 儲存資料表</span><span class="sxs-lookup"><span data-stu-id="e85b4-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzStorageTable -Name "tableabc"
```

<span data-ttu-id="e85b4-109">此命令會建立具有 tableabc 名稱的儲存資料表。</span><span class="sxs-lookup"><span data-stu-id="e85b4-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="e85b4-110">範例 2：建立多個 Azure 儲存資料表</span><span class="sxs-lookup"><span data-stu-id="e85b4-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzStorageTable
```

<span data-ttu-id="e85b4-111">此命令會建立多個資料表。</span><span class="sxs-lookup"><span data-stu-id="e85b4-111">This command creates multiple tables.</span></span>
<span data-ttu-id="e85b4-112">它 **使用** .NET **String** 類的 Split 方法，然後傳遞管線上的名稱。</span><span class="sxs-lookup"><span data-stu-id="e85b4-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="e85b4-113">參數</span><span class="sxs-lookup"><span data-stu-id="e85b4-113">PARAMETERS</span></span>

### <span data-ttu-id="e85b4-114">-內容</span><span class="sxs-lookup"><span data-stu-id="e85b4-114">-Context</span></span>
<span data-ttu-id="e85b4-115">指定儲存內容。</span><span class="sxs-lookup"><span data-stu-id="e85b4-115">Specifies the storage context.</span></span>
<span data-ttu-id="e85b4-116">若要建立，您可以使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e85b4-116">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e85b4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e85b4-117">-DefaultProfile</span></span>
<span data-ttu-id="e85b4-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e85b4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e85b4-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="e85b4-119">-Name</span></span>
<span data-ttu-id="e85b4-120">指定新資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="e85b4-120">Specifies a name for the new table.</span></span>

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

### <span data-ttu-id="e85b4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e85b4-121">CommonParameters</span></span>
<span data-ttu-id="e85b4-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e85b4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e85b4-123">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e85b4-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e85b4-124">輸入</span><span class="sxs-lookup"><span data-stu-id="e85b4-124">INPUTS</span></span>

### <span data-ttu-id="e85b4-125">System.String</span><span class="sxs-lookup"><span data-stu-id="e85b4-125">System.String</span></span>

### <span data-ttu-id="e85b4-126">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="e85b4-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e85b4-127">輸出</span><span class="sxs-lookup"><span data-stu-id="e85b4-127">OUTPUTS</span></span>

### <span data-ttu-id="e85b4-128">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="e85b4-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="e85b4-129">筆記</span><span class="sxs-lookup"><span data-stu-id="e85b4-129">NOTES</span></span>

## <span data-ttu-id="e85b4-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="e85b4-130">RELATED LINKS</span></span>

[<span data-ttu-id="e85b4-131">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="e85b4-131">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)

[<span data-ttu-id="e85b4-132">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="e85b4-132">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)


