---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/test-azeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Test-AzEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Test-AzEventHubName.md
ms.openlocfilehash: 49b47e637d009eabac106679e81ec763b0898160
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795646"
---
# <span data-ttu-id="f3f06-101">Test-AzEventHubName</span><span class="sxs-lookup"><span data-stu-id="f3f06-101">Test-AzEventHubName</span></span>

## <span data-ttu-id="f3f06-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3f06-102">SYNOPSIS</span></span>
<span data-ttu-id="f3f06-103">檢查 (DR 設定名稱的指定命名空間名稱或別名的可用性) </span><span class="sxs-lookup"><span data-stu-id="f3f06-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="f3f06-104">句法</span><span class="sxs-lookup"><span data-stu-id="f3f06-104">SYNTAX</span></span>

### <span data-ttu-id="f3f06-105">NamespaceCheckNameAvailabilitySet (預設) </span><span class="sxs-lookup"><span data-stu-id="f3f06-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3f06-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f3f06-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3f06-107">說明</span><span class="sxs-lookup"><span data-stu-id="f3f06-107">DESCRIPTION</span></span>
<span data-ttu-id="f3f06-108">**AzEventhubName** Cmdlet 會檢查命名空間名稱或別名 (DR 配置名稱是否可用) </span><span class="sxs-lookup"><span data-stu-id="f3f06-108">The **Test-AzEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="f3f06-109">示例</span><span class="sxs-lookup"><span data-stu-id="f3f06-109">EXAMPLES</span></span>

### <span data-ttu-id="f3f06-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f3f06-110">Example 1</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="f3f06-111">將命名空間名稱 ' MyNameSapceName」的可用性傳回狀態為 True （如果有的話）</span><span class="sxs-lookup"><span data-stu-id="f3f06-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True if available</span></span>

### <span data-ttu-id="f3f06-112">範例2</span><span class="sxs-lookup"><span data-stu-id="f3f06-112">Example 2</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="f3f06-113">傳回命名空間名稱 ' MyNameSapceName ' 的可用性狀態為 False，原因如下</span><span class="sxs-lookup"><span data-stu-id="f3f06-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="f3f06-114">範例3</span><span class="sxs-lookup"><span data-stu-id="f3f06-114">Example 3</span></span>
```
PS C:\> Test-AzEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="f3f06-115">傳回將命名空間 "MyNameSapceName" 的別名 "myAliasName" 的狀態顯示為 True （如果有的話）</span><span class="sxs-lookup"><span data-stu-id="f3f06-115">Returns the status on availability of the alias name 'myAliasName' for namespace 'MyNameSapceName' as True if available</span></span>

## <span data-ttu-id="f3f06-116">參數</span><span class="sxs-lookup"><span data-stu-id="f3f06-116">PARAMETERS</span></span>

### <span data-ttu-id="f3f06-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="f3f06-117">-AliasName</span></span>
<span data-ttu-id="f3f06-118">DR 配置名稱-別名名稱</span><span class="sxs-lookup"><span data-stu-id="f3f06-118">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="f3f06-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3f06-119">-DefaultProfile</span></span>
<span data-ttu-id="f3f06-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f3f06-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3f06-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="f3f06-121">-Namespace</span></span>
<span data-ttu-id="f3f06-122">Eventhub 命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="f3f06-122">Eventhub Namespace Name</span></span>

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

### <span data-ttu-id="f3f06-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3f06-123">-ResourceGroupName</span></span>
<span data-ttu-id="f3f06-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="f3f06-124">Resource Group Name</span></span>

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

### <span data-ttu-id="f3f06-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3f06-125">CommonParameters</span></span>
<span data-ttu-id="f3f06-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3f06-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3f06-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f3f06-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3f06-128">輸入</span><span class="sxs-lookup"><span data-stu-id="f3f06-128">INPUTS</span></span>

### <span data-ttu-id="f3f06-129">System.object</span><span class="sxs-lookup"><span data-stu-id="f3f06-129">System.String</span></span>

## <span data-ttu-id="f3f06-130">輸出</span><span class="sxs-lookup"><span data-stu-id="f3f06-130">OUTPUTS</span></span>

### <span data-ttu-id="f3f06-131">PSCheckNameAvailabilityResultAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="f3f06-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="f3f06-132">筆記</span><span class="sxs-lookup"><span data-stu-id="f3f06-132">NOTES</span></span>

## <span data-ttu-id="f3f06-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3f06-133">RELATED LINKS</span></span>
