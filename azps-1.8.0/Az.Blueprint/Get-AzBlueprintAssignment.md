---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
ms.openlocfilehash: 121811c88493a4f6f069a60c8f9662eb9d11303e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622881"
---
# <span data-ttu-id="30832-101">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="30832-101">Get-AzBlueprintAssignment</span></span>

## <span data-ttu-id="30832-102">摘要</span><span class="sxs-lookup"><span data-stu-id="30832-102">SYNOPSIS</span></span>
<span data-ttu-id="30832-103">取得一或多個藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="30832-103">Get one or more blueprint assignments.</span></span>

## <span data-ttu-id="30832-104">句法</span><span class="sxs-lookup"><span data-stu-id="30832-104">SYNTAX</span></span>

### <span data-ttu-id="30832-105">BlueprintAssignmentsBySubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="30832-105">BlueprintAssignmentsBySubscription (Default)</span></span>
```
Get-AzBlueprintAssignment [[-SubscriptionId] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="30832-106">BlueprintAssignmentByName</span><span class="sxs-lookup"><span data-stu-id="30832-106">BlueprintAssignmentByName</span></span>
```
Get-AzBlueprintAssignment [[-SubscriptionId] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30832-107">說明</span><span class="sxs-lookup"><span data-stu-id="30832-107">DESCRIPTION</span></span>
<span data-ttu-id="30832-108">取得一或多個藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="30832-108">Get one or more blueprint assignments.</span></span> <span data-ttu-id="30832-109">在訂閱範圍中存在藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="30832-109">Blueprint assignments exist at the subscription scope.</span></span>

## <span data-ttu-id="30832-110">示例</span><span class="sxs-lookup"><span data-stu-id="30832-110">EXAMPLES</span></span>

### <span data-ttu-id="30832-111">範例1</span><span class="sxs-lookup"><span data-stu-id="30832-111">Example 1</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000"

Name              : Assignment-PS-BlueprintDefinition
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/Assignment-PS-BlueprintDefinition
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : AllResourcesReadOnly
ProvisioningState : Succeeded
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="30832-112">在指定的訂閱中取得藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="30832-112">Get the blueprint assignments within the specified subscription.</span></span>

### <span data-ttu-id="30832-113">範例2</span><span class="sxs-lookup"><span data-stu-id="30832-113">Example 2</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myAssignmentName"
```

<span data-ttu-id="30832-114">在指定的訂閱中取得具有指定名稱的藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="30832-114">Get the blueprint assignment with the given name within the specified subscription.</span></span>

## <span data-ttu-id="30832-115">參數</span><span class="sxs-lookup"><span data-stu-id="30832-115">PARAMETERS</span></span>

### <span data-ttu-id="30832-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30832-116">-DefaultProfile</span></span>
<span data-ttu-id="30832-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="30832-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30832-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="30832-118">-Name</span></span>
<span data-ttu-id="30832-119">藍圖作業名稱。</span><span class="sxs-lookup"><span data-stu-id="30832-119">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlueprintAssignmentByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30832-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="30832-120">-SubscriptionId</span></span>
<span data-ttu-id="30832-121">已部署藍圖指派的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="30832-121">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30832-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30832-122">CommonParameters</span></span>
<span data-ttu-id="30832-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="30832-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30832-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="30832-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30832-125">輸入</span><span class="sxs-lookup"><span data-stu-id="30832-125">INPUTS</span></span>

### <span data-ttu-id="30832-126">System.object</span><span class="sxs-lookup"><span data-stu-id="30832-126">System.String</span></span>

## <span data-ttu-id="30832-127">輸出</span><span class="sxs-lookup"><span data-stu-id="30832-127">OUTPUTS</span></span>

### <span data-ttu-id="30832-128">System.object</span><span class="sxs-lookup"><span data-stu-id="30832-128">System.Object</span></span>
## <span data-ttu-id="30832-129">筆記</span><span class="sxs-lookup"><span data-stu-id="30832-129">NOTES</span></span>

## <span data-ttu-id="30832-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="30832-130">RELATED LINKS</span></span>
