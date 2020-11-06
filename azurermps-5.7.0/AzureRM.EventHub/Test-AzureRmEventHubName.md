---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/test-azurermeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
ms.openlocfilehash: e1b6de255896adbf8fd47eb57973b5c5df0d79a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448667"
---
# <span data-ttu-id="a129c-101">Test-AzureRmEventHubName</span><span class="sxs-lookup"><span data-stu-id="a129c-101">Test-AzureRmEventHubName</span></span>

## <span data-ttu-id="a129c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a129c-102">SYNOPSIS</span></span>
<span data-ttu-id="a129c-103">檢查 (DR 設定名稱的指定命名空間名稱或別名的可用性) </span><span class="sxs-lookup"><span data-stu-id="a129c-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a129c-104">句法</span><span class="sxs-lookup"><span data-stu-id="a129c-104">SYNTAX</span></span>

### <span data-ttu-id="a129c-105">NamespaceCheckNameAvailabilitySet (預設) </span><span class="sxs-lookup"><span data-stu-id="a129c-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzureRmEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a129c-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a129c-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzureRmEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a129c-107">說明</span><span class="sxs-lookup"><span data-stu-id="a129c-107">DESCRIPTION</span></span>
<span data-ttu-id="a129c-108">**AzureRmEventhubName** Cmdlet 會檢查命名空間名稱或別名 (DR 配置名稱是否可用) </span><span class="sxs-lookup"><span data-stu-id="a129c-108">The **Test-AzureRmEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="a129c-109">示例</span><span class="sxs-lookup"><span data-stu-id="a129c-109">EXAMPLES</span></span>

### <span data-ttu-id="a129c-110">範例1</span><span class="sxs-lookup"><span data-stu-id="a129c-110">Example 1</span></span>
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="a129c-111">將命名空間名稱 ' MyNameSapceName ' 的可用性傳回狀態傳回 True</span><span class="sxs-lookup"><span data-stu-id="a129c-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="a129c-112">範例2</span><span class="sxs-lookup"><span data-stu-id="a129c-112">Example 2</span></span>
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="a129c-113">傳回命名空間名稱 ' MyNameSapceName ' 的可用性狀態為 False，原因如下</span><span class="sxs-lookup"><span data-stu-id="a129c-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="a129c-114">範例3</span><span class="sxs-lookup"><span data-stu-id="a129c-114">Example 3</span></span>
```
PS C:\> Test-AzureRmEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="a129c-115">傳回在 namespace "MyNameSapceName" 下，別名名稱 "myAliasName" 的狀態是否為 True</span><span class="sxs-lookup"><span data-stu-id="a129c-115">Returns the status on availability of the alias name 'myAliasName' under namespace 'MyNameSapceName' as True</span></span>

## <span data-ttu-id="a129c-116">參數</span><span class="sxs-lookup"><span data-stu-id="a129c-116">PARAMETERS</span></span>

### <span data-ttu-id="a129c-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="a129c-117">-AliasName</span></span>
<span data-ttu-id="a129c-118">DR 配置名稱-別名名稱</span><span class="sxs-lookup"><span data-stu-id="a129c-118">DR Configuration Name - Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a129c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a129c-119">-DefaultProfile</span></span>
<span data-ttu-id="a129c-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a129c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a129c-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="a129c-121">-Namespace</span></span>
<span data-ttu-id="a129c-122">Eventhub 命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="a129c-122">Eventhub Namespace Name</span></span>

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

### <span data-ttu-id="a129c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a129c-123">-ResourceGroupName</span></span>
<span data-ttu-id="a129c-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="a129c-124">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a129c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a129c-125">CommonParameters</span></span>
<span data-ttu-id="a129c-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a129c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a129c-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a129c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a129c-128">輸入</span><span class="sxs-lookup"><span data-stu-id="a129c-128">INPUTS</span></span>

### <span data-ttu-id="a129c-129">System.object</span><span class="sxs-lookup"><span data-stu-id="a129c-129">System.String</span></span>


## <span data-ttu-id="a129c-130">輸出</span><span class="sxs-lookup"><span data-stu-id="a129c-130">OUTPUTS</span></span>

### <span data-ttu-id="a129c-131">PSCheckNameAvailabilityResultAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="a129c-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>


## <span data-ttu-id="a129c-132">筆記</span><span class="sxs-lookup"><span data-stu-id="a129c-132">NOTES</span></span>

## <span data-ttu-id="a129c-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="a129c-133">RELATED LINKS</span></span>
