---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 17065902-97EA-4F5F-926B-B7CBEE3EAF84
online version: ''
schema: 2.0.0
ms.openlocfilehash: ab76cf3052f28b0ff89e3e41aaa08127cc33411e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967266"
---
# <span data-ttu-id="1907c-101">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1907c-101">Set-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="1907c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1907c-102">SYNOPSIS</span></span>
<span data-ttu-id="1907c-103">更新現有的服務匯流排授權規則。</span><span class="sxs-lookup"><span data-stu-id="1907c-103">Updates existing Service Bus authorization rule.</span></span>

## <span data-ttu-id="1907c-104">句法</span><span class="sxs-lookup"><span data-stu-id="1907c-104">SYNTAX</span></span>

### <span data-ttu-id="1907c-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="1907c-105">EntitySAS</span></span>
```
Set-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1907c-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="1907c-106">NamespaceSAS</span></span>
```
Set-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1907c-107">說明</span><span class="sxs-lookup"><span data-stu-id="1907c-107">DESCRIPTION</span></span>
<span data-ttu-id="1907c-108">更新現有的服務匯流排授權規則。</span><span class="sxs-lookup"><span data-stu-id="1907c-108">Updates existing Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="1907c-109">示例</span><span class="sxs-lookup"><span data-stu-id="1907c-109">EXAMPLES</span></span>

### <span data-ttu-id="1907c-110">範例1：針對命名空間層級的授權規則續約主鍵</span><span class="sxs-lookup"><span data-stu-id="1907c-110">Example 1: Renew primary key for authorization rule at namespace level</span></span>
```
PS C:\> Set-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="1907c-111">主鍵已更新。</span><span class="sxs-lookup"><span data-stu-id="1907c-111">The primary key is renewed.</span></span>

### <span data-ttu-id="1907c-112">範例2：更新授權規則許可權</span><span class="sxs-lookup"><span data-stu-id="1907c-112">Example 2: Update authorization rule permission</span></span>
```
PS C:\> Set-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Listen", "Send") -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="1907c-113">更新許可權。</span><span class="sxs-lookup"><span data-stu-id="1907c-113">Updates the permissions.</span></span>

## <span data-ttu-id="1907c-114">參數</span><span class="sxs-lookup"><span data-stu-id="1907c-114">PARAMETERS</span></span>

### <span data-ttu-id="1907c-115">-EntityName</span><span class="sxs-lookup"><span data-stu-id="1907c-115">-EntityName</span></span>
<span data-ttu-id="1907c-116">要套用規則的機構名稱。</span><span class="sxs-lookup"><span data-stu-id="1907c-116">The entity name to apply rule at.</span></span>

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

### <span data-ttu-id="1907c-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="1907c-117">-EntityType</span></span>
<span data-ttu-id="1907c-118">實體類型 (佇列、主題、繼電器、NotificationHub) 。</span><span class="sxs-lookup"><span data-stu-id="1907c-118">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

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

### <span data-ttu-id="1907c-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="1907c-119">-Name</span></span>
<span data-ttu-id="1907c-120">唯一的授權規則名稱。</span><span class="sxs-lookup"><span data-stu-id="1907c-120">The unique authorization rule name.</span></span>

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

### <span data-ttu-id="1907c-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="1907c-121">-Namespace</span></span>
<span data-ttu-id="1907c-122">要套用授權規則的命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="1907c-122">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="1907c-123">如果沒有任何 EntityName 提供該規則，則會位於命名空間層級。</span><span class="sxs-lookup"><span data-stu-id="1907c-123">If no EntityName provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="1907c-124">-許可權</span><span class="sxs-lookup"><span data-stu-id="1907c-124">-Permission</span></span>
<span data-ttu-id="1907c-125"> (傳送、管理、偵聽) 的授權許可權。</span><span class="sxs-lookup"><span data-stu-id="1907c-125">The authorization permissions (Send, Manage, Listen).</span></span>

```yaml
Type: AccessRights[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1907c-126">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="1907c-126">-PrimaryKey</span></span>
<span data-ttu-id="1907c-127">共用訪問簽章主鍵。</span><span class="sxs-lookup"><span data-stu-id="1907c-127">The Shared Access Signature primary key.</span></span>
<span data-ttu-id="1907c-128">如果未提供，就會產生。</span><span class="sxs-lookup"><span data-stu-id="1907c-128">Will be generated if not provided.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1907c-129">-設定檔</span><span class="sxs-lookup"><span data-stu-id="1907c-129">-Profile</span></span>
<span data-ttu-id="1907c-130">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="1907c-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1907c-131">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="1907c-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1907c-132">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="1907c-132">-SecondaryKey</span></span>
<span data-ttu-id="1907c-133">共用存取簽名次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="1907c-133">The Shared Access Signature secondary key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1907c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1907c-134">CommonParameters</span></span>
<span data-ttu-id="1907c-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1907c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1907c-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1907c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1907c-137">輸入</span><span class="sxs-lookup"><span data-stu-id="1907c-137">INPUTS</span></span>

## <span data-ttu-id="1907c-138">輸出</span><span class="sxs-lookup"><span data-stu-id="1907c-138">OUTPUTS</span></span>

## <span data-ttu-id="1907c-139">筆記</span><span class="sxs-lookup"><span data-stu-id="1907c-139">NOTES</span></span>

## <span data-ttu-id="1907c-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="1907c-140">RELATED LINKS</span></span>

[<span data-ttu-id="1907c-141">AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1907c-141">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="1907c-142">新-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1907c-142">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="1907c-143">移除-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1907c-143">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)


