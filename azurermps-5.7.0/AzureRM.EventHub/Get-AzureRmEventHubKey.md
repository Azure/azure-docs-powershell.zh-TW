---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
ms.openlocfilehash: f8a9f074398df5ce9d8464adf3c22a65d14784b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454235"
---
# <span data-ttu-id="2842a-101">Get-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="2842a-101">Get-AzureRmEventHubKey</span></span>

## <span data-ttu-id="2842a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2842a-102">SYNOPSIS</span></span>
<span data-ttu-id="2842a-103">取得指定事件中心授權規則的主要金鑰詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2842a-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2842a-104">句法</span><span class="sxs-lookup"><span data-stu-id="2842a-104">SYNTAX</span></span>

### <span data-ttu-id="2842a-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2842a-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2842a-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2842a-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2842a-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="2842a-107">AliasAuthoRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2842a-108">說明</span><span class="sxs-lookup"><span data-stu-id="2842a-108">DESCRIPTION</span></span>
<span data-ttu-id="2842a-109">Get-AzureRmEventHubKey Cmdlet 會傳回主要和次要 connectionstrings 以及指定命名空間/事件中樞/別名授權規則的金鑰詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2842a-109">The Get-AzureRmEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="2842a-110">示例</span><span class="sxs-lookup"><span data-stu-id="2842a-110">EXAMPLES</span></span>

### <span data-ttu-id="2842a-111">範例1</span><span class="sxs-lookup"><span data-stu-id="2842a-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="2842a-112">取得授權規則 MyAuthRuleName 的主要和次要 connectionstrings 及金鑰的詳細 \` 資料 \` 。</span><span class="sxs-lookup"><span data-stu-id="2842a-112">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="2842a-113">範例1</span><span class="sxs-lookup"><span data-stu-id="2842a-113">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="2842a-114">取得授權規則 MyAuthRuleName 的主要、次要、AliasPrimary 和 AliasSecondary connectionstrings 及金鑰的詳細 \` 資料 \` 。</span><span class="sxs-lookup"><span data-stu-id="2842a-114">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="2842a-115">參數</span><span class="sxs-lookup"><span data-stu-id="2842a-115">PARAMETERS</span></span>

### <span data-ttu-id="2842a-116">-AliasName</span><span class="sxs-lookup"><span data-stu-id="2842a-116">-AliasName</span></span>
<span data-ttu-id="2842a-117">別名名稱</span><span class="sxs-lookup"><span data-stu-id="2842a-117">Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2842a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2842a-118">-DefaultProfile</span></span>
<span data-ttu-id="2842a-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2842a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2842a-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="2842a-120">-EventHub</span></span>
<span data-ttu-id="2842a-121">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="2842a-121">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2842a-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="2842a-122">-Name</span></span>
<span data-ttu-id="2842a-123">AuthorizationRule 名稱</span><span class="sxs-lookup"><span data-stu-id="2842a-123">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2842a-124">-命名空間</span><span class="sxs-lookup"><span data-stu-id="2842a-124">-Namespace</span></span>
<span data-ttu-id="2842a-125">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="2842a-125">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2842a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2842a-126">-ResourceGroupName</span></span>
<span data-ttu-id="2842a-127">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="2842a-127">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2842a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2842a-128">CommonParameters</span></span>
<span data-ttu-id="2842a-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2842a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2842a-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2842a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2842a-131">輸入</span><span class="sxs-lookup"><span data-stu-id="2842a-131">INPUTS</span></span>

### <span data-ttu-id="2842a-132">System.object</span><span class="sxs-lookup"><span data-stu-id="2842a-132">System.String</span></span>


## <span data-ttu-id="2842a-133">輸出</span><span class="sxs-lookup"><span data-stu-id="2842a-133">OUTPUTS</span></span>

### <span data-ttu-id="2842a-134">PSListKeysAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="2842a-134">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>


## <span data-ttu-id="2842a-135">筆記</span><span class="sxs-lookup"><span data-stu-id="2842a-135">NOTES</span></span>

## <span data-ttu-id="2842a-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="2842a-136">RELATED LINKS</span></span>
