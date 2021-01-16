---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/new-azdatamigrationmongodbdatabasesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
ms.openlocfilehash: 9ae50501306dfa1a76fa4966113ac2e9b681f6c5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98289312"
---
# <span data-ttu-id="f68ca-101">New-AzDataMigrationMongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="f68ca-101">New-AzDataMigrationMongoDbDatabaseSetting</span></span>

## <span data-ttu-id="f68ca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f68ca-102">SYNOPSIS</span></span>
<span data-ttu-id="f68ca-103">針對 mongoDb 遷移建立遷移的資料庫設定</span><span class="sxs-lookup"><span data-stu-id="f68ca-103">Creates database setting for migration for the mongoDb migration</span></span>

## <span data-ttu-id="f68ca-104">句法</span><span class="sxs-lookup"><span data-stu-id="f68ca-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbDatabaseSetting  -Name <Name> [-RU <RU>] -CollectionSetting <Collections>
```

## <span data-ttu-id="f68ca-105">說明</span><span class="sxs-lookup"><span data-stu-id="f68ca-105">DESCRIPTION</span></span>
<span data-ttu-id="f68ca-106">New-AzDataMigrationMongoDbDatabaseSetting Cmdlet 會建立可指定輸送量與刪除行為的 [遷移設定] 物件。</span><span class="sxs-lookup"><span data-stu-id="f68ca-106">The New-AzDataMigrationMongoDbDatabaseSetting  cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="f68ca-107">輸出是 [集合] 的名稱和設定值的鍵值組，可以用來喚醒喚醒作業。</span><span class="sxs-lookup"><span data-stu-id="f68ca-107">The output is a key value pair with name of collection and value of the setting, which can be used in invoking the migration task.</span></span>

## <span data-ttu-id="f68ca-108">示例</span><span class="sxs-lookup"><span data-stu-id="f68ca-108">EXAMPLES</span></span>

### <span data-ttu-id="f68ca-109">範例1</span><span class="sxs-lookup"><span data-stu-id="f68ca-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationMongoDbDatabaseSetting  -Name mycollection -RU 1000 -CollectionSetting @($coll1, $coll2)

Name Setting
---- -------
test Microsoft.Azure.Management.DataMigration.Models.MongoDbDatabaseSettings

```

## <span data-ttu-id="f68ca-110">參數</span><span class="sxs-lookup"><span data-stu-id="f68ca-110">PARAMETERS</span></span>

### <span data-ttu-id="f68ca-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="f68ca-111">-Name</span></span>
<span data-ttu-id="f68ca-112">資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="f68ca-112">Name of the database</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="f68ca-113">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="f68ca-113">-TargetRequestUnit</span></span>
<span data-ttu-id="f68ca-114">專用資料庫層級要求單位值。</span><span class="sxs-lookup"><span data-stu-id="f68ca-114">The dedicated database level request unit value.</span></span> <span data-ttu-id="f68ca-115">如果未設定，該集合會使用共用資料庫 RU。</span><span class="sxs-lookup"><span data-stu-id="f68ca-115">If not set, that collection uses shared database RU.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: RU

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f68ca-116">-集合</span><span class="sxs-lookup"><span data-stu-id="f68ca-116">-Collections</span></span>
<span data-ttu-id="f68ca-117">New-AzureRmDmsMongoDbDatabaseSetting call 傳回的 MongoDb 集合設定物件陣列。</span><span class="sxs-lookup"><span data-stu-id="f68ca-117">The array of MongoDb collection setting objects returned by New-AzureRmDmsMongoDbDatabaseSetting call.</span></span>

```yaml
Type: System.Collections.Generic.KeyValuePair<string, MongoDbCollectionSettings>[]
Parameter Sets: (All)
Aliases: colls

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f68ca-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f68ca-118">CommonParameters</span></span>
<span data-ttu-id="f68ca-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f68ca-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f68ca-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f68ca-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f68ca-121">輸入</span><span class="sxs-lookup"><span data-stu-id="f68ca-121">INPUTS</span></span>

### <span data-ttu-id="f68ca-122">所有</span><span class="sxs-lookup"><span data-stu-id="f68ca-122">None</span></span>

## <span data-ttu-id="f68ca-123">輸出</span><span class="sxs-lookup"><span data-stu-id="f68ca-123">OUTPUTS</span></span>

### <span data-ttu-id="f68ca-124">MongoDbDatabaseSetting 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="f68ca-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span></span>

## <span data-ttu-id="f68ca-125">筆記</span><span class="sxs-lookup"><span data-stu-id="f68ca-125">NOTES</span></span>

## <span data-ttu-id="f68ca-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="f68ca-126">RELATED LINKS</span></span>
