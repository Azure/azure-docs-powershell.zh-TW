---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: aa9b4dba29c766923966571c736c7f96a608df29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448089"
---
# <span data-ttu-id="f62e3-101">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f62e3-101">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="f62e3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f62e3-102">SYNOPSIS</span></span>
<span data-ttu-id="f62e3-103">取得與通知中心命名空間相關聯之授權規則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f62e3-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f62e3-104">句法</span><span class="sxs-lookup"><span data-stu-id="f62e3-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f62e3-105">說明</span><span class="sxs-lookup"><span data-stu-id="f62e3-105">DESCRIPTION</span></span>
<span data-ttu-id="f62e3-106">**AzureRmNotificationHubsNamespaceAuthorizationRules** Cmdlet 會傳回有關共用存取簽章 (SAS) 與通知中心命名空間相關聯的授權規則的資訊。</span><span class="sxs-lookup"><span data-stu-id="f62e3-106">The **Get-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="f62e3-107">您可以傳回與命名空間關聯的所有規則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f62e3-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="f62e3-108">或者，您也可以透過包括 *AuthorizationRule* 參數，傳回特定規則的資訊。</span><span class="sxs-lookup"><span data-stu-id="f62e3-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>

<span data-ttu-id="f62e3-109">授權規則可管理命名空間的存取權。</span><span class="sxs-lookup"><span data-stu-id="f62e3-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="f62e3-110">這是透過根據不同許可權等級建立連結（例如 Uri）來完成。</span><span class="sxs-lookup"><span data-stu-id="f62e3-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="f62e3-111">平台層級可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="f62e3-111">Platform levels can be one of the following:</span></span> 

- <span data-ttu-id="f62e3-112">聆聽</span><span class="sxs-lookup"><span data-stu-id="f62e3-112">Listen</span></span>
- <span data-ttu-id="f62e3-113">發送</span><span class="sxs-lookup"><span data-stu-id="f62e3-113">Send</span></span>
- <span data-ttu-id="f62e3-114">管理</span><span class="sxs-lookup"><span data-stu-id="f62e3-114">Manage</span></span>

<span data-ttu-id="f62e3-115">用戶端會根據適當的許可權等級，導向到其中一個 Uri。</span><span class="sxs-lookup"><span data-stu-id="f62e3-115">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="f62e3-116">例如，擁有偵聽許可權的用戶端將會導向該許可權的 URI。</span><span class="sxs-lookup"><span data-stu-id="f62e3-116">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="f62e3-117">這個 Cmdlet 只會取得與命名空間相關聯的授權規則。</span><span class="sxs-lookup"><span data-stu-id="f62e3-117">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="f62e3-118">若要取得命名空間本身的相關資訊，請使用 AzureRmNotificationHubsNamespace。</span><span class="sxs-lookup"><span data-stu-id="f62e3-118">To get information about the namespace itself, use Get-AzureRmNotificationHubsNamespace.</span></span>

## <span data-ttu-id="f62e3-119">示例</span><span class="sxs-lookup"><span data-stu-id="f62e3-119">EXAMPLES</span></span>

### <span data-ttu-id="f62e3-120">範例1：取得指派給命名空間的所有授權規則的相關資訊</span><span class="sxs-lookup"><span data-stu-id="f62e3-120">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="f62e3-121">這個命令會取得指派給 namespace ContosoNamespace 和 ContosoNotificationsGroup 資源群組的所有授權規則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f62e3-121">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="f62e3-122">範例2：取得授權規則的相關資訊</span><span class="sxs-lookup"><span data-stu-id="f62e3-122">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="f62e3-123">這個命令會取得名為 ListenRule 的單一命名空間授權規則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f62e3-123">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="f62e3-124">當您取得特定授權規則的資訊時，您必須包含命名空間和資源群組。</span><span class="sxs-lookup"><span data-stu-id="f62e3-124">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="f62e3-125">參數</span><span class="sxs-lookup"><span data-stu-id="f62e3-125">PARAMETERS</span></span>

### <span data-ttu-id="f62e3-126">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f62e3-126">-AuthorizationRule</span></span>
<span data-ttu-id="f62e3-127">指定 SAS 驗證規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="f62e3-127">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="f62e3-128">這些規則決定使用者對命名空間擁有的存取類型。</span><span class="sxs-lookup"><span data-stu-id="f62e3-128">These rules determine the type of access that users have to the namespace.</span></span>

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

### <span data-ttu-id="f62e3-129">-命名空間</span><span class="sxs-lookup"><span data-stu-id="f62e3-129">-Namespace</span></span>
<span data-ttu-id="f62e3-130">指定授權規則指派的命名空間。</span><span class="sxs-lookup"><span data-stu-id="f62e3-130">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="f62e3-131">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="f62e3-131">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="f62e3-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f62e3-132">-ResourceGroup</span></span>
<span data-ttu-id="f62e3-133">指定授權規則指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="f62e3-133">Specifies the resource group to which the authorization rules are assigned.</span></span>

<span data-ttu-id="f62e3-134">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="f62e3-134">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="f62e3-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f62e3-135">-DefaultProfile</span></span>
<span data-ttu-id="f62e3-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f62e3-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f62e3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f62e3-137">CommonParameters</span></span>
<span data-ttu-id="f62e3-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f62e3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f62e3-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f62e3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f62e3-140">輸入</span><span class="sxs-lookup"><span data-stu-id="f62e3-140">INPUTS</span></span>

## <span data-ttu-id="f62e3-141">輸出</span><span class="sxs-lookup"><span data-stu-id="f62e3-141">OUTPUTS</span></span>

### <span data-ttu-id="f62e3-142">[System.object]. 清單 ' 1 [NotificationHubs]。 SharedAccessAuthorizationRuleAttributes]</span><span class="sxs-lookup"><span data-stu-id="f62e3-142">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes]</span></span>

## <span data-ttu-id="f62e3-143">筆記</span><span class="sxs-lookup"><span data-stu-id="f62e3-143">NOTES</span></span>

## <span data-ttu-id="f62e3-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="f62e3-144">RELATED LINKS</span></span>

[<span data-ttu-id="f62e3-145">AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f62e3-145">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="f62e3-146">新-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f62e3-146">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="f62e3-147">移除-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f62e3-147">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="f62e3-148">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f62e3-148">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


