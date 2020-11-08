---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/update-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
ms.openlocfilehash: 77e7904a83b7d14fac1379532a619547888d5542
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139417"
---
# <span data-ttu-id="26fd3-101">Update-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="26fd3-101">Update-AzSubscription</span></span>

## <span data-ttu-id="26fd3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="26fd3-102">SYNOPSIS</span></span>
<span data-ttu-id="26fd3-103">更新 Azure 訂閱</span><span class="sxs-lookup"><span data-stu-id="26fd3-103">Updates an Azure Subscription</span></span>

## <span data-ttu-id="26fd3-104">句法</span><span class="sxs-lookup"><span data-stu-id="26fd3-104">SYNTAX</span></span>

```
Update-AzSubscription -SubscriptionId <String> -Action <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26fd3-105">說明</span><span class="sxs-lookup"><span data-stu-id="26fd3-105">DESCRIPTION</span></span>
<span data-ttu-id="26fd3-106">**AzSubscription** Cmdlet 會更新 Azure 訂閱</span><span class="sxs-lookup"><span data-stu-id="26fd3-106">The **Update-AzSubscription** cmdlet updates an Azure subscription</span></span>

## <span data-ttu-id="26fd3-107">示例</span><span class="sxs-lookup"><span data-stu-id="26fd3-107">EXAMPLES</span></span>

### <span data-ttu-id="26fd3-108">範例1</span><span class="sxs-lookup"><span data-stu-id="26fd3-108">Example 1</span></span>
```powershell
PS C:\> Update-AzSubscription -SubscriptionId "86869d42-1782-4337-98b0-c905fb937d46" -Action "Cancel"

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="26fd3-109">更新訂閱</span><span class="sxs-lookup"><span data-stu-id="26fd3-109">Updates the subscription</span></span>

## <span data-ttu-id="26fd3-110">參數</span><span class="sxs-lookup"><span data-stu-id="26fd3-110">PARAMETERS</span></span>

### <span data-ttu-id="26fd3-111">-動作</span><span class="sxs-lookup"><span data-stu-id="26fd3-111">-Action</span></span>
<span data-ttu-id="26fd3-112">在訂閱上執行的動作</span><span class="sxs-lookup"><span data-stu-id="26fd3-112">Action to perform on subscription</span></span>

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

### <span data-ttu-id="26fd3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26fd3-113">-AsJob</span></span>
<span data-ttu-id="26fd3-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26fd3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26fd3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26fd3-115">-DefaultProfile</span></span>
<span data-ttu-id="26fd3-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="26fd3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26fd3-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="26fd3-117">-Name</span></span>
<span data-ttu-id="26fd3-118">訂閱的名稱</span><span class="sxs-lookup"><span data-stu-id="26fd3-118">Name of the subscription</span></span>

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

### <span data-ttu-id="26fd3-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="26fd3-119">-SubscriptionId</span></span>
<span data-ttu-id="26fd3-120">要更新的訂閱 Id</span><span class="sxs-lookup"><span data-stu-id="26fd3-120">Subscription Id to update</span></span>

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

### <span data-ttu-id="26fd3-121">-確認</span><span class="sxs-lookup"><span data-stu-id="26fd3-121">-Confirm</span></span>
<span data-ttu-id="26fd3-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="26fd3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26fd3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26fd3-123">-WhatIf</span></span>
<span data-ttu-id="26fd3-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="26fd3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26fd3-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26fd3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26fd3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26fd3-126">CommonParameters</span></span>
<span data-ttu-id="26fd3-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="26fd3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26fd3-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="26fd3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26fd3-129">輸入</span><span class="sxs-lookup"><span data-stu-id="26fd3-129">INPUTS</span></span>

### <span data-ttu-id="26fd3-130">所有</span><span class="sxs-lookup"><span data-stu-id="26fd3-130">None</span></span>

## <span data-ttu-id="26fd3-131">輸出</span><span class="sxs-lookup"><span data-stu-id="26fd3-131">OUTPUTS</span></span>

### <span data-ttu-id="26fd3-132">PSAzureSubscription 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="26fd3-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="26fd3-133">筆記</span><span class="sxs-lookup"><span data-stu-id="26fd3-133">NOTES</span></span>

## <span data-ttu-id="26fd3-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="26fd3-134">RELATED LINKS</span></span>