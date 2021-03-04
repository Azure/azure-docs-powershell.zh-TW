---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/test-azblockchainlocationnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
ms.openlocfilehash: 9507271fe283277c212e4ed8d4117483a2797857
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906337"
---
# <span data-ttu-id="5f2cd-101">Test-AzBlockchainLocationNameAvailability</span><span class="sxs-lookup"><span data-stu-id="5f2cd-101">Test-AzBlockchainLocationNameAvailability</span></span>

## <span data-ttu-id="5f2cd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5f2cd-102">SYNOPSIS</span></span>
<span data-ttu-id="5f2cd-103">檢查資源名稱是否可用。</span><span class="sxs-lookup"><span data-stu-id="5f2cd-103">To check whether a resource name is available.</span></span>

## <span data-ttu-id="5f2cd-104">語法</span><span class="sxs-lookup"><span data-stu-id="5f2cd-104">SYNTAX</span></span>

```
Test-AzBlockchainLocationNameAvailability -Location <String> [-SubscriptionId <String>] [-Name <String>]
 [-Type <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5f2cd-105">描述</span><span class="sxs-lookup"><span data-stu-id="5f2cd-105">DESCRIPTION</span></span>
<span data-ttu-id="5f2cd-106">檢查資源名稱是否可用。</span><span class="sxs-lookup"><span data-stu-id="5f2cd-106">To check whether a resource name is available.</span></span>

## <span data-ttu-id="5f2cd-107">例子</span><span class="sxs-lookup"><span data-stu-id="5f2cd-107">EXAMPLES</span></span>

### <span data-ttu-id="5f2cd-108">範例 1：檢查資源名稱是否可用</span><span class="sxs-lookup"><span data-stu-id="5f2cd-108">Example 1: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name erw123 -type Microsoft.Blockchain/blockchainMembers

Message NameAvailable Reason
------- ------------- ------
        True          NotSpecified
```

<span data-ttu-id="5f2cd-109">命令會檢查資源名稱是否可用。</span><span class="sxs-lookup"><span data-stu-id="5f2cd-109">The command checks whether a resource name is available.</span></span>

### <span data-ttu-id="5f2cd-110">範例 2：檢查資源名稱是否可用</span><span class="sxs-lookup"><span data-stu-id="5f2cd-110">Example 2: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name 123 -Type Microsoft.Blockchain/blockchainMembers

Message                                                                                                                                                                             NameAvailable Reason
-------                                                                                                                                                                             ------------- ------
The blockchain member name is invalid. It can contain only lowercase letters and numbers. The first character must be a letter. The value must be between 2 and 20 characters long. False         Invalid
```

<span data-ttu-id="5f2cd-111">命令會檢查資源名稱是否可用。</span><span class="sxs-lookup"><span data-stu-id="5f2cd-111">The command checks whether a resource name is available.</span></span>

## <span data-ttu-id="5f2cd-112">參數</span><span class="sxs-lookup"><span data-stu-id="5f2cd-112">PARAMETERS</span></span>

### <span data-ttu-id="5f2cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f2cd-113">-DefaultProfile</span></span>
<span data-ttu-id="5f2cd-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5f2cd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f2cd-115">-位置</span><span class="sxs-lookup"><span data-stu-id="5f2cd-115">-Location</span></span>
<span data-ttu-id="5f2cd-116">位置名稱。</span><span class="sxs-lookup"><span data-stu-id="5f2cd-116">Location Name.</span></span>

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

### <span data-ttu-id="5f2cd-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="5f2cd-117">-Name</span></span>
<span data-ttu-id="5f2cd-118">獲得或設定要檢查的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f2cd-118">Gets or sets the name to check.</span></span>

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

### <span data-ttu-id="5f2cd-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5f2cd-119">-SubscriptionId</span></span>
<span data-ttu-id="5f2cd-120">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="5f2cd-120">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="5f2cd-121">訂閱識別碼是每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="5f2cd-121">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f2cd-122">-類型</span><span class="sxs-lookup"><span data-stu-id="5f2cd-122">-Type</span></span>
<span data-ttu-id="5f2cd-123">獲取或設定要檢查的資源類型。</span><span class="sxs-lookup"><span data-stu-id="5f2cd-123">Gets or sets the type of the resource to check.</span></span>

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

### <span data-ttu-id="5f2cd-124">-確認</span><span class="sxs-lookup"><span data-stu-id="5f2cd-124">-Confirm</span></span>
<span data-ttu-id="5f2cd-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5f2cd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f2cd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f2cd-126">-WhatIf</span></span>
<span data-ttu-id="5f2cd-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5f2cd-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f2cd-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5f2cd-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f2cd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f2cd-129">CommonParameters</span></span>
<span data-ttu-id="5f2cd-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5f2cd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f2cd-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5f2cd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f2cd-132">輸入</span><span class="sxs-lookup"><span data-stu-id="5f2cd-132">INPUTS</span></span>

## <span data-ttu-id="5f2cd-133">輸出</span><span class="sxs-lookup"><span data-stu-id="5f2cd-133">OUTPUTS</span></span>

### <span data-ttu-id="5f2cd-134">Microsoft.Azure.PowerShell.Cmdlets.Azure.Models.Api20180601Preview.INameAvailability</span><span class="sxs-lookup"><span data-stu-id="5f2cd-134">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.INameAvailability</span></span>

## <span data-ttu-id="5f2cd-135">筆記</span><span class="sxs-lookup"><span data-stu-id="5f2cd-135">NOTES</span></span>

<span data-ttu-id="5f2cd-136">別名</span><span class="sxs-lookup"><span data-stu-id="5f2cd-136">ALIASES</span></span>

## <span data-ttu-id="5f2cd-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="5f2cd-137">RELATED LINKS</span></span>

