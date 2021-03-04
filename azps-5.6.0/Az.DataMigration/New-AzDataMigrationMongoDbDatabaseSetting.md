---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/new-azdatamigrationmongodbdatabasesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
ms.openlocfilehash: cf034b01d0cc7bd707d65cb2ddd90e9567003861
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909709"
---
# <span data-ttu-id="04086-101">New-AzDataMigrationMongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="04086-101">New-AzDataMigrationMongoDbDatabaseSetting</span></span>

## <span data-ttu-id="04086-102">簡介</span><span class="sxs-lookup"><span data-stu-id="04086-102">SYNOPSIS</span></span>
<span data-ttu-id="04086-103">為 mongoDb 移移建立移移的資料庫設定</span><span class="sxs-lookup"><span data-stu-id="04086-103">Creates database setting for migration for the mongoDb migration</span></span>

## <span data-ttu-id="04086-104">語法</span><span class="sxs-lookup"><span data-stu-id="04086-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbDatabaseSetting  -Name <Name> [-RU <RU>] -CollectionSetting <Collections>
```

## <span data-ttu-id="04086-105">描述</span><span class="sxs-lookup"><span data-stu-id="04086-105">DESCRIPTION</span></span>
<span data-ttu-id="04086-106">Cmdlet New-AzDataMigrationMongoDbDatabaseSetting建立指定輸送量和刪除行為的移轉設定物件。</span><span class="sxs-lookup"><span data-stu-id="04086-106">The New-AzDataMigrationMongoDbDatabaseSetting  cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="04086-107">輸出是一組金鑰值，包含集合名稱和設定值，可用來叫出移移工作。</span><span class="sxs-lookup"><span data-stu-id="04086-107">The output is a key value pair with name of collection and value of the setting, which can be used in invoking the migration task.</span></span>

## <span data-ttu-id="04086-108">例子</span><span class="sxs-lookup"><span data-stu-id="04086-108">EXAMPLES</span></span>

### <span data-ttu-id="04086-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="04086-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationMongoDbDatabaseSetting  -Name mycollection -RU 1000 -CollectionSetting @($coll1, $coll2)

Name Setting
---- -------
test Microsoft.Azure.Management.DataMigration.Models.MongoDbDatabaseSettings

```

## <span data-ttu-id="04086-110">參數</span><span class="sxs-lookup"><span data-stu-id="04086-110">PARAMETERS</span></span>

### <span data-ttu-id="04086-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="04086-111">-Name</span></span>
<span data-ttu-id="04086-112">資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="04086-112">Name of the database</span></span>

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
### <span data-ttu-id="04086-113">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="04086-113">-TargetRequestUnit</span></span>
<span data-ttu-id="04086-114">專用資料庫層級要求單位值。</span><span class="sxs-lookup"><span data-stu-id="04086-114">The dedicated database level request unit value.</span></span> <span data-ttu-id="04086-115">如果未設定，該集合會使用共用資料庫 RU。</span><span class="sxs-lookup"><span data-stu-id="04086-115">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="04086-116">-集合</span><span class="sxs-lookup"><span data-stu-id="04086-116">-Collections</span></span>
<span data-ttu-id="04086-117">MongoDb 集合陣列會設定由呼叫New-AzureRmDmsMongoDbDatabaseSetting物件。</span><span class="sxs-lookup"><span data-stu-id="04086-117">The array of MongoDb collection setting objects returned by New-AzureRmDmsMongoDbDatabaseSetting call.</span></span>

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

### <span data-ttu-id="04086-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04086-118">CommonParameters</span></span>
<span data-ttu-id="04086-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="04086-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04086-120">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="04086-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04086-121">輸入</span><span class="sxs-lookup"><span data-stu-id="04086-121">INPUTS</span></span>

### <span data-ttu-id="04086-122">沒有</span><span class="sxs-lookup"><span data-stu-id="04086-122">None</span></span>

## <span data-ttu-id="04086-123">輸出</span><span class="sxs-lookup"><span data-stu-id="04086-123">OUTPUTS</span></span>

### <span data-ttu-id="04086-124">Microsoft.Azure.Commands.DataMigration.models.MongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="04086-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span></span>

## <span data-ttu-id="04086-125">筆記</span><span class="sxs-lookup"><span data-stu-id="04086-125">NOTES</span></span>

## <span data-ttu-id="04086-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="04086-126">RELATED LINKS</span></span>
