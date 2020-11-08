---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: d501faaebcc5e381dc2a7270c8b55b148e2812b4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138067"
---
# <span data-ttu-id="20690-101">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="20690-101">Get-AzStorageTable</span></span>

## <span data-ttu-id="20690-102">摘要</span><span class="sxs-lookup"><span data-stu-id="20690-102">SYNOPSIS</span></span>
<span data-ttu-id="20690-103">列出儲存資料表。</span><span class="sxs-lookup"><span data-stu-id="20690-103">Lists the storage tables.</span></span>

## <span data-ttu-id="20690-104">句法</span><span class="sxs-lookup"><span data-stu-id="20690-104">SYNTAX</span></span>

### <span data-ttu-id="20690-105">TableName (預設) </span><span class="sxs-lookup"><span data-stu-id="20690-105">TableName (Default)</span></span>
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="20690-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="20690-106">TablePrefix</span></span>
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="20690-107">說明</span><span class="sxs-lookup"><span data-stu-id="20690-107">DESCRIPTION</span></span>
<span data-ttu-id="20690-108">**AzStorageTable** Cmdlet 會列出與 Azure 中的儲存空間帳戶相關聯的儲存空間資料表。</span><span class="sxs-lookup"><span data-stu-id="20690-108">The **Get-AzStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="20690-109">示例</span><span class="sxs-lookup"><span data-stu-id="20690-109">EXAMPLES</span></span>

### <span data-ttu-id="20690-110">範例1：列出所有 Azure 儲存空間資料表</span><span class="sxs-lookup"><span data-stu-id="20690-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzStorageTable
```

<span data-ttu-id="20690-111">這個命令會取得儲存空間帳戶的所有儲存空間資料表。</span><span class="sxs-lookup"><span data-stu-id="20690-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="20690-112">範例2：使用萬用字元列出 Azure 儲存空間資料表</span><span class="sxs-lookup"><span data-stu-id="20690-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzStorageTable -Name table*
```

<span data-ttu-id="20690-113">這個命令使用萬用字元來取得名稱以 table 開頭的儲存資料表。</span><span class="sxs-lookup"><span data-stu-id="20690-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="20690-114">範例3：使用表格名稱首碼列出 Azure 儲存空間資料表</span><span class="sxs-lookup"><span data-stu-id="20690-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

<span data-ttu-id="20690-115">這個命令會使用 *Prefix* 參數來取得名稱以 table 開頭的儲存空間資料表。</span><span class="sxs-lookup"><span data-stu-id="20690-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="20690-116">參數</span><span class="sxs-lookup"><span data-stu-id="20690-116">PARAMETERS</span></span>

### <span data-ttu-id="20690-117">-內容</span><span class="sxs-lookup"><span data-stu-id="20690-117">-Context</span></span>
<span data-ttu-id="20690-118">指定儲存內容。</span><span class="sxs-lookup"><span data-stu-id="20690-118">Specifies the storage context.</span></span>
<span data-ttu-id="20690-119">若要建立它，您可以使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="20690-119">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="20690-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20690-120">-DefaultProfile</span></span>
<span data-ttu-id="20690-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="20690-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20690-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="20690-122">-Name</span></span>
<span data-ttu-id="20690-123">指定資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="20690-123">Specifies the table name.</span></span>
<span data-ttu-id="20690-124">如果資料表名稱是空值，該 Cmdlet 會列出所有的資料表。</span><span class="sxs-lookup"><span data-stu-id="20690-124">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="20690-125">否則，它會列出符合指定名稱或一般名稱模式的所有資料表。</span><span class="sxs-lookup"><span data-stu-id="20690-125">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

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

### <span data-ttu-id="20690-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="20690-126">-Prefix</span></span>
<span data-ttu-id="20690-127">指定要取得的資料表名稱中所用的首碼。</span><span class="sxs-lookup"><span data-stu-id="20690-127">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="20690-128">您可以使用此程式來找出所有以相同字串（例如 table）開頭的資料表。</span><span class="sxs-lookup"><span data-stu-id="20690-128">You can use this to find all tables that start with the same string, such as table.</span></span>

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

### <span data-ttu-id="20690-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20690-129">CommonParameters</span></span>
<span data-ttu-id="20690-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="20690-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20690-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="20690-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20690-132">輸入</span><span class="sxs-lookup"><span data-stu-id="20690-132">INPUTS</span></span>

### <span data-ttu-id="20690-133">System.object</span><span class="sxs-lookup"><span data-stu-id="20690-133">System.String</span></span>

### <span data-ttu-id="20690-134">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="20690-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="20690-135">輸出</span><span class="sxs-lookup"><span data-stu-id="20690-135">OUTPUTS</span></span>

### <span data-ttu-id="20690-136">AzureStorageTable WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="20690-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="20690-137">筆記</span><span class="sxs-lookup"><span data-stu-id="20690-137">NOTES</span></span>

## <span data-ttu-id="20690-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="20690-138">RELATED LINKS</span></span>

[<span data-ttu-id="20690-139">新-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="20690-139">New-AzStorageTable</span></span>](./New-AzStorageTable.md)

[<span data-ttu-id="20690-140">移除-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="20690-140">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)


