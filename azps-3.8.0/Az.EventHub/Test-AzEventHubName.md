---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/test-azeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
ms.openlocfilehash: 8eb43982db0eddeb9127006e0cfa3336698eb7e3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797205"
---
# <span data-ttu-id="2596e-101">Test-AzEventHubName</span><span class="sxs-lookup"><span data-stu-id="2596e-101">Test-AzEventHubName</span></span>

## <span data-ttu-id="2596e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2596e-102">SYNOPSIS</span></span>
<span data-ttu-id="2596e-103">檢查 (DR 設定名稱的指定命名空間名稱或別名的可用性) </span><span class="sxs-lookup"><span data-stu-id="2596e-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="2596e-104">句法</span><span class="sxs-lookup"><span data-stu-id="2596e-104">SYNTAX</span></span>

### <span data-ttu-id="2596e-105">NamespaceCheckNameAvailabilitySet (預設) </span><span class="sxs-lookup"><span data-stu-id="2596e-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2596e-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2596e-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2596e-107">說明</span><span class="sxs-lookup"><span data-stu-id="2596e-107">DESCRIPTION</span></span>
<span data-ttu-id="2596e-108">**AzEventhubName** Cmdlet 會檢查命名空間名稱或別名 (DR 配置名稱是否可用) </span><span class="sxs-lookup"><span data-stu-id="2596e-108">The **Test-AzEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="2596e-109">示例</span><span class="sxs-lookup"><span data-stu-id="2596e-109">EXAMPLES</span></span>

### <span data-ttu-id="2596e-110">範例1</span><span class="sxs-lookup"><span data-stu-id="2596e-110">Example 1</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="2596e-111">將命名空間名稱 ' MyNameSapceName」的可用性傳回狀態為 True （如果有的話）</span><span class="sxs-lookup"><span data-stu-id="2596e-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True if available</span></span>

### <span data-ttu-id="2596e-112">範例2</span><span class="sxs-lookup"><span data-stu-id="2596e-112">Example 2</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="2596e-113">傳回命名空間名稱 ' MyNameSapceName ' 的可用性狀態為 False，原因如下</span><span class="sxs-lookup"><span data-stu-id="2596e-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="2596e-114">範例3</span><span class="sxs-lookup"><span data-stu-id="2596e-114">Example 3</span></span>
```
PS C:\> Test-AzEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="2596e-115">傳回將命名空間 "MyNameSapceName" 的別名 "myAliasName" 的狀態顯示為 True （如果有的話）</span><span class="sxs-lookup"><span data-stu-id="2596e-115">Returns the status on availability of the alias name 'myAliasName' for namespace 'MyNameSapceName' as True if available</span></span>

## <span data-ttu-id="2596e-116">參數</span><span class="sxs-lookup"><span data-stu-id="2596e-116">PARAMETERS</span></span>

### <span data-ttu-id="2596e-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="2596e-117">-AliasName</span></span>
<span data-ttu-id="2596e-118">DR 配置名稱-別名名稱</span><span class="sxs-lookup"><span data-stu-id="2596e-118">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="2596e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2596e-119">-DefaultProfile</span></span>
<span data-ttu-id="2596e-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2596e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2596e-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="2596e-121">-Namespace</span></span>
<span data-ttu-id="2596e-122">Eventhub 命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="2596e-122">Eventhub Namespace Name</span></span>

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

### <span data-ttu-id="2596e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2596e-123">-ResourceGroupName</span></span>
<span data-ttu-id="2596e-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="2596e-124">Resource Group Name</span></span>

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

### <span data-ttu-id="2596e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2596e-125">CommonParameters</span></span>
<span data-ttu-id="2596e-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2596e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2596e-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2596e-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2596e-128">輸入</span><span class="sxs-lookup"><span data-stu-id="2596e-128">INPUTS</span></span>

### <span data-ttu-id="2596e-129">System.object</span><span class="sxs-lookup"><span data-stu-id="2596e-129">System.String</span></span>

## <span data-ttu-id="2596e-130">輸出</span><span class="sxs-lookup"><span data-stu-id="2596e-130">OUTPUTS</span></span>

### <span data-ttu-id="2596e-131">PSCheckNameAvailabilityResultAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="2596e-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="2596e-132">筆記</span><span class="sxs-lookup"><span data-stu-id="2596e-132">NOTES</span></span>

## <span data-ttu-id="2596e-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="2596e-133">RELATED LINKS</span></span>
