---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 75320133-E7B1-40D4-B16D-567686D5AE99
online version: ''
schema: 2.0.0
ms.openlocfilehash: 40d3bdc73ce6bcbb199cf99bb0586de52f05e132
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967433"
---
# <span data-ttu-id="4b7b2-101">New-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4b7b2-101">New-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="4b7b2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4b7b2-102">SYNOPSIS</span></span>
<span data-ttu-id="4b7b2-103">建立新的服務匯流排授權規則。</span><span class="sxs-lookup"><span data-stu-id="4b7b2-103">Creates new Service Bus authorization rule.</span></span>

## <span data-ttu-id="4b7b2-104">句法</span><span class="sxs-lookup"><span data-stu-id="4b7b2-104">SYNTAX</span></span>

### <span data-ttu-id="4b7b2-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="4b7b2-105">EntitySAS</span></span>
```
New-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4b7b2-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="4b7b2-106">NamespaceSAS</span></span>
```
New-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4b7b2-107">說明</span><span class="sxs-lookup"><span data-stu-id="4b7b2-107">DESCRIPTION</span></span>
<span data-ttu-id="4b7b2-108">**新的-AzureSBAuthorizationRule** Cmdlet 會建立服務匯流排授權規則。</span><span class="sxs-lookup"><span data-stu-id="4b7b2-108">The **New-AzureSBAuthorizationRule** cmdlet creates a Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="4b7b2-109">示例</span><span class="sxs-lookup"><span data-stu-id="4b7b2-109">EXAMPLES</span></span>

### <span data-ttu-id="4b7b2-110">範例1：使用產生的主鍵建立授權規則</span><span class="sxs-lookup"><span data-stu-id="4b7b2-110">Example 1: Create an authorization rule with generated primary key</span></span>
```
PS C:\> New-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="4b7b2-111">在具有傳送許可權的命名空間層級建立新的授權規則。</span><span class="sxs-lookup"><span data-stu-id="4b7b2-111">Creates new authorization rule on namespace level with Send permission.</span></span>

### <span data-ttu-id="4b7b2-112">範例2：透過提供主鍵來建立授權規則</span><span class="sxs-lookup"><span data-stu-id="4b7b2-112">Example 2: Creates an authorization rule by providing the primary key</span></span>
```
PS C:\> New-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Manage", "Listen", "Send") -EntityName MyEntity -EntityType Queue -PrimaryKey P+lL/Mnd2Z9sj5hwMrRyAxQDdX8RHfbdqU2eIAqs1rc=
```

<span data-ttu-id="4b7b2-113">在具有擁有權限的 MyEntity 佇列層級建立新的授權規則。</span><span class="sxs-lookup"><span data-stu-id="4b7b2-113">Creates new authorization rule on MyEntity Queue level with all permissions.</span></span>

## <span data-ttu-id="4b7b2-114">參數</span><span class="sxs-lookup"><span data-stu-id="4b7b2-114">PARAMETERS</span></span>

### <span data-ttu-id="4b7b2-115">-EntityName</span><span class="sxs-lookup"><span data-stu-id="4b7b2-115">-EntityName</span></span>
<span data-ttu-id="4b7b2-116">指定要套用規則的機構名稱。</span><span class="sxs-lookup"><span data-stu-id="4b7b2-116">Specifies the entity name to apply rule at.</span></span>

```yaml
Type: String
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7b2-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="4b7b2-117">-EntityType</span></span>
<span data-ttu-id="4b7b2-118">指定實體類型。</span><span class="sxs-lookup"><span data-stu-id="4b7b2-118">Specifies the entity type.</span></span>
<span data-ttu-id="4b7b2-119">有效值為：</span><span class="sxs-lookup"><span data-stu-id="4b7b2-119">Valid values are:</span></span>
  
- <span data-ttu-id="4b7b2-120">序列</span><span class="sxs-lookup"><span data-stu-id="4b7b2-120">Queue</span></span>
- <span data-ttu-id="4b7b2-121">主題</span><span class="sxs-lookup"><span data-stu-id="4b7b2-121">Topic</span></span>
- <span data-ttu-id="4b7b2-122">轉送</span><span class="sxs-lookup"><span data-stu-id="4b7b2-122">Relay</span></span>
- <span data-ttu-id="4b7b2-123">NotificationHub</span><span class="sxs-lookup"><span data-stu-id="4b7b2-123">NotificationHub</span></span>

```yaml
Type: ServiceBusEntityType
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7b2-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="4b7b2-124">-Name</span></span>
<span data-ttu-id="4b7b2-125">指定唯一的授權規則名稱。</span><span class="sxs-lookup"><span data-stu-id="4b7b2-125">Specifies the unique authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b7b2-126">-命名空間</span><span class="sxs-lookup"><span data-stu-id="4b7b2-126">-Namespace</span></span>
<span data-ttu-id="4b7b2-127">指定要套用授權規則的命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="4b7b2-127">Specifies the namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="4b7b2-128">如果沒有任何 *EntityName* 提供該規則，則會位於命名空間層級。</span><span class="sxs-lookup"><span data-stu-id="4b7b2-128">If no *EntityName* provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="4b7b2-129">-許可權</span><span class="sxs-lookup"><span data-stu-id="4b7b2-129">-Permission</span></span>
<span data-ttu-id="4b7b2-130"> (傳送、管理、偵聽) 的授權許可權。</span><span class="sxs-lookup"><span data-stu-id="4b7b2-130">The authorization permissions (Send, Manage, Listen).</span></span>

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

### <span data-ttu-id="4b7b2-131">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="4b7b2-131">-PrimaryKey</span></span>
<span data-ttu-id="4b7b2-132">指定共用存取簽章主鍵。</span><span class="sxs-lookup"><span data-stu-id="4b7b2-132">Specifies the Shared Access Signature primary key.</span></span>
<span data-ttu-id="4b7b2-133">如果未提供，就會產生。</span><span class="sxs-lookup"><span data-stu-id="4b7b2-133">Will be generated if not provided.</span></span>

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

### <span data-ttu-id="4b7b2-134">-設定檔</span><span class="sxs-lookup"><span data-stu-id="4b7b2-134">-Profile</span></span>
<span data-ttu-id="4b7b2-135">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="4b7b2-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4b7b2-136">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="4b7b2-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4b7b2-137">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="4b7b2-137">-SecondaryKey</span></span>
<span data-ttu-id="4b7b2-138">指定共用存取簽章輔助金鑰。</span><span class="sxs-lookup"><span data-stu-id="4b7b2-138">Specifies the Shared Access Signature secondary key.</span></span>

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

### <span data-ttu-id="4b7b2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b7b2-139">CommonParameters</span></span>
<span data-ttu-id="4b7b2-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4b7b2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b7b2-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4b7b2-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b7b2-142">輸入</span><span class="sxs-lookup"><span data-stu-id="4b7b2-142">INPUTS</span></span>

## <span data-ttu-id="4b7b2-143">輸出</span><span class="sxs-lookup"><span data-stu-id="4b7b2-143">OUTPUTS</span></span>

## <span data-ttu-id="4b7b2-144">筆記</span><span class="sxs-lookup"><span data-stu-id="4b7b2-144">NOTES</span></span>

## <span data-ttu-id="4b7b2-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="4b7b2-145">RELATED LINKS</span></span>

[<span data-ttu-id="4b7b2-146">AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4b7b2-146">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="4b7b2-147">移除-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4b7b2-147">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)

[<span data-ttu-id="4b7b2-148">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4b7b2-148">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


