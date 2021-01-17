---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/New-azstorageobjectreplicationpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
ms.openlocfilehash: c8d41300250e41548cf949248b02c819b7da497f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435916"
---
# <span data-ttu-id="07c3e-101">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="07c3e-101">New-AzStorageObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="07c3e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="07c3e-102">SYNOPSIS</span></span>
<span data-ttu-id="07c3e-103">建立物件複製原則規則。</span><span class="sxs-lookup"><span data-stu-id="07c3e-103">Creates an object replication policy rule.</span></span>

## <span data-ttu-id="07c3e-104">句法</span><span class="sxs-lookup"><span data-stu-id="07c3e-104">SYNTAX</span></span>

```
New-AzStorageObjectReplicationPolicyRule -SourceContainer <String> -DestinationContainer <String>
 [-PrefixMatch <String[]>] [-MinCreationTime <DateTime>] [-RuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07c3e-105">說明</span><span class="sxs-lookup"><span data-stu-id="07c3e-105">DESCRIPTION</span></span>
<span data-ttu-id="07c3e-106">**AzStorageObjectReplicationPolicy** Cmdlet 會建立物件複製原則規則，這會在 Set-AzStorageObjectReplicationPolicy Cmdlet 中使用。</span><span class="sxs-lookup"><span data-stu-id="07c3e-106">The **Get-AzStorageObjectReplicationPolicy** cmdlet creates an object replication policy rule, which will be used in Set-AzStorageObjectReplicationPolicy cmdlet.</span></span>

## <span data-ttu-id="07c3e-107">示例</span><span class="sxs-lookup"><span data-stu-id="07c3e-107">EXAMPLES</span></span>

### <span data-ttu-id="07c3e-108">範例1：建立只有來源與目的地帳戶的物件複製原則規則，並顯示其屬性</span><span class="sxs-lookup"><span data-stu-id="07c3e-108">Example 1: Create an object replication policy rule with only source and destination account, and show its properties</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule1

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src1            dest1                {}
```

<span data-ttu-id="07c3e-109">這個命令會建立只有來源和目的地帳戶的物件複製原則規則，並顯示其屬性。</span><span class="sxs-lookup"><span data-stu-id="07c3e-109">This command creates an object replication policy rule with only source and destination account, and show its properties.</span></span>

### <span data-ttu-id="07c3e-110">範例2：使用所有屬性建立物件複製原則規則，並顯示其屬性</span><span class="sxs-lookup"><span data-stu-id="07c3e-110">Example 2: Create an object replication policy rule with all properties, and show its properties</span></span>
```
PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $rule2

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="07c3e-111">這個命令包含所有屬性的物件複製原則規則，並顯示其屬性。</span><span class="sxs-lookup"><span data-stu-id="07c3e-111">This command an object replication policy rule with all properties, and show its properties.</span></span>

## <span data-ttu-id="07c3e-112">參數</span><span class="sxs-lookup"><span data-stu-id="07c3e-112">PARAMETERS</span></span>

### <span data-ttu-id="07c3e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07c3e-113">-DefaultProfile</span></span>
<span data-ttu-id="07c3e-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="07c3e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07c3e-115">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="07c3e-115">-DestinationContainer</span></span>
<span data-ttu-id="07c3e-116">要複製的目的地容器名稱。</span><span class="sxs-lookup"><span data-stu-id="07c3e-116">The Destination Container name to replicate to.</span></span>

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

### <span data-ttu-id="07c3e-117">-MinCreationTime</span><span class="sxs-lookup"><span data-stu-id="07c3e-117">-MinCreationTime</span></span>
<span data-ttu-id="07c3e-118">在該時間之後建立的 blob 將會複製到目的地。</span><span class="sxs-lookup"><span data-stu-id="07c3e-118">Blobs created after the time will be replicated to the destination..</span></span>

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

### <span data-ttu-id="07c3e-119">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="07c3e-119">-PrefixMatch</span></span>
<span data-ttu-id="07c3e-120">篩選結果，只複製名稱以指定的首碼開頭的 blob。</span><span class="sxs-lookup"><span data-stu-id="07c3e-120">Filters the results to replicate only blobs whose names begin with the specified prefix.</span></span>

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

### <span data-ttu-id="07c3e-121">-RuleId</span><span class="sxs-lookup"><span data-stu-id="07c3e-121">-RuleId</span></span>
<span data-ttu-id="07c3e-122">物件複製規則 Id。</span><span class="sxs-lookup"><span data-stu-id="07c3e-122">Object Replication Rule Id.</span></span>

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

### <span data-ttu-id="07c3e-123">-SourceContainer</span><span class="sxs-lookup"><span data-stu-id="07c3e-123">-SourceContainer</span></span>
<span data-ttu-id="07c3e-124">要從中複製的來源容器名稱。</span><span class="sxs-lookup"><span data-stu-id="07c3e-124">The Source Container name to replicate from.</span></span>

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

### <span data-ttu-id="07c3e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07c3e-125">CommonParameters</span></span>
<span data-ttu-id="07c3e-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="07c3e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07c3e-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="07c3e-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07c3e-128">輸入</span><span class="sxs-lookup"><span data-stu-id="07c3e-128">INPUTS</span></span>

### <span data-ttu-id="07c3e-129">所有</span><span class="sxs-lookup"><span data-stu-id="07c3e-129">None</span></span>

## <span data-ttu-id="07c3e-130">輸出</span><span class="sxs-lookup"><span data-stu-id="07c3e-130">OUTPUTS</span></span>

### <span data-ttu-id="07c3e-131">PSObjectReplicationPolicyRule 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="07c3e-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="07c3e-132">筆記</span><span class="sxs-lookup"><span data-stu-id="07c3e-132">NOTES</span></span>

## <span data-ttu-id="07c3e-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="07c3e-133">RELATED LINKS</span></span>
