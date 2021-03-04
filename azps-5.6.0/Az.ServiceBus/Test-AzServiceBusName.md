---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/test-azservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
ms.openlocfilehash: b2bca900be878e6f89f52b1f6096e82f79ec7863
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904318"
---
# <span data-ttu-id="3272e-101">Test-AzServiceBusName</span><span class="sxs-lookup"><span data-stu-id="3272e-101">Test-AzServiceBusName</span></span>

## <span data-ttu-id="3272e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3272e-102">SYNOPSIS</span></span>
<span data-ttu-id="3272e-103">檢查指定 NameSpace 名稱或別名 (DR 組) </span><span class="sxs-lookup"><span data-stu-id="3272e-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

## <span data-ttu-id="3272e-104">語法</span><span class="sxs-lookup"><span data-stu-id="3272e-104">SYNTAX</span></span>

### <span data-ttu-id="3272e-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="3272e-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3272e-106">命名空間CheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="3272e-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3272e-107">描述</span><span class="sxs-lookup"><span data-stu-id="3272e-107">DESCRIPTION</span></span>
<span data-ttu-id="3272e-108">**Test-AzServiceBusName** Cmdlet 檢查名稱空格名稱或別名 (DR 組) </span><span class="sxs-lookup"><span data-stu-id="3272e-108">The **Test-AzServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="3272e-109">例子</span><span class="sxs-lookup"><span data-stu-id="3272e-109">EXAMPLES</span></span>

### <span data-ttu-id="3272e-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="3272e-110">Example 1</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="3272e-111">將命名空間名稱 "MyNameSapceName" 的可用性狀態當做 True</span><span class="sxs-lookup"><span data-stu-id="3272e-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="3272e-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="3272e-112">Example 2</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="3272e-113">將命名空間名稱 'MyNameSapceName' 的可用性狀態以 False 與原因</span><span class="sxs-lookup"><span data-stu-id="3272e-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="3272e-114">範例 3</span><span class="sxs-lookup"><span data-stu-id="3272e-114">Example 3</span></span>
```
PS C:\> Test-AzServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

## <span data-ttu-id="3272e-115">參數</span><span class="sxs-lookup"><span data-stu-id="3272e-115">PARAMETERS</span></span>

### <span data-ttu-id="3272e-116">-AliasName</span><span class="sxs-lookup"><span data-stu-id="3272e-116">-AliasName</span></span>
<span data-ttu-id="3272e-117">DR 組組名稱 - 別名名稱</span><span class="sxs-lookup"><span data-stu-id="3272e-117">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="3272e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3272e-118">-DefaultProfile</span></span>
<span data-ttu-id="3272e-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3272e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3272e-120">-命名空間</span><span class="sxs-lookup"><span data-stu-id="3272e-120">-Namespace</span></span>
<span data-ttu-id="3272e-121">Servicebus 命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="3272e-121">Servicebus Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3272e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3272e-122">-ResourceGroupName</span></span>
<span data-ttu-id="3272e-123">資源組名</span><span class="sxs-lookup"><span data-stu-id="3272e-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3272e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3272e-124">CommonParameters</span></span>
<span data-ttu-id="3272e-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3272e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3272e-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="3272e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3272e-127">輸入</span><span class="sxs-lookup"><span data-stu-id="3272e-127">INPUTS</span></span>

### <span data-ttu-id="3272e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="3272e-128">System.String</span></span>

## <span data-ttu-id="3272e-129">輸出</span><span class="sxs-lookup"><span data-stu-id="3272e-129">OUTPUTS</span></span>

### <span data-ttu-id="3272e-130">Microsoft.Azure.Commands.ServiceBus.models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="3272e-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="3272e-131">筆記</span><span class="sxs-lookup"><span data-stu-id="3272e-131">NOTES</span></span>

## <span data-ttu-id="3272e-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="3272e-132">RELATED LINKS</span></span>
