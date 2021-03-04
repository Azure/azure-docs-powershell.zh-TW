---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
ms.openlocfilehash: 8c6b24dd2d208ea4465138f1e901b030ee5c30e6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901738"
---
# <span data-ttu-id="eb741-101">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="eb741-101">New-AzNotificationHubKey</span></span>

## <span data-ttu-id="eb741-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eb741-102">SYNOPSIS</span></span>
<span data-ttu-id="eb741-103">重新產生 NotificationHub 的授權規則金鑰。</span><span class="sxs-lookup"><span data-stu-id="eb741-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

## <span data-ttu-id="eb741-104">語法</span><span class="sxs-lookup"><span data-stu-id="eb741-104">SYNTAX</span></span>

```
New-AzNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb741-105">描述</span><span class="sxs-lookup"><span data-stu-id="eb741-105">DESCRIPTION</span></span>
<span data-ttu-id="eb741-106">New-AzNotificationHubKey Cmdlet 會重新產生 NotificationHub 授權規則的主鍵/次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="eb741-106">New-AzNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="eb741-107">例子</span><span class="sxs-lookup"><span data-stu-id="eb741-107">EXAMPLES</span></span>

### <span data-ttu-id="eb741-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="eb741-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="eb741-109">{{ 在這裡新增範例描述 }}</span><span class="sxs-lookup"><span data-stu-id="eb741-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="eb741-110">參數</span><span class="sxs-lookup"><span data-stu-id="eb741-110">PARAMETERS</span></span>

### <span data-ttu-id="eb741-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="eb741-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="eb741-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb741-112">-DefaultProfile</span></span>
<span data-ttu-id="eb741-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="eb741-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb741-114">-強制</span><span class="sxs-lookup"><span data-stu-id="eb741-114">-Force</span></span>
<span data-ttu-id="eb741-115">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="eb741-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="eb741-116">-命名空間</span><span class="sxs-lookup"><span data-stu-id="eb741-116">-Namespace</span></span>
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

### <span data-ttu-id="eb741-117">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="eb741-117">-NotificationHub</span></span>
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

### <span data-ttu-id="eb741-118">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="eb741-118">-PolicyKey</span></span>
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

### <span data-ttu-id="eb741-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="eb741-119">-ResourceGroup</span></span>
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

### <span data-ttu-id="eb741-120">-確認</span><span class="sxs-lookup"><span data-stu-id="eb741-120">-Confirm</span></span>
<span data-ttu-id="eb741-121">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="eb741-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb741-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb741-122">-WhatIf</span></span>
<span data-ttu-id="eb741-123">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eb741-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb741-124">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eb741-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb741-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb741-125">CommonParameters</span></span>
<span data-ttu-id="eb741-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eb741-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb741-127">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="eb741-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb741-128">輸入</span><span class="sxs-lookup"><span data-stu-id="eb741-128">INPUTS</span></span>

### <span data-ttu-id="eb741-129">System.String</span><span class="sxs-lookup"><span data-stu-id="eb741-129">System.String</span></span>

## <span data-ttu-id="eb741-130">輸出</span><span class="sxs-lookup"><span data-stu-id="eb741-130">OUTPUTS</span></span>

### <span data-ttu-id="eb741-131">Microsoft.Azure.management.NotificationHubs.models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="eb741-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="eb741-132">筆記</span><span class="sxs-lookup"><span data-stu-id="eb741-132">NOTES</span></span>

## <span data-ttu-id="eb741-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb741-133">RELATED LINKS</span></span>
