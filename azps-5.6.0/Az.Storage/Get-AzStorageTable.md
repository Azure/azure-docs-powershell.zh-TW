---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: d4296acd16b29640fa8925d8482cca012be27b73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912993"
---
# <span data-ttu-id="02a75-101">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="02a75-101">Get-AzStorageTable</span></span>

## <span data-ttu-id="02a75-102">簡介</span><span class="sxs-lookup"><span data-stu-id="02a75-102">SYNOPSIS</span></span>
<span data-ttu-id="02a75-103">列出儲存資料表。</span><span class="sxs-lookup"><span data-stu-id="02a75-103">Lists the storage tables.</span></span>

## <span data-ttu-id="02a75-104">語法</span><span class="sxs-lookup"><span data-stu-id="02a75-104">SYNTAX</span></span>

### <span data-ttu-id="02a75-105">TableName (預設) </span><span class="sxs-lookup"><span data-stu-id="02a75-105">TableName (Default)</span></span>
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="02a75-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="02a75-106">TablePrefix</span></span>
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="02a75-107">描述</span><span class="sxs-lookup"><span data-stu-id="02a75-107">DESCRIPTION</span></span>
<span data-ttu-id="02a75-108">**Get-AzStorageTable** Cmdlet 會列出與 Azure 中儲存帳戶相關聯的儲存資料表。</span><span class="sxs-lookup"><span data-stu-id="02a75-108">The **Get-AzStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="02a75-109">例子</span><span class="sxs-lookup"><span data-stu-id="02a75-109">EXAMPLES</span></span>

### <span data-ttu-id="02a75-110">範例 1：列出所有 Azure 儲存體資料表</span><span class="sxs-lookup"><span data-stu-id="02a75-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzStorageTable
```

<span data-ttu-id="02a75-111">此命令會獲得儲存帳戶的所有儲存資料表。</span><span class="sxs-lookup"><span data-stu-id="02a75-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="02a75-112">範例 2：使用萬用字元列出 Azure 儲存體資料表</span><span class="sxs-lookup"><span data-stu-id="02a75-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzStorageTable -Name table*
```

<span data-ttu-id="02a75-113">此命令使用萬用字元取得名稱以資料表開頭的儲存資料表。</span><span class="sxs-lookup"><span data-stu-id="02a75-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="02a75-114">範例 3：使用資料表名稱首碼列出 Azure 儲存體資料表</span><span class="sxs-lookup"><span data-stu-id="02a75-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

<span data-ttu-id="02a75-115">此命令使用 *首碼參數* 取得名稱以資料表開頭的儲存資料表。</span><span class="sxs-lookup"><span data-stu-id="02a75-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="02a75-116">參數</span><span class="sxs-lookup"><span data-stu-id="02a75-116">PARAMETERS</span></span>

### <span data-ttu-id="02a75-117">-內容</span><span class="sxs-lookup"><span data-stu-id="02a75-117">-Context</span></span>
<span data-ttu-id="02a75-118">指定儲存內容。</span><span class="sxs-lookup"><span data-stu-id="02a75-118">Specifies the storage context.</span></span>
<span data-ttu-id="02a75-119">若要建立，您可以使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02a75-119">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="02a75-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02a75-120">-DefaultProfile</span></span>
<span data-ttu-id="02a75-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="02a75-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02a75-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="02a75-122">-Name</span></span>
<span data-ttu-id="02a75-123">指定資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="02a75-123">Specifies the table name.</span></span>
<span data-ttu-id="02a75-124">如果資料表名稱為空白，Cmdlet 會列出所有資料表。</span><span class="sxs-lookup"><span data-stu-id="02a75-124">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="02a75-125">否則，它會列出符合指定名稱或一般名稱模式的所有資料表。</span><span class="sxs-lookup"><span data-stu-id="02a75-125">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02a75-126">-首碼</span><span class="sxs-lookup"><span data-stu-id="02a75-126">-Prefix</span></span>
<span data-ttu-id="02a75-127">指定要取得之資料表名稱中使用的首碼。</span><span class="sxs-lookup"><span data-stu-id="02a75-127">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="02a75-128">您可以使用這個來尋找以相同字串開頭的所有資料表，例如資料表。</span><span class="sxs-lookup"><span data-stu-id="02a75-128">You can use this to find all tables that start with the same string, such as table.</span></span>

```yaml
Type: System.String
Parameter Sets: TablePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a75-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02a75-129">CommonParameters</span></span>
<span data-ttu-id="02a75-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="02a75-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02a75-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="02a75-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02a75-132">輸入</span><span class="sxs-lookup"><span data-stu-id="02a75-132">INPUTS</span></span>

### <span data-ttu-id="02a75-133">System.String</span><span class="sxs-lookup"><span data-stu-id="02a75-133">System.String</span></span>

### <span data-ttu-id="02a75-134">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="02a75-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="02a75-135">輸出</span><span class="sxs-lookup"><span data-stu-id="02a75-135">OUTPUTS</span></span>

### <span data-ttu-id="02a75-136">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="02a75-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="02a75-137">筆記</span><span class="sxs-lookup"><span data-stu-id="02a75-137">NOTES</span></span>

## <span data-ttu-id="02a75-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="02a75-138">RELATED LINKS</span></span>

[<span data-ttu-id="02a75-139">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="02a75-139">New-AzStorageTable</span></span>](./New-AzStorageTable.md)

[<span data-ttu-id="02a75-140">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="02a75-140">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)


