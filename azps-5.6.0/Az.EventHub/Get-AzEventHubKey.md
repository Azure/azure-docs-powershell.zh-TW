---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
ms.openlocfilehash: f9f4eb7f60683524eccec8b3d35926b86fa52bbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903233"
---
# <span data-ttu-id="7d664-101">Get-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="7d664-101">Get-AzEventHubKey</span></span>

## <span data-ttu-id="7d664-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7d664-102">SYNOPSIS</span></span>
<span data-ttu-id="7d664-103">獲得指定事件中樞授權規則的主鍵詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7d664-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="7d664-104">語法</span><span class="sxs-lookup"><span data-stu-id="7d664-104">SYNTAX</span></span>

### <span data-ttu-id="7d664-105">命名空間驗證RuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7d664-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d664-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7d664-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d664-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="7d664-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d664-108">描述</span><span class="sxs-lookup"><span data-stu-id="7d664-108">DESCRIPTION</span></span>
<span data-ttu-id="7d664-109">Cmdlet Get-AzEventHubKey會傳回指定 NameSpace/Event Hubs/Alias 授權規則的主要和次要連接字串和金鑰詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7d664-109">The Get-AzEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="7d664-110">例子</span><span class="sxs-lookup"><span data-stu-id="7d664-110">EXAMPLES</span></span>

### <span data-ttu-id="7d664-111">範例 1：命名空間</span><span class="sxs-lookup"><span data-stu-id="7d664-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

### <span data-ttu-id="7d664-112">範例 2：EventHub</span><span class="sxs-lookup"><span data-stu-id="7d664-112">Example 2: EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="7d664-113">針對 MyAuthRuleName 的授權規則，獲得主要和次要連接字串和 \` 金鑰的詳細資訊 \` 。</span><span class="sxs-lookup"><span data-stu-id="7d664-113">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="7d664-114">範例 3：GeoRecovery 組 (別名) </span><span class="sxs-lookup"><span data-stu-id="7d664-114">Example 3: Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="7d664-115">獲得主、次要、AliasPrimary 和 Alias Secondarary 連接字串和授權規則 \` MyAuthRuleName 的金鑰詳細資料 \` 。</span><span class="sxs-lookup"><span data-stu-id="7d664-115">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="7d664-116">參數</span><span class="sxs-lookup"><span data-stu-id="7d664-116">PARAMETERS</span></span>

### <span data-ttu-id="7d664-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="7d664-117">-AliasName</span></span>
<span data-ttu-id="7d664-118">別名名稱</span><span class="sxs-lookup"><span data-stu-id="7d664-118">Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d664-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d664-119">-DefaultProfile</span></span>
<span data-ttu-id="7d664-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d664-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d664-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="7d664-121">-EventHub</span></span>
<span data-ttu-id="7d664-122">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="7d664-122">EventHub Name</span></span>

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

### <span data-ttu-id="7d664-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="7d664-123">-Name</span></span>
<span data-ttu-id="7d664-124">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="7d664-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="7d664-125">-命名空間</span><span class="sxs-lookup"><span data-stu-id="7d664-125">-Namespace</span></span>
<span data-ttu-id="7d664-126">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="7d664-126">Namespace Name</span></span>

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

### <span data-ttu-id="7d664-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d664-127">-ResourceGroupName</span></span>
<span data-ttu-id="7d664-128">資源組名</span><span class="sxs-lookup"><span data-stu-id="7d664-128">Resource Group Name</span></span>

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

### <span data-ttu-id="7d664-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d664-129">CommonParameters</span></span>
<span data-ttu-id="7d664-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7d664-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d664-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="7d664-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d664-132">輸入</span><span class="sxs-lookup"><span data-stu-id="7d664-132">INPUTS</span></span>

### <span data-ttu-id="7d664-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7d664-133">System.String</span></span>

## <span data-ttu-id="7d664-134">輸出</span><span class="sxs-lookup"><span data-stu-id="7d664-134">OUTPUTS</span></span>

### <span data-ttu-id="7d664-135">Microsoft.Azure.Commands.EventHub.models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="7d664-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="7d664-136">筆記</span><span class="sxs-lookup"><span data-stu-id="7d664-136">NOTES</span></span>

## <span data-ttu-id="7d664-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d664-137">RELATED LINKS</span></span>
