---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/powershell/module/az.subscription/update-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
ms.openlocfilehash: 0fe030e3ef4dfcb8e43ba436d37d582871e55a5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907957"
---
# <span data-ttu-id="fa75b-101">Update-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="fa75b-101">Update-AzSubscription</span></span>

## <span data-ttu-id="fa75b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fa75b-102">SYNOPSIS</span></span>
<span data-ttu-id="fa75b-103">更新 Azure 訂閱</span><span class="sxs-lookup"><span data-stu-id="fa75b-103">Updates an Azure Subscription</span></span>

## <span data-ttu-id="fa75b-104">語法</span><span class="sxs-lookup"><span data-stu-id="fa75b-104">SYNTAX</span></span>

```
Update-AzSubscription -SubscriptionId <String> -Action <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa75b-105">描述</span><span class="sxs-lookup"><span data-stu-id="fa75b-105">DESCRIPTION</span></span>
<span data-ttu-id="fa75b-106">**Update-AzSubscription** Cmdlet 會更新 Azure 訂閱</span><span class="sxs-lookup"><span data-stu-id="fa75b-106">The **Update-AzSubscription** cmdlet updates an Azure subscription</span></span>

## <span data-ttu-id="fa75b-107">例子</span><span class="sxs-lookup"><span data-stu-id="fa75b-107">EXAMPLES</span></span>

### <span data-ttu-id="fa75b-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="fa75b-108">Example 1</span></span>
```powershell
PS C:\> Update-AzSubscription -SubscriptionId "86869d42-1782-4337-98b0-c905fb937d46" -Action "Cancel"

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="fa75b-109">更新訂閱</span><span class="sxs-lookup"><span data-stu-id="fa75b-109">Updates the subscription</span></span>

## <span data-ttu-id="fa75b-110">參數</span><span class="sxs-lookup"><span data-stu-id="fa75b-110">PARAMETERS</span></span>

### <span data-ttu-id="fa75b-111">-動作</span><span class="sxs-lookup"><span data-stu-id="fa75b-111">-Action</span></span>
<span data-ttu-id="fa75b-112">在訂閱上執行的動作</span><span class="sxs-lookup"><span data-stu-id="fa75b-112">Action to perform on subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa75b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa75b-113">-AsJob</span></span>
<span data-ttu-id="fa75b-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fa75b-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa75b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa75b-115">-DefaultProfile</span></span>
<span data-ttu-id="fa75b-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fa75b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa75b-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="fa75b-117">-Name</span></span>
<span data-ttu-id="fa75b-118">訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="fa75b-118">Name of the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa75b-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fa75b-119">-SubscriptionId</span></span>
<span data-ttu-id="fa75b-120">要更新的訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="fa75b-120">Subscription Id to update</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa75b-121">-確認</span><span class="sxs-lookup"><span data-stu-id="fa75b-121">-Confirm</span></span>
<span data-ttu-id="fa75b-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fa75b-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa75b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa75b-123">-WhatIf</span></span>
<span data-ttu-id="fa75b-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fa75b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa75b-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fa75b-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa75b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa75b-126">CommonParameters</span></span>
<span data-ttu-id="fa75b-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fa75b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa75b-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa75b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa75b-129">輸入</span><span class="sxs-lookup"><span data-stu-id="fa75b-129">INPUTS</span></span>

### <span data-ttu-id="fa75b-130">沒有</span><span class="sxs-lookup"><span data-stu-id="fa75b-130">None</span></span>

## <span data-ttu-id="fa75b-131">輸出</span><span class="sxs-lookup"><span data-stu-id="fa75b-131">OUTPUTS</span></span>

### <span data-ttu-id="fa75b-132">Microsoft.Azure.Commands.subscription.models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="fa75b-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="fa75b-133">筆記</span><span class="sxs-lookup"><span data-stu-id="fa75b-133">NOTES</span></span>

## <span data-ttu-id="fa75b-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="fa75b-134">RELATED LINKS</span></span>
