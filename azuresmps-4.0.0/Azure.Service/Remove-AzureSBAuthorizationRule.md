---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E246C177-EAEE-4D7A-A544-664F47862FC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92d450a10628ea7e85a49962ac262d4dece8e4c8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967577"
---
# <span data-ttu-id="e57a3-101">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e57a3-101">Remove-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="e57a3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e57a3-102">SYNOPSIS</span></span>
<span data-ttu-id="e57a3-103">移除現有的服務匯流排授權規則。</span><span class="sxs-lookup"><span data-stu-id="e57a3-103">Removes existing Service Bus authorization rule.</span></span>

## <span data-ttu-id="e57a3-104">句法</span><span class="sxs-lookup"><span data-stu-id="e57a3-104">SYNTAX</span></span>

### <span data-ttu-id="e57a3-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="e57a3-105">EntitySAS</span></span>
```
Remove-AzureSBAuthorizationRule -Name <String> -Namespace <String> -EntityName <String>
 -EntityType <ServiceBusEntityType> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e57a3-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="e57a3-106">NamespaceSAS</span></span>
```
Remove-AzureSBAuthorizationRule -Name <String> -Namespace <String> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e57a3-107">說明</span><span class="sxs-lookup"><span data-stu-id="e57a3-107">DESCRIPTION</span></span>
<span data-ttu-id="e57a3-108">移除現有的服務匯流排授權規則。</span><span class="sxs-lookup"><span data-stu-id="e57a3-108">Removes existing Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="e57a3-109">示例</span><span class="sxs-lookup"><span data-stu-id="e57a3-109">EXAMPLES</span></span>

### <span data-ttu-id="e57a3-110">範例1：移除位於命名空間層級的授權規則</span><span class="sxs-lookup"><span data-stu-id="e57a3-110">Example 1: Remove authorization rule at namespace level</span></span>
```
PS C:\> Remove-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace
```

<span data-ttu-id="e57a3-111">從 MyNamespace 中移除授權規則 MyRule。</span><span class="sxs-lookup"><span data-stu-id="e57a3-111">Removes authorization rule MyRule from MyNamespace.</span></span>

### <span data-ttu-id="e57a3-112">範例2：移除佇列的授權規則</span><span class="sxs-lookup"><span data-stu-id="e57a3-112">Example 2: Remove authorization rule for a Queue</span></span>
```
PS C:\> Remove-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="e57a3-113">針對 MyNamespace 中的 MyEntity 佇列移除稱為 MyRule 的授權規則。</span><span class="sxs-lookup"><span data-stu-id="e57a3-113">Removes authorization rule called MyRule for a MyEntity Queue on MyNamespace.</span></span>

## <span data-ttu-id="e57a3-114">參數</span><span class="sxs-lookup"><span data-stu-id="e57a3-114">PARAMETERS</span></span>

### <span data-ttu-id="e57a3-115">-EntityName</span><span class="sxs-lookup"><span data-stu-id="e57a3-115">-EntityName</span></span>
<span data-ttu-id="e57a3-116">要套用規則的機構名稱。</span><span class="sxs-lookup"><span data-stu-id="e57a3-116">The entity name to apply rule at.</span></span>

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

### <span data-ttu-id="e57a3-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="e57a3-117">-EntityType</span></span>
<span data-ttu-id="e57a3-118">實體類型 (佇列、主題、繼電器、NotificationHub) 。</span><span class="sxs-lookup"><span data-stu-id="e57a3-118">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

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

### <span data-ttu-id="e57a3-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="e57a3-119">-Name</span></span>
<span data-ttu-id="e57a3-120">唯一的授權規則名稱。</span><span class="sxs-lookup"><span data-stu-id="e57a3-120">The unique authorization rule name.</span></span>

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

### <span data-ttu-id="e57a3-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="e57a3-121">-Namespace</span></span>
<span data-ttu-id="e57a3-122">要套用授權規則的命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="e57a3-122">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="e57a3-123">如果沒有任何 EntityName 提供該規則，則會位於命名空間層級。</span><span class="sxs-lookup"><span data-stu-id="e57a3-123">If no EntityName provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="e57a3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e57a3-124">-PassThru</span></span>
<span data-ttu-id="e57a3-125">表示此 Cmdlet 會傳回代表其操作專案的物件。</span><span class="sxs-lookup"><span data-stu-id="e57a3-125">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="e57a3-126">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="e57a3-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e57a3-127">-設定檔</span><span class="sxs-lookup"><span data-stu-id="e57a3-127">-Profile</span></span>
<span data-ttu-id="e57a3-128">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e57a3-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e57a3-129">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="e57a3-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e57a3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e57a3-130">CommonParameters</span></span>
<span data-ttu-id="e57a3-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e57a3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e57a3-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e57a3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e57a3-133">輸入</span><span class="sxs-lookup"><span data-stu-id="e57a3-133">INPUTS</span></span>

## <span data-ttu-id="e57a3-134">輸出</span><span class="sxs-lookup"><span data-stu-id="e57a3-134">OUTPUTS</span></span>

## <span data-ttu-id="e57a3-135">筆記</span><span class="sxs-lookup"><span data-stu-id="e57a3-135">NOTES</span></span>

## <span data-ttu-id="e57a3-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="e57a3-136">RELATED LINKS</span></span>

[<span data-ttu-id="e57a3-137">AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e57a3-137">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="e57a3-138">新-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e57a3-138">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="e57a3-139">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e57a3-139">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


