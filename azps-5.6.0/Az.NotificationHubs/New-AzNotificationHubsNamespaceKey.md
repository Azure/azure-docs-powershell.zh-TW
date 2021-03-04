---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhubsnamespacekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
ms.openlocfilehash: 2d3fb02aa41d58521d35382aa35eb47c4b1d523c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901713"
---
# <span data-ttu-id="e72ab-101">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="e72ab-101">New-AzNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="e72ab-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e72ab-102">SYNOPSIS</span></span>
<span data-ttu-id="e72ab-103">重新產生命名空間的授權規則金鑰。</span><span class="sxs-lookup"><span data-stu-id="e72ab-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

## <span data-ttu-id="e72ab-104">語法</span><span class="sxs-lookup"><span data-stu-id="e72ab-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e72ab-105">描述</span><span class="sxs-lookup"><span data-stu-id="e72ab-105">DESCRIPTION</span></span>
<span data-ttu-id="e72ab-106">New-AzNotificationHubNamespaceKey Cmdlet 會重新產生命名空間授權規則的主鍵/次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="e72ab-106">New-AzNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="e72ab-107">例子</span><span class="sxs-lookup"><span data-stu-id="e72ab-107">EXAMPLES</span></span>

### <span data-ttu-id="e72ab-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="e72ab-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="e72ab-109">{{ 在這裡新增範例描述 }}</span><span class="sxs-lookup"><span data-stu-id="e72ab-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="e72ab-110">參數</span><span class="sxs-lookup"><span data-stu-id="e72ab-110">PARAMETERS</span></span>

### <span data-ttu-id="e72ab-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e72ab-111">-AuthorizationRule</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e72ab-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e72ab-112">-DefaultProfile</span></span>
<span data-ttu-id="e72ab-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="e72ab-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e72ab-114">-強制</span><span class="sxs-lookup"><span data-stu-id="e72ab-114">-Force</span></span>
<span data-ttu-id="e72ab-115">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="e72ab-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e72ab-116">-命名空間</span><span class="sxs-lookup"><span data-stu-id="e72ab-116">-Namespace</span></span>
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

### <span data-ttu-id="e72ab-117">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="e72ab-117">-PolicyKey</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e72ab-118">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e72ab-118">-ResourceGroup</span></span>
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

### <span data-ttu-id="e72ab-119">-確認</span><span class="sxs-lookup"><span data-stu-id="e72ab-119">-Confirm</span></span>
<span data-ttu-id="e72ab-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e72ab-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e72ab-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e72ab-121">-WhatIf</span></span>
<span data-ttu-id="e72ab-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e72ab-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e72ab-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e72ab-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e72ab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e72ab-124">CommonParameters</span></span>
<span data-ttu-id="e72ab-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e72ab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e72ab-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e72ab-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e72ab-127">輸入</span><span class="sxs-lookup"><span data-stu-id="e72ab-127">INPUTS</span></span>

### <span data-ttu-id="e72ab-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e72ab-128">System.String</span></span>

## <span data-ttu-id="e72ab-129">輸出</span><span class="sxs-lookup"><span data-stu-id="e72ab-129">OUTPUTS</span></span>

### <span data-ttu-id="e72ab-130">Microsoft.Azure.management.NotificationHubs.models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="e72ab-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="e72ab-131">筆記</span><span class="sxs-lookup"><span data-stu-id="e72ab-131">NOTES</span></span>

## <span data-ttu-id="e72ab-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="e72ab-132">RELATED LINKS</span></span>
