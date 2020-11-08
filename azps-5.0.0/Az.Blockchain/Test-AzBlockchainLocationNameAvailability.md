---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/test-azblockchainlocationnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
ms.openlocfilehash: 42bd50dd96d235db823ec12498388f78d5ec641c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139864"
---
# <span data-ttu-id="40dc7-101">Test-AzBlockchainLocationNameAvailability</span><span class="sxs-lookup"><span data-stu-id="40dc7-101">Test-AzBlockchainLocationNameAvailability</span></span>

## <span data-ttu-id="40dc7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="40dc7-102">SYNOPSIS</span></span>
<span data-ttu-id="40dc7-103">檢查資源名稱是否可用。</span><span class="sxs-lookup"><span data-stu-id="40dc7-103">To check whether a resource name is available.</span></span>

## <span data-ttu-id="40dc7-104">句法</span><span class="sxs-lookup"><span data-stu-id="40dc7-104">SYNTAX</span></span>

```
Test-AzBlockchainLocationNameAvailability -Location <String> [-SubscriptionId <String>] [-Name <String>]
 [-Type <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="40dc7-105">說明</span><span class="sxs-lookup"><span data-stu-id="40dc7-105">DESCRIPTION</span></span>
<span data-ttu-id="40dc7-106">檢查資源名稱是否可用。</span><span class="sxs-lookup"><span data-stu-id="40dc7-106">To check whether a resource name is available.</span></span>

## <span data-ttu-id="40dc7-107">示例</span><span class="sxs-lookup"><span data-stu-id="40dc7-107">EXAMPLES</span></span>

### <span data-ttu-id="40dc7-108">範例1：檢查資源名稱是否可供使用</span><span class="sxs-lookup"><span data-stu-id="40dc7-108">Example 1: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name erw123 -type Microsoft.Blockchain/blockchainMembers

Message NameAvailable Reason
------- ------------- ------
        True          NotSpecified
```

<span data-ttu-id="40dc7-109">該命令會檢查資源名稱是否可用。</span><span class="sxs-lookup"><span data-stu-id="40dc7-109">The command checks whether a resource name is available.</span></span>

### <span data-ttu-id="40dc7-110">範例2：檢查資源名稱是否可供使用</span><span class="sxs-lookup"><span data-stu-id="40dc7-110">Example 2: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name 123 -Type Microsoft.Blockchain/blockchainMembers

Message                                                                                                                                                                             NameAvailable Reason
-------                                                                                                                                                                             ------------- ------
The blockchain member name is invalid. It can contain only lowercase letters and numbers. The first character must be a letter. The value must be between 2 and 20 characters long. False         Invalid
```

<span data-ttu-id="40dc7-111">該命令會檢查資源名稱是否可用。</span><span class="sxs-lookup"><span data-stu-id="40dc7-111">The command checks whether a resource name is available.</span></span>

## <span data-ttu-id="40dc7-112">參數</span><span class="sxs-lookup"><span data-stu-id="40dc7-112">PARAMETERS</span></span>

### <span data-ttu-id="40dc7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40dc7-113">-DefaultProfile</span></span>
<span data-ttu-id="40dc7-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="40dc7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40dc7-115">-位置</span><span class="sxs-lookup"><span data-stu-id="40dc7-115">-Location</span></span>
<span data-ttu-id="40dc7-116">位置名稱。</span><span class="sxs-lookup"><span data-stu-id="40dc7-116">Location Name.</span></span>

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

### <span data-ttu-id="40dc7-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="40dc7-117">-Name</span></span>
<span data-ttu-id="40dc7-118">取得或設定要檢查的名稱。</span><span class="sxs-lookup"><span data-stu-id="40dc7-118">Gets or sets the name to check.</span></span>

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

### <span data-ttu-id="40dc7-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="40dc7-119">-SubscriptionId</span></span>
<span data-ttu-id="40dc7-120">取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="40dc7-120">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="40dc7-121">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="40dc7-121">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="40dc7-122">-類型</span><span class="sxs-lookup"><span data-stu-id="40dc7-122">-Type</span></span>
<span data-ttu-id="40dc7-123">取得或設定要檢查的資源類型。</span><span class="sxs-lookup"><span data-stu-id="40dc7-123">Gets or sets the type of the resource to check.</span></span>

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

### <span data-ttu-id="40dc7-124">-確認</span><span class="sxs-lookup"><span data-stu-id="40dc7-124">-Confirm</span></span>
<span data-ttu-id="40dc7-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="40dc7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40dc7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40dc7-126">-WhatIf</span></span>
<span data-ttu-id="40dc7-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="40dc7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40dc7-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="40dc7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40dc7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40dc7-129">CommonParameters</span></span>
<span data-ttu-id="40dc7-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="40dc7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40dc7-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="40dc7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40dc7-132">輸入</span><span class="sxs-lookup"><span data-stu-id="40dc7-132">INPUTS</span></span>

## <span data-ttu-id="40dc7-133">輸出</span><span class="sxs-lookup"><span data-stu-id="40dc7-133">OUTPUTS</span></span>

### <span data-ttu-id="40dc7-134">INameAvailability （Blockchain）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="40dc7-134">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.INameAvailability</span></span>

## <span data-ttu-id="40dc7-135">筆記</span><span class="sxs-lookup"><span data-stu-id="40dc7-135">NOTES</span></span>

<span data-ttu-id="40dc7-136">別名</span><span class="sxs-lookup"><span data-stu-id="40dc7-136">ALIASES</span></span>

## <span data-ttu-id="40dc7-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="40dc7-137">RELATED LINKS</span></span>

