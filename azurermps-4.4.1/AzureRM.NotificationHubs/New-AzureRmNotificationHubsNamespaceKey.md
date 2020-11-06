---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
ms.openlocfilehash: ba33dd46a899f03539c39e61368570fb2bce0537
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448082"
---
# <span data-ttu-id="40fec-101">New-AzureRmNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="40fec-101">New-AzureRmNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="40fec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="40fec-102">SYNOPSIS</span></span>
<span data-ttu-id="40fec-103">重新產生命名空間的授權規則金鑰。</span><span class="sxs-lookup"><span data-stu-id="40fec-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40fec-104">句法</span><span class="sxs-lookup"><span data-stu-id="40fec-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40fec-105">說明</span><span class="sxs-lookup"><span data-stu-id="40fec-105">DESCRIPTION</span></span>
<span data-ttu-id="40fec-106">New-AzureRmNotificationHubNamespaceKey Cmdlet 會為命名空間授權規則重新產生主鍵/次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="40fec-106">New-AzureRmNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="40fec-107">示例</span><span class="sxs-lookup"><span data-stu-id="40fec-107">EXAMPLES</span></span>

### <span data-ttu-id="40fec-108">範例1</span><span class="sxs-lookup"><span data-stu-id="40fec-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="40fec-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="40fec-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="40fec-110">參數</span><span class="sxs-lookup"><span data-stu-id="40fec-110">PARAMETERS</span></span>

### <span data-ttu-id="40fec-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="40fec-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="40fec-112">-Force</span><span class="sxs-lookup"><span data-stu-id="40fec-112">-Force</span></span>
<span data-ttu-id="40fec-113">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="40fec-113">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="40fec-114">-命名空間</span><span class="sxs-lookup"><span data-stu-id="40fec-114">-Namespace</span></span>
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

### <span data-ttu-id="40fec-115">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="40fec-115">-PolicyKey</span></span>
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

### <span data-ttu-id="40fec-116">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="40fec-116">-ResourceGroup</span></span>
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

### <span data-ttu-id="40fec-117">-確認</span><span class="sxs-lookup"><span data-stu-id="40fec-117">-Confirm</span></span>
<span data-ttu-id="40fec-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="40fec-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40fec-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40fec-119">-WhatIf</span></span>
<span data-ttu-id="40fec-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="40fec-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40fec-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="40fec-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40fec-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40fec-122">-DefaultProfile</span></span>
<span data-ttu-id="40fec-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="40fec-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40fec-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40fec-124">CommonParameters</span></span>
<span data-ttu-id="40fec-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="40fec-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40fec-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="40fec-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40fec-127">輸入</span><span class="sxs-lookup"><span data-stu-id="40fec-127">INPUTS</span></span>

## <span data-ttu-id="40fec-128">輸出</span><span class="sxs-lookup"><span data-stu-id="40fec-128">OUTPUTS</span></span>

### <span data-ttu-id="40fec-129">ResourceListKeys 中的 NotificationHubs。</span><span class="sxs-lookup"><span data-stu-id="40fec-129">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="40fec-130">筆記</span><span class="sxs-lookup"><span data-stu-id="40fec-130">NOTES</span></span>

## <span data-ttu-id="40fec-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="40fec-131">RELATED LINKS</span></span>

