---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/New-azstorageobjectreplicationpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
ms.openlocfilehash: 8338f13829ebc3feff4c5a81fdfb3bd13934d90d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915065"
---
# <span data-ttu-id="11f36-101">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="11f36-101">New-AzStorageObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="11f36-102">簡介</span><span class="sxs-lookup"><span data-stu-id="11f36-102">SYNOPSIS</span></span>
<span data-ttu-id="11f36-103">建立物件複製原則規則。</span><span class="sxs-lookup"><span data-stu-id="11f36-103">Creates an object replication policy rule.</span></span>

## <span data-ttu-id="11f36-104">語法</span><span class="sxs-lookup"><span data-stu-id="11f36-104">SYNTAX</span></span>

```
New-AzStorageObjectReplicationPolicyRule -SourceContainer <String> -DestinationContainer <String>
 [-PrefixMatch <String[]>] [-MinCreationTime <DateTime>] [-RuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11f36-105">描述</span><span class="sxs-lookup"><span data-stu-id="11f36-105">DESCRIPTION</span></span>
<span data-ttu-id="11f36-106">**Get-AzStorageObjectReplicationPolicy** Cmdlet 會建立物件複製原則規則，將于 Set-AzStorageObjectReplicationPolicy Cmdlet 中使用。</span><span class="sxs-lookup"><span data-stu-id="11f36-106">The **Get-AzStorageObjectReplicationPolicy** cmdlet creates an object replication policy rule, which will be used in Set-AzStorageObjectReplicationPolicy cmdlet.</span></span>

## <span data-ttu-id="11f36-107">例子</span><span class="sxs-lookup"><span data-stu-id="11f36-107">EXAMPLES</span></span>

### <span data-ttu-id="11f36-108">範例 1：建立只包含來源和目的地帳戶的物件複製原則規則，並顯示其屬性</span><span class="sxs-lookup"><span data-stu-id="11f36-108">Example 1: Create an object replication policy rule with only source and destination account, and show its properties</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule1

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src1            dest1                {}
```

<span data-ttu-id="11f36-109">此命令會建立只包含來源和目的帳戶的物件複製原則規則，並顯示其屬性。</span><span class="sxs-lookup"><span data-stu-id="11f36-109">This command creates an object replication policy rule with only source and destination account, and show its properties.</span></span>

### <span data-ttu-id="11f36-110">範例 2：建立包含所有屬性的物件複製原則規則，並顯示其屬性</span><span class="sxs-lookup"><span data-stu-id="11f36-110">Example 2: Create an object replication policy rule with all properties, and show its properties</span></span>
```
PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $rule2

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="11f36-111">此命令會命令具有所有屬性的物件複製原則規則，並顯示其屬性。</span><span class="sxs-lookup"><span data-stu-id="11f36-111">This command an object replication policy rule with all properties, and show its properties.</span></span>

## <span data-ttu-id="11f36-112">參數</span><span class="sxs-lookup"><span data-stu-id="11f36-112">PARAMETERS</span></span>

### <span data-ttu-id="11f36-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11f36-113">-DefaultProfile</span></span>
<span data-ttu-id="11f36-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="11f36-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f36-115">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="11f36-115">-DestinationContainer</span></span>
<span data-ttu-id="11f36-116">要複製到的目的地容器名稱。</span><span class="sxs-lookup"><span data-stu-id="11f36-116">The Destination Container name to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f36-117">-MinCreationTime</span><span class="sxs-lookup"><span data-stu-id="11f36-117">-MinCreationTime</span></span>
<span data-ttu-id="11f36-118">在時間之後建立 Blob 將會複製到目的地。</span><span class="sxs-lookup"><span data-stu-id="11f36-118">Blobs created after the time will be replicated to the destination..</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f36-119">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="11f36-119">-PrefixMatch</span></span>
<span data-ttu-id="11f36-120">篩選結果以只複製名稱以指定首碼開頭的 Blob。</span><span class="sxs-lookup"><span data-stu-id="11f36-120">Filters the results to replicate only blobs whose names begin with the specified prefix.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f36-121">-RuleId</span><span class="sxs-lookup"><span data-stu-id="11f36-121">-RuleId</span></span>
<span data-ttu-id="11f36-122">物件複製規則識別碼。</span><span class="sxs-lookup"><span data-stu-id="11f36-122">Object Replication Rule Id.</span></span>

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

### <span data-ttu-id="11f36-123">-SourceContainer</span><span class="sxs-lookup"><span data-stu-id="11f36-123">-SourceContainer</span></span>
<span data-ttu-id="11f36-124">要複製的來源容器名稱。</span><span class="sxs-lookup"><span data-stu-id="11f36-124">The Source Container name to replicate from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f36-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11f36-125">CommonParameters</span></span>
<span data-ttu-id="11f36-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="11f36-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11f36-127">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="11f36-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11f36-128">輸入</span><span class="sxs-lookup"><span data-stu-id="11f36-128">INPUTS</span></span>

### <span data-ttu-id="11f36-129">沒有</span><span class="sxs-lookup"><span data-stu-id="11f36-129">None</span></span>

## <span data-ttu-id="11f36-130">輸出</span><span class="sxs-lookup"><span data-stu-id="11f36-130">OUTPUTS</span></span>

### <span data-ttu-id="11f36-131">Microsoft.Azure.Commands.management.storage.models.PSObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="11f36-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="11f36-132">筆記</span><span class="sxs-lookup"><span data-stu-id="11f36-132">NOTES</span></span>

## <span data-ttu-id="11f36-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="11f36-133">RELATED LINKS</span></span>
