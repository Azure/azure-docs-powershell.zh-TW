---
external help file: Microsoft.Azure.Commands.Subscription.dll-Help.xml
Module Name: AzureRM.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.subscription/new-azurermsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscription.md
ms.openlocfilehash: cc88f762f1e965eb4e46462f7d43074fa3fe4646
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455904"
---
# <span data-ttu-id="51d17-101">New-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="51d17-101">New-AzureRmSubscription</span></span>

## <span data-ttu-id="51d17-102">摘要</span><span class="sxs-lookup"><span data-stu-id="51d17-102">SYNOPSIS</span></span>
<span data-ttu-id="51d17-103">建立 Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="51d17-103">Creates an Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51d17-104">句法</span><span class="sxs-lookup"><span data-stu-id="51d17-104">SYNTAX</span></span>

```
New-AzureRmSubscription -EnrollmentAccountObjectId <String> [[-Name] <String>] -OfferType <String>
 [-OwnerObjectId <String[]>] [-OwnerSignInName <String[]>] [-OwnerApplicationId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51d17-105">說明</span><span class="sxs-lookup"><span data-stu-id="51d17-105">DESCRIPTION</span></span>
<span data-ttu-id="51d17-106">**新的-AzureRmSubscription** Cmdlet 會建立 Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="51d17-106">The **New-AzureRmSubscription** cmdlet creates an Azure subscription.</span></span>

## <span data-ttu-id="51d17-107">示例</span><span class="sxs-lookup"><span data-stu-id="51d17-107">EXAMPLES</span></span>

### <span data-ttu-id="51d17-108">範例1</span><span class="sxs-lookup"><span data-stu-id="51d17-108">Example 1</span></span>
```
PS C:\> New-AzureRmSubscription -Name "My Subscription" -EnrollmentAccountObjectId ((Get-AzureRmEnrollmentAccount)[0].ObjectId) -OfferType MS-AZR-0017P

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="51d17-109">在具有指定優惠類型的指定註冊帳戶下建立 Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="51d17-109">Creates an Azure subscription under the specified enrollment account with the specified offer type.</span></span>

## <span data-ttu-id="51d17-110">參數</span><span class="sxs-lookup"><span data-stu-id="51d17-110">PARAMETERS</span></span>

### <span data-ttu-id="51d17-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51d17-111">-AsJob</span></span>
<span data-ttu-id="51d17-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="51d17-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51d17-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51d17-113">-DefaultProfile</span></span>
<span data-ttu-id="51d17-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="51d17-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51d17-115">-EnrollmentAccountObjectId</span><span class="sxs-lookup"><span data-stu-id="51d17-115">-EnrollmentAccountObjectId</span></span>
<span data-ttu-id="51d17-116">建立訂閱時要使用之註冊帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="51d17-116">Name of the enrollment account to use when creating the subscription.</span></span>

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

### <span data-ttu-id="51d17-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="51d17-117">-Name</span></span>
<span data-ttu-id="51d17-118">要建立之訂閱的名稱。</span><span class="sxs-lookup"><span data-stu-id="51d17-118">The name of the subscription to create.</span></span>

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

### <span data-ttu-id="51d17-119">-OfferType</span><span class="sxs-lookup"><span data-stu-id="51d17-119">-OfferType</span></span>
<span data-ttu-id="51d17-120">建立訂閱時要使用的優惠類型。</span><span class="sxs-lookup"><span data-stu-id="51d17-120">The type of offer to use when creating the subscription.</span></span>

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

### <span data-ttu-id="51d17-121">-OwnerApplicationId</span><span class="sxs-lookup"><span data-stu-id="51d17-121">-OwnerApplicationId</span></span>
<span data-ttu-id="51d17-122">應用程式 SPN (s) 將擁有訂閱的擁有者存取權給擁有者的許可權。</span><span class="sxs-lookup"><span data-stu-id="51d17-122">The app SPN(s) to be granted Owner access to the subscription.</span></span>

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

### <span data-ttu-id="51d17-123">-OwnerObjectId</span><span class="sxs-lookup"><span data-stu-id="51d17-123">-OwnerObjectId</span></span>
<span data-ttu-id="51d17-124">使用者 (s) 或群組物件 (s) 識別碼 (s) 將擁有該訂閱的擁有者存取權。</span><span class="sxs-lookup"><span data-stu-id="51d17-124">The user(s) or group object(s) id(s) to be granted Owner access to the subscription.</span></span>

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

### <span data-ttu-id="51d17-125">-OwnerSignInName</span><span class="sxs-lookup"><span data-stu-id="51d17-125">-OwnerSignInName</span></span>
<span data-ttu-id="51d17-126">使用者 (s) 被授予訂閱擁有者的許可權。</span><span class="sxs-lookup"><span data-stu-id="51d17-126">The user(s) to be granted Owner access to the subscription.</span></span>

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

### <span data-ttu-id="51d17-127">-確認</span><span class="sxs-lookup"><span data-stu-id="51d17-127">-Confirm</span></span>
<span data-ttu-id="51d17-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="51d17-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51d17-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51d17-129">-WhatIf</span></span>
<span data-ttu-id="51d17-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="51d17-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51d17-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="51d17-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51d17-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51d17-132">CommonParameters</span></span>
<span data-ttu-id="51d17-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="51d17-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51d17-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="51d17-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51d17-135">輸入</span><span class="sxs-lookup"><span data-stu-id="51d17-135">INPUTS</span></span>

### <span data-ttu-id="51d17-136">所有</span><span class="sxs-lookup"><span data-stu-id="51d17-136">None</span></span>

## <span data-ttu-id="51d17-137">輸出</span><span class="sxs-lookup"><span data-stu-id="51d17-137">OUTPUTS</span></span>

### <span data-ttu-id="51d17-138">PSAzureSubscription 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="51d17-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="51d17-139">筆記</span><span class="sxs-lookup"><span data-stu-id="51d17-139">NOTES</span></span>

## <span data-ttu-id="51d17-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="51d17-140">RELATED LINKS</span></span>
