---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespacekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
ms.openlocfilehash: a575ae0151cd28a9bcc3580a77ad3a0c79a2984b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958723"
---
# <span data-ttu-id="5ead4-101">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="5ead4-101">New-AzNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="5ead4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ead4-102">SYNOPSIS</span></span>
<span data-ttu-id="5ead4-103">重新產生命名空間的授權規則金鑰。</span><span class="sxs-lookup"><span data-stu-id="5ead4-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

## <span data-ttu-id="5ead4-104">句法</span><span class="sxs-lookup"><span data-stu-id="5ead4-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ead4-105">說明</span><span class="sxs-lookup"><span data-stu-id="5ead4-105">DESCRIPTION</span></span>
<span data-ttu-id="5ead4-106">New-AzNotificationHubNamespaceKey Cmdlet 會為命名空間授權規則重新產生主鍵/次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="5ead4-106">New-AzNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="5ead4-107">示例</span><span class="sxs-lookup"><span data-stu-id="5ead4-107">EXAMPLES</span></span>

### <span data-ttu-id="5ead4-108">範例1</span><span class="sxs-lookup"><span data-stu-id="5ead4-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="5ead4-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="5ead4-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="5ead4-110">參數</span><span class="sxs-lookup"><span data-stu-id="5ead4-110">PARAMETERS</span></span>

### <span data-ttu-id="5ead4-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5ead4-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="5ead4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ead4-112">-DefaultProfile</span></span>
<span data-ttu-id="5ead4-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5ead4-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ead4-114">-Force</span><span class="sxs-lookup"><span data-stu-id="5ead4-114">-Force</span></span>
<span data-ttu-id="5ead4-115">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="5ead4-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5ead4-116">-命名空間</span><span class="sxs-lookup"><span data-stu-id="5ead4-116">-Namespace</span></span>
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

### <span data-ttu-id="5ead4-117">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="5ead4-117">-PolicyKey</span></span>
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

### <span data-ttu-id="5ead4-118">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5ead4-118">-ResourceGroup</span></span>
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

### <span data-ttu-id="5ead4-119">-確認</span><span class="sxs-lookup"><span data-stu-id="5ead4-119">-Confirm</span></span>
<span data-ttu-id="5ead4-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5ead4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ead4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ead4-121">-WhatIf</span></span>
<span data-ttu-id="5ead4-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5ead4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ead4-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5ead4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ead4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ead4-124">CommonParameters</span></span>
<span data-ttu-id="5ead4-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ead4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ead4-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5ead4-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ead4-127">輸入</span><span class="sxs-lookup"><span data-stu-id="5ead4-127">INPUTS</span></span>

### <span data-ttu-id="5ead4-128">System.object</span><span class="sxs-lookup"><span data-stu-id="5ead4-128">System.String</span></span>

## <span data-ttu-id="5ead4-129">輸出</span><span class="sxs-lookup"><span data-stu-id="5ead4-129">OUTPUTS</span></span>

### <span data-ttu-id="5ead4-130">ResourceListKeys 中的 NotificationHubs。</span><span class="sxs-lookup"><span data-stu-id="5ead4-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="5ead4-131">筆記</span><span class="sxs-lookup"><span data-stu-id="5ead4-131">NOTES</span></span>

## <span data-ttu-id="5ead4-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ead4-132">RELATED LINKS</span></span>
