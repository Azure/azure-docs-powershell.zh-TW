---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: aeb4c89ec4928118c5ebad05fe3c3602d88420ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622481"
---
# <span data-ttu-id="d4e9b-101">New-AzDataMigrationMongoDbCollectionSetting</span><span class="sxs-lookup"><span data-stu-id="d4e9b-101">New-AzDataMigrationMongoDbCollectionSetting</span></span>

## <span data-ttu-id="d4e9b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d4e9b-102">SYNOPSIS</span></span>
<span data-ttu-id="d4e9b-103">根據 mongoDb 遷移建立要遷移的集合設定</span><span class="sxs-lookup"><span data-stu-id="d4e9b-103">Creates collection setting for migration according for the mongoDb migration</span></span>

## <span data-ttu-id="d4e9b-104">句法</span><span class="sxs-lookup"><span data-stu-id="d4e9b-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## <span data-ttu-id="d4e9b-105">說明</span><span class="sxs-lookup"><span data-stu-id="d4e9b-105">DESCRIPTION</span></span>
<span data-ttu-id="d4e9b-106">New-AzDataMigrationMongoDbCollectionSetting Cmdlet 會建立可指定輸送量與刪除行為的 [遷移設定] 物件。</span><span class="sxs-lookup"><span data-stu-id="d4e9b-106">The New-AzDataMigrationMongoDbCollectionSetting cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="d4e9b-107">輸出 Cmdlet 是具有集合名稱的 key 值對，以及設定的值。</span><span class="sxs-lookup"><span data-stu-id="d4e9b-107">The output the cmdlet is key value pair with name of the collection, and value of the setting.</span></span> <span data-ttu-id="d4e9b-108">輸出是用來將 [遷移] 的資料庫層級設定組合在一起。</span><span class="sxs-lookup"><span data-stu-id="d4e9b-108">The output is used in assembling the database level settings for migration.</span></span>

## <span data-ttu-id="d4e9b-109">示例</span><span class="sxs-lookup"><span data-stu-id="d4e9b-109">EXAMPLES</span></span>

### <span data-ttu-id="d4e9b-110">範例1</span><span class="sxs-lookup"><span data-stu-id="d4e9b-110">Example 1</span></span>
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

## <span data-ttu-id="d4e9b-111">參數</span><span class="sxs-lookup"><span data-stu-id="d4e9b-111">PARAMETERS</span></span>

### <span data-ttu-id="d4e9b-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="d4e9b-112">-Name</span></span>
<span data-ttu-id="d4e9b-113">收藏的名稱</span><span class="sxs-lookup"><span data-stu-id="d4e9b-113">Name of the collection</span></span>

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

### <span data-ttu-id="d4e9b-114">-ShardKey</span><span class="sxs-lookup"><span data-stu-id="d4e9b-114">-ShardKey</span></span>
<span data-ttu-id="d4e9b-115">以逗號分隔的 shard 鍵清單。</span><span class="sxs-lookup"><span data-stu-id="d4e9b-115">The comma seperated list of the shard keys.</span></span> <span data-ttu-id="d4e9b-116">對於 mongoDb 目標，您可以指定 shard 的 [ShardKeyName：順序] 順序，其中順序為1、-1 或空，以進行雜湊運算，例如「_id、email：-1」。</span><span class="sxs-lookup"><span data-stu-id="d4e9b-116">For mongoDb target, you can specify shard key order of "ShardKeyName:Order", where order is 1, -1 or empty for hashed, for example "_id,email:-1".</span></span>

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

### <span data-ttu-id="d4e9b-117">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="d4e9b-117">-TargetRequestUnit</span></span>
<span data-ttu-id="d4e9b-118">專用集合要求單位值。</span><span class="sxs-lookup"><span data-stu-id="d4e9b-118">The dedicated collection request unit value.</span></span> <span data-ttu-id="d4e9b-119">如果未設定，該集合會使用共用資料庫 RU。</span><span class="sxs-lookup"><span data-stu-id="d4e9b-119">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="d4e9b-120">-CanDelete</span><span class="sxs-lookup"><span data-stu-id="d4e9b-120">-CanDelete</span></span>
<span data-ttu-id="d4e9b-121">是否應該刪除目標資料（如果已設定），系統會在遷移時清除該選項</span><span class="sxs-lookup"><span data-stu-id="d4e9b-121">Whether the target data is supposed to be deleted, if the switch is set, it will be cleaned up at migration</span></span>

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


### <span data-ttu-id="d4e9b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4e9b-122">CommonParameters</span></span>
<span data-ttu-id="d4e9b-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d4e9b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4e9b-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d4e9b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4e9b-125">輸入</span><span class="sxs-lookup"><span data-stu-id="d4e9b-125">INPUTS</span></span>

### <span data-ttu-id="d4e9b-126">所有</span><span class="sxs-lookup"><span data-stu-id="d4e9b-126">None</span></span>

## <span data-ttu-id="d4e9b-127">輸出</span><span class="sxs-lookup"><span data-stu-id="d4e9b-127">OUTPUTS</span></span>

### <span data-ttu-id="d4e9b-128">[DataMigration MongoDbCollectionSetting] 的></span><span class="sxs-lookup"><span data-stu-id="d4e9b-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span></span>

## <span data-ttu-id="d4e9b-129">筆記</span><span class="sxs-lookup"><span data-stu-id="d4e9b-129">NOTES</span></span>

## <span data-ttu-id="d4e9b-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4e9b-130">RELATED LINKS</span></span>
