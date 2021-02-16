---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/test-azblockchainlocationnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
ms.openlocfilehash: 42bd50dd96d235db823ec12498388f78d5ec641c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127983"
---
# <span data-ttu-id="0d55a-101">Test-AzBlockchainLocationNameAvailability</span><span class="sxs-lookup"><span data-stu-id="0d55a-101">Test-AzBlockchainLocationNameAvailability</span></span>

## <span data-ttu-id="0d55a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d55a-102">SYNOPSIS</span></span>
<span data-ttu-id="0d55a-103">檢查資源名稱是否可用。</span><span class="sxs-lookup"><span data-stu-id="0d55a-103">To check whether a resource name is available.</span></span>

## <span data-ttu-id="0d55a-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d55a-104">SYNTAX</span></span>

```
Test-AzBlockchainLocationNameAvailability -Location <String> [-SubscriptionId <String>] [-Name <String>]
 [-Type <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0d55a-105">說明</span><span class="sxs-lookup"><span data-stu-id="0d55a-105">DESCRIPTION</span></span>
<span data-ttu-id="0d55a-106">檢查資源名稱是否可用。</span><span class="sxs-lookup"><span data-stu-id="0d55a-106">To check whether a resource name is available.</span></span>

## <span data-ttu-id="0d55a-107">示例</span><span class="sxs-lookup"><span data-stu-id="0d55a-107">EXAMPLES</span></span>

### <span data-ttu-id="0d55a-108">範例1：檢查資源名稱是否可供使用</span><span class="sxs-lookup"><span data-stu-id="0d55a-108">Example 1: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name erw123 -type Microsoft.Blockchain/blockchainMembers

Message NameAvailable Reason
------- ------------- ------
        True          NotSpecified
```

<span data-ttu-id="0d55a-109">該命令會檢查資源名稱是否可用。</span><span class="sxs-lookup"><span data-stu-id="0d55a-109">The command checks whether a resource name is available.</span></span>

### <span data-ttu-id="0d55a-110">範例2：檢查資源名稱是否可供使用</span><span class="sxs-lookup"><span data-stu-id="0d55a-110">Example 2: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name 123 -Type Microsoft.Blockchain/blockchainMembers

Message                                                                                                                                                                             NameAvailable Reason
-------                                                                                                                                                                             ------------- ------
The blockchain member name is invalid. It can contain only lowercase letters and numbers. The first character must be a letter. The value must be between 2 and 20 characters long. False         Invalid
```

<span data-ttu-id="0d55a-111">該命令會檢查資源名稱是否可用。</span><span class="sxs-lookup"><span data-stu-id="0d55a-111">The command checks whether a resource name is available.</span></span>

## <span data-ttu-id="0d55a-112">參數</span><span class="sxs-lookup"><span data-stu-id="0d55a-112">PARAMETERS</span></span>

### <span data-ttu-id="0d55a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d55a-113">-DefaultProfile</span></span>
<span data-ttu-id="0d55a-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d55a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d55a-115">-位置</span><span class="sxs-lookup"><span data-stu-id="0d55a-115">-Location</span></span>
<span data-ttu-id="0d55a-116">位置名稱。</span><span class="sxs-lookup"><span data-stu-id="0d55a-116">Location Name.</span></span>

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

### <span data-ttu-id="0d55a-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="0d55a-117">-Name</span></span>
<span data-ttu-id="0d55a-118">取得或設定要檢查的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d55a-118">Gets or sets the name to check.</span></span>

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

### <span data-ttu-id="0d55a-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0d55a-119">-SubscriptionId</span></span>
<span data-ttu-id="0d55a-120">取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="0d55a-120">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="0d55a-121">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="0d55a-121">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0d55a-122">-類型</span><span class="sxs-lookup"><span data-stu-id="0d55a-122">-Type</span></span>
<span data-ttu-id="0d55a-123">取得或設定要檢查的資源類型。</span><span class="sxs-lookup"><span data-stu-id="0d55a-123">Gets or sets the type of the resource to check.</span></span>

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

### <span data-ttu-id="0d55a-124">-確認</span><span class="sxs-lookup"><span data-stu-id="0d55a-124">-Confirm</span></span>
<span data-ttu-id="0d55a-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0d55a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d55a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d55a-126">-WhatIf</span></span>
<span data-ttu-id="0d55a-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0d55a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d55a-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0d55a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d55a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d55a-129">CommonParameters</span></span>
<span data-ttu-id="0d55a-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d55a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d55a-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0d55a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d55a-132">輸入</span><span class="sxs-lookup"><span data-stu-id="0d55a-132">INPUTS</span></span>

## <span data-ttu-id="0d55a-133">輸出</span><span class="sxs-lookup"><span data-stu-id="0d55a-133">OUTPUTS</span></span>

### <span data-ttu-id="0d55a-134">INameAvailability （Blockchain）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="0d55a-134">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.INameAvailability</span></span>

## <span data-ttu-id="0d55a-135">筆記</span><span class="sxs-lookup"><span data-stu-id="0d55a-135">NOTES</span></span>

<span data-ttu-id="0d55a-136">別名</span><span class="sxs-lookup"><span data-stu-id="0d55a-136">ALIASES</span></span>

## <span data-ttu-id="0d55a-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d55a-137">RELATED LINKS</span></span>

