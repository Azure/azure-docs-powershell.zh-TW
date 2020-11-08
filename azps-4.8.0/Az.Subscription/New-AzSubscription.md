---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/new-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscription.md
ms.openlocfilehash: 167678bfe84117cdc53e9e90b520abe24fed4b92
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127188"
---
# <span data-ttu-id="320e7-101">New-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="320e7-101">New-AzSubscription</span></span>

## <span data-ttu-id="320e7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="320e7-102">SYNOPSIS</span></span>
<span data-ttu-id="320e7-103">建立 Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="320e7-103">Creates an Azure subscription.</span></span>

## <span data-ttu-id="320e7-104">句法</span><span class="sxs-lookup"><span data-stu-id="320e7-104">SYNTAX</span></span>

```
New-AzSubscription -EnrollmentAccountObjectId <String> [[-Name] <String>] -OfferType <String>
 [-OwnerObjectId <String[]>] [-OwnerSignInName <String[]>] [-OwnerApplicationId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="320e7-105">說明</span><span class="sxs-lookup"><span data-stu-id="320e7-105">DESCRIPTION</span></span>
<span data-ttu-id="320e7-106">**新的-AzSubscription** Cmdlet 會建立 Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="320e7-106">The **New-AzSubscription** cmdlet creates an Azure subscription.</span></span>

## <span data-ttu-id="320e7-107">示例</span><span class="sxs-lookup"><span data-stu-id="320e7-107">EXAMPLES</span></span>

### <span data-ttu-id="320e7-108">範例1</span><span class="sxs-lookup"><span data-stu-id="320e7-108">Example 1</span></span>
```
PS C:\> New-AzSubscription -Name "My Subscription" -EnrollmentAccountObjectId ((Get-AzEnrollmentAccount)[0].ObjectId) -OfferType MS-AZR-0017P

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="320e7-109">在具有指定優惠類型的指定註冊帳戶下建立 Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="320e7-109">Creates an Azure subscription under the specified enrollment account with the specified offer type.</span></span>

## <span data-ttu-id="320e7-110">參數</span><span class="sxs-lookup"><span data-stu-id="320e7-110">PARAMETERS</span></span>

### <span data-ttu-id="320e7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="320e7-111">-AsJob</span></span>
<span data-ttu-id="320e7-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="320e7-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="320e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="320e7-113">-DefaultProfile</span></span>
<span data-ttu-id="320e7-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="320e7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="320e7-115">-EnrollmentAccountObjectId</span><span class="sxs-lookup"><span data-stu-id="320e7-115">-EnrollmentAccountObjectId</span></span>
<span data-ttu-id="320e7-116">建立訂閱時要使用之註冊帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="320e7-116">Name of the enrollment account to use when creating the subscription.</span></span>

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

### <span data-ttu-id="320e7-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="320e7-117">-Name</span></span>
<span data-ttu-id="320e7-118">要建立之訂閱的名稱。</span><span class="sxs-lookup"><span data-stu-id="320e7-118">The name of the subscription to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320e7-119">-OfferType</span><span class="sxs-lookup"><span data-stu-id="320e7-119">-OfferType</span></span>
<span data-ttu-id="320e7-120">建立訂閱時要使用的優惠類型。</span><span class="sxs-lookup"><span data-stu-id="320e7-120">The type of offer to use when creating the subscription.</span></span>

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

### <span data-ttu-id="320e7-121">-OwnerApplicationId</span><span class="sxs-lookup"><span data-stu-id="320e7-121">-OwnerApplicationId</span></span>
<span data-ttu-id="320e7-122">應用程式 SPN (s) 將擁有訂閱的擁有者存取權給擁有者的許可權。</span><span class="sxs-lookup"><span data-stu-id="320e7-122">The app SPN(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerSPN, OwnerServicePrincipalName

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320e7-123">-OwnerObjectId</span><span class="sxs-lookup"><span data-stu-id="320e7-123">-OwnerObjectId</span></span>
<span data-ttu-id="320e7-124">使用者 (s) 或群組物件 (s) 識別碼 (s) 將擁有該訂閱的擁有者存取權。</span><span class="sxs-lookup"><span data-stu-id="320e7-124">The user(s) or group object(s) id(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerId, OwnerPrincipalId

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320e7-125">-OwnerSignInName</span><span class="sxs-lookup"><span data-stu-id="320e7-125">-OwnerSignInName</span></span>
<span data-ttu-id="320e7-126">使用者 (s) 被授予訂閱擁有者的許可權。</span><span class="sxs-lookup"><span data-stu-id="320e7-126">The user(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerEmail, OwnerUserPrincipalName

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320e7-127">-確認</span><span class="sxs-lookup"><span data-stu-id="320e7-127">-Confirm</span></span>
<span data-ttu-id="320e7-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="320e7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="320e7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="320e7-129">-WhatIf</span></span>
<span data-ttu-id="320e7-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="320e7-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="320e7-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="320e7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="320e7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="320e7-132">CommonParameters</span></span>
<span data-ttu-id="320e7-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="320e7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="320e7-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="320e7-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="320e7-135">輸入</span><span class="sxs-lookup"><span data-stu-id="320e7-135">INPUTS</span></span>

### <span data-ttu-id="320e7-136">所有</span><span class="sxs-lookup"><span data-stu-id="320e7-136">None</span></span>

## <span data-ttu-id="320e7-137">輸出</span><span class="sxs-lookup"><span data-stu-id="320e7-137">OUTPUTS</span></span>

### <span data-ttu-id="320e7-138">PSAzureSubscription 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="320e7-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="320e7-139">筆記</span><span class="sxs-lookup"><span data-stu-id="320e7-139">NOTES</span></span>

## <span data-ttu-id="320e7-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="320e7-140">RELATED LINKS</span></span>
