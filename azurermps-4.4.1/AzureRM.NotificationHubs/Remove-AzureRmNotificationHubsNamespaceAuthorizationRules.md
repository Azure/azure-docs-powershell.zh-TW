---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 860AB403-3F99-45FA-8E6A-8C9872C121E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: e9b699e8839f2ba9426945ef0de883c4bfac40d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625124"
---
# <span data-ttu-id="3fd87-101">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="3fd87-101">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="3fd87-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3fd87-102">SYNOPSIS</span></span>
<span data-ttu-id="3fd87-103">從通知中心命名空間移除授權規則。</span><span class="sxs-lookup"><span data-stu-id="3fd87-103">Removes an authorization rule from a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fd87-104">句法</span><span class="sxs-lookup"><span data-stu-id="3fd87-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3fd87-105">說明</span><span class="sxs-lookup"><span data-stu-id="3fd87-105">DESCRIPTION</span></span>
<span data-ttu-id="3fd87-106">**AzureRmNotificationHubsNamespaceAuthorizationRules** Cmdlet 會從通知中心命名空間中移除 (SAS) 授權規則的共用存取簽章。</span><span class="sxs-lookup"><span data-stu-id="3fd87-106">The **Remove-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub namespace.</span></span>

<span data-ttu-id="3fd87-107">授權規則可管理命名空間的存取權。</span><span class="sxs-lookup"><span data-stu-id="3fd87-107">Authorization rules manage access to a namespace.</span></span>
<span data-ttu-id="3fd87-108">這是透過根據不同的許可權等級建立連結（例如 Uri）來完成。</span><span class="sxs-lookup"><span data-stu-id="3fd87-108">This is done by through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="3fd87-109">許可權等級可以是下列各項：</span><span class="sxs-lookup"><span data-stu-id="3fd87-109">Permission levels can be of the following:</span></span> 

- <span data-ttu-id="3fd87-110">聆聽</span><span class="sxs-lookup"><span data-stu-id="3fd87-110">Listen</span></span>
- <span data-ttu-id="3fd87-111">發送</span><span class="sxs-lookup"><span data-stu-id="3fd87-111">Send</span></span>
- <span data-ttu-id="3fd87-112">管理</span><span class="sxs-lookup"><span data-stu-id="3fd87-112">Manage</span></span>

<span data-ttu-id="3fd87-113">用戶端會根據適當的許可權等級，導向到其中一個 Uri。</span><span class="sxs-lookup"><span data-stu-id="3fd87-113">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="3fd87-114">例如，擁有 [偵聽] 許可權的用戶端會定向至該許可權的 URI。</span><span class="sxs-lookup"><span data-stu-id="3fd87-114">For instance, a client given the Listen permission is directed to the URI for that permission.</span></span>

<span data-ttu-id="3fd87-115">移除授權規則也會移除對應的使用者許可權。</span><span class="sxs-lookup"><span data-stu-id="3fd87-115">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="3fd87-116">示例</span><span class="sxs-lookup"><span data-stu-id="3fd87-116">EXAMPLES</span></span>

### <span data-ttu-id="3fd87-117">範例1：從命名空間移除授權規則</span><span class="sxs-lookup"><span data-stu-id="3fd87-117">Example 1: Remove an authorization rule from a namespace</span></span>
```
PS C:\>Remove-AzureRmNotificationHubNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="3fd87-118">這個命令會將名為 ListenRule 的授權規則從名為 ContosoNamespace 的命名空間中移除。</span><span class="sxs-lookup"><span data-stu-id="3fd87-118">This command removes the authorization rule named ListenRule from the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="3fd87-119">當您執行此命令時，您必須指定將命名空間指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="3fd87-119">When you run this command you must specify the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="3fd87-120">參數</span><span class="sxs-lookup"><span data-stu-id="3fd87-120">PARAMETERS</span></span>

### <span data-ttu-id="3fd87-121">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3fd87-121">-AuthorizationRule</span></span>
<span data-ttu-id="3fd87-122">指定要移除的 SAS 驗證規則名稱。</span><span class="sxs-lookup"><span data-stu-id="3fd87-122">Specifies the name of the SAS authentication rule to be removed.</span></span>

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

### <span data-ttu-id="3fd87-123">-Force</span><span class="sxs-lookup"><span data-stu-id="3fd87-123">-Force</span></span>
<span data-ttu-id="3fd87-124">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="3fd87-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3fd87-125">-命名空間</span><span class="sxs-lookup"><span data-stu-id="3fd87-125">-Namespace</span></span>
<span data-ttu-id="3fd87-126">指定授權規則指派的命名空間。</span><span class="sxs-lookup"><span data-stu-id="3fd87-126">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="3fd87-127">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="3fd87-127">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="3fd87-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3fd87-128">-ResourceGroup</span></span>
<span data-ttu-id="3fd87-129">指定將命名空間指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="3fd87-129">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="3fd87-130">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="3fd87-130">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="3fd87-131">-確認</span><span class="sxs-lookup"><span data-stu-id="3fd87-131">-Confirm</span></span>
<span data-ttu-id="3fd87-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3fd87-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fd87-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fd87-133">-WhatIf</span></span>
<span data-ttu-id="3fd87-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3fd87-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3fd87-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3fd87-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fd87-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fd87-136">-DefaultProfile</span></span>
<span data-ttu-id="3fd87-137">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3fd87-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3fd87-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fd87-138">CommonParameters</span></span>
<span data-ttu-id="3fd87-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3fd87-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fd87-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3fd87-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fd87-141">輸入</span><span class="sxs-lookup"><span data-stu-id="3fd87-141">INPUTS</span></span>

## <span data-ttu-id="3fd87-142">輸出</span><span class="sxs-lookup"><span data-stu-id="3fd87-142">OUTPUTS</span></span>

### <span data-ttu-id="3fd87-143">System.object</span><span class="sxs-lookup"><span data-stu-id="3fd87-143">System.Boolean</span></span>

## <span data-ttu-id="3fd87-144">筆記</span><span class="sxs-lookup"><span data-stu-id="3fd87-144">NOTES</span></span>

## <span data-ttu-id="3fd87-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="3fd87-145">RELATED LINKS</span></span>

[<span data-ttu-id="3fd87-146">AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="3fd87-146">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="3fd87-147">新-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="3fd87-147">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="3fd87-148">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="3fd87-148">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md)


