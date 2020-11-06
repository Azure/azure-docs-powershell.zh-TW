---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubKey.md
ms.openlocfilehash: 66d947cc9d5765fdbfeb815019bbd739f7c3d819
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456156"
---
# <span data-ttu-id="43b70-101">New-AzureRmNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="43b70-101">New-AzureRmNotificationHubKey</span></span>

## <span data-ttu-id="43b70-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43b70-102">SYNOPSIS</span></span>
<span data-ttu-id="43b70-103">重新產生 NotificationHub 的授權規則金鑰。</span><span class="sxs-lookup"><span data-stu-id="43b70-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43b70-104">句法</span><span class="sxs-lookup"><span data-stu-id="43b70-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43b70-105">說明</span><span class="sxs-lookup"><span data-stu-id="43b70-105">DESCRIPTION</span></span>
<span data-ttu-id="43b70-106">New-AzureRmNotificationHubKey Cmdlet 會為 NotificationHub 授權規則重新產生主鍵/次鍵。</span><span class="sxs-lookup"><span data-stu-id="43b70-106">New-AzureRmNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="43b70-107">示例</span><span class="sxs-lookup"><span data-stu-id="43b70-107">EXAMPLES</span></span>

### <span data-ttu-id="43b70-108">範例1</span><span class="sxs-lookup"><span data-stu-id="43b70-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="43b70-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="43b70-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="43b70-110">參數</span><span class="sxs-lookup"><span data-stu-id="43b70-110">PARAMETERS</span></span>

### <span data-ttu-id="43b70-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="43b70-111">-AuthorizationRule</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43b70-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43b70-112">-DefaultProfile</span></span>
<span data-ttu-id="43b70-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="43b70-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43b70-114">-Force</span><span class="sxs-lookup"><span data-stu-id="43b70-114">-Force</span></span>
<span data-ttu-id="43b70-115">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="43b70-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="43b70-116">-命名空間</span><span class="sxs-lookup"><span data-stu-id="43b70-116">-Namespace</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43b70-117">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="43b70-117">-NotificationHub</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43b70-118">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="43b70-118">-PolicyKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43b70-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="43b70-119">-ResourceGroup</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43b70-120">-確認</span><span class="sxs-lookup"><span data-stu-id="43b70-120">-Confirm</span></span>
<span data-ttu-id="43b70-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="43b70-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43b70-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43b70-122">-WhatIf</span></span>
<span data-ttu-id="43b70-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="43b70-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43b70-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="43b70-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43b70-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43b70-125">CommonParameters</span></span>
<span data-ttu-id="43b70-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43b70-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43b70-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="43b70-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43b70-128">輸入</span><span class="sxs-lookup"><span data-stu-id="43b70-128">INPUTS</span></span>

### <span data-ttu-id="43b70-129">所有</span><span class="sxs-lookup"><span data-stu-id="43b70-129">None</span></span>
<span data-ttu-id="43b70-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="43b70-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="43b70-131">輸出</span><span class="sxs-lookup"><span data-stu-id="43b70-131">OUTPUTS</span></span>

### <span data-ttu-id="43b70-132">ResourceListKeys 中的 NotificationHubs。</span><span class="sxs-lookup"><span data-stu-id="43b70-132">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="43b70-133">筆記</span><span class="sxs-lookup"><span data-stu-id="43b70-133">NOTES</span></span>

## <span data-ttu-id="43b70-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="43b70-134">RELATED LINKS</span></span>

