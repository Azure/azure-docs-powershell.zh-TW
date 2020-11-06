---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/stop-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: 01ca3c42db57760f23e49f93fc7e4d533b4047b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612620"
---
# <span data-ttu-id="ea5f8-101">Stop-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="ea5f8-101">Stop-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="ea5f8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ea5f8-102">SYNOPSIS</span></span>
<span data-ttu-id="ea5f8-103">停止對共用訂閱進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="ea5f8-103">Stops ongoing synchronization for a share subscription.</span></span> <span data-ttu-id="ea5f8-104">您可以透過其資源識別碼或其名稱來指定共用訂閱。</span><span class="sxs-lookup"><span data-stu-id="ea5f8-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="ea5f8-105">句法</span><span class="sxs-lookup"><span data-stu-id="ea5f8-105">SYNTAX</span></span>

### <span data-ttu-id="ea5f8-106">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ea5f8-106">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea5f8-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea5f8-107">ByResourceIdParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -SynchronizationId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea5f8-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea5f8-108">ByObjectParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea5f8-109">說明</span><span class="sxs-lookup"><span data-stu-id="ea5f8-109">DESCRIPTION</span></span>
<span data-ttu-id="ea5f8-110">**Stop-AzDataShareSubscriptionSynchronization** Cmdlet 會停止對共用訂閱進行同步處理</span><span class="sxs-lookup"><span data-stu-id="ea5f8-110">The **Stop-AzDataShareSubscriptionSynchronization** cmdlet stops ongoing synchronization for a share subscription</span></span>

## <span data-ttu-id="ea5f8-111">示例</span><span class="sxs-lookup"><span data-stu-id="ea5f8-111">EXAMPLES</span></span>

### <span data-ttu-id="ea5f8-112">範例1</span><span class="sxs-lookup"><span data-stu-id="ea5f8-112">Example 1</span></span>
```
PS C:\> Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationId 20a4416b-b33b-4539-a908-71dc8ef698fb

Confirm
AdsShareSubscription
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

durationMs        : 231869
endTime           : 
message           :
startTime         : 7/9/2019 11:40:53 PM
status            : Canceled
synchronizationId : 20a4416b-b33b-4539-a908-71dc8ef698fb
```

<span data-ttu-id="ea5f8-113">停止進行由識別碼識別的同步處理-20a4416b-b33b-4539-a908-71dc8ef698fb</span><span class="sxs-lookup"><span data-stu-id="ea5f8-113">Stops ongoing synchronization identified by id - 20a4416b-b33b-4539-a908-71dc8ef698fb</span></span>

## <span data-ttu-id="ea5f8-114">參數</span><span class="sxs-lookup"><span data-stu-id="ea5f8-114">PARAMETERS</span></span>

### <span data-ttu-id="ea5f8-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ea5f8-115">-AccountName</span></span>
<span data-ttu-id="ea5f8-116">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="ea5f8-116">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5f8-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea5f8-117">-AsJob</span></span>
<span data-ttu-id="ea5f8-118">{{Fill AsJob 描述}}</span><span class="sxs-lookup"><span data-stu-id="ea5f8-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="ea5f8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea5f8-119">-DefaultProfile</span></span>
<span data-ttu-id="ea5f8-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ea5f8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea5f8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea5f8-121">-InputObject</span></span>
<span data-ttu-id="ea5f8-122">Azure data share 訂閱物件</span><span class="sxs-lookup"><span data-stu-id="ea5f8-122">Azure data share subscription object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea5f8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea5f8-123">-ResourceGroupName</span></span>
<span data-ttu-id="ea5f8-124">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="ea5f8-124">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5f8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea5f8-125">-ResourceId</span></span>
<span data-ttu-id="ea5f8-126">Azure 共用訂閱的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ea5f8-126">The resource id of the azure share subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea5f8-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ea5f8-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="ea5f8-128">Azure 資料共用訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="ea5f8-128">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5f8-129">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="ea5f8-129">-SynchronizationId</span></span>
<span data-ttu-id="ea5f8-130">需要停止的同步處理 id</span><span class="sxs-lookup"><span data-stu-id="ea5f8-130">Synchronization id that needs to be stopped</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5f8-131">-確認</span><span class="sxs-lookup"><span data-stu-id="ea5f8-131">-Confirm</span></span>
<span data-ttu-id="ea5f8-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ea5f8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea5f8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea5f8-133">-WhatIf</span></span>
<span data-ttu-id="ea5f8-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ea5f8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea5f8-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ea5f8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea5f8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea5f8-136">CommonParameters</span></span>
<span data-ttu-id="ea5f8-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ea5f8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea5f8-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ea5f8-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea5f8-139">輸入</span><span class="sxs-lookup"><span data-stu-id="ea5f8-139">INPUTS</span></span>

### <span data-ttu-id="ea5f8-140">System.object</span><span class="sxs-lookup"><span data-stu-id="ea5f8-140">System.String</span></span>

### <span data-ttu-id="ea5f8-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="ea5f8-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="ea5f8-142">輸出</span><span class="sxs-lookup"><span data-stu-id="ea5f8-142">OUTPUTS</span></span>

### <span data-ttu-id="ea5f8-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="ea5f8-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="ea5f8-144">筆記</span><span class="sxs-lookup"><span data-stu-id="ea5f8-144">NOTES</span></span>

## <span data-ttu-id="ea5f8-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="ea5f8-145">RELATED LINKS</span></span>