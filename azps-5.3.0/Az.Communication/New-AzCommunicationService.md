---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/new-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationService.md
ms.openlocfilehash: 821590b158478c38e5d4e997254e98a802d4befd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449906"
---
# <span data-ttu-id="b33dd-101">New-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="b33dd-101">New-AzCommunicationService</span></span>

## <span data-ttu-id="b33dd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b33dd-102">SYNOPSIS</span></span>
<span data-ttu-id="b33dd-103">建立新的 CommunicationService 或更新現有的 CommunicationService。</span><span class="sxs-lookup"><span data-stu-id="b33dd-103">Create a new CommunicationService or update an existing CommunicationService.</span></span>

## <span data-ttu-id="b33dd-104">句法</span><span class="sxs-lookup"><span data-stu-id="b33dd-104">SYNTAX</span></span>

```
New-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DataLocation <String>] [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b33dd-105">說明</span><span class="sxs-lookup"><span data-stu-id="b33dd-105">DESCRIPTION</span></span>
<span data-ttu-id="b33dd-106">建立新的 CommunicationService 或更新現有的 CommunicationService。</span><span class="sxs-lookup"><span data-stu-id="b33dd-106">Create a new CommunicationService or update an existing CommunicationService.</span></span>

## <span data-ttu-id="b33dd-107">示例</span><span class="sxs-lookup"><span data-stu-id="b33dd-107">EXAMPLES</span></span>

### <span data-ttu-id="b33dd-108">範例1：建立 ACS 資源</span><span class="sxs-lookup"><span data-stu-id="b33dd-108">Example 1: Create a ACS resource</span></span>
```powershell
PS C:\> New-AzCommunicationService -ResourceGroupName ContosoResourceProvider1 -Name ContosoAcsResource1 -DataLocation UnitedStates -Location Global

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="b33dd-109">使用指定的參數建立 ACS 資源。</span><span class="sxs-lookup"><span data-stu-id="b33dd-109">Creates a ACS resource using the specified parameters.</span></span>

## <span data-ttu-id="b33dd-110">參數</span><span class="sxs-lookup"><span data-stu-id="b33dd-110">PARAMETERS</span></span>

### <span data-ttu-id="b33dd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b33dd-111">-AsJob</span></span>
<span data-ttu-id="b33dd-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="b33dd-112">Run the command as a job</span></span>

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

### <span data-ttu-id="b33dd-113">-DataLocation</span><span class="sxs-lookup"><span data-stu-id="b33dd-113">-DataLocation</span></span>
<span data-ttu-id="b33dd-114">通訊服務儲存其資料的位置。</span><span class="sxs-lookup"><span data-stu-id="b33dd-114">The location where the communication service stores its data at rest.</span></span>

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

### <span data-ttu-id="b33dd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b33dd-115">-DefaultProfile</span></span>
<span data-ttu-id="b33dd-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b33dd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b33dd-117">-位置</span><span class="sxs-lookup"><span data-stu-id="b33dd-117">-Location</span></span>
<span data-ttu-id="b33dd-118">CommunicationService 正在執行的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="b33dd-118">The Azure location where the CommunicationService is running.</span></span>

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

### <span data-ttu-id="b33dd-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="b33dd-119">-Name</span></span>
<span data-ttu-id="b33dd-120">CommunicationService 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="b33dd-120">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="b33dd-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b33dd-121">-NoWait</span></span>
<span data-ttu-id="b33dd-122">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="b33dd-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b33dd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b33dd-123">-ResourceGroupName</span></span>
<span data-ttu-id="b33dd-124">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b33dd-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b33dd-125">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="b33dd-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b33dd-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b33dd-126">-SubscriptionId</span></span>
<span data-ttu-id="b33dd-127">取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="b33dd-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b33dd-128">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="b33dd-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b33dd-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="b33dd-129">-Tag</span></span>
<span data-ttu-id="b33dd-130">服務的標記，是描述資源之鍵值對的清單。</span><span class="sxs-lookup"><span data-stu-id="b33dd-130">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="b33dd-131">-確認</span><span class="sxs-lookup"><span data-stu-id="b33dd-131">-Confirm</span></span>
<span data-ttu-id="b33dd-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b33dd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b33dd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b33dd-133">-WhatIf</span></span>
<span data-ttu-id="b33dd-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b33dd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b33dd-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b33dd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b33dd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b33dd-136">CommonParameters</span></span>
<span data-ttu-id="b33dd-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b33dd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b33dd-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b33dd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b33dd-139">輸入</span><span class="sxs-lookup"><span data-stu-id="b33dd-139">INPUTS</span></span>

## <span data-ttu-id="b33dd-140">輸出</span><span class="sxs-lookup"><span data-stu-id="b33dd-140">OUTPUTS</span></span>

### <span data-ttu-id="b33dd-141">ICommunicationServiceResource 中的 Api20200820Preview （）。</span><span class="sxs-lookup"><span data-stu-id="b33dd-141">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="b33dd-142">筆記</span><span class="sxs-lookup"><span data-stu-id="b33dd-142">NOTES</span></span>

<span data-ttu-id="b33dd-143">別名</span><span class="sxs-lookup"><span data-stu-id="b33dd-143">ALIASES</span></span>

## <span data-ttu-id="b33dd-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="b33dd-144">RELATED LINKS</span></span>

