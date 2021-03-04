---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: c96df19d110a795177d138b7ec34faefb72c0970
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905561"
---
# <span data-ttu-id="af3b3-101">Remove-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="af3b3-101">Remove-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="af3b3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="af3b3-102">SYNOPSIS</span></span>
<span data-ttu-id="af3b3-103">移除同步處理設定</span><span class="sxs-lookup"><span data-stu-id="af3b3-103">removes a synchronization setting</span></span>

## <span data-ttu-id="af3b3-104">語法</span><span class="sxs-lookup"><span data-stu-id="af3b3-104">SYNTAX</span></span>

### <span data-ttu-id="af3b3-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="af3b3-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af3b3-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="af3b3-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af3b3-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af3b3-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -InputObject <PSDataShareSynchronizationSetting> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af3b3-108">描述</span><span class="sxs-lookup"><span data-stu-id="af3b3-108">DESCRIPTION</span></span>
<span data-ttu-id="af3b3-109">**Remove-AzDataShareSynchronizationSetting** Cmdlet 會移除資料共用同步處理設定</span><span class="sxs-lookup"><span data-stu-id="af3b3-109">The **Remove-AzDataShareSynchronizationSetting** cmdlet removes a datashare synchronization setting</span></span>

## <span data-ttu-id="af3b3-110">例子</span><span class="sxs-lookup"><span data-stu-id="af3b3-110">EXAMPLES</span></span>

### <span data-ttu-id="af3b3-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="af3b3-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsShareSynchronizationSetting"

Are you sure you want to remove synchronization-setting "AdsShareSynchronizationSetting"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="af3b3-112">這個命令會從 Share AdsShare 移除名為 AdsShareSynchronizationSetting 的同步處理設定。</span><span class="sxs-lookup"><span data-stu-id="af3b3-112">This commands removes a synchronization setting named AdsShareSynchronizationSetting from share AdsShare.</span></span> 

## <span data-ttu-id="af3b3-113">參數</span><span class="sxs-lookup"><span data-stu-id="af3b3-113">PARAMETERS</span></span>

### <span data-ttu-id="af3b3-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="af3b3-114">-AccountName</span></span>
<span data-ttu-id="af3b3-115">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="af3b3-115">Azure Data Share Account name</span></span>

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

### <span data-ttu-id="af3b3-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af3b3-116">-AsJob</span></span>
<span data-ttu-id="af3b3-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="af3b3-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="af3b3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af3b3-118">-DefaultProfile</span></span>
<span data-ttu-id="af3b3-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="af3b3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af3b3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af3b3-120">-InputObject</span></span>
<span data-ttu-id="af3b3-121">Azure 資料共用同步處理設定。</span><span class="sxs-lookup"><span data-stu-id="af3b3-121">The Azure Data Share Synchronization setting.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af3b3-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="af3b3-122">-Name</span></span>
<span data-ttu-id="af3b3-123">同步處理設定名稱</span><span class="sxs-lookup"><span data-stu-id="af3b3-123">Synchronization setting name</span></span>

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

### <span data-ttu-id="af3b3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af3b3-124">-PassThru</span></span>
<span data-ttu-id="af3b3-125">如果指定 (，則) 。</span><span class="sxs-lookup"><span data-stu-id="af3b3-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="af3b3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af3b3-126">-ResourceGroupName</span></span>
<span data-ttu-id="af3b3-127">Azure 資料共用帳戶的資源組名</span><span class="sxs-lookup"><span data-stu-id="af3b3-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="af3b3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af3b3-128">-ResourceId</span></span>
<span data-ttu-id="af3b3-129">同步處理設定的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="af3b3-129">The resource id of the synchronization setting</span></span>

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

### <span data-ttu-id="af3b3-130">-ShareName</span><span class="sxs-lookup"><span data-stu-id="af3b3-130">-ShareName</span></span>
<span data-ttu-id="af3b3-131">Azure 資料共用名稱</span><span class="sxs-lookup"><span data-stu-id="af3b3-131">Azure data share name</span></span>

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

### <span data-ttu-id="af3b3-132">-確認</span><span class="sxs-lookup"><span data-stu-id="af3b3-132">-Confirm</span></span>
<span data-ttu-id="af3b3-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="af3b3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af3b3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af3b3-134">-WhatIf</span></span>
<span data-ttu-id="af3b3-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="af3b3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af3b3-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="af3b3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af3b3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af3b3-137">CommonParameters</span></span>
<span data-ttu-id="af3b3-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="af3b3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af3b3-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af3b3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af3b3-140">輸入</span><span class="sxs-lookup"><span data-stu-id="af3b3-140">INPUTS</span></span>

### <span data-ttu-id="af3b3-141">System.String</span><span class="sxs-lookup"><span data-stu-id="af3b3-141">System.String</span></span>

### <span data-ttu-id="af3b3-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="af3b3-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="af3b3-143">輸出</span><span class="sxs-lookup"><span data-stu-id="af3b3-143">OUTPUTS</span></span>

### <span data-ttu-id="af3b3-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="af3b3-144">System.Boolean</span></span>

## <span data-ttu-id="af3b3-145">筆記</span><span class="sxs-lookup"><span data-stu-id="af3b3-145">NOTES</span></span>

## <span data-ttu-id="af3b3-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="af3b3-146">RELATED LINKS</span></span>
