---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/new-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationService.md
ms.openlocfilehash: 8382358e6bad15948ed8cdfeb904cf8c431bd131
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912090"
---
# <span data-ttu-id="ef139-101">New-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="ef139-101">New-AzCommunicationService</span></span>

## <span data-ttu-id="ef139-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ef139-102">SYNOPSIS</span></span>
<span data-ttu-id="ef139-103">建立新 CommunicationService 或更新現有的 CommunicationService。</span><span class="sxs-lookup"><span data-stu-id="ef139-103">Create a new CommunicationService or update an existing CommunicationService.</span></span>

## <span data-ttu-id="ef139-104">語法</span><span class="sxs-lookup"><span data-stu-id="ef139-104">SYNTAX</span></span>

```
New-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DataLocation <String>] [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ef139-105">描述</span><span class="sxs-lookup"><span data-stu-id="ef139-105">DESCRIPTION</span></span>
<span data-ttu-id="ef139-106">建立新 CommunicationService 或更新現有的 CommunicationService。</span><span class="sxs-lookup"><span data-stu-id="ef139-106">Create a new CommunicationService or update an existing CommunicationService.</span></span>

## <span data-ttu-id="ef139-107">例子</span><span class="sxs-lookup"><span data-stu-id="ef139-107">EXAMPLES</span></span>

### <span data-ttu-id="ef139-108">範例 1：建立 ACS 資源</span><span class="sxs-lookup"><span data-stu-id="ef139-108">Example 1: Create a ACS resource</span></span>
```powershell
PS C:\> New-AzCommunicationService -ResourceGroupName ContosoResourceProvider1 -Name ContosoAcsResource1 -DataLocation UnitedStates -Location Global

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="ef139-109">使用指定的參數建立 ACS 資源。</span><span class="sxs-lookup"><span data-stu-id="ef139-109">Creates a ACS resource using the specified parameters.</span></span>

## <span data-ttu-id="ef139-110">參數</span><span class="sxs-lookup"><span data-stu-id="ef139-110">PARAMETERS</span></span>

### <span data-ttu-id="ef139-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef139-111">-AsJob</span></span>
<span data-ttu-id="ef139-112">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="ef139-112">Run the command as a job</span></span>

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

### <span data-ttu-id="ef139-113">-DataLocation</span><span class="sxs-lookup"><span data-stu-id="ef139-113">-DataLocation</span></span>
<span data-ttu-id="ef139-114">通訊服務儲存其資料的位置。</span><span class="sxs-lookup"><span data-stu-id="ef139-114">The location where the communication service stores its data at rest.</span></span>

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

### <span data-ttu-id="ef139-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef139-115">-DefaultProfile</span></span>
<span data-ttu-id="ef139-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef139-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef139-117">-位置</span><span class="sxs-lookup"><span data-stu-id="ef139-117">-Location</span></span>
<span data-ttu-id="ef139-118">執行 CommunicationService 的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="ef139-118">The Azure location where the CommunicationService is running.</span></span>

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

### <span data-ttu-id="ef139-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="ef139-119">-Name</span></span>
<span data-ttu-id="ef139-120">CommunicationService 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef139-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef139-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ef139-121">-NoWait</span></span>
<span data-ttu-id="ef139-122">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="ef139-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ef139-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef139-123">-ResourceGroupName</span></span>
<span data-ttu-id="ef139-124">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="ef139-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ef139-125">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="ef139-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ef139-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ef139-126">-SubscriptionId</span></span>
<span data-ttu-id="ef139-127">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="ef139-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ef139-128">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="ef139-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ef139-129">-標記</span><span class="sxs-lookup"><span data-stu-id="ef139-129">-Tag</span></span>
<span data-ttu-id="ef139-130">服務標記，這是描述資源的金鑰值組清單。</span><span class="sxs-lookup"><span data-stu-id="ef139-130">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef139-131">-確認</span><span class="sxs-lookup"><span data-stu-id="ef139-131">-Confirm</span></span>
<span data-ttu-id="ef139-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ef139-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef139-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef139-133">-WhatIf</span></span>
<span data-ttu-id="ef139-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ef139-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef139-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef139-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef139-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef139-136">CommonParameters</span></span>
<span data-ttu-id="ef139-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ef139-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef139-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef139-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef139-139">輸入</span><span class="sxs-lookup"><span data-stu-id="ef139-139">INPUTS</span></span>

## <span data-ttu-id="ef139-140">輸出</span><span class="sxs-lookup"><span data-stu-id="ef139-140">OUTPUTS</span></span>

### <span data-ttu-id="ef139-141">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="ef139-141">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="ef139-142">筆記</span><span class="sxs-lookup"><span data-stu-id="ef139-142">NOTES</span></span>

<span data-ttu-id="ef139-143">別名</span><span class="sxs-lookup"><span data-stu-id="ef139-143">ALIASES</span></span>

## <span data-ttu-id="ef139-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef139-144">RELATED LINKS</span></span>

