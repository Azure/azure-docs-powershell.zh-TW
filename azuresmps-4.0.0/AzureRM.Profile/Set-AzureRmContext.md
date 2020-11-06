---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: e141e2af2dea2a07a9a64ab25c2417ffb6842837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442975"
---
# <span data-ttu-id="6bd42-101">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="6bd42-101">Set-AzureRmContext</span></span>

## <span data-ttu-id="6bd42-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6bd42-102">SYNOPSIS</span></span>
<span data-ttu-id="6bd42-103">設定要在目前會話中使用之 Cmdlet 的租使用者、訂閱及環境。</span><span class="sxs-lookup"><span data-stu-id="6bd42-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

## <span data-ttu-id="6bd42-104">句法</span><span class="sxs-lookup"><span data-stu-id="6bd42-104">SYNTAX</span></span>

### <span data-ttu-id="6bd42-105">SubscriptionName (預設) </span><span class="sxs-lookup"><span data-stu-id="6bd42-105">SubscriptionName (Default)</span></span>
```
Set-AzureRmContext [-SubscriptionName <String>] [-TenantId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bd42-106">這裡</span><span class="sxs-lookup"><span data-stu-id="6bd42-106">Context</span></span>
```
Set-AzureRmContext -Context <PSAzureContext> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bd42-107">Id</span><span class="sxs-lookup"><span data-stu-id="6bd42-107">SubscriptionId</span></span>
```
Set-AzureRmContext [-TenantId <String>] [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bd42-108">說明</span><span class="sxs-lookup"><span data-stu-id="6bd42-108">DESCRIPTION</span></span>
<span data-ttu-id="6bd42-109">Set-AzureRmContext Cmdlet 會針對您在目前會話中執行的 Cmdlet 設定驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="6bd42-109">The Set-AzureRmContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="6bd42-110">內容包括租使用者、訂閱及環境資訊。</span><span class="sxs-lookup"><span data-stu-id="6bd42-110">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="6bd42-111">示例</span><span class="sxs-lookup"><span data-stu-id="6bd42-111">EXAMPLES</span></span>

### <span data-ttu-id="6bd42-112">範例1：設定訂閱內容</span><span class="sxs-lookup"><span data-stu-id="6bd42-112">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Account      : PFuller@contoso.com
Environment  : AzureCloud
Subscription : xxxx-xxxx-xxxx-xxxx
Tenant       : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="6bd42-113">這個命令會將內容設定為使用指定的訂閱。</span><span class="sxs-lookup"><span data-stu-id="6bd42-113">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="6bd42-114">參數</span><span class="sxs-lookup"><span data-stu-id="6bd42-114">PARAMETERS</span></span>

### <span data-ttu-id="6bd42-115">-內容</span><span class="sxs-lookup"><span data-stu-id="6bd42-115">-Context</span></span>
<span data-ttu-id="6bd42-116">指定目前會話的內容。</span><span class="sxs-lookup"><span data-stu-id="6bd42-116">Specifies the context for the current session.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: Context
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd42-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6bd42-117">-SubscriptionId</span></span>
<span data-ttu-id="6bd42-118">指定此 Cmdlet 針對目前會話所設定之內容的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="6bd42-118">Specifies the subscription ID for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd42-119">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="6bd42-119">-SubscriptionName</span></span>
<span data-ttu-id="6bd42-120">指定此 Cmdlet 針對目前會話所設定之內容的訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="6bd42-120">Specifies the subscription name for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd42-121">-TenantId</span><span class="sxs-lookup"><span data-stu-id="6bd42-121">-TenantId</span></span>
<span data-ttu-id="6bd42-122">指定此 Cmdlet 針對目前會話所設定之內容的租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="6bd42-122">Specifies the ID of the tenant for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionName, SubscriptionId
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd42-123">-確認</span><span class="sxs-lookup"><span data-stu-id="6bd42-123">-Confirm</span></span>
<span data-ttu-id="6bd42-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6bd42-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bd42-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bd42-125">-WhatIf</span></span>
<span data-ttu-id="6bd42-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6bd42-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6bd42-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6bd42-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bd42-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bd42-128">CommonParameters</span></span>
<span data-ttu-id="6bd42-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6bd42-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bd42-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6bd42-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bd42-131">輸入</span><span class="sxs-lookup"><span data-stu-id="6bd42-131">INPUTS</span></span>

## <span data-ttu-id="6bd42-132">輸出</span><span class="sxs-lookup"><span data-stu-id="6bd42-132">OUTPUTS</span></span>

### <span data-ttu-id="6bd42-133">PSAzureCoNtext</span><span class="sxs-lookup"><span data-stu-id="6bd42-133">PSAzureContext</span></span>

## <span data-ttu-id="6bd42-134">筆記</span><span class="sxs-lookup"><span data-stu-id="6bd42-134">NOTES</span></span>

## <span data-ttu-id="6bd42-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="6bd42-135">RELATED LINKS</span></span>

[<span data-ttu-id="6bd42-136">AzureRMCoNtext</span><span class="sxs-lookup"><span data-stu-id="6bd42-136">Get-AzureRMContext</span></span>]()

