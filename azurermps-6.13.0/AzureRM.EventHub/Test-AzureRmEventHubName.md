---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/test-azurermeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
ms.openlocfilehash: 64a8282cb1dc99b32e0296ebf97f59ab96b5fd96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443831"
---
# <span data-ttu-id="423e3-101">Test-AzureRmEventHubName</span><span class="sxs-lookup"><span data-stu-id="423e3-101">Test-AzureRmEventHubName</span></span>

## <span data-ttu-id="423e3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="423e3-102">SYNOPSIS</span></span>
<span data-ttu-id="423e3-103">檢查 (DR 設定名稱的指定命名空間名稱或別名的可用性) </span><span class="sxs-lookup"><span data-stu-id="423e3-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="423e3-104">句法</span><span class="sxs-lookup"><span data-stu-id="423e3-104">SYNTAX</span></span>

### <span data-ttu-id="423e3-105">NamespaceCheckNameAvailabilitySet (預設) </span><span class="sxs-lookup"><span data-stu-id="423e3-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzureRmEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="423e3-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="423e3-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzureRmEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="423e3-107">說明</span><span class="sxs-lookup"><span data-stu-id="423e3-107">DESCRIPTION</span></span>
<span data-ttu-id="423e3-108">**AzureRmEventhubName** Cmdlet 會檢查命名空間名稱或別名 (DR 配置名稱是否可用) </span><span class="sxs-lookup"><span data-stu-id="423e3-108">The **Test-AzureRmEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="423e3-109">示例</span><span class="sxs-lookup"><span data-stu-id="423e3-109">EXAMPLES</span></span>

### <span data-ttu-id="423e3-110">範例1</span><span class="sxs-lookup"><span data-stu-id="423e3-110">Example 1</span></span>
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="423e3-111">將命名空間名稱 ' MyNameSapceName」的可用性傳回狀態為 True （如果有的話）</span><span class="sxs-lookup"><span data-stu-id="423e3-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True if available</span></span>

### <span data-ttu-id="423e3-112">範例2</span><span class="sxs-lookup"><span data-stu-id="423e3-112">Example 2</span></span>
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="423e3-113">傳回命名空間名稱 ' MyNameSapceName ' 的可用性狀態為 False，原因如下</span><span class="sxs-lookup"><span data-stu-id="423e3-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="423e3-114">範例3</span><span class="sxs-lookup"><span data-stu-id="423e3-114">Example 3</span></span>
```
PS C:\> Test-AzureRmEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="423e3-115">傳回將命名空間 "MyNameSapceName" 的別名 "myAliasName" 的狀態顯示為 True （如果有的話）</span><span class="sxs-lookup"><span data-stu-id="423e3-115">Returns the status on availability of the alias name 'myAliasName' for namespace 'MyNameSapceName' as True if available</span></span>

## <span data-ttu-id="423e3-116">參數</span><span class="sxs-lookup"><span data-stu-id="423e3-116">PARAMETERS</span></span>

### <span data-ttu-id="423e3-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="423e3-117">-AliasName</span></span>
<span data-ttu-id="423e3-118">DR 配置名稱-別名名稱</span><span class="sxs-lookup"><span data-stu-id="423e3-118">DR Configuration Name - Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="423e3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="423e3-119">-DefaultProfile</span></span>
<span data-ttu-id="423e3-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="423e3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="423e3-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="423e3-121">-Namespace</span></span>
<span data-ttu-id="423e3-122">Eventhub 命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="423e3-122">Eventhub Namespace Name</span></span>

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

### <span data-ttu-id="423e3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="423e3-123">-ResourceGroupName</span></span>
<span data-ttu-id="423e3-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="423e3-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="423e3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="423e3-125">CommonParameters</span></span>
<span data-ttu-id="423e3-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="423e3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="423e3-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="423e3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="423e3-128">輸入</span><span class="sxs-lookup"><span data-stu-id="423e3-128">INPUTS</span></span>

### <span data-ttu-id="423e3-129">System.object</span><span class="sxs-lookup"><span data-stu-id="423e3-129">System.String</span></span>

## <span data-ttu-id="423e3-130">輸出</span><span class="sxs-lookup"><span data-stu-id="423e3-130">OUTPUTS</span></span>

### <span data-ttu-id="423e3-131">PSCheckNameAvailabilityResultAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="423e3-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="423e3-132">筆記</span><span class="sxs-lookup"><span data-stu-id="423e3-132">NOTES</span></span>

## <span data-ttu-id="423e3-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="423e3-133">RELATED LINKS</span></span>
