---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
ms.openlocfilehash: 891e72945e3557ad1047b007504572a981449cd9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625576"
---
# <span data-ttu-id="0234c-101">New-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="0234c-101">New-AzureRmEventHubKey</span></span>

## <span data-ttu-id="0234c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0234c-102">SYNOPSIS</span></span>
<span data-ttu-id="0234c-103">針對指定的事件中心授權規則，建立新的主要或次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="0234c-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0234c-104">句法</span><span class="sxs-lookup"><span data-stu-id="0234c-104">SYNTAX</span></span>

### <span data-ttu-id="0234c-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0234c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0234c-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="0234c-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0234c-107">說明</span><span class="sxs-lookup"><span data-stu-id="0234c-107">DESCRIPTION</span></span>
<span data-ttu-id="0234c-108">New-AzureRmEventHubKey Cmdlet 會為指定的事件中心授權規則重新產生主要或次要 SAS 金鑰。</span><span class="sxs-lookup"><span data-stu-id="0234c-108">The New-AzureRmEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="0234c-109">示例</span><span class="sxs-lookup"><span data-stu-id="0234c-109">EXAMPLES</span></span>

### <span data-ttu-id="0234c-110">範例 1.1-命名空間-AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="0234c-110">Example 1.1 - Namespace - AuthorizationRule PrimaryKey</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="0234c-111">重新生成授權規則 MyAuthRuleName 的主鍵 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="0234c-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="0234c-112">範例 1.2-AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="0234c-112">Example 1.2 - EventHub - AuthorizationRule PrimaryKey</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="0234c-113">重新生成授權規則 MyAuthRuleName 的主鍵 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="0234c-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="0234c-114">範例 2.1-命名空間-AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="0234c-114">Example 2.1  - Namespace - AuthorizationRule SecondaryKey</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="0234c-115">範例 2.2-EventHub-AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="0234c-115">Example 2.2 - EventHub - AuthorizationRule SecondaryKey</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="0234c-116">重新生成授權規則 MyAuthRuleName 的次要金鑰 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="0234c-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="0234c-117">參數</span><span class="sxs-lookup"><span data-stu-id="0234c-117">PARAMETERS</span></span>

### <span data-ttu-id="0234c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0234c-118">-DefaultProfile</span></span>
<span data-ttu-id="0234c-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0234c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0234c-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="0234c-120">-EventHub</span></span>
<span data-ttu-id="0234c-121">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="0234c-121">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0234c-122">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="0234c-122">-KeyValue</span></span>
<span data-ttu-id="0234c-123">用於簽署及驗證 SAS 權杖的 base64 編碼256位金鑰。</span><span class="sxs-lookup"><span data-stu-id="0234c-123">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0234c-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="0234c-124">-Name</span></span>
<span data-ttu-id="0234c-125">AuthorizationRule 名稱</span><span class="sxs-lookup"><span data-stu-id="0234c-125">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0234c-126">-命名空間</span><span class="sxs-lookup"><span data-stu-id="0234c-126">-Namespace</span></span>
<span data-ttu-id="0234c-127">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="0234c-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0234c-128">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="0234c-128">-RegenerateKey</span></span>
<span data-ttu-id="0234c-129">重新產生按鍵-"PrimaryKey"/"SecondaryKey"</span><span class="sxs-lookup"><span data-stu-id="0234c-129">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

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

### <span data-ttu-id="0234c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0234c-130">-ResourceGroupName</span></span>
<span data-ttu-id="0234c-131">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="0234c-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0234c-132">-確認</span><span class="sxs-lookup"><span data-stu-id="0234c-132">-Confirm</span></span>
<span data-ttu-id="0234c-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0234c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0234c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0234c-134">-WhatIf</span></span>
<span data-ttu-id="0234c-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0234c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0234c-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0234c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0234c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0234c-137">CommonParameters</span></span>
<span data-ttu-id="0234c-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0234c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0234c-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0234c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0234c-140">輸入</span><span class="sxs-lookup"><span data-stu-id="0234c-140">INPUTS</span></span>

### <span data-ttu-id="0234c-141">System.object</span><span class="sxs-lookup"><span data-stu-id="0234c-141">System.String</span></span>

## <span data-ttu-id="0234c-142">輸出</span><span class="sxs-lookup"><span data-stu-id="0234c-142">OUTPUTS</span></span>

### <span data-ttu-id="0234c-143">PSListKeysAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="0234c-143">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="0234c-144">筆記</span><span class="sxs-lookup"><span data-stu-id="0234c-144">NOTES</span></span>

## <span data-ttu-id="0234c-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="0234c-145">RELATED LINKS</span></span>
