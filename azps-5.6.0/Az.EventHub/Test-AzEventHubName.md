---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/test-azeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
ms.openlocfilehash: 6620579ad49143dc715fc62f23d305e2efd3d5ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916412"
---
# <span data-ttu-id="d4bbd-101">Test-AzEventHubName</span><span class="sxs-lookup"><span data-stu-id="d4bbd-101">Test-AzEventHubName</span></span>

## <span data-ttu-id="d4bbd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d4bbd-102">SYNOPSIS</span></span>
<span data-ttu-id="d4bbd-103">檢查指定 NameSpace 名稱或別名 (DR 組) </span><span class="sxs-lookup"><span data-stu-id="d4bbd-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="d4bbd-104">語法</span><span class="sxs-lookup"><span data-stu-id="d4bbd-104">SYNTAX</span></span>

### <span data-ttu-id="d4bbd-105">命名空間CheckNameAvailabilitySet (預設) </span><span class="sxs-lookup"><span data-stu-id="d4bbd-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4bbd-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d4bbd-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4bbd-107">描述</span><span class="sxs-lookup"><span data-stu-id="d4bbd-107">DESCRIPTION</span></span>
<span data-ttu-id="d4bbd-108">**Test-AzEventhubName** Cmdlet 檢查名稱Space 名稱或別名 (DR 組) </span><span class="sxs-lookup"><span data-stu-id="d4bbd-108">The **Test-AzEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="d4bbd-109">例子</span><span class="sxs-lookup"><span data-stu-id="d4bbd-109">EXAMPLES</span></span>

### <span data-ttu-id="d4bbd-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="d4bbd-110">Example 1</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="d4bbd-111">如果可用，將命名空間名稱 'MyNameSapceName' 的可用性狀態以 True 表示</span><span class="sxs-lookup"><span data-stu-id="d4bbd-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True if available</span></span>

### <span data-ttu-id="d4bbd-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="d4bbd-112">Example 2</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="d4bbd-113">將命名空間名稱 'MyNameSapceName' 的可用性狀態以 False 與原因</span><span class="sxs-lookup"><span data-stu-id="d4bbd-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="d4bbd-114">範例 3</span><span class="sxs-lookup"><span data-stu-id="d4bbd-114">Example 3</span></span>
```
PS C:\> Test-AzEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="d4bbd-115">將命名空間 'MyNameSapceName' 的別名 'myAliasName' 的可用性狀態當做 True 時 ，如果可用</span><span class="sxs-lookup"><span data-stu-id="d4bbd-115">Returns the status on availability of the alias name 'myAliasName' for namespace 'MyNameSapceName' as True if available</span></span>

## <span data-ttu-id="d4bbd-116">參數</span><span class="sxs-lookup"><span data-stu-id="d4bbd-116">PARAMETERS</span></span>

### <span data-ttu-id="d4bbd-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="d4bbd-117">-AliasName</span></span>
<span data-ttu-id="d4bbd-118">DR 組組名稱 - 別名名稱</span><span class="sxs-lookup"><span data-stu-id="d4bbd-118">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="d4bbd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4bbd-119">-DefaultProfile</span></span>
<span data-ttu-id="d4bbd-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d4bbd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4bbd-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="d4bbd-121">-Namespace</span></span>
<span data-ttu-id="d4bbd-122">Eventhub 命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="d4bbd-122">Eventhub Namespace Name</span></span>

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

### <span data-ttu-id="d4bbd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4bbd-123">-ResourceGroupName</span></span>
<span data-ttu-id="d4bbd-124">資源組名</span><span class="sxs-lookup"><span data-stu-id="d4bbd-124">Resource Group Name</span></span>

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

### <span data-ttu-id="d4bbd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4bbd-125">CommonParameters</span></span>
<span data-ttu-id="d4bbd-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d4bbd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4bbd-127">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d4bbd-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4bbd-128">輸入</span><span class="sxs-lookup"><span data-stu-id="d4bbd-128">INPUTS</span></span>

### <span data-ttu-id="d4bbd-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d4bbd-129">System.String</span></span>

## <span data-ttu-id="d4bbd-130">輸出</span><span class="sxs-lookup"><span data-stu-id="d4bbd-130">OUTPUTS</span></span>

### <span data-ttu-id="d4bbd-131">Microsoft.Azure.Commands.EventHub.models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="d4bbd-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="d4bbd-132">筆記</span><span class="sxs-lookup"><span data-stu-id="d4bbd-132">NOTES</span></span>

## <span data-ttu-id="d4bbd-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4bbd-133">RELATED LINKS</span></span>
