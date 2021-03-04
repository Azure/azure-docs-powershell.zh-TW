---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: 817a4c8469d1d3652dade426857f88f9249f82b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905565"
---
# <span data-ttu-id="71470-101">New-AzDataMigrationMongoDbCollectionSetting</span><span class="sxs-lookup"><span data-stu-id="71470-101">New-AzDataMigrationMongoDbCollectionSetting</span></span>

## <span data-ttu-id="71470-102">簡介</span><span class="sxs-lookup"><span data-stu-id="71470-102">SYNOPSIS</span></span>
<span data-ttu-id="71470-103">根據 mongoDb 移移建立移移集合設定</span><span class="sxs-lookup"><span data-stu-id="71470-103">Creates collection setting for migration according for the mongoDb migration</span></span>

## <span data-ttu-id="71470-104">語法</span><span class="sxs-lookup"><span data-stu-id="71470-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## <span data-ttu-id="71470-105">描述</span><span class="sxs-lookup"><span data-stu-id="71470-105">DESCRIPTION</span></span>
<span data-ttu-id="71470-106">Cmdlet New-AzDataMigrationMongoDbCollectionSetting建立指定輸送量和刪除行為的移轉設定物件。</span><span class="sxs-lookup"><span data-stu-id="71470-106">The New-AzDataMigrationMongoDbCollectionSetting cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="71470-107">Cmdlet 的輸出是按鍵值與集合名稱和設定值配對。</span><span class="sxs-lookup"><span data-stu-id="71470-107">The output the cmdlet is key value pair with name of the collection, and value of the setting.</span></span> <span data-ttu-id="71470-108">輸出用於組合資料庫層級的移移設定。</span><span class="sxs-lookup"><span data-stu-id="71470-108">The output is used in assembling the database level settings for migration.</span></span>

## <span data-ttu-id="71470-109">例子</span><span class="sxs-lookup"><span data-stu-id="71470-109">EXAMPLES</span></span>

### <span data-ttu-id="71470-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="71470-110">Example 1</span></span>
```
PS C:\> $x = New-AzDataMigrationMongoDbCollectionSetting -Name myCollection -TargetRequestUnit 1000 -CanDelete -ShardKey "_id:-1,age:1,name"
PS C:\> $x

Name         Setting
----         -------
myCollection Microsoft.Azure.Management.DataMigration.Models.MongoDbCollectionSettings

PS C:\> $x.Setting

CanDelete ShardKey                                                               TargetRUs
--------- --------                                                               ---------
     True Microsoft.Azure.Management.DataMigration.Models.MongoDbShardKeySetting      1000

```

## <span data-ttu-id="71470-111">參數</span><span class="sxs-lookup"><span data-stu-id="71470-111">PARAMETERS</span></span>

### <span data-ttu-id="71470-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="71470-112">-Name</span></span>
<span data-ttu-id="71470-113">集合名稱</span><span class="sxs-lookup"><span data-stu-id="71470-113">Name of the collection</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71470-114">-S一鍵</span><span class="sxs-lookup"><span data-stu-id="71470-114">-ShardKey</span></span>
<span data-ttu-id="71470-115">s一鍵的逗號分隔清單。</span><span class="sxs-lookup"><span data-stu-id="71470-115">The comma separated list of the shard keys.</span></span> <span data-ttu-id="71470-116">對於 mongoDb 目標，您可以指定 "S有KeyName：Order" 的 s一鍵順序，其中順序為 1、-1 或雜湊為空白，例如"_id，email：-1"。</span><span class="sxs-lookup"><span data-stu-id="71470-116">For mongoDb target, you can specify shard key order of "ShardKeyName:Order", where order is 1, -1 or empty for hashed, for example "_id,email:-1".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71470-117">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="71470-117">-TargetRequestUnit</span></span>
<span data-ttu-id="71470-118">專用集合要求單位值。</span><span class="sxs-lookup"><span data-stu-id="71470-118">The dedicated collection request unit value.</span></span> <span data-ttu-id="71470-119">如果未設定，該集合會使用共用資料庫 RU。</span><span class="sxs-lookup"><span data-stu-id="71470-119">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="71470-120">-CanDelete</span><span class="sxs-lookup"><span data-stu-id="71470-120">-CanDelete</span></span>
<span data-ttu-id="71470-121">是否要刪除目標資料，如果設定了切換，就會在移轉時清除</span><span class="sxs-lookup"><span data-stu-id="71470-121">Whether the target data is supposed to be deleted, if the switch is set, it will be cleaned up at migration</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="71470-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71470-122">CommonParameters</span></span>
<span data-ttu-id="71470-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="71470-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71470-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="71470-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71470-125">輸入</span><span class="sxs-lookup"><span data-stu-id="71470-125">INPUTS</span></span>

### <span data-ttu-id="71470-126">沒有</span><span class="sxs-lookup"><span data-stu-id="71470-126">None</span></span>

## <span data-ttu-id="71470-127">輸出</span><span class="sxs-lookup"><span data-stu-id="71470-127">OUTPUTS</span></span>

### <span data-ttu-id="71470-128">Microsoft.Azure.Commands.DataMigration.models.MongoDbCollectionSetting></span><span class="sxs-lookup"><span data-stu-id="71470-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span></span>

## <span data-ttu-id="71470-129">筆記</span><span class="sxs-lookup"><span data-stu-id="71470-129">NOTES</span></span>

## <span data-ttu-id="71470-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="71470-130">RELATED LINKS</span></span>
