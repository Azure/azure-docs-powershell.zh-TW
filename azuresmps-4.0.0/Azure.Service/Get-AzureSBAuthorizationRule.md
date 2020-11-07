---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D7B2CDFF-D9A2-48C7-B331-132A6A6843CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 10fdb8920164857b42ac57a3c989417c2a967ab9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967060"
---
# <span data-ttu-id="482a9-101">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="482a9-101">Get-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="482a9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="482a9-102">SYNOPSIS</span></span>
<span data-ttu-id="482a9-103">取得服務匯流排授權規則。</span><span class="sxs-lookup"><span data-stu-id="482a9-103">Gets Service bus authorization rules.</span></span>


## <span data-ttu-id="482a9-104">句法</span><span class="sxs-lookup"><span data-stu-id="482a9-104">SYNTAX</span></span>

### <span data-ttu-id="482a9-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="482a9-105">EntitySAS</span></span>
```
Get-AzureSBAuthorizationRule [-Name <String>] [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="482a9-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="482a9-106">NamespaceSAS</span></span>
```
Get-AzureSBAuthorizationRule [-Name <String>] [-Permission <AccessRights[]>] -Namespace <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="482a9-107">說明</span><span class="sxs-lookup"><span data-stu-id="482a9-107">DESCRIPTION</span></span>
<span data-ttu-id="482a9-108">取得服務匯流排授權規則。</span><span class="sxs-lookup"><span data-stu-id="482a9-108">Gets Service bus authorization rules.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="482a9-109">示例</span><span class="sxs-lookup"><span data-stu-id="482a9-109">EXAMPLES</span></span>

### <span data-ttu-id="482a9-110">範例1：在命名空間層級取得授權規則</span><span class="sxs-lookup"><span data-stu-id="482a9-110">Example 1: Get authorization rule at namespace level</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace
```

<span data-ttu-id="482a9-111">取得 MyNamespace 上所有可用的授權規則。</span><span class="sxs-lookup"><span data-stu-id="482a9-111">Gets all available authorization rules at MyNamespace.</span></span>

### <span data-ttu-id="482a9-112">範例2：取得佇列的授權規則</span><span class="sxs-lookup"><span data-stu-id="482a9-112">Example 2: Get authorization rule for a Queue</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="482a9-113">取得 MyNamespace 上的 MyEntity 佇列中所有可用的授權規則。</span><span class="sxs-lookup"><span data-stu-id="482a9-113">Gets all available authorization rules a MyEntity Queue on MyNamespace.</span></span>

### <span data-ttu-id="482a9-114">範例3：依名稱取得授權規則</span><span class="sxs-lookup"><span data-stu-id="482a9-114">Example 3: Get authorization rule by name</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace
```

<span data-ttu-id="482a9-115">取得在 MyNamespace 層級上稱為 MyRule 的授權規則。</span><span class="sxs-lookup"><span data-stu-id="482a9-115">Gets an authorization rule called MyRule on MyNamespace level.</span></span>

### <span data-ttu-id="482a9-116">範例4：按照許可權取得授權規則</span><span class="sxs-lookup"><span data-stu-id="482a9-116">Example 4: Get authorization rule by permission</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="482a9-117">取得具有命名空間層級之傳送許可權的所有授權規則。</span><span class="sxs-lookup"><span data-stu-id="482a9-117">Gets all authorization rules that have send permission on namespace level.</span></span>

## <span data-ttu-id="482a9-118">參數</span><span class="sxs-lookup"><span data-stu-id="482a9-118">PARAMETERS</span></span>

### <span data-ttu-id="482a9-119">-EntityName</span><span class="sxs-lookup"><span data-stu-id="482a9-119">-EntityName</span></span>
<span data-ttu-id="482a9-120">要套用規則的機構名稱。</span><span class="sxs-lookup"><span data-stu-id="482a9-120">The entity name to apply rule at.</span></span>

```yaml
Type: String
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="482a9-121">-EntityType</span><span class="sxs-lookup"><span data-stu-id="482a9-121">-EntityType</span></span>
<span data-ttu-id="482a9-122">實體類型 (佇列、主題、繼電器、NotificationHub) 。</span><span class="sxs-lookup"><span data-stu-id="482a9-122">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

```yaml
Type: ServiceBusEntityType
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="482a9-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="482a9-123">-Name</span></span>
<span data-ttu-id="482a9-124">唯一的授權規則名稱。</span><span class="sxs-lookup"><span data-stu-id="482a9-124">The unique authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="482a9-125">-命名空間</span><span class="sxs-lookup"><span data-stu-id="482a9-125">-Namespace</span></span>
<span data-ttu-id="482a9-126">要套用授權規則的命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="482a9-126">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="482a9-127">如果沒有任何 EntityName 提供該規則，則會位於命名空間層級。</span><span class="sxs-lookup"><span data-stu-id="482a9-127">If no EntityName provided the rule will be on the namespace level.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="482a9-128">-許可權</span><span class="sxs-lookup"><span data-stu-id="482a9-128">-Permission</span></span>
<span data-ttu-id="482a9-129">篩選 (傳送、管理、偵聽) 的授權許可權。</span><span class="sxs-lookup"><span data-stu-id="482a9-129">The authorization permissions to filter (Send, Manage, Listen).</span></span>
<span data-ttu-id="482a9-130">這會使用完全相符的專案。</span><span class="sxs-lookup"><span data-stu-id="482a9-130">This uses exact match.</span></span>

```yaml
Type: AccessRights[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="482a9-131">-設定檔</span><span class="sxs-lookup"><span data-stu-id="482a9-131">-Profile</span></span>
<span data-ttu-id="482a9-132">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="482a9-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="482a9-133">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="482a9-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="482a9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="482a9-134">CommonParameters</span></span>
<span data-ttu-id="482a9-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="482a9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="482a9-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="482a9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="482a9-137">輸入</span><span class="sxs-lookup"><span data-stu-id="482a9-137">INPUTS</span></span>

## <span data-ttu-id="482a9-138">輸出</span><span class="sxs-lookup"><span data-stu-id="482a9-138">OUTPUTS</span></span>

## <span data-ttu-id="482a9-139">筆記</span><span class="sxs-lookup"><span data-stu-id="482a9-139">NOTES</span></span>

## <span data-ttu-id="482a9-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="482a9-140">RELATED LINKS</span></span>

[<span data-ttu-id="482a9-141">新-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="482a9-141">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="482a9-142">移除-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="482a9-142">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)

[<span data-ttu-id="482a9-143">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="482a9-143">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


