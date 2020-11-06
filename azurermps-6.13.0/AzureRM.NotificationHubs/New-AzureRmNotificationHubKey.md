---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubKey.md
ms.openlocfilehash: d129d34ab9bcbcd67a7c643e4f412bacf262b293
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455960"
---
# <span data-ttu-id="3dbb5-101">New-AzureRmNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="3dbb5-101">New-AzureRmNotificationHubKey</span></span>

## <span data-ttu-id="3dbb5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3dbb5-102">SYNOPSIS</span></span>
<span data-ttu-id="3dbb5-103">重新產生 NotificationHub 的授權規則金鑰。</span><span class="sxs-lookup"><span data-stu-id="3dbb5-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3dbb5-104">句法</span><span class="sxs-lookup"><span data-stu-id="3dbb5-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dbb5-105">說明</span><span class="sxs-lookup"><span data-stu-id="3dbb5-105">DESCRIPTION</span></span>
<span data-ttu-id="3dbb5-106">New-AzureRmNotificationHubKey Cmdlet 會為 NotificationHub 授權規則重新產生主鍵/次鍵。</span><span class="sxs-lookup"><span data-stu-id="3dbb5-106">New-AzureRmNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="3dbb5-107">示例</span><span class="sxs-lookup"><span data-stu-id="3dbb5-107">EXAMPLES</span></span>

### <span data-ttu-id="3dbb5-108">範例1</span><span class="sxs-lookup"><span data-stu-id="3dbb5-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="3dbb5-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="3dbb5-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="3dbb5-110">參數</span><span class="sxs-lookup"><span data-stu-id="3dbb5-110">PARAMETERS</span></span>

### <span data-ttu-id="3dbb5-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3dbb5-111">-AuthorizationRule</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dbb5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dbb5-112">-DefaultProfile</span></span>
<span data-ttu-id="3dbb5-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3dbb5-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dbb5-114">-Force</span><span class="sxs-lookup"><span data-stu-id="3dbb5-114">-Force</span></span>
<span data-ttu-id="3dbb5-115">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="3dbb5-115">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dbb5-116">-命名空間</span><span class="sxs-lookup"><span data-stu-id="3dbb5-116">-Namespace</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dbb5-117">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="3dbb5-117">-NotificationHub</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dbb5-118">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="3dbb5-118">-PolicyKey</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dbb5-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3dbb5-119">-ResourceGroup</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dbb5-120">-確認</span><span class="sxs-lookup"><span data-stu-id="3dbb5-120">-Confirm</span></span>
<span data-ttu-id="3dbb5-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3dbb5-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dbb5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dbb5-122">-WhatIf</span></span>
<span data-ttu-id="3dbb5-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3dbb5-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dbb5-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3dbb5-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dbb5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dbb5-125">CommonParameters</span></span>
<span data-ttu-id="3dbb5-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3dbb5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dbb5-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3dbb5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dbb5-128">輸入</span><span class="sxs-lookup"><span data-stu-id="3dbb5-128">INPUTS</span></span>

### <span data-ttu-id="3dbb5-129">System.object</span><span class="sxs-lookup"><span data-stu-id="3dbb5-129">System.String</span></span>

## <span data-ttu-id="3dbb5-130">輸出</span><span class="sxs-lookup"><span data-stu-id="3dbb5-130">OUTPUTS</span></span>

### <span data-ttu-id="3dbb5-131">ResourceListKeys 中的 NotificationHubs。</span><span class="sxs-lookup"><span data-stu-id="3dbb5-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="3dbb5-132">筆記</span><span class="sxs-lookup"><span data-stu-id="3dbb5-132">NOTES</span></span>

## <span data-ttu-id="3dbb5-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="3dbb5-133">RELATED LINKS</span></span>
