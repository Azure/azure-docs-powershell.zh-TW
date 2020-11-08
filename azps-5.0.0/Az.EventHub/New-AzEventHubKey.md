---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
ms.openlocfilehash: 477884e676118f461578be500715fd3698957003
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140119"
---
# <span data-ttu-id="be314-101">New-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="be314-101">New-AzEventHubKey</span></span>

## <span data-ttu-id="be314-102">摘要</span><span class="sxs-lookup"><span data-stu-id="be314-102">SYNOPSIS</span></span>
<span data-ttu-id="be314-103">針對指定的事件中心授權規則，建立新的主要或次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="be314-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="be314-104">句法</span><span class="sxs-lookup"><span data-stu-id="be314-104">SYNTAX</span></span>

### <span data-ttu-id="be314-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="be314-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be314-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="be314-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be314-107">說明</span><span class="sxs-lookup"><span data-stu-id="be314-107">DESCRIPTION</span></span>
<span data-ttu-id="be314-108">New-AzEventHubKey Cmdlet 會為指定的事件中心授權規則重新產生主要或次要 SAS 金鑰。</span><span class="sxs-lookup"><span data-stu-id="be314-108">The New-AzEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="be314-109">示例</span><span class="sxs-lookup"><span data-stu-id="be314-109">EXAMPLES</span></span>

### <span data-ttu-id="be314-110">範例1： Namespace-AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="be314-110">Example 1: Namespace - AuthorizationRule PrimaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="be314-111">重新生成授權規則 MyAuthRuleName 的主鍵 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="be314-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="be314-112">範例2： EventHub-AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="be314-112">Example 2: EventHub - AuthorizationRule PrimaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="be314-113">重新生成授權規則 MyAuthRuleName 的主鍵 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="be314-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="be314-114">範例3：-Namespace-AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="be314-114">Example 3: - Namespace - AuthorizationRule SecondaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="be314-115">範例4： EventHub-AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="be314-115">Example 4: EventHub - AuthorizationRule SecondaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="be314-116">重新生成授權規則 MyAuthRuleName 的次要金鑰 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="be314-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="be314-117">參數</span><span class="sxs-lookup"><span data-stu-id="be314-117">PARAMETERS</span></span>

### <span data-ttu-id="be314-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be314-118">-DefaultProfile</span></span>
<span data-ttu-id="be314-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="be314-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be314-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="be314-120">-EventHub</span></span>
<span data-ttu-id="be314-121">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="be314-121">EventHub Name</span></span>

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

### <span data-ttu-id="be314-122">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="be314-122">-KeyValue</span></span>
<span data-ttu-id="be314-123">用於簽署及驗證 SAS 權杖的 base64 編碼256位金鑰。</span><span class="sxs-lookup"><span data-stu-id="be314-123">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="be314-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="be314-124">-Name</span></span>
<span data-ttu-id="be314-125">AuthorizationRule 名稱</span><span class="sxs-lookup"><span data-stu-id="be314-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="be314-126">-命名空間</span><span class="sxs-lookup"><span data-stu-id="be314-126">-Namespace</span></span>
<span data-ttu-id="be314-127">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="be314-127">Namespace Name</span></span>

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

### <span data-ttu-id="be314-128">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="be314-128">-RegenerateKey</span></span>
<span data-ttu-id="be314-129">重新產生按鍵-"PrimaryKey"/"SecondaryKey"</span><span class="sxs-lookup"><span data-stu-id="be314-129">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

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

### <span data-ttu-id="be314-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be314-130">-ResourceGroupName</span></span>
<span data-ttu-id="be314-131">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="be314-131">Resource Group Name</span></span>

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

### <span data-ttu-id="be314-132">-確認</span><span class="sxs-lookup"><span data-stu-id="be314-132">-Confirm</span></span>
<span data-ttu-id="be314-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="be314-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be314-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be314-134">-WhatIf</span></span>
<span data-ttu-id="be314-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="be314-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be314-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="be314-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be314-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be314-137">CommonParameters</span></span>
<span data-ttu-id="be314-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="be314-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be314-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="be314-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be314-140">輸入</span><span class="sxs-lookup"><span data-stu-id="be314-140">INPUTS</span></span>

### <span data-ttu-id="be314-141">System.object</span><span class="sxs-lookup"><span data-stu-id="be314-141">System.String</span></span>

## <span data-ttu-id="be314-142">輸出</span><span class="sxs-lookup"><span data-stu-id="be314-142">OUTPUTS</span></span>

### <span data-ttu-id="be314-143">PSListKeysAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="be314-143">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="be314-144">筆記</span><span class="sxs-lookup"><span data-stu-id="be314-144">NOTES</span></span>

## <span data-ttu-id="be314-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="be314-145">RELATED LINKS</span></span>
